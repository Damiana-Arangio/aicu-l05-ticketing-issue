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
- I campi title, customer e priority sono obbligatori.
- Il campo title deve essere breve, massimo 100 caratteri.
- Il nuovo ticket dovrà essere aggiunto all’array locale già esistente
- La possibilità di creare un nuovo ticket verrà inserita nella schermata della lista dei ticket aperti

## Domande Aperte (Questions)
- Dopo la creazione, il nuovo ticket deve essere aggiunto mantenendo l’ordine attuale dell’array oppure deve essere previsto un ordinamento specifico?
- La priority deve essere selezionata da valori predefiniti (Alta, Media, Bassa) oppure inserita manualmente e validata?


## Decisione (Decision)
Per questo slice, "creare ticket" significa:

```txt
Permettere a un operatore del team supporto di creare un nuovo ticket dalla schermata della lista dei ticket aperti, compilando `title`, `customer` e `priority`.

Il ticket viene validato, completato automaticamente con `id`, `status: open` e `updatedAt`, aggiunto all’array locale e mostrato nella lista dei ticket aperti.
```

## Fuori Scope / Non-Obiettivi (Non-Goals)
- Autenticazione
- Redesign
- Refactoring fuori dallo scope
- Database reale
- Allegati
- Notifiche
- Dashboard
- Persistenza permanente del nuovo ticket oltre il ciclo di vita dell’array locale/backend
- Campi aggiuntivi del ticket non esplicitamente dichiarati
- pagina dedicata alla creazione ticket
- Definizione di un ordinamento specifico del nuovo ticket dopo la creazione; la decisione resta aperta per L06

## Criteri Di Accettazione (Acceptance Criteria)
1. Dalla schermata della lista dei ticket aperti, un operatore può compilare title, customer e priority e creare un nuovo ticket.
2. Se il supporto lascia vuoto un campo obbligatorio o inserisce un title più lungo di 100 caratteri, il ticket non viene creato e viene mostrato un errore comprensibile.
3. Dopo una creazione valida, il nuovo ticket compare nella lista dei ticket aperti e il totale dei ticket viene aggiornato.

## Piano Di Verifica Manuale (Manual Test Plan)
- Verifica valida: creare un ticket compilando title, customer e priority con valori validi; controllare che il nuovo ticket compaia nella lista dei ticket aperti e che il conteggio totale aumenti di 1.
- Verifica non valida: provare a creare un ticket con title vuoto, customer vuoto oppure title oltre 100 caratteri; controllare che venga mostrato un errore comprensibile e che la lista dei ticket aperti resti invariata.

## Note Per L06
- Chiarire se, dopo la creazione, il nuovo ticket deve mantenere l’ordine attuale dell’array o seguire un ordinamento specifico.
- Chiarire se priority sarà selezionata da valori predefiniti o inserita manualmente e validata.
- Chiarire il payload minimo per creare un ticket: title, customer e priority.
- Chiarire quali messaggi o errori mostrare quando la validazione fallisce.
- Chiarire il formato finale dei campi generati automaticamente: id e updatedAt.