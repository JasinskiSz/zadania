## Etap 1: Pierwsze kroki – Klasy, Pola i Metody

### Zadanie 1: Pierwsza Klasa
- Stwórz nowy projekt konsolowy.
- Dodaj nową klasę o nazwie `Samochod`.
- Wewnątrz klasy dodaj dwa pola publiczne: `string Marka` oraz `int RokProdukcji`.
- W pliku `Program.cs` utwórz obiekt tej klasy. Przypisz mu markę "Fiat" i rok 2010.
- Wypisz te dane na konsolę.

### Zadanie 2: Pierwsza Metoda

- Do klasy `Samochod` dodaj metodę publiczną `void Jedz()`, która wypisuje na konsolę tekst: "Brum brum!".
- W Program.cs wywołaj tę metodę na utworzonym wcześniej obiekcie.

### Zadanie 3: Wiele Obiektów

- Stwórz dwa różne obiekty klasy Samochod (np. auto1 i auto2) w pliku `Program.cs`
- Przypisz im różne marki i roczniki (np. BMW i Audi).
- Wypisz dane obu samochodów, aby udowodnić, że przechowują one własne, niezależne dane.

### Zadanie 4: Metoda z parametrami

- Stwórz nową klasę Kalkulator.
- Dodaj metodę `int Dodaj(int a, int b)`, która zwraca sumę dwóch liczb.
- W `Program.cs` stwórz obiekt kalkulatora, wywołaj metodę, przekaż jej dwie liczby, a wynik zapisz do zmiennej i wyświetl na ekranie.

### Zadanie 5: Przechowywanie stanu

- Stwórz klasę KontoBankowe.
- Dodaj pole publiczne `decimal Saldo` zainicjowane wartością `0`.
- Dodaj metodę `void Wplac(decimal kwota)`, która zwiększa saldo o podaną kwotę.
- W `Program.cs` wpłać pieniądze trzy razy i wyświetl końcowe saldo.