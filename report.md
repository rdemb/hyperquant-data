⚠️ **Problem z danymi skanera** — sprawdzono 2026-10-30 06:52 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 37 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 3 min |
| Wiek liq-map/BTC.json | 3 min |
| Wiek dziennika prognoz | 3 min |
| Wiek profilu płynności | 10 min |
| Wiek laboratorium folkloru | 60 min |
| Pokrycie OI | 45.7% |
| Mediana wieku pozycji (ważona) | 37 min |
| Pozycje / adresy | 28991 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
