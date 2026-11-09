⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-09 21:37 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 32 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 3 min |
| Wiek liq-map/BTC.json | 3 min |
| Wiek dziennika prognoz | 7 min |
| Wiek profilu płynności | 6 min |
| Wiek laboratorium folkloru | 16 min |
| Wiek warstwy wielorybów | 5 min |
| Pokrycie OI | 47.4% |
| Mediana wieku pozycji (ważona) | 32 min |
| Pozycje / adresy | 31895 / 50001 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
