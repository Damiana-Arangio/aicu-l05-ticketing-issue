# Issue: Create ticket with validation

## Request

```txt
Serve creare ticket dal supporto.
```

## Fatti (Facts)

- L’app di partenza è una piccola applicazione di ticketing.
- Il frontend è sviluppato in React.
- Il backend espone un’API Express con Node.js per recuperare ticket fittizi.
- I ticket attuali non sono salvati in un database, ma sono definiti in un array locale.
- L’app mostra una lista di ticket aperti, indicandone anche il numero totale.
- Ogni ticket contiene i seguenti campi: id, title, customer, priority, status e updatedAt.


## Assunzioni (Assumptions)

- Il nuovo ticket dovrà usare la stessa struttura dei ticket già presenti nell’app
- Il supporto dovrà compilare manualmente solo i campi title, customer e priority
- I campi id e updatedAt dovranno essere inseriti automaticamente durante la creazione
- Il campo status verrà impostato automaticamente a open
- La priorità dovrà usare uno dei valori già presenti nei ticket attuali: Alta, Media o Bassa.
- Il campo title deve essere breve (max 100 caratteri)
- Il nuovo ticket dovrà essere aggiunto all’array locale già esistente

## Domande Aperte (Questions)

- La possibilità di creare un nuovo ticket conviene inserirla nella schermata della lista dei ticket aperti o in una nuova pagina dedicata?
- Dopo la creazione, il nuovo ticket deve comparire in cima alla lista, in fondo alla lista o seguire un ordinamento basato sulla priorità?

## Decisione (Decision)

Per questo slice, "creare ticket" significa:

```txt
Permettere ad un operatore del team supporto di creare un nuovo ticket, che verrà poi inserito nella lista dei ticket aperti dell’app.
```

## Fuori Scope / Non-Obiettivi (Non-Goals)

- autenticazione
- redesign
- refactoring fuori dallo scope
- database reale
- Campi aggiuntivi del ticket non esplicitamente dichiarati

## Criteri Di Accettazione (Acceptance Criteria)

1. Se il supporto compila title, customer e priority, il nuovo ticket viene creato
2. Se il supporto lascia vuoto un campo obbligatorio o inserisce un title più lungo di 100 caratteri, il ticket non viene creato
3. Dopo una creazione valida, il nuovo ticket compare nella lista dei ticket aperti e il conteggio totale aumenta di 1.


## Piano Di Verifica Manuale (Manual Test Plan)

- Verifica valida: creare un nuovo ticket, compilando tutti i campi obbligatori con valori validi, controllare che il nuovo ticket compaia nella lista dei ticket aperti e che il conteggio totale aumenti di 1.
Verifica non valida: creare un nuovo ticket, lasciando vuoto almeno un campo obbligatorio oppure inserendo un title più lungo di 100 caratteri, controllare che non venga aggiunto alla lista.

## Note Per L06

- [quale payload andra' chiarito]
- [quale errore andra' chiarito]
- [quale campo dati andra' deciso]
