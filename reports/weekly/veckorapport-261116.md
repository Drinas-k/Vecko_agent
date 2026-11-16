# Veckorapport: Nordisk Rotation
**Vecka:** v 47 | **Datum:** 2026-11-16
**Marknadsklimat:** OMXS30 (`^OMX`) stängde fredag på **3 356,871** (`state/prices.json`, source "Yahoo Finance (chart API)", marketTime 2026-11-13T16:35:00Z), **+2,72 %** mot förra rotationens bas (fredag 2026-11-06: 3 267,884). **Regimfiltret är PÅ:** 3 356,87 ligger **+5,81 %** över MA200 **3 172,56** (200 daterade stängningar ur `state/price_history.json`, serien bär 250 punkter), mot +3,26 % vid v46-rotationen. Riksbankens höjning till 2,00 % trädde i kraft 11/11; nästa besked 16/12. **Nordisk medvind:** biotech/läkemedel efter Q3 (HNSA.ST **+18,70 %**), teknik/elektronik efter Q3 (NORBT.OL +10,71 %, AUTO.OL +12,58 %), spel (EMBRAC-B.ST +9,35 %, EG7.ST +8,30 %), bank (NDA-SE.ST +5,57 %, SWED-A.ST +5,50 %) och bygg (SKA-B.ST +6,07 %). **Nordisk motvind:** medicinteknik/bioprint (BICO.ST **−31,42 %** efter Q3 11/11, DEMANT.CO −7,16 %), förnybart (VWS.CO −7,31 %, ORSTED.CO −4,54 %) och HEM.ST −18,16 %.

**DATAFÄRSKHET.**
- `state/prices.json`: `generatedAt` **2026-11-14T01:28:52Z**, `schemaVersion` "2026-08-02-prevclose", `wideAt` 2026-11-14T01:28:52Z (321 symboler). Fredagens stängningar är senaste handelsdagens stängning och godkänns före öppning. **Måndagens förbörskörningar har inte nått `main`** – senaste kurscommit på `origin/main` är från 2026-11-14 01:28 UTC (kontrollerat ~06:45 UTC).
- `state/news_feed.json`: `generatedAt` 2026-11-14T01:29:15Z, alltså äldre än 24 timmar (helg). Websök har använts som komplement. Fönstret bär **10 av 10 handelsdagar** (2026-11-02 → 2026-11-14, `missingDays` tomt).
- `state/alerts.json`: `checkedAt` 2026-11-13T21:48:29Z och `active` är tom.
- `state/movers.json`: `asOf` **2026-11-13**, alltså förra fredagens stängning. 107 av 110 symboler är OK.
- `state/earnings_calendar.json`: `generatedAt` 2026-11-14T01:26:58Z, 230 av 246 symboler lösta, `failed` 0, 19 kommande.

---

## 0. Facit: Förra veckans val
| Aktie | Entry | Exit | Utfall | Stop/Mål träffad? |
|---|---|---|---|---|
| BOOZT.ST | 169,20 | 172,40 (öppen) | +1,89 % | Nej (dagslägsta 2026-11-13 169,70 över stop 163,00; ben 2 ≤ 165,00 ej triggat, avfört) |
| MORLD.OL | 26,40 (köpt 2026-11-12) | 27,10 (öppen) | +2,65 % | Nej (dagslägsta 2026-11-13 26,40 över stop 25,30) |
| XACT-OMXS30.ST | 494,60 | 501,30 (öppen) | +1,36 % mot entry, +2,86 % på veckan | Nej (sleeven har varken stop eller mål) |

**Veckans portföljutfall (viktat):** **≈ +2,8 % brutto.** Sleeven bar 75–87,5 % av boken och gick 487,35 → **501,30** (+2,86 %), BOOZT.ST 12,5 % gick 169,20 → 172,40 (+1,89 %) och MORLD.OL 12,5 % sedan torsdagen 26,40 → 27,10 (+2,65 %). `^OMX` gick +2,72 % över samma period. Talet är en approximation ur dagliga stängningar och vikter; dashboardens nettosiffra drar dessutom rundturskostnaden.
**Ackumulerad avkastning sedan strategistart:** **−3,70 %** (fyra stängda affärer, alla 25 %: ASSA-B.ST −3,26 %, SALM.OL −5,48 %, SAAB-B.ST −2,70 %, KOG.OL −3,55 %). Ingen affär stängd denna vecka. Sleevens och de öppna innehavens orealiserade rörelse ingår inte i fältet.
**Portföljallokering denna vecka:** **12,5 % BOOZT.ST + 12,5 % MORLD.OL + 12,5 % HNSA.ST (ben 1) + 62,5 % indexsleeve (XACT-OMXS30.ST) + 0 % kassa.**
- Ben 2 för HNSA.ST (≤ 45,00) och MORLD.OL (≤ 26,00) ligger i Pending; fylls båda blir sleeven 37,5 %.
- BOOZT.ST:s ben 2 avfördes (punkt 4a) – positionen förblir 12,5 %, vilket inte är ett fel.
- En plats står ledig; den villkorade bubblar-planen NORBT.OL ≤ 174,00 kan fylla den.
- Vikten är platt 25 % per fylld position.

**Lärdom:** Båda innehaven från förra veckan är positiva men ligger nära sina dagslägsta i förhållande till stoppen – ingen har ännu bekräftat sig. Den rena limit-entryn för ben 2 triggade inte för BOOZT.ST trots en rekyl till 166,20; ben 1-direktköpet (punkt 4a) gav ändå exponering, vilket är precis vad regeln finns för. Den återkommande lärdomen från v46 (**L-7**, sektorrisk syns i rörelsegenomgången) har styrt veckans val: HNSA.ST ligger i en sektor med egen medvind och skiljer sig i riskprofil från BOOZT.ST (konsument) och MORLD.OL (oljeservice). Underlaget är fortsatt brus; `state/decision_eval.json` bär inget urvalstal som klarar `MIN_CLUSTERS`, så inget tal citeras.

Tillämpade lärdomar:
- **L-1** och **L-5:** rapportkalendern står i radarn, med täckning.
- **L-2:** varje bubblare har en rad i watchlisten (ALIV-SDB.ST tillagd).
- **L-3:** datadefekterna eskaleras, och samtliga är redan öppna i `state/action_items.json`.
- **L-4:** ingen nordisk kandidat har `status: "new"` (den enda `new`-posten är APP, `book: "us"`).
- **L-6:** ingen kandidat är struken på en universumregel.
- **L-7:** rörelsegenomgången är rangordnad ur prishistoriken.
- **L-8:** inga indexöversyner hittades.

### Bred scanning – varifrån bruttolistan kom

**Bruttolistan omfattar 18 kandidater:**
- **6 ur nyhetsflödet** (punkt g0): SUBC.OL, ALIV-SDB.ST, HSHP.OL, ALVO-SDB.ST, TAGM-B.ST, COFFEE-B.ST.
- **4 bubblare från v46**: SOBI.ST, LUG.ST, ORSTED.CO, SAGA-B.ST (MORLD.OL, den femte, köptes 2026-11-12).
- **8 ur egen scanning** av veckans rörelser och rapportreaktioner: HNSA.ST, NORBT.OL, AUTO.OL, GRK.HE, EMBRAC-B.ST, AUSS.OL, SKA-B.ST, DOM.ST.

Nyhetsfönstret bar **10 av 10 handelsdagar** (`window.tradingDaysCovered`).

**Veckans rörelser (punkt g1, enligt L-7).** Rangordningen bygger på `state/price_history.json` och omfattar **169 nordiska symboler** (.ST/.OL/.CO/.HE) med daterad stängning både på basdagen **2026-11-06** och mätdagen **2026-11-13**. `state/movers.json` (`asOf` 2026-11-13) flaggar HNSA.ST (+18,7 %), EMBRAC-B.ST (+9,35 %) och CTM.ST (+10,26 % på dagen); alla tre finns i prishistorikens rangordning.
- **Störst uppåt:** HNSA.ST +18,70 %, AUTO.OL +12,58 %, NORBT.OL +10,71 %, GRK.HE +10,29 %, EMBRAC-B.ST +9,35 %, AUSS.OL +8,51 %, EG7.ST +8,30 %, NAPA.OL +6,75 %, DOM.ST +6,74 %, TRMD-A.CO +6,45 %, SF.ST +6,45 %, CTM.ST +6,38 %, SKA-B.ST +6,07 %.
- **Störst nedåt:** BICO.ST −31,42 %, HEM.ST −18,16 %, XBRANE.ST −9,84 %, ALVO-SDB.ST −8,39 %, OSSD.ST −7,53 %, VWS.CO −7,31 %, DEMANT.CO −7,16 %, HEALTH.HE −5,00 %, SOBI.ST −4,82 %, VOLCAR-B.ST −4,65 %, ORSTED.CO −4,54 %.

Följande togs inte upp i bruttolistan: EG7.ST (volymkvot 0,68×, 6m −23,4 %), NAPA.OL (RSI 46,0, kurs under EMA20/EMA50), SF.ST (volymkvot 0,41×), CTM.ST (kurs 3,17 SEK, ingen daterad händelse), TRMD-A.CO (tankrekyl utan egen katalysator). Var och en faller på ett grind 2-kriterium som går att se direkt ur siffrorna. Nedgångarna saknar turnaround-katalysator.

**Nyhetsflödets nordiska poster i femdagarsfönstret (2026-11-09 – 2026-11-13):**
- **Autoliv:** höjd kvartalsutdelning (MFN 2026-11-09T22:00Z).
- **Himalaya Shipping:** commercial update och oktoberutdelning (MFN 2026-11-10T21:15Z).
- **TagMaster:** avtal om förvärv av Kapsch TrafficComs nordamerikanska 915MHz-verksamhet (MFN 2026-11-10T20:24Z).
- **Alvotech:** niomånadersrapport (MFN 2026-11-11T21:15Z).
- **Subsea 7:** kontrakt offshore USA (MFN 2026-11-13T18:36Z).
- **Coffee Stain:** avtal om förvärv av IP:t Chronicles: Medieval (MFN 2026-11-13T23:08Z).
- **Övrigt, ej kandidater:**
  - Emissioner: Arctic Minerals (140 MSEK), Klaria (111,1 MSEK), Novakand Pharma (50,9 MSEK), Qbim, INQ Group (konvertering).
  - Övrigt: Hansa Biopharma deltar i Jefferies-konferensen, poLights kapitalmarknadsdag, Konkurrensverket avslutar utredningen av Apotea, SmartCraft syntetiska återköp, Framery återköp, Proximar Seafood rekapitalisering, Okeanis Eco Tankers Q3, Lyko valberedning, Nasdaq överväger avnotering av Subgen AI.
  - Síldarvinnslan (positiv vinstvarning) är isländsk och ligger utanför universumet.
- **Saknas i flödet:** Hansa Biopharmas och Norbits Q3-rapporter (11/11 respektive 12/11, publicerade på morgonen). Samma dygnstaksdefekt som tidigare; de har verifierats via websök.

**⚠️ ÅTGÄRDSPUNKT TILL DREN (L-3) – ÅTERKOMMANDE: måndagens schemalagda kurs- och nyhetskörningar har inte startat.**
- **Fil och fält:** `state/prices.json` `generatedAt` 2026-11-14T01:28:52Z och `state/news_feed.json` `generatedAt` 2026-11-14T01:29:15Z. Ingen commit från `prices.yml` eller `news.yml` syns på `main` före cirka 06:45 UTC.
- **Omfång:** 2 av 2 förbörskörningar i `prices.yml` och 1 av 1 i `news.yml`. Femte måndagen i rad.
- **Ersättningskälla:** fredagens stängningar, som är giltiga före öppning, samt websök.
- **Status:** redan öppen i `state/action_items.json` som `scheduled-actions-not-firing` (`weeksOpen` 11).

**⚠️ ÅTGÄRDSPUNKT TILL DREN (L-3) – ÅTERKOMMANDE: nyhetsflödena `globenewswire` och `globenewswire-earnings` svarar fortfarande HTTP 403.**
- **Fil och fält:** `state/news_feed.json` `feeds.globenewswire` = "HTTP 403 – båda försöken (0.0 s)". `feeds.globenewswire-earnings` = "HTTP 403 – båda försöken (0.1 s)".
- **Omfång:** 2 av 6 flöden, sjunde veckan i rad.
- **Status:** redan öppen som `news-feed-globenewswire-http-403`.

**⚠️ ÅTGÄRDSPUNKT TILL DREN (L-3) – ÅTERKOMMANDE: MFN-flödets dygnstak tar bort handelssessionen.**
- **Fil och fält:** alla `src: "mfn"`-poster 2026-11-09 – 2026-11-13 ligger mellan **17:08 och 23:59 UTC**.
- **Konsekvens:** veckans två starkaste nordiska rapportkatalysatorer (Hansa Biopharma och Norbit) finns inte i flödet.
- **Status:** öppen som `news-window-daily-cap-drops-morning-posts`.

**Likviditetsgolvet** räknas som 20-dagarssnittet av volymen ur `state/volume_history.json` gånger verifierad kurs. För `.OL`/`.CO`/`.HE` anges talet i lokal valuta, eftersom växelkurser saknas (`fx-rates-missing-eur-dkk-nok`).

---

## Case 1: Hansa Biopharma (HNSA.ST / Nasdaq Stockholm)

### 1. Katalysatorn
**Q3-rapport 2026-11-11.**
- **Intäkter:** 143,0 MSEK (30,8), varav **121,6 MSEK licensintäkt** från SERB Pharmaceuticals-avtalet (förskottsbetalning 110 MEUR).
- **Rörelseresultat:** −138,6 MSEK (−147,6), alltså minskad rörelseförlust.
- **Kassa:** 1 337,2 MSEK (252,1); NovaQuest-lånet om cirka 808,8 MSEK kvarstår.
- **Nästa händelse:** FDA:s måldatum (PDUFA) för imlifidase är **2026-12-19**; vid godkännande planeras lansering i USA Q1 2027.
- **Källor:** Placera-telegram "Hansa Biopharma ökade intäkterna och minskade rörelseförlusten" (2026-11-11), Finwire/Börsvärlden "Hansa Biopharma (Q3 Update): Europe Below Expectations, but the US Will Drive Value – Redeye" (2026-11-11), RTTNews "Hansa Biopharma Q3 loss widens" (2026-11-11).
- **Reaktion:** aktien gick 38,94 → **44,76** (+14,95 %) på rapportdagen och fortsatte till 46,28 och 46,84 (`state/price_history.json`). Volymen låg på 2,12, 2,65 och 1,28 miljoner aktier mot ett 20-dagarssnitt kring 0,7 miljoner (`state/volume_history.json`).
- **`catalystType`:** earnings.

### 2. Investerings-tes (The Bull Case)
* Rapporten lyfte finansieringsrisken: kassan femdubblades genom SERB-avtalet, och marknaden prisar om bolaget från "kassabränning" till "finansierad väg till USA-lansering". Reaktionen höll i två sessioner efter rapportdagen.
* **Lång trend bakom rörelsen (punkt 0a):** +39,5 % på sex månader och hel EMA-stack (EMA20 40,28 > EMA50 38,56 > EMA200 35,27). Tvåveckorsrörelsen (+19,1 %) bärs alltså av trend, inte enbart av en spik.
* **Drift in mot PDUFA:** inflödet inför FDA-datumet 19/12 ger efterfrågan under hela horisonten (20 handelsdagar → omkring 11/12), som slutar före det binära beskedet.

### 3. Motargument & Risker (The Bear Case)
* **Intäktslyftet är engångs:** licensintäkten bär nästan hela kvartalet, produktförsäljningen gick till nära noll till följd av redovisningsbytet, och Redeye beskriver Europa som under förväntan. Resultatet efter finansnetto försämrades.
* **Binärt FDA-besked 19/12:** ligger utanför horisonten, men positionen måste omprövas uttryckligen före datumet (punkt 4 BEHÅLL-regeln). Ett avslag skulle ge ett gap långt under stoppet.
* **RSI 72,1** ligger över det föredragna intervallet 50–70 (under 75-spärren). En rekyl mot stödet 44,76 är sannolik; ben 2 ligger där.
* **Olönsamt bioteknikbolag:** runwayen anges av bolaget räcka "långt in i 2028" men av Redeye (proforma 888 MSEK) bara in i 2027 – källorna är oeniga.

### 4. Fundamental snapshot
* **Börsvärde:** ej verifierat i körningen | **P/E / EV/EBITDA:** ej meningsfullt (förlust) | **Tillväxt:** intäkter 143,0 MSEK (30,8), engångsdrivet | **Snittomsättning/dag:** **33,0 MSEK** (20-dagarssnitt × 46,84; `state/volume_history.json`), alltså över likviditetsgolvet och i lägsta kostnadsnivån (≥ 20 MSEK/dag, 0,25 %)

### 5. Teknisk setup
* **RSI(14):** 72,1 | **MACD:** histogrammet positivt och stigande, 0,756 → 0,887 | **Kurs vs EMA20/50/200:** över alla tre (40,28 / 38,56 / 35,27; hel stack) | **Volym vs 20d-snitt:** **1,82×** (1 282 831, 2026-11-13) | **Stöd:** 44,76 (stängning 2026-11-11) och 41,30 (stängning 2026-11-09) | **Motstånd:** inget i serien – 46,84 (2026-11-13) är 250-dagarshögsta.

### 6. Handelsplan
| Entry | Stop-loss | Målkurs | Risk/Reward |
|---|---|---|---|
| 46,84 (ben 1, verifierad stängning 2026-11-13T16:29:56Z) / ≤ 45,00 (ben 2, limit) | 44,50 (−5,00 %) | 52,50 (+12,08 %) | 1:2,42 (ben 1), 1:15,0 (ben 2) |

* **Stopp:** 44,50 ligger strax under stödet 44,76, i överkant av bandet 3–5 %, och sätts tekniskt.
* **Mål:** 52,50 ligger i earnings-bandet 12–15 %. Det är ≥ 2× stoppavståndet (2,34 kr → minst 51,52).
* **Kostnadströskel:** entry → mål är **+12,08 %**, vilket är ≥ 6 % och cirka 48× rundturskostnaden 0,25 %.
* **Nåbarhet (punkt 6):** genomsnittlig absolut dagsrörelse över 60 dagar är **2,72 %**. Taket blir 2 × 2,72 % × √20 = **24,3 %** ≥ 12,08 %, så målet ryms vid 20 handelsdagars horisont.
* **Horisont:** 20 handelsdagar (`earnings`, 3–6 veckor) utan tidsstopp; slutar omkring 2026-12-11, före PDUFA 19/12.
* **Binära händelser:** ingen inom 2 handelsdagar. HNSA.ST saknas bland `upcoming` i `state/earnings_calendar.json` eftersom rapporten nyss passerats.
* **Totalpoäng 6,5:** katalysator 6 (35 %), teknik 8 (30 %), makro 5 (15 %), R/R 6 (20 %).

**Planerad vikt:** **25 %, delad entry enligt punkt 4a.**
- **Ben 1 (12,5 %)** köps direkt vid rotationen till verifierad marknadskurs.
- **Ben 2 (12,5 %)** läggs som limit ≤ 45,00 i Pending. Det avförs om det inte triggat inom 5 handelsdagar (t.o.m. 2026-11-20).
- Inget undantag för hel limit gäller. Gapet (+14,95 %) var 11/11, inte i dag, och fredagen var +1,21 %. Ingen binär händelse infaller inom 2 handelsdagar.

---

## Övriga kandidater – varför de föll

**1 av 18 bruttokandidater passerade alla fem grindar.** Grinden som loggas är den första som fäller kandidaten i ordningen 1 → 5 (se `gate-assignment-ambiguous`).

| Grind | Fäller (primärt) | Andel |
|---|---|---|
| 1 – verifierad kurs med källa + tidsstämpel | 2 | 11 % |
| 2 – teknisk filtrering (RSI/MACD/EMA/volym/likviditet), inkl. spärr 2e | 14 | 78 % |
| 3 – namngiven, bekräftad och daterad katalysator | 0 | – |
| 4 – R/R ≥ 2:1, kostnadströskel ≥ 6 % och teknisk stop inom bandet | 1 | 6 % |
| 5 – nåbarhetstak | 0 | – |
| **Valda** | **1 (HNSA.ST)** | 6 % |
| **Jämförelse v46** | grind 1: 4, grind 2: 14, grind 3: 3 av 22, valda 1 | – |

### Föll på grind 1 – kurs saknas (2 st)
TAGM-B.ST och COFFEE-B.ST har ingen rad i `state/prices.json`. Båda läggs i `config/watchlist.txt` i denna körning (punkt 6b).

| Ticker | Bolag | Händelse (datum, källa) | `catalystType` |
|---|---|---|---|
| TAGM-B.ST | TagMaster | Förvärv av Kapsch TrafficComs nordamerikanska 915MHz-verksamhet (MFN 2026-11-10T20:24Z) | other |
| COFFEE-B.ST | Coffee Stain | Förvärv av IP:t Chronicles: Medieval (MFN 2026-11-13T23:08Z) | other |

### Föll på grind 2 (14 st)
| Ticker | Kurs (marketTime 2026-11-13) | Veckan | Spärr |
|---|---|---|---|
| SUBC.OL | 311,20 NOK | +2,10 % | **RSI 43,8**, volymkvot 0,58×, kurs under EMA20/EMA50, MACD fallande. Kontraktet 13/11 gav ingen reaktion. Q3 19/11. |
| ALIV-SDB.ST | 1 214,00 SEK | +0,08 % | **Volymkvot 1,18×.** Höjd utdelning 9/11, hel EMA-stack, MACD positivt. Bubblare. |
| HSHP.OL | 151,00 NOK | +5,45 % | **RSI 45,7**, volymkvot 0,56×, kurs under EMA20/EMA50. |
| ALVO-SDB.ST | 43,70 SEK | −8,39 % | **Likviditet 1,4 MSEK/dag < 3 MSEK**, RSI 39,7, kurs under alla EMA. |
| SOBI.ST | 474,20 SEK | −4,82 % | **MACD-histogrammet vände negativt** (0,521 → −0,797), kurs under EMA20. Ingen katalysator i fönstret. Bubblare v46, stryks. |
| LUG.ST | 656,80 SEK | −2,06 % | **Volymkvot 0,60×**, EMA20 647,07 under EMA200 649,68, MACD-histogrammet fallande. Bubblare v46, stryks. |
| ORSTED.CO | 141,95 DKK | −4,54 % | **Volymkvot 0,91×**, EMA20/EMA50 under EMA200, 6m −13,5 %. Bubblare v46, stryks. |
| SAGA-B.ST | 186,90 SEK | +0,86 % | **Volymkvot 0,38×**, EMA50 under EMA200, fortfarande ingen daterad händelse. Bubblare v46, stryks. |
| AUTO.OL | 15,93 NOK | +12,58 % | **Volymkvot 0,72×.** Återköp pågår, hel EMA-stack, 6m +31,9 %. Bubblare. |
| GRK.HE | 20,80 EUR | +10,29 % | **RSI 42,7**, volymkvot 0,65×, kurs under EMA20/EMA50. |
| EMBRAC-B.ST | 104,60 SEK | +9,35 % | **RSI 75,6 > 75** och volymkvot 1,46×. Q3 11/11, hel EMA-stack, 6m +53,8 %. Bubblare. |
| AUSS.OL | 89,30 NOK | +8,51 % | **Volymkvot 1,20×**, EMA20/EMA50 under EMA200, 6m −4,1 %. |
| SKA-B.ST | 306,00 SEK | +6,07 % | **RSI 77,7 > 75**, volymkvot 0,83×. |
| DOM.ST | 24,70 SEK | +6,74 % | **Volymkvot 0,90×**, kurs under EMA200 27,24, 6m −23,6 % (punkt 0a: tvåveckorsspik utan trend). |

### Föll på grind 4 (1 st)
| Ticker | Kurs (marketTime 2026-11-13T15:25:35Z) | Spärr |
|---|---|---|
| NORBT.OL | 178,80 NOK | Q3 12/11 slog: intäkter 676,7 MNOK (+34 %), EBIT 115,5 MNOK (+53 %), helårsprognos 3,0–3,1 mdr NOK och EBIT-marginal 21–22 % (Quartr-sammanfattning 2026-11-12; Norbits egen release har inte gått att öppna). Tekniken håller: RSI 61,8, volymkvot **2,38×**, kurs över EMA20/50/200, MACD stigande, likviditet 29,8 MNOK/dag. **Men närmaste stöd 168,80 ligger 5,6 % under entry**, så en stop strax under stödet hamnar utanför bandet 3–5 %, och en stop inom bandet saknar tekniskt ankare. Fredagen gav tillbaka −4,3 % av rapportdagens +14,1 %, och sexmånaderstrenden är −5,8 % (punkt 0a-varning). Läggs som villkorad bubblar-plan ≤ 174,00 där stoppen 168,00 ryms i bandet. |

### Grind 3/5
Ingen kandidat föll primärt på grind 3 eller 5. HNSA.ST klarar nåbarhetstaket (24,3 %) med god marginal. Bokens beslutsstatistik citeras inte i veckan: `state/decision_eval.json` bär inget tal som klarar `MIN_CLUSTERS`, och ett tal utan `effectiveN` vore ofärdigt. **L-4:** `state/scout_candidates.json` bär noll nordiska poster med `status: "new"`, vilket är normalt för den nordiska boken.

### Innehav (punkt 0, hållregeln)
- **BOOZT.ST – BEHÅLL** @ 172,40 SEK (prices.json, marketTime 2026-11-13T16:29:58Z), +1,89 % mot entry 169,20. Dagsspann 169,70–173,30; stop 163,00 och mål 189,50 orörda. Tesen (Q3 3/11, höjd prognos) är intakt. Ben 2 ≤ 165,00 **avfört** – ej triggat inom 5 handelsdagar (lägsta dagslägsta 166,20 den 11/11).
- **MORLD.OL – BEHÅLL** @ 27,10 NOK (prices.json, marketTime 2026-11-13T15:25:28Z), +2,65 % mot entry 26,40, ny 250-dagarshögsta i stängning. Dagsspann 26,40–27,10; stop 25,30 och mål 29,60 orörda. Ben 2 ≤ 26,00 ligger kvar t.o.m. 2026-11-19.
- Ingen av dem har en binär händelse inom 2 handelsdagar enligt `state/earnings_calendar.json`.

---

## Bubblare (watchlist inför nästa vecka)
1. **NORBT.OL** – Q3 12/11 slog på intäkter och EBIT, volymkvot 2,38×; fälld enbart på att stoppen inte kan ankras i bandet vid dagens kurs. Villkorad plan ≤ 174,00. Rad finns i watchlisten.
2. **EMBRAC-B.ST** – Q3 11/11, hel EMA-stack och 6m +53,8 %; fälld på RSI 75,6 och volymkvot 1,46×. Rad finns i watchlisten.
3. **ALIV-SDB.ST** – höjd utdelning 9/11, hel EMA-stack, likviditet 62,6 MSEK/dag; fälld på volymkvoten 1,18×. Rad tillagd i watchlisten.
4. **AUTO.OL** – +12,58 % på veckan med pågående återköp och hel EMA-stack; fälld på volymkvoten 0,72×. Rad finns i watchlisten.

Samtliga fyra har **verifierad kurs med källa och `marketTime` i `state/prices.json`**. Ingen av dem föll på saknad kurs.

**Förra veckans bubblare:**
- **MORLD.OL** – VALD (bubblar-planen ≤ 26,40 triggade 2026-11-12, ben 1 köpt).
- **SOBI.ST** – STRUKEN (grind 2: MACD-histogrammet negativt, kurs under EMA20; fortfarande ingen katalysator).
- **LUG.ST** – STRUKEN (grind 2: volymkvot 0,60×, EMA20 under EMA200).
- **ORSTED.CO** – STRUKEN (grind 2: volymkvot 0,91×, EMA20/50 under EMA200, −4,54 % på veckan).
- **SAGA-B.ST** – STRUKEN (grind 2: volymkvot 0,38×; ingen daterad händelse två veckor i rad).

**Villkorade bubblar-planer:** **1 av 2.** **NORBT.OL** – entry-villkor verifierad kurs ≤ 174,00 NOK, stop 168,00 (−3,45 %, strax under stödet 168,80), mål 195,00 (+12,07 %), R/R 3,50:1, nåbarhetstak 14,6 %, planerad vikt 12,5 % (ben 1), avförs t.o.m. 2026-11-20. Speglar Pending i `state/portfolj.md`. Pending bär dessutom två ben 2-rader (HNSA.ST ≤ 45,00, MORLD.OL ≤ 26,00), som inte är bubblar-planer.

## Veckans radar (kommande 5 handelsdagar)
* **Måndag 16/11** – **HNSA.ST ben 1** köps i dag.
* **Tisdag 17/11** – **NIBE (NIBE-B.ST)** Q3 (`isEstimate: false`).
* **Onsdag 18/11** – **Hafnia (HAFNI.OL)** Q3 (`isEstimate: false`).
* **Torsdag 19/11** – **Implantica (IMP-A-SDB.ST)** och **Subsea 7 (SUBC.OL)** Q3 (`isEstimate: false`). **Sista dagen för MORLD.OL:s ben 2-limit.**
* **Fredag 20/11** – **Frontline (FRO.OL)** Q3 (`isEstimate: false`). **Sista dagen för HNSA.ST:s ben 2-limit och NORBT.OL-bubblarplanen.**
* **Inom 10 handelsdagar:** Cadeler (CADLR.OL) 23/11, BioArctic (BIOA-B.ST), Elekta (EKTA-B.ST) och Nykode (NYKD.OL) 25/11, NOL.OL 27/11 (samtliga `isEstimate: false`). Längre fram: FDA-beskedet för Hansas imlifidase 19/12 och Riksbanken 16/12.

**⚠️ TÄCKNINGSANGIVELSE ENLIGT L-1 OCH L-5.**
- **Källa:** rapportuppräkningen ovan vilar på `state/earnings_calendar.json` (`generatedAt` 2026-11-14T01:26:58Z, `counts.resolved` **230 av 246 symboler**, `failed` 0, `noCoverage` 14).
- **Täckning:** kalendern begär inte symbolerna i moversuniversumet (`earnings-calendar-excludes-movers-universe`, öppen). **Nordiska Large/Mid Cap-bolag utanför kalenderns symboler är därför OKONTROLLERADE.**
- **L-8:** ingen indexöversyn med beslut och ikraftträdande inom fönstret hittades bland fönstrets nordiska MFN-poster. Indexleverantörernas primärkällor täcks inte av någon fil i repot och är därmed **OKONTROLLERADE**.

---

## Bruttolista – samtliga 18 kandidater i `state/decisions.json`
- **KÖP:** HNSA.ST (ben 1, 12,5 %).
- **BEHÅLL (innehav):** BOOZT.ST, MORLD.OL.
- **Grind 1 (AVVAKTA):** TAGM-B.ST, COFFEE-B.ST.
- **Grind 2 (AVVAKTA):** SUBC.OL, ALIV-SDB.ST, HSHP.OL, ALVO-SDB.ST, SOBI.ST, LUG.ST, ORSTED.CO, SAGA-B.ST, AUTO.OL, GRK.HE, EMBRAC-B.ST, AUSS.OL, SKA-B.ST, DOM.ST.
- **Grind 4 (AVVAKTA):** NORBT.OL (villkorad bubblar-plan).
- **Indexsleeven:** XACT-OMXS30.ST BEHÅLL, vikten minskad 75,0 % → 62,5 %.

**Watchlist (punkt 6/6b, L-2):**
- **Tillagda, tre rader:** TAGM-B.ST och COFFEE-B.ST (beslut utan kurs), ALIV-SDB.ST (bubblare).
- **Borttagna: inga.** Listan skyddas enligt `prompts/gemensam_korning.md` av ännu omogna beslut (20 handelsdagars utvärderingsfönster), och riktmärket 25 är underordnat mätbarheten (`watchlist-cap-vs-measurability-conflict`).

---
*Detta är automatiserat beslutsstöd, inte finansiell rådgivning.*
