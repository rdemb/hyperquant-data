⚠️ **Problem z danymi skanera** — sprawdzono 2026-10-30 16:22 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 38 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 2 min |
| Wiek liq-map/BTC.json | 4 min |
| Wiek dziennika prognoz | 5 min |
| Wiek profilu płynności | 5 min |
| Wiek laboratorium folkloru | 45 min |
| Pokrycie OI | 45.7% |
| Mediana wieku pozycji (ważona) | 38 min |
| Pozycje / adresy | 27902 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
