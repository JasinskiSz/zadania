Stwórz system, który będzie przechowywał informacje o postaci.

```javascript
const character = {
    name: "Justynian",
    role: "Wizard",
    level: 1,
    skills: ["Fireball", "Healing field"],
    equipment: {
        weapon: "dagger",
        armor: "wooden armor",
        items: ["Healing potion", "Compass"]
    }
}
```

## Funkcje do implementacji

1. `createCharacter(name, role)`:

    Tworzy nową postać z podaną nazwą i rolą.

2. `addItem(character, item)`:

    Dodaje nowy przedmiot do ekwipunku postaci.

3. `learnSkill(character, newSkill)`:

    Uczy postać nowej umiejętności.

4. `levelUp(character)`:

    Zwiększa poziom postaci o 1.

5. `characterDescription(character)`:

    Zwraca opis postaci w formie tekstowej.

## Dodatkowe wymagania
- Walidacja danych:
    - Nie pozwalaj na dodanie więcej niż 5 umiejętności
    - Imię postaci musi mieć minimum 3 znaki

- Użycie tablic i pętli
    - Użyj pętli do wyświetlania listy przedmiotów
- Użycie instrukcji warunkowych (if)
    - Różne zestawy startowe dla różnych klas. Dla przykładu, wojownik zaczyna z "sword" i "shield", a mag z "staff" i "robe".

## Przykład użycia

Jak można użyć tych funkcji:

```javascript
// Tworzenie nowej postaci
const mojaPostac = stworzPostac("Gandalf", "Mag");

// Dodawanie przedmiotów
dodajPrzedmiot(mojaPostac, "Różdżka");
dodajPrzedmiot(mojaPostac, "Księga zaklęć");

// Nauka nowej umiejętności
nauczUmiejetnosci(mojaPostac, "Teleportacja");

// Awans na wyższy poziom
awansuj(mojaPostac);

// Wyświetlenie opisu
console.log(opisPostaci(mojaPostac));
```

Stworzenie wszystkich funkcji zostawiam Tobie jako ćwiczenie! Powodzenia :))

## Przykładowy wynik

```txt
=== KARTA POSTACI ===
Imię: Gandalf
Klasa: Mag
Poziom: 2

Umiejętności:
- Kula ognia
- Tarcza magiczna
- Teleportacja
- Błyskawica

Ekwipunek:
Broń: Kostur
Zbroja: Szata
Przedmioty:
- Mikstura many
- Zwój teleportacji
- Różdżka
- Księga zaklęć
```

## Rozszerzenia dla ambitnych

- System walki - Stwórz funkcję `walka(postac1, postac2)` symulującą prostą walkę
- Zapis do localStorage - Zapisuj i wczytuj postacie z pamięci przeglądarki
- Generator losowych imion - Zaimplementuj funkcję generującą losowe imiona fantasy