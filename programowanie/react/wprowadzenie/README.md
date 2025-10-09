# Zadanie: Interaktywny Licznik w React

## Wprowadzenie

### Czym jest React?

**React** to biblioteka JavaScript stworzona przez Facebook (obecnie Meta), która służy do budowania interfejsów użytkownika. W przeciwieństwie do tradycyjnego podejścia, gdzie bezpośrednio manipulujemy elementami strony (DOM), React pozwala tworzyć aplikacje w sposób deklaratywny - opisujemy JAK ma wyglądać interfejs, a React zajmuje się resztą.

### Podstawowe koncepcje

#### 1. Komponenty

Komponenty to podstawowe building blocks w React. Można je porównać do funkcji - przyjmują dane wejściowe (props) i zwracają elementy opisujące, co powinno się pojawić na ekranie.

Przykład prostego komponentu:

```jsx
function Powitanie() {
  return <h1>Witaj w React!</h1>;
}
```

#### 2. JSX (JavaScript XML)

JSX to rozszerzenie składni JavaScript, które pozwala pisać kod podobny do HTML bezpośrednio w JavaScript. Wygląda jak HTML, ale jest przekształcany do wywołań funkcji JavaScript.

Przykład:

```jsx
const element = <h1 className="title">To jest JSX</h1>;

// Po kompilacji staje się:
const element = React.createElement('h1', {className: 'title'}, 'To jest JSX');
```

Ważne zasady JSX:
- Używamy `className` zamiast `class` (bo `class` to słowo kluczowe w JavaScript)
- Atrybuty zapisujemy w camelCase: `onClick`, `onChange`
- Możemy wstawiać wyrażenia JavaScript w nawiasach klamrowych: `{zmienna}`
- JSX musi zwracać jeden element główny

#### 3. State (Stan)

Stan to obiekt przechowujący dane, które mogą się zmieniać w czasie życia komponentu. Gdy stan się zmienia, React automatycznie renderuje komponent ponownie, aktualizując interfejs.

W funkcyjnych komponentach używamy hooka `useState`:

```jsx
import { useState } from 'react';

function Przyklad() {
  const [licznik, setLicznik] = useState(0);
  
  // licznik - aktualna wartość stanu
  // setLicznik - funkcja do aktualizacji stanu
  // 0 - wartość początkowa
  
  return <p>Wartość: {licznik}</p>;
}
```

**Kluczowe zasady pracy ze stanem:**
- Nigdy nie modyfikuj stanu bezpośrednio: `licznik = 5` jest BŁĘDEM
- Zawsze używaj funkcji setter: `setLicznik(5)`
- Stan jest asynchroniczny - zmiana nie następuje natychmiast
- Można mieć wiele stanów w jednym komponencie

#### 4. Obsługa zdarzeń

W React obsługujemy zdarzenia podobnie jak w HTML, ale z drobnymi różnicami:

```jsx
function Przycisk() {
  const handleClick = () => {
    console.log('Kliknięto!');
  };
  
  return <button onClick={handleClick}>Kliknij mnie</button>;
}
```

Ważne:
- Nazwy zdarzeń w camelCase: `onClick`, nie `onclick`
- Przekazujemy funkcję, nie jej wywołanie: `onClick={handleClick}`, nie `onClick={handleClick()}`
- Często używamy funkcji strzałkowych bezpośrednio: `onClick={() => coś()}`

## Przygotowanie środowiska

### Wymagania wstępne

- Node.js (zainstalowany)
- npm (zainstalowany razem z Node.js)
- Edytor kodu (np. VS Code, Sublime Text, WebStorm)
- Przeglądarka internetowa

### Utworzenie projektu

Otwórz terminal i wykonaj następujące polecenia:

```bash
npm create vite moj-licznik
cd moj-licznik
npm install
npm run dev
```

**Wyjaśnienie poleceń:**
- `npm create vite moj-licznik` - tworzy nowy projekt React za pomocą narzędzia [Vite](https://vite.dev/) o nazwie "moj-licznik".
- `cd moj-licznik` - przechodzi do folderu projektu
- `npm install` - instaluje zależności potrzebne do Vite i Reacta
- `npm run dev` - uruchamia serwer deweloperski, aplikacja otworzy się automatycznie w przeglądarce pod adresem http://localhost:5137 (lub na innym porcie, jeśli ten jest zajęty)

### Struktura projektu

Po utworzeniu projektu zobaczysz następującą strukturę folderów:

```
moj-licznik/
├── node_modules/     # Zainstalowane biblioteki
├── public/           # Pliki statyczne
├── src/              # Kod źródłowy aplikacji
│   ├── App.js       # Główny komponent (tu będziesz pracować)
│   ├── App.css      # Style dla App.js
│   ├── index.js     # Punkt wejścia aplikacji
│   └── ...
├── package.json      # Konfiguracja projektu i zależności
└── README.md
```

## Zadanie do wykonania

### Cel

Stwórz interaktywny licznik, który:

1. Wyświetla aktualną wartość liczbową (początkowa wartość: 0)
2. Posiada przycisk "Dodaj", który zwiększa wartość o 1
3. Posiada przycisk "Odejmij", który zmniejsza wartość o 1
4. Posiada przycisk "Resetuj", który przywraca wartość do 0

### Wymagania funkcjonalne

- Licznik powinien być widoczny na środku ekranu
- Przyciski powinny być wyraźnie opisane
- Po kliknięciu każdego przycisku, wyświetlana wartość powinna natychmiast się zaktualizować
- Wartość może być ujemna (nie ma dolnego ograniczenia)

### Kroki do wykonania

#### Krok 1: Przygotowanie pliku App.js

Otwórz plik `src/App.js` i usuń całą jego zawartość. Zacznij od nowa.

#### Krok 2: Import niezbędnych zależności

Na początku pliku zaimportuj potrzebne elementy:

```jsx
import React, { useState } from 'react';
import './App.css';
```

#### Krok 3: Stworzenie komponentu

Stwórz komponent funkcyjny `App`:

```jsx
function App() {
  // Tu umieścisz logikę
  
  return (
    <div className="App">
      {/* Tu umieścisz interfejs użytkownika */}
    </div>
  );
}

export default App;
```

#### Krok 4: Dodanie stanu

Wewnątrz funkcji `App`, przed instrukcją `return`, dodaj stan przechowujący wartość licznika.

**Pytania pomocnicze:**
- Jaka powinna być początkowa wartość?
- Jaką nazwę nadasz zmiennej stanu i funkcji do jej aktualizacji?

#### Krok 5: Wyświetlenie wartości

W sekcji `return`, wewnątrz `<div className="App">`, dodaj:
- Nagłówek z tytułem aplikacji (np. `<h1>Licznik</h1>`)
- Element wyświetlający aktualną wartość licznika

**Podpowiedź:** Aby wyświetlić wartość zmiennej w JSX, użyj nawiasów klamrowych.

#### Krok 6: Dodanie przycisków

Dodaj trzy przyciski, każdy z odpowiednią funkcjonalnością:

**Przycisk "Dodaj":**
- Po kliknięciu zwiększa wartość o 1

**Przycisk "Odejmij":**
- Po kliknięciu zmniejsza wartość o 1

**Przycisk "Resetuj":**
- Po kliknięciu ustawia wartość na 0

**Pytania pomocnicze:**
- Jak przekazać funkcję do atrybutu `onClick`?
- Jak odwołać się do aktualnej wartości stanu podczas jej aktualizacji?
- Czy możesz użyć funkcji strzałkowej bezpośrednio w `onClick`?

#### Krok 7: Stylowanie (opcjonalne)

Otwórz plik `src/App.css` i dodaj własne style, aby poprawić wygląd aplikacji.

Przykładowe style do wykorzystania:

```css
.App {
  text-align: center;
  padding-top: 50px;
  font-family: Arial, sans-serif;
}

button {
  margin: 5px;
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  border: 1px solid #ccc;
  border-radius: 4px;
  background-color: #f0f0f0;
}

button:hover {
  background-color: #e0e0e0;
}
```

### Zadania dodatkowe (dla chętnych)

Po wykonaniu podstawowego zadania, spróbuj rozszerzyć funkcjonalność:

1. **Kolorowanie wartości:**
   - Wartości ujemne wyświetlaj na czerwono
   - Wartości dodatnie wyświetlaj na zielono
   - Zero wyświetlaj standardowym kolorem

2. **Dodatkowe przyciski:**
   - "Dodaj 10" - zwiększa wartość o 10
   - "Odejmij 10" - zmniejsza wartość o 10

3. **Ograniczenia:**
   - Ustaw minimalną wartość (np. -10)
   - Ustaw maksymalną wartość (np. 10)
   - Przyciski powinny być nieaktywne (disabled), gdy osiągnięto limit

4. **Historia:**
   - Przechowuj historię ostatnich 5 wartości
   - Wyświetl je jako listę pod licznikiem

## Wskazówki

### Częste problemy i rozwiązania

**Problem:** Przyciski nie reagują na kliknięcia
- Sprawdź czy używasz `onClick` (z wielką literą 'C')
- Upewnij się, że przekazujesz funkcję, a nie jej wywołanie

**Problem:** Wartość się nie aktualizuje
- Pamiętaj, że musisz użyć funkcji setter ze `useState`
- Nie próbuj modyfikować zmiennej stanu bezpośrednio

**Problem:** Błąd "X is not defined"
- Sprawdź czy zaimportowałeś wszystkie potrzebne elementy
- Upewnij się, że nazwy zmiennych są konsekwentne

**Problem:** Aplikacja się nie kompiluje
- Sprawdź czy wszystkie tagi JSX są zamknięte
- Upewnij się, że zwracasz pojedynczy element główny w `return`

### Dobre praktyki

- Używaj znaczących nazw dla zmiennych i funkcji
- Trzymaj funkcje obsługi zdarzeń poza JSX (definiuj je przed `return`)
- Stosuj wcięcia dla lepszej czytelności
- Dodawaj komentarze wyjaśniające skomplikowaną logikę

## Kryteria sukcesu

Twoje rozwiązanie jest poprawne, gdy:

1. Aplikacja uruchamia się bez błędów
2. Przycisk "Dodaj" zwiększa wyświetlaną wartość o 1
3. Przycisk "Odejmij" zmniejsza wyświetlaną wartość o 1
4. Przycisk "Resetuj" ustawia wartość z powrotem na 0
5. Zmiany są widoczne natychmiast po kliknięciu
6. Kod jest czytelny i zgodny z konwencjami React

## Pytania do refleksji

Po wykonaniu zadania zastanów się:

1. Dlaczego używamy `useState` zamiast zwykłej zmiennej JavaScript?
2. Co się dzieje, gdy React wykrywa zmianę stanu?
3. Dlaczego w `onClick` przekazujemy funkcję, a nie jej wywołanie?
4. Jak React wie, którą część interfejsu zaktualizować?

## Dalsze kroki

Po ukończeniu tego zadania będziesz gotowy do:
- Tworzenia bardziej złożonych komponentów
- Pracy z wieloma stanami
- Przekazywania danych między komponentami (props)
- Budowania formularzy i obsługi wprowadzania danych

---

**Powodzenia!**

Pamiętaj, że nauka programowania to proces iteracyjny. Nie zniechęcaj się, jeśli coś nie działa za pierwszym razem. Eksperymentuj, poprawiaj błędy i ucz się na nich.
