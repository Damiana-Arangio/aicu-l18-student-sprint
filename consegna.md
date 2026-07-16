# Sprint L18 - Il pannello che non appartiene al prodotto

## Scenario

La dashboard mostra la descrizione nel pannello **Dettagli ticket**.

Una descrizione normale e' leggibile. Una descrizione ostile costruisce invece un
blocco neon molto visibile, marcato come contenuto malevolo e non previsto.

Il payload usa solo HTML e CSS: non esegue JavaScript.

## Missione

Rimuovi il rischio senza perdere il comportamento utile.

## Criteri di accettazione

- la descrizione normale resta leggibile;
- il contenuto ostile viene mostrato come testo;
- non viene creato `[data-testid="malicious-panel"]`;
- il valore salvato non viene mutilato per far passare il test;
- nessuna nuova dipendenza;
- test mirato e suite precedente verdi;
- diff limitato al rischio osservato.

## Processo

1. Esegui `pnpm test:e2e`.
2. Leggi il verde e il rosso.
3. Ricostruisci source, percorso, sink ed effetto.
4. Scegli un controllo coerente con cio' che il prodotto deve mostrare.
5. Implementa la patch.
6. Esegui `pnpm test:e2e` e `pnpm test:all`.
7. Rivedi il diff e rimuovi modifiche fuori scope.

Puoi usare un agente liberamente. Non c'e' un prompt obbligatorio.

## Debrief

Devi poter spiegare:

- dove entrava il contenuto;
- dove diventava struttura;
- quale controllo hai scelto;
- cosa ha proposto l'agente;
- cosa hai rifiutato;
- perche' il test e' diventato verde.

Condividere il codice e' facoltativo.
