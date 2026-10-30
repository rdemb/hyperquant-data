⚠️ **Problem z danymi skanera** — sprawdzono 2026-10-30 05:52 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 35 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 1 min |
| Wiek liq-map/BTC.json | 1 min |
| Wiek dziennika prognoz | 2 min |
| Wiek profilu płynności | 0 min |
| Wiek laboratorium folkloru | 60 min |
| Pokrycie OI | 45.6% |
| Mediana wieku pozycji (ważona) | 35 min |
| Pozycje / adresy | 29867 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
