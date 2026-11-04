⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-04 21:22 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 34 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 1 min |
| Wiek liq-map/BTC.json | 3 min |
| Wiek dziennika prognoz | 3 min |
| Wiek profilu płynności | 0 min |
| Wiek laboratorium folkloru | 30 min |
| Wiek warstwy wielorybów | 3 min |
| Pokrycie OI | 47.1% |
| Mediana wieku pozycji (ważona) | 34 min |
| Pozycje / adresy | 29916 / 50000 |
| Błędy API (od startu procesu) | 1 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
