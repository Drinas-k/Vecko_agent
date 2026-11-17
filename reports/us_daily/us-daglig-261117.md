# Daglig bevakning – US-rotation
**Datum:** 2026-11-17 | **Läge:** Daglig bevakning (USD)
**Marknadsläget i korthet:** Måndagen 16/11 föll S&P 500 **−1,92 % till 7 416,59** (intervall 7 400,15–7 515,60) och Nasdaq Composite **−2,49 % till 24 509,76** (`state/prices.json`, marketTime 2026-11-16T22:22Z resp. 22:15Z, `generatedAt` 2026-11-17T03:48Z, `schemaVersion` 2026-08-02-prevclose). Nasdaq ligger nu **2,52 % under sitt MA200** 25 142,61. **Regimfiltret är ändå PÅ:** ^GSPC ligger **+1,01 %** över MA200 7 342,68 (`state/price_history.json`, 250 punkter), men marginalen har krympt från +3,02 % i fredags. Indexet ligger under EMA20 7 583,19 och EMA50 7 626,74 och strax över EMA200 7 395,57, med RSI 40,2 och ett MACD-histogram som fallit från −0,83 till −8,18. USD/SEK står på 10,0872 (marketTime 2026-11-17T03:48Z). NVIDIA (`NVDA`) och Home Depot (`HD`) rapporterar i dag (`state/earnings_calendar.json`, `isEstimate: false`).
**Pre-/after-hours:** Körningen startade ~13:18 UTC, före den reguljära öppningen 14:30 UTC. `state/prices.json` (03:48Z) bär bara stängningen 16/11 för SPY och CBOE och saknar utökade kurser (`extendedCount`). En websök på förbörsläget och S&P-terminer för 2026-11-17 gav ingen daterad nivå. Förbörsläget är därför **EJ VERIFIERAT**. Inget beslut hänger på det: CBOE:s stop ligger 6,89 % under senaste stängning, och sleeven har inga nivåer. Målet ligger dock bara 1,32 % bort och kan nås i dag (se Bevakning).
**Portföljvikt & kassa:** 87,5 % indexsleeve (SPY) / 12,5 % CBOE (ben 1), 0 % kassa. En av fyra aktieplatser är upptagen. Inga öppna pending-planer.

---

## Innehav 1: Indexsleeve (SPY) (SPY / NYSE Arca)

| Aktuell kurs (källa, tidsstämpel) | Sedan entry | Stop-loss | Målkurs | DAGENS BESLUT |
|---|---|---|---|---|
| $739,95 – prices.json/Yahoo chart API, 2026-11-16 21:00 UTC, reguljär stängning | −4,31 % | – | – | **BEHÅLL** |

**Pre-/after-hours:** – (ingen utökad kurs i filen, och sleeven har inga nivåer)
**Nyheter senaste 24h:** 2026-11-16: S&P 500 −1,92 %, Nasdaq −2,49 %. SPY handlades mellan 738,07 och 749,82 och stängde −1,91 %, på volym 1,47× 20-dagarssnittet (`state/prices.json`, `state/volume_history.json`). Ingen daterad förklaring till nedgången kunde verifieras via websök.
**Motivering:** Sleeven har varken stop eller mål och ligger kvar på 87,5 %, eftersom inget aktieköp eller -sälj i dag kräver omviktning. Den säljs aldrig på nedgång. Kursen ligger 1,06 % över MA200 732,16 men under EMA20 756,10 och EMA50 760,40.

---

## Innehav 2: Cboe Global Markets (CBOE / Cboe BZX)

| Aktuell kurs (källa, tidsstämpel) | Sedan entry | Stop-loss | Målkurs | DAGENS BESLUT |
|---|---|---|---|---|
| $377,50 – prices.json/Yahoo chart API, 2026-11-16 21:00 UTC, reguljär stängning | +12,51 % | $351,50 (avstånd −6,89 %) | $382,50 (avstånd +1,32 %) | **BEHÅLL** |

**Pre-/after-hours:** EJ VERIFIERAT (ingen utökad kurs i `state/prices.json`, ingen daterad nivå via websök).
**Nyheter senaste 24h:** 2026-11-16: CBOE steg +0,55 % till 377,50 på en dag då S&P 500 föll −1,92 %. Dagshögsta 379,76 är ett nytt 250-dagarshögsta. Volymen var 0,89× (`state/prices.json`, `state/volume_history.json`). `state/news_feed.json` (`generatedAt` 2026-11-16T23:45Z) har inga CBOE-poster. Websök gav inga bolagsnyheter daterade 16–17/11. De senaste daterade posterna är oktobervolymerna (4/11) och CMA-stämningen mot CFTC (3/11).
**Motivering:** Tesen är intakt (Q3 30/10: justerat EPS 3,63, +36 %, sänkt opex-guide; SEC 8-K ex. 99.1). Läget har **stärkts relativt marknaden**: aktien steg mot ett fallande index och nådde nytt högsta. Uppgången börjar dock bli sträckt, med RSI 75,4 och ett MACD-histogram som sjunker (2,38 → 2,28). Ingen nivå korsades: dagslägsta 372,05 låg över stoppen och dagshögsta 379,76 under målet. Trenden står kvar, med kurs över EMA20 345,91 > EMA50 321,00 > EMA200 295,97. Stoppen 351,50 (flyttad upp i v47) lämnas orörd, eftersom inget nytt swingstöd har bildats inom 5–6 %-bandet. CBOE har ingen rapport inom 2 handelsdagar (`state/earnings_calendar.json`).

---

## Pending-planer
Inga pending-planer. Alla rader i `state/portfolj_us.md`:s Pending-sektioner är redan överstrukna (TRIGGADE eller AVFÖRDA).

**Intradag-signaler (2c/2c2):** `state/alerts.json` har `checkedAt` **2026-11-17T00:39:15Z**, alltså ~12,6 timmar gammalt vid körningen. Monitorn har inte kört under dagens handelstimmar (cron varje timme 07–20 UTC). Enligt punkt 2c2 räknas intradagsskyddet därför som **FRÅNVARANDE** för den här körningen. Nivåerna har prövats manuellt mot verifierad kurs ovan. `active` är tom.

**Scout-kandidat (punkt 2d) – en ny, avvisad:**
- **`261117-BIIB` (Biogen) – AVVISAD, spärr (b): kurs ej verifierbar.** Katalysatorn är bekräftad: femårsdata för Leqembi presenterades på CTAD 16/11 23:00 UTC (Biogen via PR Newswire och mfn, BioArctic via mfn 23:05 UTC; `state/news_feed.json`). Den enda kursen i `state/prices.json`, stängningen **251,65** (2026-11-16 21:00 UTC), ligger dock **före** katalysatorn. Ingen daterad förbörskurs gick att verifiera via websök. Kandidaten hade dessutom fallit på **grind 2**: volym 0,69× och ett fallande MACD-histogram (−0,62 → −0,75). Trendstacken är däremot hel, med kurs 22,4 % över MA200 205,51 och RSI 57,1.

Avgörandet är loggat i `state/scout_candidates.json` (`decidedBy` = denna rapport, `decidedAt` 2026-11-17) och som en `AVVAKTA`-rad i `state/decisions.json`.

**Villkorad bubblar-plan (LÄGE B):** Ingen bubblare omfattas. us-veckorapport-261116 angav inte saknad verifierad kurs som skäl för någon bubblare (alla fyra har kurs, L-2). `HD` rankades under på grund av rapporten 17/11 och prövas om enligt L-9 på reaktionsdagens verifierade stängning. Den finns ännu inte vid körningen, eftersom den reguljära sessionen inte har öppnat.

## Åtgärder i portfolj_us.md
- Inga affärer. CBOE (12,5 %, stop 351,50, mål 382,50) och sleeven (87,5 %) är oförändrade. Anteckningen på CBOE-raden är kompletterad med dagens BEHÅLL.
- "Senast uppdaterad" och Kassa-sektionen är uppdaterade. Ackumulerad avkastning är oförändrad, **−6,49 %**, eftersom ingen affär stängdes.
- `state/decisions.json`: 3 nya rader (`book: "us"`, `mode: "B"`): BEHÅLL SPY (vikt 0,875), BEHÅLL CBOE och AVVAKTA BIIB.

## Bevakning inför imorgon
* **CBOE nära målet:** mål 382,50 ligger 1,32 % över stängningen och 0,72 % över gårdagens dagshögsta. Nås det intradag ska monitorn larma (`basis: "intraday"`), men den har inte kört i dag (se nedan). Nästa körning prövar målet mot dagens dagshögsta.
* **Regimmarginalen är tunn:** ^GSPC ligger bara 1,01 % över MA200 (7 342,68). En stängning under nivån stänger boken för nya positioner (punkt 2b). Befintliga innehav berörs inte.
* **Rapporter (`state/earnings_calendar.json`, `generatedAt` 2026-11-17T00:31Z):** 17/11 `NVDA`, `HD` och `DLB`; 18/11 `LOW` och `TGT`; 19/11 `ROST` och `WMT`. `NVDA` rapporterar efter stängning och är en tung S&P 500-vikt, så rapporten kan slå mot sleeven. `HD` prövas om på reaktionsdagens stängning (L-9). Kalendern täcker bara symboler som prisbevakas, så resten av US-marknaden är **OKONTROLLERAD** (L-5).
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE:** schemalagda Actions har inte kört under dagens handelstimmar. `state/alerts.json` har `checkedAt` 2026-11-17T00:39Z, och `state/prices.json` har `generatedAt` 2026-11-17T03:48Z. Ingen körning av `monitor.yml` (cron 07–20 UTC) eller `prices.yml` (07:07/07:37 …) syns på main före ~13:18 UTC. **Omfång:** intradagsskyddet och kurserna för båda böckerna, alltså samtliga 282 symboler i `prices.json`. **Ersättningskälla:** stängningen 16/11 i `prices.json`, som är senaste handelsdagens stängning och därför verifierad för dagens beslut. Kontrollera Actions-fliken (`scheduled-actions-not-firing`).
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE:** i `state/news_feed.json` (`generatedAt` 2026-11-16T23:45Z) står `feeds.globenewswire` och `feeds.globenewswire-earnings` på "HTTP 403 – båda försöken". **Omfång:** 2 av 6 flöden. Fönstret täcker ändå 10 av 10 handelsdagar (`missingDays` tom). **Ersättningskälla:** websök och SEC 8-K.

---
*Detta är automatiserat beslutsstöd, inte finansiell rådgivning.*
