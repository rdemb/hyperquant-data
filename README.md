# Gałąź `health` — stan strażnika skanera HyperQuant

Strażnik na serwerze skanera (`scripts/watchdog.mjs` w [rdemb/HyperQuant](https://github.com/rdemb/HyperQuant)) co 15 min
sprawdza publiczne dane z gałęzi `main` tego repo, w razie zawieszenia restartuje skaner i zapisuje tu stan:

- `alert.json` — `{ v, ok, checkedAt, problems[] }`,
- `report.md` — ten sam raport w Markdown.

Zapis następuje tylko przy zmianie stanu (oraz co 6 h przy trwałym problemie). Każdy zapis uruchamia workflow
`.github/workflows/health-alert.yml`, który otwiera, komentuje albo zamyka zgłoszenie z etykietą `alert-danych`.
Dane są publiczne — bez adresów, ścieżek ani danych serwera.

Niezależna weryfikacja dziennika działa od 11.11.2026 w repo HyperQuant: workflow
[`ledger-verify.yml`](https://github.com/rdemb/HyperQuant/actions/workflows/ledger-verify.yml) co 6 h sprawdza gałąź
`ledger` tego repo i zapisuje wynik w gałęzi `weryfikacja-dziennika` repo HyperQuant
([`verify/latest.json`](https://raw.githubusercontent.com/rdemb/HyperQuant/weryfikacja-dziennika/verify/latest.json)).
Znaczek: `https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/rdemb/HyperQuant/weryfikacja-dziennika/badge/ledger.json`.

Pliki `badge/` i `verify/` w tej gałęzi są nieaktualne (zostają jako historia) i nie są już zmieniane.
