⚠️ **Problem z danymi skanera** — sprawdzono 2026-10-31 08:37 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 32 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 1 min |
| Wiek liq-map/BTC.json | 3 min |
| Wiek dziennika prognoz | 3 min |
| Wiek profilu płynności | 0 min |
| Wiek laboratorium folkloru | 9 min |
| Wiek warstwy wielorybów | 3 min |
| Pokrycie OI | 46.1% |
| Mediana wieku pozycji (ważona) | 32 min |
| Pozycje / adresy | 25462 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
