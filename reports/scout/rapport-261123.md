# Daglig Scout: USA & Krypto
**Datum:** 2026-11-23
**Marknadsklimat:** Måndag i Thanksgiving-veckan och ännu före öppning i New York. Läget är fredagens: `^GSPC` 6 910,39 ligger 5,96 % under MA200, och US-bokens regimfilter är **AV**. Bitcoin föll i helgen till cirka 55 000 USD med likvidationer på 1,8–2,3 mdr USD och studsade sedan tillbaka över 60 000 (Yahoo Finance/Motley Fool 2026-11-22). Inga helgkurser är verifierade ur state. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (kandidatkön kontrollerad), L-5 (negativa påståenden avgränsade till genomsökta källor, och `ZM`, `ADI`, `ADSK`, `WDAY` och `MDT` tillagda i watchlist) och L-6 (krypto täcks enligt `config/fokus_scout.md`). L-1, L-2, L-7, L-8 och L-9 gäller inte scouten.

## Marknadsöversikt

`git pull` och `git fetch origin main` kördes 2026-11-23 cirka 05:48 UTC (06:48 CET), och `origin/main` var `bbc4477`. Källan är `state/prices.json` med `generatedAt` 2026-11-21T02:13:44Z, `schemaVersion` 2026-08-02-prevclose och `okCount` 326 av 331 (Yahoo Finance chart API via GitHub Actions). **Ingen pris-körning har gått i dag:** måndagens 05:09 UTC-cron i `prices.yml` startade inte. GitHub Actions senaste `prices.yml`-körning är nr 941 (2026-11-21T02:09Z, success), kontrollerad 05:50 UTC. Nyhetsflödet (`state/news_feed.json`, `generatedAt` 2026-11-20T22:15:20Z) täcker **10 av 10 handelsdagar** (2026-11-09 – 2026-11-20, `missingDays` tomt).

| Symbol | Nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 6 910,39 | −3,70 % (fredag) | 2026-11-20T21:35:54Z |
| `^IXIC` | 22 617,73 | −5,28 % (fredag) | 2026-11-20T22:15:59Z |
| `BTC-USD` | 58 959,74 | ingen ny punkt sedan 2026-11-21 | 2026-11-21T02:11:46Z |
| `ETH-USD` | 1 624,60 | ingen ny punkt sedan 2026-11-21 | 2026-11-21T02:12:20Z |
| `SPY` (sleeve) | 689,81 | −3,64 % (fredag) | 2026-11-20T21:00:04Z |

**Krypto: KURS EJ VERIFIERAD för i dag.** Den senaste verifierade kursen är cirka 51,5 timmar gammal. Enligt nyhetskällor föll BTC till cirka 55 000–55 300 USD på lördagen, vilket är lägsta sedan september 2024. Den var 60 121 USD kl. 19 New York-tid på lördagen och 60 785 USD söndag kväll. ETH var cirka 1 683 respektive 1 720 USD (Yahoo Finance/Motley Fool 2026-11-22, CoinGecko-data; ceoeconomy.com 2026-11-22). Nivåerna kommer ur artiklar och används **inte** som verifierade kurser. Ingen beslutsbar nivå sätts ur dem (åtgärdspunkt 1).

**Teknik** (räknad på råserien i `state/price_history.json`; ingen ny punkt sedan 2026-11-20):
- `^GSPC` ligger **5,96 % under MA200** (7 348,55), RSI(14) 29,2. **Regimfiltret för US-boken är AV** inför dagens LÄGE A. `SPY` ligger 5,86 % under MA200 (732,76).
- `^IXIC` ligger 10,09 % under MA200 (25 157,42).
- `BTC-USD` låg 18,36 % under MA200 (72 219,77) och `ETH-USD` 23,14 % under MA200 (2 113,60) vid senaste verifierade punkt. Även helgens återhämtning till cirka 60 800 USD ligger långt under MA200.

## Ekonomiska siffror & kalender

**Senaste utfall:**
- **Jobless claims (tor 2026-11-19):** 203 000 mot väntade 197 000, med ett fyraveckorssnitt på 197 750 (veckokalendrar, websök 2026-11-23).
- **FOMC-protokollet (2026-11-18):** "nearly all" ledamöter väntar sig +25 bp i december (CNBC 2026-11-18).
- **KPI oktober (2026-11-10):** +0,4 % totalt och +0,3 % i kärnan m/m, båda över förväntan.
- **Michigan, slutligt november (2026-11-20):** utfallet är fortfarande **EJ VERIFIERAT**.

**Kommande** (Newsquawk "Week in Focus", Yardeni och Sensei.news, veckan 23–27/11, websök 2026-11-23):
- **Mån 2026-11-23:** flash-PMI. `HPE` (bekräftat datum i `state/earnings_calendar.json`) och `ZM` rapporterar efter stängning. Zoom väntas redovisa EPS cirka 1,49 USD på cirka 1,28 mdr i intäkter.
- **Tis 2026-11-24:** `ADI` och `MDT` rapporterar före öppning. Efter stängning rapporterar `DELL` (EPS cirka 6,00–6,62 USD på cirka 49,3 mdr), `HPQ`, `ADSK` och `WDAY` (Opening Bell Daily 2026-11-21; Kiplinger). `CLSK` rapporterar enligt kalendern. Conference Boards konsumentförtroende publiceras.
- **Ons 2026-11-25 – MEST MARKNADSRÖRANDE:** allt kommer på en förmiddag. Det gäller PCE för oktober (kärnan väntas +0,27 % m/m och 3,2 % å/å, headline +0,3 % m/m), andra BNP-skattningen för Q3 (preliminärt 3,4 %), varaktiga varor, jobless claims (en dag tidigare än vanligt) och på kvällen Beige Book. Det är sista inflationssiffran före FOMC 9/12. `DE` rapporterar före öppning.
- **Tor 2026-11-26:** Thanksgiving, börsen stängd. **Fre 2026-11-27:** halvdag med stängning 13:00 ET.
- Konsensus kommer ur förhandsvisningar, och källorna skiljer sig åt. En källa anger kärn-PCE till 2,5 %, vilket inte går ihop med de övriga. Behandla siffrorna som riktmärken.

**Rapporter nästa 10 handelsdagar** ur `state/earnings_calendar.json` (`generatedAt` 2026-11-21T02:11:10Z, `errors` tomt), US-symboler: 11-23 `HPE`, 11-24 `CLSK`, 11-25 `DE`, 12-01 `MRVL`, 12-02 `CBRL`, `FIVE` och `ZS`, samt 12-03 `COO` och `S`. **L-5:** kalendern känner bara symbolerna som `prices.yml` hämtar. Veckans rapportkalendrar (Opening Bell Daily, Kiplinger, StockTitan) visade att `ZM`, `ADI`, `ADSK`, `WDAY` och `MDT` rapporterar i veckan utan att ha en watchlist-rad. De läggs därför till i dag. `DELL`, `HPQ` och `BBY` lades till i går men har ännu ingen kurs, eftersom ingen pris-körning gått. Resten av det amerikanska universumet är **OKONTROLLERAT**. Samtliga datum är bevakningsposter enligt punkt 8, aldrig köpförslag.

## Aktuella händelser & katalysatorer

- **Kryptoras och studs i helgen, 2026-11-21/22.** BTC föll till cirka 55 000 USD, lägsta sedan september 2024, och tvångslikvidationerna landade på cirka 1,8 mdr USD. En annan källa anger 2,3 mdr i terminsförluster på lördagen, huvudsakligen långa positioner. Därefter återtog BTC 60 000 USD. Under veckan föll BTC från 65 804 till 60 880 USD (−7,5 %) och ETH från 1 837 till 1 711 USD (−6,8 %). Bitcoin-ETF:erna hade utflöden på 1,12 mdr USD måndag–torsdag (Yahoo Finance/Motley Fool 2026-11-22; ceoeconomy.com 2026-11-22; finin2min 2026-11-22). Detta är en negativ katalysator och ger ingen kandidatpost.
- **SEC-utredningen av Nvidia.** WSJ och Reuters uppger att SEC har inlett en civilrättslig utredning om huruvida bolagets information vilseledde investerare. Kaliforniens justitieminister Rob Bonta säger att hans kontor granskar delar av affären, och utredningen följer på Jensen Huangs avgång (InvestmentNews; PYMNTS; Crypto Briefing, 2026-11). Varken SEC eller Nvidia har bekräftat utredningen. ⚠️ **RYKTE – EJ BEKRÄFTAT (WSJ/Reuters, 2026-11-20).** Inga nya uppgifter dagtecknade 22–23/11 hittades i websöket 05:55 UTC. `NVDA` stängde 125,53 (−14,01 %, marketTime 2026-11-20T21:00:01Z).
- **Brookfield köper PGP Glass från Blackstone för cirka 1,7 mdr USD (2026-11-23).** Affären väntas slutföras under Q1 2027 och kräver myndighetsgodkännanden (Seeking Alpha; StockTitan 2026-11-23). Brookfield är köpare, och PGP är onoterat, så det finns ingen handlingsbar målrabatt för ett US-namn. Ingen kandidatpost.
- **Andra affärer under veckan:** Palo Alto Networks köper Applied Compute för 4,5 mdr USD i aktier (2026-11-18), och MasTec köper Murphy för 1,25 mdr USD (2026-11-20). MasTec-aktien föll 10,76 % den dagen (Quartz; FinChannel, 2026-11). Ingen av affärerna är bevakad eller köpbar för målbolagets del.
- **Nyhetsflödet:** inga poster efter 2026-11-20T22:15Z, eftersom news-actionen kör vardagar från 05:17 UTC och dagens körning ännu inte landat. Inga nya bekräftade positiva katalysatorer hittades för bevakade US- eller kryptonamn. Påståendet gäller websöken 05:50–05:58 UTC och flödet ovan, och resten är OKONTROLLERAT (L-5).

## Uppföljning av tidigare case

Rapport-261122 hade inga case, så det finns inga tidigare case att följa upp därifrån. Det senaste caset är från rapport-261121:
- `PAYO` (rapport-261121): KURS EJ VERIFIERAD → KURS EJ VERIFIERAD. `state/prices.json` saknar fortfarande `PAYO`, eftersom ingen pris-körning gått sedan symbolen lades till. Tesen om OCC:s villkorade godkännande är **INTAKT** men omätt. Kandidaten `261121-PAYO` är `new` och ska avgöras av US-boken vid dagens LÄGE A, kl. 15:00 CET. Den är giltig t.o.m. 2026-11-30.

**Kandidatkön (`state/scout_candidates.json`):** 130 poster, varav 120 `rejected`, 9 `promoted` och **1 `new`** (`261121-PAYO`). **L-4:** inga nya post-event-kurser har tillkommit, eftersom prices.json är oförändrad sedan 2026-11-21. Därför har ingen vilande avvisning fått ny data. `261119-TGT` och `261120-WMT` vilar på regimspärren, som fortfarande gäller. **Ingen ny post i dag**, eftersom inget nytt case finns.

**US-boken (läses, ändras inte):** `CBOE` 357,71 (marketTime 2026-11-20T21:00:04Z) ligger 1,77 % över stoppen 351,50. Sleeven är `SPY` 689,81.

## Dagens case

Inga case i dag. Inga nya verifierade kurser finns sedan fredag, och dagens pris-körning har uteblivit. Helgens katalysatorer är negativa (kryptolikvidationerna, Nvidia) eller väntade händelser (HPE, Zoom, Dell, HP, ADI, PCE), och väntade rapporter är enligt punkt 8 bevakningsposter, aldrig köpförslag. Regimfiltret är dessutom AV. Skälen till avvaktan står under Makro.

## Makro- & sektorfaktorer att bevaka

- **Regimen (viktigast):** `^GSPC` ligger 5,96 % under MA200. Dagens US-rotation (LÄGE A) startar med regimfiltret AV, alltså inga nya aktiepositioner oavsett case.
- **Inflation och Fed:** onsdagens samlade datablock med PCE, BNP, varaktiga varor och claims är veckans största risk. KPI var starkare än väntat, och Fed väntas höja i december. Det är motvind för tillväxtaktier och krypto. Räntor, DXY och VIX är inte verifierade ur state (åtgärdspunkt 2).
- **AI och halvledare:** Nvidias regulatoriska fråga hänger kvar. Dells AI-serverorder (tis) och ADI:s industriefterfrågan (tis) blir veckans test. Samtliga stora halvledarnamn i watchlisten ligger under MA200 per 2026-11-20.
- **Krypto:** helgens likvidationsvåg har rensat bort hävstång, men ETF-utflödena fortsätter, och BTC/ETH ligger långt under MA200. En studs efter tvångsförsäljning är ingen bekräftad katalysator.
- **Varför marknaden är avvaktande:** Index är i korrektion med RSI under 30. AI-ledaren är föremål för en utredning, Fed väntas strama åt och veckan förkortas av helgdagen med samlad datarisk på onsdagen. Översålda lägen kan ge studsar, men regimfiltret är byggt för att inte köpa dem.

**Watchlist-hygien:** `config/watchlist_us.txt` har långt fler än 25 symboler, men ingen rensning görs. Skyddade är innehavet (`CBOE`), sleeven och indexen, kandidaterna inom `expiresAt` (`PAYO`, `WMT`, `TGT` med flera), rapportbolag inom 10 handelsdagar och beslut inom 20-dagarsfönstret. **Tillägg:** `ZM`, `ADI`, `ADSK`, `WDAY` och `MDT` (L-5, rapportbolag utan rad).

### Åtgärdspunkter till Dren (L-3)

1. **`scout-crypto-no-weekend-price` – ÅTERKOMMANDE** (rapport-261122 och 261123). `state/prices.json` → `quotes["BTC-USD"].marketTime` och `quotes["ETH-USD"].marketTime` är 2026-11-21T02:1xZ, alltså cirka 51,5 timmar gamla vid måndagens körning. **Omfång:** 2 av 2 mynt, hela helgen plus måndag morgon. **Ersättningskälla:** endast nyhetsartiklar, som inte är verifierade. Rapporten skriver därför KURS EJ VERIFIERAD. **Förslag:** en helgcron i `prices.yml` för `*-USD`.
2. **`scheduled-actions-not-firing` – ÅTERKOMMANDE.** `prices.yml`-cronen `9 5 * * 1-5` startade inte 2026-11-23. Senaste körning är nr 941, 2026-11-21T02:09Z, kontrollerat 05:50 UTC. **Omfång:** samtliga 331 symboler är 2,5 dygn gamla vid scoutens körning, och de 8 nya rapportbolagen (`DELL`, `HPQ`, `BBY` plus dagens fem) saknar kurs. Dygnsgrinden `needsDailyRun` bör ta igen det vid 06:09-körningen. Kontrollera att den gör det före US-rotationen kl. 15:00 CET.
3. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas i `state/prices.json`. **Omfång:** samtliga makrovärden i rapporten.
4. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** `feeds.globenewswire` och `feeds.globenewswire-earnings` ger fortfarande `"HTTP 403 – båda försöken (0.0 s)"`. **Omfång:** 2 av 6 flöden. **Ersättningskälla:** websök, prnewswire, mfn och SEC 8-K.
5. **`crypto-previousclose-misdated` – ÅTERKOMMANDE** (oförändrat, eftersom filen inte skrivits om). `previousClose` för BTC-USD och ETH-USD motsvarar ingen daterad punkt i `state/price_history.json`. **Omfång:** 2 av 2 mynt.
6. **`scout-cannot-fetch-press-release-body` – ÅTERKOMMANDE.** I dag nekades även `www.fool.com` av miljöns nätverkspolicy (ENOTFOUND), så helgens kryptoartikel kunde bara läsas som sökutdrag. **Omfång:** samtliga artikelbrödtexter i dagens rapport.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
