⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-06 17:52 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 38 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 1 min |
| Wiek liq-map/BTC.json | 3 min |
| Wiek dziennika prognoz | 4 min |
| Wiek profilu płynności | 0 min |
| Wiek laboratorium folkloru | 50 min |
| Wiek warstwy wielorybów | 3 min |
| Pokrycie OI | 47.9% |
| Mediana wieku pozycji (ważona) | 38 min |
| Pozycje / adresy | 32552 / 50000 |
| Błędy API (od startu procesu) | 7 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
