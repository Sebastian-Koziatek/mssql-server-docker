# SQL Server w kontenerze Docker

Ten projekt umożliwia szybkie uruchomienie instancji Microsoft SQL Server 2017 w kontenerze Docker z zachowaniem trwałości danych.

## Zawartość

Plik `docker-compose.yml` zawiera konfigurację do uruchomienia kontenera z bazą danych SQL Server, z wykorzystaniem wolumenu do przechowywania danych oraz mechanizmem sprawdzania kondycji kontenera.

## Wymagania

- **Docker** i **Docker Compose** zainstalowane na Twoim systemie.
- Minimum **2 GB RAM** dostępne dla kontenera.

## Konfiguracja

W pliku `docker-compose.yml` zdefiniowane są następujące zmienne środowiskowe:
- `ACCEPT_EULA`: Automatyczna akceptacja licencji EULA (wartość `"Y"`).
- `SA_PASSWORD`: Hasło dla administratora SQL Server (`sa`). Domyślna wartość to `"password123"`, ale możesz zmienić ją na bezpieczniejsze hasło.

Port 1433 jest mapowany z kontenera na hosta, co umożliwia dostęp do bazy danych.

## Uruchomienie

Aby uruchomić instancję SQL Server, wykonaj poniższe kroki:

1. Sklonuj repozytorium lub skopiuj plik `docker-compose.yml` do lokalnego katalogu.
2. Uruchom kontener za pomocą polecenia:

   ```bash
   docker-compose up -d
