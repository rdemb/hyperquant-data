⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-06 05:37 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 39 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 2 min |
| Wiek liq-map/BTC.json | 6 min |
| Wiek dziennika prognoz | 6 min |
| Wiek profilu płynności | 5 min |
| Wiek laboratorium folkloru | 45 min |
| Wiek warstwy wielorybów | 2 min |
| Pokrycie OI | 46.7% |
| Mediana wieku pozycji (ważona) | 39 min |
| Pozycje / adresy | 30422 / 50000 |
| Błędy API (od startu procesu) | 7 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
