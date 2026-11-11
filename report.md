⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-11 10:23 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 30 min (alarm powyżej 30 min, koniec po 2 przebiegach poniżej 25 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 2 min |
| Wiek liq-map/BTC.json | 6 min |
| Wiek dziennika prognoz | 6 min |
| Wiek profilu płynności | 1 min |
| Wiek laboratorium folkloru | 11 min |
| Wiek warstwy wielorybów | 6 min |
| Wiek niezależnej weryfikacji dziennika | 1 h |
| Pokrycie OI | 47.2% |
| Mediana wieku pozycji (ważona) | 30 min |
| Pozycje / adresy | 30237 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
