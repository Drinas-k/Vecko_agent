# Daglig bevakning – US-rotation
**Datum:** 2026-11-24 | **Läge:** Daglig bevakning (USD)
**Marknadsläget i korthet:** Måndagen 23/11 steg S&P 500 **+4,73 % till 7 237,17** (intervall 7 152,66–7 295,60) och Nasdaq Composite **+6,51 % till 24 089,56** (`state/prices.json`, marketTime 2026-11-23T21:42Z resp. 22:15Z, `generatedAt` 2026-11-24T05:19Z, `schemaVersion` 2026-08-02-prevclose). Studsen kom efter fem raka nedgångsdagar. **Regimfiltret är fortfarande AV:** ^GSPC ligger **1,54 % under MA200** 7 350,08 (`state/price_history.json`, 250 punkter), mot −5,96 % i fredags. RSI(14) är 41,3. USD/SEK står på 10,273 (marketTime 2026-11-24T05:19Z). Thanksgiving-veckan pågår: torsdag 26/11 är NYSE stängd och fredag 27/11 är en kortdag.
**Pre-/after-hours:** Körningen startade ~13:18 UTC, före den reguljära öppningen 14:30 UTC. `state/prices.json` (05:19Z) bär bara stängningen 23/11 för SPY och CBOE. Websök gav ingen daterad förbörsnivå för 2026-11-24. Förbörsläget är därför **EJ VERIFIERAT**, men det påverkar inte dagens beslut: CBOE:s stop bröts redan i den reguljära sessionen 23/11. HPE och ZM rapporterade efter stängning 23/11 (se scoutkandidaterna nedan).
**Portföljvikt & kassa:** 100 % indexsleeve (SPY), 0 % kassa efter dagens försäljning av CBOE (12,5 %). Ingen av fyra aktieplatser är upptagen, och inga pending-planer är öppna.

---

## Innehav 1: Indexsleeve (SPY) (SPY / NYSE Arca)

| Aktuell kurs (källa, tidsstämpel) | Sedan entry | Stop-loss | Målkurs | DAGENS BESLUT |
|---|---|---|---|---|
| $722,29 – prices.json/Yahoo chart API, 2026-11-23 21:00 UTC, reguljär stängning | −6,59 % | – | – | **BEHÅLL** (ökad 87,5 % → 100 %) |

**Pre-/after-hours:** – (ingen utökad kurs i filen, och sleeven har inga nivåer)
**Nyheter senaste 24h:** 2026-11-23: SPY steg +4,71 % (intervall 713,54–727,97) i en bred studs efter fem raka nedgångsdagar (`state/prices.json`).
**Motivering:** Sleeven ökas med CBOE:s 12,5 % till 100 %. Ett aktiesälj är det enda tillåtna skälet att röra sleeven i LÄGE B. Eftersom regimen är AV (punkt 2b) är sleeven den enda tillåtna placeringen för alla fyra platserna.

---

## Innehav 2: Cboe Global Markets (CBOE / Cboe BZX)

| Aktuell kurs (källa, tidsstämpel) | Sedan entry | Stop-loss | Målkurs | DAGENS BESLUT |
|---|---|---|---|---|
| $354,67 – prices.json/Yahoo chart API, 2026-11-23 21:00 UTC, reguljär stängning (dagslägsta 350,55) | +5,70 % (exit 351,50: +4,76 %) | $351,50 – **BRUTEN** | $382,50 | **SÄLJ** |

**Pre-/after-hours:** EJ VERIFIERAT (ingen utökad kurs i `state/prices.json`, ingen daterad nivå via websök). Det är inte avgörande, eftersom stoppen bröts i den reguljära sessionen.
**Nyheter senaste 24h:** 2026-11-23: CBOE handlades mellan 364,98 och **350,55** och stängde −0,85 % på 354,67, på volym 1,33× 20-dagarssnittet (`state/prices.json`, `state/volume_history.json`). Aktien föll samma dag som index steg +4,73 %, vilket ser ut som en rotation ut ur volatilitetsvinnarna när VIX-läget lugnade sig. Det är en tolkning, inte en verifierad nyhet. Varken `state/news_feed.json` (`generatedAt` 2026-11-24T03:21Z) eller websök gav bolagsnyheter daterade 23–24/11.
**Motivering:** Stoppen **351,50 bröts i sessionen 23/11** (dagslägsta 350,55), och monitorn larmade (`state/alerts.json`: SÄLJ, `basis: "intraday"`, `hitPrice` 350,55, `checkedAt` 2026-11-24T04:15Z). Ingen gapöppning skedde genom nivån (föregående stängning 357,71, dagshögsta 364,98), så exit bokförs till stoppnivån 351,50 enligt bokens konvention. Utfallet blir **+4,76 %** på 12,5 % vikt efter 15 handelsdagar. ^GSPC föll −4,52 % från 30/10 (entrykursens datum) till 23/11, vilket ger alpha **+9,28 pp**. Realiserad R/R är **+0,82** (4,76 / 5,82 planerat stoppavstånd). Det uppflyttade stoppet säkrade alltså en vinst. Kapitalet går till SPY-sleeven.

---

## Pending-planer
Inga pending-planer. Alla rader i `state/portfolj_us.md`:s Pending-sektioner är redan överstrukna (TRIGGADE eller AVFÖRDA).

**Intradag-signaler (2c/2c2):** `state/alerts.json` har `checkedAt` **2026-11-24T04:15:21Z**, alltså ~9 timmar gammalt vid körningen. Det är äldre än gränsen på ~6 timmar. Monitorn körde dock under gårdagens US-session (`generatedAt` 2026-11-23T18:59Z) och fångade CBOE-korsningen. För dagens session räknas intradagsskyddet ändå som **FRÅNVARANDE** enligt 2c2. Den enda aktiva signalen (CBOE SÄLJ) hanteras ovan, och efter försäljningen har boken inga nivåer att bevaka.

**Scoutkandidater (punkt 2d) – två nya, båda avvisade:**
- **`261124-HPE` (Hewlett Packard Enterprise) – AVVISAD, spärr (b): kursen kan inte verifieras.** Katalysatorn är bekräftad: Q4 FY26 23/11 efter stängning, intäkter 14,5 mdr (+50 %), justerat EPS 1,43 mot guidning 1,20–1,30, FY27-guide EPS 5,05–5,35 och ett återköp på 5 mdr (HPE 8-K ex. 99.1, SEC 2026-11-23, enligt scout-rapport-261124). Stängningen 48,02 (marketTime 2026-11-23T21:04Z) ligger **före** rapporten, och `state/prices.json` har ingen utökad kurs för HPE. Kandidaten hade fallit även på **spärr (c)** (regim AV). Scouten anger dessutom en efterhandel på ca −7 % på en svag Q1-guide.
- **`261124-ZM` (Zoom Communications) – AVVISAD, spärr (b): kursen kan inte verifieras.** Katalysatorn är bekräftad: Q3 FY27 23/11 efter stängning, intäkter 1 290,6 MUSD (+4,9 %), justerat EPS 1,59 mot 1,49 väntat och en första utdelning på 0,25 per kvartal (GlobeNewswire 2026-11-23, enligt scout-rapport-261124). Stängningen 86,03 (marketTime 2026-11-23T21:00Z) ligger före rapporten, och ingen utökad kurs finns. Kandidaten hade fallit även på **spärr (c)** (regim AV), och scouten noterar att kursen ligger under MA200.

Avgörandena är loggade i `state/scout_candidates.json` (`decidedBy` = denna rapport, `decidedAt` 2026-11-24) och som `AVVAKTA`-rader med `price: null` i `state/decisions.json`.

**Villkorad bubblar-plan (LÄGE B):** Ingen, eftersom villkor (5) inte håller (regimfiltret är AV).

## Åtgärder i portfolj_us.md
- **SÄLJ CBOE:** positionen är flyttad till Historik (exit 351,50, +4,76 %, vikt 12,5 %, STOPP). Raden är borttagen ur Aktuellt innehav.
- Sleeven SPY är ökad 87,5 % → **100 %**. Kassa 0 %.
- **Ackumulerad avkastning är omräknad direkt:** 0,93512 × (1 + 0,125 × 0,0476) = 0,94068 ⇒ **−5,93 %** (från −6,49 %), på sju stängda affärer.
- `state/decisions.json`: 4 nya rader (`book: "us"`, `mode: "B"`): SÄLJ CBOE, BEHÅLL SPY (vikt 1,0), AVVAKTA HPE och AVVAKTA ZM.

## Bevakning inför imorgon
* **Boken står i 100 % sleeve.** En ny position kräver att ^GSPC stänger över MA200 (~7 350, avstånd +1,56 % från stängningen 23/11).
* **Rapporter (`state/earnings_calendar.json`, `generatedAt` 2026-11-24T03:04Z):** 24/11 ADI, ADSK, BBY, DELL, HPQ, MDT, WDAY och CLSK; 25/11 DE. Kalendern täcker bara symboler som prisbevakas, så resten av US-marknaden är **OKONTROLLERAD** (L-5).
* **HPE/ZM:** båda är avgjorda. En ny kandidat skapas bara om scouten tar upp dem igen med en verifierad kurs efter rapporten.
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE:** schemalagda Actions kör inte under handelstimmarna. `state/prices.json` har `generatedAt` 2026-11-24T05:19Z och `state/alerts.json` har `checkedAt` 04:15Z, och ingen körning av `prices.yml` eller `monitor.yml` syns på main fram till ~13:18 UTC. **Omfång:** kurserna och intradagsskyddet för båda böckerna. **Ersättningskälla:** stängningen 23/11 i `prices.json`. Kontrollera Actions-fliken (`scheduled-actions-not-firing`).
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE:** i `state/news_feed.json` står `feeds.globenewswire` och `feeds.globenewswire-earnings` fortfarande på "HTTP 403 – båda försöken". **Omfång:** 2 av 6 flöden. Fönstret täcker ändå 10 av 10 handelsdagar (`missingDays` tom). **Ersättningskälla:** websök och SEC 8-K.

---
*Detta är automatiserat beslutsstöd, inte finansiell rådgivning.*
