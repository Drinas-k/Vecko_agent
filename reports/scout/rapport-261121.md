# Daglig Scout: USA & Krypto
**Datum:** 2026-11-21
**Marknadsklimat:** Fredagen var veckans värsta dag. `^GSPC` föll **−3,70 % till 6 910,39**, sjunde förlustdagen i rad, och ligger nu **5,96 % under MA200**. Nasdaq föll −5,28 %, och NVDA föll −14,01 % efter att Reuters rapporterat om en SEC-utredning av bolagets redovisning. US-bokens regimfilter är fortsatt **AV**. BTC (58 959,74) och ETH (1 624,60) ligger 18–23 % under MA200. Det är lördag och börserna är stängda, så aktiekurserna nedan är fredagens stängning. **Aktiva lärdomar tillämpade:** L-3 (åtgärdspunkter sist), L-4 (kandidatkön kontrollerad), L-5 (negativa påståenden avgränsade till genomsökta källor, `PAYO` tillagd i watchlist) och L-6 (krypto täcks enligt `config/fokus_scout.md`). L-1, L-2, L-7, L-8 och L-9 gäller inte scouten.

## Marknadsöversikt

`git pull` och `git fetch origin main` kördes 2026-11-21 cirka 05:48 UTC (06:48 CET). `origin/main` = `080c81a`. Källan är `state/prices.json` med `generatedAt` 2026-11-21T02:13:44Z, `schemaVersion` 2026-08-02-prevclose, `tickerCount` 331 och `okCount` 326 (Yahoo Finance chart API via GitHub Actions). Nyhetsflödet (`state/news_feed.json`) har `generatedAt` 2026-11-20T22:15:20Z och täcker **10 av 10 handelsdagar** (2026-11-09 – 2026-11-20, `missingDays` tomt).

| Symbol | Nivå | Rörelse | marketTime |
|---|---|---|---|
| `^GSPC` | 6 910,39 | −3,70 % (7 175,83 → 6 910,39) | 2026-11-20T21:35:54Z |
| `^IXIC` | 22 617,73 | −5,28 % (23 879,20 → 22 617,73) | 2026-11-20T22:15:59Z |
| `BTC-USD` | 58 959,74 | −4,19 % mot gårdagens rapport (61 539,57); +0,14 % mot daterad punkt 2026-11-20 (58 879,38) | 2026-11-21T02:11:46Z |
| `ETH-USD` | 1 624,60 | −6,60 % mot gårdagens rapport (1 739,34); +0,66 % mot daterad punkt 2026-11-20 (1 614,00) | 2026-11-21T02:12:20Z |
| `SPY` (sleeve) | 689,81 | −3,64 % (715,87 → 689,81) | 2026-11-20T21:00:04Z |

Kryptorörelserna är räknade mot gårdagens rapport och mot daterade punkter i `state/price_history.json`, inte mot `previousClose` (se åtgärdspunkt 1).

**Teknik** (räknad på råserien i `state/price_history.json`, sista aktiepunkt 2026-11-20):
- `^GSPC` ligger **5,96 % UNDER MA200** (7 348,55). Det är fjärde stängningen i rad under, och **regimfiltret för US-boken är AV**. Dagsintervallet var 6 882,66–7 198,67, och index stängde nära dagslägsta. Index ligger 9,4 % under MA50 (7 625,26). RSI(14, enkel) är 29,2, alltså översålt. Volymen var 1,42x 20-dagarssnittet. Motley Fool och Yahoo Finance anger att index stängde i en korrektion, mer än 10 % under rekordet 6/10, och att veckan gav −8,6 %, den sämsta veckan sedan april 2025 (2026-11-20). `SPY` ligger 5,86 % under sin MA200 (732,76) på volym 2,94x.
- `^IXIC` ligger **10,09 % under MA200** (25 157,42) och 13,4 % under MA50 (26 113,44). Enligt Motley Fool (2026-11-20) är Nasdaq nu negativt för 2026.
- `BTC-USD` ligger **18,36 % under MA200** (72 219,77) och 24,5 % under MA50 (78 096,91). RSI(14) ligger på 2,7, vilket är extremt översålt men i sig inte en köpsignal. `ETH-USD` ligger **23,14 % under MA200** (2 113,60).

## Ekonomiska siffror & kalender

**Senaste utfall:**
- **University of Michigan, slutligt konsumentförtroende november (fre 2026-11-20, 10:00 ET):** utfallet är **EJ VERIFIERAT**, eftersom websök inte gav någon träff på den slutliga siffran. Den preliminära siffran var 51,0 (från 48,0 i oktober), ett tremånadershögsta över förväntan (StockAnalysis 2026-11; TheStreet Pro 2026-11).
- **Jobless claims (tor 2026-11-19):** 203 000 mot väntade 197 000 (WSJ-enkät; se rapport-261120).
- **FOMC-protokollet (ons 2026-11-18):** "nearly all" ledamöter väntar sig +25 bp i december (CNBC 2026-11-18).
- **KPI oktober (2026-11-10):** total +0,4 % och kärna +0,3 % m/m, båda 0,1 pp över förväntan. **PPI oktober (2026-11-13):** +0,3 % mot väntade +0,4 %.
- **Räntor:** den senaste verifierbara uppgiften är 10-åringen på 5,118 % och 2-åringen på 4,806 % (RootData, veckan som började 2026-11-17). Fredagens nivå är **EJ VERIFIERAD** (åtgärdspunkt 3).

**Kommande (nästa 1–5 handelsdagar):**
- **Mån 2026-11-23:** `HPE` rapporterar. Aktien föll redan −10,07 % i fredags till 40,91, 4,2 % under MA200 (42,71).
- **Tis 2026-11-24:** `CLSK` (inte längre märkt `isEstimate` i kalendern).
- **Ons 2026-11-25:** `DE`.
- **Tor 2026-11-26:** Thanksgiving, börsen stängd. **Fre 2026-11-27:** halvdag.
- PCE för oktober och BNP-revisionen väntas runt Thanksgiving, men datumen är **EJ VERIFIERADE** ur state. **Mest marknadsrörande** närmast är ändå om SEC-frågan kring Nvidia eskalerar, och därefter PCE. FOMC 8–9/12 ligger utanför fönstret.

**Rapporter nästa 10 handelsdagar** ur `state/earnings_calendar.json` (`generatedAt` 2026-11-21T02:11:10Z, `errors` tomt), US-symboler i `config/watchlist_us.txt`:
- **11-23:** `HPE`. **11-24:** `CLSK`. **11-25:** `DE`. **12-01:** `MRVL`. **12-02:** `CBRL`, `FIVE`, `ZS`. **12-03:** `COO`, `S`.

**L-5:** Kalendern omfattar bara de symboler som `prices.yml` hämtar. Resten av det amerikanska universumet är **OKONTROLLERAT**. Alla datum ovan är bevakningsposter enligt punkt 8, aldrig köpförslag.

## Aktuella händelser & katalysatorer

- **SEC utreder Nvidias redovisning, 2026-11-20.** Reuters rapporterade, med hänvisning till två personer som informerats, att SEC:s enforcement-avdelning granskar möjliga redovisningsfrågor hos Nvidia. Det framgår inte när utredningen inleddes (Bloomberg 2026-11-20, "Wall Street Regulator Probes Nvidia Accounting, Reuters Says"; The Daily Star/Reuters). Inget 8-K eller uttalande från bolaget hittades. ⚠️ **RYKTE – EJ BEKRÄFTAT (Reuters via Bloomberg, 2026-11-20).** Reuters nämner också att justitiedepartementet granskar Nvidias köp av Hugging Face för 12,9 mdr USD. `NVDA` föll **−14,01 % till 125,53**, sjunde förlustdagen i rad, med dagsintervallet 124,50–143,72 och volymen 2,48x (marketTime 2026-11-20T21:00:01Z). Aktien ligger 38,3 % under MA200 (203,35). **Ingen kandidatpost**, eftersom katalysatorn är negativ. Den befintliga kandidaten `261118-NVDA` (avvisad) påverkas inte.
- **AI-utförsäljningen breddades, 2026-11-20:** `AVGO` −12,19 % (304,41), `AMD` −13,25 % (424,39, nu 1,3 % under MA200 429,79), `MU` −13,89 %, `TSM` −9,48 %, `MRVL` −11,69 %. Anthropic (`ANT`) föll −8,50 % till 88,91, men ligger fortfarande 7,1 % över IPO-priset 83. VIX steg 26,2 % till **35,89**, ett nytt 52-veckorshögsta (The Wall Street Republic 2026-11-20; Motley Fool 2026-11-20). VIX är **inte verifierat ur state** (åtgärdspunkt 3). Dow föll −1,9 % till 48 147,33 (Motley Fool 2026-11-20).
- **Defensiva namn höll emot:** av 149 US-symboler med fredagskurs i `state/prices.json` steg bara ett tjugotal. `UNH` steg +2,84 %, `WMT` +1,52 % (volym 1,91x), `JNJ` +1,25 %, `PG` +0,91 % och `COST` +0,76 %. Ingen ny bolagsspecifik katalysator för dem hittades i websök. Den genomsökningen gäller **bara de symboler som hämtas**, och resten av marknaden är OKONTROLLERAD (L-5).
- **Payoneer (`PAYO`), 2026-11-20 22:02 UTC efter stängning, BEKRÄFTAT:** bolaget meddelar att OCC gett villkorat godkännande för att bilda en nationell trustbank för stablecoins (PR Newswire, rubrik i `state/news_feed.json`). Ansökan om PAYO Digital Bank, N.A., som ska ge ut PAYO-USD, lämnades 2026-02-24 (The Block 2026-02-24). Brödtexten kunde inte läsas (åtgärdspunkt 4). → Case 1 och kandidatpost `261121-PAYO`.
- **Krypto:** BTC fortsatte nedåt med AI-försäljningen. `COIN` föll −6,34 % (101,97), `MSTR` −9,67 % (77,80), `MARA` −18,64 %, `IREN` −17,97 % och `CLSK` −16,27 %. Miners med AI-compute-exponering föll mest. Inga bekräftade ETF-flödessiffror för 2026-11-19 eller 2026-11-20 hittades (L-5: avser websök 05:55 UTC 2026-11-21).

## Uppföljning av tidigare case

- `WMT` (rapport-261120): 126,04 → 127,95 (**+1,52 %**, prices.json/Yahoo chart API, marketTime 2026-11-20T21:00:00Z) på en dag då index föll 3,70 %. Dagsintervallet var 127,22–130,52 och volymen 1,91x. Aktien ligger 7,5 % över MA200 (118,99) och har RSI 50,7. Tesen är **INTAKT** och stärkt av den relativa styrkan. Kandidaten `261120-WMT` avvisades 2026-11-20 på spärr (c), regimen av. Spärren gäller fortfarande, och `^GSPC` ligger nu ännu längre under MA200. Kandidaten giltig t.o.m. 2026-11-30.

**Kandidatkön (`state/scout_candidates.json`):** före körningen fanns 129 poster, varav 120 `rejected`, 9 `promoted` och **0 `new`**. **L-4:** `261117-BIIB` och `261118-NVDA` avvisades bland annat på "kurs ej verifierbar". Båda har numera post-event-kurser, men de bär också omdömesspärrar: BIIB grind 2, NVDA regim och MA200. Därför utlöses ingen omprövning som enbart beror på data. `261119-TGT` och `261120-WMT` vilar på regimspärren. **En ny post i dag:** `261121-PAYO` (`status: new`, `price: null`). Katalysatorn kom efter fredagens stängning och PAYO saknas i `prices.json`, så det finns ingen post-event-kurs. Symbolen läggs i `config/watchlist_us.txt`.

**US-boken (läses, ändras inte):** `CBOE` stängde på 357,71 (+0,01 %, dagsintervall 355,35–367,26, marketTime 2026-11-20T21:00:04Z). Det är **1,77 % över stoppen 351,50**, och dagslägsta låg 1,10 % över stoppen. Avståndet till målet 382,50 är 6,9 %. Sleeven är `SPY` 689,81.

## Dagens case
### Case 1: Payoneer (PAYO / NASDAQ)
**Katalysator:** Payoneer meddelade 2026-11-20 kl. 22:02 UTC, efter stängning, att OCC gett villkorat godkännande för att bilda en nationell trustbank för stablecoins (PR Newswire 2026-11-20, rubrik i `state/news_feed.json`). Ansökan om PAYO Digital Bank, N.A. lämnades 2026-02-24 (The Block 2026-02-24; PYMNTS 2026). Beskedet har inträffat och är bekräftat av bolaget, men villkoren i godkännandet har inte kunnat läsas.
**Bull case:** En federal trustbank låter Payoneer ge ut PAYO-USD, förvalta reserverna själv och erbjuda förvaring och växling till lokal valuta för sina gränsöverskridande B2B-kunder (The Block 2026-02-24). Det ger bolaget en egen avkastning på stablecoin-reserver och lägre kostnader mot partnerbanker. Konkurrenterna Circle, Paxos, BitGo och Stripes Bridge har redan fått motsvarande villkorade godkännanden (American Banker; The Block). Beskedet gör alltså att Payoneer inte längre ligger efter dem. Caset ligger inom fokusområdet kryptoinfrastruktur och stablecoins i `config/fokus_scout.md`.
**Bear case:** **Regimfiltret i US-boken är AV** (`^GSPC` 5,96 % under MA200), vilket blockerar en ny aktieposition oavsett case. Godkännandet är villkorat: kapital-, likviditets- och compliancekrav måste uppfyllas före start, och tidsplanen är okänd. Intäktseffekten ligger troligen flera kvartal bort. Beskedet kom på en dag med VIX nära 36 och kraftig försäljning av krypto- och tillväxtaktier, så en positiv reaktion kan drunkna i marknaden. Teknik och likviditet är okända eftersom PAYO saknar kursserie i state.
**Setup:** **KURS EJ VERIFIERAD.** `PAYO` saknas i `state/prices.json` och `state/price_history.json`, så nyckeltal, trend, MA200 och volym kan inte räknas ur state. Fredagens reguljära stängning hade dessutom legat **före** katalysatorn. Kandidaten läggs därför med `price: null`. `prices.yml` fyller i en post-event-kurs automatiskt när den kan hämtas, tidigast vid måndagens förbörs eller reguljära session. Ansvarig bok (US) ska pröva samtliga fem grindar. Med regimen av och utan kursserie blir utfallet en avvisning, men den ska namnges och loggas som kontrafaktiskt underlag. Ingen rapport i `earnings_calendar.json` för PAYO (symbolen bevakas inte där ännu, så detta är OKONTROLLERAT enligt L-5).

Inga fler case i dag. NVDA:s, AVGO:s och HPE:s katalysatorer är negativa. De defensiva namn som steg saknade en ny bekräftad katalysator, och WMT är redan en kandidat. Inget kryptonamn har en bekräftad positiv katalysator. Skälen till avvaktan står under Makro nedan.

## Makro- & sektorfaktorer att bevaka

- **Regimen (VIKTIGAST för US-boken):** `^GSPC` 6 910,39 ligger 5,96 % under MA200 (7 348,55), fjärde stängningen under. Index är i korrektion med sju raka förlustdagar och −8,6 % på veckan. Rotationen läser regimen som AV, och måndagens LÄGE A kommer att ha det som utgångspunkt.
- **Räntor och dollar:** Fed väntas höja i december, och 10-åringen låg nyligen över 5 %. Det är motvind för långdurationstillgångar, tillväxtaktier och krypto. Fredagens räntenivåer, DXY och VIX är inte verifierade ur state (åtgärdspunkt 3).
- **AI och halvledare:** sektorn bär hela nedgången. Nvidia har en ny redovisnings- och regulatorisk risk ovanpå VD-skiftet och DOJ-granskningen. AVGO, AMD, MU, TSM och MRVL föll 9–14 %. AMD har nu också fallit under MA200, så samtliga stora halvledarnamn i watchlisten ligger under MA200. Inga köpbara setups förrän trenderna har reparerats.
- **Krypto:** BTC och ETH ligger 18–23 % under MA200. Miners med AI-compute-exponering (IREN, MARA, CLSK, APLD) föll 16–19 % och tar alltså stryk från båda hållen. Inget kryptocase görs i dag. Payoneer är ett infrastrukturcase som inte beror på kryptopriset.
- **Defensivt:** dagligvaror och hälsovård (WMT, COST, PG, JNJ, UNH, KHC) steg på en −3,7 %-dag. Rotationen in i kvalitet och defensiva namn är tydlig.
- **Varför marknaden är avvaktande:** Index är i korrektion, VIX ligger på ett 52-veckorshögsta, AI-ledarna faller kraftigt på en regulatorisk risk och Fed väntas höja i december. Översålda lägen (RSI 29 för `^GSPC`, RSI 3 för BTC) kan ge studsar, men regimfiltret är byggt för att inte köpa dem. Bevakning är rätt läge tills index återtagit MA200.

**Watchlist-hygien:** `config/watchlist_us.txt` innehåller långt fler än 25 symboler (153 aktiva rader), men ingen rensning görs. Följande skyddas enligt `prompts/gemensam_korning.md`: innehavet (`CBOE`), sleeven och indexen, kandidaterna inom `expiresAt` (`WMT`, `TGT`, `NVDA`, `BIIB` med flera), rapportbolagen inom 10 handelsdagar, besluten från rotationen 2026-11-16 inom 20-dagarsfönstret och `ANT`. **Tillägg:** `PAYO` (kandidat `261121-PAYO`, saknade kurs, L-5).

### Åtgärdspunkter till Dren (L-3)

1. **`crypto-previousclose-misdated` – ÅTERKOMMANDE.** `quotes["BTC-USD"].previousClose` (61 901,82) och `quotes["ETH-USD"].previousClose` (1 755,19) motsvarar ingen daterad punkt i `state/price_history.json` (2026-11-20: 58 879,38 respektive 1 614,00). Mot `previousClose` blir rörelsen −4,75 % och −7,44 %, mot den daterade punkten +0,14 % och +0,66 %. **Omfång:** 2 av 2 mynt. **Ersättningskälla:** `state/price_history.json` och gårdagens rapport.
2. **`news-feed-globenewswire-http-403` – ÅTERKOMMANDE.** `feeds.globenewswire` och `feeds.globenewswire-earnings` ger fortfarande `"HTTP 403 – båda försöken (0.0 s)"`. **Omfång:** 2 av 6 flöden. **Ersättningskälla:** websök, prnewswire, mfn och SEC 8-K.
3. **`macro-calendar-not-verifiable-from-state` – ÅTERKOMMANDE.** `^TNX`, `^VIX`, `DX-Y.NYB`, `CL=F` och `^SOX` saknas i `state/prices.json`. VIX 35,89 kunde därför bara anges ur nyhetskällor, och räntenivåerna och Michigan-utfallet inte alls. **Omfång:** samtliga makrovärden.
4. **`scout-cannot-fetch-press-release-body` – ÅTERKOMMANDE.** `www.prnewswire.com` svarar 403 genom miljöns proxy, och sammanställningssajter (fool.com, stocktitan.net) går inte att slå upp. Payoneers pressmeddelande lästes därför bara som rubrik. **Omfång:** varje case som bygger på ett pressmeddelande, i dag 1 av 1. **Förslag:** tillåt `sec.gov` och `prnewswire.com` i miljöns nätverkspolicy.

Detta är automatiserat beslutsstöd, inte finansiell rådgivning.
