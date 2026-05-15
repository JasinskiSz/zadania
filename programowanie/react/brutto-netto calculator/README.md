# Specyfikacja Techniczna: Kalkulator Wynagrodzenia Netto/Brutto
## 1. Cel projektu
Celem zadania jest implementacja interaktywnego kalkulatora płac w formie aplikacji jednostronicowej (SPA - Single Page Application). Aplikacja ma umożliwiać przeliczanie kwot brutto na netto w oparciu o aktualne wskaźniki podatkowe.

## 2. Wymagania Funkcjonalne
### Obsługa danych wejściowych:
* Pole numeryczne do wpisania kwoty wynagrodzenia brutto.
* Ograniczenie techniczne: blokada wprowadzania wartości ujemnych.
* Wybór rodzaju opodatkowania - Skala podatkowa i Podatek liniowy.
* Opcja do wyboru uwzględniająca status osoby uczącej się.

### Logika obliczeniowa:
* Przeliczanie wyników w czasie rzeczywistym po modyfikacji dowolnego pola wejściowego.
* Obliczanie poszczególnych składek: emerytalnej, rentowej oraz chorobowej.
* Wyliczanie zaliczki na podatek dochodowy.

### Prezentacja danych:
* Czytelne wyświetlenie końcowej kwoty netto.
* Zestawienie wszystkich składowych - poszczególnych składek i podatków - w formie listy.
* Formatowanie wszystkich kwot do dwóch miejsc po przecinku.

## 3. Wytyczne Techniczne
* Aplikacja powinna być podzielona na komponenty.
* Wykorzystanie semantycznego HTML5 oraz nowoczesnej składni JavaScript.
* Zastosowanie dowolnej metody stylowania w celu zapewnienia przejrzystości formularza.

## 4. Kryteria Akceptacji
* Wprowadzenie poprawnych danych wejściowych skutkuje natychmiastową aktualizacją wszystkich pól wynikowych.
* Brak błędów i ostrzeżeń w konsoli deweloperskiej podczas użytkowania aplikacji.
* Zgodność algorytmu obliczeniowego z aktualnymi stawkami podatkowymi oraz systemem ubezpieczeń społecznych obowiązującym w bieżącym roku podatkowym.
