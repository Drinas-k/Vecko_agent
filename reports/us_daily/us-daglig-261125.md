# Daglig bevakning – US-rotation
**Datum:** 2026-11-25 | **Läge:** Daglig bevakning (USD)
**Marknadsläget i korthet:** Tisdagen 24/11 föll S&P 500 **−0,50 % till 7 201,09** (intervall 7 138,93–7 223,95) och Nasdaq Composite **−1,48 % till 23 733,54** efter måndagens studs (`state/prices.json`, marketTime 2026-11-24T21:54Z resp. 22:15Z, `generatedAt` 2026-11-25T04:09Z, `schemaVersion` 2026-08-02-prevclose). **Regimfiltret är fortfarande AV:** ^GSPC ligger **2,04 % under MA200** 7 351,26 (`state/price_history.json`, 250 punkter, sista punkt 2026-11-24), mot −1,54 % i går. USD/SEK står på 10,265 (marketTime 2026-11-25T04:09Z). Thanksgiving-veckan pågår: torsdag 26/11 är NYSE stängd och fredag 27/11 är en kortdag.
**Pre-/after-hours:** Körningen startade ~13:16 UTC, före den reguljära öppningen 14:30 UTC. `state/prices.json` (04:09Z) bär bara stängningen 24/11. Websök 2026-11-25 gav ingen daterad förbörsnivå för SPY eller ^GSPC-terminerna. Förbörsläget är därför **EJ VERIFIERAT**. Det påverkar inte beslutet, eftersom sleeven saknar nivåer. DELL, WDAY och ADSK rapporterade efter stängning 24/11 och BBY samma dag (se scoutkandidaterna nedan), men ingen av dem har en utökad kurs i filen.
**Portföljvikt & kassa:** 100 % indexsleeve (SPY), 0 % kassa. Ingen av fyra aktieplatser är upptagen, och inga pending-planer är öppna.

---

## Innehav 1: Indexsleeve (SPY) (SPY / NYSE Arca)

| Aktuell kurs (källa, tidsstämpel) | Sedan entry | Stop-loss | Målkurs | DAGENS BESLUT |
|---|---|---|---|---|
| $718,78 – prices.json/Yahoo chart API, 2026-11-24 21:00 UTC, reguljär stängning | −7,05 % | – | – | **BEHÅLL** |

**Pre-/after-hours:** – (ingen utökad kurs i filen, och sleeven har inga nivåer)
**Nyheter senaste 24h:** 2026-11-24: SPY föll −0,49 % (intervall 712,14–720,92) dagen efter +4,71 % (`state/prices.json`). Websök 2026-11-25 gav inga daterade marknadsnyheter för dagen.
**Motivering:** Sleeven ligger kvar på 100 %. I LÄGE B rörs den bara när ett aktieköp eller -sälj kräver det, och i dag sker inget av det. Regimen är AV (punkt 2b), så sleeven är den enda tillåtna placeringen för alla fyra platserna. RSI(14) 40,5.

---

## Pending-planer
Inga pending-planer. Alla rader i `state/portfolj_us.md`:s Pending-sektioner är redan överstrukna (TRIGGADE eller AVFÖRDA).

**Intradag-signaler (2c/2c2):** `state/alerts.json` har `checkedAt` **2026-11-25T02:56:10Z**, alltså ~10 timmar gammalt vid körningen. Det är äldre än gränsen på ~6 timmar, så intradagsskyddet räknas som **FRÅNVARANDE** för dagens session. `active` är tom, och boken har inga nivåer att bevaka.

**Scoutkandidater (punkt 2d) – fyra nya, alla avvisade:**
- **`261125-DELL` (Dell Technologies) – AVVISAD, spärr (b): kursen kan inte verifieras.** Katalysatorn är bekräftad: Q3 FY27 24/11 efter stängning, intäkter 54,94 mdr (+103 %), justerat EPS 9,45 mot 6,59 väntat och ett återköp på 25 mdr (Dell 8-K ex. 99.1, SEC 2026-11-24, enligt scout-rapport-261125). Stängningen 295,28 (marketTime 2026-11-24T21:04Z) ligger **före** rapporten, och ingen utökad kurs finns. Kandidaten hade fallit även på **spärr (c)** (regim AV), och scouten noterar att kursen ligger 15,7 % under MA200.
- **`261125-WDAY` (Workday) – AVVISAD, spärr (b): kursen kan inte verifieras.** Katalysatorn är bekräftad: Q3 FY27 24/11 efter stängning, intäkter 2,705 mdr (+11,2 %) och höjd helårsguide (Workday 8-K ex. 99.1, SEC 2026-11-24). Stängningen 179,23 (marketTime 2026-11-24T21:00Z) är pre-event. Även spärr (c).
- **`261125-ADSK` (Autodesk) – AVVISAD, spärr (b): kursen kan inte verifieras.** Katalysatorn är bekräftad: Q3 FY27 24/11 efter stängning, intäkter 2,16 mdr (+17 %) och höjd helårsguide (Autodesk via PR Newswire 2026-11-24). Stängningen 255,70 (marketTime 2026-11-24T21:00Z) är pre-event. Även spärr (c).
- **`261125-BBY` (Best Buy) – AVVISAD, spärr (b): kursen kan inte verifieras.** Katalysatorn är bekräftad: Q3 FY27 24/11, justerat EPS 1,62 mot 1,49 och höjd helårsguide (Investing.com 2026-11-24). Kandidaten bär `price: null`, och rapporttiden är inte verifierad, så stängningen 99,62 (marketTime 2026-11-24T21:00Z) kan vara pre-event. Även spärr (c).

Avgörandena är loggade i `state/scout_candidates.json` (`decidedBy` = denna rapport, `decidedAt` 2026-11-25) och som `AVVAKTA`-rader med `price: null` i `state/decisions.json`.

**Villkorad bubblar-plan (LÄGE B):** Ingen. **PAYO** är den enda bubblaren i us-veckorapport-261123 där saknad kurs angavs som skälet (villkor 1). Den har nu en verifierad kurs, 7,17 (marketTime 2026-11-24T21:00Z, prices.json/Yahoo chart API). Den faller ändå på **villkor (5): regimfiltret är AV**. Avgörandet är loggat som en `AVVAKTA`-rad. TGT, WMT och ABNB rankades under av andra skäl (regim och teknik) och omfattas inte av regeln.

## Åtgärder i portfolj_us.md
- Inga ändringar – endast tidsstämpel uppdaterad.
- `state/decisions.json`: 6 nya rader (`book: "us"`, `mode: "B"`): BEHÅLL SPY (vikt 1,0) samt AVVAKTA DELL, WDAY, ADSK, BBY och PAYO.

## Bevakning inför imorgon
* **Torsdag 26/11 är NYSE stängd (Thanksgiving).** Nästa US-session är fredag 27/11, en kortdag med stängning 18:00 UTC.
* **Boken står i 100 % sleeve.** En ny position kräver att ^GSPC stänger över MA200 (~7 351, avstånd +2,08 % från stängningen 24/11).
* **Rapporter (`state/earnings_calendar.json`, `generatedAt` 2026-11-25T01:07Z):** DE 25/11, MRVL 1/12. Kalendern täcker bara symboler som prisbevakas, så resten av US-marknaden är **OKONTROLLERAD** (L-5).
* **DELL/WDAY/ADSK/BBY:** alla fyra är avgjorda. En ny kandidat skapas bara om scouten tar upp dem igen med en verifierad kurs efter rapporten.
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE:** schemalagda Actions kör inte under handelstimmarna. `state/prices.json` har `generatedAt` 2026-11-25T04:09Z och `state/alerts.json` har `checkedAt` 02:56Z, och ingen körning av `prices.yml` eller `monitor.yml` syns på main fram till ~13:16 UTC. **Omfång:** kurserna och intradagsskyddet för båda böckerna. **Ersättningskälla:** stängningen 24/11 i `prices.json`. Kontrollera Actions-fliken (`scheduled-actions-not-firing`).
* **Åtgärdspunkt till Dren (L-3), ÅTERKOMMANDE:** i `state/news_feed.json` står `feeds.globenewswire` och `feeds.globenewswire-earnings` fortfarande på "HTTP 403 – båda försöken". **Omfång:** 2 av 6 flöden. Fönstret täcker ändå 10 av 10 handelsdagar (`missingDays` tom). **Ersättningskälla:** websök, PR Newswire och SEC 8-K.

---
*Detta är automatiserat beslutsstöd, inte finansiell rådgivning.*
