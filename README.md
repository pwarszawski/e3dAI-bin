# e3dAI

Generator dekoracji do scenerii realistycznych symulatora
**[MaSzyna EU07](https://store.steampowered.com/app/1033030/MaSzyna/)**. Na podstawie torów
z pliku scenerii i otwartych danych z Geoportalu tworzy teren, budynki i roślinność w postaci
modeli `.e3d`, gotowych do wstawienia do scenerii.

To repozytorium zawiera wyłącznie wydania programu.

## Pobieranie

Najnowsza wersja jest w zakładce **[Releases](https://github.com/pwarszawski/e3dAI-bin/releases)** –
plik `e3dAI-<wersja>-windows.zip`.

## Wymagania

- Windows 10 lub 11, 64-bitowy.
- Sceneria realistyczna do MaSzyny – najlepiej wykonana w edytorze
  [RaiNsteD](https://rainsted.com/), z torami o realistycznym profilu pionowym. Na ich podstawie
  program dopasowuje teren do przebiegu torów.
- Połączenie z internetem przy sprawdzaniu i pobieraniu danych z Geoportalu.
- Miejsce na dysku na dane źródłowe – zależnie od długości tras i szerokości pasa wokół torów od
  kilku do kilkudziesięciu GB.

Program nie wymaga instalacji ani żadnych dodatkowych bibliotek.

## Pierwsze kroki

1. Rozpakuj archiwum do osobnego katalogu.
2. Pobierz dane **NMT100** – numeryczny model terenu o siatce 100 m, w postaci pliku tekstowego – z
   [dane.gov.pl](https://dane.gov.pl/pl/dataset/792,numeryczny-model-terenu-o-interwale-siatki-co-najmniej-100-m).
   Program buduje z nich daleki horyzont. To jedyne dane, które trzeba pobrać samodzielnie –
   dokładny model terenu (NMT1), chmury LiDAR i modele budynków program pobiera sam z Geoportalu.
3. W pliku `e3dAI.ini` wpisz ścieżkę do pliku scenerii (`PlikiSCN`), do pliku NMT100 (`PlikNMT100`)
   oraz katalogi na dane. Opis każdego ustawienia znajdziesz w samym pliku.
4. Uruchom `e3dAI.exe`, zaznacz scenerię i kliknij kolejno **Sprawdź aktualność**,
   **Pobierz dane** i **Generuj modele**.

Wzorcowy `e3dAI.ini` ma włączony tryb próbny pobierania: program pokaże, co by pobrał, ale niczego
nie zapisze. Gdy wszystko się zgadza, ustaw `PobieranieTrybProbny = false`.

## Warunki korzystania

Program jest bezpłatny do użytku niekomercyjnego. Pełne warunki są w pliku
[LICENCJA.txt](LICENCJA.txt). Program zawiera biblioteki innych autorów – ich wykaz i licencje są
w katalogu `LICENCJE` w paczce.

## Kontakt

Uwagi, zgłoszenia błędów i prośby – przez zakładkę
**[Issues](https://github.com/pwarszawski/e3dAI-bin/issues)**.
