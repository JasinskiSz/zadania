## Etap 1: Pierwsze kroki – Klasy, Pola i Metody

### Zadanie 1: Pierwsza Klasa
- Stwórz nowy projekt konsolowy.
- Dodaj nową klasę o nazwie `Samochod`.
- Wewnątrz klasy dodaj dwa pola publiczne: `string Marka` oraz `int RokProdukcji`.
- W pliku `Program.cs` utwórz obiekt tej klasy. Przypisz mu markę "Fiat" i rok 2010.
- Wypisz te dane na konsolę.

### Zadanie 2: Pierwsza Metoda

- Do klasy `Samochod` dodaj metodę publiczną `void Jedz()`, która wypisuje na konsolę tekst: "Brum brum!".
- W `Program.cs` wywołaj tę metodę na utworzonym wcześniej obiekcie.

### Zadanie 3: Wiele Obiektów

- Stwórz dwa różne obiekty klasy `Samochod` (np. auto1 i auto2) w pliku `Program.cs`
- Przypisz im różne marki i roczniki (np. BMW i Audi).
- Wypisz dane obu samochodów, aby udowodnić, że przechowują one własne, niezależne dane.

### Zadanie 4: Metoda z parametrami

- Stwórz nową klasę `Kalkulator`.
- Dodaj metodę `int Dodaj(int a, int b)`, która zwraca sumę dwóch liczb.
- W `Program.cs` stwórz obiekt kalkulatora, wywołaj metodę, przekaż jej dwie liczby, a wynik zapisz do zmiennej i wyświetl na ekranie.

### Zadanie 5: Przechowywanie stanu

- Stwórz klasę `KontoBankowe`.
- Dodaj pole publiczne `decimal Saldo` zainicjowane wartością `0`.
- Dodaj metodę `void Wplac(decimal kwota)`, która zwiększa saldo o podaną kwotę.
- W `Program.cs` wpłać pieniądze trzy razy i wyświetl końcowe saldo.

### Zadanie 6: Rozbudowa Samochodu
- W klasie `Samochod` dodaj pole `int Predkosc` (początkowo 0).
- Dodaj metodę `void Przyspiesz()`, która zwiększa prędkość o 10 km/h.
- Dodaj metodę `void Hamuj()`, która zmniejsza prędkość o 10. Dodaj w niej instrukcję warunkową, aby nie pozwolić prędkości spaść poniżej 0.
- W `Program.cs` rozpędź auto, wypisz jego prędkość, a potem spróbuj wyhamować poniżej zera i sprawdź wynik.

### Zadanie 7: Logika w Banku
- W klasie `KontoBankowe` dodaj metodę `bool Wyplac(decimal kwota)`. Logika metody:
  - Jeśli `Saldo` jest większe lub równe kwocie: odejmij kwotę od salda i zwróć true (oznaczając operację jako udaną).
  - W przeciwnym razie: wypisz "Brak środków" i zwróć false.
- W `Program.cs` spróbuj wypłacić więcej pieniędzy, niż wpłaciłeś w jednym z poprzednich zadań.

### Zadanie 8: Użycie Kalkulatora do obliczeń
To zadanie połączy klasy w `Program.cs`.

Załóżmy, że chcemy obliczyć koszt paliwa na wycieczkę.
- Do klasy `Kalkulator` dodaj metodę `double Mnozenie(double a, double b)`.

W `Program.cs`:
- Zdefiniuj zmienną `double cenaPaliwa = 6.5`.
- Zdefiniuj zmienną `double litry = 20`.
- Użyj obiektu `Kalkulator` (stworzonego w jednym z poprzednich zadań), aby pomnożyć te liczby.
- Jeśli operacja `Wyplac` na kwotę obliczoną przez kalkulator się udała, wypisz: "Zatankowano samochód [Marka]!".