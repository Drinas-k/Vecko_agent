# Daglig Scout: USA & Krypto
**Datum:** 2026-11-19
**Marknadsklimat:** Tredje raka svaga dagen. `^GSPC` föll 0,23 % och stängde **0,31 % under MA200**, vilket är andra stängningen under. US-bokens regimfilter är därmed fortsatt **AV**. Nvidia föll 2,89 % trots en stark rapport. FOMC-protokollet pekar på en räntehöjning i december, och BTC (62 595,96) och ETH (1 770,24) föll ytterligare till 14–17 % under MA200. Anthropic noteras i dag efter en rekordstor IPO på 83 USD. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (kandidatkön kontrollerad), L-5 (negativa påståenden avgränsade till genomsökta källor) och L-6 (krypto täcks enligt `config/fokus_scout.md`). L-1, L-2, L-7, L-8 och L-9 gäller inte scouten.

## Marknadsöversikt

`git pull` kördes 2026-11-19 05:48 UTC (06:48 CET). HEAD = `origin/main` = `76f3538`. Källan är `state/prices.json` med `generatedAt` 2026-11-19T02:33:49Z, `schemaVersion` 2026-08-02-prevclose, `tickerCount` 330 och `okCount` 324 (Yahoo Finance chart API via GitHub Actions). Aktiekurserna är onsdagens stängning. Nyhetsflödet (`state/news_feed.json`) har `generatedAt` 2026-11-18T22:36:42Z och täcker **10 av 10 handelsdagar** (2026-11-04 – 2026-11-18, `missingDays` tomt).

| Symbol | Nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 7 323,63 | −0,23 % (7 340,53 → 7 323,63) | 2026-11-18T21:57:25Z |
| `^IXIC` | 24 429,89 | +0,42 % (24 328,38 → 24 429,89) | 2026-11-18T22:15:59Z |
| `BTC-USD` | 62 595,96 | −2,41 % mot gårdagens rapport (64 144,52); +0,14 % mot daterad punkt 2026-11-18 (62 510,27) | 2026-11-19T02:32:12Z |
| `ETH-USD` | 1 770,24 | −1,50 % mot gårdagens rapport (1 797,28); +0,09 % mot daterad punkt 2026-11-18 (1 768,63) | 2026-11-19T02:32:32Z |
| `SPY` (sleeve) | 730,20 | −0,31 % (732,44 → 730,20) | 2026-11-18T21:00:00Z |

Kryptorörelserna är räknade mot gårdagens rapport och mot daterade punkter i `state/price_history.json`, inte mot `previousClose` (se åtgärdspunkt 1).

**Teknik** (räknad på råserien i `state/price_history.json`, sista aktiepunkt 2026-11-18):
- `^GSPC` ligger **0,31 % UNDER MA200** (7 346,53). Det är andra stängningen under, efter −0,05 % i går. **Regimfiltret för US-boken är AV**: inga nya aktiepositioner förrän index stänger över MA200. Index ligger 4,2 % under MA50 (7 648,51). Dagsintervallet var 7 285,76–7 367,68, så index handlades över MA200 intradag men stängde under. `SPY` ligger 0,32 % under sin egen MA200 (732,55).
- `^IXIC` ligger **2,87 % under MA200** (25 152,16) och 6,9 % under MA50 (26 231,80).
- `BTC-USD` ligger **13,54 % under MA200** (72 395,00) och 20,9 % under MA50 (79 102,28). `ETH-USD` ligger **16,55 % under MA200** (2 121,32).

## Ekonomiska siffror & kalender

**Senaste utfall:**
- **FOMC-protokollet från 27–28/10 (ons 2026-11-18, 14:00 ET) – GÅRDAGENS MEST MARKNADSRÖRANDE:** "nearly all" ledamöter väntar sig en höjning på en kvarts procentenhet i december. Två lyfte möjligheten av en höjning på en halv procentenhet. En "vast majority" oroar sig för att inflationen biter sig fast även om bensinpriset faller, och protokollet varnar för snabbt växande AI-relaterade skulder i "complex and opaque financing structures" (CNBC 2026-11-18, "Fed officials expect more rate hikes, worry about AI impact on inflation, minutes show"; Yahoo Finance/AP 2026-11-18). CME prisar enligt samma rapportering 92,7 % för +25 bp i december. Sannolikheten är inte verifierad ur state. Räntan är 3,75–4,00 % efter beskedet 28/10 (10–2, Cook och Hammack röstade för höjning). Protokollet finns i `news_feed.json` (fed-press, 2026-11-18T19:00Z).
- **PPI oktober (fre 2026-11-13):** +0,3 % m/m mot väntade +0,4 % (se rapport-261114).
- **KPI oktober (2026-11-10):** total +0,4 % m/m och kärna +0,3 %, båda 0,1 pp över förväntan.
- **Bostadsbyggandet (ons 2026-11-18):** utfall och förväntan är **EJ VERIFIERADE**. Websök gav inga träffar daterade 2026.

**Kommande (nästa 1–5 handelsdagar):**
- **Tor 2026-11-19 (i dag):** jobless claims kl. 08:30 ET. Konsensus är **EJ VERIFIERAD**, websök gav bara äldre årgångar. `WMT` rapporterar före öppning och `ROST` efter stängning (`state/earnings_calendar.json`). **`ANT` börjar handlas på Nasdaq.** Det är nu bekräftat av bolaget, se nedan.
- **Fre 2026-11-20:** University of Michigan, slutligt konsumentförtroende.
- **Tor 2026-11-26:** Thanksgiving, börsen stängd. **Fre 2026-11-27:** halvdag.
- **FOMC 8–9/12** är nästa räntebesked och ligger utanför fönstret.

**Rapporter nästa 10 handelsdagar** ur `state/earnings_calendar.json` (`generatedAt` 2026-11-19T02:31:57Z, `errors` tomt), US-symboler i `config/watchlist_us.txt`:
- **11-19:** `WMT`, `ROST`. **11-23:** `HPE`. **11-24:** `CLSK` (gissat datum, `isEstimate: true`). **11-25:** `DE`. **12-01:** `MRVL`. **12-02:** `CBRL`, `FIVE`, `ZS`. **12-03:** `COO`, `S`.

**L-5:** Kalendern omfattar bara de symboler som `prices.yml` hämtar. Resten av det amerikanska universumet är **OKONTROLLERAT**. Alla datum ovan är bevakningsposter enligt punkt 8, aldrig köpförslag. Efterbörskurserna för `WMT` (127,564 post, 2026-11-19T00:58Z) och `ROST` (231,00 post, 2026-11-19T00:51Z) är tagna **före** respektive rapport.

## Aktuella händelser & katalysatorer

- **Target (`TGT`) Q3 2026, 2026-11-18 före öppning, BEKRÄFTAT utfall:** nettoförsäljningen var 27,1 mdr USD (+7,1 %), jämförbar försäljning +5,6 % och trafiken +5 %. CNBC kallar det bästa försäljningstillväxten på fem år. Justerad EPS var 2,65 mot 2,07 väntat, och helårsguiden för försäljningen höjdes till cirka +6 %, en procentenhet över det tidigare intervallet. **Av EPS är 0,50 USD en engångspost från tullåterbetalningar** (301 MUSD före skatt). Vd Michael Fiddelke säger att bolaget är "encouraged" av julhandelns start (CNBC 2026-11-18, "Target shares rise 7% as retailer posts best sales growth in five years, hikes guidance"; Target 8-K ex. 99, SEC 2026-11-18). Kursen stängde på 165,93 (+4,01 %, dagsintervall 159,95–171,91, volym 3,14x 20-dagarssnittet, marketTime 2026-11-18T21:03:24Z). CNBC:s +7 % var intradagshögsta. → Case 1 och kandidatpost `261119-TGT`.
- **Anthropic (`ANT`) prissatte sin IPO på 83 USD**, över intervallet 70–78. Bolaget säljer 980 miljoner aktier, mot planerade 825 miljoner, och tar in cirka 81,3 mdr USD. Det är den största börsnoteringen hittills. Handeln på Nasdaq startar i dag 2026-11-19 (CNBC 2026-11-18, "Anthropic IPO raises over $81 billion in largest offering on record"; Axios 2026-11-18; Yahoo Finance 2026-11-18). Axios anger ett initialt börsvärde på 1,08 biljoner USD. Gårdagens ryktesmärkning om datumet är därmed ersatt av bolagets besked. Aktien saknar kurs och MA200 (`prices.json`: "kunde inte hämtas", vilket är väntat före noteringen). Det blockerar en ny position per definition. **Ingen kandidatpost.** Utbudet drar likviditet ur AI-sektorn i dag.
- **Nvidia (`NVDA`) reaktionsdag:** aktien föll 2,89 % till 150,96 (dagsintervall 150,40–159,70, volym 1,49x, marketTime 2026-11-18T21:00:00Z) trots rapporten 17/11 (intäkter 115,8 mdr, Q4-guide 130 mdr). Efterbörsuppgången höll alltså inte. Websök gav ingen artikel daterad 2026-11-18 som förklarar fallet (L-5: avser websök 05:55 UTC). Därför anges ingen orsak. Se uppföljningen nedan.
- **Lowe's (`LOW`) Q3, 2026-11-18 före öppning, BEKRÄFTAT:** justerad EPS 3,10, försäljningen +9,3 % och jämförbar försäljning +1,8 %. Onlineförsäljningen ökade 17,4 %, och helårsprognosen uppdaterades (LOW 8-K ex. 99.1, SEC 2026-11-18). Konsensus är inte verifierad. Kursen stängde på 222,78 (+1,05 %, 1,51x volym, dagslägsta 211,00), **0,03 % under MA200** (222,86). **Ingen kandidatpost:** kursen ligger under MA200 och konsensusjämförelsen saknas.
- **Krypto:** The Block rapporterade 2026-11-14 att de tolv amerikanska spot-ETF:erna för bitcoin tappat 1,91 mdr USD på sju raka handelsdagar. Flödet för 2026-11-17 och 2026-11-18 är **OKONTROLLERAT** (L-5). Websökets träffar för "18 november" är 2025 års data, med BTC runt 89 000. FXStreet (2026-11-19) beskriver kryptomarknaden som "subdued" efter det hökaktiga protokollet. `COIN` föll 3,92 % (110,51) och `MSTR` 6,40 % (90,32). Ingen bekräftad regulatorisk händelse eller protokollhändelse hittades i websök.

## Uppföljning av tidigare case

- `NVDA` (rapport-261118): 155,46 → 150,96 (−2,89 %, prices.json/Yahoo chart API, marketTime 2026-11-18T21:00:00Z). Det är den första post-event-stängningen. Rapporten slog förväntningarna på alla punkter, men aktien föll på 1,49x volym och ligger nu **25,9 % under MA200** (203,72). Tesen är **FÖRSVAGAD**. Fundamenten är oförändrade, men marknaden sålde utfallet, och trenden plus regimen blockerar en ny position.

**Kandidatkön (`state/scout_candidates.json`):** före körningen fanns 127 poster, varav 118 `rejected`, 9 `promoted` och **0 `new`**. **L-4:** `261118-NVDA` avvisades 2026-11-18 delvis på ett tillfälligt datavillkor, eftersom kursen inte var verifierbar efter katalysatorn. Villkoret har nu upphört: 150,96 är en post-event-stängning. Avvisningen vilar dock också på två spärrar som inte är tillfälliga, regimen av och kursen under MA200. Båda gäller fortfarande. L-4 utlöser därför ingen ny post. **En ny post i dag:** `261119-TGT` (`status: new`, `price` 165,93, `priceAsOf` 2026-11-18T21:03:24Z, alltså post-event).

**US-boken (läses, ändras inte):** `CBOE` stängde på 359,91 (−2,75 %, dagslägsta 359,83, marketTime 2026-11-18T21:00:00Z). Det är **2,40 % över stoppen 351,50** och 5,9 % under målet 382,50. Sleeven är `SPY` 730,20.

## Dagens case
### Case 1: Target (TGT / NYSE)
**Katalysator:** Q3 2026 rapporterades 2026-11-18 före öppning. Försäljningen ökade 7,1 % till 27,1 mdr, jämförbar försäljning +5,6 % och trafiken +5 %. Justerad EPS var 2,65 mot 2,07 väntat, och helårsguiden för försäljningen höjdes till cirka +6 % (CNBC 2026-11-18; Target 8-K ex. 99, SEC 2026-11-18). Utfallet har inträffat och är bekräftat. Pressmeddelandets brödtext lästes inte direkt, se åtgärdspunkt 4.
**Bull case:** Det är tredje kvartalet i rad med tillväxt och den starkaste försäljningen på fem år, driven av trafik och inte bara av pris. Guiden höjdes in i julkvartalet, och ledningen säger att handeln börjat bra. HD föll 17/11 på sin rapport medan TGT steg på sin, så det här är bolagsspecifik styrka, inte sektorvind. Trenden är intakt: kursen ligger **20,7 % över MA200** (137,52) och 6,1 % över MA50 (156,39), och volymen var 3,14x snittet på reaktionsdagen.
**Bear case:** **Regimfiltret i US-boken är AV** (`^GSPC` 0,31 % under MA200). Det blockerar en ny aktieposition oavsett caset. EPS-överraskningen är till stor del en engångspost: utan tullåterbetalningen på 0,50 USD blir justerad EPS cirka 2,15 mot 2,07 väntat, ett betydligt mindre slag. Aktien är enligt CNBC upp över 70 % i år, så mycket är redan inprisat. Aktien gav tillbaka mer än hälften av intradagsuppgången (högsta 171,91, stängning 165,93). Konsumenten pressas av höjningsförväntningar, och WMT:s rapport i dag kan flytta hela sektorn. Det är en binär händelse för jämförelsen men inte för TGT självt.
**Setup:** Den reguljära stängningen 165,93 (marketTime 2026-11-18T21:03:24Z, prices.json/Yahoo chart API) ligger **efter** katalysatorn, så den är en post-event-kurs. Föregående stängning var 159,53, MA50 156,39, MA200 137,52 och volymen 3,14x 20-dagarssnittet (`state/volume_history.json`). Värderingstal är inte hämtade. Ingen rapport i `earnings_calendar.json`:s fönster för TGT. Ansvarig bok (US) ska pröva samtliga fem grindar. Med regimen av blir utfallet en avvisning, men den ska namnges och loggas som kontrafaktiskt underlag. Stänger `^GSPC` över MA200 inom kandidatens giltighet (t.o.m. 2026-11-27) faller den spärren. Kursen ska då prövas mot RSI och nåbarhet efter uppgången, inte köpas på gapet.

Inga fler case i dag. Ett starkt case kräver en bekräftad katalysator och en kurs som regimfiltret tillåter. US-bokens regim är fortsatt av, Nvidias bekräftade rapport fick en negativ reaktion, LOW stängde under MA200 och ANT saknar kurshistorik. WMT och ROST är väntade event och därmed bevakningsposter enligt punkt 8. Skälen till avvaktan står under Makro nedan.

## Makro- & sektorfaktorer att bevaka

- **Regimen (VIKTIGAST för US-boken):** `^GSPC` 7 323,63 mot MA200 7 346,53 är 0,31 % under, andra stängningen under. Intradag handlades index över MA200 (högsta 7 367,68), men regeln läser stängningen. Rotationen 15:00 CET läser alltså regimen som AV.
- **Räntor och dollar:** Protokollet bekräftar att en höjning i december är huvudscenariot, med en minoritet för +50 bp. Det är motvind för långdurationstillgångar, tillväxtaktier och krypto. Varningen för AI-relaterad skuldsättning är en ny riskfaktor för sektorn. Räntenivåer och DXY är inte verifierade ur state (åtgärdspunkt 3).
- **AI och halvledare:** Nvidia sålde av trots rapporten, och ANT-noteringen tar i dag cirka 81 mdr USD ur marknaden. `NVDA` (−25,9 % mot MA200), `TSM` (−10,1 %) och `AVGO` (−3,7 %, men +3,64 % i går) ligger alla under MA200. Inga köpbara setups förrän trenderna har reparerats.
- **Krypto:** BTC och ETH ligger 14–17 % under MA200 och fortsätter nedåt. `COIN` och `MSTR` ligger 32–36 % under. Höjningsförväntningarna, ETF-utflöden och svag riskaptit pekar åt samma håll. Inget kryptocase görs.
- **Konsument:** Bilden är splittrad. TGT steg på stark trafik, LOW steg svagt och HD föll i förrgår. WMT i dag och ROST i kväll avgör veckans konsumentbild. `WMT` (+7,0 % mot MA200) och `ROST` (+1,1 %) har intakta trender, men rapportdagarna köps aldrig in i (punkt 8).
- **Varför marknaden är avvaktande:** Index har stängt under MA200 två dagar i rad, Fed signalerar höjning och sektorns starkaste rapport (NVDA) blev en säljsignal. Det enda starka caset (TGT) är blockerat av regimen. Bevakning är rätt läge tills index återtagit MA200.

**Watchlist-hygien:** `config/watchlist_us.txt` innehåller långt fler än 25 symboler, men ingen rensning görs. Följande skyddas enligt `prompts/gemensam_korning.md`: innehavet (`CBOE`), sleeven och indexen, kandidaterna inom `expiresAt` (`TGT`, `NVDA`, `BIIB`, `AMAT`, `APP` med flera), rapportbolagen inom 10 handelsdagar, besluten från rotationen 2026-11-16 inom 20-dagarsfönstret och `ANT` (noteras i dag). `TGT`, `LOW` och `NVDA` finns redan i listan. Inga tillägg.

### Åtgärdspunkter till Dren (L-3)

1. **`crypto-previousclose-misdated` – ÅTERKOMMANDE.** `quotes["BTC-USD"].previousClose` (64 893,95) och `quotes["ETH-USD"].previousClose` (1 822,96) motsvarar ingen daterad punkt i `state/price_history.json` (2026-11-18: 62 510,27 respektive 1 768,63). Mot `previousClose` blir rörelsen −3,54 % och −2,89 %, mot den daterade punkten +0,14 % och +0,09 %. **Omfång:** 2 av 2 mynt. **Ersättningskälla:** `state/price_history.json`.
2. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** `feeds.globenewswire` och `feeds.globenewswire-earnings` ger fortfarande `"HTTP 403 – båda försöken (0.0 s)"`. **Omfång:** 2 av 6 flöden. **Ersättningskälla:** websök, prnewswire, mfn och SEC 8-K.
3. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas i `state/prices.json`. Jobless claims-konsensus, bostadsbyggandet och räntenivåerna kunde därför inte anges. **Omfång:** samtliga makrovärden.
4. **`scout-cannot-fetch-press-release-body` – ÅTERKOMMANDE.** Primärdokumenten (Target 8-K ex. 99, Lowe's 8-K ex. 99.1) är hämtade ur sökresultatens sammanfattningar och inte lästa direkt. **Omfång:** varje case som bygger på ett pressmeddelande, i dag 1 av 1. **Förslag:** tillåt `sec.gov` och `prnewswire.com` i miljöns nätverkspolicy.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
