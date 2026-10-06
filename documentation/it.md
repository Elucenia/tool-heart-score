<!-- ELUCENIA technical documentation · heart-score · it · no clinical/professional/rights approval -->

# Punteggio HEART

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/heart-score)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Anamnesi

`h`

- `0` — Poco sospetta
- `1` — Moderatamente sospetta
- `2` — Molto sospetta

### ECG

`e`

- `0` — Normale
- `1` — Alterazione aspecifica della ripolarizzazione
- `2` — Sottoslivellamento significativo del tratto ST

### Età

`a`

- `0` — ≤ 45 anni
- `1` — \> 45 e \< 65 anni
- `2` — ≥ 65 anni

### Fattori di rischio

`r`

- `0` — Nessuno
- `1` — 1 o 2
- `2` — ≥ 3 o malattia aterosclerotica nota

### Troponina

`t`

- `0` — ≤ limite normale
- `1` — \> 1× e \< 3× il limite superiore della norma
- `2` — ≥ 3× il limite superiore della norma

## Edizione del metodo

HEART/Backus 2013: 5 componenti da 0–2 punti, totale 0–10; età ≤45, \>45 e \<65, ≥65 anni; troponina ≤LSN, \>1×LSN e \<3×LSN, ≥3×LSN; non è il HEART Pathway con valutazioni seriali

## Formula documentata

Da 0 a 2 punti per item: History (anamnesi), ECG, Age (età), Risk factors (fattori di rischio), Troponina. Totale da 0 a 10.

Fattori di rischio: ipertensione, dislipidemia, diabete, obesità (IMC \> 30), fumo attuale o recente, familiarità per coronaropatia precoce.

## Limiti e popolazione

L’HEART originale è stato studiato in pronto soccorso in persone con dolore toracico e sospetta sindrome coronarica senza sopraslivellamento ST. Un punteggio basso non significa rischio nullo e la somma originale non equivale all’HEART Pathway con valutazione seriale. La sicurezza della dimissione, i tempi delle troponine e le esclusioni richiedono il protocollo corrispondente.

## Riferimenti

- [Six AJ, Backus BE, Kelder JC. Chest pain in the emergency room: value of the HEART score. Neth Heart J, 2008.](https://doi.org/10.1007/BF03086144)

- [Backus BE et al. A prospective validation of the HEART score for chest pain patients at the emergency department. Int J Cardiol, 2013.](https://doi.org/10.1016/j.ijcard.2013.01.255)

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

Rischio alto: strategia invasiva precoce

| Dettagli del risultato | |
| --- | --- |
| MACE a 6 settimane | 50,1% |


### 2

Basso rischio: considerare la dimissione con troponine seriali negative e follow-up ambulatoriale

| Dettagli del risultato | |
| --- | --- |
| MACE a 6 settimane | 1,7% |


### 3

Rischio moderato: osservazione, troponina seriale e indagine non invasiva

| Dettagli del risultato | |
| --- | --- |
| MACE a 6 settimane | 16,6% |

