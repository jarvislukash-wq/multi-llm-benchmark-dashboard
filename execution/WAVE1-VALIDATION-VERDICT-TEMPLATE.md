# Wave 1 Validation Verdict Template — multi-llm-benchmark-dashboard

## Purpose

Lehká šablona pro zápis výsledku po prvních odpovědích, follow-upech a discovery callech.

Cíl není udělat další velký report. Cíl je rychle rozhodnout 4 věci:
1. který segment reaguje nejsilněji
2. který framing otevírá nejlepší konverzace
3. jaká je první realistická placená jednotka
4. jestli pokračovat, zúžit wedge, nebo stopnout

Používat po prvním mini-souboru signálů, typicky když už existuje aspoň:
- 5+ odpovědí nebo
- 3+ discovery cally nebo
- 2+ high-intent signály z jednoho segmentu

---

## Snapshot

- Date:
- Owner:
- Wave covered: Wave 1A / Wave 1B / combined
- Period covered:
- Total leads touched:
- Total replies:
- Positive replies:
- Calls booked:
- Calls completed:

---

## 1. Segment verdict

| Segment | Leads touched | Replies | Positive replies | Calls | Avg pain | Avg purchase intent | Notes |
|---|---:|---:|---:|---:|---:|---:|---|
| AI startup / applied AI |  |  |  |  |  |  |  |
| AI agentura |  |  |  |  |  |  |  |
| SaaS s AI feature |  |  |  |  |  |  |  |
| Enterprise / governance |  |  |  |  |  |  |  |

### Segment winner
- Strongest segment now:
- Why:
- Confidence: low / medium / high

### Segment loser / weak signal
- Weakest segment now:
- Why:

---

## 2. Framing verdict

| Framing | Leads touched | Replies | High-quality replies | Calls | Strongest phrase heard back | Verdict |
|---|---:|---:|---:|---:|---|---|
| dashboard |  |  |  |  |  |  |
| scorecard |  |  |  |  |  |  |
| memo |  |  |  |  |  |  |

### Framing decision
- Current winner: dashboard / scorecard / memo / hybrid
- Why it wins:
- What to stop saying:
- Exact phrasing to reuse:

---

## 3. Pricing + paid unit verdict

| Probe | Mentioned to how many leads | Positive signal count | Negative signal count | Notes |
|---|---:|---:|---:|---|
| Starter hypothesis (~€39) |  |  |  |  |
| Pro workspace hypothesis (€99–149) |  |  |  |  |
| Team workspace hypothesis (from ~€399) |  |  |  |  |
| Paid pilot / enterprise memo |  |  |  |  |

### First paid unit decision
- Best first paid unit now: starter hypothesis (~€39) / pro workspace hypothesis (€99–149) / team workspace hypothesis (from ~€399) / paid scorecard workflow / paid memo pilot
- Why:
- Objection pattern:
- Sweet spot signal: none / under_39 / 39_149 / 149_plus / enterprise
- `price_probe` summary used in this verdict: none / under_39 / 39_149 / 149_plus / enterprise
- `pro_signal` summary used in this verdict: positive / neutral / negative
- One exact sentence that best confirms pricing signal:

### Pricing evidence normalization rule
- Do not rename pricing evidence inside the verdict.
- If a reply or call note exists in `execution/OUTREACH-LOG-TEMPLATE.md`, copy the same `price_probe` and `pro_signal` labels here without translation.
- If evidence is mixed, summarize by segment but keep the same allowed values only.

### Pro workspace hypothesis (€99–149) check
- Hypothesis status: confirmed / leaning_yes / unclear / leaning_no / rejected
- Evidence that supports `Pro workspace (€99–149)`:
  - buyer says ongoing monitoring is worth more than one-off audit
  - buyer compares budget to existing observability / eval / QA tooling, ne k jednorázové konzultaci
  - buyer accepts workspace framing pro tým nebo opakované benchmark review
- Evidence that weakens `Pro workspace (€99–149)`:
  - buyer chce jen jednorázový teardown nebo PDF výstup bez průběžného používání
  - buyer price-anchoruje řešení pod `€39` nebo čeká čistě free artifact
  - buyer value vidí jen v enterprise memo / custom pilotu mimo self-serve workspace
- Minimum signal to keep `Pro workspace (€99–149)` v další vlně: aspoň 2 nezávislé high-intent konverzace, kde buyer bez odporu přijme rozmezí `€99–149` pro ongoing workspace
- If signal missing, next action: test `paid scorecard workflow` nebo posunout pricing probe níž, ale neměnit ICP bez reply evidence

---

## 4. Artifact verdict

| Artifact | Sent count | Mentioned positively | Asked for again | Best-fit segment | Notes |
|---|---:|---:|---:|---|---|
| scorecard |  |  |  |  |  |
| dashboard demo |  |  |  |  |  |
| memo |  |  |  |  |  |

### Artifact decision
- Best opener:
- Best follow-up asset:
- Asset to deprioritize:

---

## 5. Top evidence

### Best exact quotes
- ""
- ""
- ""

### Strongest objections
- 
- 
- 

### Strongest next-step signals
- wants pilot
- wants sample for own use case
- wants intro to teammate
- wants pricing / procurement follow-up
- other:

---

## 6. Decision

### Final verdict
- Continue / Narrow / Stop

### If continue
- Keep this segment:
- Keep this framing:
- Keep this CTA:
- Keep this pricing probe:

### If narrow
- Drop this segment:
- Drop this framing:
- Focus next wave on:

### If stop
- Main reason:
- What failed:

---

## 7. Next wave rules

- Next 5 leads should be:
- Primary CTA for next wave:
- Fallback CTA:
- Primary artifact:
- Fallback artifact:
- Pricing question to ask explicitly:
- One thing not to change yet:
- One thing to rewrite before next send:

---

## 8. SPEC-readiness check

Mark `yes / no`:

- Problem confirmed by real buyer conversations:
- One segment clearly stronger than others:
- One framing clearly stronger than others:
- One realistic first paid unit identified:
- Enough signal to draft first SPEC without guessing:

### Readiness note
- If not ready, what is still missing:
- If ready, what SPEC should assume as the first wedge:
