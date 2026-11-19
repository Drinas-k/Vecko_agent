# Daglig bevakning – US-rotation
**Datum:** 2026-11-19 | **Läge:** Daglig bevakning (USD)
**Marknadsläget i korthet:** Onsdagen 18/11 föll S&P 500 **−0,23 % till 7 323,63** (intervall 7 285,76–7 367,68), medan Nasdaq Composite steg **+0,42 % till 24 429,89** (`state/prices.json`, marketTime 2026-11-18T21:57Z resp. 22:15Z, `generatedAt` 2026-11-19T02:33Z, `schemaVersion` 2026-08-02-prevclose). **Regimfiltret är fortfarande AV:** ^GSPC stängde **0,31 % under MA200** 7 346,53 (`state/price_history.json`, 250 punkter). Marginalen var −0,05 % i går. Indexet ligger under EMA20 7 537,56, EMA50 7 604,07 och EMA200 7 387,84, med RSI 36,6 och ett MACD-histogram som sjunkit från −16,81 till −21,99. NVIDIA (`NVDA`) föll −2,89 % på reaktionsdagen efter rapporten. USD/SEK står på 10,177 (marketTime 2026-11-19T02:33Z). Walmart (`WMT`) rapporterar i dag före öppning.
**Pre-/after-hours:** Körningen startade ~13:17 UTC, före den reguljära öppningen 14:30 UTC. `state/prices.json` (02:33Z) bär bara stängningen 18/11 för SPY och CBOE. Utökade kurser finns för 7 symboler (`extendedCount`), men inte för innehaven. En websök på CBOE-nyheter och förbörsläget för 2026-11-19 gav ingen daterad nivå. Förbörsläget är därför **EJ VERIFIERAT**. CBOE:s stop ligger nu bara 2,34 % under senaste stängning, så nästa körning och monitorn behöver pröva den mot dagens intervall.
**Portföljvikt & kassa:** 87,5 % indexsleeve (SPY) / 12,5 % CBOE (ben 1), 0 % kassa. En av fyra aktieplatser är upptagen. Inga öppna pending-planer.

---

## Innehav 1: Indexsleeve (SPY) (SPY / NYSE Arca)

| Aktuell kurs (källa, tidsstämpel) | Sedan entry | Stop-loss | Målkurs | DAGENS BESLUT |
|---|---|---|---|---|
| $730,20 – prices.json/Yahoo chart API, 2026-11-18 21:00 UTC, reguljär stängning | −5,57 % | – | – | **BEHÅLL** |

**Pre-/after-hours:** – (ingen utökad kurs i filen, och sleeven har inga nivåer)
**Nyheter senaste 24h:** 2026-11-18: S&P 500 −0,23 %, tredje raka nedgångsdagen. SPY handlades mellan 726,80 och 735,06 och stängde −0,31 %, på volym 1,02× 20-dagarssnittet (`state/prices.json`, `state/volume_history.json`).
**Motivering:** Sleeven har varken stop eller mål och ligger kvar på 87,5 %, eftersom inget aktieköp eller -sälj i dag kräver omviktning. Den säljs aldrig på nedgång. Med regimen AV är sleeven den enda tillåtna placeringen för de tre lediga platserna (punkt 2b).

---

## Innehav 2: Cboe Global Markets (CBOE / Cboe BZX)

| Aktuell kurs (källa, tidsstämpel) | Sedan entry | Stop-loss | Målkurs | DAGENS BESLUT |
|---|---|---|---|---|
| $359,91 – prices.json/Yahoo chart API, 2026-11-18 21:00 UTC, reguljär stängning | +7,27 % | $351,50 (avstånd −2,34 %) | $382,50 (avstånd +6,28 %) | **BEHÅLL** |

**Pre-/after-hours:** EJ VERIFIERAT (ingen utökad kurs i `state/prices.json`, ingen daterad nivå via websök).
**Nyheter senaste 24h:** 2026-11-18: CBOE föll −2,75 % till 359,91 (intervall 359,83–369,91, volym 0,84×; `state/prices.json`, `state/volume_history.json`). Varken `state/news_feed.json` (`generatedAt` 2026-11-18T22:36Z) eller websök gav bolagsnyheter daterade 18–19/11.
**Motivering:** Tesen är intakt (Q3 30/10: justerat EPS 3,63, +36 %, sänkt opex-guide; SEC 8-K ex. 99.1). Läget har **försvagats**: andra raka nedgångsdagen, stängning nära dagslägsta, och MACD-histogrammet har nästan nått noll (1,47 → 0,08). RSI har svalnat till 61,1 och trenden står kvar med kurs över EMA20 349,33 > EMA50 324,37 > EMA200 297,03. Fallet kom på låg volym (0,84×), alltså utan tecken på tvångsförsäljning. Ingen nivå korsades: dagslägsta 359,83 låg 8,33 USD över stoppen och dagshögsta 369,91 under målet. Stoppen 351,50 lämnas orörd, eftersom den aldrig flyttas ned och ingen trailing-höjning är motiverad efter en nedgång. Regim AV gäller bara nyöppning (punkt 2b). CBOE har ingen rapport inom 2 handelsdagar (`state/earnings_calendar.json`).

---

## Pending-planer
Inga pending-planer. Alla rader i `state/portfolj_us.md`:s Pending-sektioner är redan överstrukna (TRIGGADE eller AVFÖRDA).

**Intradag-signaler (2c/2c2):** `state/alerts.json` har `checkedAt` **2026-11-18T23:16:14Z**, alltså ~14 timmar gammalt vid körningen. Monitorn har inte kört under dagens handelstimmar. Enligt punkt 2c2 räknas intradagsskyddet därför som **FRÅNVARANDE** för den här körningen. Nivåerna har prövats manuellt mot verifierad kurs ovan. `active` är tom.

**Scout-kandidat (punkt 2d) – en ny, avvisad:**
- **`261119-TGT` (Target) – AVVISAD, spärr (c): regimen är av, så inga nya positioner öppnas.** Katalysatorn är bekräftad: Q3 2026 18/11 före öppning, försäljning 27,1 mdr USD (+7,1 %), jämförbar försäljning +5,6 %, justerat EPS 2,65 mot 2,07 väntat, och helårsguiden höjd (CNBC och Target 8-K ex. 99, SEC 2026-11-18, enligt scout-rapport-261119). Reaktionsdagens verifierade stängning blev **165,93, +4,01 %** (intervall 159,95–171,91, marketTime 2026-11-18T21:03:24Z, prices.json/Yahoo chart API), på volym **3,14×**. Kursen ligger 20,66 % över MA200 137,52, och EMA-stacken håller (EMA20 159,12 > EMA50 156,41 > EMA200 138,47) med RSI 60,2 och stigande MACD-histogram (0,35 → 0,58). Tekniken hade alltså inte fällt den, men ^GSPC ligger 0,31 % under MA200, och spärren gäller före grindprövningen. Scouten noterar dessutom att 0,50 USD av EPS är en tullåterbetalning.

**Omprövning enligt L-9:**
- **`NVDA` (spärr 2e i us-veckorapport-261116, rapport 17/11 efter stängning):** I går fanns ingen verifierad kurs efter rapporten. Reaktionsdagens verifierade stängning blev **150,96, −2,89 %** (intervall 150,40–159,70, marketTime 2026-11-18T21:00:00Z, prices.json/Yahoo chart API), på volym **1,49×**. **AVVISAD:** regimen är AV (punkt 2b), **grind 2** fäller den (kursen ligger 25,90 % under MA200 203,72 och under EMA20 183,08, EMA50 200,90 och EMA200 203,56, med RSI 21,1), och **grind 3** fäller den eftersom reaktionen på en slagen rapport var negativ. Loggad som `AVVAKTA` med `lessonIds` L-9.
- **`WMT` (spärr 2e, rapport 19/11):** **Inte prövad i dag.** Reaktionsdagen är i dag, och ingen verifierad stängning efter rapporten finns än. `state/prices.json` har bara stängningen 18/11, 127,36, plus en efterbörskurs 127,56 från 2026-11-19T00:58Z, och båda ligger före rapporten. Prövas i nästa LÄGE B-körning, fredag 20/11, som ligger inom 5 handelsdagar från rotationen.
- `HD` prövades och avvisades i går (us-daglig-261118).

Avgörandet för TGT är loggat i `state/scout_candidates.json` (`decidedBy` = denna rapport, `decidedAt` 2026-11-19). Både TGT och NVDA har loggats som `AVVAKTA`-rader i `state/decisions.json`.

**Villkorad bubblar-plan (LÄGE B):** Ingen. Villkor (5) håller inte, eftersom regimfiltret är AV. Dessutom angav us-veckorapport-261116 inte saknad verifierad kurs som skäl för någon bubblare.

## Åtgärder i portfolj_us.md
- Inga affärer. CBOE (12,5 %, stop 351,50, mål 382,50) och sleeven (87,5 %) är oförändrade. Anteckningen på CBOE-raden har kompletterats med dagens BEHÅLL.
- "Senast uppdaterad" är uppdaterad. Ackumulerad avkastning är oförändrad, **−6,49 %**, eftersom ingen affär stängdes.
- `state/decisions.json`: 4 nya rader (`book: "us"`, `mode: "B"`): BEHÅLL SPY (vikt 0,875), BEHÅLL CBOE, AVVAKTA TGT och AVVAKTA NVDA.

## Bevakning inför imorgon
* **CBOE:** stoppen 351,50 ligger bara 2,34 % under stängningen, jämfört med en genomsnittlig dagsrörelse på cirka 2,0 % (60 dagar, `state/price_history.json`). En vanlig nedgångsdag kan alltså utlösa den. Monitorn kör inte under börstid, så nästa prövning blir sannolikt först i morgondagens körning, mot dagens intervall.
* **Regimen:** ^GSPC måste stänga över MA200 (~7 346,5) för att boken ska få öppna nya positioner igen. Avståndet ökade från −0,05 % till −0,31 %.
* **WMT:** prövas enligt L-9 på dagens stängning i morgondagens körning.
* **Rapporter (`state/earnings_calendar.json`, `generatedAt` 2026-11-19T02:31Z):** 19/11 `ROST` och `WMT`; 23/11 `HPE`; 24/11 `CLSK` (gissat datum); 25/11 `DE`. Kalendern täcker bara symboler som prisbevakas, så resten av US-marknaden är **OKONTROLLERAD** (L-5).
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE (tredje dagen i rad):** schemalagda Actions kör inte under handelstimmarna. `state/alerts.json` har `checkedAt` 2026-11-18T23:16Z, och `state/prices.json` har `generatedAt` 2026-11-19T02:33Z. Ingen körning av `monitor.yml` eller `prices.yml` syns på main mellan 02:33 och ~13:17 UTC. **Omfång:** intradagsskyddet och kurserna för båda böckerna. Det är särskilt kännbart nu när CBOE:s stop ligger 2,34 % bort. **Ersättningskälla:** stängningen 18/11 i `prices.json`, som är senaste handelsdagens stängning och därför verifierad för dagens beslut. Kontrollera Actions-fliken (`scheduled-actions-not-firing`).
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE:** i `state/news_feed.json` (`generatedAt` 2026-11-18T22:36Z) står `feeds.globenewswire` och `feeds.globenewswire-earnings` fortfarande på "HTTP 403 – båda försöken". **Omfång:** 2 av 6 flöden. Fönstret täcker ändå 10 av 10 handelsdagar (`missingDays` tom). **Ersättningskälla:** websök och SEC 8-K.

---
*Detta är automatiserat beslutsstöd, inte finansiell rådgivning.*
