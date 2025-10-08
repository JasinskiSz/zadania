# Zadanie: Eksplorator plików w React

## Cel zadania

Celem zadania jest stworzenie aplikacji webowej imitującej prosty eksplorator plików. Aplikacja pozwoli na przeglądanie struktury folderów i plików, rozwijanie i zwijanie katalogów oraz wyświetlanie informacji o wybranych elementach.

## Wymagania techniczne

### Technologie
- React 18+
- Vite
- JavaScript lub TypeScript (do wyboru)
- CSS

### Przykładowa struktura danych

Struktura plików i folderów może być zdefiniowana jako obiekt JavaScript umieszczony bezpośrednio w kodzie. Przykładowa struktura, którą można wykorzystać:

```JavaScript
const fileSystem = {
  id: 1,
  name: "root",
  type: "folder",
  children: [
    {
      id: 2,
      name: "Dokumenty",
      type: "folder",
      children: [
        { id: 3, name: "CV.pdf", type: "file", size: "245 KB" },
        { id: 4, name: "List motywacyjny.docx", type: "file", size: "128 KB" }
      ]
    },
    {
      id: 5,
      name: "Zdjęcia",
      type: "folder",
      children: [
        { id: 6, name: "wakacje.jpg", type: "file", size: "2.1 MB" },
        { id: 7, name: "rodzina.png", type: "file", size: "1.8 MB" }
      ]
    },
    {
      id: 8,
      name: "readme.txt",
      type: "file",
      size: "1 KB"
    }
  ]
};
```

## Wymagania funkcjonalne
### Funkcjonalność podstawowa
1. Wyświetlanie struktury

- Aplikacja wyświetla drzewo folderów i plików
- Pliki i foldery powinny być wizualnie odróżnialne (ikony, kolory, czcionka)

2. Rozwijanie i zwijanie folderów

- Kliknięcie na folder powoduje rozwinięcie lub zwinięcie jego zawartości
- Domyślnie wszystkie foldery są zwinięte
- Rozwinięty folder pokazuje swoje elementy podrzędne

3. Wyświetlanie szczegółów

- Po kliknięciu na plik wyświetlają się jego szczegóły (nazwa, typ, rozmiar)
- Panel ze szczegółami może być umieszczony obok drzewa katalogów lub poniżej

4. Interfejs użytkownika

- Przejrzysta i czytelna struktura wizualna
- Odpowiednie wcięcia dla zagnieżdżonych elementów
- Wskaźnik pokazujący czy folder jest rozwinięty czy zwinięty (np. strzałka)

## Wskazówki implementacyjne

### Podział na komponenty
Zalecana struktura komponentów:

- App - główny komponent aplikacji
- FileExplorer - kontener dla całego eksploratora
- FileTree - komponent wyświetlający drzewo plików
- FileItem / FolderItem - pojedynczy element (plik lub folder)
- FileDetails - panel ze szczegółami wybranego pliku

### Zarządzanie stanem
Należy wykorzystać `useState` do zarządzania:

- Stanem rozwiniętych folderów (które foldery są otwarte)
- Aktualnie wybranym plikiem/folderem
- Ewentualnie stanem widoczności panelu szczegółów

Przykład:

```JavaScript
const [expandedFolders, setExpandedFolders] = useState([]);
const [selectedFile, setSelectedFile] = useState(null);
```

### Conditional rendering
Należy zastosować renderowanie warunkowe do:

- Wyświetlania dzieci folderu tylko gdy jest rozwinięty
- Pokazywania panelu szczegółów tylko gdy plik jest wybrany
- Wyświetlania różnych ikon dla plików i folderów
- Zmiany wskaźnika kierunku strzałki (rozwinięty/zwinięty)

Przykład:

```JavaScript
{isExpanded && folder.children && (
  <div className="folder-content">
    {folder.children.map(child => (
      <FileItem key={child.id} item={child} />
    ))}
  </div>
)}
```

### Obsługa zdarzeń
Należy zaimplementować:

- Obsługę kliknięcia na folder - rozwinięcie go
- Obsługę kliknięcia na plik - wyświetlenie szczegółów

### Podstawowe operacje JavaScript

W zadaniu warto wykorzystać:

- Metody tablicowe - `map`, `filter`, `find`
- Destrukturyzacja
- Operatory logiczne - `&&`, `||`
- Funkcje strzałkowe

## Struktura projektu

Przykładowa organizacja plików:

```text
src/
  ├── components/
  │   ├── FileExplorer.jsx
  │   ├── FileTree.jsx
  │   ├── FileItem.jsx
  │   ├── FolderItem.jsx
  │   └── FileDetails.jsx
  ├── data/
  │   └── fileSystem.js
  ├── App.jsx
  ├── App.css
  └── main.jsx
  ```

## Funkcjonalności dodatkowe (opcjonalne)

Dla chętnych, którzy chcą rozwinąć projekt:

- Breadcrumbs - ścieżka nawigacyjna pokazująca aktualną lokalizację
- Wyszukiwarka - filtrowanie plików i folderów po nazwie
- Sortowanie - sortowanie elementów po nazwie, typie lub rozmiarze
- Ikony - dodanie różnych ikon w zależności od rozszerzenia pliku
- Animacje - płynne animacje rozwijania/zwijania folderów
- Widok listy/siatki - możliwość przełączania między różnymi widokami
- Licznik elementów - wyświetlanie liczby elementów w folderze
- Zaznaczanie wielokrotne - możliwość zaznaczenia wielu plików jednocześnie