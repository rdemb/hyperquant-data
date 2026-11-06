⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-06 16:07 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 31 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 2 min |
| Wiek liq-map/BTC.json | 4 min |
| Wiek dziennika prognoz | 4 min |
| Wiek profilu płynności | 5 min |
| Wiek laboratorium folkloru | 5 min |
| Wiek warstwy wielorybów | 4 min |
| Pokrycie OI | 47.3% |
| Mediana wieku pozycji (ważona) | 31 min |
| Pozycje / adresy | 32295 / 50000 |
| Błędy API (od startu procesu) | 7 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
