⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-05 22:22 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 31 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 1 min |
| Wiek liq-map/BTC.json | 7 min |
| Wiek dziennika prognoz | 17 min |
| Wiek profilu płynności | 0 min |
| Wiek laboratorium folkloru | 30 min |
| Wiek warstwy wielorybów | 7 min |
| Pokrycie OI | 46.2% |
| Mediana wieku pozycji (ważona) | 31 min |
| Pozycje / adresy | 32911 / 50000 |
| Błędy API (od startu procesu) | 7 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
