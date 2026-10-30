⚠️ **Problem z danymi skanera** — sprawdzono 2026-10-30 18:53 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 31 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 2 min |
| Wiek liq-map/BTC.json | 2 min |
| Wiek dziennika prognoz | 3 min |
| Wiek profilu płynności | 1 min |
| Wiek laboratorium folkloru | 10 min |
| Wiek warstwy wielorybów | 2 min |
| Pokrycie OI | 46.3% |
| Mediana wieku pozycji (ważona) | 31 min |
| Pozycje / adresy | 27848 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
