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