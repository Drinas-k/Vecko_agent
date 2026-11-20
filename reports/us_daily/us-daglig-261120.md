# Daglig bevakning – US-rotation
**Datum:** 2026-11-20 | **Läge:** Daglig bevakning (USD)
**Marknadsläget i korthet:** Torsdagen 19/11 föll S&P 500 **−2,02 % till 7 175,83**. Dagens intervall var 7 173,63–7 415,64, så indexet vände ned från plus och stängde nära dagslägsta. Nasdaq Composite föll **−2,26 % till 23 879,20** (`state/prices.json`, marketTime 2026-11-19T21:59Z resp. 22:15Z, `generatedAt` 2026-11-20T02:19Z, `schemaVersion` 2026-08-02-prevclose). **Regimfiltret är fortfarande AV, nu med bredare marginal:** ^GSPC ligger **2,34 % under MA200** 7 347,99 (`state/price_history.json`, 250 punkter), mot −0,31 % i går. Indexet ligger under EMA20 7 503,11, EMA50 7 587,28 och EMA200 7 391,00, med RSI 31,4 och ett MACD-histogram som sjunkit från −21,99 till −33,03. USD/SEK står på 10,199 (marketTime 2026-11-20T02:19Z). Walmart (`WMT`) rapporterade Q3 FY27 i går före öppning och föll −1,04 %.
**Pre-/after-hours:** Körningen startade ~13:17 UTC, före den reguljära öppningen 14:30 UTC. `state/prices.json` (02:19Z) bär bara stängningen 19/11 för SPY och CBOE. Utökade kurser finns för 4 symboler (`extendedCount`: CLSK, HPE, FRO.OL, NYKD.OL), men inte för innehaven. Websök på CBOE och på förbörsläget för 2026-11-20 gav ingen daterad nivå. Förbörsläget är därför **EJ VERIFIERAT**. CBOE:s stop ligger nu bara 1,73 % under senaste stängning.
**Portföljvikt & kassa:** 87,5 % indexsleeve (SPY) / 12,5 % CBOE (ben 1), 0 % kassa. En av fyra aktieplatser är upptagen. Inga öppna pending-planer.

---

## Innehav 1: Indexsleeve (SPY) (SPY / NYSE Arca)

| Aktuell kurs (källa, tidsstämpel) | Sedan entry | Stop-loss | Målkurs | DAGENS BESLUT |
|---|---|---|---|---|
| $715,87 – prices.json/Yahoo chart API, 2026-11-19 21:00 UTC, reguljär stängning | −7,42 % | – | – | **BEHÅLL** |

**Pre-/after-hours:** – (ingen utökad kurs i filen, och sleeven har inga nivåer)
**Nyheter senaste 24h:** 2026-11-19: S&P 500 −2,02 %, fjärde raka nedgångsdagen. SPY handlades mellan 715,65 och 739,90 och stängde −1,96 %, på volym 1,51× 20-dagarssnittet (`state/prices.json`, `state/volume_history.json`).
**Motivering:** Sleeven har varken stop eller mål och ligger kvar på 87,5 %, eftersom inget aktieköp eller -sälj i dag kräver omviktning. Den säljs aldrig på nedgång. Med regimen AV är sleeven den enda tillåtna placeringen för de tre lediga platserna (punkt 2b).

---

## Innehav 2: Cboe Global Markets (CBOE / Cboe BZX)

| Aktuell kurs (källa, tidsstämpel) | Sedan entry | Stop-loss | Målkurs | DAGENS BESLUT |
|---|---|---|---|---|
| $357,69 – prices.json/Yahoo chart API, 2026-11-19 21:00 UTC, reguljär stängning | +6,60 % | $351,50 (avstånd −1,73 %) | $382,50 (avstånd +6,94 %) | **BEHÅLL** |

**Pre-/after-hours:** EJ VERIFIERAT (ingen utökad kurs i `state/prices.json`, ingen daterad nivå via websök).
**Nyheter senaste 24h:** 2026-11-19: CBOE föll −0,62 % till 357,69 (intervall 354,08–360,055, volym 0,75×; `state/prices.json`, `state/volume_history.json`). Den tappade alltså klart mindre än index (−2,02 %). Varken `state/news_feed.json` (`generatedAt` 2026-11-19T22:40Z) eller websök gav bolagsnyheter daterade 19–20/11.
**Motivering:** Tesen är intakt (Q3 30/10: justerat EPS 3,63, +36 %, sänkt opex-guide; SEC 8-K ex. 99.1). Ingen nivå korsades: dagslägsta 354,08 låg 2,58 USD över stoppen och dagshögsta 360,055 under målet. Läget har **försvagats ytterligare**: tredje raka nedgångsdagen, och MACD-histogrammet har gått negativt (0,08 → −1,09). Trenden står kvar med kurs över EMA20 350,12 > EMA50 325,68 > EMA200 297,41, RSI är 59,5, och fallet kom på låg volym (0,75×). Stoppen 351,50 lämnas orörd, eftersom den aldrig flyttas ned och ingen trailing-höjning är motiverad efter en nedgång. Regim AV gäller bara nyöppning (punkt 2b). CBOE har ingen rapport inom 2 handelsdagar (`state/earnings_calendar.json`).

---

## Pending-planer
Inga pending-planer. Alla rader i `state/portfolj_us.md`:s Pending-sektioner är redan överstrukna (TRIGGADE eller AVFÖRDA).

**Intradag-signaler (2c/2c2):** `state/alerts.json` har `checkedAt` **2026-11-19T23:24:34Z**, alltså ~14 timmar gammalt vid körningen. Monitorn har inte kört under dagens handelstimmar. Enligt punkt 2c2 räknas intradagsskyddet därför som **FRÅNVARANDE** för den här körningen. Nivåerna har prövats manuellt mot verifierad kurs ovan. `active` är tom.

**Scout-kandidat (punkt 2d) – en ny, avvisad:**
- **`261120-WMT` (Walmart) – AVVISAD, spärr (c): regimen är av, så inga nya positioner öppnas.** Katalysatorn är bekräftad: Q3 FY27 19/11 före öppning, intäkter 188,8 mdr USD (+5,2 %) mot 187,2 väntat, justerat EPS 0,65 mot 0,64, e-handel +17 % och helårsguiden höjd till EPS 2,84–2,89 (Proactive Investors, Supermarket News, Benzinga 2026-11-19, enligt scout-rapport-261120). Reaktionsdagens verifierade stängning blev **126,04, −1,04 %** (intervall 123,29–126,95, marketTime 2026-11-19T21:00:01Z, prices.json/Yahoo chart API), på volym **1,43×**. Spärren gäller före grindprövningen, men kandidaten hade fallit även utan den: **grind 2** (volym 1,43× under kravet 1,5×, MACD-histogram fallande −0,26 → −0,42) och **grind 3** (negativ reaktion på ett litet slag). Kursen ligger 5,93 % över MA200 118,99, med EMA20 124,39 > EMA50 119,16 > EMA200 116,05 och RSI 59,8.

**Omprövning enligt L-9:**
- **`WMT` (spärr 2e i us-veckorapport-261116, rapport 19/11):** Prövad i dag på reaktionsdagens verifierade stängning, se ovan. **AVVISAD** (regim AV, grind 2, grind 3). En gemensam `AVVAKTA`-rad täcker både scoutkandidaten och L-9-omprövningen (`lessonIds` L-9).
- Samtliga tre namn som avvisades med spärr 2e i us-veckorapport-261116 har nu fått ett nytt avgörande: `HD` (us-daglig-261118), `NVDA` (us-daglig-261119) och `WMT` (i dag).

Avgörandet för WMT är loggat i `state/scout_candidates.json` (`decidedBy` = denna rapport, `decidedAt` 2026-11-20) och som `AVVAKTA`-rad i `state/decisions.json`.

**Villkorad bubblar-plan (LÄGE B):** Ingen. Villkor (5) håller inte, eftersom regimfiltret är AV. Dessutom angav us-veckorapport-261116 inte saknad verifierad kurs som skäl för någon bubblare.

## Åtgärder i portfolj_us.md
- Inga affärer. CBOE (12,5 %, stop 351,50, mål 382,50) och sleeven (87,5 %) är oförändrade. Anteckningen på CBOE-raden har kompletterats med dagens BEHÅLL.
- "Senast uppdaterad" är uppdaterad. Ackumulerad avkastning är oförändrad, **−6,49 %**, eftersom ingen affär stängdes.
- `state/decisions.json`: 3 nya rader (`book: "us"`, `mode: "B"`): BEHÅLL SPY (vikt 0,875), BEHÅLL CBOE och AVVAKTA WMT.

## Bevakning inför imorgon
* **Nästa körning är måndag 2026-11-23 (LÄGE A, v48).** Den ska pröva CBOE:s stop mot fredagens intervall.
* **CBOE:** stoppen 351,50 ligger bara 1,73 % under stängningen, jämfört med en genomsnittlig dagsrörelse på cirka 2,0 % (60 dagar, `state/price_history.json`). En vanlig nedgångsdag kan alltså utlösa den. Monitorn kör inte under börstid.
* **Regimen:** ^GSPC måste stänga över MA200 (~7 348) för att boken ska få öppna nya positioner igen. Avståndet ökade från −0,31 % till −2,34 %.
* **Rapporter (`state/earnings_calendar.json`, `generatedAt` 2026-11-20T02:17Z):** 23/11 `HPE`; 24/11 `CLSK`; 25/11 `DE`. Kalendern täcker bara symboler som prisbevakas, så resten av US-marknaden är **OKONTROLLERAD** (L-5). Torsdag 26/11 är Thanksgiving (NYSE stängd), och fredag 27/11 är en kortdag.
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE (fjärde dagen i rad):** schemalagda Actions kör inte under handelstimmarna. `state/alerts.json` har `checkedAt` 2026-11-19T23:24Z, och `state/prices.json` har `generatedAt` 2026-11-20T02:19Z. Ingen körning av `monitor.yml` eller `prices.yml` syns på main mellan 02:19 och ~13:17 UTC. **Omfång:** intradagsskyddet och kurserna för båda böckerna. Det är särskilt kännbart nu när CBOE:s stop ligger 1,73 % bort. **Ersättningskälla:** stängningen 19/11 i `prices.json`, som är senaste handelsdagens stängning och därför verifierad för dagens beslut. Kontrollera Actions-fliken (`scheduled-actions-not-firing`).
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE:** i `state/news_feed.json` (`generatedAt` 2026-11-19T22:40Z) står `feeds.globenewswire` och `feeds.globenewswire-earnings` fortfarande på "HTTP 403 – båda försöken". **Omfång:** 2 av 6 flöden. Fönstret täcker ändå 10 av 10 handelsdagar (`missingDays` tom). **Ersättningskälla:** websök och SEC 8-K.

---
*Detta är automatiserat beslutsstöd, inte finansiell rådgivning.*
