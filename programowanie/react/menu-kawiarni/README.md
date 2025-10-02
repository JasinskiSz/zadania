# Interaktywne menu kawiarni
## Cel
Stworzenie od podstaw interaktywnej aplikacji, która będzie pełnić funkcję cyfrowego menu dla kawiarni. W trakcie projektu potrzebne będą umiejętności z zakresu:
- Tworzenia aplikacji
- Budowania komponentów
- Zarządzania stanem
- Renderowania warunkowego
- Korzystania z gita w podstawowym zakresie
## Zadanie
Przygotowanie aplikacji zostało podzielone na 4 etapy. **Wskazane jest wykonywać committy jak najczęściej, z dokładną i czytelną wiadomością.** Dobrym momentem na committowanie jest zakończenie etapu, ale **silnie sugerowane** jest committowanie **jeszcze częściej**, przy każdej działającej zmianie.
### Etap 1 - Podstawowa struktura
W głównym komponencie `App.jsx` należy stworzyć tablicę obiektów, która będzie reprezentować dane o kawach. Każdy obiekt powinien zawierać co najmniej:
- id
- nazwa
- typ (typ kawy - espresso, przelew, mrożona etc.)
- opis
- nowość (boolean true/false)

Następnie należy przygotować stronę w taki sposób, aby renderować całą, niefiltrowaną listę kaw na stronie.
### Etap 2 - Podział na komponenty
Jeśli poprzedni etap został wykonany cały w `App.jsx`, to należy go rozbić na komponenty `CoffeeCard.jsx` oraz `CoffeeList.jsx`.

`CoffeeList.jsx` to komponent, do którego przekazywana jest tablica z kawami jako props, które potem mapowane są do `CoffeeCard.jsx`. Tablica musi znajdować się w `App.jsx`.

Należy również stworzyć komponent `FilterMenu.jsx`, który będzie odpowiedzialny za wyświetlanie przycisków do filtrowania różnych pozycji w menu. Przykładowe dostępne kontrolki zawierałyby: Espresso, Przelewy, Mrożone.
### Etap 3 - Implementacja stanu
W głównym komponencie aplikacji `App.jsx` należy zaimplementować stan, który będzie reprezentować aktualnie wybrany filtr typu kawy. Domyślnie wybrane mają być wszystkie kawy. Kliknięcie w przycisk z komponentu `FilterMenu.jsx` powinno zmieniać aktualizować ten stan.
### Etap 4 - Renderowanie warunkowe
Zmodyfikuj logikę aplikacji w taki sposób, aby do komponentu `CoffeeList.jsx` przekazywana była tylko ta część danych, która odpowiada aktualnie wybranemu filtrowi w stanie.

Jeśli po wybraniu filtra nie jest wyświetlana żadna kawa, ponieważ przekazywana lista jest pusta, wyświetl komunikat, przykładowo "Przepraszamy, obecnie nie mamy kaw tego typu.".

Należy wykorzystać renderowanie warunkowe w komponencie `CoffeeCard.jsx`. Jeśli dana kawa ma ustawioną właściwość "nowość" na "true", to na jej karcie powinien pojawić się dodatkowy element wizualny, jak np. czerwona etykieta "NOWOŚĆ!" w rogu karty.