# Wave 1 Reply Tagging Cheatsheet — multi-llm-benchmark-dashboard

## Purpose

Minimalni operator pomucka pro prvni reply capture.

Nedelá novy routing.
Neresi novy research.
Jen zkracuje prvni logovani po reply do jednoho listu.

Pouziti:
- po prvni relevantni odpovedi
- pred zapsanim do `execution/OUTREACH-LOG-TEMPLATE.md`
- kdyz je potreba rychle normalizovat signal bez vymysleni vlastnich labelu

---

## Canonical labels only

### Reply quality
- `none` = zadna odpoved nebo jen seen
- `weak` = zdvorilostni reakce bez realneho signalu
- `relevant` = popsal problem, workflow nebo preference
- `high_intent` = chce call, sample pro vlastni use case, pricing nebo intro

### Preferred artifact
- `dashboard`
- `scorecard`
- `memo`
- `report`
- `API`
- `hybrid`
- `unknown`

### Status quo
- `spreadsheet` = spreadsheet / Notion / rucni compare tabulka
- `memo` = slides / deck / rucni report / interni memo
- `provider_native` = provider playground / provider dashboard / vendor-native compare
- `mixed` = kombinace vice workflow
- `unclear` = z reply to nejde poznat

### Status-quo break
- `speed` = chce rychlejsi rozhodnuti
- `shareable_output` = chce lepsi vystup pro management / klienta / tym
- `refreshability` = chce jednodussi refresh po zmene modelu nebo ceny
- `mixed`
- `unclear`

### Price probe
- `none`
- `under_39`
- `39_149`
- `149_plus`
- `enterprise`

### Pro signal
- `positive`
- `neutral`
- `negative`

---

## 30-second tagging flow

1. Je v reply realny signal?
   - ne -> `reply_quality = weak`
   - ano -> pokracuj

2. Co buyer pouziva dnes?
   - tabulka / Notion -> `status_quo = spreadsheet`
   - slides / memo / report -> `status_quo = memo`
   - provider UI / playground -> `status_quo = provider_native`
   - vic veci naraz -> `status_quo = mixed`

3. Co chce porazit?
   - pomalost -> `status_quo_break = speed`
   - rucni prepis do shareable vystupu -> `shareable_output`
   - potrebu opakovaneho refresh -> `refreshability`

4. Na co reaguje nejlip?
   - compare workflow -> `preferred_artifact = dashboard`
   - konkretni sample -> `scorecard`
   - obhajoba rozhodnuti -> `memo`

5. Je tam komercni signal?
   - jen zvedavost -> `pro_signal = neutral`
   - chce dalsi krok / pilot / pricing -> `positive`
   - chce jen free / jednorazovy artifact / nic platit -> `negative`

---

## Exact phrase prompts to capture

Po kazde reply zapsat 1 presnou vetu nebo frazi pro kazdou relevantni oblast:
- co pouzivaji dnes
- co je na tom otravne
- jaky format chteji videt
- jestli je tam pricing signal

Priklad zapisovych vet:
- "Dnes to mame v Notion tabulce." -> `status_quo = spreadsheet`
- "Problem je, ze to pak musim prepsat do decku." -> `status_quo_break = shareable_output`
- "Posli radsi sample scorecard." -> `preferred_artifact = scorecard`
- "Kdyby to bylo pro tym jako ongoing workspace, smysl by to davalo." -> `price_probe = 39_149` nebo `149_plus` podle kontextu

---

## High-intent triggers

Pouzij `reply_quality = high_intent`, kdyz buyer:
- chce call
- chce sample pro vlastni use case
- pta se na pricing
- pta se na workflow pro tym
- dela intro na dalsiho cloveka

---

## Anti-drift rules

- nevymyslet nove labely
- nepsat volne kategorie typu `doc`, `table`, `cool`, `maybe`
- kdyz je signal smiseny, pouzit `mixed` a detail dat do notes
- kdyz neni jasne nic, pouzit `unclear`, ne domyslet

---

## Source-of-truth

Tento cheatsheet jen zkracuje praci s existujici pravdou:
- `execution/OUTREACH-LOG-TEMPLATE.md`
- `execution/WAVE1-LIVE-EVIDENCE-BOARD.md`
- `execution/STATUS-QUO-DISPLACEMENT-PLAYBOOK.md`
- `execution/PRICING-PROBE-CHEATSHEET.md`
