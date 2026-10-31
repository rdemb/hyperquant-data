# HyperQuant — historia taśmy i arkusza

Gałąź `history` repo danych: nagranie publicznych kanałów Hyperliquid (trades, l2Book, activeAssetCtx) przez rejestrator
skanera [HyperQuant](https://github.com/rdemb/HyperQuant) (katalog backend/). API Hyperliquid nie udostępnia historii taśmy
ani arkusza — bez nagrania wykres miałby footprint, Deltę, CVD i mapę ciepła dopiero od otwarcia strony.

- `index.json` — spis: godziny z plikiem godzinowym i części 5-minutowe bieżącej godziny dla każdego rynku.
- `<RYNEK>/<RRRR-MM-DD>/<GG>.trades.json.gz` — taśma godziny (JSON w gzip): czas i tid różnicowo, cena, wielkość, strona
  agresora (B/A), numery zlecenia agresora, biorcy i makera w obrębie godziny, indeksy transakcji z hashem zerowym (`z`,
  m.in. podzlecenia TWAP; brak kolumny — plik sprzed jej wprowadzenia); kontekst minutowy (OI, finansowanie, mark); pokrycie.
- `<RYNEK>/<RRRR-MM-DD>/<GG>.book.json.gz` — migawki arkusza (co ok. 5 s, 20 poziomów na stronę: cena, wielkość, liczba
  zleceń) w agregacji bliskiej (~2 pb ceny) i dalekiej (10 × większy krok); pokrycie.
- `<GG>-<MM>.*.json.gz` — części 5-minutowe godziny w toku (po jej zamknięciu łączone w plik godzinowy).

Pokrycie (`spans`) to odcinki ciągłego nagrania: luka po zerwaniu połączenia albo restarcie zostaje jawną luką.
Bez adresów portfeli i hashy transakcji. Gałąź zawiera jeden commit z oknem ostatnich dni (starsze dni są usuwane).
Format i odczyt: src/utils/tapeHistory.ts w repo HyperQuant.
