# Veckorapport: Nordisk Rotation
**Vecka:** v 48 | **Datum:** 2026-11-23
**Marknadsklimat:** Veckan var bred riskavvecklig. OMXS30 (`^OMX`) stängde fredag på **3 175,06** (`state/prices.json`, source "Yahoo Finance (chart API)", marketTime 2026-11-20T16:35:00Z). Det är **−5,42 %** mot förra rotationens bas (fredag 2026-11-13: 3 356,87) och **−2,51 % bara på fredagen**. Nedgången följde USA: S&P 500 (`^GSPC`) gick 7 561,67 → 6 910,39 (**−8,61 %**) och Nasdaq Composite (`^IXIC`) 25 136,27 → 22 617,73 (**−10,02 %**), båda daterade stängningar 2026-11-13 → 2026-11-20 ur `state/price_history.json`. Kronan försvagades: USD/SEK 10,073 → 10,225 (+1,51 %). **Regimfiltret har slagit om till AV:** ^OMX 3 175,06 ligger **0,05 % under** MA200 **3 176,73** (200 daterade stängningar ur `state/price_history.json`, serien bär 250 punkter). Vid v47-rotationen var marginalen +5,81 % och i torsdags +2,53 %. Riksbankens nästa besked kommer 16/12.
- **Nordisk motvind:** telekom/teknik (NOKIA.HE −11,65 %, SINCH.ST −11,19 %), förnybart och energi (VWS.CO −10,85 %, NESTE.HE −10,64 %, NEL.OL −20,28 %), gruv och verkstad (BOL.ST −10,77 %, SAND.ST −10,44 %, ALLEI.ST −10,43 %) samt spel och finans (EMBRAC-B.ST −10,00 %, EQT.ST −9,37 %).
- **Relativ medvind:** bara ett fåtal namn steg. Störst uppgång hade TRUE-B.ST (+4,56 %), BAVA.CO (+3,46 %) och SUBC.OL (+2,63 %, Q3 19/11). Lax (MOWI.OL +0,18 %, SALM.OL ±0,00 %) och GMAB.CO (+0,61 %) höll emot.

**DATAFÄRSKHET.**
- `state/prices.json`: `generatedAt` **2026-11-21T02:13:44Z**, `schemaVersion` "2026-08-02-prevclose", `wideAt` 2026-11-21T02:13:44Z (331 symboler, 326 OK). Fredagens stängningar är senaste handelsdagens stängning och godkänns före öppning. Senaste kurscommit på `origin/main` är 2026-11-21 02:13 UTC (kontrollerat 06:41 UTC). Det betyder att **måndagens förbörskörningar inte har nått `main`**.
- `state/news_feed.json`: `generatedAt` 2026-11-20T22:15:20Z, alltså äldre än 24 timmar (helg). Fönstret bär **10 av 10 handelsdagar** (2026-11-09 → 2026-11-20, `missingDays` tomt). Ingen websök har gjorts i körningen. Nyhetsunderlaget är flödet plus `state/earnings_calendar.json`.
- `state/alerts.json`: `checkedAt` 2026-11-20T22:30:09Z, alltså färskt för senaste handelsdagen. `active` är tom.
- `state/movers.json`: `asOf` **2026-11-20**, förra fredagens stängning. 107 av 110 symboler är OK.
- `state/earnings_calendar.json`: `generatedAt` 2026-11-21T02:11:10Z, 236 av 257 symboler lösta, `failed` 0, 15 kommande.

---

## 0. Facit: Förra veckans val
| Aktie | Entry | Exit | Utfall | Stop/Mål träffad? |
|---|---|---|---|---|
| BOOZT.ST | 169,20 | 167,50 (öppen) | −1,00 % | Nej (dagslägsta 2026-11-20 166,80 över stop 163,00) |
| MORLD.OL | 26,40 | 26,05 (öppen) | −1,33 % | Nej (dagslägsta 2026-11-20 25,55 över stop 25,30 och punkteringsnivån 25,40) |
| HNSA.ST | 46,84 (köpt 2026-11-16) | 45,14 (öppen) | −3,63 % | Nej (dagslägsta 2026-11-20 45,10 över stop 44,50; ben 2 ≤ 45,00 ej triggat, avfört) |
| XACT-OMXS30.ST | 494,60 | 473,85 (öppen) | −4,20 % mot entry, −5,48 % på veckan | Nej (sleeven har varken stop eller mål) |

Samtliga kurser kommer ur `state/prices.json` (source "Yahoo Finance (chart API)"). Tidsstämplar (marketTime 2026-11-20): BOOZT.ST 16:29:48Z, MORLD.OL 15:25:43Z, HNSA.ST 16:29:45Z, XACT-OMXS30.ST 16:24:38Z.

**Veckans portföljutfall (viktat):** **≈ −4,7 % brutto.** Viktningen var 62,5 % sleeve och 12,5 % vardera i de tre aktierna:
- **Sleeven:** 501,30 → 473,85 (−5,48 %).
- **BOOZT.ST:** 172,40 → 167,50 (−2,84 %).
- **MORLD.OL:** 27,10 → 26,05 (−3,87 %).
- **HNSA.ST:** 46,84 → 45,14 (−3,63 %).

`^OMX` gick −5,42 % över samma period. Aktieurvalet föll alltså mindre än index, men på tre namn och en vecka är skillnaden brus. Talet är en approximation ur stängningar och vikter. Dashboardens nettosiffra drar dessutom rundturskostnaden.

**Ackumulerad avkastning sedan strategistart:** **−3,70 %** (fyra stängda affärer, alla på vikt 25 %: ASSA-B.ST −3,26 %, SALM.OL −5,48 %, SAAB-B.ST −2,70 %, KOG.OL −3,55 %). Ingen affär har stängts denna vecka. Sleevens och de öppna innehavens orealiserade rörelse ingår inte i fältet.

**Portföljallokering denna vecka:** **12,5 % BOOZT.ST + 12,5 % MORLD.OL + 12,5 % HNSA.ST + 62,5 % indexsleeve (XACT-OMXS30.ST) + 0 % kassa.** Allokeringen är oförändrad.
- Ingen ny position öppnas, eftersom **regimfiltret är AV** (punkt 2b, hård spärr). Den lediga platsen och de tre halva positionerna ligger kvar i sleeven.
- Ben 2 för HNSA.ST (≤ 45,00) **avfördes**: det triggade inte inom 5 handelsdagar (lägsta dagslägsta 45,10 den 20/11). Positionen förblir 12,5 %, vilket inte är ett fel.
- Regeln gäller bara nyöppning. De tre innehaven sköts av sina stop och mål som vanligt.

**Lärdom:**
- Alla tre innehav fick backa med marknaden. Inget stop har träffats, och tesernas katalysatorer (Q3-rapporterna 3/11, 5/11 och 11/11) är oförändrade. Det är hållregeln (punkt 0b) som bär: inget av innehaven poängsätts om.
- Veckans viktigaste observation är att **regimspärren slog till på en marginal av 0,05 %**. Det är precis så spärren är konstruerad – den är binär och mäts på stängning – och den får inte tolkas mjukt. Spärren ändrar ingenting för befintliga innehav (punkt 2b, sista stycket).
- `state/decision_eval.json` bär inget urvalstal som klarar `MIN_CLUSTERS`, så inget tal citeras.

Tillämpade lärdomar:
- **L-1** och **L-5:** rapportkalendern står i radarn, med täckning.
- **L-2:** varje bubblare har en rad i watchlisten.
- **L-3:** datadefekterna eskaleras. De är redan öppna i `state/action_items.json`.
- **L-4:** ingen nordisk kandidat har `status: "new"`. Den enda `new`-posten är PAYO, som har `book: "us"`.
- **L-7:** rörelsegenomgången är rangordnad ur prishistoriken.
- **L-8:** ingen indexöversyn hittades.
- **L-9:** CADLR.OL rapporterar i dag och ska avgöras på nytt i första LÄGE B med reaktionsdagens stängning.

### Bred scanning – varifrån bruttolistan kom

**Bruttolistan omfattar 15 kandidater.** De kommer från tre källor:
- **8 ur nyhetsflödet** (punkt g0): BIOA-B.ST, SINCH.ST, BORR.OL, SAGA.OL, SUBC.OL, FRO.OL, HAFNI.OL, NIBE-B.ST. De fyra sista är rapporthändelser i fönstret. De är daterade ur `state/earnings_calendar.json` och v47-radarn (`isEstimate: false`), eftersom MFN-flödets dygnstak tar bort morgonposterna.
- **4 bubblare från v47:** NORBT.OL, EMBRAC-B.ST, ALIV-SDB.ST, AUTO.OL.
- **3 ur egen scanning** av veckans rörelser och rapportkalendern: TRUE-B.ST, BAVA.CO, CADLR.OL.

Nyhetsfönstret bar **10 av 10 handelsdagar** (`window.tradingDaysCovered`).

**Veckans rörelser (punkt g1, enligt L-7).** Rangordningen bygger på `state/price_history.json`. Den omfattar **172 nordiska symboler** (.ST/.OL/.CO/.HE) med daterad stängning både på basdagen **2026-11-13** och mätdagen **2026-11-20**. `state/movers.json` (`asOf` 2026-11-20) flaggar enbart nedgångar. Störst var VPLAY-B.ST (−14,72 %), DOM.ST (−11,82 %), NOKIA.HE (−11,65 %, −8,88 % på dagen) och SINCH.ST (−11,19 %). Alla finns i prishistorikens rangordning.
- **Störst uppåt:** TRUE-B.ST +4,56 %, BAVA.CO +3,46 %, SUBC.OL +2,63 %, COFFEE-B.ST +2,10 %, SCST.ST +1,11 %, NOBI.ST +0,79 %, GMAB.CO +0,61 %, LOOMIS.ST +0,38 %, MOWI.OL +0,18 %. Endast 9 av 172 symboler steg.
- **Störst nedåt:** HEM.ST −23,70 %, VOW.OL −23,08 %, NEL.OL −20,28 %, LUMI.ST −18,73 %, OSSD.ST −14,86 %, VPLAY-B.ST −14,72 %, ZEAL.CO −13,31 %, CHECK.ST −13,03 %, NAPA.OL −12,00 %, DOM.ST −11,82 %.

Följande togs inte upp i bruttolistan:
- **COFFEE-B.ST** (+2,10 %): förvärvet 13/11 ligger utanför femdagarsfönstret, och volymkvoten är 0,84×.
- **SCST.ST, NOBI.ST, LOOMIS.ST och MOWI.OL:** under +1,2 % och utan daterad händelse i fönstret.
- **GMAB.CO:** volymkvot 0,52× och MACD-histogram −56,9.
- **Nedgångarna:** de saknar turnaround-katalysator. Regimspärren gäller dessutom alla.

**Nyhetsflödets nordiska poster i femdagarsfönstret (2026-11-16 – 2026-11-20):**
- **BioArctic:** femårsdata för kontinuerlig Leqembi-behandling, med ökande nytta över tid (MFN 2026-11-16T23:05Z).
- **Sinch:** Jonas Dahlberg utsedd till vd (MFN 2026-11-16T18:50Z).
- **Borr Drilling:** Q3-rapport (MFN 2026-11-18T21:45Z; PR Newswire 2026-11-18T22:09Z).
- **Saga Pure:** avtal om återköp och återköpserbjudande via Euronext Oslo Børs (MFN 2026-11-19T19:23Z).
- **Övrigt, ej kandidater:**
  - Enersense sänker prognosen (vinstvarning, MFN 2026-11-18T19:00Z).
  - LeadDesk avyttrar Case Management.
  - Vend Marketplaces: röstfullmakt inför extra bolagsstämma.
  - Attana: förvärv av BioNavis med riktad emission.
  - Emissionsutfall: Nanologica, BrightBid.
  - Kitron: aktier till anställda. Framery och ContextVision: återköpsrapporter.
  - Flaggningar: Vimian, MTG, Moberg Pharma.
  - Hunter Group/Jacktel: förlängt erbjudande.
- **Saknas i flödet:** Q3-rapporterna från NIBE (17/11), Hafnia (18/11), Subsea 7 (19/11) och Frontline (20/11). De publicerades på morgonen och föll bort på dygnstaket (`news-window-daily-cap-drops-morning-posts`, öppen). Rapporternas siffror har inte verifierats i körningen. De loggas därför enbart på sina tekniska spärrar.

**⚠️ ÅTGÄRDSPUNKT TILL DREN (L-3) – ÅTERKOMMANDE: måndagens schemalagda kurs- och nyhetskörningar har inte startat.**
- **Fil och fält:** `state/prices.json` `generatedAt` 2026-11-21T02:13:44Z och `state/news_feed.json` `generatedAt` 2026-11-20T22:15:20Z.
- **Omfång:** ingen commit från `prices.yml` eller `news.yml` syns på `main` 2026-11-23 före 06:41 UTC. Sjätte måndagen i rad.
- **Ersättningskälla:** fredagens stängningar, som är giltiga före öppning.
- **Status:** redan öppen i `state/action_items.json` som `scheduled-actions-not-firing` (`weeksOpen` 12).

**⚠️ ÅTGÄRDSPUNKT TILL DREN (L-3) – ÅTERKOMMANDE: nyhetsflödena `globenewswire` och `globenewswire-earnings` svarar fortfarande HTTP 403.**
- **Fil och fält:** `state/news_feed.json`, fälten `feeds.globenewswire` och `feeds.globenewswire-earnings` = "HTTP 403 – båda försöken (0.0 s)".
- **Omfång:** 2 av 6 flöden, åttonde veckan i rad.
- **Status:** redan öppen som `news-feed-globenewswire-http-403`.

**⚠️ ÅTGÄRDSPUNKT TILL DREN (L-3) – NY OBSERVATION: CADLR.OL har en inaktuell kurs trots watchlist-rad.**
- **Fil och fält:** `state/prices.json` `quotes["CADLR.OL"].marketTime` = **2026-11-04T15:25Z**, alltså 12 handelsdagar gammal. Tickern står på rad 163 i `config/watchlist.txt`.
- **Konsekvens:** bolaget rapporterar Q3 i dag (`state/earnings_calendar.json`, `isEstimate: false`). Utan en färsk kurs kan reaktionen inte mätas.
- **Möjlig orsak (ej verifierad):** handelsstopp eller symbolbyte hos Yahoo.
- **Status:** ingen matchande punkt i `state/action_items.json`. Miss-retron äger filen.

**Likviditetsgolvet** räknas som 20-dagarssnittet av volymen ur `state/volume_history.json` gånger verifierad kurs. För `.OL`/`.CO`/`.HE` anges talet i lokal valuta, eftersom växelkurser saknas (`fx-rates-missing-eur-dkk-nok`).

---

## Case: INGA NYA VALDA DENNA VECKA

**Regimfiltret är AV, så boken öppnar ingen ny position (punkt 2b).** ^OMX 3 175,06 ≤ MA200 3 176,73, en marginal på −0,05 %. Spärren är hård: den gäller oavsett hur en enskild kandidat poängsätts, och den mildare varianten ("höj ribban") har aldrig mätts. Den lediga platsen och de tre halva positionerna ligger kvar i indexsleeven (62,5 %), alltså kvar i marknaden.

För att det kontrafaktiska underlaget i `state/decision_eval.json` ska vara användbart har varje kandidat ändå prövats mot grindarna. **Även med regimen PÅ hade 0 av 15 passerat alla fem.** Grinden som loggas är den första som fäller kandidaten i ordningen 1 → 5 (se `gate-assignment-ambiguous`). Varje rad i beslutsloggen bär dessutom regimspärren i `reason`.

| Spärr / grind | Fäller (primärt) | Andel |
|---|---|---|
| **Regimfiltret AV (punkt 2b)** | **15 (samtliga)** | 100 % |
| 1 – verifierad kurs med källa + tidsstämpel | 3 | 20 % |
| 2 – teknisk filtrering (RSI/MACD/EMA/volym/likviditet) | 12 | 80 % |
| 3 – namngiven, bekräftad och daterad katalysator | 0 | – |
| 4 – R/R ≥ 2:1, kostnadströskel ≥ 6 % och teknisk stop inom bandet | 0 | – |
| 5 – nåbarhetstak | 0 | – |
| **Valda** | **0** | – |
| **Jämförelse v47** | grind 1: 2, grind 2: 14, grind 4: 1 av 18, valda 1 | – |

### Föll på grind 1 – kurs saknas eller är inaktuell (3 st)
| Ticker | Bolag | Händelse (datum, källa) | `catalystType` | Åtgärd |
|---|---|---|---|---|
| BORR.OL | Borr Drilling | Q3-rapport (MFN 2026-11-18T21:45Z) | earnings | Läggs i `config/watchlist.txt` (punkt 6b) |
| SAGA.OL | Saga Pure | Återköpsavtal och återköpserbjudande (MFN 2026-11-19T19:23Z) | buyback | Läggs i `config/watchlist.txt` (punkt 6b) |
| CADLR.OL | Cadeler | Q3-rapport **i dag 2026-11-23** (`state/earnings_calendar.json`, `isEstimate: false`) | earnings | Senaste kurs är från 2026-11-04 (se åtgärdspunkten ovan). Spärr 2e gäller oberoende av kursen. L-9: avgörs på nytt efter reaktionsdagen. |

### Föll på grind 2 (12 st)
Kurser och indikatorer är räknade ur stängningen 2026-11-20 (`state/prices.json` / `state/price_history.json`, råserien) och `state/volume_history.json`.

| Ticker | Kurs | Veckan | Spärr |
|---|---|---|---|
| BIOA-B.ST | 300,60 SEK | −3,03 % | **RSI 42,5**, MACD-histogram fallande (−0,55 → −0,96), kurs under EMA20/50/200, volymkvot 0,75×. Leqembi-data 16/11 gav ingen reaktion. Q3 25/11 ligger 3 handelsdagar bort. |
| SINCH.ST | 38,51 SEK | −11,19 % | **RSI 30,3**, kurs under EMA20/EMA50, MACD fallande. Vd-bytet 16/11 är ingen bekräftad vändning. |
| SUBC.OL | 319,40 NOK | +2,63 % | **Volymkvot 1,29× < 1,5×**, EMA20 316,83 under EMA50 321,47. MACD-histogrammet vände positivt (−0,37 → +0,28) efter Q3 19/11. RSI 50,6. Bubblare. |
| FRO.OL | 442,60 NOK | −0,65 % | **RSI 43,1**, kurs under EMA20/EMA50, MACD-histogram negativt (−1,43). Q3 20/11. |
| HAFNI.OL | 86,70 NOK | −4,88 % | **RSI 37,8**, kurs under EMA20/EMA50, volymkvot 1,00×. Q3 18/11. |
| NIBE-B.ST | 43,31 SEK | −6,24 % | **RSI 39,8**, kurs under EMA20/EMA50, MACD fallande. Q3 17/11. |
| NORBT.OL | 159,50 NOK | −10,79 % | **RSI 44,8**, kurs under EMA20/50/200, MACD fallande. Bubblarplanen avfördes 18/11. Bubblare v47, **stryks** (Q3-gapet från 12/11 är helt stängt). |
| EMBRAC-B.ST | 94,14 SEK | −10,00 % | **Volymkvot 0,92×**, MACD-histogram fallande (−0,11 → −0,55), kurs under EMA20. Bubblare v47, **stryks**. |
| ALIV-SDB.ST | 1 184,00 SEK | −2,47 % | **Volymkvot 0,79×**, MACD-histogram fallande (−0,62 → −2,30), kurs under EMA20. Bubblare v47, **stryks**. |
| AUTO.OL | 14,79 NOK | −7,16 % | **Volymkvot 1,13×**, RSI 44,1, kurs under EMA20/EMA50. Bubblare v47, **stryks**. |
| TRUE-B.ST | 24,33 SEK | +4,56 % | **Volymkvot 0,80×.** Hel EMA-stack (23,79 > 23,07 > 19,81), RSI 52,7, 6m +91,0 %. Ingen daterad händelse i fönstret. Bubblare. |
| BAVA.CO | 245,40 DKK | +3,46 % | **Volymkvot 0,96×**, MACD-histogram negativt (−0,77). Hel EMA-stack, RSI 55,5, 6m +28,1 %. Ingen daterad händelse. Bubblare. |

### Grind 3/4/5
Ingen kandidat föll primärt på grind 3, 4 eller 5. Bokens beslutsstatistik citeras inte i veckan: `state/decision_eval.json` bär inget tal som klarar `MIN_CLUSTERS`, och ett tal utan `effectiveN` vore ofärdigt. **L-4:** `state/scout_candidates.json` har noll nordiska poster med `status: "new"`, vilket är normalt för den nordiska boken.

### Innehav (punkt 0, hållregeln)
- **BOOZT.ST – BEHÅLL** @ 167,50 SEK (prices.json, marketTime 2026-11-20T16:29:48Z), −1,00 % mot entry 169,20.
  - Dagsspann 166,80–172,30. Stop 163,00 och mål 189,50 är orörda.
  - Tesen (Q3 3/11, höjd prognos) är intakt. Kursen ligger kvar över EMA20 166,72. Volymen 0,61× visar att nedgången inte bärs av säljtryck.
- **MORLD.OL – BEHÅLL** @ 26,05 NOK (prices.json, marketTime 2026-11-20T15:25:43Z), −1,33 % mot entry 26,40.
  - Dagslägsta 25,55 ligger över punkteringsnivån 25,40 och stoppen 25,30, men marginalen till stoppen är bara **2,88 %**.
  - Tesen (Q3 5/11) är intakt.
- **HNSA.ST – BEHÅLL** @ 45,14 SEK (prices.json, marketTime 2026-11-20T16:29:45Z), −3,63 % mot entry 46,84.
  - Dagslägsta 45,10 ligger över stoppen 44,50, men marginalen är bara **1,42 %**. Monitorn larmar intradag om nivån korsas.
  - Ben 2 ≤ 45,00 **avfört**, eftersom det inte triggade inom 5 handelsdagar.
  - Tesen (Q3 11/11, finansierad väg till USA-lansering) är intakt. FDA-beskedet 19/12 ligger utanför horisonten och omprövas före datumet.
- Ingen av dem har en binär händelse inom 2 handelsdagar enligt `state/earnings_calendar.json`.

---

## Bubblare (watchlist inför nästa vecka)
1. **SUBC.OL** – Q3 19/11 vände MACD-histogrammet positivt och aktien steg i en fallande marknad. Den fälls på volymkvoten 1,29× och EMA20 under EMA50. Rad finns i watchlisten.
2. **TRUE-B.ST** – veckans starkaste nordiska namn (+4,56 %) med hel EMA-stack och 6m +91 %. Den fälls på volymkvoten 0,80× och saknar daterad katalysator. Rad finns i watchlisten.
3. **BAVA.CO** – +3,46 % mot marknaden, med hel EMA-stack och 6m +28,1 %. Den fälls på volymkvoten 0,96× och negativt MACD-histogram. Rad finns i watchlisten.

Samtliga tre har **verifierad kurs med källa och `marketTime` i `state/prices.json`**. Ingen av dem föll på saknad kurs. **Oavsett grindarna kan ingen av dem köpas förrän regimfiltret åter är PÅ.**

**Förra veckans bubblare:**
- **NORBT.OL** – STRUKEN. Bubblarplanen ≤ 174,00 triggade 17/11 men avfördes 18/11 (stängning under planens stop). Aktien har nu stängt Q3-gapet, och grind 2 fäller den (RSI 44,8, kurs under EMA200).
- **EMBRAC-B.ST** – STRUKEN (grind 2: volymkvot 0,92×, MACD fallande, −10,00 % på veckan).
- **ALIV-SDB.ST** – STRUKEN (grind 2: volymkvot 0,79×, MACD-histogram −2,30). Utdelningshöjningen 9/11 ligger utanför fönstret.
- **AUTO.OL** – STRUKEN (grind 2: volymkvot 1,13×, kurs under EMA20/EMA50, −7,16 %).

**Villkorade bubblar-planer:** **Inga.** En villkorad plan är en nyöppning, och regimfiltret är AV (punkt 2b). Pending-sektionen i `state/portfolj.md` har noll öppna rader efter att HNSA.ST:s ben 2 avfördes.

## Veckans radar (kommande 5 handelsdagar)
* **Måndag 23/11** – **Cadeler (CADLR.OL)** och **Nykode (NYKD.OL)** Q3 (`isEstimate: false`). Regimen prövas om vid varje körning. Stänger ^OMX över MA200 (≈ 3 177) är den åter PÅ, och då öppnas LÄGE B:s spärrade köpvägar igen.
* **Onsdag 25/11** – **BioArctic (BIOA-B.ST)** och **Elekta (EKTA-B.ST)** Q3 (`isEstimate: false`).
* **Fredag 27/11** – **NOL.OL** Q3 (`isEstimate: false`).
* **Inom 10 handelsdagar:** Clas Ohlson (CLAS-B.ST) 3/12 (`isEstimate: false`).
* **Längre fram:** FDA-beskedet för Hansas imlifidase 19/12 (HNSA.ST är ett innehav och omprövas före datumet) och Riksbanken 16/12.
* **Innehavens nivåer:**
  - HNSA.ST stop 44,50 (1,42 % under fredagens stängning).
  - MORLD.OL stop 25,30 och punkteringsnivå 25,40.
  - BOOZT.ST stop 163,00. Stoppen flyttas upp till entry om aktien stänger ≥ 177,66.

**⚠️ TÄCKNINGSANGIVELSE ENLIGT L-1 OCH L-5.**
- **Källa:** rapportuppräkningen ovan vilar på `state/earnings_calendar.json` (`generatedAt` 2026-11-21T02:11:10Z, `counts.resolved` **236 av 257 symboler**, `failed` 0, `noCoverage` 19).
- **Täckning:** kalendern begär inte symbolerna i moversuniversumet (`earnings-calendar-excludes-movers-universe`, öppen). **Nordiska Large/Mid Cap-bolag utanför kalenderns symboler är därför OKONTROLLERADE.**
- **L-8:** bland fönstrets nordiska MFN-poster hittades ingen indexöversyn med beslut och ikraftträdande inom fönstret. Indexleverantörernas primärkällor täcks inte av någon fil i repot och är därmed **OKONTROLLERADE**.

---

## Bruttolista – samtliga 15 kandidater i `state/decisions.json`
- **KÖP:** inga (regimfiltret AV).
- **BEHÅLL (innehav):** BOOZT.ST, MORLD.OL, HNSA.ST.
- **Grind 1 (AVVAKTA):** BORR.OL, SAGA.OL, CADLR.OL.
- **Grind 2 (AVVAKTA):** BIOA-B.ST, SINCH.ST, SUBC.OL, FRO.OL, HAFNI.OL, NIBE-B.ST, NORBT.OL, EMBRAC-B.ST, ALIV-SDB.ST, AUTO.OL, TRUE-B.ST, BAVA.CO.
- **Indexsleeven:** XACT-OMXS30.ST BEHÅLL, vikten oförändrad 62,5 %.

Samtliga 15 AVVAKTA-rader bär dessutom regimspärren i `reason`.

**Watchlist (punkt 6/6b, L-2):**
- **Tillagda, två rader:** BORR.OL och SAGA.OL (beslut utan kurs).
- **Borttagna: inga.** Listan skyddas enligt `prompts/gemensam_korning.md` av ännu omogna beslut (20 handelsdagars utvärderingsfönster), och riktmärket 25 är underordnat mätbarheten (`watchlist-cap-vs-measurability-conflict`).

---
*Detta är automatiserat beslutsstöd, inte finansiell rådgivning.*
