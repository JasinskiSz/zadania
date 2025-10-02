# Interaktywne menu kawiarni
## Cel
Stworzenie od podstaw interaktywnej aplikacji, która będzie pełnić funkcję cyfrowego menu dla kawiarni. W trakcie projektu potrzebne będą umiejętności z zakresu:
- Tworzenia aplikacji
- Budowania komponentów
- Zarządzania stanem
- Renderowania warunkowego
- Korzystania z gita w podstawowym zakresie
## Zadanie
W głównym komponencie `App.jsx` należy stworzyć tablicę obiektów, która będzie reprezentować dane o kawach. Każdy obiekt powinien zawierać co najmniej:
- id
- nazwa
- typ (typ kawy - espresso, przelew, mrożona etc.)
- opis
- nowość (boolean true/false)

Następnie należy przygotować stronę w taki sposób, aby renderować całą, niefiltrowaną listę kaw na stronie. Jeśli ten etap został wykonany cały w `App.jsx`, to należy go rozbić na komponenty `CoffeeCard.jsx` oraz `CoffeeList.jsx`.

Należy również stworzyć komponent `FilterMenu.jsx`, który będzie odpowiedzialny za wyświetlanie przycisków do filtrowania różnych pozycji w menu.