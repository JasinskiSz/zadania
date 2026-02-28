# Kalkulator kosztów kafelkowania

Twoim zadaniem jest przygotowanie prostej strony internetowej, która pozwoli klientowi obliczyć szacunkowy koszt położenia kafelek w pomieszczeniu.

## Wymagania dotyczące struktury strony

Strona powinna zawierać następujące elementy umieszczone w sekcji body:

- Nagłówek pierwszego stopnia (h1) o treści: "Kalkulator Remontowy".
- Paragraf lub etykietę z napisem: "Podaj powierzchnię do wykafelkowania (m²):".
- Pole edycyjne (input typu numerycznego) do wprowadzania metrażu.
- Pole wyboru (checkbox) z opisem: "Dolicz koszt fugi i kleju".
- Przycisk (button) z napisem: "OBLICZ".
- Blok lub paragraf na wynik działania skryptu (początkowo pusty).

## Wymagania dotyczące wyglądu
Zdefiniuj prosty styl w osobnym pliku:

- Strona powinna mieć kolor tła jasnoszary - #E0E0E0
- Nagłówek h1 powinien być wyśrodkowany.
- Wynik działania skryptu powinien być wyświetlany pogrubioną czcionką w kolorze granatowym.

## Wymagania dotyczące skryptu
Skrypt powinien uruchamiać się po kliknięciu przycisku "OBLICZ" i realizować następującą logikę:

- Pobiera wartość wpisaną w pole powierzchni (metraż).
- Cena za 1 m² kafelkowania wynosi bazowo 70 PLN.
- Sprawdza, czy zaznaczono pole wyboru "Dolicz koszt fugi i kleju":
- Jeśli TAK: do ceny za metr należy doliczyć dodatkowe 15 PLN.
- Jeśli NIE: cena pozostaje bez zmian.
- Oblicza koszt całkowity.
- Wypisuje wynik w przygotowanym elemencie HTML w formacie:
`"Szacunkowy koszt remontu wynosi: [WYNIK] PLN"`

