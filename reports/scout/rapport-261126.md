# Daglig Scout: USA & Krypto
**Datum:** 2026-11-26
**Marknadsklimat:** US-börsen är stängd i dag för Thanksgiving, så marknadsdata är onsdagens stängning. Onsdagen gav en het PCE-siffra (kärna 3,3 % mot 3,2 % väntat), en kraftig BNP-uppjustering och ett AI-ras där Nasdaq som mest låg 4,6 % ned. Marknaden återhämtade det mesta: `^GSPC` −0,25 %, `^IXIC` −0,62 %, Dow +0,33 %. Bredden var positiv (cirka tre fjärdedelar av S&P 500 steg), men regimfiltret för US-boken är fortsatt **AV**. Krypto studsar svagt från översålt läge (BTC cirka 60 600) mitt i fortsatta ETF-utflöden. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (`261125-DELL`, `-WDAY` och `-ADSK` har nu en kurs efter katalysatorn och flaggas för omprövning), L-5 (negativa påståenden avgränsas till genomsökta källor) och L-6 (spärrar citeras ur sin fil). L-1, L-2 och L-7–L-9 gäller inte scouten.

## Marknadsöversikt

`git pull` och `git fetch origin main` kördes 2026-11-26 cirka 05:48 UTC (06:48 CET). `origin/main` var då `96527b6`. Kurserna kommer ur `state/prices.json` (`generatedAt` 2026-11-26T03:31:56Z, `schemaVersion` 2026-08-02-prevclose, `okCount` 296 av 298, `wideAt` 2026-11-26T00:44:15Z), hämtade från Yahoo Finance chart API via GitHub Actions. Nyhetsflödet (`state/news_feed.json`, `generatedAt` 2026-11-26T01:00:14Z) täcker **10 av 10 handelsdagar** (2026-11-12 – 2026-11-26, `missingDays` tomt).

| Symbol | Nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 7 182,78 | −0,25 % (ons) | 2026-11-25T21:32:06Z |
| `^IXIC` | 23 585,80 | −0,62 % (ons) | 2026-11-25T22:15:59Z |
| `BTC-USD` | 60 588,46 | +1,56 % mot den daterade punkten 2026-11-25 (59 654,57) | 2026-11-26T03:30:35Z |
| `ETH-USD` | 1 691,78 | +0,76 % mot den daterade punkten 2026-11-25 (1 679,07) | 2026-11-26T03:30:50Z |
| `SPY` (sleeve) | 716,70 | −0,29 % (ons) | 2026-11-25T21:00:00Z |

Indexens stängningar stämmer med pressens (Yahoo Finance, GSM Global News och StockTitan, 2026-11-25). Kryptots rörelse är räknad mot daterade stängningar i `state/price_history.json` (se åtgärdspunkt 1).

**Teknik** (räknad på råserien i `state/price_history.json`):
- `^GSPC` ligger **2,31 % under MA200** (7 352,46), med RSI(14) 39,7. **Regimfiltret för US-boken är AV.** `SPY` ligger 2,25 % under MA200 (733,16).
- `^IXIC` ligger 6,29 % under MA200 (25 167,61), med RSI 38,6.
- `BTC-USD` ligger 15,76 % under MA200 (71 919,41), med RSI 27,6. `ETH-USD` ligger 19,49 % under MA200 (2 101,26), med RSI 29,0.
- **Onsdagens största rörelser** bland 159 US-symboler med stängning 2026-11-25 i `state/price_history.json` (L-5: resten av marknaden är **OKONTROLLERAD**). Uppåt: `HPQ` +11,49 % (2,72× volym, efter rapport), `ASTS` +10,25 %, `ADI` +6,44 % (rekyl efter −17 %) och `DE` +4,44 % (1,79×, efter rapport). Nedåt: `SNDK` −5,57 %, `ORCL` −5,13 %, `MU` −4,53 %, `NVDA` −3,91 % (149,30), `AMAT` −3,89 % och `ADSK` −3,49 % (1,61×, efter rapport).

## Ekonomiska siffror & kalender

**Senaste utfall (ons 2026-11-25):**
- **PCE oktober – MEST MARKNADSRÖRANDE:** totalen +3,8 % å/å (3,6 % i september), i linje med konsensus. Kärnan blev **+3,3 % å/å mot väntade 3,2 %**, den högsta sedan november 2023 (CNBC 2026-11-25; Quartz 2026-11-25; Invezz 2026-11-25). Marknaden prisar enligt rapporteringen en höjning med +25 bp på FOMC 8–9/12 till cirka 98 %, och enligt Reuters/CME FedWatch (via Invezz) ytterligare en i januari 2027.
- **BNP Q3, andra skattningen:** **4,3 %** i årstakt mot 3,4 % i första skattningen och cirka 3,5 % väntat (Reuters-enkät), driven av investeringar, konsumtion och offentliga utgifter (Seeking Alpha 2026-11-25; StockTitan 2026-11-25).
- **Jobless claims (veckan t.o.m. 2026-11-21):** 189 000 mot cirka 200 000 väntat och 203 000 veckan innan (två sekundärkällor, ej verifierat mot Labor Department).
- **Varaktiga varor och Beige Book:** varaktiga varor +0,2 % mot +1,1 % väntat; Beige Book visade att 8 av 12 distrikt växte "slight to moderate" och att insatskostnaderna steg snabbare än försäljningspriserna. **Båda bygger på en enda nyhetsbrevskälla och är OKONTROLLERADE** (sidan gick inte att hämta, se åtgärdspunkt 4).
- Rapporteringen nämner dessutom ett amerikanskt förslag om nya tullar mot 14 handelspartner (Yahoo Finance 2026-11-25). Detaljerna är inte verifierade.

**Kommande:**
- **Tor 2026-11-26 (i dag):** Thanksgiving, NYSE/Nasdaq stängda. **Fre 2026-11-27:** halvdag med stängning 13:00 ET och tunn likviditet. Inga större makroutfall väntas före måndag.
- **Vecka 49:** ISM Manufacturing (mån 2026-12-01) och november-NFP (fre 2026-12-04, datum enligt BLS normala schema, ej verifierat i dag). NFP blir den sista stora siffran före FOMC 9/12.
- **Rapporter nästa 10 handelsdagar** (US-symboler i `state/earnings_calendar.json`, `generatedAt` 2026-11-26T00:42:18Z, `errors` tomt, alla `isEstimate: false`): 12-01 `MRVL`, 12-02 `CBRL` och `FIVE`, 12-03 `COO` och `S`, 12-09 `AVGO`, 12-10 `CIEN` och `COST`. **L-5:** kalendern känner bara de symboler som `prices.yml` hämtar, så resten av US-universumet är **OKONTROLLERAT**. Samtliga datum är bevakningsposter enligt punkt 8, aldrig köpförslag.

## Aktuella händelser & katalysatorer

- **HP Inc Q4 FY26 (2026-11-24 efter stängning) – reaktion 2026-11-25:** justerad EPS blev 0,83 mot bolagets egen guidning 0,69–0,79, och intäkterna 16,0 mdr (+9,3 %). FY27-guidningen är EPS 3,15–3,45 och ett fritt kassaflöde på 2,9–3,1 mdr. Bolaget kallar själv guidningen "prudent". Tullåterbetalningar bidrog med 0,15 USD per aktie mot 0,08 i guidningen. Aktien steg **+11,49 % till 31,15** (Benzinga 2026-11-25; Proactive Investors 2026-11-25; Quantisnow 2026-11-25). I går bedömde scouten överraskningen som för liten för en kandidatpost, och marknaden sa emot. → **Case 1.**
- **Deere Q4 FY26 (2026-11-25 före öppning):** nettovinsten blev 1,051 mdr (3,89 USD per aktie mot 3,93 året innan), intäkterna föll 2 % till 12,12 mdr och försäljningen av stora jordbruksmaskiner tappade 15 %. FY27-guidningen för nettovinst är 4,5–5,25 mdr mot väntade 5,91 mdr, inklusive en pensionskostnad på 250–400 MUSD utan kassaflödespåverkan. Bolaget ser stora jordbruksmaskiner i USA/Kanada +5–15 % under FY27 (StockAnalysis, Kalkine, Yahoo Finance 2026-11-25). Aktien vände från cirka −6 % före öppning till **+4,44 % (641,02)**. → **Case 2.**
- **AI-/halvledarraset på onsdagen:** `NVDA` föll 3,91 % (som mest mer än −9 %). Enligt Yahoo Finance hade S&P Global satt Nvidias kreditbetyg under bevakning för en möjlig sänkning med ett steg, men den uppgiften kommer från en enda källa och är inte verifierad. Ambarella föll 19,8 % på sin prognos. Nvidia ligger enligt CNBC (via sökutdrag) cirka 27 % ned i november (Yahoo Finance; GSM Global News; mlq.ai, 2026-11-25).
- **Autodesk efter rapporten:** −3,49 % till 246,79 på 1,61× volym, mer än efterhandelns −4,5 % som rapporterades i går. Dell (+0,60 %) och Workday (+0,68 %) stängde i stället svagt uppåt, trots att efterhandeln för Workday rapporterades till −7 %. Gårdagens efterhandelskurser höll alltså inte.
- **Krypto:** spot-bitcoin-ETF:erna hade nettoutflöden på cirka 453 MUSD den 25/11 (IBIT 329,7 MUSD), sjunde dagen i rad, och november summerar till omkring 5 mdr USD i utflöden (Coinotag 2026-11-25; BusinessToday 2026-11-25). Fear & Greed-index ligger på 13 (Extreme Fear) (Cryptonews). Rekylen i går drevs enligt Motley Fool av likviderade korta positioner (Motley Fool 2026-11-25). **Ingen positiv fundamental katalysator för `BTC-USD` eller `ETH-USD` har hittats** i de genomsökta källorna.
- **Brus i flödet:** `state/news_feed.json` (sedan 2026-11-25 00:00 UTC) innehåller främst Nasdaq-noteringsvarningar, en omvänd split (Vivakor) och advokatreklam (Medline). Ingen post bygger ett case.

## Uppföljning av tidigare case

- `DELL` (rapport-261125): 295,28 (pre-event) → **297,06** (+0,60 %, `state/prices.json`, marketTime 2026-11-25T21:03:52Z, Yahoo chart API), på 2,91× volym. Aktien ligger 15,37 % under MA200 (350,99). Tesen är **FÖRSVAGAD**: rekordrapporten gav ingen omvärdering, och aktien ligger kvar långt under MA200.
- `WDAY` (rapport-261125): 179,23 (pre-event) → **180,44** (+0,68 %, marketTime 2026-11-25T21:00:02Z), på 1,82× volym. Aktien ligger 15,18 % över MA200 (156,66). Tesen är **INTAKT**, eftersom det befarade efterhandelsfallet inte höll.
- `ADSK` (rapport-261125): 255,70 (pre-event) → **246,79** (−3,49 %, marketTime 2026-11-25T21:00:02Z), på 1,61× volym. Aktien ligger 5,40 % över MA200 (234,13). Tesen är **FÖRSVAGAD**: marknaden sålde trots beat och höjd guidning.

**L-4:** `261125-DELL`, `261125-WDAY` och `261125-ADSK` avvisades 2026-11-25 på "kurs ej verifierbar – stängningen 24/11 är pre-event", ett tillfälligt datavillkor. Nu finns en reguljär stängning en hel handelsdag efter katalysatorn (24/11 efter stängning → 25/11). Posterna gäller t.o.m. 2026-12-03 och ska prövas på nytt av US-boken mot samtliga grindar och loggas. `261125-BBY` har ingen verifierad rapporttid, men stängningen 25/11 (102,58, +2,97 %) ligger med säkerhet efter rapporten 24/11, så även den kan prövas om. Alla faller fortfarande på spärr (c), regimen, och DELL dessutom på "Saknad MA200 eller kurs ≤ MA200 blockerar nya aktiepositioner" i `prompts/gemensam_korning.md`. `261124-HPE` (40,82, under MA200) och `261124-ZM` (88,56, under MA200) gäller t.o.m. 2026-12-02 och spärras på samma sätt.

**Kandidatkön (`state/scout_candidates.json`):** före dagens körning fanns 136 poster, varav 127 `rejected`, 9 `promoted` och 0 `new`. I dag läggs **2 nya poster** till: `261126-HPQ` (price 31,15, marketTime 2026-11-25T21:00:03Z, en reguljär stängning dagen efter AMC-rapporten) och `261126-DE` (price 641,02, marketTime 2026-11-25T21:00:02Z, reguljär stängning samma dag som en rapport före öppning, alltså efter katalysatorn).

**US-boken (läses, ändras inte):** boken ligger 100 % i sleeven `SPY` 716,70, och ingen pending-plan är öppen (`state/portfolj_us.md`, senast uppdaterad 2026-11-25T13:30:00Z).

## Dagens case
### Case 1: HP Inc (HPQ / NYSE)
**Katalysator:** Q4-rapporten för FY26 släpptes 2026-11-24 efter stängning. Justerad EPS blev 0,83 mot bolagets egen guidning 0,69–0,79, och intäkterna 16,0 mdr (+9,3 % å/å). FY27-guidningen är EPS 3,15–3,45 och ett fritt kassaflöde på 2,9–3,1 mdr. Utdelningen höjs till 0,31 USD per kvartal (rapport-261125; Benzinga, Proactive Investors och Quantisnow, 2026-11-25). Utfallet är bekräftat. Marknadens reaktion den 25/11 blev +11,49 % på 2,72× 20-dagarsvolymen.
**Bull case:** Högre snittpriser och en premiummix väger upp fallande PC-volymer, och FY27-guidningen antyder ungefär oförändrade intäkter med ett stabilt kassaflöde. Barclays höjde riktkursen (Proactive Investors 2026-11-25). Aktien ligger tydligt över MA200 och är ett av få teknikrelaterade namn med positiv trend när AI-hårdvaran säljs.
**Bear case:** Tullåterbetalningar stod för 0,15 USD av justerad EPS mot 0,08 i guidningen, alltså en stor del av beatet (Quantisnow 2026-11-25). Guidningen beskrivs som "prudent" i ljuset av kostnads- och efterfrågetryck, och enligt en källa ligger konsensus för riktkursen cirka 17 % under nuvarande kurs. Rörelsen kan delvis vara en täckning av korta positioner i en oviss rotation. Regimfiltret är AV.
**Setup:** Stängningen är 31,15 (`state/prices.json`, marketTime 2026-11-25T21:00:03Z, Yahoo chart API), med dagshögsta 32,05 och dagslägsta 29,70. Aktien ligger 22,8 % över MA200 (25,36) och strax över MA50 (30,70), med RSI(14) 57,4. 60-dagarstoppen är 35,48 och snittomsättningen cirka 447 MUSD/dag (20 dagar, egen beräkning ur `state/volume_history.json`). Ingen P/E kan verifieras ur state. Kandidaten är prissatt men **kan inte köpas medan regimen är AV**.

### Case 2: Deere & Company (DE / NYSE)
**Katalysator:** Q4-rapporten för FY26 släpptes 2026-11-25 före öppning. Nettovinsten blev 1,051 mdr (3,89 USD per aktie mot 3,93 året innan), och intäkterna föll 2 % till 12,12 mdr. FY27-guidningen för nettovinst är 4,5–5,25 mdr, under analytikernas 5,91 mdr, och inkluderar en pensionskostnad på 250–400 MUSD utan kassaflödespåverkan. Samtidigt väntas stora jordbruksmaskiner i USA/Kanada öka 5–15 % under FY27 (StockAnalysis, Kalkine och Yahoo Finance, 2026-11-25). Utfallet är bekräftat.
**Bull case:** Aktien vände från cirka −6 % före öppning (cirka 595,50) till +4,44 % på 1,79× volym. Marknaden verkar läsa guidningen som botten i jordbrukscykeln, med en återhämtning i stora maskiner under FY27. Dessutom handlas aktien över MA200 i en marknad där pengar roterar till cykliska industrinamn (Dow över 50 000).
**Bear case:** Guidningen ligger tydligt under konsensus, försäljningen av stora maskiner föll 15 % i kvartalet och aktien ligger under MA50 (660,99) och 9,7 % under 60-dagarstoppen 709,48. Vändningen skedde på en enda dag före en helg med tunn handel. Regimfiltret är AV, och nya tullförslag är en risk för jordbruksexporten.
**Setup:** Stängningen är 641,02 (`state/prices.json`, marketTime 2026-11-25T21:00:02Z, Yahoo chart API), med dagshögsta 646,89 och dagslägsta 580,51. Aktien ligger 4,1 % över MA200 (615,53), med RSI(14) 47,0. Snittomsättningen är cirka 841 MUSD/dag (egen beräkning). Ingen P/E kan verifieras ur state. Kandidaten är prissatt men **kan inte köpas medan regimen är AV**, och tekniken är blandad (under MA50).

## Makro- & sektorfaktorer att bevaka

- **Regimen (viktigast):** `^GSPC` ligger 2,31 % under MA200, ett större avstånd än i går (2,04 %). Regimfiltret är AV, så det blir inga nya aktiepositioner oavsett rapporternas styrka.
- **Inflation och Fed:** kärn-PCE på 3,3 % och BNP på 4,3 % cementerar en höjning i december, och diskussionen flyttar till januari. Högre realräntor är motvind för långdurationstillväxt och krypto. Räntor, DXY, VIX och olja kan inte verifieras ur state (åtgärdspunkt 2).
- **Sektorrotation:** AI-hårdvara och minnen säljs (NVDA, MU, AMAT, SNDK, ORCL), medan bredden är positiv: Dow och Russell 2000 steg. Kapitalet söker sig till cykliska industrinamn och värdebolag. Det gynnar Deere-typen av case, men regimfiltret mäter S&P 500, som tyngs av tekniksektorn.
- **Krypto:** ETF-utflödena fortsätter, sentimentet är extrem rädsla och kursen ligger långt under MA200. Rekylen är driven av likviderade korta positioner, inte av fundamenta, så det finns inget case.
- **Varför bara bevakning i dag:** båda casen är bekräftade och prissatta efter katalysatorn, men regimen är AV. Fredagens halvdag med tunn likviditet gör dessutom rörelser svårtolkade.

**Watchlist-hygien:** `config/watchlist_us.txt` har långt fler symboler än riktmärket 25. Ingen rensning görs, eftersom skydden i `prompts/gemensam_korning.md` gäller: sleeven och indexen, kandidater inom `expiresAt` (`PAYO`, `WMT`, `HPE`, `ZM`, `DELL`, `WDAY`, `ADSK`, `BBY`, `HPQ`, `DE`), rapportbolag inom 10 handelsdagar och beslut inom 20-dagarsfönstret. Den genomgången hör hemma i US-rotationen. Inga tillägg behövs: dagens kandidater har redan en kurs i `state/prices.json`, och alla US-bolag i rapportkalendern har en rad.

### Åtgärdspunkter till Dren (L-3)

1. **`crypto-previousclose-misdated` – ÅTERKOMMANDE.** `quotes["BTC-USD"].previousClose` är 59 747,77, medan den daterade punkten för 2026-11-25 i `state/price_history.json` är 59 654,57. För ETH är motsvarande värden 1 677,69 och 1 679,07. Avvikelsen är mindre än i går (0,16 % mot 1,9 %) men består. **Omfång:** 2 av 2 mynt. **Ersättningskälla:** daterade stängningar i `price_history.json`.
2. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas fortfarande i `state/prices.json`. **Omfång:** samtliga makrovärden i rapporten. Halvledarraset kan bara anges ur artiklar.
3. **`news-feed-globenewswire-http-403` – kan stängas.** `feeds.globenewswire` och `feeds.globenewswire-earnings` svarar i dag `"20 poster"` (`state/news_feed.json`, `generatedAt` 2026-11-26T01:00:14Z), och `perSource` visar 38 respektive 30 poster i fönstret. Åtgärdspunkten var ÅTERKOMMANDE i går men verkar nu självläkt. Bekräfta i nästa retro.
4. **`scout-cannot-fetch-press-release-body` – ÅTERKOMMANDE.** I dag nekades `theweekendspread.substack.com` av miljöns nätverkspolicy (ENOTFOUND), så samtliga rapportsiffror kommer ur sökutdrag. Därför är varaktiga varor, Beige Book och jobless claims inte verifierade mot primärkälla. **Omfång:** samtliga pressmeddelande- och makrotexter i dagens rapport.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
