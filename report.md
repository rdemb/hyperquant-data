⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-12 07:53 UTC

**Wykryte problemy:**
- odczyty pozycji opóźnione: mediana ważona 27 min (alarm powyżej 30 min, koniec po 2 przebiegach poniżej 25 min)

| Miara | Wartość |
|---|---|
| Wiek status.json | 1 min |
| Wiek liq-map/BTC.json | 7 min |
| Wiek dziennika prognoz | 4 min |
| Wiek profilu płynności | 8 min |
| Wiek laboratorium folkloru | 28 min |
| Wiek warstwy wielorybów | 5 min |
| Wiek niezależnej weryfikacji dziennika | 0 h |
| Pokrycie OI | 47.4% |
| Mediana wieku pozycji (ważona) | 27 min |
| Pozycje / adresy | 30400 / 50000 |
| Błędy API (od startu procesu) | 1 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
