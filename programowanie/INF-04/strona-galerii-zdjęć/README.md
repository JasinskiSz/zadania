# Strona galerii zdjęć na bazie zadania z INF-04
To zadanie bazuje na II części arkusza [INF.04-01-25.01-SG.pdf](./INF.04-01-25.01-SG.pdf) dostępnego do wglądu w tym samym repozytorium. 

## Cel
Z zastosowaniem frameworka Angular lub biblioteki React.js wykonaj aplikację internetową typu front-end realizującą funkcję kategoryzacji zdjęć w galerii. Na obrazach 2, 3, 4 przedstawiono działanie aplikacji (obrazy dostępne w [INF.04-01-25.01-SG.pdf](./INF.04-01-25.01-SG.pdf)). W zależności od zastosowanego narzędzia wygląd aplikacji może nieznacznie się różnić. 

W tym repozytorium znajduje się archiwum, z materiałami do wykonania zadania, o nazwie [pliki3.zip](./pliki3.zip) zabezpieczone hasłem: `K@tegorie)`.

## Założenia
- Aplikacja składa się z jednego komponentu, którego widok w stanie początkowym zaprezentowany jest na obrazie 2 (zdjęcia mogą być wyświetlane w dowolnej kolejności)
- Do utworzenia aplikacji należy wykorzystać zdjęcia oraz plik `dane.txt` wypakowane z archiwum
- Obrazy należy umieścić w folderze `assets` (egzamin/src/assets lub egzamin/public/assets)
- Dokument `dane.txt` zawiera listę obiektów zdjęć, którą należy skopiować jako elementy tablicy. Każdy obiekt zdjęcia zawiera pola: 
  - id 
  - alt (tekst alternatywny dla zdjęcia)
  - filename (nazwa pliku ze zdjęciem)
  - category (1 dla kategorii kwiaty, 2 zwierzęta, 3 samochody)
  - downloads (liczba pobrań zdjęcia)
- Komponent składa się z:
  - Nagłówka pierwszego stopnia o treści: „Kategorie zdjęć”
  - Trzech pól switch (checkbox) domyślnie włączonych, o etykietach: Kwiaty, Zwierzęta, Samochody
  - Bloków zdjęć, które są wyświetlane warunkowo, w zależności od ustawień pól switch. Bloki są wyświetlone jeden obok drugiego, zawierają zdjęcie, nagłówek 4 stopnia z liczbą pobrań oraz przycisk o treści „Pobierz”. Układ elementów jest przedstawiony na obrazie 2 
    - Zdjęcia są formatowane stylem: marginesy zewnętrzne 5 px, zaokrąglone rogi
- Przyciski oraz pola switch są stylowane zgodnie z przykładami w tabeli 1 
- W stanie początkowym włączone są wszystkie pola switch co powoduje wyświetlenie wszystkich 
zdjęć 
- Wyświetlane są tylko zdjęcia z kategorii dla której jest włączone pole switch (obraz 4) 
- Gdy przycisk „Pobierz” zostanie kliknięty, wzrasta o jeden liczba pobrań dla danego zdjęcia. Liczba pobrań jest zapisywana w tablicy z obiektami zdjęć, co na bieżąco powoduje wyświetlenie tej modyfikacji na ekranie (obraz 5)
- W aplikacji zastosowano pętle oraz warunki do wyświetlenia bloków zdjęć. Aplikacja jest napisana uniwersalnie i działa poprawnie też dla innej liczby zdjęć
- Aplikacja powinna być zapisana czytelnie, z zachowaniem zasad czystego formatowania kodu, należy stosować znaczące nazwy zmiennych i funkcji. 

Podejmij próbę uruchomienia aplikacji w przeglądarce