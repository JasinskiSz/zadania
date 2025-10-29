# Formularz na bazie zadania z INF-04
To zadanie bazuje na II części arkusza [INF.04-03-23.06-SG.pdf](./INF.04-03-23.06-SG.pdf) dostępnego do wglądu w tym samym repozytorium. 

W tym pliku znajdują się zdjęcia poglądowe formularza wykonanego w Angularze i React.js oraz tabela I wspomniana w dalszej części tego dokumentu.

## Cel
Wykonaj aplikację internetową typu front-end obsługującą formularz z zastosowaniem frameworka Angular lub biblioteki React. Zastosuj bibliotekę Bootstrap do zdefiniowania stylu formularza.

## Założenia aplikacji
- Aplikacja składa się z jednego komponentu formularza
- Formularz składa się z:
  - pola edycyjnego i jego etykiety o treści „Tytuł filmu”
  - listy rozwijalnej i jej etykiety o treści „Rodzaj"
  - przycisku „Dodaj” 
- Lista rozwijalna ma 5 opcji:
  - pustą 
  - Komedia o wartości 1 
  - Obyczajowy o wartości 2 
  - Sensacyjny o wartości 3 
  - Horror o wartości 4
- Aplikacja w stanie początkowym wyświetla puste pola formularza
- Po wybraniu przycisku „Dodaj” jest generowane zdarzenie, które ma za zadanie wypisanie danych 
z formularza w konsoli przeglądarki (w miejscu trzech kropek wartości pól formularza)
  - w Angular postaci: {tytul: ”...”, kategoria: ”...”} - obraz 1a
  - w React.js postaci: tytul: ...; rodzaj: ... - obraz 1b
  - (Obrazy dostępne w pliku [INF.04-03-23.06-SG.pdf](./INF.04-03-23.06-SG.pdf))
- Strona jest formatowana stylem: `body { padding: 20px; }`
- Elementy formularza są formatowane stylami biblioteki Bootstrap. Szablon HTML formularza należy 
zbudować sugerując się pomocą zamieszczoną w Tabeli 1 ([INF.04-03-23.06-SG.pdf](./INF.04-03-23.06-SG.pdf)). Należy zastosować znaczące nazwy dla 
identyfikatorów pól formularza.
- Aplikacja powinna być zapisana czytelnie, z zachowaniem zasad czystego formatowania kodu, należy 
stosować znaczące nazwy zmiennych i funkcji. 
- Dokumentacja do programu wykonana zgodnie z wytycznymi z części III zadania egzaminacyjnego.