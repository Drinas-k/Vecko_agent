# Daglig bevakning – US-rotation
**Datum:** 2026-11-18 | **Läge:** Daglig bevakning (USD)
**Marknadsläget i korthet:** Tisdagen 17/11 föll S&P 500 **−1,03 % till 7 340,53** (intervall 7 288,34–7 415,37) och Nasdaq Composite **−0,74 % till 24 328,38** (`state/prices.json`, marketTime 2026-11-17T21:42Z resp. 22:15Z, `generatedAt` 2026-11-18T02:55Z, `schemaVersion` 2026-08-02-prevclose). **Regimfiltret är nu AV:** ^GSPC stängde **0,05 % under MA200** 7 344,50 (`state/price_history.json`, 250 punkter). Marginalen var +1,01 % i går och +3,02 % i fredags. Indexet ligger under EMA20 7 560,08 och EMA50 7 615,52 och strax under EMA200 7 397,06, med RSI 37,2 och ett MACD-histogram som fallit från −8,18 till −16,81. Nasdaq ligger 3,25 % under MA200. USD/SEK står på 10,131 (marketTime 2026-11-18T02:55Z). NVIDIA (`NVDA`) rapporterade efter stängning 17/11 och slog förväntningarna (se Pending-planer). FOMC-protokollet publiceras i kväll.
**Pre-/after-hours:** Körningen startade ~13:18 UTC, före den reguljära öppningen 14:30 UTC. `state/prices.json` (02:55Z) bär bara stängningen 17/11 för SPY och CBOE. Utökade kurser finns för 8 symboler (`extendedCount`), men inte för innehaven. En websök på förbörsläget och S&P-terminer för 2026-11-18 gav ingen daterad nivå. Förbörsläget är därför **EJ VERIFIERAT**. Inget beslut hänger på det: CBOE:s stop ligger 5,02 % under senaste stängning och målet 3,36 % över, och sleeven har inga nivåer.
**Portföljvikt & kassa:** 87,5 % indexsleeve (SPY) / 12,5 % CBOE (ben 1), 0 % kassa. En av fyra aktieplatser är upptagen. Inga öppna pending-planer.

---

## Innehav 1: Indexsleeve (SPY) (SPY / NYSE Arca)

| Aktuell kurs (källa, tidsstämpel) | Sedan entry | Stop-loss | Målkurs | DAGENS BESLUT |
|---|---|---|---|---|
| $732,44 – prices.json/Yahoo chart API, 2026-11-17 21:00 UTC, reguljär stängning | −5,28 % | – | – | **BEHÅLL** |

**Pre-/after-hours:** – (ingen utökad kurs i filen, och sleeven har inga nivåer)
**Nyheter senaste 24h:** 2026-11-17: S&P 500 −1,03 %, Nasdaq −0,74 %, andra raka nedgångsdagen in i NVIDIA-rapporten. SPY handlades mellan 727,00 och 739,76 och stängde −1,01 %, på volym 1,45× 20-dagarssnittet (`state/prices.json`, `state/volume_history.json`).
**Motivering:** Sleeven har varken stop eller mål och ligger kvar på 87,5 %, eftersom inget aktieköp eller -sälj i dag kräver omviktning. Den säljs aldrig på nedgång. Med regimen AV är sleeven dessutom den enda tillåtna placeringen för de tre lediga platserna (punkt 2b).

---

## Innehav 2: Cboe Global Markets (CBOE / Cboe BZX)

| Aktuell kurs (källa, tidsstämpel) | Sedan entry | Stop-loss | Målkurs | DAGENS BESLUT |
|---|---|---|---|---|
| $370,07 – prices.json/Yahoo chart API, 2026-11-17 21:00 UTC, reguljär stängning | +10,29 % | $351,50 (avstånd −5,02 %) | $382,50 (avstånd +3,36 %) | **BEHÅLL** |

**Pre-/after-hours:** EJ VERIFIERAT (ingen utökad kurs i `state/prices.json`, ingen daterad nivå via websök).
**Nyheter senaste 24h:** 2026-11-17: CBOE föll −1,97 % till 370,07 (intervall 367,92–377,16, volym 0,87×; `state/prices.json`, `state/volume_history.json`). Websök gav inga bolagsnyheter daterade 17–18/11. De senaste daterade posterna är oktobervolymerna (PR Newswire 2026-11-04) och CFTC-stämningen (PR Newswire 2026-11-03).
**Motivering:** Tesen är intakt (Q3 30/10: justerat EPS 3,63, +36 %, sänkt opex-guide; SEC 8-K ex. 99.1). Läget har **försvagats något**: aktien gav tillbaka gårdagens uppgång och MACD-histogrammet sjunker (2,28 → 1,47), men RSI har svalnat från 75,4 till 68,9 och trenden står kvar med kurs över EMA20 348,21 > EMA50 322,92 > EMA200 296,31. Ingen nivå korsades: dagslägsta 367,92 låg över stoppen och dagshögsta 377,16 under målet. Regim AV gäller bara nyöppning och påverkar inte befintliga innehav (punkt 2b). Stoppen 351,50 lämnas orörd. CBOE har ingen rapport inom 2 handelsdagar (`state/earnings_calendar.json`).

---

## Pending-planer
Inga pending-planer. Alla rader i `state/portfolj_us.md`:s Pending-sektioner är redan överstrukna (TRIGGADE eller AVFÖRDA).

**Intradag-signaler (2c/2c2):** `state/alerts.json` har `checkedAt` **2026-11-17T23:45:01Z**, alltså ~13,5 timmar gammalt vid körningen. Monitorn har inte kört under dagens handelstimmar. Enligt punkt 2c2 räknas intradagsskyddet därför som **FRÅNVARANDE** för den här körningen. Nivåerna har prövats manuellt mot verifierad kurs ovan. `active` innehåller bara en nordisk signal (NORBT.OL), inget US-innehav.

**Scout-kandidat (punkt 2d) – en ny, avvisad:**
- **`261118-NVDA` (NVIDIA) – AVVISAD, spärr (b): kurs ej verifierbar.** Katalysatorn är bekräftad: Q3 FY27 17/11 efter stängning, intäkter 115,8 mdr USD (+103 %) mot cirka 109 väntat, justerat EPS 2,68 mot cirka 2,47, Q4-guide 130 mdr ± 3 % (NVIDIA-pressmeddelande 2026-11-17 enligt scout-rapport-261118). Den enda kursen i `state/prices.json`, stängningen **155,46** (2026-11-17 21:00 UTC), ligger **före** katalysatorn, och ingen efterbörskurs finns. Kandidaten hade dessutom fallit på **spärr (c)**, eftersom regimen är AV, och på **grind 2**: kursen ligger 23,7 % under MA200 203,87, med RSI 22,5.

**Omprövning enligt L-9 – `HD` (spärr 2e i us-veckorapport-261116):** Q3 rapporterades 17/11 före öppning. Reaktionsdagens verifierade stängning blev **339,01, −2,45 %** (intervall 334,44–346,90, marketTime 2026-11-17T21:00:03Z, prices.json/Yahoo chart API), på volym **1,59×**. Kursen ligger kvar över MA200 332,36 och EMA-stacken (EMA20 336,58 > EMA50 325,35 > EMA200 329,09) med RSI 55,3. Ändå **AVVISAD**: **regimen är AV** (punkt 2b), **grind 2** fäller den eftersom MACD-histogrammet vände negativt (0,44 → −0,61), och **grind 3** fäller den eftersom reaktionen var negativ, så det finns ingen bullish katalysator. Loggad som `AVVAKTA` med `lessonIds` L-9.

Avgörandena är loggade i `state/scout_candidates.json` (`decidedBy` = denna rapport, `decidedAt` 2026-11-18) och som `AVVAKTA`-rader i `state/decisions.json`.

**Villkorad bubblar-plan (LÄGE B):** Ingen. Villkor (5) håller inte, eftersom regimfiltret är AV. Dessutom angav us-veckorapport-261116 inte saknad verifierad kurs som skäl för någon bubblare.

## Åtgärder i portfolj_us.md
- Inga affärer. CBOE (12,5 %, stop 351,50, mål 382,50) och sleeven (87,5 %) är oförändrade. Anteckningen på CBOE-raden är kompletterad med dagens BEHÅLL.
- "Senast uppdaterad" och Kassa-sektionen är uppdaterade. Ackumulerad avkastning är oförändrad, **−6,49 %**, eftersom ingen affär stängdes.
- `state/decisions.json`: 4 nya rader (`book: "us"`, `mode: "B"`): BEHÅLL SPY (vikt 0,875), BEHÅLL CBOE, AVVAKTA NVDA (`price: null`) och AVVAKTA HD.

## Bevakning inför imorgon
* **Regimen:** ^GSPC måste stänga över MA200 (~7 344,50) för att boken ska få öppna nya positioner igen. Regeln läser stängningen, inte terminer eller NVIDIA:s efterbörsrörelse. FOMC-protokollet i kväll kan avgöra riktningen.
* **CBOE:** stoppen 351,50 ligger nu bara 5,02 % under stängningen, och målet 382,50 ligger 3,36 % över. Nästa körning prövar båda mot dagens intervall. Monitorn kör inte, så skyddet mellan körningarna saknas (se nedan).
* **NVDA:** en post-event-kurs (förbörs eller reguljär 18/11) bör fyllas av `prices.yml`. Kandidaten är ändå avgjord. Kursen under MA200 och regimen AV blockerar oavsett, så en ny prövning kräver en ny kandidat.
* **Rapporter (`state/earnings_calendar.json`, `generatedAt` 2026-11-18T02:53Z):** 18/11 `LOW` och `TGT`; 19/11 `ROST` och `WMT` (`WMT` avvisades med spärr 2e i v47 och prövas om enligt L-9 på reaktionsdagens stängning); 23/11 `HPE`. Kalendern täcker bara symboler som prisbevakas, så resten av US-marknaden är **OKONTROLLERAD** (L-5).
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE:** schemalagda Actions kör inte under handelstimmarna. `state/alerts.json` har `checkedAt` 2026-11-17T23:45Z, och `state/prices.json` har `generatedAt` 2026-11-18T02:55Z. Ingen körning av `monitor.yml` (cron 07–20 UTC) eller `prices.yml` (07:07/07:37 …) syns på main före ~13:18 UTC, och samma sak gällde i går. **Omfång:** intradagsskyddet och kurserna för båda böckerna. **Ersättningskälla:** stängningen 17/11 i `prices.json`, som är senaste handelsdagens stängning och därför verifierad för dagens beslut. Kontrollera Actions-fliken (`scheduled-actions-not-firing`).
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE:** i `state/news_feed.json` (`generatedAt` 2026-11-17T22:56Z) står `feeds.globenewswire` och `feeds.globenewswire-earnings` fortfarande på "HTTP 403 – båda försöken". **Omfång:** 2 av 6 flöden. Fönstret täcker ändå 10 av 10 handelsdagar (`missingDays` tom). **Ersättningskälla:** websök och SEC 8-K.

---
*Detta är automatiserat beslutsstöd, inte finansiell rådgivning.*
