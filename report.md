⚠️ **Problem z danymi skanera** — sprawdzono 2026-11-11 08:38 UTC

**Wykryte problemy:**
- niezależna weryfikacja dziennika: ostatnia 48 h temu (próg 36 h) — przebieg nie kończy się albo nie startuje

| Miara | Wartość |
|---|---|
| Wiek status.json | 2 min |
| Wiek liq-map/BTC.json | 2 min |
| Wiek dziennika prognoz | 4 min |
| Wiek profilu płynności | 8 min |
| Wiek laboratorium folkloru | 5 min |
| Wiek warstwy wielorybów | 2 min |
| Wiek niezależnej weryfikacji dziennika | 48 h |
| Pokrycie OI | 46.6% |
| Mediana wieku pozycji (ważona) | 30 min |
| Pozycje / adresy | 30165 / 50000 |
| Błędy API (od startu procesu) | 0 |

Źródło: https://raw.githubusercontent.com/rdemb/hyperquant-data/main

Diagnostyka: stan usługi `hyperquant-scanner` i jej dziennik (`journalctl -u hyperquant-scanner`) na serwerze skanera. Zgłoszenie zamknie się samo, gdy dane znów będą świeże.
