# Issue: Create ticket with validation

## Request

```txt
Serve creare ticket dal supporto.
```

## Fatti (Facts)
- L’app di partenza è una piccola applicazione di ticketing.

## Assunzioni (Assumptions)
- Il ticket viene creato dal team supporto.
- Il team supporto può compilare un’apposita sezione con le informazioni necessarie per creare un nuovo ticket.
- Dopo una creazione valida, il nuovo ticket viene registrato nel sistema di ticketing e mostrato in un elenco.

## Domande Aperte (Questions)
- Quali informazioni minime sono necessarie per la creazione di un ticket?

## Decisione (Decision)
Per questo slice, "creare ticket" significa:

```txt
Permettere al team supporto di creare un nuovo ticket tramite un’apposita sezione dell’applicazione, compilando le informazioni necessarie.
```

## Fuori Scope / Non-Obiettivi (Non-Goals)
- Autenticazione
- Redesign
- Refactoring fuori dallo scope

## Criteri Di Accettazione (Acceptance Criteria)
1. Il team supporto può compilare le informazioni necessarie e avviare la creazione di un nuovo ticket.
2. Se le informazioni richieste sono valide, il ticket viene creato e mostrato in un elenco.
3. Se mancano informazioni necessarie per la creazione, il ticket non viene creato.

## Piano Di Verifica Manuale (Manual Test Plan)
- Verifica valida: inserisco le informazioni necessarie per creare il ticket e controllo che il nuovo ticket compaia nell’elenco.
- Verifica non valida: provo a creare un ticket senza inserire le informazioni necessarie e controllo che l’elenco resti invariato.

## Note Per L06

- Chiarire il payload minimo necessario per creare un ticket.
- Chiarire quali errori mostrare quando mancano informazioni obbligatorie.
- Chiarire quali dati vengono inseriti dal team supporto e quali vengono generati dal sistema.