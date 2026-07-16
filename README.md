# AICU L18 - Student sprint

Questa repo contiene lo sprint individuale della lezione Payload lab.

## Requisiti

- Node.js 26 o superiore;
- pnpm.

## Setup

```bash
pnpm install
pnpm setup:browsers
```

## Primo run

```bash
pnpm test:e2e
```

Il risultato iniziale e' intenzionale:

- descrizione normale: verde;
- descrizione ostile: rosso.

Il rosso mostra che il contenuto di un ticket crea un pannello HTML/CSS non previsto.
Non cambiare il test o il payload per nascondere l'effetto.

## Missione

Leggi `consegna.md`. Puoi usare un agente dall'inizio, ma devi saper spiegare la
catena osservata, la patch, lo scope e il motivo del verde.

## Comandi

```bash
pnpm dev
pnpm check
pnpm test
pnpm test:e2e
pnpm test:all
```

SQLite usa un file locale in `data/` per `pnpm dev` e un database in-memory nei test.
