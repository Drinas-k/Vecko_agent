# Daglig Scout: USA & Krypto
**Datum:** 2026-11-17
**Marknadsklimat:** Måndagen blev bred risk-off inför veckans binära händelser: `^GSPC` −1,92 % och `^IXIC` −2,49 %, ledda av halvledare och AI-namn inför Nvidias rapport i kväll och Anthropics notering. Nasdaq stängde 2,52 % under MA200, och S&P 500 har bara 1,01 % marginal kvar till sin MA200. BTC (64 994,69) och ETH (1 830,75) har fallit ~5 % sedan lördagens verifierade punkt och ligger 10–14 % under MA200. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (kandidatkön kontrollerad), L-5 (negativa påståenden avgränsade till genomsökta källor) och L-6 (krypto täcks enligt `config/fokus_scout.md`). L-1, L-2, L-7, L-8 och L-9 gäller inte scouten.

## Marknadsöversikt

`git pull` kördes 2026-11-17 05:48 UTC (06:48 CET). HEAD = `origin/main` = `e21344c`. Källan är `state/prices.json` med `generatedAt` 2026-11-17T03:48:09Z, `schemaVersion` 2026-08-02-prevclose, `tickerCount` 282 och `okCount` 279 (Yahoo Finance chart API via GitHub Actions), `wideAt` 2026-11-17T00:33:46Z. Aktiekurserna är måndagens stängning. Nyhetsflödet (`state/news_feed.json`) har `generatedAt` 2026-11-16T23:45:18Z och täcker **10 av 10 handelsdagar** (2026-11-02 – 2026-11-16, `missingDays` tomt).

| Symbol | Nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 7 416,59 | −1,92 % (7 561,67 → 7 416,59) | 2026-11-16T22:22:10Z |
| `^IXIC` | 24 509,76 | −2,49 % (25 136,27 → 24 509,76) | 2026-11-16T22:15:59Z |
| `BTC-USD` | 64 994,69 | −4,84 % mot daterad punkt 2026-11-14 (68 301,90); +0,31 % mot punkt 2026-11-16 (64 792,03) | 2026-11-17T03:46:50Z |
| `ETH-USD` | 1 830,75 | −5,14 % mot daterad punkt 2026-11-14 (1 929,88); +0,20 % mot punkt 2026-11-16 (1 827,12) | 2026-11-17T03:47:04Z |
| `SPY` (sleeve) | 739,95 | −1,91 % (754,37 → 739,95) | 2026-11-16T21:00:00Z |

Kryptorörelserna är räknade mot daterade punkter i `state/price_history.json`, inte mot `previousClose` (se åtgärdspunkt 1). Helgens fall syns nu i verifierade data: BTC −4,84 % och ETH −5,14 % sedan lördag 01:27 UTC.

**Teknik** (räknad på råserien i `state/price_history.json`, sista aktiepunkt 2026-11-16):
- `^GSPC` ligger **1,01 % över MA200** (7 342,68), så **regimfiltret för US-boken är fortfarande PÅ**. Marginalen krympte från 3,02 % i går. Index ligger 3,2 % under MA50 (7 661,42).
- `^IXIC` ligger **2,52 % under MA200** (25 142,61) och 6,8 % under MA50 (26 310,13).
- `BTC-USD` ligger **10,37 % under MA200** (72 514,98) och 18,4 % under MA50 (79 651,34). `ETH-USD` ligger **13,93 % under MA200** (2 127,07).

## Ekonomiska siffror & kalender

**Senaste utfall** (inga nya sedan rapport-261116):
- **PPI oktober (fre 2026-11-13):** +0,3 % m/m mot väntade +0,4 %, årstakt +6,5 % (se rapport-261114).
- **KPI oktober (2026-11-10):** total +0,4 % m/m och kärna +0,3 %, båda 0,1 pp över förväntan.
- **FOMC 27–28/10:** räntan oförändrad på 3,75–4,00 % (10–2).
- **Fed-ordföranden Kevin Warsh (mån 2026-11-16):** hans uttalanden ändrade inte prissättningen av en räntehöjning i december. Dollarindex nådde sin högsta nivå sedan april 2025 (Reuters via Devdiscourse, "Wall Street ends sharply lower on AI jitters ahead of Nvidia results, Anthropic IPO", 2026-11-16). DXY-nivån är inte verifierad, eftersom `DX-Y.NYB` saknas i `prices.json`.

**Kommande (nästa 1–5 handelsdagar):**
- **Tis 2026-11-17 (i dag) – VECKANS MEST MARKNADSRÖRANDE:** **Nvidia (`NVDA`) Q3 FY27 efter stängning.** Det är den första rapporten under interim-vd Colette Kress (se nedan). Konsensus enligt rapport-261116 är EPS 2,47 och intäkter 108,7 mdr USD. Samma dag kommer detaljhandelns försäljning för oktober (enligt rapport-261116, kl. 08:30 ET). `HD` och `DLB` rapporterar.
- **Ons 2026-11-18:** FOMC-protokollet kl. 14:00 ET och bostadsbyggandet. `TGT` och `LOW` rapporterar. `ANT` prissätts enligt uppgift (se nedan).
- **Tor 2026-11-19:** jobless claims. `WMT` och `ROST` rapporterar. `ANT` väntas börja handlas på Nasdaq.
- **Fre 2026-11-20:** University of Michigan, slutligt konsumentförtroende.

**Rapporter nästa 10 handelsdagar** ur `state/earnings_calendar.json` (`generatedAt` 2026-11-17T00:31:11Z, `errors` tomt), US-symboler:
- **11-17:** `NVDA`, `HD`, `DLB`. **11-18:** `TGT`, `LOW`. **11-19:** `WMT`, `ROST`.
- **11-23:** `HPE`. **11-24:** `CLSK` (gissat datum, `isEstimate: true`). **11-25:** `DE`. **12-01:** `MRVL`.

**L-5:** Kalendern omfattar bara de symboler som `prices.yml` hämtar. Resten av det amerikanska universumet är **OKONTROLLERAT**. Alla datum ovan är bevakningsposter enligt punkt 8, aldrig köpförslag.

## Aktuella händelser & katalysatorer

- **Måndagens nedgång (2026-11-16):** US-chipbolagen föll 5,3 %. Nvidia, Intel, Micron, CoreWeave och Nebius föll, och Alphabet, Amazon och Meta stängde klart lägre (Reuters via Devdiscourse 2026-11-16; Yahoo Finance live, "Nasdaq sinks over 2% as Nvidia leads AI trade lower, Anthropic IPO looms", 2026-11-16). Olja föll samma dag (Reuters-rubrik "Stocks end lower ahead of Nvidia earnings and Anthropic IPO; oil drops"), men nivån är inte verifierad. I `prices.json`: `NVDA` 156,14 (−4,12 %), `AMD` 504,28 (−5,58 %), `AVGO` 333,40 (−3,92 %), `COIN` 119,84 (−6,12 %) och `MSTR` 103,03 (−7,70 %), samtliga med marketTime 2026-11-16T21:00Z.
- **Nvidia, vd-bytet är BEKRÄFTAT (för att rätta tidigare formuleringar):** Jensen Huang lämnade posterna som vd, president och styrelseledamot med omedelbar verkan. Styrelsen godkände avgången 2026-11-11, och CFO Colette Kress är interim-vd (NVIDIA 8-K, SEC, avgång godkänd 2026-11-11; pressmeddelandet "NVIDIA Announces CEO Transition", 2026-11-12). Harvey C. Jones är utsedd till styrelseordförande, och sökandet efter en permanent vd pågår. Kandidaten `261112-NVDA` avvisades som "rykte WSJ 11/11, ingen bolagskommuniké", men en kommuniké fanns alltså. Avvisningen står sig ändå på kurs under MA200 och rapporten 17/11 (spärr 2e). Enligt uppgifter i medier överväger styrelsen inte att återinsätta Huang (Benzinga/Stocktwits via Yahoo Finance 2026-11-16, ⚠️ RYKTE – EJ BEKRÄFTAT).
- **Anthropics notering (`ANT`), villkoren är oförändrade:** 825 miljoner aktier till 70–78 USD, vilket ger ≈ 64,4 mdr USD (CNBC 2026-11-10; Yahoo Finance 2026-11-16). ⚠️ **RYKTE – EJ BEKRÄFTAT (CNBC, källor med insyn, 2026-11-10):** prissättning 18/11 och handel från 19/11. Aktien har ingen kurs och ingen MA200, så noteringen blockerar en ny position per definition. **Ingen kandidatpost.**
- **Biogen/Eisai (`BIIB`), femårsdata för Leqembi (lecanemab), 2026-11-16 23:00 UTC:** "New Five-Year Lecanemab Data from Clarity AD Study Long-Term Extension Presented at CTAD 2026" publicerades av Biogen (PR Newswire och mfn, båda i `state/news_feed.json`). Partnern BioArctic skriver i ett parallellt pressmeddelande att kontinuerlig behandling i fem år "visar ökande nytta över tid" (mfn 2026-11-16 23:05 UTC). Publiceringen skedde efter US-stängning. **Studiens siffror är inte verifierade:** pressmeddelandets brödtext gick inte att hämta från körmiljön, eftersom prnewswire.com inte är tillåten i nätverksinställningarna. → Case 1 och kandidatpost `261117-BIIB`.
- **Krypto:** ETF-utflödena från rapport-261116 (sju raka dagar till och med 13/11) har inte kunnat uppdateras för 16/11. Websök gav inga träffar daterade 2026-11-16, så flödet för 16/11 är **OKONTROLLERAT** (L-5). Ingen bekräftad regulatorisk händelse eller protokollhändelse hittades i websök.

## Uppföljning av tidigare case

Inga tidigare case att följa upp. Rapport-261116 hade inga case.

Kandidaten från rapport-261114, `APP`, är nu avgjord: 409,10 → 415,22 (+1,50 %, marketTime 2026-11-16T21:00:01Z, prices.json/Yahoo chart API). US-rotationen avvisade den 2026-11-16 (`us-veckorapport-261116`) med skälen grind 2 (volym 0,59x, EMA20 under EMA200) och grind 3 (katalysatorn ligger 8 handelsdagar bak). Det är omdömesspärrar, så L-4 gäller inte. Tesen är **INTAKT** som bevakning: `APP` steg mot en fallande marknad och ligger 2,40 % över MA200 (405,50).

**Kandidatkön (`state/scout_candidates.json`):** före körningen fanns 125 poster, varav 116 `rejected`, 9 `promoted` och **0 `new`**. **L-4:** inga poster inom `expiresAt` är avvisade på ett tillfälligt datavillkor som nu har fyllts. `261112-AMAT` och `261112-NVDA` (`price: null`) avvisades på omdöme eller obekräftad katalysator och har fått nya avgöranden i 261113-posterna. **En ny post i dag:** `261117-BIIB`.

**US-boken (läses, ändras inte):** `CBOE` stängde på 377,50 (+0,55 %, dagshögsta 379,76; marketTime 2026-11-16T21:00:00Z). Det är 1,32 % under målet 382,50 och 7,4 % över den flyttade stoppen 351,50. Sleeven är `SPY` 739,95.

## Dagens case
### Case 1: Biogen (BIIB / NASDAQ)
**Katalysator:** Femårsdata från förlängningsstudien till Clarity AD för Leqembi (lecanemab) presenterades på CTAD 2026, 2026-11-16 23:00 UTC (Biogen via PR Newswire och mfn; BioArctic mfn 23:05 UTC: "ökande nytta över tid"). Utfallet har inträffat och är bekräftat av bolagen. Studiens siffror är **EJ VERIFIERADE** av scouten, eftersom brödtexten inte gick att hämta (se åtgärdspunkt 4).
**Bull case:** Långtidsdata som visar ökande nytta över tid stärker argumentet för kontinuerlig underhållsbehandling. Det är den kommersiella frågan för Leqembi: hur länge patienterna står kvar på behandlingen avgör intäkten per patient. Kursen har en hel trendstack. Stängningen 251,65 ligger 22,4 % över MA200 (205,51) och 7,6 % över MA50 (233,96).
**Bear case:** Förlängningsstudier är öppna och saknar placebo efter 18 månader, så "ökande nytta" jämförs normalt med modellerad naturalförlopp och inte med en kontrollgrupp. Marknaden kan läsa det som inkrementellt, och säkerheten (ARIA) är okänd i dag. Biogen delar Leqembi med Eisai, som har huvudansvaret, så effekten på BIIB späds ut. Kursen har stått still i en månad (250–253 sedan 10/11) och volymen är låg: 838 744 aktier den 16/11 (`state/volume_history.json`). Det är en katalysator av typen "other" och inte en rapportöverraskning.
**Setup:** Senaste stängning 251,65 (marketTime 2026-11-16T21:00:00Z, prices.json/Yahoo chart API), −0,69 % på dagen, **före** katalysatorn. Den är en pre-event-kurs, så `price: null` i kandidatposten. `prices.yml` fyller i en kvalificerad post-event-kurs (förbörs eller reguljär 17/11). MA50 233,96, MA200 205,51 och 250-dagarsserie finns. Värderingstal är inte hämtade. Ansvarig bok (US) ska pröva samtliga fem grindar, däribland volymkravet > 1,5x. En ny köpbedömning görs först mot en post-event-kurs, och ett förbörskurs-köp blir i så fall en villkorad plan mot reguljär session.

Inga fler case i dag. Marknaden handlas på väntade händelser (NVDA i kväll, FOMC-protokollet, ANT, WMT). Enligt punkt 8 är de bevakningsposter och inte köpförslag. Måndagens få uppgångar (`CNC` +4,91 %, `PAYC` +2,37 %) saknar en daterad katalysator i `news_feed.json`. Skälen till avvaktan står under Makro nedan.

## Makro- & sektorfaktorer att bevaka

- **Räntor och dollar:** Enligt Reuters (2026-11-16) står förväntan om en höjning i december kvar efter Warshs kommentarer, och dollarindex nådde den högsta nivån sedan april 2025. Det är motvind för långdurationstillgångar och krypto. PPI-årstakten är 6,5 %. Räntenivåer och DXY är inte verifierade ur state (åtgärdspunkt 3).
- **Regimen:** S&P 500 har bara 1,01 % marginal till MA200. En svag reaktion på NVDA-rapporten kan slå av US-bokens regimfilter redan i morgon, och då får boken inte ta nya aktiepositioner. Nasdaq ligger redan 2,5 % under MA200. Det är veckans viktigaste systemrisk för US-boken.
- **AI och halvledare:** Sektorn föll 5,3 % på en dag. Den bär en dubbel osäkerhet: vd-krisen i Nvidia med en kongressutfrågning av Huang (CNN 2026-11-11) och frågor om exportkontroll, plus utbudet från Anthropics notering. `AMD`, `AVGO`, `CIEN` och `RKLB` ligger under eller nära MA200 efter måndagen. Inget AI-case görs före rapporten.
- **Krypto:** BTC och ETH ligger 10–14 % under MA200 efter ett verifierat helgfall på ~5 %. Hård dollar, ETF-utflöden och höjningsrisk pekar åt samma håll. `COIN` och `MSTR` föll 6–8 %. Inget kryptocase görs förrän flödena vänder eller en bekräftad händelse inträffar.
- **Defensiv rotation:** Måndagens få vinnare fanns i hälsovård och konsumentstaplar (`CNC`, `PG`, `KMB`, `UNH`). Det passar dagens enda case (`BIIB`), men rotationen är ingen katalysator i sig.
- **Varför marknaden är avvaktande:** Tre binära händelser kommer inom 72 timmar, och regimmarginalen är tunn. Det rationella läget är bevakning tills NVDA-rapporten har prisats in. Den rapporten avgör sannolikt både Nasdaqs riktning och US-bokens regimfilter.

**Watchlist-hygien:** `config/watchlist_us.txt` innehåller långt fler än 25 symboler, men ingen rensning görs. Följande skyddas enligt `prompts/gemensam_korning.md`: innehavet (`CBOE`), sleeven och indexen, kandidaterna inom `expiresAt` (`APP`, `NVDA`, `CSCO`, `AMAT`, `COST`, `CRWV`, nu även `BIIB`), rapportbolagen inom 10 handelsdagar, besluten från rotationen 2026-11-16 inom 20-dagarsfönstret och `ANT`. `BIIB` finns redan i listan. Inga tillägg.

### Åtgärdspunkter till Dren (L-3)

1. **`crypto-previousclose-misdated` – ÅTERKOMMANDE.** `quotes["BTC-USD"].previousClose` (65 305,06) och `quotes["ETH-USD"].previousClose` (1 835,50) motsvarar ingen daterad punkt i `state/price_history.json` (2026-11-16: 64 792,03 respektive 1 827,12). **Omfång:** 2 av 2 mynt. **Ersättningskälla:** `state/price_history.json`.
2. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** `feeds.globenewswire` och `feeds.globenewswire-earnings` ger fortfarande `"HTTP 403 – båda försöken (0.1 s)"`. **Omfång:** 2 av 6 flöden. **Ersättningskälla:** prnewswire, mfn, SEC 8-K och websök.
3. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas i `state/prices.json`. Dollarns flerårshögsta och oljefallet 16/11 kunde därför bara anges ur rubriker, utan nivå. **Omfång:** samtliga makrovärden.
4. **`scout-cannot-fetch-press-release-body` – NY.** WebFetch mot `www.prnewswire.com` och `lufkindailynews.com` (Reuters-syndikering) ger `getaddrinfo ENOTFOUND` från scoutens körmiljö, eftersom värdarna inte är tillåtna i sessionens nätverksinställningar. Därför kunde Leqembi-studiens siffror inte verifieras, bara rubriken, datumet och avsändaren ur `news_feed.json`. **Omfång:** varje case som bygger på ett pressmeddelande. **Förslag:** tillåt `prnewswire.com` (och gärna `mfn.se`) i miljöns nätverkspolicy.
5. **`weekend-crypto-price-unverifiable` – LÖST för denna helg.** Helgfallet syns nu i en verifierad punkt (2026-11-16 och 2026-11-17 03:46 UTC). Luckan lördag 01:28 UTC – måndag ~00:30 UTC finns kvar strukturellt.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
