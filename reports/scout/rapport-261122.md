# Daglig Scout: USA & Krypto
**Datum:** 2026-11-22
**Marknadsklimat:** Det är söndag och de amerikanska börserna är stängda. `state/prices.json` har inte uppdaterats sedan lördag 02:13 UTC, eftersom pris-actionen bara kör vardagar. Läget är därför fredagens: `^GSPC` 6 910,39 ligger 5,96 % under MA200 och US-bokens regimfilter är **AV**. Under helgen har Reuters uppgift om att SEC utreder Nvidias redovisning fått stöd av WSJ, och inför Thanksgiving-veckan väntar PCE, BNP och rapporter från Dell och HP. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (kandidatkön kontrollerad), L-5 (negativa påståenden avgränsade till genomsökta källor, och `DELL`, `HPQ` och `BBY` tillagda i watchlist) och L-6 (krypto täcks enligt `config/fokus_scout.md`). L-1, L-2, L-7, L-8 och L-9 gäller inte scouten.

## Marknadsöversikt

`git pull` och `git fetch origin main` kördes 2026-11-22 cirka 05:48 UTC (06:48 CET), och `origin/main` var `b66bc1f`. Källan är `state/prices.json` med `generatedAt` 2026-11-21T02:13:44Z, `schemaVersion` 2026-08-02-prevclose och `okCount` 326 av 331 (Yahoo Finance chart API via GitHub Actions). Filen är samma som i rapport-261121. Nyhetsflödet (`state/news_feed.json`, `generatedAt` 2026-11-20T22:15:20Z) täcker **10 av 10 handelsdagar** (2026-11-09 – 2026-11-20, `missingDays` tomt).

| Symbol | Nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 6 910,39 | −3,70 % (fredag) | 2026-11-20T21:35:54Z |
| `^IXIC` | 22 617,73 | −5,28 % (fredag) | 2026-11-20T22:15:59Z |
| `BTC-USD` | 58 959,74 | ingen ny punkt sedan gårdagens rapport | 2026-11-21T02:11:46Z |
| `ETH-USD` | 1 624,60 | ingen ny punkt sedan gårdagens rapport | 2026-11-21T02:12:20Z |
| `SPY` (sleeve) | 689,81 | −3,64 % (fredag) | 2026-11-20T21:00:04Z |

**Krypto: KURS EJ VERIFIERAD för i dag.** Kryptomarknaden handlas dygnet runt, men den senaste verifierade kursen är cirka 27,5 timmar gammal. Reservkällan (query1.finance.yahoo.com) och api.coinbase.com nekades av miljöns proxy (HTTP 403). Websök gav ingen daterad söndagskurs (L-5 gäller sökningen 2026-11-22 cirka 05:50 UTC). Nivåerna ovan är alltså lördagens nattkurser. De ska inte läsas som dagens nivå (åtgärdspunkt 1).

**Teknik** (räknad på råserien i `state/price_history.json`; ingen ny aktiepunkt sedan 2026-11-20):
- `^GSPC` ligger **5,96 % under MA200** (7 348,55), RSI(14) 29,2. **Regimfiltret för US-boken är AV** inför måndagens LÄGE A. `SPY` ligger 5,86 % under MA200 (732,76).
- `^IXIC` ligger 10,09 % under MA200 (25 157,42).
- `BTC-USD` ligger 18,36 % under MA200 (72 219,77) och `ETH-USD` 23,14 % under MA200 (2 113,60), räknat på lördagens punkt.

## Ekonomiska siffror & kalender

**Senaste utfall:**
- **Michigan, slutligt konsumentförtroende november (fre 2026-11-20):** utfallet är fortfarande **EJ VERIFIERAT**, eftersom websök inte gav någon daterad träff. Den preliminära siffran var 51,0 (StockAnalysis 2026-11).
- **Jobless claims (tor 2026-11-19):** 203 000 mot väntade 197 000 (se rapport-261120).
- **FOMC-protokollet (2026-11-18):** "nearly all" ledamöter väntar sig +25 bp i december (CNBC 2026-11-18).
- **KPI oktober (2026-11-10):** +0,4 % totalt och +0,3 % i kärnan m/m, båda över förväntan.

**Kommande** (veckoförhandsvisningar från CMC Markets, Schaeffer's 2026-11-19 och Futu, websök 2026-11-22):
- **Mån 2026-11-23:** flash-PMI, och `HPE` rapporterar efter stängning. HPE har bekräftat datum i `state/earnings_calendar.json`. Aktien stängde 40,91 i fredags, 4,2 % under MA200.
- **Tis 2026-11-24:** Conference Boards konsumentförtroende. `CLSK` rapporterar (kalendern). `DELL` (16:30 ET) och `HPQ` (17:00 ET) rapporterar efter stängning, enligt förhandsvisningarna. Dell väntas redovisa EPS cirka 6,48–6,61 USD, och fokus ligger på AI-serverorderboken.
- **Ons 2026-11-25 – MEST MARKNADSRÖRANDE:** PCE för oktober plus personlig inkomst och konsumtion. Headline väntas +0,3 % m/m (från +0,5 %), och kärnan väntas stiga från 3,1 till 3,2 % å/å. Andra BNP-skattningen för Q3 väntas 3,5 % (preliminärt 3,4 %). Det är den sista stora inflationssiffran före FOMC 9/12. `DE` rapporterar samma dag (kalendern).
- **Tor 2026-11-26:** Thanksgiving, börsen stängd. **Fre 2026-11-27:** halvdag med stängning 13:00 ET.
- Uppgifterna om konsensus kommer ur förhandsvisningar och inte ur en officiell kalender, och källorna skiljer sig åt i detaljer. Behandla dem som riktmärken.

**Rapporter nästa 10 handelsdagar** ur `state/earnings_calendar.json` (`generatedAt` 2026-11-21T02:11:10Z, `errors` tomt): 11-23 `HPE`, 11-24 `CLSK`, 11-25 `DE`, 12-01 `MRVL`, 12-02 `CBRL`, `FIVE` och `ZS`, samt 12-03 `COO` och `S`. **L-5:** kalendern känner bara symbolerna som `prices.yml` hämtar. Websök visade att `DELL`, `HPQ` och `BBY` (Best Buy, datum EJ VERIFIERAT) rapporterar i veckan men saknade watchlist-rad. De läggs därför till i dag. Resten av det amerikanska universumet är **OKONTROLLERAT**. Samtliga datum är bevakningsposter enligt punkt 8, aldrig köpförslag.

## Aktuella händelser & katalysatorer

- **SEC-utredningen av Nvidia har bekräftats av fler medier, 2026-11-20/21.** Reuters rapporterade, med hänvisning till två personer som informerats, att SEC granskar Nvidias redovisning. WSJ rapporterar att utredningen även gäller om bolagets information vilseledde investerare. SEC avböjde att kommentera, och Nvidia har inte svarat (Yahoo Finance; The Korea Times/Reuters 2026-11-21; Motley Fool 2026-11-21). Q3-releasen 17/11 angav redan att 10-Q kommer "in the coming weeks" och att en oberoende styrelsekommitté utreder (Nvidia 8-K 2026-11-17, sec.gov). ⚠️ **RYKTE – EJ BEKRÄFTAT (Reuters/WSJ, 2026-11-20).** Katalysatorn är negativ och ger ingen kandidatpost. `NVDA` stängde 125,53 (−14,01 %, marketTime 2026-11-20T21:00:01Z).
- **ETF-utflöden ur krypto, veckan 16–20/11:** amerikanska spot-ETF:er för bitcoin hade nettoutflöden på cirka 1,25 mdr USD, och tillsammans med ether-fonderna var utflödet cirka 1,47 mdr. IBIT hade rekordutflödet 541 MUSD på en dag den 19/11 (coinotag; crypto.news; FinanceFeeds, 2026-11). Källorna anger olika belopp för månaden hittills (3,47–3,59 mdr USD), så siffrorna är preliminära.
- **Veckosummering:** Dow föll mer än 8 % på veckan, och Nasdaq har förlorat hela årets uppgång (BigGo Finance 2026-11-21). Det stämmer med prices.json, där `^IXIC` gick −5,28 % i fredags och ligger 10,09 % under MA200.
- **Nyhetsflödet:** inga poster efter 2026-11-20T22:15Z, eftersom news-actionen kör vardagar. Den senaste relevanta rubriken är Payoneers OCC-besked (22:02 UTC, se uppföljningen). Inga nya bekräftade positiva katalysatorer hittades för bevakade US- eller kryptonamn i helgens websök. Det påståendet gäller bara sökningen 05:50 UTC och flödet ovan, och resten är OKONTROLLERAT (L-5).

## Uppföljning av tidigare case

- `PAYO` (rapport-261121): KURS EJ VERIFIERAD → KURS EJ VERIFIERAD. Symbolen lades i watchlist 2026-11-21, men ingen pris-körning har gått sedan dess (helg), så `state/prices.json` saknar fortfarande `PAYO`. Ingen ny information om villkoren i OCC-godkännandet har hittats. Tesen är **INTAKT** men omätt. Kandidaten `261121-PAYO` är `new` och ska avgöras av US-boken vid måndagens LÄGE A. Den är giltig t.o.m. 2026-11-30.

**Kandidatkön (`state/scout_candidates.json`):** 130 poster, varav 120 `rejected`, 9 `promoted` och **1 `new`** (`261121-PAYO`). **L-4:** inga nya post-event-kurser har tillkommit sedan gårdagen, eftersom prices.json är oförändrad. Därför har ingen vilande avvisning fått ny data. `261119-TGT` och `261120-WMT` vilar på regimspärren, som fortfarande gäller. **Ingen ny post i dag**, eftersom inget nytt case finns.

**US-boken (läses, ändras inte):** `CBOE` 357,71 (marketTime 2026-11-20T21:00:04Z) ligger 1,77 % över stoppen 351,50. Sleeven är `SPY` 689,81.

## Dagens case

Inga case i dag. Det är söndag och marknaderna är stängda. Det finns inga nya verifierade kurser, och nyhetsflödet har inte uppdaterats sedan fredag kväll. De katalysatorer som tillkommit under helgen är negativa (Nvidia) eller väntade händelser (Dell, HP, HPE, PCE). Väntade rapporter är enligt punkt 8 bevakningsposter och aldrig köpförslag. Skälen till avvaktan står under Makro.

## Makro- & sektorfaktorer att bevaka

- **Regimen (viktigast):** `^GSPC` ligger 5,96 % under MA200. Måndagens US-rotation (LÄGE A) startar med regimfiltret AV, alltså inga nya aktiepositioner oavsett case.
- **Inflation och Fed:** PCE onsdag är veckans viktigaste siffra. KPI var starkare än väntat, Fed väntas höja i december och 10-åringen låg nyligen över 5 %. Det är motvind för tillväxtaktier och krypto. Räntor, DXY och VIX är inte verifierade ur state (åtgärdspunkt 2).
- **AI och halvledare:** Nvidias redovisningsfråga och det försenade 10-Q är en öppen risk för hela sektorn. Dells AI-serverorderbok på tisdag blir nästa test av efterfrågan. Samtliga stora halvledarnamn i watchlisten ligger under MA200.
- **Krypto:** ETF-utflödena fortsätter. BTC och ETH låg 18–23 % under MA200 vid senaste verifierade punkt. Dagens nivå är ej verifierad.
- **Varför marknaden är avvaktande:** Index är i korrektion och VIX låg i fredags på ett 52-veckorshögsta (35,89 enligt nyhetskällor, ej ur state). Dessutom har AI-ledaren en regulatorisk utredning mot sig, Fed väntas strama åt och veckan förkortas av helgdagen med samlad datarisk på onsdagen. Översålda lägen kan ge studsar, men regimfiltret är byggt för att inte köpa dem.

**Watchlist-hygien:** `config/watchlist_us.txt` har långt fler än 25 symboler, men ingen rensning görs. Skyddade är innehavet (`CBOE`), sleeven och indexen, kandidaterna inom `expiresAt` (`PAYO`, `WMT`, `TGT`, `NVDA` med flera), rapportbolag inom 10 handelsdagar och beslut inom 20-dagarsfönstret. **Tillägg:** `DELL`, `HPQ` och `BBY` (L-5, rapportbolag utan rad).

### Åtgärdspunkter till Dren (L-3)

1. **`scout-crypto-no-weekend-price` – ny.** `state/prices.json` uppdateras inte på helger (`prices.yml` kör bara vardagar), så `quotes["BTC-USD"].marketTime` och `quotes["ETH-USD"].marketTime` är cirka 27,5 timmar gamla vid söndagens körning. Reservkällorna nekas av proxyn: `query1.finance.yahoo.com` och `api.coinbase.com` ger HTTP 403. **Omfång:** 2 av 2 mynt, varje söndag (och lördag eftermiddag). **Ersättningskälla:** ingen verifierad, och rapporten skriver KURS EJ VERIFIERAD. **Förslag:** en helgcron i `prices.yml` som bara hämtar `*-USD`-symboler, eller att Yahoo tillåts i miljöns nätverkspolicy.
2. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas i `state/prices.json`. **Omfång:** samtliga makrovärden i rapporten.
3. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** `feeds.globenewswire` och `feeds.globenewswire-earnings` ger fortfarande `"HTTP 403 – båda försöken (0.0 s)"`. **Omfång:** 2 av 6 flöden. **Ersättningskälla:** websök, prnewswire, mfn och SEC 8-K.
4. **`crypto-previousclose-misdated` – ÅTERKOMMANDE** (oförändrat sedan rapport-261121, eftersom filen inte skrivits om). `previousClose` för BTC-USD och ETH-USD motsvarar ingen daterad punkt i `state/price_history.json`. **Omfång:** 2 av 2 mynt.
5. **`scout-cannot-fetch-press-release-body` – ÅTERKOMMANDE.** `stocktitan.net` resolvar inte i miljön, och `prnewswire.com` gav 403 tidigare. **Omfång:** i dag kunde rapportkalendern för veckan och Payoneers brödtext inte läsas.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
