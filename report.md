⚠️ **Problem z danymi skanera** — sprawdzono 2026-10-30 14:37 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 38 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 7 min |
| Wiek liq-map/BTC.json | 7 min |
| Wiek dziennika prognoz | 17 min |
| Wiek profilu płynności | 10 min |
| Wiek laboratorium folkloru | 60 min |
| Pokrycie OI | 45.2% |
| Mediana wieku pozycji (ważona) | 38 min |
| Pozycje / adresy | 27562 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
