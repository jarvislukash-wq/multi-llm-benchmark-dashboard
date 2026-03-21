# Wave 1 Live Evidence Board — multi-llm-benchmark-dashboard

## Purpose

Poslední missing bridge mezi "assety jsou hotové" a "první live send opravdu běží".

Tenhle dokument neslouží na nový research ani nový routing.
Slouží čistě jako **jedna operační tabule**, kde je pro každý Wave 1 účet na jednom místě:
- koho oslovit
- s jakou confidence
- přes jaký framing
- s jakým triggerem
- s jakým CTA
- s jakým primary/fallback artifactem
- co přesně po reply logovat

Praktický cíl:
- zkrátit první live execution z více souborů na jeden operativní view
- snížit riziko, že se při live sendu potichu přepíše framing nebo artifact mapping
- připravit čistý podklad pro první reálnou reply evidence

---

## Source-of-truth order

Tenhle board nic nepřeroutovává. Jen skládá dohromady existující pravdu.

1. `DISCOVERY-TRACKER.md` = buyer situation + prioritizace
2. `execution/WAVE1-OUTREACH-BATCH.md` = canonical contact + framing + CTA + artifact routing
3. `execution/WAVE1-CONTACT-VERIFICATION.md` = confidence na public person vs account
4. `execution/WAVE1-TIMING-TRIGGERS.md` = timing opener a trigger layer
5. `execution/OUTREACH-LOG-TEMPLATE.md` = finální evidence labels po sendu a reply

Když se změní routing, neměnit ho tady jako první.

---

## Status labels

Používat stejné hodnoty jako v `execution/OUTREACH-LOG-TEMPLATE.md`:
- `drafted`
- `sent`
- `follow_up_1`
- `follow_up_2`
- `replied`
- `booked`
- `completed`
- `disqualified`

## Reply evidence labels

Po reálné odpovědi logovat jen canonical hodnoty:
- `reply_quality = none / weak / relevant / high_intent`
- `preferred_artifact = dashboard / scorecard / memo / report / API / hybrid / unknown`
- `status_quo = spreadsheet / memo / provider_native / mixed / unclear`
- `status_quo_break = speed / shareable_output / refreshability / mixed / unclear`
- `price_probe = none / under_39 / 39_149 / 149_plus / enterprise`
- `pro_signal = positive / neutral / negative`

---

## Wave 1 live queue

| Priority | Wave | Company | Contact | Verification | Channel | Buyer situation | Trigger | Framing | CTA | Primary artifact | Fallback artifact | Current status | Why this lead now |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | 1A | SumUp | Ana Casado | person_verified | LinkedIn | budget ceiling a fallback rozhodnuti | budget_fallback | scorecard | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | drafted | nejkratší pain path: cost ceiling + fallback |
| 2 | 1A | Magic Patterns | Alexander Danilowicz | person_verified | LinkedIn + company site | rychle porovnava modely pro novy use case | pre_llmops_gap | scorecard | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | drafted | AI-native founder, lehký scorecard-first wedge |
| 3 | 1A | Canva | Andreas Schuster | person_verified | LinkedIn | rychle porovnat modely pro support use case | budget_fallback | scorecard | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | drafted | support use case dobře spojuje quality + cost |
| 4 | 1A | Graphite | Quinten Farmer | person_verified | LinkedIn + request demo | rychle porovnava modely pro novy use case | new_ai_surface | scorecard | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | drafted | coding wedge, nový AI surface, founder fit |
| 5 | 1A | Notion | Sarav Bhatia | person_verified | LinkedIn + request demo | ma evaly nebo quality signaly, ale chybi finalni decision layer | new_ai_surface | dashboard | ask for 20min demo call | `SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | drafted | multi-model AI surface, silný dashboard opener |
| 6 | 1A | Khan Academy | Walt Wells | person_verified | LinkedIn | ma evaly nebo quality signals, ale chybi finalni decision layer | compare_chaos | dashboard | ask for 20min demo call | `SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | drafted | quality-vs-cost tradeoff bez čistého leaderboard řešení |
| 7 | 1A | Fintool | Paul Klein IV | person_verified | LinkedIn + company site | ma evaly nebo routing signals, ale chybi finalni decision layer | compare_chaos | dashboard | ask for 20min demo call | `SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | drafted | eval + routing pain, decision layer wedge |
| 8 | 1A | Ramp | Ben Levick | person_verified | LinkedIn + demo/contact path | obhajit volbu modelu pred managementem nebo klientem | stakeholder_alignment | memo | ask for executive feedback | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | drafted | productivity + cost discipline + executive alignment |
| 9 | 1A | Merck | Walid Mehanna | person_verified | LinkedIn | obhajit volbu modelu pred managementem nebo klientem | stakeholder_alignment | memo | ask for executive feedback | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | drafted | governance-heavy account, memo-first fit |
| 10 | 1B | Dropbox | Josh Clemm | person_verified | LinkedIn | ma evaly nebo quality signals, ale chybi finalni decision layer | compare_chaos | dashboard | ask for 20min demo call | `SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | drafted | silný eval-merge story, ale až po 1A signálech |
| 11 | 1B | Coursera | Winne Tam / role fallback | account_verified | LinkedIn + leadership path | obhajit volbu modelu pred managementem nebo klientem | stakeholder_alignment | memo | ask for executive feedback | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | drafted | account fit ano, named contact confidence slabší |
| 12 | 1B | Zapier | Mike Knoop / role fallback | account_verified | LinkedIn + contact sales | ma evaly nebo quality signals, ale chybi finalni decision layer | compare_chaos | dashboard | ask for 20min demo call | `SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | drafted | orchestration-heavy context, ale radši až po 1A |
| 13 | 1B | Loom | Matt Granmoe / role fallback | account_verified | LinkedIn + Atlassian path | hleda lightweight vrstvu pred plnym LLMOps stackem | pre_llmops_gap | scorecard | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | drafted | dobrý low-friction wedge, ale slabší person proof |

---

## First 5 send set

Pokud je cíl co nejrychleji získat první kvalitní reply evidence, poslat nejdřív těchto 5:

1. SumUp
2. Magic Patterns
3. Canva
4. Graphite
5. Notion

### Why this exact set

- 3× velmi konkrétní `scorecard` wedge
- 2× jasný `new_ai_surface` / `dashboard` decision workflow
- mix startup + SaaS
- mix `budget_fallback`, `pre_llmops_gap`, `new_ai_surface`
- vysoká verification confidence
- `Canva` je v tomhle first-live-send subsetu záměrně vedena přes `scorecard`, ne přes širší dashboard variantu, protože první mikro-cíl je rychlejší `budget_fallback` reply signal

První mini-cíl není maximalizovat volume.
První mini-cíl je získat **5 odeslání -> první reply quality signal -> první trigger verdict**.

---

## Operator checklist per lead

### Before send
- potvrdit, že `Verification` odpovídá `WAVE1-CONTACT-VERIFICATION.md`
- neposouvat lead mezi `dashboard / scorecard / memo` bez změny v canonical routing souboru
- držet `Primary artifact` a `Fallback artifact` přesně podle batch mappingu
- u `account_verified` použít role-based fallback wording

### After send
Zapsat do `execution/OUTREACH-LOG-TEMPLATE.md` minimálně:
- `Date`
- `Channel`
- `Status = sent`
- `Framing`
- `CTA`
- `Sent artifact`
- do notes přidat:
  - `trigger_used: ...`
  - `trigger_confirmed: unclear`
  - `trigger_shift: none`

### After reply
Dopsat navíc:
- `Reply quality`
- `First reply artifact`
- `Preferred artifact`
- `status_quo`
- `status_quo_break`
- `price_probe`
- `pro_signal`
- 1 přesnou citaci buyera
- zapisovat `price_probe` a `pro_signal` do explicitnich sloupcu v `execution/OUTREACH-LOG-TEMPLATE.md`, ne jen do notes
- do notes přidat:
  - `trigger_confirmed: yes / no / unclear`
  - `trigger_shift: none / dashboard / scorecard / memo`

### After call
Dopsat navíc:
- `Pain (1-5)`
- booking / completion status
- jestli chce pilot, sample pro vlastní use case, pricing follow-up nebo intro na dalšího člověka

---

## Daily execution rhythm

### Day 0
- odeslat first 5
- všechny 4 povinné log vrstvy zapsat ihned po sendu

### Day 3
- poslat framing-specific follow-up jen podle `execution/WAVE1-FOLLOW-UP-SEQUENCES.md`
- nezavádět nový messaging mimo canonical follow-up sekvenci

### Day 7
- poslední low-friction follow-up
- pokud stále bez reply, neřešit další interní docs; počkat na další live wave nebo signál

---

## Mini verdict threshold

Jakmile existuje aspoň jedna z těchto podmínek, má smysl vyplnit `execution/WAVE1-VALIDATION-VERDICT-TEMPLATE.md`:
- 5+ reply
- 3+ discovery calls
- 2+ high-intent leady v jednom segmentu

Do té doby neřešit další strategy docs.
Poctivý další krok po tomto boardu už je opravdu jen live send + evidence capture.
