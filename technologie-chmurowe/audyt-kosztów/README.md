# Audyt kosztów

Dla pewnej firmy został przygotowany opis ich kosztów w chmurze:
- 15 TB w S3 Standard (50% danych nie było dostępnych od 6 miesięcy)
- 200 GB snapshot EBS (z usuniętych instancji sprzed roku)
- Multi-region replication ALL files (włącznie z logami)
- Versioning enabled - 50 wersji każdego pliku
- Brak lifecycle policies
- Requester Pays: disabled
- Intelligent-Tiering: nie używają

Koszt miesięczny dla firmy: 3,200 USD

## Cel

Twoim zadaniem jako analityka jest:
1. Zidentyfikować min. 5 problemów
2. Zaproponować poprawki
3. Oszacować oszczędności

Przygotuj listę, która opisze:
1. obecny problem w firmie na podstawie powyższych danych
2. zaproponowane przez Ciebie rozwiązanie (ulepszenie)
3. oszczędność dla firmy w USD lub PLN na miesiąc