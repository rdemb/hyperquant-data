⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-09 08:07 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 37 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 3 min |
| Wiek liq-map/BTC.json | 3 min |
| Wiek dziennika prognoz | 3 min |
| Wiek profilu płynności | 6 min |
| Wiek laboratorium folkloru | 6 min |
| Wiek warstwy wielorybów | 5 min |
| Pokrycie OI | 47.2% |
| Mediana wieku pozycji (ważona) | 37 min |
| Pozycje / adresy | 31980 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
