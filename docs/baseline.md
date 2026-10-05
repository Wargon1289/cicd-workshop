# Baseline — pomiar stanu wyjściowego

Plik uzupełniasz w ZADANIU 01. Czasy odczytujesz w zakładce **Actions**. Wystarczy dokładność
do sekundy.

## Czasy kroków — przebieg na `main`

| Krok | Czas |
|---|---|
| Set up job | 1s|
| Checkout | 0s|
| Set up Node | 1s|
| Install dependencies | 6s|
| Install Playwright browsers | 20s|
| Unit tests | 0s|
| API tests | 20s|
| UI tests | 2m 26s|
| Upload Playwright report | 2s|
| Post Set up Node | 0s|
| Post Checkout | 1s|
| Complete job | 0s|
| **Cały przebieg** | 3m 20s|

## Czas do pierwszego czerwonego sygnału

| Branch | Czas samego testu | Od startu przebiegu do informacji o błędzie |
|---|---|---|
| `demo/failing-unit` | | |
| `demo/failing-search` | — | |

Co na `demo/failing-unit` stało się z testami API i UI:

## `demo/failing-lint` i `demo/failing-security`

| Branch | Wynik przebiegu | Dlaczego tak |
|---|---|---|
| `demo/failing-lint` | | |
| `demo/failing-security` | | |

## Pięć problemów obecnego pipeline’u

1.
2.
3.
4.
5.

## Pomiary z kolejnych zadań

Tu dopisujesz pomiary i odpowiedzi z kolejnych zadań, pod nagłówkiem z numerem zadania.


Zadanie 3

BEFORE
| Krok | Czas |
|---|---|
| Set up job | 1s|
| Checkout | 1s|
| Set up Node | 0s|
| Install dependencies | 6s|
| Install Playwright browsers | 18s|
| Lint | 1s|
| Typecheck | 3s|
| Build | 2s|
| Unit tests | 1s|
| API tests | 19s|
| UI tests | 2m 26s|
| Upload Playwright report | 1s|
| Post Set up Node | 2s|
| Post Cache Playrighw Browse | 6s|
| Post Checkout | 0s|
| Complete job | 0s|
| **Cały przebieg** | 3m 20s|

AFTER

| Krok | Czas |
|---|---|
| Set up job | 1s|
| Checkout | 1s|
| Set up Node | 1s|
| Install dependencies | 5s|
| Install Playwright browsers | 1s|
| Lint | 2s|
| Typecheck | 3s|
| Build | 2s|
| Unit tests | 1s|
| API tests | 20s|
| UI tests | 2m 28s|
| Upload Playwright report | 1s|
| Post Set up Node | 2s|
| Post Cache Playrighw Browse | 6s|
| Post Checkout | 0s|
| Complete job | 0s|
| **Cały przebieg** | 3m 14s|


czy lint, testy jednostkowe i build zależą od siebie, czy mogą wystartować równolegle?
Równolegle
czy testy API i UI powinny wystartować, jeśli aplikacja się nie buduje?
Nie powinny
czy warto uruchamiać drogie testy API i UI, jeśli lint albo testy jednostkowe już wykryły problem?
Nie, bo i tak trzeba naprawic
na co testy API i UI czekają, bo muszą, a na co tylko dlatego, że tak zdecydowaliśmy?
Muszą na build, obowiązkowo, na npm
Reszta bo zdecydowaliśmy bo nie ma sensu odpalać jak inne testy padna (unit czy lint)

Czas Security:
11s
czas do znalezienia na pull requescie 11s


decyzja : zdecydowany blok


A: 2m 43s |  3m 39s

B:  1m2s| 1m 29s 

C:    42s najdłuższy | 1m 9s

Dodatkowe 8:  37s| 1m 22s

wywalony : UI 2gi sie wywalil reszta przeszła.

Matrix : 46s | 1m 10s

Tylko po zmianach małych odpaliły się dwa : 22s | 50s