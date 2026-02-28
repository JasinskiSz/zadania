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

## Zadanie 5: Odwracanie tekstu

Napisz program, który wczyta od użytkownika tekst, a następnie wypisze go od tyłu.

### Przykład:
Wejście: `Programowanie`\
Wyjście: `einawomargorP`

Podpowiedź: Użyj pętli `for`, która zaczyna się od ostatniego indeksu `Length - 1` i schodzi do zera `i--`.

## Zadanie 6: Czy to palindrom?

Palindrom to wyraz, który czytany od przodu i od tyłu brzmi tak samo - np. "kajak".

Napisz program, który sprawdzi, czy podany tekst jest palindromem.

- Wczytaj tekst.
- Odwróć go (korzystając z logiki z Zadania 5).
- Porównaj oryginał z odwróconą wersją.
- Wypisz "TAK" lub "NIE", zależnie czy wpisany tekst jest palindromem.

### Zadanie 6.1
Spraw, aby program ignorował wielkość liter. Słowo `Kajak` też powinno być uznane za palindrom, pomimo pierwszej wielkiej litery.

### Zadanie 6.2
Ulepsz program tak, aby ignorował wielkość liter oraz spacje. Dzięki temu będzie w stanie poprawnie rozpoznać bardziej złożone palindromy.

#### Przykład:

Wejście: `Kobyła ma mały bok`\
Wyjście: `Zdanie "Kobyła ma mały bok" jest palindromem.`

Podpowiedź: Przed sprawdzeniem usuń spacje `.Replace(" ", "")` i zamień cały tekst na małe litery `.ToLower()`.

## Zadanie 7: Licznik słów

Napisz program, który policzy, z ilu słów składa się wpisane zdanie. Zakładamy, że słowa są oddzielone spacjami.

Podpowiedź: Użyj metody `.Split(' ')`, która zwróci tablicę słów, a następnie sprawdź długość tej tablicy za pomocą `.Length`. Pamiętaj o użyciu `.Trim()` przed podziałem, aby nie policzyć spacji na końcu jako słowa.

### Przykład:
Wejście: `Nauka programowania jest super`\
Wyjście: `Ilość słów: 4`

## Zadanie 8: Generator akronimów

Napisz program, który zamieni wpisane zdanie na akronim (skrótowiec utworzony z pierwszych liter słów). Skrót ma być wypisany wielkimi literami.

### Przykład:
Wejście: `Wielka orkiestra świątecznej pomocy`\
Wyjście: `WOŚP`

Rozszerzony przykład, w którym omijamy "of":\
Wejście: `United states of america`\
Wyjście: `USA`

Podpowiedź: Najpierw podziel tekst na słowa za pomocą `Split`, a potem w pętli pobieraj pierwszy znak z każdego słowa za pomocą np. `[0]`.

## Zadanie 9: Wyciąganie domeny z e-maila

Poproś użytkownika o podanie adresu e-mail. Program ma wypisać tylko to, co znajduje się po znaku `@`.

### Przykład:
Wejście: `jan.kowalski@gmail.com`\
Wyjście: `Domena: gmail.com`

Podpowiedź: Musisz znaleźć indeks znaku `@` np. przy użyciu `.IndexOf`, a następnie użyć `.Substring()`, zaczynając od pozycji o jeden większej niż indeks `@`.

## Zadanie 10: Cenzura
Napisz program, który wczyta od użytkownika zdanie. Następnie program powinien zastąpić wszystkie wystąpienia zakazanych słów ciągiem gwiazdek `*`. Słowa zakazane wymyśl i ustaw na sztywno w kodzie.

### Przykład
Wejście: `Mój kot jest szybszy niż twój pies.`\
Wyjście: `Mój *** jest szybszy niż twój ****.`
(Zakładajac, że kot i pies to słowa zakazane)

### Zadanie 10.1
Rozbuduj program tak, aby wczytał od użytkownika również listę słów zakazanych.

#### Przykład:
Wejście:
```
Podaj zdanie.
Mój kot jest szybszy niż twój pies.

Podaj słowa zakazane. Oddziel je pojedynczą spacją.
kot pies
```
Wyjście: `Mój *** jest szybszy niż twój ****.`

### Zadanie 10.2
Rozszerz program tak, aby cenzurował słowa niezależnie od wielkości liter (np. "Kot", "kOt", "KOT").

Podpowiedź: Możesz wielokrotnie wywołać `.Replace()` dla każdej kombinacji lub poszukać w dokumentacji C# przeciążenia metody `Replace`, które pozwala ignorować wielkość liter.

## Zadanie 11: Cenzura cyfr

Napisz program, który wczyta tekst zawierający litery i cyfry. Program ma wypisać tekst, w którym każda cyfra została zamieniona na słowo "LICZBA".

### Przykład:
Wejście: `Mam 2 koty i 3 psy`
Wyjście: `Mam LICZBA koty i LICZBA psy`

### Zadanie 11.1
Zamiast zamieniać wszystkie cyfry na to samo słowo, zamieniaj je na słowa odpowiadające cyfrom, np. 1 -> "jeden", 2 -> "dwa".

## Zadanie 12: Wyszukiwarka w tekście

Napisz program, który:

1. Wczyta długi tekst (np. artykuł lub zdanie).
2. Wczyta słowo szukane przez użytkownika.
3. Sprawdzi, czy słowo występuje w tekście `.Contains`.
4. Jeśli tak – wypisze indeks, pod którym to słowo się zaczyna `.IndexOf`.

### Przykład:
Tekst: `Ala ma kota i psa`\
Szukane: `kota`\
Wyjście: `Znaleziono na indeksie: 7`

## Zadanie 13: Formatowanie imienia i nazwiska

Czasami użytkownicy wpisują dane niedbale, np. "jan kOWALski".

Napisz program, który wczyta imię i nazwisko w jednej linii, oddzielone spacją i poprawi je tak, aby:
- Pierwsza litera imienia była duża, reszta mała.
- Pierwsza litera nazwiska była duża, reszta mała.

### Przykład:
Wejście: `jAN koWALski`\
Wyjście: `Jan Kowalski`

Podpowiedź: Rozdziel stringa na dwa elementy. Dla każdego elementu: weź pierwszą literę -> `ToUpper()`, weź resztę `Substring(1) -> ToLower()`, a potem połącz je z powrotem.

## Zadanie 14: "SpongeBob Case" - Przeplatanie liter

Napisz program, który zmienia wielkość liter w zdaniu naprzemiennie: mała, duża, mała, duża... Spacje ignorujemy lub traktujemy jak znak - według uznania.

### Przykład:
Wejście: `Dzień dobry`
Wyjście: `dZiEń dObRy`

Podpowiedź: Użyj pętli `for`. Jeśli indeks `i` jest parzysty (`i % 2 == 0`), zmień literę na małą, a jeśli nieparzysty - na dużą.

## Zadanie 15: Odwracanie kolejności słów

Napisz program, który wczyta zdanie, a następnie wyświetli je z odwróconą kolejnością słów.

### Przykład:
Wejście: `Niebieski wieloryb płynie wolno`
Wyjście: `wolno płynie wieloryb Niebieski`

Podpowiedź: Użyj `.Split(' ')`, aby podzielić zdanie na tablicę słów. Następnie użyj pętli `for` idącej od końca tablicy do początku, aby zbudować nowy string.

## Zadanie 16: Prosty parser CSV

Dane w formacie CSV ([Comma-Separated Values](https://en.wikipedia.org/wiki/Comma-separated_values) lub dla niketórych czasami [Delimeter-Separated Values](https://en.wikipedia.org/wiki/Delimiter-separated_values)) to popularny sposób zapisu danych tabelarycznych w plikach tekstowych. Każdy wiersz to rekord, a wartości są oddzielone przecinkami.

Napisz program, który wczyta od użytkownika pojedynczą linię w formacie `Imię,Nazwisko,Wiek` i wyświetli te dane w przyjaznej formie.

### Przykład:
Wejście: `Anna,Nowak,31`

Wyjście:
```text
Imię: Anna
Nazwisko: Nowak
Wiek: 31
```

### Zadanie 16.1
Dodaj walidację. Jeżeli użytkownik poda dane w niepoprawnym formacie - np. bez dwóch przecinków, program powinien wyświetlić komunikat błędu.

## Zadanie 17: Liczenie samogłosek i spółgłosek

Napisz program, który wczyta zdanie i policzy, ile jest w nim samogłosek, a ile spółgłosek. Zignoruj cyfry, spacje i znaki interpunkcyjne.

### Przykład:
Wejście: `To jest test.`

Wyjście:
```text
Liczba samogłosek: 3
Liczba spółgłosek: 6
```

Podpowiedź: Stwórz stringa lub tablicę zawierającą wszystkie samogłoski `"aeiouy"`. W pętli przechodzącej po każdym znaku w tekście wejściowym sprawdzaj:
- Czy znak jest literą char.IsLetter().
- Jeśli tak, to czy znajduje się w zbiorze samogłosek np. za pomocą `Contains(litera)`.

## Zadanie 18: Szyfr Cezara

Szyfr Cezara to prosta technika szyfrowania, w której każda litera w tekście jest zastępowana literą oddaloną o stałą liczbę pozycji w alfabecie.

Napisz program, który:
1. Wczyta tekst do zaszyfrowania.
2. Wczyta liczbę (czyli klucz), o którą należy przesunąć litery.
3. Zaszyfruje tekst i go wyświetli. Program powinien zawijać alfabet, czyli po 'z' następuje 'a'.

### Przykład:
Wejście:
```text
Tekst: abc
Klucz: 2
Wyjście: cde
```

Wejście:
```text
Tekst: xyz
Klucz: 3
Wyjście: abc
```