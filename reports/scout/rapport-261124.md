# Daglig Scout: USA & Krypto
**Datum:** 2026-11-24
**Marknadsklimat:** Nvidia återinsatte Jensen Huang som vd, och marknaden svarade med en historisk studs på måndagen: `^GSPC` steg 4,73 % och `^IXIC` 6,51 %. Båda indexen ligger ändå kvar under MA200, så US-bokens regimfilter är fortfarande **AV**. Krypto hängde inte med. BTC står kring 60 500 USD, 16 % under MA200, med RSI(14) 13,7. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (`261121-PAYO` har nu fått en verifierad post-katalysatorkurs och flaggas för omprövning), L-5 (negativa påståenden avgränsas till de källor som genomsökts) och L-6 (spärrar citeras ur sin fil). L-1, L-2 och L-7–L-9 gäller inte scouten.

## Marknadsöversikt

`git pull` och `git fetch origin main` kördes 2026-11-24 cirka 05:48 UTC (06:48 CET). `origin/main` var då `e84633a`. Kurserna kommer ur `state/prices.json` (`generatedAt` 2026-11-24T05:19:11Z, `schemaVersion` 2026-08-02-prevclose, `okCount` 295 av 297, `wideAt` 2026-11-24T03:06:36Z), hämtade från Yahoo Finance chart API via GitHub Actions. **Pris-körningen gick i dag.** Nyhetsflödet (`state/news_feed.json`, `generatedAt` 2026-11-24T03:21:18Z) täcker **10 av 10 handelsdagar** (2026-11-11 – 2026-11-24, `missingDays` tomt).

| Symbol | Nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 7 237,17 | +4,73 % (mån) | 2026-11-23T21:42:33Z |
| `^IXIC` | 24 089,56 | +6,51 % (mån) | 2026-11-23T22:15:59Z |
| `BTC-USD` | 60 508,53 | −1,54 % mot den daterade punkten 2026-11-23 (61 453,35) | 2026-11-24T05:17:44Z |
| `ETH-USD` | 1 702,76 | −2,10 % mot den daterade punkten 2026-11-23 (1 739,30) | 2026-11-24T05:18:04Z |
| `SPY` (sleeve) | 722,29 | +4,71 % (mån) | 2026-11-23T21:00:00Z |

Kryptots rörelse är räknad mot daterade stängningar i `state/price_history.json` och inte mot `previousClose`, se åtgärdspunkt 3.

**Teknik** (räknad på råserien i `state/price_history.json`):
- `^GSPC` ligger **1,54 % under MA200** (7 350,08), med RSI(14) 40,9. **Regimfiltret för US-boken är AV.** `SPY` ligger 1,45 % under MA200 (732,91).
- `^IXIC` ligger 4,26 % under MA200 (25 162,71), med RSI 41,8.
- `BTC-USD` ligger 16,06 % under MA200 (72 081,66), med RSI 13,7. `ETH-USD` ligger 19,21 % under MA200 (2 107,73), med RSI 16,7.
- Måndagens ledare: `NVDA` 165,05 (+31,48 %, 2,77× 20-dagarsvolymen), `MU` 707,70 (+19,04 %), `DELL` 334,91 (+20,46 %), `MRVL` 144,74 (+18,37 %), `HPE` 48,02 (+17,38 %) och `TSM` 363,60 (+14,08 %). Samtliga marketTime är 2026-11-23T21:00–21:05Z. Av dem ligger bara `HPE` över MA200 (+12,10 %). `NVDA` ligger 18,79 % under, `MRVL` 23,38 % under och `DELL` 4,11 % under.

## Ekonomiska siffror & kalender

**Senaste utfall:**
- **S&P Global flash-PMI november (mån 2026-11-23):** Composite blev 54,6 mot 55,9 i oktober, den lägsta sedan juli. Services blev 54,7 mot väntade cirka 55,6 och 56,1 föregående månad. Manufacturing blev 54,5 mot 54,9. Prisindikatorerna ligger kvar över Feds mål (S&P Global; Newsquawk; FXStreet, 2026-11-23).
- **Jobless claims (tor 2026-11-19):** 203 000 mot väntade 197 000 (rapport-261123).
- **FOMC-protokollet (2026-11-18):** "nearly all" ledamöter väntar sig +25 bp i december (CNBC 2026-11-18).
- **KPI oktober (2026-11-10):** +0,4 % totalt och +0,3 % i kärnan m/m, båda över förväntan.

**Kommande:**
- **Tis 2026-11-24 (i dag):** Conference Boards konsumentförtroende. Före öppning rapporterar `ADI` och `MDT`. Efter stängning rapporterar `DELL`, `HPQ`, `ADSK`, `WDAY`, `BBY` och `CLSK`. Datumen är bekräftade i `state/earnings_calendar.json` (`isEstimate: false`, `generatedAt` 2026-11-24T03:04:40Z, `errors` tomt).
- **Ons 2026-11-25 – MEST MARKNADSRÖRANDE:** PCE för oktober (kärnan väntas cirka +0,27 % m/m), andra BNP-skattningen för Q3, varaktiga varor och jobless claims, plus Beige Book på kvällen. Det är sista inflationssiffran före FOMC 9/12. `DE` rapporterar före öppning. Förväntningarna är hämtade ur rapport-261123 och har inte kontrollerats på nytt i dag.
- **Tor 2026-11-26:** Thanksgiving, börsen stängd. **Fre 2026-11-27:** halvdag med stängning 13:00 ET.
- **Rapporter nästa 10 handelsdagar** (US-symboler i kalendern): 12-01 `MRVL`, 12-02 `CBRL`, `FIVE` och `ZS`, samt 12-03 `COO` och `S`. **L-5:** kalendern känner bara de symboler som `prices.yml` hämtar, så resten av det amerikanska universumet är **OKONTROLLERAT**. Samtliga datum är bevakningsposter enligt punkt 8, aldrig köpförslag.

## Aktuella händelser & katalysatorer

- **Nvidia återinsätter Jensen Huang som vd (2026-11-23).** Styrelsen tog tillbaka Huang elva dagar efter hans avgång. Aktien stängde 165,05 (+31,48 %) och lade till cirka 950 mdr USD i börsvärde (CNBC; StockTitan; Motley Fool, 2026-11-23). Council of Institutional Investors publicerade ett uttalande om återinsättningen (PR Newswire 2026-11-24T02:01Z, rubrik i `state/news_feed.json`). Den rapporterade SEC-utredningen är fortfarande ⚠️ **RYKTE – EJ BEKRÄFTAT (WSJ/Reuters, 2026-11-20)**. **Ingen kandidatpost:** `NVDA` ligger 18,79 % under MA200, och enligt `prompts/gemensam_korning.md` ("kurs ≤ MA200 blockerar nya aktiepositioner") är den inte handlingsbar.
- **HPE Q4 FY26 (2026-11-23, efter stängning):** intäkterna blev 14,5 mdr USD (+50 %) och justerad EPS 1,43, mot guidningen 1,20–1,30. Bolaget höjde FY27-guidningen och utökade återköpen med 5 mdr USD. Aktien föll ändå cirka 5–7 % i efterhandeln, till cirka 44,60–44,81 USD, eftersom Q1-guidningen låg under konsensus (HPE 8-K ex. 99.1, SEC 2026-11-23; Investing.com; Yahoo Finance; BigGo, 2026-11-23). Efterhandelskurserna kommer ur artiklar och är **inte** verifierade. → **Case 1.**
- **Zoom Q3 FY27 (2026-11-23, efter stängning):** intäkterna blev 1 290,6 MUSD (+4,9 %) och enterprise växte +8,6 %, den snabbaste takten på 13 kvartal. Justerad EPS blev 1,59 mot väntade 1,49. Bolaget höjde helårsguidningen till EPS 6,24–6,25 och inför en kvartalsutdelning på 0,25 USD. Aktien gick enligt en rubrik ned något i efterhandeln, men rörelsen är inte kvantifierad (Zoom via GlobeNewswire 2026-11-23; Investing.com 2026-11-23). → **Case 2.**
- **Clariant och CD&R bekräftar samtal om att köpa Ashland (`ASH`), 2026-11-23.** Clariant bekräftade samtalen efter en Bloomberg-artikel från 2026-11-22, men det finns inget avtal och ingen säkerhet om att något blir av. Enligt Bloomberg ligger den diskuterade värderingen nära fredagens stängning på 72,40 USD, och aktien steg cirka 1 % (Clariant via GlobeNewswire/MFN 2026-11-23T21:00Z; Bloomberg 2026-11-22; Seeking Alpha 2026-11-23). ⚠️ **RYKTE – EJ BEKRÄFTAT (Bloomberg, 2026-11-22)** vad gäller pris och avtal. Ingen budpremie finns att tala om, så det blir inget case och ingen kandidatpost. `ASH` läggs i watchlist för att få en verifierad kurs om ett avtal tecknas.
- **Linamar köper Genie från Terex (2026-11-23, MFN-rubrik 22:05Z).** `TEX` är säljare och saknar watchlist-rad. Innehållet är inte verifierat utöver rubriken, så ingen post skapas.
- **Krypto:** BTCS betalade tillbaka 43,8 MUSD i Aave-lån och minskade hävstången efter kursfallet (GlobeNewswire 2026-11-23T14:30Z, rubrik). Bitmine (`BMNR`) uppger att bolaget äger 6,09 miljoner ETH (PR Newswire 2026-11-24T01:22Z, rubrik). Ingen av händelserna är en positiv katalysator för `BTC-USD` eller `ETH-USD`, och kryptoaktierna `COIN` (+6,68 %) och `MSTR` (+8,48 %) följde bara med Nasdaq. **L-5:** ETF-flöden för 23–24/11 hittades inte i websöket 06:00 UTC, så de är OKONTROLLERADE.

## Uppföljning av tidigare case

Rapport-261123 och rapport-261122 hade inga case, så det senaste caset är från rapport-261121:
- `PAYO` (rapport-261121): KURS EJ VERIFIERAD → **7,23** (`state/prices.json`, marketTime 2026-11-23T21:00:00Z, Yahoo chart API). Det är den första verifierade kursen. Den ligger på en hel handelsdag strikt efter katalysatorn (OCC-beskedet 2026-11-20T22:02Z, efter stängning), men reaktionen blev bara +0,56 % på 1,02× volym. Tesen är **FÖRSVAGAD**, eftersom marknaden inte prisade in godkännandet. **L-4:** `261121-PAYO` avvisades 2026-11-23 på "kurs ej verifierbar", ett tillfälligt datavillkor, och posten är giltig t.o.m. 2026-11-30. Nu när kursen finns ska US-boken pröva posten på nytt mot samtliga grindar och logga det. Posten avvisades också på spärr (c), regimen, som fortfarande gäller.

**Kandidatkön (`state/scout_candidates.json`):** före dagens körning fanns 130 poster, varav 121 `rejected`, 9 `promoted` och 0 `new`. I dag läggs **2 nya poster** till: `261124-HPE` och `261124-ZM`. `261119-TGT` och `261120-WMT` vilar på regimspärren, som fortfarande gäller (`^GSPC` 1,54 % under MA200).

**US-boken (läses, ändras inte):** `CBOE` 354,67 (marketTime 2026-11-23T21:00:00Z) ligger 0,90 % över stoppen 351,50. Dagslägsta var 350,55, under stoppnivån, så nivån korsades intradag. Monitorn och US-boken äger den bedömningen. Sleeven är `SPY` 722,29.

## Dagens case
### Case 1: Hewlett Packard Enterprise (HPE / NYSE)
**Katalysator:** Q4-rapporten för FY26 släpptes 2026-11-23 efter stängning. Intäkterna blev 14,5 mdr USD (+50 % å/å) mot cirka 14,3 mdr väntat. Justerad EPS blev 1,43 mot guidningen 1,20–1,30. Cloud & AI växte +68,6 % till 11,3 mdr. FY27-guidningen är EPS 5,05–5,35 och fritt kassaflöde minst 5,5 mdr. Återköpsramen utökades med 5 mdr USD (HPE 8-K ex. 99.1, SEC 2026-11-23; TipRanks; Futu, 2026-11-23). Utfallet är bekräftat.
**Bull case:** HPE är en av få AI-infrastrukturnamn som ligger över MA200 efter novemberraset. Höjd FY27-guidning, AI-serverintäkter som enligt BigGo nästan fördubblas och en utökad återköpsram motsvarande cirka 8 % av börsvärdet (egen beräkning) ger både vinstmomentum och ett golv under aktien.
**Bear case:** Q1-guidningen låg under konsensus, och marginalen späds ut av AI-servermixen (Networking-marginalen gick till 22,1 % från 23,4 %). Aktien hade dessutom stigit 17 % samma dag, före rapporten. Efterhandeln föll cirka 5–7 %, vilket är ett klassiskt "sell the news". Regimfiltret är AV.
**Setup:** Stängningen 48,02 (`state/prices.json`, marketTime 2026-11-23T21:04:13Z, Yahoo chart API) är en **PRE-event-kurs**, så kandidatens `price` är `null`. Aktien ligger 12,10 % över MA200 (42,84), med RSI(14) 41,9. Volymen var 2,97× 20-dagarssnittet. 60-dagarstoppen 73,46 ligger 53 % över, så trenden är fortfarande nedåtriktad från höstens topp. Ingen P/E kan verifieras ur state; FY27-guidningens mittpunkt ger cirka 9× på efterhandelskursen enligt egen beräkning, som inte är verifierad. `prices.yml` fyller i post-event-kursen automatiskt.

### Case 2: Zoom Communications (ZM / NASDAQ)
**Katalysator:** Q3-rapporten för FY27 släpptes 2026-11-23 efter stängning. Intäkterna blev 1 290,6 MUSD (+4,9 %) och enterprise-intäkterna 805,4 MUSD (+8,6 %). Justerad EPS blev 1,59 mot väntade 1,49. Helårsguidningen höjdes till EPS 6,24–6,25. Bolaget inför sin **första kvartalsutdelning** på 0,25 USD och har återköpt 3,9 miljoner aktier under kvartalet (Zoom via GlobeNewswire 2026-11-23; Yahoo Finance 2026-11-23). Utfallet är bekräftat.
**Bull case:** Enterprise-segmentet växer snabbast på 13 kvartal, och den första utdelningen i kombination med återköp signalerar att bolaget går över till kapitalåterföring. Värderingen är låg för mjukvara (cirka 14× FY27-EPS på 86,03, egen beräkning).
**Bear case:** Den totala tillväxten är bara 4,9 %, och det fria kassaflödet sjönk till 558,1 från 614,3 MUSD. Aktien ligger 6,84 % under MA200, vilket enligt `prompts/gemensam_korning.md` blockerar nya aktiepositioner. Efterhandeln var svagt negativ, och regimfiltret är AV.
**Setup:** Stängningen 86,03 (`state/prices.json`, marketTime 2026-11-23T21:00:00Z, Yahoo chart API) är en **PRE-event-kurs**, så kandidatens `price` är `null`. MA200 är 92,34 och RSI(14) 43,1. Volymen var 2,14× 20-dagarssnittet. 60-dagarstoppen är 101,33. Caset kan inte bli ett köp förrän kursen ligger över MA200 **och** regimen är på. Det redovisas som bevakning av en bekräftad överraskning.

## Makro- & sektorfaktorer att bevaka

- **Regimen (viktigast):** `^GSPC` ligger 1,54 % under MA200 efter måndagens studs. Avståndet krympte från 5,96 % i går, men regimfiltret är fortfarande AV, så det blir inga nya aktiepositioner.
- **Inflation och Fed:** PMI-prisindikatorerna ligger över målet, KPI var starkare än väntat och Fed väntas höja i december. Onsdagens PCE avgör om studsen håller. Räntor, DXY och VIX går inte att verifiera ur state (åtgärdspunkt 2).
- **AI och halvledare:** Huangs återkomst tog bort ledarskapsrisken, men inte den rapporterade SEC-frågan. Nästan alla stora AI-namn ligger kvar under MA200, så studsen är en reparation och ingen trendvändning. I kväll blir Dells AI-serverorder veckans test.
- **Krypto:** BTC och ETH deltog inte i riskaptiten, och RSI under 15 är extremt översålt. Någon bekräftad katalysator finns inte.
- **Varför bara bevakning i dag:** båda casen är bekräftade överraskningar, men regimen är AV och ZM ligger dessutom under MA200. HPE:s efterhandel visar att marknaden säljer in i styrka. Ingen kandidat har ännu en kvalificerad post-event-kurs.

**Watchlist-hygien:** `config/watchlist_us.txt` har cirka 165 symboler, långt över riktmärket 25. Ingen rensning görs, eftersom skydden i `prompts/gemensam_korning.md` gäller: innehavet `CBOE`, sleeven och indexen, kandidater inom `expiresAt` (`PAYO`, `WMT`, `TGT`, `HPE`, `ZM`), rapportbolag inom 10 handelsdagar och beslut inom 20-dagarsfönstret. Att avgöra vilka rader som är fria kräver en genomgång av `decisions.json` mot 14 handelsdagar, och den hör hemma i US-rotationen. **Tillägg:** `ASH` (bekräftade uppköpssamtal).

### Åtgärdspunkter till Dren (L-3)

1. **`scout-crypto-no-weekend-price` – ÅTERKOMMANDE, men inte aktuell i dag.** Dagens kryptokurser är färska (marketTime 2026-11-24T05:1xZ). `state/price_history.json` saknar dock fortfarande en punkt för 2026-11-22 för `BTC-USD` och `ETH-USD`. **Omfång:** 2 av 2 mynt, varje söndag. **Förslag:** oförändrat, en helgcron i `prices.yml` för `*-USD`.
2. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas i `state/prices.json`. **Omfång:** samtliga makrovärden i rapporten.
3. **`crypto-previousclose-misdated` – ÅTERKOMMANDE.** `quotes["BTC-USD"].previousClose` är 61 161,91, men den daterade punkten för 2026-11-23 i `state/price_history.json` är 61 453,35. ETH visar samma mönster: 1 721,08 mot 1 739,30. **Omfång:** 2 av 2 mynt. **Ersättningskälla:** daterade stängningar i `price_history.json`, som tabellen ovan använder.
4. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** `feeds.globenewswire` och `feeds.globenewswire-earnings` ger fortfarande `"HTTP 403 – båda försöken (0.1 s)"`. **Omfång:** 2 av 6 flöden. Zooms rapport fanns därför bara via websök. **Ersättningskälla:** websök, prnewswire, mfn och SEC 8-K.
5. **`scout-cannot-fetch-press-release-body` – ÅTERKOMMANDE.** I dag nekades `www.sec.gov` av miljöns nätverkspolicy (ENOTFOUND), så HPE:s 8-K kunde bara läsas via sökutdrag. **Omfång:** samtliga pressmeddelandetexter i dagens rapport.
6. **`scheduled-actions-not-firing` – LÖST för i dag.** `prices.yml` körde i natt: `wideAt` är 2026-11-24T03:06Z och `generatedAt` 05:19Z.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
