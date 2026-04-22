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

### Zadanie 5: Kalkulator potęg
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Pobiera z dwóch pól edycyjnych podstawę oraz wykładnik potęgi.
− Jeśli oba pola są wypełnione, oblicza wynik potęgowania.
− W przypadku pozostawienia pustych pól, wyświetla komunikat: "Wpisz obie liczby".
− Wyświetla w bloku wynikowym tekst: "Wynik potęgowania: [wynik]".

### Zadanie 6: Przelicznik jednostek temperatury
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Pobiera wartość temperatury w stopniach Celsjusza z pola numerycznego.
− Po kliknięciu przycisku "Na Kelwiny", wyświetla wynik obliczony według wzoru: K = C + 273.15.
− Po kliknięciu przycisku "Na Fahrenheity", wyświetla wynik według wzoru: F = (C * 9/5) + 32.
− Wynik zaokrągla do dwóch miejsc po przecinku i wyświetla w paragrafie o id "temp-wynik".

### Zadanie 7: Generator listów powitalnych
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Pobiera imię z pola tekstowego oraz płeć z listy rozwijalnej.
− Po kliknięciu przycisku generuje tekst: "Witaj Pani [Imię]!" dla kobiet lub "Witaj Panie [Imię]!" dla mężczyzn.
− Cały tekst powinien zostać wyświetlony wielkimi literami.

### Zadanie 8: Wybór opcji dostawy
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Pobiera wartość zamówienia z pola edycyjnego.
− Odczytuje stan pola typu checkbox o nazwie "Dostawa ekspresowa" (koszt dodatkowy 15 zł).
− Oblicza sumę końcową: wartość zamówienia + ewentualny koszt dostawy.
− Wyświetla w paragrafie tekst: "Do zapłaty: [suma] zł".

### Zadanie 9: Zamiana obrazów (Galeria)
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Posiada trzy przyciski z nazwami kolorów: "Widok 1", "Widok 2", "Widok 3".
− Kliknięcie w przycisk zmienia atrybut src głównego obrazu na stronie (np. na pliki "1.jpg", "2.jpg", "3.jpg").
− Pod obrazem wyświetla tekst odpowiadający nazwie aktualnie wyświetlanego pliku.

### Zadanie 10: Obliczanie pola powierzchni koła
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Pobiera promień koła z pola edycyjnego.
− Sprawdza, czy podana wartość jest liczbą dodatnią; jeśli nie, wyświetla błąd: "Podaj liczbę dodatnią".
− Oblicza pole powierzchni (P = πr²) wykorzystując stałą Math.PI.
− Wyświetla wynik w paragrafie, zaokrąglając go w dół do najbliższej liczby całkowitej.

### Zadanie 11: Formatowanie treści przez użytkownika
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Pobiera tekst z pola textarea.
− Posiada dwa przyciski: "Kursywa" oraz "Pogrubienie".
− Kliknięcie przycisku nakłada odpowiedni styl CSS (.style.fontStyle lub .style.fontWeight) na paragraf wyświetlający wpisany tekst.

### Zadanie 12: Walidacja wieku
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Pobiera rok urodzenia z pola numerycznego.
− Oblicza wiek użytkownika na podstawie bieżącego roku (wpisanego na sztywno w kodzie lub pobranego z systemu).
− Jeśli wiek jest mniejszy niż 18, wyświetla: "Osoba niepełnoletnia", w przeciwnym razie: "Zapraszamy do rejestracji".

### Zadanie 13: Prosty kalkulator BMI
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Pobiera masę ciała w kg oraz wzrost w cm.
− Przelicza wzrost na metry i oblicza BMI według wzoru: masa / (wzrost^2).
− Wyświetla wartość BMI oraz interpretację: "Niedowaga" (poniżej 18.5), "Waga prawidłowa" (18.5 - 24.9), "Nadwaga" (powyżej 25).

### Zadanie 14: Dynamiczna zmiana tła sekcji
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Pobiera wartość koloru z pola typu "color".
− Po zmianie wartości w polu (zdarzenie oninput), ustawia wybrany kolor jako tło (backgroundColor) dla wyznaczonego bloku artykułu.
− Wewnątrz bloku wypisuje kod HEX wybranego koloru.

### Zadanie 15: Licznik znaków w polu tekstowym
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Na bieżąco zlicza znaki wpisywane do pola textarea.
− Wyświetla informację: "Liczba znaków: [X]/200".
− Jeśli liczba znaków przekroczy 200, zmienia kolor licznika na czerwony i blokuje możliwość wpisywania dalszego tekstu lub wyświetla komunikat o błędzie.

### Zadanie 16: Losowanie liczb z zakresu
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Pobiera dwie liczby: "Minimum" oraz "Maximum".
− Po kliknięciu przycisku "Losuj", generuje liczbę całkowitą z podanego zakresu włącznie.
− Wyświetla wylosowaną liczbę w elemencie o identyfikatorze "totolotek".

### Zadanie 17: Ukrywanie i pokazywanie elementów
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Posiada przycisk o nazwie "Pokaż/Ukryj regulamin".
− Po kliknięciu sprawdza aktualny stan wyświetlania bloku z regulaminem (.style.display).
− Jeśli blok jest widoczny, ukrywa go; jeśli jest ukryty, przywraca jego widoczność.

### Zadanie 18: Sumowanie elementów listy zakupów
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Posiada pole tekstowe na nazwę produktu oraz pole numeryczne na cenę.
− Kliknięcie przycisku "Dodaj" dopisuje produkt do listy `<ul>` w formacie: "Nazwa - Cena zł".
− Skrypt sumuje ceny wszystkich dodanych produktów i aktualizuje wartość w paragrafie "Suma całkowita".

### Zadanie 19: Prosty test wyboru
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Posiada pytanie i trzy odpowiedzi w polach radio.
− Po kliknięciu "Sprawdź", skrypt weryfikuje, czy wybrana opcja jest poprawna.
− Wyświetla komunikat "Poprawna odpowiedź" na zielono lub "Błędna odpowiedź" na czerwono.

### Zadanie 20: Wyświetlanie daty i czasu
Wymagania dotyczące skryptu:
− Należy stosować znaczące nazewnictwo zmiennych i funkcji w języku polskim lub angielskim.
− Po kliknięciu przycisku pobiera aktualną datę systemową.
− Wyświetla w wyznaczonym miejscu informację w formacie: "Dziś jest [dzień].[miesiąc].[rok], godzina [godzina]:[minuty]".
− Miesiąc powinien być wyświetlony jako liczba (pamiętaj o odpowiednim indeksowaniu miesięcy w JS).