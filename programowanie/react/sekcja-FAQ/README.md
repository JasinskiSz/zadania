# Sekcja FAQ
Zadanie polega na stworzeniu prostej, funkcjonalnej sekcji FAQ (Frequently Asked Questions - Najczęściej zadawane pytania). Pytania powinny wyświetlać się w formie listy z góry do dołu, gdzie każde pytanie można kliknąć, co powoduje rozwinięcie się pod pytaniem odpowiedzi.

## Opis funkcjonalności
- Wszystkie odpowiedzi są początkowo ukryte.
- W danym momencie widoczna może być tylko jedna odpowiedź. Kliknięcie na zwinięte pytanie powinno je rozwinąć, tym samym zwijając inne rozwinięte pytanie.
- Ponowne kliknięcie na to samo, już otwarte pytanie, powinno schować jego odpowiedź.

## Dane wejściowe
Przykładowe dane, które można, ale nie trzeba wykorzystać:

``` javascript
const data = [
  {
    id: 1,
    question: "Jakie są główne zalety Reacta?",
    answer: "React pozwala na tworzenie reużywalnych komponentów UI, wykorzystuje Virtual DOM dla lepszej wydajności i ma ogromną społeczność oraz ekosystem."
  },
  {
    id: 2,
    question: "Czym jest JSX?",
    answer: "JSX (JavaScript XML) to rozszerzenie składni JavaScript, które pozwala pisać kod przypominający HTML bezpośrednio w plikach JavaScript. Ułatwia to tworzenie i wizualizację struktury komponentów."
  },
  {
    id: 3,
    question: "Czym różni się state od props?",
    answer: "Props (properties) są przekazywane do komponentu z zewnątrz (od rodzica) i są niemutowalne (tylko do odczytu). State to wewnętrzne dane komponentu, które mogą się zmieniać w czasie i powodować ponowne renderowanie komponentu."
  },
  {
    id: 4,
    question: "Do czego służy hook useState?",
    answer: "Hook useState pozwala na dodanie stanu do komponentów funkcyjnych. Zwraca tablicę z dwiema wartościami: aktualną wartością stanu oraz funkcją, która pozwala na jego aktualizację."
  }
];
```