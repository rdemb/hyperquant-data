# Gałąź `health` — stan strażnika skanera HyperQuant

Strażnik na serwerze skanera (`scripts/watchdog.mjs` w [rdemb/HyperQuant](https://github.com/rdemb/HyperQuant)) co 15 min
sprawdza publiczne dane z gałęzi `main` tego repo, w razie zawieszenia restartuje skaner i zapisuje tu stan:

- `alert.json` — `{ v, ok, checkedAt, problems[] }`,
- `report.md` — ten sam raport w Markdown.

Zapis następuje tylko przy zmianie stanu (oraz co 6 h przy trwałym problemie). Każdy zapis uruchamia workflow
`.github/workflows/health-alert.yml`, który otwiera, komentuje albo zamyka zgłoszenie z etykietą `alert-danych`.
Dane są publiczne — bez adresów, ścieżek ani danych serwera.

Zapis strażnika (także puls co 12 h przy „ok”) uruchamia też `.github/workflows/ledger-verify.yml` — niezależną
weryfikację dziennika z gałęzi `ledger` weryfikatorem z repo HyperQuant (`scripts/verify-ledger.mjs`):

- `verify/latest.json` — wynik ostatniego zakończonego przebiegu (`ok`, `at`, `run`, `commit`, `lines`),
- `verify/checkpoint.json` — punkt kontrolny: ostatni commit gałęzi `ledger` z udaną weryfikacją; historia git jest
  sprawdzana od niego, cała historia co najmniej raz na 7 dni,
- `badge/ledger.json` — znaczek shields.io; zielony tylko przy zgodnym wyniku nie starszym niż 36 h.
