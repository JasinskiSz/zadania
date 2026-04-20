## Zadanie 1: Kalkulator kosztów paliwa
Wymagania dotyczące skryptu:
- Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
- Pobiera wartość liczbową z pola edycyjnego określającą ilość litrów paliwa.
- Odczytuje wybrany przez użytkownika rodzaj paliwa za pomocą przycisków opcji (radio): benzyna lub olej napędowy po wciśnięciu przycisku "Oblicz"
- Oblicza koszt na podstawie cen: benzyna – 5 zł/l, olej napędowy – 6 zł/l.
- Wyświetla w paragrafie pod przyciskiem tekst: "Koszt paliwa: [wynik] zł", gdzie [wynik] jest obliczoną wartością.

## Zadanie 2: Formularz zmiany wyglądu tekstu
Wymagania dotyczące skryptu:
- Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
- Po kliknięciu w jeden z trzech przycisków (Czerwony, Zielony, Niebieski) zmienia kolor czcionki w wyznaczonym bloku tekstu na odpowiadający nazwie przycisku.
- Pobiera wartość z suwaka (pole typu range) i na jej podstawie dynamicznie zmienia rozmiar czcionki (fontSize) w tym samym bloku tekstu.
- Zmiana rozmiaru czcionki powinna zachodzić natychmiast po przesunięciu suwaka (zdarzenie oninput lub onchange).

## Zadanie 3: Weryfikacja siły hasła
Wymagania dotyczące skryptu:
- Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
- Pobiera ciąg znaków z pola typu password.
- Sprawdza następujące warunki i wyświetla odpowiedni komunikat w paragrafie pod formularzem:
    - Jeśli pole jest puste: "Wpisz hasło".
    - Jeśli hasło ma długość od 1 do 6 znaków: "Hasło jest słabe".
    - Jeśli hasło ma 7 i więcej znaków oraz zawiera przynajmniej jedną cyfrę: "Hasło jest dobre".
- Kolor tekstu komunikatu dla hasła dobrego powinien zmienić się na zielony, a dla pozostałych przypadków pozostać czerwony.

## Zadanie 4: Dynamiczne generowanie listy usług
Wymagania dotyczące skryptu:
- Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
- Definiuje tablicę jednowymiarową zawierającą nazwy pięciu usług serwisowych (np. Naprawa, Przegląd, Czyszczenie, Wymiana, Diagnostyka).
- Wykonywany automatycznie po załadowaniu całej struktury dokumentu HTML.
- Tworzy dynamicznie elementy listy punktowanej `<li>` dla każdego elementu tablicy.
- Dodaje utworzone elementy do istniejącego w dokumencie znacznika listy wypunktowanej `<ul>`.
