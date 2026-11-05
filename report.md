⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-05 00:37 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 30 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 2 min |
| Wiek liq-map/BTC.json | 6 min |
| Wiek dziennika prognoz | 6 min |
| Wiek profilu płynności | 6 min |
| Wiek laboratorium folkloru | 46 min |
| Wiek warstwy wielorybów | 6 min |
| Pokrycie OI | 46.2% |
| Mediana wieku pozycji (ważona) | 30 min |
| Pozycje / adresy | 28601 / 50000 |
| Błędy API (od startu procesu) | 1 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
