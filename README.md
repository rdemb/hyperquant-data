# Gałąź `health` — stan strażnika skanera HyperQuant

Strażnik na serwerze skanera (`scripts/watchdog.mjs` w [rdemb/HyperQuant](https://github.com/rdemb/HyperQuant)) co 15 min
sprawdza publiczne dane z gałęzi `main` tego repo, w razie zawieszenia restartuje skaner i zapisuje tu stan:

- `alert.json` — `{ v, ok, checkedAt, problems[] }`,
- `report.md` — ten sam raport w Markdown.

Zapis następuje tylko przy zmianie stanu (oraz co 6 h przy trwałym problemie). Każdy zapis uruchamia workflow
`.github/workflows/health-alert.yml`, który otwiera, komentuje albo zamyka zgłoszenie z etykietą `alert-danych`.
Dane są publiczne — bez adresów, ścieżek ani danych serwera.
