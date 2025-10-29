# System Zarządzania Dostawami i Magazynem w Centrum Logistycznym (CL)

Stwórz system decyzyjny dla centrum logistycznego, który zarządza przyjmowaniem towarów, alokacją miejsca w magazynie oraz planowaniem wysyłek. System musi podejmować decyzje na podstawie wielu kryteriów logistycznych.

## Część I - tworzenie zmiennych
Stwórz zmienne, reprezentujące następujące cechy o:

1. dostawie:
- rodzaj - jedno z: EXPRESS, STANDARD, ECONOMY
- waga - w kg
- objętość - w m³
- czy delikatna
- czy wymaga chłodzenia
- liczba palet
- odległość dostawy - w km

2. magazynie:
- obecnie dostępne miejsce paletowe
- maksymalny udźwig
- czy posiada chłodnie
- ilość aktualnie dostępnych pracowników
- czy jest teraz weekend
- aktualna godzina (bez minut)

3. transporcie:
- czy ciężarówka jest dostępna
- czy van jest dostępny
- cena paliwa za litr
- czy posiada ADR (licencję na towary niebezpieczne)

## Część II - instrukcje warunkowe

Sprawdź czy można przyjąć dostawę, zakładając następujące warunki:
- Jest miejsce w magazynie AND
- Waga nie przekracza max udźwigu AND
- Jeśli wymaga chłodzenia to chłodnia musi być dostępna AND
- Magazyn jest otwarty (godziny np. 6-22 LUB typ EXPRESS)

Wybór strefy magazynowej - określ strefę:
- Strefa A: delikatne LUB wymaga chłodzenia
- Strefa B: waga > 500kg ORAZ NIE delikatne
- Strefa C: objętość > 10m³ ORAZ waga < 500kg
- Strefa D: pozostałe
Dodatkowo: jeśli to weekend ORAZ nie EXPRESS, dodaj "_TEMP" do strefy

Oblicz koszt obsługi na podstawie warunków:
- Koszt podstawowy = 100 PLN
- Jeśli delikatne: +50% do kosztu
- Jeśli wymaga chłodzenia: +30% do kosztu
- Jeśli EXPRESS ORAZ odległość > 300km: +100% do kosztu
- Jeśli weekend ORAZ NIE ma 3 pracowników: +200 PLN
- Jeśli godzina między 22-6: tarfya nocna +40%

Dokonaj wyboru środka transportu na podstawie cech przesyłki:
- Van: waga < 1000kg ORAZ objętość < 15m³ ORAZ odległość < 200km
- Ciężarówka: waga >= 1000kg LUB objętość >= 15m³ LUB odległość >= 200km
- Dodatkowo sprawdź dostępność wybranego pojazdu
- Jeśli paliwo > 7 PLN/l ORAZ odległość > 500km ORAZ NIE EXPRESS -> odłóż na jutro

Ustal priorytet (1-najwyższy, 5-najniższy):
- Priorytet 1: EXPRESS ORAZ (delikatne LUB wymaga chłodzenia)
- Priorytet 2: EXPRESS LUB (odległość > 400km ORAZ dzień roboczy)
- Priorytet 3: delikatne ORAZ NIE EXPRESS
- Priorytet 4: STANDARD ORAZ waga < 100kg
- Priorytet 5: pozostałe

Kompleksowa walidacja i finalna decyzja, czy przesyłka może być zrealizowana dzisiaj. Jeżeli:
- przyjęta do magazynu ORAZ transport dostępny ORAZ 
- priorytet <= 3 LUB liczba pracowników >= 4
LUB
- typ EXPRESS ORAZ NIE weekend
ORAZ NIE
- godzina > 20 ORAZ odległość > 300km ORAZ NIE EXPRESS

Na sam koniec generowanie raportu dla pracowników, tj. na podstawie wszystkich warunków wygeneruj szczegółowe instrukcje dla dostawy.