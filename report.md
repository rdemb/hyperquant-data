⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-05 19:52 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 31 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 3 min |
| Wiek liq-map/BTC.json | 3 min |
| Wiek dziennika prognoz | 3 min |
| Wiek profilu płynności | 10 min |
| Wiek laboratorium folkloru | 60 min |
| Wiek warstwy wielorybów | 3 min |
| Pokrycie OI | 46.1% |
| Mediana wieku pozycji (ważona) | 31 min |
| Pozycje / adresy | 33322 / 50002 |
| Błędy API (od startu procesu) | 6 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
