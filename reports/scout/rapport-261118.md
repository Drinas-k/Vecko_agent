# Daglig Scout: USA & Krypto
**Datum:** 2026-11-18
**Marknadsklimat:** Andra raka risk-off-dagen: `^GSPC` −1,03 % och `^IXIC` −0,74 % in i Nvidias rapport. Nvidia slog sedan förväntningarna efter stängning och steg efterbörs enligt medier, men **S&P 500 stängde 0,05 % under sin MA200**. Därmed är US-bokens regimfilter **AV** på stängningsbasis. BTC (64 144,52) och ETH (1 797,28) föll ytterligare drygt 1 % och ligger 11–15 % under MA200. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (kandidatkön kontrollerad), L-5 (negativa påståenden avgränsade till genomsökta källor) och L-6 (krypto täcks enligt `config/fokus_scout.md`). L-1, L-2, L-7, L-8 och L-9 gäller inte scouten.

## Marknadsöversikt

`git pull` kördes 2026-11-18 05:48 UTC (06:48 CET). HEAD = `origin/main` = `5862503`. Källan är `state/prices.json` med `generatedAt` 2026-11-18T02:55:18Z, `schemaVersion` 2026-08-02-prevclose, `tickerCount` 330 och `okCount` 324 (Yahoo Finance chart API via GitHub Actions). Aktiekurserna är tisdagens stängning. Nyhetsflödet (`state/news_feed.json`) har `generatedAt` 2026-11-17T22:56:38Z och täcker **10 av 10 handelsdagar** (2026-11-03 – 2026-11-17, `missingDays` tomt).

| Symbol | Nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 7 340,53 | −1,03 % (7 416,59 → 7 340,53) | 2026-11-17T21:42:12Z |
| `^IXIC` | 24 328,38 | −0,74 % (24 509,76 → 24 328,38) | 2026-11-17T22:15:59Z |
| `BTC-USD` | 64 144,52 | −1,13 % mot daterad punkt 2026-11-17 (64 879,88) | 2026-11-18T02:53:41Z |
| `ETH-USD` | 1 797,28 | −1,46 % mot daterad punkt 2026-11-17 (1 823,83) | 2026-11-18T02:54:02Z |
| `SPY` (sleeve) | 732,44 | −1,01 % (739,95 → 732,44) | 2026-11-17T21:00:00Z |

Kryptorörelserna är räknade mot daterade punkter i `state/price_history.json`, inte mot `previousClose` (se åtgärdspunkt 1).

**Teknik** (räknad på råserien i `state/price_history.json`, sista aktiepunkt 2026-11-17):
- `^GSPC` ligger **0,05 % UNDER MA200** (7 344,50). **Regimfiltret för US-boken slår därmed AV**: boken får inte ta nya aktiepositioner förrän index stänger över MA200 igen. Marginalen var +1,01 % i går och +3,02 % i förrgår. Index ligger 4,1 % under MA50 (7 654,76). `SPY` ligger 0,01 % över sin egen MA200 (732,34). Det spelar ingen roll för regeln, som läser `^GSPC`.
- `^IXIC` ligger **3,25 % under MA200** (25 146,29) och 7,4 % under MA50 (26 268,27).
- `BTC-USD` ligger **11,48 % under MA200** (72 464,22) och 19,2 % under MA50 (79 410,70). `ETH-USD` ligger **15,40 % under MA200** (2 124,41).

## Ekonomiska siffror & kalender

**Senaste utfall:**
- **Detaljhandelns försäljning, oktober (tis 2026-11-17):** utfallet och förväntan är **EJ VERIFIERADE**. Websök gav inga träffar daterade 2026, bara äldre årgångar, så siffran redovisas inte.
- **PPI oktober (fre 2026-11-13):** +0,3 % m/m mot väntade +0,4 %, årstakt +6,5 % (se rapport-261114).
- **KPI oktober (2026-11-10):** total +0,4 % m/m och kärna +0,3 %, båda 0,1 pp över förväntan.
- **FOMC 27–28/10:** räntan oförändrad på 3,75–4,00 % (10–2). Marknadsrapporter 2026-11-17 anger fortsatt förväntningar om en höjning som motvind (CapitalStreetFX dagsrapport 2026-11-18, "Chip Curbs And Fed Hike Bets Hit Stocks Before Nvidia"). Sannolikheten är inte verifierad.

**Kommande (nästa 1–5 handelsdagar):**
- **Ons 2026-11-18 (i dag) – DAGENS MEST MARKNADSRÖRANDE:** **FOMC-protokollet kl. 14:00 ET** (20:00 CET). Höjningsfrågan är det som pressar marknaden. Samma dag kommer bostadsbyggandet. `TGT` och `LOW` rapporterar före öppning. Efterbörskurserna i `prices.json` är före rapport (`TGT` 158,46 post, 2026-11-18T00:59Z; `LOW` 220,23 post, 2026-11-18T00:47Z). `ANT` prissätts enligt uppgift (se nedan).
- **Tor 2026-11-19:** jobless claims. `WMT` och `ROST` rapporterar. `ANT` väntas börja handlas på Nasdaq (⚠️ RYKTE – EJ BEKRÄFTAT, CNBC 2026-11-10).
- **Fre 2026-11-20:** University of Michigan, slutligt konsumentförtroende.

**Rapporter nästa 10 handelsdagar** ur `state/earnings_calendar.json` (`generatedAt` 2026-11-18T02:53:27Z, `errors` tomt), US-symboler:
- **11-18:** `TGT`, `LOW`. **11-19:** `WMT`, `ROST`. **11-23:** `HPE`. **11-24:** `CLSK` (gissat datum, `isEstimate: true`). **11-25:** `DE`. **12-01:** `MRVL`. **12-02:** `ZS`, `FIVE` (gissat datum).

**L-5:** Kalendern omfattar bara de symboler som `prices.yml` hämtar. Resten av det amerikanska universumet är **OKONTROLLERAT**. Alla datum ovan är bevakningsposter enligt punkt 8, aldrig köpförslag.

## Aktuella händelser & katalysatorer

- **Nvidia (`NVDA`) Q3 FY27, 2026-11-17 efter stängning, BEKRÄFTAT utfall:** intäkterna var 115,8 mdr USD (+103 % å/å) mot cirka 109 mdr väntat. Datacenter stod för 107,6 mdr (+110 %). Justerad EPS var 2,68 mot cirka 2,47 väntat, och GAAP-bruttomarginalen 74,8 %. Q4-guiden är **130,0 mdr ± 3 %**. Guiden antar **ingen datacenterintäkt från Kina**, och kvartalet har en extra vecka. Vera Rubin NVL72 skeppas (NVIDIA-pressmeddelande 2026-11-17 via Morningstar/GlobeNewswire; Yahoo Finance UK "Nvidia beats third-quarter estimates as revenue more than doubles", 2026-11-17). Styrelseordföranden Harvey Jones utesluter att Huang återinsätts (Yahoo Finance 2026-11-17; TipRanks 2026-11-17). Det rättar gårdagens ryktesmärkning: uppgiften kommer nu från bolaget. **Efterbörsreaktion:** medierna anger olika storlek, från cirka +2 % till +4,57 % (Investing.com: 162,56 USD; TechFlow Post med hänvisning till CNBC: nära +4 %). **KURS EJ VERIFIERAD:** `prices.json` saknar efterbörskurs för `NVDA`, och mediernas kurser används inte. Den reguljära stängningen var 155,46 (−0,44 %, marketTime 2026-11-17T21:00:00Z, volym 370,1 milj. = 1,71x 20-dagarssnittet). → Case 1 och kandidatpost `261118-NVDA`.
- **Home Depot (`HD`) Q3 FY26, 2026-11-17 före öppning, BEKRÄFTAT:** försäljningen var 43,4 mdr USD (+4,9 %), jämförbar försäljning +2,2 % och justerad EPS 3,86 mot 3,74 året innan. Bolaget skriver att resultatet "exceeded our expectations" (HD 8-K ex. 99.1, SEC, 2026-11-17). De uppdaterade helårssiffrorna gick inte att läsa ur det utdrag som var tillgängligt. Kursen föll ändå: 339,01 (−2,45 %, 1,59x volym, marketTime 2026-11-17T21:00:03Z). Den ligger 2,0 % över MA200 (332,36). **Ingen kandidatpost**, eftersom reaktionen var negativ och guiden inte är verifierad.
- **Exportregeln för AI-chips (måndag 2026-11-16):** handelsdepartementet införde en regel som skärper granskningen av försäljning till datacenter i tredjeland, för att stänga en väg runt Kina-förbudet. SOX föll över 5 % den dagen (Inquirer 2026-11-16; Motley Fool 2026-11-16). Nvidias Kina-fria guide ska läsas mot den bakgrunden. `TSM` föll ytterligare 3,68 % i går (359,69), medan `AVGO` steg 2,46 % (341,60). Båda har marketTime 2026-11-17T21:00Z.
- **Anthropic (`ANT`):** villkoren är oförändrade, 70–78 USD per aktie (Renaissance Capital 2026-11-10; Fortune 2026-11-10). ⚠️ **RYKTE – EJ BEKRÄFTAT (CNBC, källor med insyn, 2026-11-10):** prissättning 18/11 och handel från 19/11. Websök gav ingen bekräftad slutlig prissättning (L-5: avser websök 05:50 UTC). Aktien saknar kurs och MA200, så noteringen blockerar en ny position per definition. **Ingen kandidatpost.**
- **AES:** slutligt regulatoriskt godkännande av uppköpet av ett konsortium som leds av GIP och EQT. Affären väntas slutföras 2026-12-02 (PR Newswire 2026-11-17T22:15Z, `news_feed.json`). Det är ett uppköp till fast pris, så **ingen kandidatpost**.
- **Krypto:** websök gav uppgifter om ETF-utflöden "till och med 17/11" (CryptoSlate, 2,57 mdr), men samma artiklar anger BTC-kurser runt 89 000–93 000. Det stämmer inte med verifierade 64 144,52 och tyder på att materialet gäller november 2025. Flödet för 2026-11-17 är därför **OKONTROLLERAT** (L-5). The Block rapporterade 2026-11-14 en andra vecka med utflöden över 1 mdr USD. `COIN` föll 4,02 % (115,02) och `MSTR` 6,34 % (96,50). Ingen bekräftad regulatorisk händelse eller protokollhändelse hittades i websök.

## Uppföljning av tidigare case

- `BIIB` (rapport-261117): 251,65 → 250,79 (−0,34 %, prices.json/Yahoo chart API, marketTime 2026-11-17T21:00:01Z). Volymen var 968 955 (0,80x). Reaktionsdagen efter femårsdatan för Leqembi blev platt med låg volym. Kursen ligger kvar 21,8 % över MA200 (205,87). Tesen är **FÖRSVAGAD**: marknaden prisade inte in datan som en katalysator. Kandidaten avvisades 2026-11-17 av US-rotationen på två skäl. Det ena är tillfälligt: kursen kunde inte verifieras. Det andra är ett omdöme: grind 2, volym 0,69x och fallande MACD-histogram. Eftersom avvisningen även vilar på omdöme gäller L-4 inte fullt ut. 17/11-stängningen är dessutom en post-event-kurs med 0,80x volym, så volymspärren kvarstår. Från i dag tillkommer regimspärren.

**Kandidatkön (`state/scout_candidates.json`):** före körningen fanns 126 poster, varav 117 `rejected`, 9 `promoted` och **0 `new`**. **L-4:** ingen post inom `expiresAt` är avvisad enbart på ett tillfälligt datavillkor som nu har fyllts. `BIIB` ovan är det närmaste fallet och omfattas inte, eftersom även grind 2 fällde den. **En ny post i dag:** `261118-NVDA` (`status: new`, `price: null`).

**US-boken (läses, ändras inte):** `CBOE` stängde på 370,07 (−1,97 %, dagslägsta 367,92, marketTime 2026-11-17T21:00:00Z). Det är 3,25 % under målet 382,50 och 5,3 % över stoppen 351,50. Sleeven är `SPY` 732,44.

## Dagens case
### Case 1: NVIDIA (NVDA / NASDAQ)
**Katalysator:** Q3 FY27 rapporterades 2026-11-17 efter stängning. Det är den första rapporten under interim-vd Colette Kress. Intäkterna blev 115,8 mdr (+103 %) mot cirka 109 mdr väntat, justerad EPS 2,68 mot cirka 2,47, och Q4-guiden 130 mdr ± 3 % utan Kina-datacenter (NVIDIA-pressmeddelande via Morningstar/GlobeNewswire 2026-11-17; Yahoo Finance UK 2026-11-17). Utfallet har inträffat och är bekräftat. Pressmeddelandets brödtext gick inte att hämta direkt, se åtgärdspunkt 4.
**Bull case:** Intäkterna fördubblades och guiden innebär ytterligare cirka +12 % kvartal mot kvartal, trots noll Kina-datacenter och en färsk exportregel. Efterfrågan bärs alltså av marknader som inte påverkas av regeln. Leveranserna av Vera Rubin har börjat, vilket minskar oron för en produktövergång. Vd-frågan har fått ett tydligt besked (ingen återkomst), och det tar bort ett osäkerhetsmoment. Aktien har fallit från MA50 211,76 till 155,46 (−26,6 %) på ledningskrisen, så förväntningarna har pressats ned kraftigt.
**Bear case:** Kursen ligger **23,7 % under MA200** (203,87) och under MA50. Det blockerar en ny aktieposition oavsett rapportens kvalitet. **Regimfiltret i US-boken slog av** vid gårdagens stängning, vilket är ytterligare en blockering. Ledningen är tillfällig och sökandet efter ny vd pågår. Minst en analytiker sänkte till Hold med hänvisning till "too much uncertainty" (Yahoo Finance 2026-11-17). Efterbörsuppgången krympte enligt medierna under natten. Det finns en risk för "sell the news" i en marknad som pressas av höjningsförväntningar och utbudet från ANT.
**Setup:** Den reguljära stängningen 155,46 (marketTime 2026-11-17T21:00:00Z, prices.json/Yahoo chart API) är en **pre-event-kurs**. Ingen verifierad efterbörskurs finns, så `price: null` i kandidatposten. `prices.yml` fyller i en kvalificerad post-event-kurs (förbörs eller reguljär 18/11). Volymen 17/11 var 1,71x 20-dagarssnittet, MA50 är 211,76, MA200 203,87 och 250-dagarsserien är komplett. Värderingstal är inte hämtade. Ansvarig bok (US) ska pröva samtliga fem grindar. Med kurs under MA200 och regimen av blir utfallet en avvisning, men den ska namnges och loggas som kontrafaktiskt underlag. En förbörskurs får bara ge en villkorad plan mot reguljär session.

Inga fler case i dag. Ett starkt case kräver en bekräftad katalysator och en kurs som ett regimfilter tillåter. US-bokens regim är nu av, och de få av gårdagens vinnare som låg över MA200 (`CXW` +4,81 %, `COHR` +3,65 %, `CIEN` +2,82 %) saknar en daterad katalysator i `news_feed.json`. HD:s bekräftade rapport fick en negativ reaktion. TGT, LOW, WMT och ROST är väntade event och därmed bevakningsposter enligt punkt 8. Skälen till avvaktan står under Makro nedan.

## Makro- & sektorfaktorer att bevaka

- **Regimen (VIKTIGAST för US-boken):** `^GSPC` 7 340,53 mot MA200 7 344,50 är 0,05 % under. Det är första stängningen under MA200 i den här serien av rapporter. Marginalen är minimal, så Nvidias efterbörsuppgång kan lyfta index tillbaka över MA200 redan i dag. Regeln läser stängningen, inte terminer. Rotationen 15:00 CET läser alltså regimen som AV tills en ny stängning finns.
- **Räntor och dollar:** Förväntningar om en höjning i december och en stark dollar (högsta nivån sedan april 2025 enligt Reuters 2026-11-16) är motvind för långdurationstillgångar och krypto. FOMC-protokollet i kväll är nästa datapunkt. Räntenivåer och DXY är inte verifierade ur state (åtgärdspunkt 3).
- **AI och halvledare:** Nvidias rapport bekräftar efterfrågan, men sektorn bär exportregeln från 16/11 och ett stort utbud genom ANT-noteringen. `TSM` (−10,8 % mot MA200), `AVGO` (−7,0 %) och `NVDA` (−23,7 %) ligger alla under MA200. Sektorn ger alltså inga köpbara setups förrän trenderna har reparerats.
- **Krypto:** BTC och ETH ligger 11–15 % under MA200 och fortsätter nedåt, och `MSTR` och `COIN` ligger 27–34 % under. Hård dollar, ETF-utflöden och höjningsrisk pekar åt samma håll. Inget kryptocase görs.
- **Konsument:** HD föll trots en rapport över bolagets egna förväntningar. TGT, LOW, WMT och ROST rapporterar 18–19/11, vilket ger veckans konsumentbild. `TGT` (+16,2 % mot MA200) och `WMT` (+7,2 %) har intakta trender, men rapportdagarna köps aldrig in i (punkt 8).
- **Varför marknaden är avvaktande:** Index har brutit MA200, FOMC-protokollet kommer i kväll och ANT-noteringen tar likviditet. Den enda starka katalysatorn (NVDA) sitter på en trasig trend. Bevakning är rätt läge tills index återtagit MA200.

**Watchlist-hygien:** `config/watchlist_us.txt` innehåller långt fler än 25 symboler, men ingen rensning görs. Följande skyddas enligt `prompts/gemensam_korning.md`: innehavet (`CBOE`), sleeven och indexen, kandidaterna inom `expiresAt` (`NVDA`, `CSCO`, `AMAT`, `APP`, `BIIB` med flera), rapportbolagen inom 10 handelsdagar, besluten från rotationen 2026-11-16 inom 20-dagarsfönstret och `ANT`. `NVDA` och `HD` finns redan i listan. Inga tillägg.

### Åtgärdspunkter till Dren (L-3)

1. **`crypto-previousclose-misdated` – ÅTERKOMMANDE.** `quotes["BTC-USD"].previousClose` (64 855,84) och `quotes["ETH-USD"].previousClose` (1 819,28) motsvarar ingen daterad punkt i `state/price_history.json` (2026-11-17: 64 879,88 respektive 1 823,83). **Omfång:** 2 av 2 mynt. **Ersättningskälla:** `state/price_history.json`.
2. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** `feeds.globenewswire` och `feeds.globenewswire-earnings` ger fortfarande `"HTTP 403 – båda försöken (0.0 s)"`. **Omfång:** 2 av 6 flöden. Det är just GlobeNewswire som publicerade Nvidias rapport, så den syns inte i `news_feed.json`. **Ersättningskälla:** websök (Morningstar-syndikering), prnewswire, mfn och SEC 8-K.
3. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas i `state/prices.json`. Detaljhandelssiffran och räntenivåerna kunde därför inte anges. **Omfång:** samtliga makrovärden.
4. **`scout-cannot-fetch-press-release-body` – ÅTERKOMMANDE.** WebFetch mot `nvidianews.nvidia.com`, `www.stocktitan.net` och `www.fool.com` ger `getaddrinfo ENOTFOUND` från scoutens körmiljö (värdarna är inte tillåtna i sessionens nätverksinställningar). Nvidias siffror är därför hämtade ur sökresultatens sammanfattningar och inte ur primärdokumentet. **Omfång:** varje case som bygger på ett pressmeddelande, i dag 1 av 1. **Förslag:** tillåt `nvidianews.nvidia.com`, `prnewswire.com` och `sec.gov` i miljöns nätverkspolicy.
5. **`nvda-no-extended-quote` – NY.** `prices.json` har `extendedCount` 8 men saknar efterbörskurs för `NVDA` (bara `TGT`, `LOW`, `WMT` och `ROST` bland US-namnen har en). Det gäller trots att NVDA rapporterade AMC och var veckans viktigaste händelse. **Omfång:** 1 rapportbolag 17/11 (även `DLB` saknar en). **Ersättningskälla:** ingen, därför `price: null` i kandidatposten.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
