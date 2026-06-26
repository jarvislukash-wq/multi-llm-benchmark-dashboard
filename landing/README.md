# Landing Page — Smoke Test

Jednoduchá 1stránková HTML landing page pro validační sprint.

## Co to testuje

1. Zda messaging **Variant S** (use-case scorecard) rezonuje s primárním ICP
2. Zda lidé chtějí vidět demo / scorecards / early access
3. Zda problém působí dost urgentně na nechání kontaktu

## Struktura

- Hero (Variant S headline + subheadline)
- Problem snapshot (5 pain points)
- 2 ukázkové scorecards (RAG support bot + Code assistant)
- „Proč nestačí existující nástroje"
- CTA formulář (Formspree placeholder)
- FAQ (4 otázky)
- Final CTA

## Deploy

### Varianta 1: GitHub Pages (0 cost)
```bash
cd /home/pulec7/projects/multi-llm-benchmark-dashboard
git add landing/
git commit -m "feat: add smoke test landing page (Variant S)"
git push
# Vytvoř branch `gh-pages` nebo použij /docs folder
```

### Varianta 2: Netlify Drop (0 cost, 30 sekund)
1. Táhni `landing/index.html` na https://app.netlify.com/drop
2. Dostaneš URL typu `https://random-name.netlify.app`
3. Můžeš přidat custom domain

### Varianta 3: Vercel (0 cost)
```bash
cd landing/
npx vercel --prod
```

## Formulář

Formulář používá Formspree (placeholder endpoint). Před deploy nahraď:
- `https://formspree.io/f/PLACEHOLDER` → tvůj Formspree endpoint

Alternativy: Tally.so, Google Forms, Typeform.

## Co měřit

| Metrika | Cíl |
|--------|-----|
| Visits (outreach) | 50+ za 2 týdny |
| CTA click rate | 15%+ |
| Form submits | 5+ |
| Reply rate (outreach) | 20%+ |

## Další krok

Po nasazení:
1. Nahradit Formspree endpoint
2. Spustit Wave 1 outreach (`execution/WAVE1-FIRST5-SEND-PACKET.md`)
3. Trackovat odpovědi v `execution/WAVE1-LIVE-EVIDENCE-BOARD.md`
4. Po 14 dnech vyhodnotit verdict podle `VALIDATION-RUNBOOK.md`