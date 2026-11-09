⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-09 15:07 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 40 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 3 min |
| Wiek liq-map/BTC.json | 5 min |
| Wiek dziennika prognoz | 3 min |
| Wiek profilu płynności | 6 min |
| Wiek laboratorium folkloru | 46 min |
| Wiek warstwy wielorybów | 5 min |
| Pokrycie OI | 47.1% |
| Mediana wieku pozycji (ważona) | 40 min |
| Pozycje / adresy | 31762 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
