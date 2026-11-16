# Veckorapport: US-rotation
**Vecka:** v 47 | **Datum:** 2026-11-16
**Marknadsklimat:** Regimen är PÅ igen med marginal, men veckan framför är binär. `^GSPC` stängde fredagen på **7 561,67 (−0,40 % fredag, vecka +2,51 %)** och `^IXIC` på **25 136,27 (−0,91 % fredag, vecka +2,27 %)** (prices.json/Yahoo chart API, marketTime 2026-11-13T21:43:19Z resp. 22:15:59Z). `^GSPC` ligger **+3,02 % över MA200** (7 340,29) men under EMA20 7 600,72 och EMA50 7 635,32, med RSI 46,8 och ett MACD-histogram som är negativt men stiger (−9,25 → −3,20 → −0,83). `^IXIC` står exakt på MA200 (25 137,37). KPI oktober blev 0,1 pp över förväntan (total +0,4 % m/m, kärna +0,3 %) och PPI +0,3 % m/m mot väntade +0,4 % (via scout-261114/-261116). 10-årsräntan ligger nära 5 % enligt sökträffar. Den är inte verifierad, eftersom `^TNX` saknas i `state/prices.json`. Veckans binära händelser är **NVDA-rapporten tisdag 17/11 AMC**, FOMC-protokollet 18/11 och Anthropics (`ANT`) väntade notering 19/11 (⚠️ RYKTE – EJ BEKRÄFTAT (CNBC, källor med insyn, 2026-11-10)). DXY och VIX finns inte i `state/prices.json` och anges därför inte med siffra. Förbörsnivåer för i dag gick inte att verifiera: websök 2026-11-16 gav inga daterade träffar för dagens förbörshandel.

---

## 0. Facit: Förra veckans val
| Aktie | Entry | Exit | Utfall | Stop/Mål träffad? |
|---|---|---|---|---|
| CBOE (ben 1, 12,5 %) | $335,53 | – (behålls) | +11,89 % (375,42, 2026-11-13T21:00:00Z); veckan +6,27 % | Nej – veckans lägsta 352,00 (10/11) > stop; högsta 378,35 (12/11) < mål 382,50 |
| U (villkorad plan, 25 %) | – | – | – (aldrig köpt) | Villkoret ≤ 49,00 korsades 10/11, men planen avfördes vid omprövningen 11/11 (grind 2: volym 0,97×) |
| SPY (sleeve, 87,5 %) | $773,26 | – (behålls) | +2,59 % i veckan (735,29 → 754,37); −2,44 % mot entry | Ingen stop/mål – sleeven |

**Veckans portföljutfall (viktat):** **+3,05 %**, räknat med faktiska vikter: SPY 87,5 % × +2,59 % och CBOE 12,5 % × +6,27 % (stängningar 2026-11-06 → 2026-11-13 ur `state/price_history.json`). Boken slog `^GSPC` (+2,51 %) med 0,54 pp. Hela skillnaden kommer från CBOE.
**Ackumulerad avkastning sedan strategistart:** **−6,49 %**, oförändrad sedan NUE-försäljningen 2026-11-06. Sex stängda affärer i skarp drift, samtliga på stop eller punkterad tes. Den öppna CBOE-positionen (+11,89 %) ingår inte förrän den stängs. Siffran är exklusive USD/SEK-effekten.
**Portföljallokering denna vecka:** **12,5 % CBOE / 87,5 % SPY-sleeve.** Vikten är platt 25 % per fullt fylld position. CBOE förblir 12,5 %, eftersom ben 2 avfördes 2026-11-09 (punkt 4a). Tre aktieplatser är tomma och ingen pending-plan är öppen.
**Lärdom:** Veckans bästa beslut var att avföra `U`-planen trots att villkoret korsades. Volymkravet höll, och aktien stängde fredagen på 52,81 utan att ha gett något bevis. Mönstret från förra veckan består: **funneln stoppar på grind 2 och 3 och inte på datatillgång.** 6 av 21 kandidater föll på grind 1, och samtliga var nyhetsflödets nya symboler. Av de 15 med kurs föll 6 på MA200, och de 9 över MA200 föll alla på volym under 1,5× eller saknade färsk katalysator. Veckans uppgång (+2,5 %) bars av halvledarnamn under MA200 (`AMD`, `AVGO`, `CIEN`), vilket är exakt vad regimregeln och MA200-spärren ska sortera bort. Tillämpade lärdomar: **L-2** (sex nya watchlist-symboler), **L-3** (åtgärdspunkter nedan), **L-4** (`ABNB` omprövad med kurs), **L-5** (radarns källa och täckning), **L-6** (ingen kandidatklass struken med hänvisning till fokusfilen), **L-7** (rörelsegenomgång ur price_history), **L-8** (`CHYM`, `INGM` i bruttolistan) och **L-9** (`HD`, `WMT` och `NVDA` ska prövas om efter rapportreaktionen).

---

## Case: INGA NYA VALDA DENNA VECKA

Ingen av de 21 aktiekandidaterna passerade alla fem grindar. Tre aktieplatser står tomma i SPY-sleeven (punkt 0, 0b och 0c). Det befintliga innehavet `CBOE` poängsätts inte om (punkt 0b). Tesen är intakt, och varken stop eller mål har träffats.

**CBOE – BEHÅLL, stop flyttad UPP.** Kursen är 375,42 (+11,89 % mot entry 335,53; dagsintervall 369,65–378,17; marketTime 2026-11-13T21:00:00Z, prices.json/Yahoo chart API), vilket är nytt 250-dagarshögsta. RSI 74,8, full EMA-stack (EMA20 342,59 > EMA50 318,69 > EMA200 295,05), MACD-histogram positivt och åter stigande (2,45 → 2,31 → 2,38), volym 0,77×. Ingen rapport finns inom fönstret i `state/earnings_calendar.json`. **Stop flyttas 345,00 → 351,50** (punkt 6: upp, aldrig ned). Nivån ligger under swinglägsta 352,00 (10/11), −6,37 % från kursen, och låser +4,76 % mot entry. Målet 382,50 är oförändrat (+1,89 % från kursen). Fredagens högsta 378,17 nådde det inte. Målet höjs inte, eftersom ingen ny katalysator finns (punkt 6). Förbörskurs för i dag gick inte att verifiera. Monitorn larmar om målet korsas intradag.

**Bred scanning – varifrån bruttolistan kom (21 aktiekandidater, samtliga loggade i `state/decisions.json` med `mode: "A"`, plus BEHÅLL-rader för CBOE och sleeven):**
* **Ur nyhetsflödet (g0): 6.**
  * `CHYM` – "Chime Financial Set to Join S&P MidCap 400" (PR Newswire 2026-11-13) och `INGM` – "Ingram Micro Holding Set to Join S&P SmallCap 600" (PR Newswire 2026-11-11). Båda är `index`-katalysatorer enligt L-8, men ikraftträdandedatumen är inte verifierade.
  * `BKNG` (8-K 2026-11-13), `MCO` (8-K 2026-11-12), `IONQ` (8-K 2026-11-13) och `DLB` (8-K 2026-11-13). Innehållet i 8-K-rubrikerna är **inte verifierat**.
  * Samtliga sex saknar kurs i `state/prices.json` och läggs i `config/watchlist_us.txt` (punkt 6b, L-2).
  * Flödets övriga 8-K-rubriker 9–14/11 gällde nästan uteslutande småbolag under likviditetsgolvet, SPAC:ar och fonder. `TGT` har ett 8-K 12/11 men rapporterar 18/11 (spärr 2e). PR Newswire-flödet bestod till största delen av stämningsannonser och pressreleaser från onoterade aktörer.
  * `state/news_feed.json` (`generatedAt` 2026-11-14T01:29:15Z) täcker **10 av 10 handelsdagar** (`tradingDaysCovered` 10, `missingDays` tomt, äldsta 2026-11-02). Filen är **äldre än 24 timmar**, eftersom `news.yml` inte har kört i dag (åtgärdspunkt 1). Websök gav inga daterade bolagsnyheter för helgen 14–15/11.
* **Ur scout (g): 4.** `NVDA` och `AMAT` (rapport-261112), `CSCO` (rapport-261113) samt `APP` (rapport-261114, kandidat `261114-APP`). Rapport-261115 och -261116 hade inga case. Scouten märker `NVDA` och `CSCO` som tes FÖRSVAGAD. De poängsätts ändå för att få en kontrafaktisk rad.
* **Förra veckans bubblare (h): 4.** `DAL`, `AMZN`, `NET` och `ABNB`.
* **Rörelsegenomgången (L-7): 5.** `AMD`, `AVGO`, `RKLB`, `ANET` och `CIEN`.
* **Veckans rapportbolag (L-9-underlag): 2.** `HD` och `WMT` ligger över MA200 och avvisas med spärr 2e. De ska prövas om efter reaktionen.

**Funneln:**
* **Grind 1 (verifierad kurs) fäller 6:** `CHYM`, `INGM`, `BKNG`, `MCO`, `IONQ` och `DLB`. De loggas med `price: null`.
* **Spärr 2e (binär händelse inom 2 handelsdagar, `isEstimate: false`) fäller 3:** `NVDA` (17/11 AMC, dessutom 20,2 % under MA200), `HD` (17/11) och `WMT` (19/11).
* **Grind 2 (teknik), kurs ≤ MA200, fäller 5:** `AMAT` (370,50 mot 446,54), `CSCO` (95,64 mot 102,35), `AVGO` (347,01 mot 367,42), `RKLB` (61,53 mot 78,28) och `CIEN` (280,54 mot 406,64).
* **Grind 2 (volym < 1,5× och/eller EMA-ordning) och grind 3 (ingen färsk katalysator) fäller 7:**
  * `APP`: volym 0,59×, EMA20 under EMA200, katalysatorn 8 handelsdagar bak.
  * `AMD`: volym 1,49×, kurs under EMA50 och MA50, ingen daterad bolagskatalysator.
  * `ABNB`: volym 1,07×, katalysatorn 7 handelsdagar bak.
  * `NET`: under EMA50, volym 0,97×, katalysatorn 7 handelsdagar bak.
  * `ANET`: EMA20 under EMA50, volym 0,97×.
  * `AMZN`: volym 0,62×, ingen ny katalysator.
  * `DAL`: volym 0,77×, fallande histogram, ingen katalysator.

Volymkvoten är räknad ur `state/volume_history.json` som senaste punkten (2026-11-13) delad med snittet av de 20 föregående. Teknik och MA200 är räknade på råserien i `state/price_history.json` (250 punkter per symbol, sista punkt 2026-11-13).

### De som kom längst – och exakt varför de föll
1. **`ABNB` – 186,78 USD** (marketTime 2026-11-13T21:00:01Z, prices.json/Yahoo chart API). **L-4:** förra veckans vilande avvisning ("kurs ej verifierbar") är nu prövad med kurs och serie. Trendbilden håller: kurs över MA200 149,10, EMA20 176,71 > EMA50 171,49 > EMA200 153,74, RSI 60,9, histogram positivt (1,64 → 1,26 → 1,29), 6 månader +40,6 %, 862 MUSD/dag. **Fällt av grind 2:** volym 1,07× < 1,5×. **Grind 3:** Q3 (5/11 AMC, scout-261107) ligger 7 handelsdagar bak, utanför femdagarskravet. Kandidaten `261107-ABNB` passerade `expiresAt` 2026-11-13 som `rejected`. Ingen ny scoutpost är skapad, och boken återställer inga avgjorda poster.
2. **`APP` – 409,10 USD** (2026-11-13T21:00:01Z). Den stängde för första gången över MA200 405,79 sedan rapporten, med RSI 72,6 och ett starkt histogram (19,70 → 17,98 → 16,85, dock fallande). **Fällt av grind 2:** volym 0,59×, och uppgången har skett på krympande volym sedan 5/11. EMA20 330,41 ligger under EMA200 398,58, så trendstrukturen är inte återställd. **Grind 3:** Q3 (4/11 AMC) ligger 8 handelsdagar bak. Marginalen till MA200 är 0,81 %, så en röd session räcker för att spärren ska gälla igen.
3. **`AMD` – 534,06 USD** (2026-11-13T21:00:01Z). Veckans största rörelse (+18,93 %) och kurs över MA200 423,12. **Fällt av grind 2:** volym 1,49×, alltså 0,01 under kravet, och kursen står strax under EMA50 534,36 och under MA50 554,55. **Grind 3:** ingen daterad bolagskatalysator inom 5 handelsdagar hittades i nyhetsflödet eller websök. Rörelsen är sektorbred (AI-halvledare).

**Scout-kandidater i `state/scout_candidates.json`:** `261114-APP` → **rejected** ("grind 2 (teknik): volym 0,59x < 1,5x och EMA20 330,41 under EMA200 398,58; grind 3: katalysatorn 4/11 ligger 8 handelsdagar bak (>5)"), med `decidedBy` satt till denna rapport. Inga poster med `book: "us"` står kvar som `new`. Avvisningen är **slutlig**, inte vilande enligt L-4: kursen och serien finns, och spärren är en teknisk bedömning, inte ett datavillkor.

**Villkorade planer:** Inga öppna. Ingen ny plan läggs, eftersom ingen bubblare klarar samtliga grindar.

---

## Bubblare (watchlist inför nästa vecka)
1. **ABNB** – 186,78 USD (2026-11-13T21:00:01Z). Full EMA-stack, kurs över MA200 och lång trend. Saknar volym och en färsk katalysator. Blir prövbar på en ny daterad bolagsnyhet med volym ≥ 1,5×.
2. **AMD** – 534,06 USD (2026-11-13T21:00:01Z). Över MA200 med volym 1,49×. Blir prövbar om kursen återtar EMA50/MA50 (~534–555) och en daterad bolagskatalysator finns. NVDA-rapporten 17/11 är sektorns binära händelse, så inget köp före den (punkt 2e).
3. **HD** – 348,69 USD (2026-11-13T21:00:02Z). Över MA200 332,69 med EMA20 > EMA50 > EMA200. Rapporterar 17/11 före öppning. Prövas om enligt L-9 på reaktionsdagens verifierade stängning, som en möjlig PEAD-kandidat mot samtliga fem grindar.
4. **AMZN** – 266,66 USD (2026-11-13T21:00:00Z). Över MA200 och EMA-stack. Behöver volym och en färsk katalysator.

Samtliga fyra finns i `config/watchlist_us.txt` och har kurs i `state/prices.json` (L-2).

**Förra veckans bubblare:** **DAL** – STRUKEN (grind 2: volym 0,77×, histogram fallande 1,36 → 0,57; grind 3: ingen katalysator). **AMZN** – RANKAD UNDER (grind 2: volym 0,62×; grind 3: ingen ny katalysator), bubblare 4. **NET** – STRUKEN (grind 2: under EMA50 306,93, volym 0,97×; grind 3: Q3 7 handelsdagar bak). **ABNB** – RANKAD UNDER (grind 2: volym 1,07×; grind 3: Q3 7 handelsdagar bak), bubblare 1.
**Scout-inflöde:** (de 5 senaste: rapport-261112 till -261116; de två sista hade inga case.) **NVDA** (261112, 261113) – STRUKEN (spärr 2e: rapport 17/11; grind 2: 20,2 % under MA200). **AMAT** (261112) – STRUKEN (grind 2: under MA200 446,54). **CSCO** (261113) – STRUKEN (grind 2: under MA200 102,35, tes försvagad). **APP** (261114) – STRUKEN (grind 2: volym 0,59×, EMA20 < EMA200; grind 3: katalysator 8 handelsdagar bak).
**Villkorade bubblar-planer:** **Inga.** Ingen bubblare klarar samtliga grindar.

**Rörelsegenomgång (L-7):** rangordningen är gjord ur `state/price_history.json` över **135 amerikanska symboler** (exklusive sleeven SPY) med daterad stängning både 2026-11-06 (bas) och 2026-11-13 (mätdag). `state/movers.json` täcker bara nordiska symboler och används inte här.
* **Topp:** `AMD` +18,93 %, `AVGO` +18,16 %, `RKLB` +15,94 %, `ANET` +15,51 %, `CIEN` +15,26 %, `CRWV` +14,50 %, `NET` +13,79 %, `COHR` +13,14 %, `MU` +12,80 % och `CEG` +12,10 %.
* **Botten:** `EVCM` −22,99 %, `RGTI` −18,13 %, `IREN` −16,04 %, `MSTR` −13,43 %, `NVDA` −12,75 %, `NG` −12,03 %, `NBIS` −10,51 %, `ACHR` −9,23 %, `SMCI` −6,59 % och `AGNC` −6,26 %.

De fem största finns i bruttolistan, och `NET` är bubblare. `CRWV` (53,13 mot MA200 88,99) och `COHR` (218,15 mot 296,81) ligger under MA200. `MU` (778,31) ligger över MA200 765,61 men under EMA20/EMA50/EMA200 med negativt histogram. `CEG` (280,20) ligger 0,6 % över MA200 men under EMA200 282,12 med volym 0,60×. Ingen av dem klarar grind 2, så de har inte poängsatts separat. Resten av den amerikanska marknaden är **OKONTROLLERAD**.

## Veckans radar (kommande 5 handelsdagar)
* **Måndag 16/11** – Inga större US-makrodata. Inga innehav berörs.
* **Tisdag 17/11** – **Nvidia (`NVDA`) Q3 FY27 efter stängning** (`state/earnings_calendar.json`, konsensus EPS 2,47, intäkter 108,7 mdr USD). Det är veckans största binära risk för index och AI-hårdvara, och `^IXIC` står exakt på MA200. Samma dag kommer detaljhandelns försäljning för oktober 08:30 ET, och `HD` rapporterar före öppning.
* **Onsdag 18/11** – FOMC-protokollet 14:00 ET och bostadsbyggandet 08:30 ET. `TGT` och `LOW` rapporterar. ⚠️ RYKTE – EJ BEKRÄFTAT (CNBC, källor med insyn, 2026-11-10): `ANT` prissätts.
* **Torsdag 19/11** – jobless claims. `WMT` och `ROST` rapporterar. `ANT` väntas börja handlas på Nasdaq (samma rykte som ovan). Ett stort AI-utbud kan ge rotation bort från noterade AI-namn.
* **Fredag 20/11** – University of Michigan, slutligt konsumentförtroende för november (via scout-261116).
* **Källa och täckning (L-5):**
  * Rapportdatumen kommer ur `state/earnings_calendar.json` (`generatedAt` 2026-11-14T01:26:58Z, `errors` tomt). Den ser bara de symboler som `prices.yml` hämtar, så resten av US-universumet är **OKONTROLLERAT**. Kalendern har inte uppdaterats i dag. `CBOE` saknar rapport i fönstret.
  * Makrodatumen kommer ur scout-261116 (websök), inte ur repot.
  * Rapportförbudet (punkt 2e) gäller samtliga namn ovan.
* **Indexöversyner (L-8):** `state/news_feed.json` gav två träffar 2026-11-09 – 2026-11-14: Chime (`CHYM`, S&P MidCap 400, 13/11) och Ingram Micro (`INGM`, S&P SmallCap 600, 11/11). Båda finns i bruttolistan som `catalystType: "index"`, men de faller på grind 1 och har inga verifierade ikraftträdandedatum. Ingen fil i repot räknar upp S&P-förändringar, så den otäckta delen är **OKONTROLLERAD**.
* **Sektorer:**
  * **Medvind:** finansiell infrastruktur (`CBOE` på 250-dagarshögsta), konsument/detaljhandel inför rapporterna (`HD`, `LOW`, `TGT` och `WMT` över MA200) samt resor (`ABNB`, `DAL`).
  * **Motvind:** AI-hårdvara under MA200 trots veckans studs (`NVDA` −12,75 %, `AVGO`, `CIEN`, `CRWV`, `COHR` och `AMAT`), krypto och kryptonära (`MSTR`, `IREN`), kvant (`RGTI`) samt långdurationsmjukvara med en 10-årsränta nära 5 % (ej verifierad).

## Åtgärdspunkter till Dren (L-3)
1. **`scheduled-actions-not-firing` – ÅTERKOMMANDE, tredje måndagen.**
   * Fält: `state/prices.json` `generatedAt` = 2026-11-14T01:28:52Z, `state/news_feed.json` `generatedAt` = 2026-11-14T01:29:15Z och `state/earnings_calendar.json` `generatedAt` = 2026-11-14T01:26:58Z vid körningen 2026-11-16 13:20 UTC.
   * Senaste `prices.yml`-körning är run 911, 2026-11-14 01:25 UTC (GitHub Actions API). **Ingen schemalagd körning har startat på måndagen.**
   * **Omfång:** samtliga 321 symboler står på fredagens stängning. Sex nya g0-symboler saknar kurs.
   * **Ersättningskälla:** fredagens reguljära stängning (senaste handelsdagen) för alla beslut.
   * **Åtgärd:** kör "Hämta kurser" via `workflow_dispatch`.
2. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** Fält: `state/news_feed.json` `feeds`:
   * `globenewswire` = "HTTP 403 – båda försöken (0.0 s)"
   * `globenewswire-earnings` = "HTTP 403 – båda försöken (0.1 s)"

   **Omfång:** 2 av 6 flöden, inklusive den enda dedikerade källan för rapportöverraskningar. **Ersättningskälla:** scout-rapporternas websök och SEC 8-K.
3. **`alerts-checkedat-heartbeat-lag`.** Fält: `state/alerts.json` `checkedAt` = 2026-11-13T21:48:29Z. Inget hjärtslag sedan fredag kväll. **Omfång:** intradagsskyddet för CBOE (stop 351,50, mål 382,50, 1,89 % bort). Stop och mål är kontrollerade manuellt mot fredagens dagsintervall. Kör monitorn inte under dagens US-session riskerar ett målgenombrott att registreras först i morgon.
4. **Förbörskurs ej verifierbar från rutinens körmiljö.** `prices.json` saknar utökade kurser för i dag, och websök gav inga daterade förbörsnivåer för 2026-11-16. **Omfång:** CBOE. LÄGE B i morgon ska pröva stoppen och målet mot måndagens dagsintervall.
5. **Watchlist-taket – `watchlist-cap-vs-measurability-conflict`.** `config/watchlist_us.txt` bär långt fler symbolrader än riktmärket 25. Ingen rensning görs, eftersom punkt 6b och `prompts/gemensam_korning.md` (20 handelsdagars utvärderingsfönster) skyddar de flesta. Sex nya symboler är tillagda (`CHYM`, `INGM`, `BKNG`, `MCO`, `IONQ`, `DLB`).

---
*Detta är automatiserat beslutsstöd, inte finansiell rådgivning.*
