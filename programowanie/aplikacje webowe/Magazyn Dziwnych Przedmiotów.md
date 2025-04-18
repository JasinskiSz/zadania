## Wstęp
Bardzo proszę o **dokładne** zapoznanie się z **całym** poniższym dokumentem!
Zawiera on wyczerpujący opis zadania i systemu, więc w razie pytań, na które odpowiedź można w nim znaleźć, będę odsyłać do niniejszego dokumentu.

Będę zwracać się w tym dokumencie do "Was" jako do klasy.
## Wprowadzenie
Zadanie podzieliłem na trzy etapy skomplikowania. Poprawne ukończenie pierwszego etapu wymagane jest do otrzymania pozytywnej oceny. Drugi etap wymaga ukończenia najpierw etapu pierwszego, natomiast etap trzeci wymaga etapu drugiego.

Jest ono podzielone na etapy, abyście mogli wykonać je zgodnie ze swoimi ambicjami i poziomem umiejętności.
## Wymagania dotyczące oddawania pracy
Pracę wrzucacie na [GitHub](https://github.com) lub [GitLab](https://gitlab.com). Jeden commit na trzy etapy wykonania pracy to za mało, musicie postarać się trochę bardziej i zacząć porządnie korzystać z tego narzędzia. Link do swojej pracy przedstawicie mi podczas naszych zajęć.

Prace oceniam podczas zajęć, także aby otrzymać ocenę, trzeba być w tym czasie na lekcji i podać mi link. Termin wykonania zadania znajdziecie w swoim terminarzu.
## Założenia pracy
Kod należy przygotować z nazwami klas, pól i metod w języku angielskim!

Kod musicie napisać w jednym z wymienionych przeze mnie języków i przy użyciu wymienionego frameworka.
### Backend:
- Java, 
- C#, 
- JS (może być "surowy" lub w node.js),
- PHP, jeśli ktoś bardzo chce to zrobić, ale to będzie najtrudniejsza opcja imo.
### Technologia webowa (frontend)
Do wykonania interfejsu użytkownika użyj jednego z podanych frameworków webowych:
- React
- Svelte
- Vue
- Vite
- Express (dla Node.js)
- ewentualnie inny po konsultacji ze mną lub na surowo HTML + CSS + JS dla odważnych :)
## System magazynu dziwnych przedmiotów
### Cel zadania
Zadanie zakłada finalnie stworzenie aplikacji webowej, która ma zostać wprowadzona w firmie kolekcjonerskiej Kuriozum Sp. z o. o. - firma wymyślona - trochę taki koncept z gier R.E.P.O. lub Lethal Company. Firma specjalizuje się w zbieraniu i katalogowaniu przedmiotów o dziwnych, czasem nielogicznych właściwościach.

Samo zadanie ma na celu doszlifować wasze już nabyte umiejętności programowania obiektowego i myślenia logicznego. Poniżej znajdziecie dokumentację projektową, która została przygotowana w jak najbliższym odzwierciedleniu warunków realnych - tak jak to powinno być robione. Ponieważ nie macie w tym zadaniu możliwości zaproponowania swojego rozwiązania, poniżej znajdziecie opis samego systemu i wymagań, a pod tym opis zaproponowanego rozwiązania - niestety jest to właściwie narzucone przez przedmiot jakiego się uczycie, dlatego tak a nie inaczej.
### Cel systemu
System ma posłużyć firmie do skatalogowania dziwnych przedmiotów przez nią kolekcjonowanych. Umożliwi to łatwe i wygodne zarządzanie magazynami poprzez zdigitalizowanie elementów obecnego systemu papierowego (zeszyt i pamięć zarządcy).

Kilka efektów, po zakładanym wdrożeniu systemu w firmie:
- poprawiona efektywność ewidencji i katalogowania
- sprawniejsze kontrolowanie liczby przedmiotów, łącznej ich wagi i reguł BHP
- optymalizacja pracy magazynierów
- możliwa dużo prostsza analiza kolekcji
# Zaproponowane rozwiązanie
## Poziom 1 - wstępniaczek
### Ocena
Maksymalnie 3 - dostateczny.
### Zakres
Implementacja podstawowych klas i najbardziej fundamentalnych operacji w aplikacji przy pomocy języka backendowego.
### Rozwiązanie (wymagania)
Stworzenie struktury i hierarchii aplikacji - części backend. Powinna składać się z dwóch klas - `Przedmiot` oraz `Magazyn`.
#### Przedmiot
Przypominam o konieczności napisania kodu w języku angielskim!

Symbolizuje pojedynczy obiekt. Przedmiot, który firma kolekcjonuje i posiada w magazynie.

Zdefiniowane atrybuty:
- `nazwa` - typ tekstowy. np. "Samomieszająca łyżeczka".
- `waga_kg` - liczba z trzema miejscami po przecinku. Waga przedmiotu w kilogramach.
- `poziom_dziwnosci` - typ liczbowy stałoprzecinkowy. Przedział <1, 10>.
- `czy_delikatny` - typ boolean.

Konstruktor klasy powinien przyjmować wszystkie te wartości przy tworzeniu obiektu.

Implementacja metod:
- `opis()` - zwraca typ tekstowy z opisem przedmiotu w formacie JavaScript Object Notation:
```
{
	"nazwa": "Przykładowa nazwa",
	"waga_kg": 42.137,
	"poziom_dziwnosci": 7,
	"czy_delikatny": [TAK/NIE]
}
```
Zwróć uwagę na formatowanie `boolean`.

Przypominam o konieczności napisania kodu w języku angielskim!
#### Magazyn
Reprezentuje shulker boxa, w którym przechowywane są przedmioty. Klasa odpowiada za zarządzanie kolekcją obiektów `Przedmiot`.

`Magazyn` powinien przechowywać przedmioty w jakiejś kolekcji.

Zdefiniowane atrybuty:
- `pojemnosc` - liczba całkowita stałoprzecinkowa. Pojemność magazynu - ile przedmiotów może być maksymalnie w magazynie.
- `aktualna_ilosc_przedmiotow` - liczba całkowita stałoprzecinkowa. Ile przedmiotów jest aktualnie w magazynie.
- `maksymalna_laczna_waga` - liczba z trzema miejscami po przecinku. Jest wyrażona w kilogramach, więc wystarczy liczba. Maksymalna dozwolona waga wszystkich przedmiotów w magazynie.

Konstruktor klasy inicjuje `pojemnosc` oraz `maksymalna_laczna_waga`.

Implementacja metod:
- `dodaj_przedmiot(Przedmiot)` - dodaje obiekt klasy `Przedmiot` do obiektu `Magazyn`.
	- Metoda powinna sprawdzać czy magazyn nie jest pełny oraz czy dodanie przedmiotu nie przekroczy maksymalnej dopuszczalnej wagi magazynu.
	- Metoda powinna dodawać przedmiot do kolekcji i aktualizować zmienną `aktualna_ilosc_przedmiotow`, jeśli warunki są spełnione.
	- Metoda powinna zwrócić `boolean` i prosty komunikat.
- `wypisz_wszystkie()` - Wypisuje opisy wszystkich obiektów typu `Przedmiot` do konsoli.
#### Pozostałe wymagania
Ponieważ na tym poziomie działamy jedynie na backendzie - po uruchomieniu aplikacji z poziomu konsoli[^1] w pierwszej kolejności użytkownik powinien zostać zapytany o `pojemnosc` i `maksymalna_laczna_waga`, aby stworzyć odpowiedni `Magazyn`.

[^1]: najprawdopodobniej będzie to konsola. Może to być czysty JS, wtedy wypytanie powinno iść przez `prompt()` - chyba, że macie lepszy pomysł.
## Poziom 2 - zaawansowany
### Ocena
Maksymalnie 5+, jeśli zrobione perfekcyjnie.
Czwóra, jeśli jest tylko ok.
### Zakres
Rozbudowa programu konsolowego z poprzedniego etapu - pełna funkcjonalność aplikacji dzięki zaimplementowaniu pozostałych metod i dokładnym wgryzieniu się w warunki.
### Rozwiązanie (wymagania)
#### Magazyn
##### Ekspansja!
Teraz magazyn to już nie powinien być tylko jeden obiekt. Magazynów może być kilka, a każdy będzie miał swoją kolekcję przedmiotów. Dodaj możliwość tworzenia nowych shulker boxów (magazynów) z ich własnymi kolekcjami przedmiotów, pojemnościami i maksymalnymi wagami. Tutaj masz dowolność wprowadzenia takiego rozwiązania.

Implementacja nowych metod:
- `usun_przedmiot(nazwa_przedmiotu)` - usuwa pierwszy napotkany przedmiot o podanej nazwie z listy, aktualizuje stan magazynu, zwraca boolean.
- `wypisz_delikatne_lub_ciezkie(prog_wagi)` - wypisuje przedmioty, które są delikatne lub mają wagę większą niż podany próg. Np. `wypisz_delikatne_lub_ciezkie(5.358)` wypisuje wszystkie przedmioty, które są delikatne lub mają wagę większą niż 5.358 kg.
- `oblicz_srednia_dziwnosc()` - oblicza i zwraca średnią. Dla pustego magazynu zwraca 0.
##### Rozbudowa
Rozbudowa metody `dodaj_przedmiot(Przedmiot)`:
- implementacja specyficznego warunku - jeśli dodawany przedmiot ma `poziom_dziwnosci` równy 7 i jednocześnie jest `delikatny` magazyn może go przyjąć tylko wtedy, gdy `aktualna_liczba_przedmiotow` jest mniejsza niż połowa jego `pojemnosc`.
- metoda powinna nadal zwracać `boolean` i wypisywać precyzyjne komunikaty o błędach, tj. "Błąd: Magazyn pełny.", "Błąd: Przekroczono maksymalną wagę magazynu.", "Błąd: Zbyt ryzykowny przedmiot (delikatny i dziwny na poziomie 7) przy obecnym zapełnieniu". Dodaj własne komunikaty w zależności od potrzeb.
## Poziom 3 - interfejs webowy
### Ocena
Maksymalna ocena 6 - celujący oraz dodatkowo ocena dodatkowa dla tych najlepszych z klasy.
### Zakres
Działająca aplikacja webowa, która pozwala zarządzać magazynem przez przeglądarkę, wykorzystując logikę zaimplementowaną w klasach `Przedmiot` i `Magazyn`. Kluczowe jest połączenie logiki backendowej wykonanej w poprzednich etapach projektu z interfejsem frontendowym HTML. 

Logika biznesowa musi pozostać taka sama jak w momencie ukończenia etapu 2 - w razie problemów z tym podpunktem proszę o kontakt.
### Rozwiązanie (wymagania)
#### Interfejs użytkownika
Stwórz stronę `index.html`, która będzie głównym interfejsem użytkownika. Nie musi to być piękna strona, ale ma być funkcjonalna i czytelna.
Teraz zamiast w konsoli, wszystkie funkcjonalności aplikacji powinny wyświetlać się w przeglądarce. 

Interfejs powinien:
- odpowiadać za wyświetlenie stanu magazynowego, np. w tabeli. 
- pozwalać na wprowadzenie przedmiotów poprzez formularz.
- wyświetlać obecnie wybrany magazyn i jego właściwości.
- wyświetlać komunikaty i informacje o ewentualnych błędach/sukcesach.

Elementy niezbędne na ocenę celującą:
- Dodanie przycisków/linków do usuwania przedmiotów bezpośrednio z wyświetlanej listy.
- Wyświetlanie na stronie średniej dziwności magazynu.
- Dodanie formularza do filtrowania przedmiotów delikatnych/ciężkich (funkcja `wypisz_delikatne_lub_ciezkie(prog_wagi)`) i wyświetlanie poprawnych wyników na stronie.
