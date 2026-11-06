⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-06 04:52 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 35 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 1 min |
| Wiek liq-map/BTC.json | 3 min |
| Wiek dziennika prognoz | 4 min |
| Wiek profilu płynności | 1 min |
| Wiek laboratorium folkloru | 1 min |
| Wiek warstwy wielorybów | 5 min |
| Pokrycie OI | 46.4% |
| Mediana wieku pozycji (ważona) | 35 min |
| Pozycje / adresy | 30889 / 50000 |
| Błędy API (od startu procesu) | 7 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
