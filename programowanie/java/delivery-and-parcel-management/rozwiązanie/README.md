Przykład zaimplementowanych zmiennych:

```java
// DANE DOSTAWY
String deliveryType = "EXPRESS";      // EXPRESS, STANDARD, ECONOMY
double cargoWeight = 850.5;           // waga w kg
double cargoVolume = 12.5;            // objętość w m³
boolean isFragile = true;             // czy przesyłka jest delikatna/krucha
boolean requiresCooling = false;      // czy wymaga chłodzenia
int palletCount = 8;                  // liczba palet
double deliveryDistance = 450.0;      // odległość dostawy w km

// DANE MAGAZYNU
int availableSpace = 15;              // dostępne miejsca paletowe
double maxLoadCapacity = 1000.0;      // max udźwig w kg
boolean coldStorageAvailable = true;  // czy dostępna chłodnia
int workersAvailable = 3;             // dostępni pracownicy
boolean isWeekend = false;            // czy jest weekend
int currentHour = 14;                 // aktualna godzina (0-23)

// DANE TRANSPORTOWE
boolean truckAvailable = true;        // czy ciężarówka dostępna
boolean vanAvailable = true;          // czy van dostępny
double fuelPrice = 6.5;               // cena paliwa PLN/litr
boolean hasADRlicense = false;        // licencja na towary niebezpieczne

```