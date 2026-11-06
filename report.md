⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-06 19:52 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 33 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 1 min |
| Wiek liq-map/BTC.json | 5 min |
| Wiek dziennika prognoz | 6 min |
| Wiek profilu płynności | 1 min |
| Wiek laboratorium folkloru | 51 min |
| Wiek warstwy wielorybów | 5 min |
| Pokrycie OI | 47.3% |
| Mediana wieku pozycji (ważona) | 33 min |
| Pozycje / adresy | 32054 / 50000 |
| Błędy API (od startu procesu) | 7 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
