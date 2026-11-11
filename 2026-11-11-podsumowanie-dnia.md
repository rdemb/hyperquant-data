---
title: "BTC kończy dzień przy 74 616, mapy dnia z Brierem 0,149 wobec 0,249"
description: "Wybicie po otwarciu Nowego Jorku zabrało shorty do 74 750. Rozliczam opublikowane mapy: 21 trafień na 44 oceny, BSS 0,40 wobec stałej częstości."
date: 2026-11-11T22:05:04+01:00
type: article
section: Podsumowanie dnia
price: 74616
summary:
  - "Sesja Nowego Jorku przeszła od dołka 73 360 do szczytu 74 750, a OI spadło o 1,11% przy cenie wyżej o 1,53%, czyli rynek napędzało krycie shortów."
  - "Opublikowane mapy dnia: 44 oceny dotknięć, 21 trafień, Brier 0,149 wobec 0,249 dla stałej częstości (BSS 0,40)."
  - "Najdroższe pudło: VWAP −2σ 73 356 z szansą 65% w mapie przed Nowym Jorkiem, a dołek sesji stanął na 73 360."
  - "Nad ceną w 1% czeka 40,9 mln USD shortów do likwidacji, pod ceną w 1% nie ma longów."
metrics:
  - { label: "Premia perp", value: "−4,3 bp", note: "średnio 24 h −3,6 bp" }
  - { label: "Funding", value: "0,08 bp/h", note: "średnio 24 h 0,11 bp/h" }
  - { label: "Przepływ agresorów 24 h", value: "−87,3 mln USD", note: "kupno biorców 279,7, sprzedaż 366,9 mln USD" }
  - { label: "Likwidacje 24 h", value: "12,1 mln USD", note: "longi 0,1, shorty 12,0 mln USD" }
  - { label: "Longi w 1% pod ceną", value: "0,0 mln USD", note: "do likwidacji między 73 870 a ceną" }
  - { label: "Shorty w 1% nad ceną", value: "40,9 mln USD", note: "do likwidacji między ceną a 75 362" }
  - { label: "Arkusz ±10 bp: bidy", value: "48% bidów", note: "zwykle o tej godzinie 50% (21 dni)" }
  - { label: "Zmienność 5 min, 24 h", value: "12,0 bp", note: "poprzednie dni robocze (5): 14,6 bp" }
liquidations:
  step: 250
  coverage: 47
  shorts: [[77750, 0.5], [77500, 1.1], [77250, 1.6], [77000, 5], [76750, 16], [76500, 2.2], [76250, 1.7], [76000, 7.2], [75750, 1.2], [75500, 2.7], [75250, 9.3], [75000, 9.1], [74750, 24.5], [74500, 5.8]]
  longs: [[73500, 18.5], [73250, 5.9], [73000, 6.8], [72750, 4.3], [72500, 31.1], [72250, 4.9], [72000, 26.3], [71750, 12.1], [71500, 16.9], [71250, 43.5]]
  note: "Mapa z 22:03, cena wtedy 74 609; pokrycie 47% otwartych pozycji."
flows:
  title: "Przepływ agresorów netto, 24 h"
  unit: "mln USD"
  rows:
    - { label: "Wieloryby", value: -89.8, note: "80 kont" }
    - { label: "Reszta rynku", value: 1.2, note: "17 160 kont" }
    - { label: "Animatorzy rynku", value: 1.3, note: "210 kont" }
# setups: 2–3 scenariusze warunkowe w tym kształcie (docs/BLOG.md desku), liczby z danych, potem znacznik setupów w treści
#   - name: "Zjawisko rynkowe, nie transakcja (do 70 znaków)"
#     bias: up                      # up, down albo flat
#     zone: [79750, 80250]          # [od, do]: klaster likwidacji, dołek/szczyt, wartość sesji
#     window: "do 10:00 w niedzielę"
#     triggers:                     # 2–4 obserwowalne warunki w kolejności, każdy do 180 znaków
#       - "Cena wchodzi w klaster, a likwidacje longów rosną skokowo."
#     invalidation: "Dwa zamknięcia 15 min pod 79 750 bez powrotu."
#     reactions:                    # 2–4 poziomy z levels albo mapy likwidacji
#       - { label: "PDL", price: 80500 }
#     evidence: "Tylko gdy hipoteza laboratorium pasuje: n, częstość wobec losowej, uczciwie o szumie."
---
## Co mówiły dzisiejsze mapy

Rano była [mapa dnia](../2026-11-11-mapa-dnia/), potem [otwarcie Londynu](../2026-11-11-otwarcie-londynu/), a rozliczam dziś dwie mapy z oknem do 19:30: [mapę przed Nowym Jorkiem](../2026-11-11-mapa-przed-nowym-jorkiem/) z 14:50 i aktualizację z [otwarcia Nowego Jorku](../2026-11-11-otwarcie-nowego-jorku/) z 15:45. Wieczorem była jeszcze [aktualizacja](../2026-11-11-aktualizacja-20/).

Mapa z 14:50 dawała zakres 68% od 72 810 do 74 623. Cena na koniec okna to 74 427, więc w zakresie. Po stronie wzrostów trafiły poziomy, którym dawałem mniej niż pół na pół: klaster shortów 74 350 z szansą 45% padł o 16:35, a klaster 26,8 mln przy 74 650 z szansą 28% o 18:18. VAH 74 259 (52%), 74 000 (74%) i VWAP +1σ 73 980 (76%) też zostały dotknięte. Wyżej mapa miała rację, że to za daleko: otwarcie tygodnia 74 820 (20%), klaster 74 850 (19%) i PDH 75 401 (5%) zostały nietknięte. Najbardziej bolesne pudło jest na dole: VWAP −2σ 73 356 z szansą 65% nie padł, a dołek sesji stanął na 73 360. Azja L 73 174 (49%) i 73 000 (37%) też bez dotknięcia. Brier tej mapy 0,126.

Aktualizacja z 15:45 wypadła gorzej. Zakres 68% od 72 824 do 74 285 cena przebiła, koniec okna 74 427 jest poza zakresem. Klaster 74 350 dostał tam tylko 24%, VAH 74 259 30%, a oba padły o 16:35. VWAP −2σ 73 349 z szansą 75% i Azja L 73 174 z szansą 55% nie zostały dotknięte. Brier 0,172.

## Jak przebiegł dzień

Sesja Nowego Jorku od 15:30 do 22:00 zrobiła szczyt 74 750 o 18:22 i dołek 73 360 o 16:24, ostatnio 74 616. Zakres 1390 USD, czyli 1,89%. Zaraz po dołku przyszło wybicie: świeca 15 min z 16:30 zrobiła 3674,4 BTC wolumenu, a w tej samej świecy zlikwidowano 7,84 mln USD shortów. CVD sesji +426 BTC, kupno 51% obrotu przy wolumenie 15 152 BTC. OI spadło o 1,11% przy cenie wyżej o 1,53%, więc to było przede wszystkim krycie shortów, a nie świeże longi.

## Analiza wykresu

[[wykres]]

**Szerszy obraz.** Dzień skończył się w środku wczorajszego zakresu, między PDL 72 668 a PDH 75 401. Dołek doby 73 174 padł w nocy, w świecy z 03:30, a szczyt 74 750 w sesji amerykańskiej. Wybicie z 16:30 miało kontynuację do 18:15, ale do PDH zabrakło sporo, więc to wybicie w zakresie, nie z zakresu.

**Wartość.** POC z 24 godzin to 73 725, obszar wartości od 73 525 do 74 125. Cena stoi nad wartością. Od świecy z 17:00 każda świeca 15 min zamknęła się nad VAH 74 125, łącznie z cofnięciem o 20:00, które zamknęło się na 74 226. To pięć godzin akceptacji nad obszarem wartości, a nie szybki powrót.

**VWAP.** VWAP dnia 73 924, σ 317,3, cena 2,18σ nad nim. Od świecy z 16:30 każde zamknięcie było nad VWAP, a od 17:00 każde nad pasmem +1σ. Pasmo +1σ działało jako wsparcie: świeca z 20:00 zeszła do 74 200 przy paśmie 74 191 i zamknęła się nad nim.

**Przepływ i pozycje.** W ostatnich 4 godzinach cena +381 USD, OI +100,5, delta −37,7 BTC. W ostatniej godzinie cena +239, OI +36,2, delta −98,8. Cena w górę i OI w górę to nowe longi, tylko że agresorzy w tym czasie sprzedawali, więc kupowali pasywni, limitami. Sama ujemna delta nie jest tu sygnałem, bo cena na nią nie zareagowała spadkiem. Ostatnia świeca dnia ma minutę luki na taśmie, więc jej delty nie liczę.

## Footprint wybicia z 16:30

[[footprint]]

Przed wybiciem dwie świece z 16:00 i 16:15 miały mały wolumen, 318,6 i 268,3, z POC na 73 500 i nierównowagą kupna na 73 350 przy samym dołku. Potem świeca z 16:30: wolumen 3674,4, delta +303,5, OI −349,8, czyli inicjatywa kupujących na kryciu shortów, ze stosami nierównowag kupna 73 750, 73 800, 73 850 oraz 74 350, 74 400, 74 450. Druga strona odpowiedziała od razu: długi górny knot, zamknięcie 73 890, a w świecy z 16:45 delta −344,2 przy OI +389,8 bez postępu w dół, z dołkiem 73 834. To absorpcja sprzedaży. Świece z 17:00 i 17:15 to druga fala, delta +511,7 i +555,9, ze stosami kupna od 74 000 do 74 100 i od 74 100 do 74 250. Po nich delta zmieniła znak, a wolumen spadł do 403,5 i 299,4, czyli wyczerpanie.

Linia frontu to teraz stos 74 100 do 74 250 z POC świecy 74 200, a niżej POC świecy wybicia 73 900 i stos 73 750 do 73 850. Dopóki cena trzyma się nad 74 200 i pasmem +1σ, wybicie jest zaakceptowane.

## Gdzie leży płynność

[[likwidacje]]

Nad ceną w 1% czeka 40,9 mln USD shortów do likwidacji, z największym klastrem 24,5 mln w przedziale od 74 750, a dalej 9,1 mln od 75 000 i 9,3 mln od 75 250. Pod ceną w 1% longów do likwidacji nie ma, pierwszy większy klaster to 18,5 mln od 73 500, potem 31,1 mln od 72 500. Mapa obejmuje 47% otwartych pozycji.

## Kto handluje

[[przeplywy]]

Przepływ agresorów z 24 godzin to −87,3 mln USD, prawie w całości od 80 kont wielorybów (−89,8 mln). Reszta rynku i animatorzy są blisko zera. Duzi sprzedawali do wzrostu, a funding 0,08 bp/h i premia perp −4,3 bp nie pokazują przegrzania po stronie longów.

## Kalibracja

Liczę tylko opublikowane mapy: 44 oceny dotknięć, 21 trafień (48%). Brier 0,149 wobec 0,249 dla stałej częstości, BSS 0,40. W koszykach model był dziś raczej ostrożny: przy szansach 50 do 70% (n 8, średnio 59%) dotknięć było 75%, przy 10 do 30% (n 11, średnio 21%) było 27%, a z 8 poziomów poniżej 10% nie padł żaden. Mapy dnia nakładają się, te same poziomy wracają w kilku mapach, więc to nie są niezależne próby. Przy kilkudziesięciu ocenach to wciąż w dużej mierze szum.

## Na co patrzę dalej

Na noc patrzę na dwa miejsca. Nad ceną klaster shortów od 74 750, czyli szczyt dnia; jego dotknięcie przy rosnącym OI byłoby czymś innym niż dzisiejsze krycie. Pod ceną 74 200 i pasmo +1σ VWAP; zamknięcia pod tym miejscem i powrót pod VAH 74 125 oznaczałyby, że akceptacja nad wartością się kończy. Prognoza na 4 godziny daje medianę 74 581, połowę rozkładu od 74 160 do 74 987, a 90% od 73 547 do 75 547. Zmienność 5 min z doby to 12,0 bp wobec 14,6 bp w poprzednich dniach roboczych, więc noc zaczyna się spokojniej niż zwykle.

## Rzetelność modelu

Przedziały 1 h: 90% obejmuje 92% wyników, 60% obejmuje 71% (n 1954); na 4 h odpowiednio 91% i 75% (n 1942), więc węższe przedziały są za szerokie. Dotknięcia PDH, PDL i środka: Brier 0,074 wobec 0,082 dla bazy odległości i 0,123 dla częstości bazowej, czyli BSS 0,10 wobec odległości i 0,40 wobec częstości (n 1949). Przewaga nad samą odległością jest mała.

Prawdopodobieństwa w mapach liczy model desku HAR + FHS z Monte Carlo, a każda mapa jest zapisana przed faktem i rozliczana na świecach z taśmy, z trafieniami i pudłami. Następny wpis to mapa dnia w czwartek o 08:00.
