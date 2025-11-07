# Cyfrowa Playlista w C#

Twoim zadaniem będzie stworzyć aplikację konsolową, która posłuży do zarządzania playlistą utworów muzycznych. Stworzysz obiekty reprezentujące piosenki, a następnie dodasz je do playlisty i wykonasz na nich różne operacje, takie jak obliczanie czasu trwania playlisty czy filtrowania utworów po gatunku. Przećwiczysz w ten sposób pętle, instrukcje warunkowe, a w zadaniu dodatkowym czeka na Ciebie małe wyzwanie - zaimplementowanie sortowania playlisty.

## Plan działania
### Struktura aplikacji
#### Utwór muzyczny
Stwórz klasę reprezentującą utwór muzyczny.

Musi on się składać przynajmniej z takich pól:
- string tytuł
- string wykonawca
- int dlugosc w sekundach
- string gatunek

##### Metoda ToString
W tej klasie nadpisz również metodę ToString (chodzi o override), która będzie wyświetlać informacje o utworze w przyjaznym dla użytkownika formacie.

Format wyświetlania:
Wykonawca - Tytuł (czas trwania w minutach i sekundach)

Przykład:
Lady Gaga - Telephone (3 min i 43 s)

Mała podpowiedź
Do zmiany sekund na minuty możesz użyć dzielenia, a potem modulo `%`.

#### Main
##### Funkcjonalności aplikacji
W metodzie Main zarządzaj playlistą utworów.
1. Stwórz playlistę

    Zadeklaruj tablicę, która będzie Twoją playlistą i która zmieści minimum 6 obiektów reprezentujących utwór.

2. Stwórz utwory
    
    Stwórz 6 różnych utworów (lub więcej, jeśli tablica może je pomieścić). Postaraj się nie zamykać na jeden gatunek muzyczny.

3. Wypełnij playlistę

    Umieść utwory w playliście

4. Wykonaj operacje na playliście

    Napisz kod, którego efektem będzie wyświetlanie w konsoli poniższych operacji:
    - wyświetl całą playlistę
    - oblicz całkowity czas trwania playlisty
    - wyświetl tylko utwory danego gatunku
    - znajdź i wyświetl najdłuższy utwór na playliście
    - znajdź i wyświetl najkrótszy utwór na playliście

## Zadanie dodatkowe

Zmodyfikuj program w taki sposób, aby potrafił sortować utwory alfabetycznie lub według długości. Obie funkcje i rosnąco i malejąco. Skup się na razie na jednej funkcji, np. rosnąco według długości, czyli od najkrótszego do najdłuższego.

![Vibe](cat-vibe.gif)