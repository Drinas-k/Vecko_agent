# Veckorapport: US-rotation
**Vecka:** v 48 | **Datum:** 2026-11-23
**Marknadsklimat:** Det var den svagaste veckan för boken sedan skarp start, och regimen är djupt **AV**. `^GSPC` stängde fredagen på **6 910,39 (−3,70 % fredag, vecka −8,61 %)** och `^IXIC` på **22 617,73 (−5,28 % fredag)** (prices.json/Yahoo chart API, marketTime 2026-11-20T21:35:54Z resp. 22:15:59Z). `^GSPC` ligger **5,96 % under MA200** (7 348,55), och under EMA20 7 446,66, EMA50 7 560,74 och EMA200 7 394,61. RSI(14) är 24,7 och MACD-histogrammet faller (−21,99 → −33,03 → −54,60). Utförsäljningen drevs av AI-namnen: Nvidia föll trots en rapport som slog förväntningarna (AP via AJC 2026-11-17/18), sedan Jensen Huang lämnat vd-posten. `NVDA` stängde fredagen på 125,53 (−14,01 %). En SEC-utredning om bolagets information uppges ha inletts: ⚠️ RYKTE – EJ BEKRÄFTAT (WSJ/Reuters, 2026-11-20, via scout-261123). Bitcoin föll i helgen till cirka 55 000 USD (Yahoo Finance/Motley Fool 2026-11-22, via scout-261123; ej verifierad kurs). Enligt FOMC-protokollet 18/11 väntar sig "nearly all" ledamöter en höjning med 25 bp i december (CNBC 2026-11-18, via scout-261119/-261123). USD/SEK står på 10,2245 (marketTime 2026-11-20T22:01:12Z). DXY, VIX och 10-årsräntan finns inte i `state/prices.json` och anges därför inte med siffra. Förbörsläget för i dag är **EJ VERIFIERAT**: körningen startade 13:20 UTC, och websök 2026-11-23 gav inga daterade förbörsnivåer för index eller CBOE. Thanksgiving-veckan: börsen är stängd torsdag 26/11, och fredag 27/11 är en halvdag.

---

## 0. Facit: Förra veckans val
| Aktie | Entry | Exit | Utfall | Stop/Mål träffad? |
|---|---|---|---|---|
| CBOE (ben 1, 12,5 %) | $335,53 | – (behålls) | +6,61 % (357,71, 2026-11-20T21:00:04Z); veckan −4,72 % | Nej – intervallet 17–20/11 var 354,08 (19/11) – 377,16 (17/11), alltså över stop 351,50 och under mål 382,50 (us-daglig-261118 till -261120 samt prices.json); 16/11 kontrollerades av us-daglig-261117 |
| SPY (sleeve, 87,5 %) | $773,26 | – (behålls) | −8,56 % i veckan (754,37 → 689,81); −10,79 % mot entry | Ingen stop/mål – sleeven |

**Veckans portföljutfall (viktat):** **−8,08 %**, räknat med faktiska vikter: SPY 87,5 % × −8,56 % och CBOE 12,5 % × −4,72 % (stängningar 2026-11-13 → 2026-11-20 ur `state/price_history.json`). `^GSPC` föll −8,61 %, så boken låg 0,53 pp före index. Hela skillnaden kommer från CBOE, som tappade hälften så mycket som marknaden.
**Ackumulerad avkastning sedan strategistart:** **−6,49 %**, oförändrad sedan NUE-försäljningen 2026-11-06. Sex stängda affärer i skarp drift. Den öppna CBOE-positionen och sleevens orealiserade −10,79 % ingår inte i det realiserade måttet. Siffran är exklusive USD/SEK-effekten.
**Portföljallokering denna vecka:** **12,5 % CBOE / 87,5 % SPY-sleeve.** Vikten är platt 25 % per fullt fylld position. CBOE förblir 12,5 %, eftersom ben 2 avfördes 2026-11-09. Tre aktieplatser är tomma, och regimspärren tillåter inga nya positioner.
**Lärdom:** Regimspärren gjorde det den är byggd för. Den slog AV 2026-11-18 (−0,31 % under MA200), och boken öppnade ingenting under veckans fall på −8,6 %. Kostnaden syns i sleeven: 87,5 % i SPY följer index nedåt, och regimfiltret påverkar bara nyöppning, inte sleeven. Det är den mätta avvägningen (halverad drawdown för skelettet, inte skydd för sleeven) och inget fel. CBOE:s stop ligger nu bara 1,77 % under kursen, så en vanlig nedgångsdag kan utlösa den. Tillämpade lärdomar: **L-2** (SITE, SNDK och TSN tillagda i watchlist), **L-3** (åtgärdspunkter nedan), **L-4** (PAYO avvisad på ett tillfälligt datavillkor, och ska prövas om), **L-5** (radarns källa och täckning), **L-7** (rörelsegenomgången ur price_history), **L-8** (SITE som `index`-kandidat) och **L-9** (HD, TGT och WMT omprövade efter sina rapporter).

---

## Case: INGA NYA VALDA DENNA VECKA

**Regimfiltret är AV** (punkt 2b): `^GSPC` 6 910,39 ligger 5,96 % under MA200 7 348,55, räknat ur `state/price_history.json` (250 punkter, sista 2026-11-20). Därför öppnas **inga nya positioner**. Alla 15 aktiekandidater i bruttolistan avvisas med regimspärren namngiven. För att det kontrafaktiska underlaget ska vara användbart prövades de också mot övriga grindar, och de spärrar som hade fällt dem även med regimen PÅ står i `reason`. Det befintliga innehavet `CBOE` poängsätts inte om (punkt 0b), eftersom tesen är intakt och varken stop eller mål har träffats.

**CBOE – BEHÅLL.** Kursen är 357,71 (+6,61 % mot entry 335,53; fredagens intervall 355,35–367,255; marketTime 2026-11-20T21:00:04Z, prices.json/Yahoo chart API). Kurs över EMA20 350,85 > EMA50 326,94 > EMA200 298,17 och 19,54 % över MA200. RSI 59,5, men MACD-histogrammet är negativt och fallande (0,08 → −1,09 → −1,92). Volymen är 0,90×, och snittomsättningen 434 MUSD/dag. Tesen (Q3 30/10: justerat EPS 3,63, +36 %, sänkt opex-guide; SEC 8-K ex. 99.1) är intakt. Ingen rapport ligger inom fönstret i `state/earnings_calendar.json`. Stop 351,50 och mål 382,50 är oförändrade. Stoppen flyttas aldrig ned, och efter en nedgångsvecka är ingen trailing-höjning motiverad. Förbörskurs för i dag är **EJ VERIFIERAD**.

**Bred scanning – varifrån bruttolistan kom (15 aktiekandidater, samtliga loggade i `state/decisions.json` med `mode: "A"`, plus BEHÅLL-rader för CBOE och sleeven, alltså 17 rader):**
* **Ur nyhetsflödet (g0): 6.**
  * `INTU` (8-K 2026-11-19), `TEVA` (8-K 2026-11-18), `BAC` (8-K 2026-11-20), `SNDK` (8-K 2026-11-19) och `TSN` (8-K 2026-11-20). Innehållet i 8-K-rubrikerna är **inte verifierat**.
  * `SITE` – "SiteOne Landscape Supply Set to Join S&P SmallCap 600" (PR Newswire 2026-11-16). Det är en `index`-katalysator enligt L-8, men ikraftträdandedatumet är inte verifierat.
  * `SITE`, `SNDK` och `TSN` saknar kurs i `state/prices.json` och läggs i `config/watchlist_us.txt` (punkt 6b, L-2).
  * Övriga rubriker 16–20/11 gällde främst småbolag under likviditetsgolvet, SPAC:ar, fonder, stämningsannonser och onoterade aktörer.
  * `state/news_feed.json` (`generatedAt` 2026-11-20T22:15:20Z) täcker **10 av 10 handelsdagar** (`tradingDaysCovered` 10, `missingDays` tomt, äldsta 2026-11-09). Filen är **äldre än 24 timmar** (cirka 39 timmar), eftersom `news.yml` inte har kört i dag (åtgärdspunkt 1). Websök gav inga daterade bolagsnyheter för helgen.
* **Ur scout (g): 3.** `TGT` (rapport-261119), `WMT` (rapport-261120) och `PAYO` (rapport-261121, kandidat `261121-PAYO`). Rapport-261122 och -261123 hade inga case.
* **Förra veckans bubblare (h): 4.** `ABNB`, `AMD`, `HD` och `AMZN`.
* **Rörelsegenomgången (L-7): 2.** `CBRL` och `S`, veckans två största uppgångar.

**Funneln:**
* **Spärr 2b (regim AV) fäller samtliga 15.**
* **Grind 1 (verifierad kurs) hade dessutom fällt 4:** `PAYO`, `SITE`, `SNDK` och `TSN`. De loggas med `price: null`.
* **Grind 2 (kurs ≤ MA200) hade fällt 3:** `AMD` (424,39 mot 429,79), `INTU` (270,44 mot 347,05, RSI 26,8) och `BAC` (47,04 mot 54,72).
* **Grind 2 (EMA-ordning, volym under 1,5× eller fallande histogram) och/eller grind 3 (ingen färsk katalysator) hade fällt 7:**
  * `ABNB`: under EMA20, volym 1,06×.
  * `AMZN`: under EMA20/50/200, volym 1,49×.
  * `HD`: histogrammet fallande.
  * `WMT`: histogrammet negativt.
  * `TEVA`: volym 0,86×.
  * `CBRL`: volym 0,97×, och ingen katalysator.
  * `S`: volym 0,63×, och ingen katalysator.
* **Utan regimspärren hade bara `TGT` klarat grind 2.** Se nedan.

Volymkvoten är räknad ur `state/volume_history.json` som senaste punkten (2026-11-20) delad med snittet av de 20 föregående. Teknik och MA200 är räknade på råserien i `state/price_history.json`.

### De som kom längst – och exakt varför de föll
1. **`TGT` – 165,83 USD** (marketTime 2026-11-20T21:04:32Z, prices.json/Yahoo chart API). Detta är L-9-omprövningen efter Q3-rapporten 18/11.
   * Tekniken håller: kurs 20,12 % över MA200 138,06, EMA20 160,48 > EMA50 157,20 > EMA200 139,09, RSI 59,1, positivt histogram (0,58 → 0,77 → 0,74), volym **1,57×**, 733 MUSD/dag och 6 månader +32,0 %.
   * Aktien steg +2,71 % under en vecka då index föll −8,61 %. Det var veckans tredje bästa US-rörelse.
   * **Fällt enbart av spärr 2b (regim AV).** Katalysatorn (Q3 18/11) ligger 3 handelsdagar bak.
   * Scoutkandidaten `261119-TGT` avgjordes tidigare som `rejected` med regimspärren, och boken återställer inga avgjorda poster.
   * Om regimen slår PÅ innan katalysatorn passerat fem handelsdagar (25/11) prövas TGT som bubblare. Med ^GSPC 5,96 % under MA200 är det inte sannolikt.
2. **`WMT` – 127,95 USD** (2026-11-20T21:00:00Z). Kurs 7,53 % över MA200 och full EMA-stack. Volymen 1,91× bekräftar fredagens relativa styrka (+1,52 % mot index −3,70 %). **Fällt av spärr 2b, och dessutom av grind 2:** histogrammet är negativt (−0,26 → −0,42 → −0,40).
3. **`HD` – 339,04 USD** (2026-11-20T21:00:03Z). Kurs 2,22 % över MA200 och volym 1,67×, men EMA20 336,91 ligger bara strax över kursen och histogrammet faller (−1,42 → −2,21). **Fällt av spärr 2b, och av grind 2/3:** rapportreaktionen 17/11 blev inte positiv.

**Scout-kandidater i `state/scout_candidates.json`:** `261121-PAYO` → **rejected** ("kurs ej verifierbar (PAYO saknas i prices.json); även spärr c: regimen av – inga nya positioner. Tillfälligt datavillkor (L-4): prövas om när kurs finns."), med `decidedBy` satt till denna rapport. Katalysatorn (OCC:s villkorade godkännande av PAYO Digital Bank, Payoneer via PR Newswire 2026-11-20T22:02Z) är bekräftad men villkoren är inte offentliga. Avvisningen är **vilande** enligt L-4: PAYO lades i watchlist 2026-11-21, men ingen pris-körning har gått sedan dess. Inga poster med `book: "us"` står kvar som `new`.

**Villkorade planer:** Inga öppna. Ingen ny plan läggs, eftersom regimspärren gäller.

---

## Bubblare (watchlist inför nästa vecka)
1. **TGT** – 165,83 USD (2026-11-20T21:04:32Z). Den enda kandidaten som klarar grind 2 och har en färsk bekräftad katalysator (Q3 18/11). Den blockeras enbart av regimen, och katalysatorn passerar fem handelsdagar 25/11.
2. **WMT** – 127,95 USD (2026-11-20T21:00:00Z). Relativ styrka och volym 1,91×. Blir prövbar om histogrammet vänder upp och regimen slår PÅ.
3. **PAYO** – KURS EJ VERIFIERAD. Bekräftad regulatorisk katalysator 20/11 (OCC). Prövas om enligt L-4 när `state/prices.json` bär en post-event-kurs.
4. **ABNB** – 170,36 USD (2026-11-20T21:00:02Z). Kurs 13,26 % över MA200 med en lång trend (6 månader +28,7 %), men under EMA20 och utan färsk katalysator.

Samtliga fyra finns i `config/watchlist_us.txt` (L-2). Tre av dem har kurs i `state/prices.json`, men PAYO saknar kurs i väntan på nästa pris-körning.

**Förra veckans bubblare:** **ABNB** – RANKAD UNDER (spärr 2b; grind 2: under EMA20 176,94, volym 1,06×; grind 3: Q3 5/11 långt bak), bubblare 4. **AMD** – STRUKEN (spärr 2b; grind 2: under MA200 429,79, histogram negativt). **HD** – STRUKEN (spärr 2b; grind 2/3: fallande histogram, rapportreaktionen 17/11 inte positiv). **AMZN** – STRUKEN (spärr 2b; grind 2: under EMA20/50/200, volym 1,49×).
**Scout-inflöde:** (de 5 senaste: rapport-261119 till -261123; de två sista hade inga case.) **TGT** (261119) – RANKAD UNDER (enbart spärr 2b), bubblare 1. **WMT** (261120) – RANKAD UNDER (spärr 2b, grind 2: histogram), bubblare 2. **PAYO** (261121) – RANKAD UNDER (spärr b: kurs ej verifierbar, spärr 2b), bubblare 3.
**Villkorade bubblar-planer:** **Inga.** Regimspärren gäller.

**Rörelsegenomgång (L-7):** rangordningen är gjord ur `state/price_history.json` över **141 amerikanska symboler** (exklusive sleeven SPY) med daterad stängning både 2026-11-13 (bas) och 2026-11-20 (mätdag). `HCA`, `NOC`, `WBD`, `BKH` och `KVUE` saknar punkt 2026-11-20 och ingår inte. `state/movers.json` täcker bara nordiska symboler och används inte här.
* **Topp:** `CBRL` +5,68 %, `S` +3,20 %, `TGT` +2,71 %, `EVCM` +1,58 %, `ZS` +1,22 %, `KHC` +1,12 %, `PNR` +0,48 % och `VZ` +0,26 %. Bara 8 av 141 symboler steg.
* **Botten:** `IREN` −34,95 %, `MSTR` −30,30 %, `NBIS` −29,83 %, `ASTS` −28,62 %, `IONQ` −28,25 %, `APLD` −28,05 %, `ACHR` −27,79 %, `MARA` −27,25 %, `CLSK` −26,47 % och `RKLB` −26,18 %.

`CBRL`, `S` och `TGT` finns i bruttolistan. `ZS` (rapport 2/12) och `EVCM`/`KHC`/`PNR`/`VZ` hade inga daterade katalysatorer och har inte poängsatts separat. Med regimen AV hade de ändå fallit. Resten av den amerikanska marknaden är **OKONTROLLERAD**.

## Veckans radar (kommande 5 handelsdagar)
* **Måndag 23/11** – Flash-PMI. `HPE` rapporterar efter stängning (`state/earnings_calendar.json`, `isEstimate: false`). Enligt scout-261123 rapporterar även `ZM` efter stängning. Inga innehav berörs.
* **Tisdag 24/11** – Conference Boards konsumentförtroende. `CLSK` rapporterar (kalendern). Enligt scout-261123 rapporterar `ADI` och `MDT` före öppning och `DELL`, `HPQ`, `ADSK` och `WDAY` efter stängning.
* **Onsdag 25/11 – veckans tyngsta dag:** PCE för oktober (kärnan väntas +0,27 % m/m), andra BNP-skattningen för Q3, varaktiga varor, jobless claims och Beige Book (via scout-261123). Det är sista inflationssiffran före FOMC 9/12. `DE` rapporterar före öppning (kalendern).
* **Torsdag 26/11** – Thanksgiving, NYSE och Nasdaq stängda.
* **Fredag 27/11** – Halvdag, stängning 13:00 ET.
* **Källa och täckning (L-5):**
  * Rapportdatumen kommer ur `state/earnings_calendar.json` (`generatedAt` 2026-11-21T02:11:10Z, `errors` tomt). Kalendern ser bara de symboler som `prices.yml` hämtar, så resten av US-universumet är **OKONTROLLERAT**. `CBOE` har ingen rapport i fönstret.
  * Makro- och övriga rapportdatum kommer ur scout-261123 (websök), inte ur repot.
  * Rapportförbudet (punkt 2e) gäller samtliga namn ovan.
* **Indexöversyner (L-8):** `state/news_feed.json` gav en träff 2026-11-16 – 2026-11-20: SiteOne (`SITE`, S&P SmallCap 600, 16/11). Den finns i bruttolistan som `catalystType: "index"`. Ingen fil i repot räknar upp S&P-förändringar, så den otäckta delen är **OKONTROLLERAD**.
* **Sektorer:**
  * **Medvind (relativt):** stora detaljhandlare (`TGT` och `WMT` steg mot index), defensiva namn (`VZ`, `KHC`, `AWK`, `PG` nära oförändrade) och finansiell infrastruktur (`CBOE` −4,72 % mot index −8,61 %).
  * **Motvind:** AI-hårdvara och AI-infrastruktur (`NVDA`, `NBIS`, `APLD`, `IREN`), krypto och kryptonära (`MSTR`, `MARA`, `CLSK`), kvant (`IONQ`) och rymd (`ASTS`, `RKLB`). Till det kommer en väntad räntehöjning i december.
* **Regimen:** ^GSPC måste stänga över MA200 (cirka 7 349, +6,3 % från fredagens stängning) innan boken får öppna nya positioner.

## Åtgärdspunkter till Dren (L-3)
1. **`scheduled-actions-not-firing` – ÅTERKOMMANDE, fjärde måndagen.**
   * Fält: `state/prices.json` `generatedAt` = 2026-11-21T02:13:44Z, `state/news_feed.json` `generatedAt` = 2026-11-20T22:15:20Z och `state/alerts.json` `checkedAt` = 2026-11-20T22:30:09Z vid körningen 2026-11-23 13:20 UTC.
   * Main:s senaste commit var `6ea6f11` (06:46 UTC, nordisk rotation). Ingen pris-, nyhets- eller monitorkörning har landat på main under måndagen.
   * **Omfång:** samtliga 331 symboler står på fredagens stängning. `PAYO`, `DELL`, `HPQ`, `BBY`, `ZM`, `ADI`, `ADSK`, `WDAY`, `MDT` och de tre nya g0-symbolerna saknar kurs.
   * **Ersättningskälla:** fredagens reguljära stängning (senaste handelsdagen) för alla beslut.
   * **Åtgärd:** kör "Hämta kurser" via `workflow_dispatch` och kontrollera Actions-fliken.
2. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** Fält: `state/news_feed.json` `feeds`:
   * `globenewswire` = "HTTP 403 – båda försöken (0.0 s)"
   * `globenewswire-earnings` = "HTTP 403 – båda försöken (0.0 s)"

   **Omfång:** 2 av 6 flöden, inklusive den enda dedikerade källan för rapportöverraskningar. **Ersättningskälla:** scout-rapporternas websök och SEC 8-K.
3. **`alerts-checkedat-heartbeat-lag`.** Fält: `state/alerts.json` `checkedAt` = 2026-11-20T22:30:09Z. Inget hjärtslag sedan fredag kväll. **Omfång:** intradagsskyddet för CBOE, vars stop 351,50 ligger bara 1,77 % under kursen. Stop och mål är kontrollerade manuellt mot fredagens dagsintervall. Kör monitorn inte under dagens US-session registreras ett stopgenombrott först i morgon.
4. **Förbörskurs ej verifierbar från rutinens körmiljö.** `prices.json` saknar utökade kurser för innehaven, och websök gav inga daterade förbörsnivåer för 2026-11-23. **Omfång:** CBOE och SPY. LÄGE B i morgon ska pröva stoppen mot måndagens dagsintervall.
5. **Watchlist-taket – `watchlist-cap-vs-measurability-conflict`.** `config/watchlist_us.txt` bär långt fler symbolrader än riktmärket 25. Ingen rensning görs, eftersom punkt 6b och `prompts/gemensam_korning.md` (20 handelsdagars utvärderingsfönster) skyddar de flesta. Tre nya symboler har lagts till (`SITE`, `SNDK`, `TSN`).

---
*Detta är automatiserat beslutsstöd, inte finansiell rådgivning.*
