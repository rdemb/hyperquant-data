⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-05 23:07 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 33 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 2 min |
| Wiek liq-map/BTC.json | 6 min |
| Wiek dziennika prognoz | 6 min |
| Wiek profilu płynności | 5 min |
| Wiek laboratorium folkloru | 15 min |
| Wiek warstwy wielorybów | 6 min |
| Pokrycie OI | 47.6% |
| Mediana wieku pozycji (ważona) | 33 min |
| Pozycje / adresy | 32890 / 50000 |
| Błędy API (od startu procesu) | 7 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
