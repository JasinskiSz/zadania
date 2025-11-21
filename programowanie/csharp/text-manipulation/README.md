# Ćwiczenia na tekście w C#, czyli manipulacja string

Mała ściąga przed startem:

- `.Length` - długość stringa,
- `.ToUpper()` / `.ToLower()` - zmiana wielkości liter,
- `.Trim()` - usuwanie spacji z "brzegów",
- `.Replace("a", "b")` - zamiana liter 'a' na 'b' w danym stringu,
- `.Contains("tekst")` - czy zawiera frazę z nawiasów,
- `.StartsWith()` / `.EndsWith()` - czy zaczyna/kończy się,
- `.Substring(start, długość)` - wycinanie fragmentu,
- `.Split(' ')` - dzielenie na stringa tablicę stringów.

## Zadanie 1: Statystyki tekstu
Napisz program, który poprosi użytkownika o wpisanie dowolnego zdania. Następnie wypisz:

- Długość tekstu (liczbę znaków).
- Tekst zapisany samymi wielkimi literami.
- Tekst zapisany samymi małymi literami.

Gdy ten etap się uda, rozszerz kod w taki sposób, aby wyświetlał tylko raz wpisany tekst - albo z wielkich liter, albo z małych. Pozwól userowi zdecydować który wariant ma się wyświetlić.

## Zadanie 2:  Długość tekstu i pierwsza/ostatnia litera
Napisz program, który wczyta od użytkownika dowolny tekst i wypisze:
- wpisany tekst bez spacji na końcu i początku tekstu
- długość tekstu,
- pierwszą literę,
- ostatnią literę.

### Przykład:

Wejście: `   Agnieszka` <- tutaj są spacje na początku stringa

Wyjście:
``` text
Wpisałeś: Agnieszka
Długość: 9
Pierwsza litera: A
Ostatnia litera: a
```