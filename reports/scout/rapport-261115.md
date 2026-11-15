# Daglig Scout: USA & Krypto
**Datum:** 2026-11-15
**Marknadsklimat:** Det är söndag, och aktiemarknaden har varit stängd sedan fredagens risk-off-session. Den sessionen gav `^GSPC` −0,40 % och `^IXIC` −0,91 %, och Nasdaq stängde exakt på MA200. Krypto låg senast verifierat kring 68 300, alltså 5,9 % under MA200, efter över 1 mdr USD i likviderade långa positioner. Veckan som börjar i morgon är binär: Nvidias rapport 17/11, detaljhandeln samma dag, FOMC-protokollet 18/11 och Anthropics börsnotering (`ANT`), som enligt rapporter väntas handlas från 19/11. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (kandidatkön kontrollerad) och L-5 (negativa påståenden avgränsas till de källor som genomsökts). L-6 tillämpas också: ingen klass utesluts, och krypto täcks enligt `config/fokus_scout.md` ("[X] Krypto – större mynt"). L-2 är uppfylld, eftersom `APP` har rad och kurs. L-1, L-7 och L-8 gäller inte scouten.

## Marknadsöversikt

`git pull` kördes 2026-11-15 05:48 UTC (06:48 CET), och HEAD = `origin/main` = `44dc3d9`. Källan är `state/prices.json` med `generatedAt` 2026-11-14T01:28:52Z, `schemaVersion` 2026-08-02-prevclose, `tickerCount` 321 och `okCount` 316 (Yahoo Finance chart API via GitHub Actions). **Filen är densamma som i går.** `prices.yml` kör bara vardagar, så aktiekurserna är fredagens stängningar, vilket är de senaste som finns. Kryptokurserna är ~28 timmar gamla. Nyhetsflödet (`state/news_feed.json`) har `generatedAt` 2026-11-14T01:29:15Z och täcker **10 av 10 handelsdagar** (2026-11-02 – 2026-11-14, `missingDays` tomt).

| Symbol | Senaste verifierade nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 7 561,67 | −0,40 % fredag (7 592,40 → 7 561,67); +2,51 % på veckan | 2026-11-13T21:43:19Z |
| `^IXIC` | 25 136,27 | −0,91 % fredag (25 366,09 → 25 136,27); +2,27 % på veckan | 2026-11-13T22:15:59Z |
| `BTC-USD` | 68 301,90 | +0,16 % mot daterad punkt 2026-11-13 (68 194,22). **Helgrörelsen är EJ VERIFIERAD.** | 2026-11-14T01:27:12Z |
| `ETH-USD` | 1 929,88 | +0,37 % mot daterad punkt 2026-11-13 (1 922,76). **Helgrörelsen är EJ VERIFIERAD.** | 2026-11-14T01:27:35Z |
| `SPY` (sleeve) | 754,37 | −0,36 % fredag (757,12 → 754,37) | 2026-11-13T21:00:00Z |

**Krypto i helgen: KURS EJ VERIFIERAD.** Prompten anvisar Yahoo Finance som reservkälla, men direktanropet `query1.finance.yahoo.com/v8/finance/chart/BTC-USD` gav `CONNECT tunnel failed, response 403`, och `api.coingecko.com` går inte att slå upp från körmiljön (åtgärdspunkt 4). En sökträff nämner BTC ~67 200 den 14/11 (CapitalStreetFX "Daily Crypto Report 14 Nov 2026"). Det är en sökträff och inte en kurs, så den används inte.

**Teknik** (räknad på råserien i `state/price_history.json`, sista aktiepunkt 2026-11-13; oförändrad sedan i går):
- `^GSPC` ligger **3,02 % över MA200** (7 340,29), så **regimfiltret för US-boken är PÅ** inför måndagens veckorotation. Index ligger under MA50 (7 667,46).
- `^IXIC` står **0,004 % under MA200** (25 137,37) och under MA50 (26 350,07).
- `BTC-USD` ligger **5,91 % under MA200** (72 592,23) och 14,8 % under MA50 (80 132,08). `ETH-USD` ligger **9,46 % under MA200** (2 131,60).

## Ekonomiska siffror & kalender

**Senaste utfall** (inga nya sedan rapport-261114):
- **PPI oktober (fre 2026-11-13):** +0,3 % m/m mot väntade +0,4 %, och årstakten är +6,5 %. Utfallet var en marginell lättnad som inte ändrade räntebilden (se rapport-261114).
- **KPI oktober (2026-11-10):** Totalen steg +0,4 % m/m och kärnan +0,3 %, båda 0,1 pp över förväntan.
- **FOMC 27–28/10:** Räntan låg kvar på 3,75–4,00 % efter röstsiffrorna 10–2. Cook och Hammack reserverade sig för en höjning med 25 bp (sökträffar: Yardeni "Economic Week Ahead: November 16–20", CMC Markets "The Week Ahead", 2026-11-13/14). Inför PPI var en decemberhöjning prisad till ~90 % (FXStreet 2026-11-13, se rapport-261114).

**Kommande (nästa 1–5 handelsdagar):**
- **Tis 2026-11-17 – VECKANS MEST MARKNADSRÖRANDE:** **Nvidia (`NVDA`) rapporterar Q3 FY27 efter stängning.** Det är den första rapporten efter Huangs avgång, med Colette Kress som tillförordnad vd. Konsensus i `state/earnings_calendar.json` är EPS 2,47 (spann 2,26–2,70) och intäkter 108,7 mdr USD. Bolagets egen guide är 108 mdr ±2 % och 74 % bruttomarginal (sökträffar, upstox/learn2.trade "Week Ahead", 2026-11-13/14). Samma dag, kl. 08:30 ET, kommer **detaljhandelns försäljning för oktober**, där konsensus är oklar: +0,2 % m/m (kontrollgruppen +0,4 %) i en källa och oförändrat i en annan. `HD` rapporterar samma dag.
- **Ons 2026-11-18:** **FOMC-protokollet** kl. 14:00 ET, där frågan är hur nära en höjning kommittén var. Bostadsbyggande kl. 08:30 ET. `TGT` och `LOW` rapporterar. Prissättningen av Anthropics börsnotering väntas enligt rapporter denna dag (se nedan).
- **Tor 2026-11-19:** Jobless claims. `WMT` och `ROST` rapporterar. **Anthropic (`ANT`, Nasdaq Global Select)** väntas börja handlas enligt rapporter (se nedan).
- **Fre 2026-11-20:** University of Michigan, slutligt konsumentförtroende för november, kl. 10:00 ET.

**Rapporter nästa 10 handelsdagar** ur `state/earnings_calendar.json` (`generatedAt` 2026-11-14T01:26:58Z, `errors` tomt), US-symboler:
- **11-17:** `NVDA`, `HD`. **11-18:** `TGT`, `LOW`. **11-19:** `WMT`, `ROST`.
- **11-23:** `HPE`. **11-24:** `CLSK` (gissat datum, `isEstimate: true`). **11-25:** `DE`.

**L-5:** Kalendern ser bara de 321 symboler som `prices.yml` hämtar, så resten av det amerikanska universumet är **OKONTROLLERAT**. Disney (`DIS`) nämns i en veckoförhandsvisning som rapportbolag denna vecka, men datumet kan inte verifieras ur kalendern eftersom `DIS` inte hämtas. Därför är den **OKONTROLLERAD**. Samtliga datum är bevakningsposter enligt punkt 8, aldrig köpförslag.

## Aktuella händelser & katalysatorer

- **Anthropics börsnotering (`ANT`), bekräftade villkor och väntad notering.** Roadshowen startade 2026-11-10 med 825 miljoner A-aktier i ett prisintervall på **70–78 USD**, på Nasdaq Global Select under tickern `ANT`. Utöver det finns en riktad placering på ~26 mdr USD till sju chip- och molnbolag (RTTNews "Anthropic sets IPO price range at $70–78 per share, launches roadshow", 2026-11-10; letsdatascience/ai-tldr 2026-11-10). Bolaget drog tillbaka ett tidigare läckt intervall på 70–80 USD (Stocktwits/Reuters 2026-11-10). ⚠️ **RYKTE – EJ BEKRÄFTAT (CNBC, källor med insyn, ~2026-11-13):** prissättning 18/11 och handel från 19/11. Värderingsuppgifterna går isär, 1,1–1,75 biljoner USD, och används inte. Eftersom handel inte har inletts finns ingen kurs, och en nynoterad aktie saknar MA200, vilket per definition blockerar en ny position (`prompts/gemensam_korning.md`: "Saknad MA200 eller kurs ≤ MA200 blockerar nya aktiepositioner"). Därför blir det **ingen kandidatpost**. Noteringen är däremot den största enskilda tillgångshändelsen i AI-sektorn i år. Den kan dra kapital från AI-namn i boken, och 825 mn aktier × ~74 USD ≈ 61 mdr USD ny emission ska absorberas. `ANT` läggs i `config/watchlist_us.txt` så att kursserien börjar byggas från första handelsdagen.
- **Nvidia (`NVDA`) inför rapporten:** Aktien stängde fredagen på 162,85 (−2,01 %; prices.json, marketTime 2026-11-13T21:00:01Z), med −12,75 % på veckan och 20,25 % under MA200 (204,19). Ingen ny bekräftad bolagshändelse har hittats sedan 8-K:n den 12/11 (i websök; övriga källor **OKONTROLLERADE**).
- **Helgen:** Inga nya bekräftade bolagshändelser i det amerikanska universumet har hittats i websök. `news_feed.json` har inte uppdaterats sedan 2026-11-14T01:29Z, eftersom `news.yml` bara kör vardagar. **Påståendet gäller bara de genomsökta källorna (L-5).** Hela helgflödet är **OKONTROLLERAT**, eftersom feeden står still.
- **Krypto:** De bekräftade siffrorna är spot-ETF:ernas nettoutflöden på ~1,6 mdr USD sedan månadsskiftet t.o.m. 10/11 (Cointelegraph 2026-11-11, SoSoValue) och utflöden på −1,28 mdr USD veckan t.o.m. 7/11, vilket gjorde årets flöde negativt (The Block 2026-11-07). Inga ETF-flöden för 13/11 med säker datering har hittats. Ingen ny bekräftad regulatorisk eller protokollkatalysator har hittats i websök, och övriga källor är **OKONTROLLERADE**.

## Uppföljning av tidigare case

- **`APP` (rapport-261114): 409,10 → 409,10** (±0,00 %, ingen ny session; marketTime 2026-11-13T21:00:01Z, prices.json/Yahoo chart API). **Tes INTAKT:** stängningen ligger 0,81 % över MA200 (405,79), med RSI 72,6 och volym 0,59× 20-dagarssnittet. Kandidaten `261114-APP` har status `new` med `expiresAt` 2026-11-20 och avgörs av US-boken, i första hand i måndagens LÄGE A (2026-11-16). Den tunna MA200-marginalen och volymkriteriet är de grindar boken behöver pröva. Anthropics notering 19/11 är ett sektorspecifikt utbudstryck att väga in, men den är ingen bolagshändelse för AppLovin.

**Kandidatkön (`state/scout_candidates.json`):** 125 poster, varav 115 `rejected`, 9 `promoted` och **1 `new`** (`261114-APP`, inom `expiresAt`). **L-4:** Ingen post avvisad på ett tillfälligt datavillkor väntar på omprövning, eftersom ingen ny kurs har tillkommit sedan i går. **Inga nya poster i dag:** ingen ny bekräftad och handlingsbar katalysator finns, och `ANT` har ingen kurs och saknar MA200.

**US-boken (läses, ändras inte):** `CBOE` stängde fredagen på 375,42 (+1,77 %, dagshögsta 378,17; marketTime 2026-11-13T21:00:00Z). Det är 1,85 % under målet 382,50 och 8,8 % över stoppen 345,00. Sleeven är `SPY`.

## Dagens case

**Inga nya case i dag.** Ingen session har handlats sedan rapport-261114, och ingen ny bekräftad katalysator har hittats. Kurser och nyhetsflöde står still sedan lördag ~01:29 UTC. Veckans stora händelser (NVDA 17/11, FOMC-protokollet 18/11, `ANT` 19/11, WMT 19/11) är väntade event och därmed bevakningsposter enligt punkt 8, inte köpförslag. Att bygga case på ~52 timmar gamla aktiekurser och overifierade helgkurser för krypto vore att tvinga fram dem. Det enda aktiva caset, `APP`, väntar på bokens avgörande. Skälen står under Makro nedan.

## Makro- & sektorfaktorer att bevaka

- **Räntor och inflation:** PPI-årstakten på 6,5 % och en 10-årsränta på ~5 % (sökträffar; `^TNX` saknas i `prices.json`) ger fortsatt motvind för långdurationstillgångar och krypto. FOMC-protokollet 18/11 avgör hur hökaktig marknaden läser Fed inför december.
- **Regimen:** `^GSPC` ligger +3,02 % över MA200, så regimen är PÅ. Nasdaq står på MA200, och NVDA-rapporten 17/11 avgör sannolikt vilken sida den hamnar på. Det är veckans största binära risk för index och för AI-hårdvaran (`AMD`, `AVGO`, `MRVL`).
- **AI-utbud:** Anthropics notering är veckans största sektorhändelse. En emission på ~60 mdr USD plus en riktad placering på 26 mdr kan ge rotation från listade AI-namn mot den nya aktien. Det är en motvind för AI-mjukvara och adtech (`APP`) under noteringsveckan, men ingen katalysator för något enskilt bolag i boken.
- **Krypto:** BTC och ETH ligger under MA200 med RSI runt 25, och ETF-flödena är negativa. `COIN` (127,65, 26,7 % under MA200) och `MSTR` (111,62, 15,9 % under MA200) är översålda, men ett översålt läge är ingen katalysator. Inget kryptocase görs förrän flödena vänder eller en bekräftad händelse inträffar.
- **Varför marknaden är avvaktande:** Börserna är stängda, och data och flöden står still över helgen. De fyra stora händelserna kommer alla tis–tor. Det rationella läget är bevakning, och måndagens US-rotation (LÄGE A) är rätt instans för att avgöra `APP` med färska kurser.

**Watchlist-hygien:** `config/watchlist_us.txt` innehåller långt fler än 25 symboler, men ingen rensning görs. Följande skyddas enligt `prompts/gemensam_korning.md`: innehavet (`CBOE`), sleeven och indexen, den giltiga kandidaten (`APP`) och de avgjorda kandidaterna inom `expiresAt` (`NVDA`, `CSCO`, `AMAT`, `AMD`), rapportbolagen inom 10 handelsdagar samt besluten inom utvärderingens 20-dagarsfönster. **Tillägg:** `ANT` (Anthropic), som saknar kurs fram till den väntade första handelsdagen 19/11. Fram till dess ger Yahoo inget svar för symbolen, och det är förväntat.

### Åtgärdspunkter till Dren (L-3)

1. **`crypto-previousclose-misdated` – ÅTERKOMMANDE.** `quotes["BTC-USD"].previousClose` (71 342,97) och `quotes["ETH-USD"].previousClose` (2 016,83) motsvarar ingen daterad punkt i `state/price_history.json` (2026-11-13: 68 194,22 respektive 1 922,76). **Omfång:** 2 av 2 mynt. **Ersättningskälla:** `state/price_history.json`.
2. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** `feeds.globenewswire` och `feeds.globenewswire-earnings` ger fortfarande `"HTTP 403 – båda försöken"`. **Omfång:** 2 av 6 flöden. **Ersättningskälla:** websök, mfn och SEC 8-K.
3. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** Räntor, DXY, olja och VIX kommer ur websök, eftersom `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas i `state/prices.json`. **Omfång:** samtliga makrovärden.
4. **`weekend-crypto-price-unverifiable` – ÅTERKOMMANDE** (även rapport-261108). `prices.yml` kör inte på helger, så `BTC-USD`/`ETH-USD` i `state/prices.json` står still från lördag ~01:28 UTC till måndag. Reservkällan Yahoo ger 403 från scoutens körmiljö, och `api.coingecko.com` går inte att slå upp. **Omfång:** 2 av 2 mynt, varje lör–sön (2 av 7 scoutrapporter per vecka). **Förslag:** en helgcron i `prices.yml` som bara hämtar `-USD`-symbolerna.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
