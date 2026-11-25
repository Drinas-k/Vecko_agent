# Daglig Scout: USA & Krypto
**Datum:** 2026-11-25
**Marknadsklimat:** Måndagens Nvidia-studs höll inte. På tisdagen föll `^GSPC` 0,50 % och `^IXIC` 1,48 %, och halvledarindexet tappade enligt BigGo nära 8 % medan Dow steg 0,85 %. Kvällens rapporter från Dell, Workday och Autodesk slog förväntningarna, men alla tre handlades enligt artiklar svagt eller motstridigt i efterhandeln. Regimfiltret för US-boken är fortfarande **AV**. Krypto fortsätter nedåt: BTC ligger under 60 000 USD och spot-ETF:erna har haft rekordutflöden i november. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (`261124-HPE` och `261124-ZM` har nu fått en verifierad kurs efter katalysatorn och flaggas för omprövning), L-5 (negativa påståenden avgränsas till de källor som genomsökts) och L-6 (spärrar citeras ur sin fil). L-1, L-2 och L-7–L-9 gäller inte scouten.

## Marknadsöversikt

`git pull` och `git fetch origin main` kördes 2026-11-25 cirka 05:48 UTC (06:48 CET). `origin/main` var då `a997edb`. Kurserna kommer ur `state/prices.json` (`generatedAt` 2026-11-25T04:09:54Z, `schemaVersion` 2026-08-02-prevclose, `okCount` 296 av 298, `wideAt` 2026-11-25T01:09:28Z), hämtade från Yahoo Finance chart API via GitHub Actions. Nyhetsflödet (`state/news_feed.json`, `generatedAt` 2026-11-25T01:26:45Z) täcker **10 av 10 handelsdagar** (2026-11-11 – 2026-11-25, `missingDays` tomt).

| Symbol | Nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 7 201,09 | −0,50 % (tis) | 2026-11-24T21:54:10Z |
| `^IXIC` | 23 733,54 | −1,48 % (tis) | 2026-11-24T22:15:59Z |
| `BTC-USD` | 59 161,18 | −1,46 % mot den daterade punkten 2026-11-24 (60 040,62) | 2026-11-25T04:08:34Z |
| `ETH-USD` | 1 657,80 | −1,45 % mot den daterade punkten 2026-11-24 (1 682,26) | 2026-11-25T04:08:45Z |
| `SPY` (sleeve) | 718,78 | −0,49 % (tis) | 2026-11-24T21:00:00Z |

Kryptots rörelse är räknad mot daterade stängningar i `state/price_history.json`, inte mot `previousClose` (se åtgärdspunkt 3). Indexens stängningar stämmer med pressens siffror (Motley Fool och Yahoo Finance, 2026-11-24).

**Teknik** (räknad på råserien i `state/price_history.json`):
- `^GSPC` ligger **2,04 % under MA200** (7 351,26), med RSI(14) 40,3. **Regimfiltret för US-boken är AV.** `SPY` ligger 1,95 % under MA200 (733,04).
- `^IXIC` ligger 5,69 % under MA200 (25 165,19), med RSI 39,5.
- `BTC-USD` ligger 17,83 % under MA200 (71 995,77), med RSI 23,2. `ETH-USD` ligger 21,22 % under MA200 (2 104,34), med RSI 26,9.
- Tisdagens största fall bland bevakade namn (marketTime 2026-11-24T21:00–21:05Z): `ADI` 312,95 (−17,37 %, efter rapport före öppning), `HPE` 40,19 (−16,31 %, efter rapport), `DELL` 295,28 (−11,83 %, före kvällens rapport) och `NVDA` 155,38 (−5,86 %). `MDT` gav 96,13 (−4,56 %) efter sin rapport.

## Ekonomiska siffror & kalender

**Senaste utfall:**
- **Conference Boards konsumentförtroende för november (tis 2026-11-24):** konsensus låg på 92,0–92,8 mot 91,7 i oktober (Gotrade; ZeroHedge, veckoförhandsvisningar). **Utfallet är OKONTROLLERAT**, eftersom websöket 06:00 UTC inte gav siffran.
- **S&P Global flash-PMI november (2026-11-23):** Composite blev 54,6 mot 55,9, och prisindikatorerna ligger kvar över Feds mål (rapport-261124).
- **KPI oktober (2026-11-10):** +0,4 % totalt och +0,3 % i kärnan m/m, båda över förväntan. Enligt FOMC-protokollet (2026-11-18) väntar sig "nearly all" ledamöter +25 bp i december.

**Kommande:**
- **Ons 2026-11-25 (i dag) – MEST MARKNADSRÖRANDE:** PCE för oktober, där kärnan väntas +0,3 % m/m och totalen +3,8 % å/å mot 3,6 % (Gotrade; Kalkine). Samtidigt kommer andra BNP-skattningen för Q3 (väntat cirka 3,5 % mot 3,4 % i första skattningen enligt TheStreet), varaktiga varor (prognoserna sprider sig mellan +0,5 % och +2,5 %), jobless claims och på kvällen Beige Book. Det är sista inflationssiffran före FOMC 9/12. `DE` rapporterar före öppning (`state/earnings_calendar.json`, `isEstimate: false`).
- **Tor 2026-11-26:** Thanksgiving, börsen stängd. **Fre 2026-11-27:** halvdag med stängning 13:00 ET.
- **Rapporter nästa 10 handelsdagar** (US-symboler i `state/earnings_calendar.json`, `generatedAt` 2026-11-25T01:07:23Z, `errors` tomt): 12-01 `MRVL`, 12-02 `CBRL` och `FIVE`, 12-03 `COO` och `S`, 12-09 `AVGO`. **L-5:** kalendern känner bara de symboler som `prices.yml` hämtar, så resten av det amerikanska universumet är **OKONTROLLERAT**. Samtliga datum är bevakningsposter enligt punkt 8, aldrig köpförslag.

## Aktuella händelser & katalysatorer

- **Dell Q3 FY27 (2026-11-24, efter stängning):** intäkterna blev 54,94 mdr USD (+103 %) mot väntade 49,32, och justerad EPS 9,45 mot 6,59. AI-serverintäkterna var 22,0 mdr (+291 %) och AI-orderboken 132,3 mdr. Q4-guidningen (56,3 mdr, EPS 8,40) ligger över konsensus, och styrelsen godkände återköp för 25 mdr USD (Dell 8-K ex. 99.1, SEC 2026-11-24; CNBC 2026-11-24; Investing.com 2026-11-24). Uppgifterna om efterhandeln går isär: CNBC:s senare version skriver "fell", medan SMB Tech anger +3–4 % till cirka 305. Siffrorna är inte verifierade. → **Case 1.**
- **Workday Q3 FY27 (2026-11-24, efter stängning):** intäkterna blev 2,705 mdr (+11,2 %) och prenumerationsintäkterna 2,532 mdr (+12,8 %). cRPO var 9,216 mdr (+12,3 %), och helårsguidningen för prenumerationer höjdes till 9,958 mdr. Aktien föll ändå mer än 7 % i efterhandeln på en Q4-guidning kring +10 % (Workday 8-K ex. 99.1, SEC 2026-11-24; StockTitan; Investing.com, 2026-11-24). → **Case 2.**
- **Autodesk Q3 FY27 (2026-11-24, efter stängning):** intäkterna blev 2,16 mdr (+17 %) och justerad EPS 3,20, båda över guidningens topp. Helårsguidningen höjdes. Enligt en enda källa föll aktien cirka 4,5 % till cirka 244,27 efter stängning (Autodesk via PR Newswire; StockTitan; Investing.com, 2026-11-24). → **Case 3.**
- **Best Buy Q3 FY27 (2026-11-24):** justerad EPS blev 1,62 mot 1,49, jämförbar försäljning +6,1 % (den högsta på fem år), och helårsguidningen för EPS höjdes till 6,90–7,05 (Investing.com 2026-11-24). Rapporttiden (före eller efter öppning) är **inte verifierad**, så stängningen 99,62 (+2,70 %, 2,32× volym) kan inte säkert räknas som en kurs efter katalysatorn. Kandidatposten får `price: null`.
- **HP Inc Q4 FY26 (2026-11-24, efter stängning):** justerad EPS blev 0,83 mot 0,75 och intäkterna 16,0 mdr (+9,3 %). Utdelningen höjs till 0,31 per kvartal, och FY27-guidningen för EPS är 3,15–3,45. Efterhandeln var ungefär oförändrad, cirka 28,19 (MarketBeat 2026-11-24, inte verifierad). Ingen kandidatpost skapas, eftersom överraskningen är liten.
- **Analog Devices (`ADI`), rapport före öppning 2026-11-24:** −17,37 % till 312,95 (marketTime 2026-11-24T21:00:01Z), 17,29 % under MA200. Innehållet i rapporten har inte verifierats. Det är en negativ reaktion och ingen köpkandidat.
- **Krypto:** spot-bitcoin-ETF:erna hade nettoutflöden på 569,7 MUSD den 24/11, varav IBIT 509,3 MUSD. Novembers utflöden uppgår till 4,71 mdr USD, ett månadsrekord som passerar junis 4,51 mdr (The Block 2026-11-24; SoSoValue). Bitcoin- och Ethereum-ETF:erna tappade tillsammans 728 MUSD på en dag (Lookonchain via KuCoin, 2026-11-24). Ingen positiv katalysator för `BTC-USD` eller `ETH-USD` har hittats.
- **Brus i flödet:** Levi & Korsinsky publicerade "fairness"-utredningar om uppköpen av Varonis, Baldwin och Surgery Partners (PR Newswire 2026-11-24T23:12Z, rubriker). Det är advokatreklam och ingen ny katalysator, så inga poster skapas.

## Uppföljning av tidigare case

- `HPE` (rapport-261124): 48,02 (pre-event) → **40,19** (−16,31 %, `state/prices.json`, marketTime 2026-11-24T21:03:36Z, Yahoo chart API), på 2,86× 20-dagarsvolymen. Aktien ligger nu 6,36 % under MA200. Tesen är **PUNKTERAD**: marknaden sålde på Q1-guidningen trots beatet.
- `ZM` (rapport-261124): 86,03 (pre-event) → **88,40** (+2,75 %, `state/prices.json`, marketTime 2026-11-24T21:00:01Z, Yahoo chart API), på 1,96× volym. Tesen är **INTAKT**, men aktien ligger fortfarande 4,23 % under MA200.

**L-4:** `261124-HPE` och `261124-ZM` avvisades 2026-11-24 på "kurs ej verifierbar – stängningen 23/11 är pre-event", ett tillfälligt datavillkor. Nu finns en reguljär stängning en hel handelsdag efter katalysatorn (23/11 efter stängning → 24/11). Båda posterna gäller t.o.m. 2026-12-02 och ska prövas på nytt av US-boken mot samtliga grindar och loggas. Båda faller dessutom på spärr (c), regimen, och på "kurs ≤ MA200 blockerar nya aktiepositioner" i `prompts/gemensam_korning.md`. `261121-PAYO` ligger 15,13 % över MA200 men vilar fortfarande på regimspärren.

**Kandidatkön (`state/scout_candidates.json`):** före dagens körning fanns 132 poster, varav 123 `rejected`, 9 `promoted` och 0 `new`. I dag läggs **4 nya poster** till, alla med `price: null` eftersom ingen kurs efter katalysatorn finns: `261125-DELL`, `261125-WDAY`, `261125-ADSK` och `261125-BBY`.

**US-boken (läses, ändras inte):** `CBOE` såldes på stop 2026-11-24, och boken ligger 100 % i sleeven `SPY` 718,78. Ingen pending-plan är öppen.

## Dagens case
### Case 1: Dell Technologies (DELL / NYSE)
**Katalysator:** Q3-rapporten för FY27 släpptes 2026-11-24 efter stängning. Intäkterna blev 54,94 mdr USD (+103 % å/å) mot 49,32 väntat, och justerad EPS 9,45 mot 6,59. AI-optimerade servrar gav 22,0 mdr (+291 %), orderingången 60,2 mdr och AI-orderboken 132,3 mdr. Q4-guidningen är cirka 56,3 mdr och EPS 8,40, mot konsensus 53,61 mdr och 7,50. Helårsguidningen höjdes till 202 mdr (+78 %), och återköpsramen är 25 mdr USD (Dell 8-K ex. 99.1, SEC 2026-11-24; CNBC 2026-11-24; Investing.com 2026-11-24). Utfallet är bekräftat.
**Bull case:** Det här är den tydligaste bekräftelsen hittills på att efterfrågan på AI-infrastruktur håller, trots höstens AI-utförsäljning. Orderboken motsvarar mer än två kvartals intäkter. Återköpet på 25 mdr motsvarar enligt egen grov beräkning cirka 12 % av börsvärdet, vilket är ett golv.
**Bear case:** AI-servrarna späder ut marginalen (KuCoin flash: "profit margins signal warning"). Aktien ligger 15,67 % under MA200 och har halverats från 60-dagarstoppen 588,40. Efterhandeln är motstridig, och marknaden sålde både HPE och ADI efter starka eller neutrala rapporter i går. Regimfiltret är AV.
**Setup:** Stängningen 295,28 (`state/prices.json`, marketTime 2026-11-24T21:04:51Z, Yahoo chart API) är en **PRE-event-kurs**, så kandidatens `price` är `null`. MA200 ligger på 350,14, RSI(14) är 36,5 och volymen var 2,34× 20-dagarssnittet. Ingen P/E kan verifieras ur state. `prices.yml` fyller i kursen efter katalysatorn automatiskt. Caset kan inte bli ett köp förrän kursen ligger över MA200 **och** regimen är på. Det redovisas som bevakning.

### Case 2: Workday (WDAY / NASDAQ)
**Katalysator:** Q3-rapporten för FY27 släpptes 2026-11-24 efter stängning. Intäkterna blev 2,705 mdr (+11,2 %) och prenumerationsintäkterna 2,532 mdr (+12,8 %). cRPO var 9,216 mdr (+12,3 %), och helårsguidningen för prenumerationer höjdes till 9,958 mdr (cirka +13 %), med en non-GAAP-rörelsemarginal på 31,5 %. AI-ARR steg 130 % till cirka 750 MUSD, och bolaget återköpte aktier för 750 MUSD (Workday 8-K ex. 99.1, SEC 2026-11-24; StockTitan; BigGo, 2026-11-24). Utfallet är bekräftat.
**Bull case:** cRPO växer snabbare än intäkterna (12,3 % mot 11,2 %), vilket talar för att tillväxten håller. Marginalen expanderar, AI-produkterna tar fart och återköpen fortsätter. Aktien ligger över MA200, till skillnad från de flesta tekniknamnen.
**Bear case:** Q4-guidningen för prenumerationer (2,600 mdr, cirka +10 %) visar att tillväxten bromsar, och US-tillväxten har svalnat till 10 %. Efterhandeln föll mer än 7 % (Investing.com, inte verifierat). Ett fall av den storleken tar aktien till ungefär MA200. Regimfiltret är AV.
**Setup:** Stängningen 179,23 (`state/prices.json`, marketTime 2026-11-24T21:00:01Z, Yahoo chart API) är en **PRE-event-kurs**, så kandidatens `price` är `null`. Aktien ligger 14,51 % över MA200 (156,53), med RSI(14) 39,5 och 1,82× volym. 60-dagarstoppen är 209,99. En efterhandel på −7 % motsvarar cirka 166, fortfarande över MA200 enligt egen beräkning. Ingen P/E kan verifieras ur state.

### Case 3: Autodesk (ADSK / NASDAQ)
**Katalysator:** Q3-rapporten för FY27 släpptes 2026-11-24 efter stängning. Intäkterna blev 2,16 mdr (+17 %, +14 % i fast valuta) och non-GAAP EPS 3,20, båda över guidningens topp. Helårsguidningen höjdes, med billings-mitten på 8,625 mdr och intäktsmitten på cirka 8,368 mdr. Bolaget återköpte 1,5 miljoner aktier för 350 MUSD (Autodesk via PR Newswire 2026-11-24; StockTitan 2026-11-24). Utfallet är bekräftat.
**Bull case:** Intäkterna accelererar till 17 % och helårsguidningen höjs. Aktien ligger över MA200 med neutral RSI, och den rekurrenta modellen är mindre utsatt för AI-hårdvarucykeln som sänker halvledarna.
**Bear case:** Efterhandeln föll cirka 4,5 % till cirka 244,27, enligt en enda källa (Investing.com, inte verifierat). Valutan bidrog med cirka 3 procentenheter av tillväxten. Regimfiltret är AV.
**Setup:** Stängningen 255,70 (`state/prices.json`, marketTime 2026-11-24T21:00:01Z, Yahoo chart API) är en **PRE-event-kurs**, så kandidatens `price` är `null`. Aktien ligger 9,22 % över MA200 (234,12), med RSI(14) 53,6 och 1,42× volym. 60-dagarstoppen är 270,09. Ingen P/E kan verifieras ur state.

## Makro- & sektorfaktorer att bevaka

- **Regimen (viktigast):** `^GSPC` ligger 2,04 % under MA200, ett större avstånd än i går (1,54 %). S&P 500 har enligt Motley Fool förlorat åtta av de senaste nio sessionerna. Regimfiltret är AV, så det blir inga nya aktiepositioner oavsett hur starka rapporterna är.
- **Inflation och Fed:** dagens PCE avgör om marknaden prisar in decemberhöjningen fullt ut. KPI och PMI-priserna talar för en hög siffra. Räntor, DXY och VIX går inte att verifiera ur state (åtgärdspunkt 2).
- **Sektorrotation:** halvledarna föll kraftigt (`ADI` −17 %, `NVDA` −6 %), medan Dow steg, vilket pekar på en rotation till defensiva och cykliska namn. Mjukvara med rekurrenta intäkter (WDAY, ADSK) och stark detaljhandel (BBY) ligger över MA200, men även deras beats säljs på guidningen.
- **Krypto:** rekordutflödena ur ETF:erna och en RSI kring 23–27 visar en översåld marknad utan katalysator. Det finns inget case.
- **Varför bara bevakning i dag:** alla tre casen är bekräftade överraskningar, men ingen har ännu en kvalificerad kurs efter katalysatorn, regimen är AV och Dell ligger dessutom under MA200. Gårdagen visade att marknaden säljer på guidningen även efter tydliga beats (HPE −16 %).

**Watchlist-hygien:** `config/watchlist_us.txt` har långt fler symboler än riktmärket 25. Ingen rensning görs, eftersom skydden i `prompts/gemensam_korning.md` gäller: sleeven och indexen, kandidater inom `expiresAt` (`PAYO`, `WMT`, `TGT`, `HPE`, `ZM`, `DELL`, `WDAY`, `ADSK`, `BBY`), rapportbolag inom 10 handelsdagar och beslut inom 20-dagarsfönstret. Den genomgången hör hemma i US-rotationen. Inga tillägg behövs: dagens samtliga kandidater har redan en kurs i `state/prices.json`.

### Åtgärdspunkter till Dren (L-3)

1. **`crypto-previousclose-misdated` – ÅTERKOMMANDE.** `quotes["BTC-USD"].previousClose` är 61 210,98, men den daterade punkten för 2026-11-24 i `state/price_history.json` är 60 040,62. ETH visar samma mönster: 1 708,85 mot 1 682,26. **Omfång:** 2 av 2 mynt. Räknat ur `previousClose` blir dagsrörelsen −3,35 % i stället för −1,46 % för BTC. **Ersättningskälla:** daterade stängningar i `price_history.json`, som tabellen ovan använder.
2. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas i `state/prices.json`. **Omfång:** samtliga makrovärden i rapporten. Halvledarindexets fall kan i dag bara anges ur en artikel (BigGo).
3. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** `feeds.globenewswire` och `feeds.globenewswire-earnings` ger fortfarande `"HTTP 403 – båda försöken (0.0 s)"`. **Omfång:** 2 av 6 flöden. **Ersättningskälla:** websök, prnewswire, mfn och SEC 8-K.
4. **`scout-cannot-fetch-press-release-body` – ÅTERKOMMANDE.** I dag nekades `www.cnbc.com` och `www.tradingkey.com` av miljöns nätverkspolicy (ENOTFOUND), så samtliga rapportsiffror kommer ur sökutdrag. Därför är Best Buys rapporttid och efterhandelskurserna inte verifierade. **Omfång:** samtliga pressmeddelandetexter i dagens rapport.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
