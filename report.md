⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-09 07:22 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 30 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 2 min |
| Wiek liq-map/BTC.json | 8 min |
| Wiek dziennika prognoz | 2 min |
| Wiek profilu płynności | 1 min |
| Wiek laboratorium folkloru | 21 min |
| Wiek warstwy wielorybów | 8 min |
| Pokrycie OI | 47.0% |
| Mediana wieku pozycji (ważona) | 30 min |
| Pozycje / adresy | 31917 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
