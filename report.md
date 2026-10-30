⚠️ **Problem z danymi skanera** — sprawdzono 2026-10-30 04:07 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 33 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 3 min |
| Wiek liq-map/BTC.json | 3 min |
| Wiek dziennika prognoz | 3 min |
| Wiek profilu płynności | 6 min |
| Wiek laboratorium folkloru | 16 min |
| Pokrycie OI | 45.3% |
| Mediana wieku pozycji (ważona) | 33 min |
| Pozycje / adresy | 30957 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
