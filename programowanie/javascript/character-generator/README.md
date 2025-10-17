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

- `createCharacter(name, role)`
- `addItem(character, item)`
- `learnSkill(character, newSkill)`
- `levelUp(character)`
- `characterDescription(character)`

## Dodatkowe wymagania
- Walidacja danych
- Użycie tablic i pętli
- Użycie instrukcji warunkowych (if)