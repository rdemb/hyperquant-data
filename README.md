# HyperQuant — dane publiczne

Agregaty publikowane automatycznie przez skaner [HyperQuant](https://github.com/rdemb/HyperQuant) (katalog backend/).
Repozytorium zawiera zawsze jeden commit z bieżącym stanem.

- `liq-map/BTC.json` — mapa likwidacji BTC z pozycji on-chain Hyperliquid: kubełki cen likwidacji, pokrycie open interest, wiek odczytów.
- `liq-tape/BTC.json` — likwidacje śledzonych pozycji z 24 h, potwierdzone fillami z polem `liquidation`: czas, strona, rozmiar, cena, błąd mapy.
- `cohorts/BTC.json` — przepływ kohort (market makerzy, statystycznie poinformowani, wieloryby, reszta): kubełki 15 min z 24 h, markouty poza próbą; k-anonimowość (komórki z < 5 uczestnikami lub z dominującym uczestnikiem ukryte).
- `liquidity/BTC.json` — profil płynności arkusza: mediana głębokości obu stron w ±10 / ±20 bp wg godziny UTC (do 30 dni), bieżąca płynność względem normy godziny, odporność po gwałtownych ruchach.
- `lab/BTC.json` — laboratorium folkloru: reguły day tradingu (okrągłe poziomy, zebranie PDH/PDL, IB, VWAP, luka CME, finansowanie, 10:00 NY, momentum) — test historyczny z FDR i prerejestrowany test do przodu (e-wartości, e-BH) ze wszystkimi zdarzeniami do przeliczenia.
- `whales.json` — warstwa wielorybów (BTC, ETH, SOL, HYPE): pozycje (wartość, wejście, likwidacja, dźwignia) i zlecenia oczekujące z wyzwalanymi (limit, stop, TP) największych kont z publicznego rankingu i dużych pozycji BTC; konto jako pseudonim ważny jedną dobę UTC, bez adresów; kwoty i ceny zaokrąglone.
- `status.json` — stan skanera (liczby adresów i pozycji, błędy API).
- `alerts/keys.json` — klucze publiczne serwera powiadomień o alarmach: VAPID (subskrypcje push przeglądarek) i Ed25519 (podpis zapytań do skrzynki alarmów).

Gałąź `history` — nagranie taśmy, arkusza i kontekstu rynków (części 5-minutowe i pliki godzinowe JSON w gzip, okno ostatnich dni, jeden commit): historia footprintu, Delty, CVD i mapy ciepła od pierwszej sekundy na stronie; opis w README gałęzi.

Gałąź `ledger` — weryfikowalny dziennik prognoz desku (historia przyrostowa): pliki dzienne `BTC/RRRR-MM-DD.jsonl` z łańcuchem hashy SHA-256,
kotwice OpenTimestamps `BTC/ots/`, podsumowanie `BTC/summary.json`. Weryfikacja: `node scripts/verify-ledger.mjs` w repo HyperQuant.

Gałąź `archive` — archiwum świec BTC 1m / 1h / 1d i godzinowego finansowania (CSV, historia przyrostowa, tylko dopisywanie): API Hyperliquid oddaje najwyżej ~5000 ostatnich świec, archiwum zachowuje resztę.

Gałąź `health` — stan strażnika skanera (`alert.json`, `report.md`) zapisywany przy zmianie stanu; workflow tej gałęzi otwiera i zamyka zgłoszenie `alert-danych`.

Wyłącznie agregaty — bez adresów portfeli. Źródło: publiczne API Hyperliquid. Metoda: src/utils/liqMap.ts w repo HyperQuant.
