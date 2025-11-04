# System rezerwacji biletów

Napisz program, który sprawdza czy użytkownik może kupić bilet na film.

1. Zapytaj użytkownika o jego wiek
2. Sprawdź czy podana wartość to liczba całkowita (użyj hasNextInt())
3. Jeśli TAK - użyj if-else aby sprawdzić czy:
    - Wiek poniżej 13 lat → "Bilet ulgowy: 10 zł"
    - Wiek 13-64 lat → "Bilet normalny: 25 zł"
    - Wiek 65+ → "Bilet seniorski: 15 zł"
4. Jeśli NIE (użytkownik wpisał coś innego niż liczbę) → wyświetl komunikat o błędzie i pokaż użytkownikowi co zostało wpisane