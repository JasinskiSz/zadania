# Mission Control Manager
Twoim zadaniem jest stworzenie systemu do zarządzania misjami kosmicznymi. Będziesz przechowywać informacje o każdej misji, zarządzać jej załogą, ładunkiem i celami badawczymi.

## Opis struktury danych

Wyobraź sobie, że każda misja jest reprezentowana przez obiekt o następującej strukturze:

```javascript
const misja = {
    nazwa: "Ekspedycja na Marsa",
    typ: "Badawcza", // Inne typy: "Transportowa", "Kolonizacyjna"
    zaloga: ["kpt. Nowak", "dr Kowalska"],
    dystans: 0, // w jednostkach astronomicznych (AU)
    celeBadawcze: ["Analiza próbek gleby", "Poszukiwanie wody"],
    ladownia: {
        narzedzia: ["Spektrometr", "Wiertło geologiczne"],
        zapasy: 100 // można oznaczać np. procent dostępnych zapasów
    }
}
```
## Funkcje do zaimplementowania
Twoim zadaniem jest stworzenie funkcji, które będą zarządzać tymi misjami. Poniżej znajdują się wymagania dotyczące funkcji, które musisz zaimplementować:
- `zaplanujMisje(misja)`: Dodaje nową misję do systemu.
- `dodajCzlonkaZalogi(nazwaMisji, czlonek)`: Dodaje członka załogi do określonej misji.
- `zaladujSprzet(nazwaMisji, sprzet)`: Dodaje sprzęt do ładowni misji.
- `przemierzDystans(nazwaMisji, odleglosc)`: Aktualizuje dystans przebytej misji.
- `raportMisji(nazwaMisji)`: Zwraca szczegółowy raport o misji.

## Przykładowe użycie

Tak powinno wyglądać przykładowe użycie Twoich funkcji:

```javascript
// Tworzenie nowej misji
const misjaAlfa = zaplanujMisje("Projekt Feniks", "Kolonizacyjna");

// Personalizacja misji
if (misjaAlfa) {
    dodajDoZalogi(misjaAlfa, "Specjalista ds. komunikacji");
    zaladujSprzet(misjaAlfa, "Generator tlenu");
    zaladujSprzet(misjaAlfa, "Drukarka 3D");

    // Postęp misji
    przemierzDystans(misjaAlfa, 10);
    przemierzDystans(misjaAlfa, 5);

    // Wygenerowanie końcowego raportu
    console.log(raportMisji(misjaAlfa));
}

// Przykład walidacji
const nieudanaMisja = zaplanujMisje("Test", "Badawcza"); // Powinien wyświetlić błąd i zwrócić null
```

## Oczekiwany wynik
Dla raportMisji("Ekspedycja na Marsa") wynik powinien wyglądać mniej więcej tak:
```txt
*** RAPORT MISJI: Ekspedycja na Marsa ***
Typ misji: Badawcza
Przebyty dystans: 15 AU
Pozostałe zapasy: 270%

--- ZAŁOGA ---
- Inżynier
- Medyk
- Biolog
- Pilot
- Architekt
- Specjalista ds. komunikacji

--- SPRZĘT W ŁADOWNI ---
- Moduł mieszkalny
- Generator tlenu
- Drukarka 3D
```

## Rozszerzenia dla ambitnych
Jeśli uporasz się z główną częścią zadania, spróbuj dodać jedną z poniższych funkcjonalności (na dodatkową ocenę!):

- Awarie systemów: Stwórz funkcję symulujAwarie(misja), która ma 25% szansy na losowe usunięcie jednego narzędzia z ładowni lub zmniejszenie zapasów o 50. (Wskazówka: użyj Math.random()).
- Zarządzanie celami: Dodaj funkcję ukonczCel(misja, cel), która usuwa dany cel z tablicy celeBadawcze.
- Wiele misji: Zmodyfikuj kod tak, abyś mógł przechowywać wszystkie stworzone misje w jednej tablicy o nazwie flota i napisz funkcję, która generuje raport dla całej floty.

Powodzenia, kosmiczny kadecie! To zadanie to świetna okazja, aby ugruntować swoją wiedzę i poczuć się pewniej w posługiwaniu się podstawowymi strukturami danych i funkcjami w JavaScript.

![Buzz](buzz.gif)