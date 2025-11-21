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

## Zadanie 1: Zamiana wielkości liter
Napisz program, który poprosi użytkownika o wpisanie dowolnego zdania. Następnie wypisz:

- Długość tekstu (liczbę znaków).
- Tekst zapisany samymi wielkimi literami.
- Tekst zapisany samymi małymi literami.

### Zadanie 1.1:
Gdy ten etap się uda, rozszerz kod w taki sposób, aby wyświetlał tylko raz wpisany tekst - albo z wielkich liter, albo z małych. Pozwól userowi zdecydować który wariant ma się wyświetlić.

### Zadanie 1.2:
Następnie dodaj opcję wyświetlania tekstu, w którym tylko pierwsza litera jest wielka, a reszta małe.

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

## Zadanie 3: Liczenie wystąpień znaku
Napisz program, który wczyta cały tekst, a potem wczyta jeden znak (np. literę) do wyszukania.

Następnie funkcją programu będzie policzenie, ile razy ten znak występuje w tekście.

### Przykład:
Wejście:
```
Tekst: banana
Znak: a
```

Wyjście: 
```
Litera 'a' występuje 3 razy.
```

Podpowiedź: pętla `for` po `text[i]`.

## Zadanie 4: Zamiana spacji na podkreślniki
Napisz program, który:

1. Wczyta zdanie.
2. Zastąpi wszystkie spacje znakiem `_`.
3. Wypisze zmieniony tekst.

### Przykład:
Wejście: `Ala ma kota`
Wyjście: `Ala_ma_kota`

### Zadanie 4.1
Pozwól użytkownikowi wybrać znak, na który ma zamienić spację

### Zadanie 4.2
Skoro użytkownik wybiera znak, na który mają być zamienione spacje, dlaczego by nie pozwolić mu wybierać też drugiego znaku zamiast na sztywno ustawione mieć spacje?