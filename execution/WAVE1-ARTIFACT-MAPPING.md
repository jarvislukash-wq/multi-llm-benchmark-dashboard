# Wave 1 Artifact Mapping — multi-llm-benchmark-dashboard

## Purpose

Explicitně propojit **konkrétní Wave 1 kontakty** s tím, jaký artifact mají dostat jako první a jaký jako fallback.

Cíl: ať je hned jasné,
- co poslat komu
- jaký framing tím testujeme
- jaký backup artifact použít, když lead nechce call

**Source-of-truth note:** tento mapping není druhý routing dokument. `framing`, `Primary artifact` a `Fallback artifact` se přebírají bez reinterpretace z `execution/WAVE1-OUTREACH-BATCH.md`, `execution/WAVE1-LIVE-EVIDENCE-BOARD.md` a odpovídajících personalizací ve `execution/WAVE1A-PERSONALIZED-SKELETONS.md` / `execution/WAVE1B-PERSONALIZED-SKELETONS.md`; tady je jen přehled a zdůvodnění pairingů.

---

## Mapping rules

| Framing | Primary artifact | Fallback artifact | Kdy použít |
|---|---|---|---|
| dashboard | `execution/SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md` | `execution/SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | když chceme otevřít demo call, ale mít po ruce lehký dashboard preview a scorecard jako fallback |
| scorecard | `execution/SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `execution/SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | když chceme low-friction vstup přes konkrétní sample |
| memo | `execution/SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | `execution/SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | když lead spíš řeší explainability, governance nebo executive alignment |

---

## Canonical first-5 execution subset

Tento subset musí být konzistentní s:
- `execution/WAVE1-LIVE-EVIDENCE-BOARD.md`
- `execution/WAVE1-FIRST5-SEND-PACKET.md`
- `execution/WAVE1-OUTREACH-BATCH.md`
- `execution/WAVE1A-PERSONALIZED-SKELETONS.md`

| Order | Company | Contact | Framing | Buyer situation | Primary artifact to send | Fallback artifact | Why this pairing |
|---|---|---|---|---|---|---|---|
| 1 | SumUp | Ana Casado | scorecard | resi budget ceiling a fallback model | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | operations + support use case sedí na konkrétní scorecard artefakt a otevírá nejkratší budget/fallback reply path |
| 2 | Magic Patterns | Alexander Danilowicz | scorecard | lightweight vrstva pred plnym LLMOps stackem | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | AI-native founder segment má dostat sample-first wedge bez těžkého dashboard pitchu |
| 3 | Canva | Andreas Schuster | scorecard | rychle porovnat modely pro support use case | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | canonical first-5 tady záměrně drží scorecard-first variantu kvůli rychlejšímu support + budget signalům |
| 4 | Graphite | Quinten Farmer | scorecard | rychle porovnava modely pro novy use case | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | founder v coding segmentu dostane nejdřív nízkotřecí sample místo širší dashboard vrstvy |
| 5 | Notion | Sarav Bhatia | dashboard | ma evaly nebo quality signaly, ale chybi finalni rozhodnuti | `SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | dashboard-first outreach testuje silný multi-model decision workflow; scorecard zůstává fallback při odmítnutí callu |

---

## Remaining Wave 1A queue after first-5

| Order | Company | Contact | Framing | Buyer situation | Primary artifact to send | Fallback artifact | Why this pairing |
|---|---|---|---|---|---|---|---|
| 6 | Khan Academy | Walt Wells | dashboard | ma evaly nebo quality signaly, ale chybi finalni rozhodnuti | `SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | tutoring quality-vs-cost tradeoff sedí na compare workflow; scorecard je nejrychlejší fallback po call CTA |
| 7 | Merck | Walid Mehanna | memo | potrebuje obhajit volbu modelu pred managementem nebo klientem | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | governance-heavy kontakt spíš ocení recommendation framing než čistý compare sheet |
| 8 | Fintool | Paul Klein IV | dashboard | ma evaly nebo routing signaly, ale chybi finalni rozhodnuti | `SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | dashboard-first pitch sedí na eval + routing decisions; scorecard funguje jako concrete leave-behind |
| 9 | Ramp | Ben Levick | memo | potrebuje obhajit volbu modelu pred managementem nebo klientem | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | ops + cost discipline angle sedí na executive memo |

---

## Wave 1B — mixed contact confidence

Tato sekce musí zůstat konzistentní s `execution/WAVE1-CONTACT-VERIFICATION.md`:
- `Dropbox` = `person_verified`
- `Coursera`, `Zapier`, `Loom` = `account_verified`

Proto se Wave 1B nesmí popisovat jako plně verified named-contact batch. Routing zůstává stejný, ale forma oslovení se u `account_verified` firem může opřít o `execution/WAVE1B-ROLE-FALLBACKS.md`.

| Order | Company | Contact / fallback mode | Verification | Framing | Buyer situation | Primary artifact to send | Fallback artifact | Why this pairing |
|---|---|---|---|---|---|---|---|---|
| 1 | Dropbox | Josh Clemm | person_verified | dashboard | ma evaly nebo quality signaly, ale chybi finalni rozhodnuti | `SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | dashboard-first, ale sample scorecard je nejrychlejší asset po prvním doteku |
| 2 | Coursera | Winne Tam / role fallback | account_verified | memo | potrebuje obhajit volbu modelu pred managementem nebo klientem | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | learning/product alignment se lépe vysvětluje přes memo; při slabém person proof použít role-based fallback |
| 3 | Zapier | Mike Knoop / role fallback | account_verified | dashboard | ma evaly nebo quality signaly, ale chybi finalni rozhodnuti | `SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | orchestration-heavy kontakt může chtít workflow call, scorecard je dobrý backup |
| 4 | Loom | Matt Granmoe / role fallback | account_verified | scorecard | hleda lightweight vrstvu pred plnym LLMOps stackem | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | high-volume workflow segment lépe otevře konkrétní scorecard než memo |

---

## Practical send logic

### If first touch is `dashboard`
1. poslat dashboard-first message
2. pokud lead nechce call, nabídnout nebo poslat `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
3. pokud se ptá na recommendation nebo obhajobu volby, přepnout na memo

### If first touch is `scorecard`
1. poslat sample-first message
2. jako první artifact použít `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
3. pokud lead řeší stakeholder alignment, přepnout na memo

### If first touch is `memo`
1. poslat executive-first message
2. jako první artifact použít `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md`
3. pokud lead chce víc operativní compare view, poslat scorecard jako doplněk

---

## Next after send

Po prvních reálných odpovědích doplnit do outreach logu navíc:
- který artifact byl skutečně poslaný
- jestli reply quality byla vyšší po scorecard nebo po memo
- jestli support-assistant sample stačil, nebo lead chtěl use-case-specific variantu
