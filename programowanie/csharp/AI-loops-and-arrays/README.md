# Poziom Podstawowy: Pierwsze kroki z tablicami i pętlami
Te zadania mają na celu oswojenie się z podstawową składnią i najprostszymi operacjami.

## Zadanie 1: Suma elementów tablicy

### Cel: 
Przećwiczenie pętli for i dostępu do elementów tablicy.

### Treść:
Stwórz tablicę liczb całkowitych ( int[] ) i zainicjuj ją kilkoma wartościami, np. { 5, 10, 15, 20, 25 }.

Napisz program, który obliczy sumę wszystkich elementów w tej tablicy.
Wykorzystaj pętlę for do iteracji po tablicy.
Na końcu wyświetl obliczoną sumę w konsoli.

## Zadanie 2: Znajdowanie największego i najmniejszego elementu

### Cel: 
Użycie pętli i instrukcji warunkowych if do przeszukiwania tablicy.
### Treść:
Stwórz tablicę liczb całkowitych z co najmniej 5 różnymi wartościami.

Napisz program, który znajdzie największy oraz najmniejszy element w tej tablicy.

Podpowiedź: Zainicjuj zmienne `max` i `min` pierwszą wartością z tablicy, a następnie w pętli porównuj z kolejnymi elementami.

Wyświetl znalezione wartości.

## Zadanie 3: Wyświetlanie tablicy od tyłu

### Cel: 
Przećwiczenie manipulacji indeksem w pętli for.

### Treść:
Stwórz tablicę zawierającą kilka imion ( string[] ).
Napisz program, który wyświetli wszystkie elementy tablicy w odwrotnej kolejności, każdy w nowej linii.
Pamiętaj, że ostatni element tablicy ma indeks tablica.Length - 1.

## Zadanie 4: Liczenie liczb parzystych

### Cel: 
Połączenie pętli foreach z operatorem modulo (%).

### Treść:
Stwórz tablicę liczb całkowitych.
Napisz program, który policzy, ile w tablicy jest liczb parzystych.
Użyj pętli foreach do przejrzenia wszystkich elementów.
Podpowiedź: Liczba jest parzysta, jeśli reszta z jej dzielenia przez 2 jest równa 0 (liczba % 2 == 0).
Wariant rozszerzony: Program powinien liczyć i wyświetlać zarówno liczbę parzystych, jak i nieparzystych.

# Poziom Średniozaawansowany: Bardziej złożone operacje
Tutaj zadania wymagają nieco więcej logiki i operacji na danych.

## Zadanie 5: Kopiowanie i modyfikacja tablicy

### Cel: 
Praca z dwiema tablicami jednocześnie.

### Treść:
Stwórz tablicę A z kilkoma liczbami całkowitymi.
Stwórz drugą, pustą tablicę B o tym samym rozmiarze co A.

Napisz program, który skopiuje każdy element z tablicy A do tablicy B, ale z podwojoną wartością (każdy element w B ma być dwa razy większy niż odpowiadający mu element w A).

Na koniec wyświetl zawartość obu tablic, aby porównać wyniki.

#### Przykład:
Tablica A: { 1, 2, 3, 4 }

Tablica B po operacji: { 2, 4, 6, 8 }

## Zadanie 6: Wyszukiwanie elementu podanego przez użytkownika

### Cel: 
Interakcja z użytkownikiem i przeszukiwanie tablicy.

### Treść:
Stwórz tablicę liczb całkowitych.

Poproś użytkownika o podanie liczby, którą chce znaleźć w tablicy (użyj Console.ReadLine() i int.Parse()).

Napisz pętlę, która przeszuka tablicę.

Jeśli liczba zostanie znaleziona, wyświetl komunikat "Liczba X znajduje się w tablicy na indeksie Y." i zakończ działanie pętli (break).

Jeśli pętla zakończy się, a liczba nie zostanie znaleziona, wyświetl komunikat "Liczba X nie została znaleziona w tablicy.".

Podpowiedź: Użyj dodatkowej zmiennej typu bool (np. czyZnaleziono), aby śledzić, czy element został odnaleziony.

## Zadanie 7: Odwracanie tablicy w miejscu (in-place)

### Cel: 
Zrozumienie algorytmu zamiany elementów bez tworzenia nowej tablicy.
### Treść:
Stwórz tablicę liczb całkowitych.

Napisz program, który odwróci kolejność jej elementów, ale bez tworzenia drugiej, pomocniczej tablicy.

Podpowiedź: Użyj pętli, która iteruje tylko do połowy długości tablicy. W każdej iteracji zamieniaj ze sobą elementy symetryczne względem środka tablicy (np. pierwszy z ostatnim, drugi z przedostatnim itd.). Do zamiany będziesz potrzebować zmiennej tymczasowej.

#### Przykład:
Tablica przed: { 1, 2, 3, 4, 5 }

Tablica po: { 5, 4, 3, 2, 1 }

## Zadanie 8: Praca z tablicą dwuwymiarową (macierzą)

### Cel: 
Przećwiczenie pętli zagnieżdżonych i tablic 2D.
### Treść:
Stwórz tablicę dwuwymiarową (macierz) 3x3 typu int[,] i wypełnij ją dowolnymi liczbami.

Napisz program, który obliczy sumę elementów znajdujących się na głównej przekątnej macierzy (elementy, gdzie indeks wiersza jest równy indeksowi kolumny, tj. macierz[0,0], macierz[1,1], macierz[2,2]).
Wyświetl sumę.

Wariant rozszerzony: Oblicz sumę elementów na anty-przekątnej.

# Poziom Zaawansowany: Problemy algorytmiczne
Te zadania wymagają myślenia algorytmicznego i są świetnym wstępem do bardziej skomplikowanych problemów programistycznych.

## Zadanie 9: Sortowanie bąbelkowe (Bubble Sort)

### Cel: 
Implementacja jednego z najprostszych algorytmów sortowania.
### Treść:
Stwórz nieposortowaną tablicę liczb całkowitych.
Zaimplementuj algorytm sortowania bąbelkowego, aby posortować tablicę rosnąco.

#### Logika algorytmu:
Użyj zagnieżdżonych pętli.

Zewnętrzna pętla kontroluje liczbę przejść przez tablicę.

Wewnętrzna pętla porównuje sąsiednie elementy (tablica[j] i tablica[j+1]) i zamienia je miejscami, jeśli są w złej kolejności.

Po posortowaniu wyświetl zawartość tablicy.

#### Przykład:
Tablica przed: { 5, 1, 4, 2, 8 }

Tablica po: { 1, 2, 4, 5, 8 }

## Zadanie 10: Usuwanie duplikatów / Znajdowanie unikalnych wartości

### Cel: 
Praca z dynamiczną strukturą danych i filtrowanie tablicy.

### Treść:
Stwórz tablicę z powtarzającymi się wartościami, np. { 1, 2, 2, 3, 4, 4, 4, 5 }.

Napisz program, który stworzy nową tablicę zawierającą tylko unikalne elementy z oryginalnej tablicy.

Podpowiedź: Możesz iterować po oryginalnej tablicy i dla każdego elementu sprawdzać, czy już znajduje się w Twojej liście/tablicy wynikowej. Jeśli nie, dodaj go.

Wyświetl tablicę z unikalnymi wartościami.

## Zadanie 11: Sprawdzanie, czy tablica jest palindromem

### Cel:
Zastosowanie algorytmu porównawczego do weryfikacji symetrii.

### Treść:
Napisz program, który sprawdzi, czy dana tablica (np. liczb lub znaków) jest palindromem, czyli czy czyta się tak samo od początku do końca i od końca do początku.

Program powinien działać dla tablic o parzystej i nieparzystej liczbie elementów.

Podpowiedź: Podobnie jak w zadaniu 7, użyj pętli iterującej do połowy tablicy. W każdej iteracji porównuj symetryczne elementy. Jeśli jakakolwiek para się nie zgadza, tablica nie jest palindromem.

#### Przykłady:
{ 1, 2, 3, 2, 1 } -> Jest palindromem.

{ 'a', 'b', 'b', 'a' } -> Jest palindromem.

{ 1, 2, 3, 4, 5 } -> Nie jest palindromem.