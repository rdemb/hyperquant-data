⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-09 17:52 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 36 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 1 min |
| Wiek liq-map/BTC.json | 1 min |
| Wiek dziennika prognoz | 2 min |
| Wiek profilu płynności | 1 min |
| Wiek laboratorium folkloru | 31 min |
| Wiek warstwy wielorybów | 1 min |
| Pokrycie OI | 47.3% |
| Mediana wieku pozycji (ważona) | 36 min |
| Pozycje / adresy | 32245 / 50001 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
