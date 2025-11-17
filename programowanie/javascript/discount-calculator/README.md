# Kalkulator obniżki cenowej
Stwórz prostą aplikację, która obliczy cenę produktu po rabacie. Po podaniu przez użytkownika ceny i procentu zniżki, aplikacja powinna wyświetlać:
- Cenę po rabacie
- Kwotę zaoszczędzoną (różnica cen przed i po obniżce)

Dodatkowo aplikację można rozbudować o:
- Wyświetlanie paska postępu, który wizualizuje oszczędności

## Wymagania
- Pola do wprowadzania wartości przez użytkownika:
  - Cena początkowa
  - Procent zniżki - liczba od 0 do 100
  - przycisk "oblicz zniżkę"

Po kliknięciu przycisku aplikacja ma wyświetlać pożądane informacje na stronie.

Po poprawnym wykonaniu powyższych wymagań zajmij się walidacjami inputu użytkownika. Zaimplementuj następujące sprawdzenia:
- cena musi być większa od 0
- rabat musi być między 0 a 100

Następnie jeśli to już będzie trybić, dodaj wizualny [pasek postępu](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/progress), który ma pokazywać graficznie ile procent ceny to rabat.

A teraz spróbuj dodać jeszcze kolejne pole `ilość sztuk`. Po wypełnieniu go aplikacja powinna brać pod uwagę całkowitą oszczędność przy zakupie tylu sztuk - wtedy input na cenę oznacza cenę jednego przedmiotu.

Jeżeli już nawet to uda Ci się zrobić, wyświetl w przeglądarce historię obliczeń, np. 3 ostatnie obliczenia.