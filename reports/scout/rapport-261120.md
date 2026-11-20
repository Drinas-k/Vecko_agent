# Daglig Scout: USA & Krypto
**Datum:** 2026-11-20
**Marknadsklimat:** Torsdagen blev en kraftig vändning nedåt. `^GSPC` handlades upp till 7 415,64, över MA200, men stängde **−2,02 % på 7 175,83**, 2,34 % under MA200. Det är tredje stängningen i rad under, och US-bokens regimfilter är fortsatt **AV**. Anthropic (`ANT`) öppnade 34 % över IPO-priset men föll tillbaka till 97,17. AMD föll 7,7 % på en blankarrapport, och Intuit och Ross föll efterbörs på svaga prognoser. BTC (61 539,57) och ETH (1 739,34) ligger 15–18 % under MA200. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (kandidatkön kontrollerad), L-5 (negativa påståenden avgränsade till genomsökta källor, `INTU` tillagd i watchlist) och L-6 (krypto täcks enligt `config/fokus_scout.md`). L-1, L-2, L-7, L-8 och L-9 gäller inte scouten.

## Marknadsöversikt

`git pull` kördes 2026-11-20 05:48 UTC (06:48 CET). HEAD = `origin/main` = `97782b5`. Källan är `state/prices.json` med `generatedAt` 2026-11-20T02:19:11Z, `schemaVersion` 2026-08-02-prevclose, `tickerCount` 330 och `okCount` 325 (Yahoo Finance chart API via GitHub Actions). Aktiekurserna är torsdagens stängning. Nyhetsflödet (`state/news_feed.json`) har `generatedAt` 2026-11-19T22:40:48Z och täcker **10 av 10 handelsdagar** (2026-11-06 – 2026-11-19, `missingDays` tomt).

| Symbol | Nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 7 175,83 | −2,02 % (7 323,63 → 7 175,83) | 2026-11-19T21:59:18Z |
| `^IXIC` | 23 879,20 | −2,25 % (24 429,88 → 23 879,20) | 2026-11-19T22:15:59Z |
| `BTC-USD` | 61 539,57 | −1,69 % mot gårdagens rapport (62 595,96); −0,73 % mot daterad punkt 2026-11-19 (61 989,68) | 2026-11-20T02:17:37Z |
| `ETH-USD` | 1 739,34 | −1,75 % mot gårdagens rapport (1 770,24); −0,97 % mot daterad punkt 2026-11-19 (1 756,36) | 2026-11-20T02:17:58Z |
| `SPY` (sleeve) | 715,87 | −1,96 % (730,20 → 715,87) | 2026-11-19T21:00:00Z |

Kryptorörelserna är räknade mot gårdagens rapport och mot daterade punkter i `state/price_history.json`, inte mot `previousClose` (se åtgärdspunkt 1).

**Teknik** (räknad på råserien i `state/price_history.json`, sista aktiepunkt 2026-11-19):
- `^GSPC` ligger **2,34 % UNDER MA200** (7 347,99). Det är tredje stängningen under, och **regimfiltret för US-boken är AV**. Dagsintervallet var 7 173,63–7 415,64, så index stängde nära dagslägsta efter att ha handlats 0,9 % över MA200 intradag. Det är en vändning nedåt, inte ett test som höll. Index ligger 6,1 % under MA50 (7 640,19). Reuters anger att det är sjätte förlustdagen i rad. `SPY` ligger 2,30 % under sin egen MA200 (732,69).
- `^IXIC` ligger **5,08 % under MA200** (25 157,04) och 8,8 % under MA50 (26 187,75).
- `BTC-USD` ligger **14,91 % under MA200** (72 323,90) och 21,8 % under MA50 (78 697,34). `ETH-USD` ligger **17,89 % under MA200** (2 118,21).

## Ekonomiska siffror & kalender

**Senaste utfall:**
- **Jobless claims (tor 2026-11-19, 08:30 ET):** 203 000 nya ansökningar mot väntade 197 000 (WSJ-enkät). Föregående vecka var 202 000 efter revidering. Fyraveckorssnittet är 197 750, och de fortsatta ansökningarna steg med 70 000 till 1,763 miljoner (Breitbart/AP 2026-11-19; FXTribune 2026-11-19; Admiral Markets 2026-11-19). Nivån är fortsatt låg, och siffran ändrar inte bilden av en stram arbetsmarknad som stödjer en höjning i december.
- **Philly Fed (tor 2026-11-19):** indexet föll till sexmånaderslägsta medan prices paid steg (mlq.ai 2026-11-19). Utfall och förväntan är **EJ VERIFIERADE** i siffror.
- **FOMC-protokollet (ons 2026-11-18) – fortfarande veckans mest marknadsrörande:** "nearly all" ledamöter väntar sig +25 bp i december (CNBC 2026-11-18, se rapport-261119).
- **KPI oktober (2026-11-10):** total +0,4 % och kärna +0,3 % m/m, båda 0,1 pp över förväntan. **PPI oktober (2026-11-13):** +0,3 % mot väntade +0,4 %.

**Kommande (nästa 1–5 handelsdagar):**
- **Fre 2026-11-20 (i dag):** University of Michigan, slutligt konsumentförtroende för november. Konsensus är **EJ VERIFIERAD**.
- **Mån 2026-11-23:** `HPE` rapporterar. **Tis 2026-11-24:** `CLSK` (gissat datum, `isEstimate: true`). **Ons 2026-11-25:** `DE`.
- **Tor 2026-11-26:** Thanksgiving, börsen stängd. **Fre 2026-11-27:** halvdag.
- **FOMC 8–9/12** ligger utanför fönstret. **Mest marknadsrörande** närmast är PCE för oktober. Datumet är **EJ VERIFIERAT** ur state.

**Rapporter nästa 10 handelsdagar** ur `state/earnings_calendar.json` (`generatedAt` 2026-11-20T02:17:22Z, `errors` tomt), US-symboler i `config/watchlist_us.txt`:
- **11-23:** `HPE`. **11-24:** `CLSK` (gissat). **11-25:** `DE`. **12-01:** `MRVL`. **12-02:** `CBRL`, `FIVE`, `ZS`. **12-03:** `COO`, `S`.

**L-5:** Kalendern omfattar bara de symboler som `prices.yml` hämtar. Resten av det amerikanska universumet är **OKONTROLLERAT**. Ett exempel är `INTU`, som rapporterade i går utan att finnas i kalendern. Det fångades via SEC 8-K i `news_feed.json` (2026-11-19T22:26Z) och websök, och symbolen läggs nu i watchlisten. Alla datum ovan är bevakningsposter enligt punkt 8, aldrig köpförslag.

## Aktuella händelser & katalysatorer

- **Anthropic (`ANT`) debuterade på Nasdaq 2026-11-19.** IPO-priset var 83 USD. Första handel skedde på 111,50 (+34 %), men kursen föll tillbaka till **97,17** (+17,1 % mot IPO-priset) med dagsintervallet 92,72–115,10 och 851,8 miljoner omsatta aktier (prices.json/Yahoo chart API, marketTime 2026-11-19T21:00:01Z; Reuters via Investing.com 2026-11-19, "Wall Street ends sharply lower as Anthropic's debut fails to revive AI fervor"; TradingKey 2026-11-19). Källorna anger något olika stängningskurser, och kursen ovan är den ur state. Aktien har en enda historikpunkt och saknar MA200, vilket blockerar en ny position per definition. **Ingen kandidatpost.**
- **Bred AI- och marknadsförsäljning, 2026-11-19:** Dow −2,19 % till 49 097,06, första stängningen under 50 000 sedan juni (CNBC 2026-11-19). Halvledarindexet SOX föll 2,4 % och VIX nådde nära 29 intradag (Reuters/CNBC 2026-11-19). VIX och SOX är **inte verifierade ur state** (åtgärdspunkt 3). `NVDA` föll 3,30 % till 145,98, den sjätte förlustdagen i rad.
- **AMD (`AMD`) föll 7,72 % till 489,19 på en blankarrapport, 2026-11-19.** Dagsintervallet var 470,56–555,01, alltså öppning upp och tvärvändning, och volymen var 1,93x snittet (marketTime 2026-11-19T21:00:01Z). Hunterbrook Media påstår att AMD:s firmware förekommit hos den svartlistade kinesiska servertillverkaren IEIT Systems. Hunterbrook Capital har uppgett att man är kort i AMD. AMD tillbakavisar anklagelserna (CNBC 2026-11-19, "AMD stock dives on short-seller report of alleged China exposure"). Påståendena är obekräftade, och en blankarrapport är en negativ katalysator. **Ingen kandidatpost.** Kursen ligger fortsatt 14,1 % över MA200 (428,63) men 11,8 % under MA50.
- **Walmart (`WMT`) Q3 FY27, 2026-11-19 före öppning, BEKRÄFTAT:** intäkterna steg 5,2 % till 188,8 mdr USD mot väntade 187,2 mdr. Justerad EPS var 0,65 mot 0,64. Global e-handel ökade 17 % och utgör nu 24 % av försäljningen. Helårsguiden höjdes för tredje gången i år, till justerad EPS 2,84–2,89 (tidigare 2,80–2,87) och försäljningstillväxt 4,9–5,2 % (Proactive Investors 2026-11-19; Supermarket News 2026-11-19; Benzinga 2026-11-19). Aktien stängde på 126,04 (−1,04 %, volym 1,43x). Den föll alltså mindre än index. → Case 1 och kandidatpost `261120-WMT`.
- **Intuit (`INTU`), efter stängning 2026-11-19, BEKRÄFTAT negativt:** prognosen för innevarande kvartal är justerad EPS 3,17–3,22 mot väntade 3,73 (FactSet). Aktien föll cirka 13 % efterbörs (CNBC 2026-11-19, "Stocks making the biggest moves Thursday"). `INTU` saknas i `state/prices.json`, så rörelsen är **KURS EJ VERIFIERAD**. Symbolen läggs i `config/watchlist_us.txt` för att mäta reaktionen (L-5). **Ingen kandidatpost**, eftersom katalysatorn är negativ.
- **Ross Stores (`ROST`), efter stängning 2026-11-19:** EPS var 1,91 mot cirka 1,87 väntat, men intäkterna på 6,26 mdr USD var något under förväntan. Q4-guiden för EPS, 2,16–2,25, ligger under konsensus på cirka 2,27 (Benzinga 2026-11-19; GuruFocus 2026-11-19). Uppgifterna om efterbörsfallet varierar mellan 5 och 10 %, och rörelsen är inte verifierad ur state. Den reguljära stängningen 219,88 (−3,41 %) är pre-event och ligger 2,5 % under MA200 (225,42). **Ingen kandidatpost.**
- **Krypto:** inga bekräftade ETF-flödessiffror för 2026-11-18 eller 2026-11-19 hittades (L-5: avser websök 05:55 UTC). `COIN` föll 1,48 % (108,87) och `MSTR` 4,64 % (86,13). Ingen regulatorisk händelse eller protokollhändelse hittades.

## Uppföljning av tidigare case

- `TGT` (rapport-261119): 165,93 → 167,46 (+0,92 %, prices.json/Yahoo chart API, marketTime 2026-11-19T21:02:00Z). Aktien steg på en dag då index föll 2 %, med dagsintervallet 165,04–169,77 och volymen 1,34x. Den ligger **21,5 % över MA200** (137,78) och nära 250-dagarshögsta (169,89). Tesen är **INTAKT**. Kandidaten `261119-TGT` avvisades 2026-11-19 på spärr (c), regimen av. Den spärren gäller fortfarande, och skillnaden mot MA200 har ökat.

**Kandidatkön (`state/scout_candidates.json`):** före körningen fanns 128 poster, varav 119 `rejected`, 9 `promoted` och **0 `new`**. **L-4:** `261118-NVDA` och `261119-TGT` vilar båda på regimspärren, som är ett omdömes- och marknadsvillkor och inte en datalucka. Ingen ny prövning utlöses. **En ny post i dag:** `261120-WMT` (`status: new`, `price` 126,04, `priceAsOf` 2026-11-19T21:00:01Z). Rapporten kom före öppning, så den reguljära stängningen är en post-event-kurs.

**US-boken (läses, ändras inte):** `CBOE` stängde på 357,69 (−0,62 %, dagsintervall 354,08–360,06, marketTime 2026-11-19T21:00:00Z). Det är **1,76 % över stoppen 351,50**, och dagslägsta låg 0,73 % över stoppen. Avståndet till målet 382,50 är 6,9 %. Sleeven är `SPY` 715,87.

## Dagens case
### Case 1: Walmart (WMT / NASDAQ)
**Katalysator:** Q3 FY27 rapporterades 2026-11-19 före öppning. Intäkterna var 188,8 mdr (+5,2 %) mot 187,2 väntat, och justerad EPS 0,65 mot 0,64. E-handeln ökade 17 %. Helårsguiden höjdes för tredje gången i år, till EPS 2,84–2,89 från 2,80–2,87 (Proactive Investors, Supermarket News, Benzinga, samtliga 2026-11-19). Utfallet har inträffat och är bekräftat. Pressmeddelandets brödtext lästes inte direkt (åtgärdspunkt 4).
**Bull case:** Walmart vinner andelar även bland höginkomsthushåll, och e-handel, annonsintäkter och medlemsavgifter driver marginalen uppåt. Det är tredje guidehöjningen i år. I en marknad som säljer av AI-namn är WMT en defensiv kvalitetstillväxtaktie. På reaktionsdagen föll aktien bara 1,04 % när index föll 2,02 %. Trenden är intakt: kursen ligger **5,9 % över MA200** (118,99) och 8,4 % över MA50 (116,23).
**Bear case:** **Regimfiltret i US-boken är AV** (`^GSPC` 2,34 % under MA200), vilket blockerar en ny aktieposition oavsett caset. Överraskningen är liten (EPS +0,01 mot konsensus), och aktien handlas till cirka 45 gånger vinsten, så det finns lite utrymme för besvikelse (MarketBeat 2026-11-19). Marknaden svarade med en nedgång, inte en uppgång. Aktien ligger 6,1 % under 250-dagarshögsta (134,20). Ross och Intuit visar samtidigt att framåtblickande prognoser straffas hårt.
**Setup:** Den reguljära stängningen 126,04 (marketTime 2026-11-19T21:00:01Z, prices.json/Yahoo chart API) ligger **efter** katalysatorn, så den är en post-event-kurs. Föregående stängning var 127,36, dagsintervallet 123,29–126,95, MA50 116,23 och MA200 118,99. Volymen var 1,43x 20-dagarssnittet (`state/volume_history.json`), och RSI(14, enkel) ligger på 56,2. Värderingstal är inte hämtade ur state. Ingen rapport i `earnings_calendar.json`:s fönster för WMT. Ansvarig bok (US) ska pröva samtliga fem grindar. Med regimen av blir utfallet en avvisning, men den ska namnges och loggas som kontrafaktiskt underlag. Stänger `^GSPC` över MA200 inom kandidatens giltighet (t.o.m. 2026-11-30) faller den spärren. Då måste volymkriteriet (1,43x mot kravet 1,5x) och nåbarheten prövas på nytt.

Inga fler case i dag. ANT saknar kurshistorik. AMD:s och INTU:s katalysatorer är negativa, och ROST stängde under MA200 med en svag prognos. Inget kryptonamn har en bekräftad positiv katalysator. Skälen till avvaktan står under Makro nedan.

## Makro- & sektorfaktorer att bevaka

- **Regimen (VIKTIGAST för US-boken):** `^GSPC` 7 175,83 ligger 2,34 % under MA200 (7 347,99), tredje stängningen under. Torsdagens vändning från 7 415,64 visar att MA200 nu fungerar som motstånd. Rotationen 15:00 CET läser regimen som AV.
- **Räntor och dollar:** Fed väntas höja i december. Claims på 203 000 och stigande prices paid i Philly Fed stödjer det scenariot. Det är motvind för långdurationstillgångar, tillväxtaktier och krypto. Räntenivåer, DXY och VIX är inte verifierade ur state (åtgärdspunkt 3).
- **AI och halvledare:** Anthropic-noteringen gav inte sektorn nytt liv, och utbudet på cirka 81 mdr USD drog likviditet. AMD:s blankarrapport lade till en Kina- och exportkontrollsrisk. `NVDA` (−28,3 % mot MA200), `TSM` (−12,8 %) och `AVGO` (−5,8 %) ligger alla under MA200. Inga köpbara setups förrän trenderna har reparerats.
- **Mjukvara:** Intuits svaga prognos (−13 % efterbörs) kan dra med sig sektorn i dag. Det är en motvind för mjukvarunamn med hög multipel.
- **Krypto:** BTC och ETH ligger 15–18 % under MA200 och fortsätter nedåt. `COIN` och `MSTR` ligger 35–37 % under. Inget kryptocase görs.
- **Konsument:** TGT och WMT visar styrka, medan ROST, LOW och HD är svagare. Kvalitetsnamnen inom dagligvaruhandeln håller bäst.
- **Varför marknaden är avvaktande:** Index har tvärvänt nedåt vid MA200 och stängt tre dagar i rad under den. Sex raka förlustdagar, en väntad räntehöjning och en AI-försäljning trots Nvidias rapport och Anthropics notering pekar åt samma håll. De två starka konsumentcasen (TGT, WMT) blockeras av regimen. Bevakning är rätt läge tills index återtagit MA200.

**Watchlist-hygien:** `config/watchlist_us.txt` innehåller långt fler än 25 symboler, men ingen rensning görs. Följande skyddas enligt `prompts/gemensam_korning.md`: innehavet (`CBOE`), sleeven och indexen, kandidaterna inom `expiresAt` (`WMT`, `TGT`, `NVDA` med flera), rapportbolagen inom 10 handelsdagar, besluten från rotationen 2026-11-16 inom 20-dagarsfönstret och `ANT`. **Tillägg:** `INTU` (L-5, för att mäta rapportreaktionen).

### Åtgärdspunkter till Dren (L-3)

1. **`crypto-previousclose-misdated` – ÅTERKOMMANDE.** `quotes["BTC-USD"].previousClose` (62 987,27) och `quotes["ETH-USD"].previousClose` (1 774,75) motsvarar ingen daterad punkt i `state/price_history.json` (2026-11-19: 61 989,68 respektive 1 756,36). Mot `previousClose` blir rörelsen −2,30 % och −2,00 %, mot den daterade punkten −0,73 % och −0,97 %. **Omfång:** 2 av 2 mynt. **Ersättningskälla:** `state/price_history.json`.
2. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** `feeds.globenewswire` och `feeds.globenewswire-earnings` ger fortfarande `"HTTP 403 – båda försöken (0.1 s)"`. **Omfång:** 2 av 6 flöden. **Ersättningskälla:** websök, prnewswire, mfn och SEC 8-K.
3. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas i `state/prices.json`. VIX nära 29 och SOX −2,4 % kunde därför bara anges ur nyhetskällor, och räntenivåerna, Philly Fed-siffran och Michigan-konsensus inte alls. **Omfång:** samtliga makrovärden.
4. **`scout-cannot-fetch-press-release-body` – ÅTERKOMMANDE.** Primärdokumenten (Walmart 8-K, Intuit 8-K 2026-11-19) är hämtade ur sökresultatens sammanfattningar och inte lästa direkt. **Omfång:** varje case som bygger på ett pressmeddelande, i dag 1 av 1. **Förslag:** tillåt `sec.gov` och `prnewswire.com` i miljöns nätverkspolicy.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
