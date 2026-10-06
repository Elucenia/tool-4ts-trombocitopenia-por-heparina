<!-- ELUCENIA technical documentation · 4ts-trombocitopenia-por-heparina · it · no clinical/professional/rights approval -->

# Punteggio 4T (trombocitopenia indotta da eparina)

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/4ts-trombocitopenia-por-heparina)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Trombocitopenia

`trombo`

- `0` — Calo \< 30% o nadir \< 10.000/µL
- `1` — Calo dal 30% al 50% o nadir da 10.000 a 19.000/µL
- `2` — Calo \> 50% e nadir ≥ 20.000/µL

### Tempo del calo delle piastrine

`tempo`

- `0` — Calo prima del giorno 4 senza esposizione recente
- `1` — Compatibile con i giorni 5–10, ma incerto; dopo il giorno 10; o ≤ 1 giorno con esposizione all’eparina da 30 a 100 giorni prima
- `2` — Esordio chiaro tra il 5° e il 10° giorno, o ≤ 1 giorno con esposizione a eparina negli ultimi 30 giorni

### Trombosi o altre sequele

`trombose`

- `0` — Nessuna
- `1` — Trombosi progressiva o ricorrente, lesione cutanea non necrotica o sospetta trombosi
- `2` — Nuova trombosi confermata, necrosi cutanea o reazione sistemica dopo bolo

### Altre cause di trombocitopenia

`outras`

- `0` — Certa
- `1` — Possibile
- `2` — Nessuna evidente

## Edizione del metodo

4Ts/Lo 2006: 4 domini 0–2, totale 0–8; contesto ASH 2018

## Formula documentata

Quattro item, 0 a 2 ciascuno: Trombocitopenia · Tempo · Trombosi · alTre cause. Massimo: 8.

## Limiti e popolazione

Stima la probabilità clinica pre-test nel sospetto di HIT dopo esposizione all’eparina. Dipende dalla storia piastrinica, temporale, trombotica e delle cause alternative. Il risultato non conferma la HIT; i valori predittivi variavano tra gli scenari studiati.

## Riferimenti

- [Lo GK et al. Evaluation of pretest clinical score (4 T's) for the diagnosis of heparin-induced thrombocytopenia in two clinical settings. J Thromb Haemost, 2006.](https://doi.org/10.1111/j.1538-7836.2006.01787.x)

- [Cuker A et al. American Society of Hematology 2018 guidelines for management of venous thromboembolism: heparin-induced thrombocytopenia. Blood Adv, 2018.](https://doi.org/10.1182/bloodadvances.2018024489)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Risultati documentati

Le informazioni seguenti conservano gli output del metodo per esempi sintetici. Non costituiscono una validazione clinica indipendente.

### 1

Bassa probabilità di HIT (0 a 3 punti)

ASH 2018: non dosare gli anticorpi anti-PF4 e mantenere l’eparina, cercando un’altra causa.


### 2

Probabilità intermedia (4 a 5 punti)

Sospendere tutta l’eparina, iniziare un anticoagulante non eparinico a dose terapeutica e dosare anti-PF4.


### 3

Alta probabilità (6 a 8 punti)

Sospendere tutta l’eparina, iniziare un anticoagulante non eparinico a dose terapeutica e confermare con anti-PF4 (e test funzionale).


### 4

Alta probabilità (6 a 8 punti)

Sospendere tutta l’eparina, iniziare un anticoagulante non eparinico a dose terapeutica e confermare con anti-PF4 (e test funzionale).

