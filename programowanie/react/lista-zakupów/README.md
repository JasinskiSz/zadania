# Zadanie: Lista Zakupów 🛒

## Cel

Stwórz prostą aplikację do listy zakupów, gdzie można:

- Dodawać produkty
- Usuwać produkty
- Przekreślać produkty (oznaczać jako kupione)

## Przygotowanie
Tworzenie aplikacji:
``` bash
npm create vite@latest
# wybierz "React" oraz "JavaScript"
cd nazwa-projektu
npm install # instaluje zależności 
npm run dev # odpala serwer deweloperski
```

### Struktura danych

Każdy produkt to obiekt z:

- id (unikalny)
- nazwa (string)
- kupiony (true/false)

### Funkcjonalności

#### Dodawanie

- Input do wpisania nazwy produktu
- Przycisk "Dodaj"

#### Wyświetlanie

- Lista wszystkich produktów
- Kupione produkty mają przekreślony tekst

#### Akcje

- Kliknięcie na produkt = zmiana statusu (kupiony/niekupiony)
- Przycisk "Usuń" przy każdym produkcie

### Podpowiedzi

- Użyj useState do przechowywania tablicy produktów
- Do generowania ID możesz użyć Date.now()
- Do renderowania listy użyj .map()
- Zacznij od App.jsx - wszystko może być w jednym komponencie