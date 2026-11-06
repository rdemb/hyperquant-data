⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-06 01:07 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 36 min (próg 30 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 2 min |
| Wiek liq-map/BTC.json | 2 min |
| Wiek dziennika prognoz | 2 min |
| Wiek profilu płynności | 5 min |
| Wiek laboratorium folkloru | 15 min |
| Wiek warstwy wielorybów | 2 min |
| Pokrycie OI | 46.5% |
| Mediana wieku pozycji (ważona) | 36 min |
| Pozycje / adresy | 33134 / 50000 |
| Błędy API (od startu procesu) | 7 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
