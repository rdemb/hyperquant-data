⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-12 01:37 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 31 min (alarm powyżej 30 min, koniec po 2 przebiegach poniżej 25 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 2 min |
| Wiek liq-map/BTC.json | 2 min |
| Wiek dziennika prognoz | 2 min |
| Wiek profilu płynności | 3 min |
| Wiek laboratorium folkloru | 13 min |
| Wiek warstwy wielorybów | 2 min |
| Wiek niezależnej weryfikacji dziennika | 6 h |
| Pokrycie OI | 47.5% |
| Mediana wieku pozycji (ważona) | 31 min |
| Pozycje / adresy | 32062 / 50000 |
| Błędy API (od startu procesu) | 1 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
