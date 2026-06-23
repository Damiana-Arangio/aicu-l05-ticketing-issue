# Consegna - Lezione 05

## Obiettivo

Trasformare una richiesta vaga in una issue verificabile.

Task:

```txt
Serve creare ticket dal supporto.
```

Come visto in aula, non partire dal codice. Prima prepara una issue che renda chiaro che cosa vorresti autorizzare.

## Repository Di Lavoro

Lavora nel tuo fork della repo:

```txt
aicu-m02-l05-ticketing-issue
```

Questa repo e' il primo checkpoint del Modulo 2. Produce l'artefatto che importerai nella repo L06.

## Input

Usa:

```txt
template/issue-create-ticket.md
template/prompt-critica-issue.md
```

Puoi lavorare in un file Markdown, in una issue GitHub o in una nota locale. L'importante e' che l'output sia leggibile e recuperabile.

## Cosa Fare

1. Copia il template issue.
2. Compila solo i fatti (facts).
3. Aggiungi le assunzioni (assumptions).
4. Scrivi le domande aperte (questions).
5. Scrivi una decisione (decision) di slice minimo.
6. Aggiungi fuori scope / non-obiettivi (non-goals).
7. Scrivi massimo 3 criteri di accettazione (acceptance criteria).
8. Scrivi 2 verifiche manuali.
9. Usa il prompt di critica issue solo per trovare buchi nella issue, senza chiedere codice.
10. Aggiorna la issue con le correzioni utili.

## Ordine Guidato

Non compilare tutto il template in autonomia dall'alto in basso.

Lavora a checkpoint:

| Step | Output minimo | Check |
| --- | --- | --- |
| Fatti (facts) | 2 fatti letti o decisi | Nessuna ipotesi nascosta |
| Assunzioni (assumptions) | 1-2 ipotesi operative | Sono dichiarate come ipotesi |
| Domande aperte (questions) | 1 domanda reale | Non blocca il primo slice |
| Decisione (decision) | 1 frase sullo slice | E' verificabile |
| Fuori scope / non-obiettivi (non-goals) | 2-3 esclusioni | Tagliano scope reale |
| Criteri di accettazione (acceptance criteria) | massimo 3 criteri | Sono osservabili |
| Piano di verifica manuale | 2 verifiche | Azione + risultato atteso |

## Vincoli

- Non chiedere codice.
- Non definire contract tecnico completo.
- Non progettare database o migration.
- Non aggiungere auth, allegati, notifiche, owner avanzato o dashboard.
- Non scrivere piu' di 3 criteri di accettazione (acceptance criteria).
- Non chiedere chain-of-thought estesa: bastano evidenze brevi.

## Criteri Di Accettazione Della Issue

La issue e' buona quando:

- distingue fatti (facts), assunzioni (assumptions) e domande aperte (questions);
- dichiara una decisione minima;
- contiene fuori scope / non-obiettivi (non-goals);
- usa criteri osservabili;
- ha 2 verifiche manuali;
- lascia chiaro cosa andra' approfondito in L06.

## Pronto Quando

Hai finito quando puoi rispondere in 60 secondi:

```txt
Che cosa voglio fare?
Che cosa non voglio fare ora?
Come capisco se il primo slice e' corretto?
Quale domanda resta da portare a L06?
```

## Micro-Task Post-Lezione

Input:

```txt
la issue compilata in aula
```

Azione:

```txt
rileggila e riduci lo scope se ha piu' di 3 criteri di accettazione (acceptance criteria),
oppure aggiungi una domanda aperta se hai nascosto un'assunzione.
```

Stop:

```txt
non aggiungere codice, contract, schema o PR.
```

## Fuori Scope

- Codice.
- Pull Request.
- UI completa.
- Endpoint completo.
- Database schema.
- Test automatici.
- Review agentica avanzata.
