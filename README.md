# Ratio — Email Templates Viewer

Visualizzatore interno delle sequenze email per il software **Ratio** — strumento SaaS per investitori immobiliari italiani.

## Cosa contiene

27 template HTML pronti per l'invio via API (9 email × 3 zone geografiche):

- **Nord Italia** — Milano, Torino, Bologna
- **Centro Italia** — Roma, Firenze
- **Sud Italia** — Napoli, Palermo, Bari

## Come usarlo

Apri `index.html` nel browser (o accedi all'URL Vercel).

Nella sidebar seleziona la zona e l'email. Il pannello mostra:
- Oggetto e preview text (3 varianti A/B/C)
- Anteprima renderizzata
- Pulsante **Copia HTML** per estrarre il codice da incollare nell'ESP/API

## Struttura sequenza

| # | Email | Timing | Bucket |
|---|-------|--------|--------|
| 1 | Benvenuto e accesso | G0 · T+0h | Tutti |
| 2 | La classifica di stamattina | G1 · T+24h | Tutti |
| 3 | Scadenza imminente | G3 · T+69h | Non convertiti |
| 4 | Trial scaduto | G4 · T+96h | Non convertiti |
| 5 | Argomento ROI | G5 · T+120h | Non convertiti |
| 6 | Bonus Report Storico | G6 · T+144h | Non convertiti |
| 7 | Domanda diretta | G7 · T+168h | Non convertiti |
| 8 | Offerta finale + referral | G8 · T+192h | Non convertiti |
| 9 | Nurturing mercato | G14+ | Non convertiti |

## Campo dinamico

Un solo campo dinamico: `[NOME]` — tutto il resto usa valori fissi o volutamente vaghi.

## Deploy

Progetto statico. Deploy su Vercel automatico a ogni push su `main`.
