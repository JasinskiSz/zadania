# Kalkulator rachunku z napiwkiem i rabatem
Program ma policzyć końcową kwotę do zapłaty w restauracji na podstawie:
- liczby pozycji na rachunku,
- cen tych pozycji,
- ewentualnego rabatu,
- napiwku zależnego od jakości obsługi.

## Wymagania
Zapytaj użytkownika o liczbę pozycji na rachunku (np. 3).
- To ma być liczba całkowita `int` i powinna być większa od 0.

W pętli wczytaj ceny każdej pozycji:
- Dla n-tej pozycji wyświetl: Podaj cenę pozycji #n:
- Cena powinna być liczbą typu `decimal`.
- Cena nie może być ujemna.
- Policz sumę wszystkich cen.

Zapytaj o rabat:
np. zadaj pytanie: Czy masz rabat? (t/n - użyj typu danych `char`):
Jeśli t, to zapytaj o procent rabatu (np. 10 oznacza 10%).
Rabat ma być w zakresie 0–50.

Zapytaj o jakość obsługi (ustali napiwek):
- np. 1 - słaba (0%), 2 - ok (10%), 3 - dobra (15%), 4 - świetna (20%)
Użyj `switch` albo `if/else` do dobrania procentu napiwku.

Wylicz i wyświetl podsumowanie:
- suma przed rabatem
- kwota rabatu
- suma po rabacie
- kwota napiwku
- kwota do zapłaty (po rabacie + napiwek)
- Formatowanie do 2 miejsc po przecinku.

Na końcu zapytaj czy liczyć jeszcze raz i użyj pętli `while`.