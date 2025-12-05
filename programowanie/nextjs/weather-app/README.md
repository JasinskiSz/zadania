# Opis projektu: Prosta aplikacja pogodowa w Next.js

## 1. Cel projektu

Celem projektu jest przygotowanie prostej aplikacji pogodowej w technologii Next.js, która:

- pobiera dane pogodowe z zewnętrznego API (np. weatherapi),
- wyświetla podstawowe informacje o aktualnej pogodzie dla wybranego miasta,
- umożliwia zapoznanie się z podstawami:
  - tworzenia aplikacji w Next.js,
  - komunikacji z zewnętrznym API (HTTP request, obsługa odpowiedzi, błędów).

Projekt ma formę aplikacji jednostronicowej (Single Page Application - SPA) z prostym i czytelnym interfejsem.

## 2. Stos technologiczny

W projekcie należy wykorzystać:

- **Next.js** (zalecana wersja 13+),
- **React** (wbudowany w Next.js),
- **JavaScript** lub **TypeScript** (wg preferencji, ale zachęcam bardzo do skorzystania z TypeScriptu),
- **CSS** (np. moduły CSS, `styled-jsx`, Tailwind CSS lub inny prosty sposób stylowania).

Jako źródło danych pogodowych należy wykorzystać API, np.:

- [weatherapi](https://www.weatherapi.com/signup.aspx)  
  (wymagane utworzenie darmowego konta i użycie klucza API).

## 3. Wymagania funkcjonalne

### 3.1. Podstawowa funkcjonalność

1. **Wyszukiwanie miasta**
   - Na stronie powinien znajdować się formularz z jednym polem tekstowym do wpisania nazwy miasta.
   - Po zatwierdzeniu powinna zostać wysłana prośba do API pogodowego.

2. **Pobieranie danych z API**
   - Aplikacja powinna wysłać żądanie HTTP do zewnętrznego API z użyciem wpisanej nazwy miasta.
   - Należy obsłużyć co najmniej:
     - poprawną odpowiedź (status 200),
     - błędną nazwę miasta (np. status 404),
     - błędy sieci lub problem z API (np. brak odpowiedzi, błędny klucz API).

3. **Wyświetlanie wyników**
   - Po poprawnym pobraniu danych na stronie powinny zostać wyświetlone minimum:
     - nazwa miasta i kraju,
     - aktualna temperatura,
     - ogólny opis pogody (taki jak np. „clear sky”, „light rain”),
     - ikona pogody (jeśli API ją udostępnia),
     - dodatkowo przynajmniej jedna z informacji:
       - wilgotność,
       - prędkość wiatru,
       - odczuwalna temperatura.
   - Dane muszą być czytelnie sformatowane (np. temperatura z jednostką °C).

4. **Obsługa stanów ładowania i błędów**
   - W trakcie pobierania danych powinien być wyświetlany stan „ładowania” (np. prosty tekst „Ładowanie danych...” lub spinner).
   - W przypadku błędu (np. niepoprawna nazwa miasta, błąd API) powinna zostać wyświetlona czytelna informacja o problemie (np. „Nie znaleziono miasta” lub „Wystąpił błąd podczas pobierania danych”).

### 3.2. Funkcjonalności opcjonalne (rozszerzenia)

Poniższe elementy są opcjonalne, ale zalecane w ramach dodatkowego ćwiczenia:

1. **Wybór jednostki temperatury**
   - Możliwość przełączania między °C a °F (np. przełącznik lub dwa przyciski).

2. **Zapamiętywanie ostatniego miasta**
   - Zapis ostatnio wyszukiwanego miasta w `localStorage`.
   - Przy pierwszym wejściu na stronę po odświeżeniu – automatyczne załadowanie pogody dla ostatnio wyszukiwanego miasta.

3. **Prognoza na kolejne dni**
   - Oprócz aktualnej pogody – wyświetlenie prognozy na kolejne 3–5 dni (jeśli pozwala na to użyte API).

## 4. Opis wyglądu strony

Strona powinna być prosta, czytelna i estetyczna. Zaleca się zastosowanie minimalistycznego layoutu.

### 4.1. Ogólny układ

Strona powinna składać się z następujących sekcji:

1. **Nagłówek (header)**
   - Zawiera tytuł aplikacji, np. „Aplikacja pogodowa” lub „Sprawdź pogodę”.
   - Tytuł powinien być wyraźny, wyróżniony większą czcionką.

2. **Główna sekcja (main)**
   - W centrum strony powinien znajdować się:
     - panel wyszukiwania,
     - panel z wynikami.

3. **Stopka (opcjonalnie)**
   - Może zawierać krótką informację, np. źródło danych: „Dane pogodowe: weatherapi".

### 4.2. Formularz wyszukiwania

- Formularz powinien znajdować się w górnej części głównej sekcji.
- Elementy formularza:
  - Pole tekstowe na nazwę miasta (z placeholderem, np. „Wpisz nazwę miasta...”),
  - Przycisk wyszukiwania (np. z napisem „Szukaj”).
- Układ:
  - Na większych ekranach pole tekstowe i przycisk mogą być w jednym wierszu.
  - Na mniejszych ekranach (np. telefon) elementy mogą ustawiać się jeden pod drugim.

### 4.3. Wyświetlanie wyników

- Wyniki powinny być prezentowane w formie wyraźnego „kafla”/„karty” (card) poniżej formularza.
- Wewnątrz karty powinny zostać umieszczone:
  - nazwa miasta i kraju (np. „Warszawa, PL”) – wyróżniona,
  - temperatura jako główny element (większy font),
  - ikonka pogodowa obok lub nad temperaturą,
  - opis pogody i dodatkowe parametry (wilgotność, wiatr, itp.) w mniejszym tekście.

Przykładowy układ karty:

- Wiersz 1: nazwa miasta i kraju.
- Wiersz 2: duża temperatura + ikona.
- Wiersz 3: opis (np. „lekkie zachmurzenie”).
- Wiersz 4: dodatkowe dane (np. „Wilgotność: 65% | Wiatr: 4 m/s”).

### 4.4. Responsywność

- Strona powinna poprawnie wyświetlać się na urządzeniach mobilnych:
  - zawartość wycentrowana,
  - brak konieczności przewijania poziomego,
  - tekst dobrze czytelny na małych ekranach.
- Układ kart i formularza powinien dostosowywać się do szerokości przeglądarki.

### 4.5. Stylizacja (ogólne wytyczne)

- Zalecane są stonowane kolory (np. tło w jasnym kolorze, tekst w ciemnym).
- Wyróżnienie ważnych elementów (tytuł, temperatura, błędy) poprzez:
  - większy rozmiar czcionki,
  - pogrubienie,
  - kontrastowy kolor (ale zachowujący czytelność).
- W przypadku błędów komunikat powinien być widoczny (np. czerwony tekst lub ramka).

## 5. Wymagania techniczne i organizacyjne

1. **Struktura projektu**
   - Należy utworzyć nowy projekt Next.js (np. przy użyciu `create-next-app`).
   - Pliki i komponenty powinny być logicznie pogrupowane (np. osobny komponent dla formularza wyszukiwania, osobny dla wyświetlania wyniku).

2. **Konfiguracja klucza API**
   - Klucz do API pogodowego powinien być przechowywany w zmiennych środowiskowych (np. `.env.local` w Next.js).
   - Klucz nie powinien być umieszczany bezpośrednio w kodzie w repozytorium.

3. **Pobieranie danych**
   - Do komunikacji z API można wykorzystać:
     - wbudowaną funkcję `fetch` (zalecane),
     - lub inną bibliotekę HTTP, jeśli jest taka potrzeba.
   - Należy zaimplementować obsługę:
     - stanu ładowania (loading),
     - stanu sukcesu,
     - stanu błędu.

4. **Obsługa błędów i walidacja**
   - W przypadku pustego pola wyszukiwania powinien zostać wyświetlony odpowiedni komunikat lub przycisk „Szukaj” powinien być nieaktywny.
   - W przypadku błędnej odpowiedzi z API (np. miasto nie istnieje) powinna zostać wyświetlona informacja, że nie znaleziono wyników.

5. **Komentarze i czytelność kodu**
   - Kod powinien być czytelny i odpowiednio sformatowany.
   - Trudniejsze fragmenty mogą być opatrzone krótkimi komentarzami wyjaśniającymi.

## 6. Możliwe kierunki dalszego rozwoju

Po zrealizowaniu podstawowej wersji aplikacji możliwe jest jej rozszerzenie, np. o:

- wyświetlanie tła strony zależnego od aktualnej pogody (inne tło dla deszczu, inne dla słońca),
- obsługę geolokalizacji (pobranie pogody dla aktualnej lokalizacji użytkownika),
- zapis historii wyszukań i możliwość szybkiego powrotu do wcześniejszych miast,
- tryb ciemny/jasny (dark/light mode).

## 7. Podsumowanie

W efekcie realizacji projektu powinna powstać prosta, responsywna aplikacja pogodowa w Next.js, która:

- umożliwia wyszukiwanie miasta,
- pobiera dane pogodowe z zewnętrznego API,
- prezentuje użytkownikowi czytelne informacje o aktualnej pogodzie,
- zapewnia podstawowe doświadczenie z Next.js oraz integracją z API.