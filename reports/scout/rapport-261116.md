# Daglig Scout: USA & Krypto
**Datum:** 2026-11-16
**Marknadsklimat:** Måndag morgon (06:48 CET) har ingen amerikansk session handlats sedan fredagens risk-off, då `^GSPC` föll −0,40 % och `^IXIC` −0,91 % och stängde exakt på MA200. Krypto ligger fortsatt under MA200. Senaste verifierade BTC-kurs är 68 301,90, och sökträffar från helgen talar om ytterligare fall mot 62 000–64 500 (EJ VERIFIERAT). Den binära veckan börjar nu: Nvidias rapport och detaljhandeln 17/11, FOMC-protokollet 18/11 och Anthropics (`ANT`) väntade notering 19/11. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (kandidatkön kontrollerad), L-5 (negativa påståenden avgränsas till genomsökta källor) och L-6 (krypto täcks enligt `config/fokus_scout.md`, "[X] Krypto – större mynt"). L-2 är uppfylld, eftersom `APP` har rad och kurs. L-1, L-7, L-8 och L-9 gäller inte scouten.

## Marknadsöversikt

`git pull` kördes 2026-11-16 05:48 UTC (06:48 CET). HEAD = `origin/main` = `f6bed1e`. Källan är `state/prices.json` med `generatedAt` 2026-11-14T01:28:52Z, `schemaVersion` 2026-08-02-prevclose, `tickerCount` 321 och `okCount` 316 (Yahoo Finance chart API via GitHub Actions). **Filen är oförändrad sedan lördag.** Måndagens dygnskörning (`9 5 * * 1-5`) hade inte startat vid läsningen. Senaste `prices.yml`-körningen i Actions är run 911 (2026-11-14 01:25 UTC, success). Aktiekurserna är fredagens stängningar, vilket är de senaste som finns. Kryptokurserna är ~52 timmar gamla. Nyhetsflödet (`state/news_feed.json`) har `generatedAt` 2026-11-14T01:29:15Z och täcker **10 av 10 handelsdagar** (2026-11-02 – 2026-11-14, `missingDays` tomt).

| Symbol | Senaste verifierade nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 7 561,67 | −0,40 % fredag (7 592,40 → 7 561,67) | 2026-11-13T21:43:19Z |
| `^IXIC` | 25 136,27 | −0,91 % fredag (25 366,09 → 25 136,27) | 2026-11-13T22:15:59Z |
| `BTC-USD` | 68 301,90 | +0,16 % mot daterad punkt 2026-11-13 (68 194,22). **Helgrörelsen är EJ VERIFIERAD.** | 2026-11-14T01:27:12Z |
| `ETH-USD` | 1 929,88 | +0,37 % mot daterad punkt 2026-11-13 (1 922,76). **Helgrörelsen är EJ VERIFIERAD.** | 2026-11-14T01:27:35Z |
| `SPY` (sleeve) | 754,37 | −0,36 % fredag (757,12 → 754,37) | 2026-11-13T21:00:00Z |

**Krypto i helgen: KURS EJ VERIFIERAD.** Reservkällorna nås inte från körmiljön. Yahoo (`query1.finance.yahoo.com/v8/finance/chart/BTC-USD`), CoinGecko, Coinbase och Kraken gav alla `CONNECT tunnel failed, response 403` 2026-11-16 05:5x UTC (åtgärdspunkt 4). Sökträffarna nämner BTC "toward $64,500" och "a three-month low just above $62,000" (Stablecoin Insider, CoinCentral; odaterad intradag, helgen 14–15/11). Det är sökträffar och inte kurser, så de används inte för nivåer. Riktningen pekar dock på att BTC handlats **ytterligare 5–9 % under** den verifierade nivån.

**Teknik** (räknad på råserien i `state/price_history.json`, sista aktiepunkt 2026-11-13, oförändrad sedan i går):
- `^GSPC` ligger **3,02 % över MA200** (7 340,29), så **regimfiltret för US-boken är PÅ** inför dagens veckorotation (LÄGE A). Index ligger under MA50 (7 667,46).
- `^IXIC` står **0,004 % under MA200** (25 137,37) och under MA50 (26 350,07).
- `BTC-USD` ligger **5,91 % under MA200** (72 592,23) på senaste verifierade punkt. `ETH-USD` ligger **9,46 % under MA200** (2 131,60).

## Ekonomiska siffror & kalender

**Senaste utfall** (inga nya sedan rapport-261115):
- **PPI oktober (fre 2026-11-13):** +0,3 % m/m mot väntade +0,4 %, årstakt +6,5 % (se rapport-261114).
- **KPI oktober (2026-11-10):** total +0,4 % m/m och kärna +0,3 %, båda 0,1 pp över förväntan.
- **FOMC 27–28/10:** räntan oförändrad på 3,75–4,00 %, med röstsiffrorna 10–2 (två reservationer för en höjning, se rapport-261115).

**Kommande (nästa 1–5 handelsdagar):**
- **Tis 2026-11-17 – VECKANS MEST MARKNADSRÖRANDE:** **Nvidia (`NVDA`) Q3 FY27 efter stängning.** Konsensus i `state/earnings_calendar.json` är EPS 2,47 och intäkter 108,7 mdr USD. Samma dag kommer **detaljhandelns försäljning för oktober** kl. 08:30 ET, och `HD` rapporterar.
- **Ons 2026-11-18:** **FOMC-protokollet** kl. 14:00 ET och bostadsbyggandet kl. 08:30 ET. `TGT` och `LOW` rapporterar. `ANT`-prissättningen väntas samma dag (se nedan).
- **Tor 2026-11-19:** jobless claims. `WMT` och `ROST` rapporterar. `ANT` väntas börja handlas på Nasdaq.
- **Fre 2026-11-20:** University of Michigan, slutligt konsumentförtroende för november.

**Rapporter nästa 10 handelsdagar** ur `state/earnings_calendar.json` (`generatedAt` 2026-11-14T01:26:58Z, `errors` tomt), US-symboler:
- **11-17:** `NVDA`, `HD`. **11-18:** `TGT`, `LOW`. **11-19:** `WMT`, `ROST`.
- **11-23:** `HPE`. **11-24:** `CLSK` (gissat datum, `isEstimate: true`). **11-25:** `DE`.

**L-5:** Kalendern ser bara de 321 symboler som `prices.yml` hämtar, så resten av det amerikanska universumet är **OKONTROLLERAT**. Samtliga datum är bevakningsposter enligt punkt 8, aldrig köpförslag.

## Aktuella händelser & katalysatorer

- **Anthropics börsnotering (`ANT`), villkoren är oförändrade.** 825 miljoner A-aktier (801,4 mn nya och 23,6 mn från befintliga ägare) erbjuds i intervallet **70–78 USD** på Nasdaq under tickern `ANT`. Det ger ≈ 64 mdr USD i toppen av intervallet, plus en separat placering på ~26 mdr USD till sju chip- och molnleverantörer (UPI 2026-11-10; CNBC "Anthropic sets IPO price range of $70 to $78, looks to start trading Nov. 19, sources say", 2026-11-10). ⚠️ **RYKTE – EJ BEKRÄFTAT (CNBC, källor med insyn, 2026-11-10):** prissättning 18/11 och handel från 19/11. ⚠️ **RYKTE – EJ BEKRÄFTAT (Bloomberg, via sökträff, odaterad):** orderboken ska vara ~6× övertecknad. Eftersom aktien inte handlas finns ingen kurs och ingen MA200, så noteringen blockerar en ny position per definition (`prompts/gemensam_korning.md`: "Saknad MA200 eller kurs ≤ MA200 blockerar nya aktiepositioner"). **Ingen kandidatpost.** `ANT` står redan i `config/watchlist_us.txt`.
- **Krypto, spot-ETF:erna:** Fredagen 13/11 gav nettoutflöden på −185,4 mn USD. Det var den **sjunde raka handelsdagen** med utflöden, ≈ −1,91 mdr USD över sviten (Farside via Stablecoin Insider). Utflödena under november t.o.m. 13/11 anges till 2,1 mdr USD (Decrypt via Bitcoinworld) respektive 2,35 mdr USD (CoinCentral). Källorna skiljer sig, så beloppen ska tas med försiktighet. Spot-ETF:ernas nettotillgångar ligger på 94,9 mdr USD, under 100 mdr för första gången sedan oktober. Ingen bekräftad regulatorisk eller protokollkatalysator har hittats i websök, och övriga källor är **OKONTROLLERADE**.
- **Nvidia (`NVDA`) inför rapporten:** Fredagens stängning var 162,85 (−2,01 %; prices.json, marketTime 2026-11-13T21:00:01Z), 20,25 % under MA200. Ingen ny bekräftad bolagshändelse har hittats sedan 8-K:n den 12/11 (i websök; övriga källor **OKONTROLLERADE**).
- **Helgen:** Inga nya bekräftade bolagshändelser i det amerikanska universumet har hittats i websök. `news_feed.json` har inte uppdaterats sedan 2026-11-14T01:29Z, så helgflödet är **OKONTROLLERAT** (L-5).

## Uppföljning av tidigare case

- **`APP` (rapport-261114): 409,10 → 409,10** (±0,00 %, ingen ny session; marketTime 2026-11-13T21:00:01Z, prices.json/Yahoo chart API). **Tes INTAKT:** kursen ligger 0,81 % över MA200 (405,79) och långt över MA50 (302,13). Kandidaten `261114-APP` har status `new` med `expiresAt` 2026-11-20, och **dagens US-rotation (LÄGE A, 15:00 CET) är ansvarig för avgörandet**. Den tunna MA200-marginalen och volymkriteriet är de grindar boken behöver pröva. Anthropics notering 19/11 är ett sektorspecifikt utbudstryck att väga in.

**Kandidatkön (`state/scout_candidates.json`):** 125 poster, varav 115 `rejected`, 9 `promoted` och **1 `new`** (`261114-APP`, inom `expiresAt`). **L-4:** Ingen post som avvisats på ett tillfälligt datavillkor väntar på omprövning, eftersom ingen ny kurs har tillkommit sedan lördag. **Inga nya poster i dag:** ingen ny bekräftad och handlingsbar katalysator finns, och `ANT` saknar kurs och MA200.

**US-boken (läses, ändras inte):** `CBOE` stängde fredagen på 375,42 (+1,77 %, dagshögsta 378,17; marketTime 2026-11-13T21:00:00Z). Det är 1,85 % under målet 382,50 och 8,8 % över stoppen 345,00. Sleeven är `SPY`.

## Dagens case

**Inga nya case i dag.** Ingen session har handlats sedan rapport-261114, och ingen ny bekräftad katalysator har hittats. Kurser och nyhetsflöde står still sedan lördag ~01:29 UTC, och måndagens prisuppdatering hade inte kört vid läsningen. Veckans stora händelser (NVDA 17/11, FOMC-protokollet 18/11, `ANT` 19/11, WMT 19/11) är väntade event och därmed bevakningsposter enligt punkt 8, inte köpförslag. Kryptot har enligt helgens sökträffar fallit vidare, men utan verifierad kurs och utan katalysator. Ett översålt läge räcker inte. Skälen står under Makro nedan.

## Makro- & sektorfaktorer att bevaka

- **Räntor och inflation:** PPI-årstakten på 6,5 % och en 10-årsränta på ~5 % (sökträffar; `^TNX` saknas i `prices.json`) ger fortsatt motvind för långdurationstillgångar och krypto. FOMC-protokollet 18/11 avgör hur hökaktig marknaden läser Fed inför december. Fed-rädsla anges också som en drivkraft bakom ETF-utflödena.
- **Regimen:** `^GSPC` ligger +3,02 % över MA200, så regimen är PÅ. Nasdaq står exakt på MA200, och NVDA-rapporten 17/11 avgör sannolikt vilken sida den hamnar på. Det är veckans största binära risk för index och AI-hårdvara (`AMD`, `AVGO`, `MRVL`).
- **AI-utbud:** Anthropics notering (≈ 64 mdr USD i emission plus 26 mdr i placering) kan ge rotation bort från listade AI-namn under noteringsveckan. Det är en motvind för AI-mjukvara och adtech (`APP`), men ingen katalysator för något enskilt bolag i boken.
- **Krypto:** BTC och ETH ligger under MA200, ETF-flödena har varit negativa sju dagar i rad och helgen pekar nedåt (overifierat). `COIN` (127,65) och `MSTR` (111,62) ligger långt under MA200. Inget kryptocase görs förrän flödena vänder eller en bekräftad händelse inträffar.
- **Varför marknaden är avvaktande:** Data och flöden har stått still över helgen, och de fyra stora händelserna kommer alla tis–tor. Det rationella läget är bevakning, och dagens US-rotation (LÄGE A) är rätt instans för att avgöra `APP` med färska kurser.

**Watchlist-hygien:** `config/watchlist_us.txt` innehåller långt fler än 25 symboler, men ingen rensning görs. Följande skyddas enligt `prompts/gemensam_korning.md`: innehavet (`CBOE`), sleeven och indexen, den giltiga kandidaten (`APP`) och de avgjorda kandidaterna inom `expiresAt` (`NVDA`, `CSCO`, `AMAT`), rapportbolagen inom 10 handelsdagar, besluten inom utvärderingens 20-dagarsfönster och `ANT` (väntad notering 19/11). Inga tillägg i dag.

### Åtgärdspunkter till Dren (L-3)

1. **`crypto-previousclose-misdated` – ÅTERKOMMANDE.** `quotes["BTC-USD"].previousClose` (71 342,97) och `quotes["ETH-USD"].previousClose` (2 016,83) motsvarar ingen daterad punkt i `state/price_history.json` (2026-11-13: 68 194,22 respektive 1 922,76). **Omfång:** 2 av 2 mynt. **Ersättningskälla:** `state/price_history.json`.
2. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** `feeds.globenewswire` och `feeds.globenewswire-earnings` ger fortfarande `"HTTP 403 – båda försöken"`. **Omfång:** 2 av 6 flöden. **Ersättningskälla:** websök, mfn och SEC 8-K.
3. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** Räntor, DXY, olja och VIX kommer ur websök, eftersom `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas i `state/prices.json`. **Omfång:** samtliga makrovärden.
4. **`weekend-crypto-price-unverifiable` – ÅTERKOMMANDE** (rapport-261108, -261115 och i dag). `prices.yml` kör inte på helger, så `BTC-USD`/`ETH-USD` stod still från lördag 01:28 UTC till minst måndag 05:48 UTC (≥ 52 h). Under den tiden föll BTC enligt sökträffar med 5–9 %, och det syns inte i någon state-fil. Samtliga fyra reservkällor (Yahoo, CoinGecko, Coinbase, Kraken) ger 403 från scoutens körmiljö. **Omfång:** 2 av 2 mynt, varje lör–sön och måndagsmorgon. **Förslag:** en helgcron i `prices.yml` som bara hämtar `-USD`-symbolerna.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
