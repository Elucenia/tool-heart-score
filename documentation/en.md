<!-- ELUCENIA technical documentation · heart-score · en · no clinical/professional/rights approval -->

# HEART score

[conditions, sources and permissions](https://elucenia.org/en/tools/heart-score)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### History

`h`

- `0` — Low suspicion
- `1` — Moderately suspicious
- `2` — Highly suspicious

### ECG

`e`

- `0` — Normal
- `1` — Nonspecific repolarization abnormality
- `2` — Significant ST depression

### Age

`a`

- `0` — ≤ 45 years
- `1` — \> 45 and \< 65 years
- `2` — ≥ 65 years

### Risk factors

`r`

- `0` — None
- `1` — 1 or 2
- `2` — ≥ 3 or known atherosclerotic disease

### Troponin

`t`

- `0` — ≤ normal limit
- `1` — \> 1× and \< 3× the upper limit of normal
- `2` — ≥ 3× the upper limit of normal

## Method edition

HEART/Backus 2013: 5 components scored 0–2, total 0–10; age ≤45, \>45 and \<65, ≥65 years; troponin ≤ULN, \>1×ULN and \<3×ULN, ≥3×ULN; not the serial HEART Pathway

## Documented formula

Add 0 to 2 points per item: History, ECG, Age, Risk factors and Troponin. Total 0 to 10.

Risk factors: hypertension, dyslipidemia, diabetes, obesity (BMI \> 30), current or recent smoking, family history of premature CAD.

## Limits and population

The original HEART was studied in emergency patients with chest pain and suspected non-ST-elevation coronary syndrome. A low score does not mean zero risk, and the original sum is not equivalent to the HEART Pathway with serial assessment. Discharge safety, troponin timing and exclusions require the corresponding protocol.

## References

- [Six AJ, Backus BE, Kelder JC. Chest pain in the emergency room: value of the HEART score. Neth Heart J, 2008.](https://doi.org/10.1007/BF03086144)

- [Backus BE et al. A prospective validation of the HEART score for chest pain patients at the emergency department. Int J Cardiol, 2013.](https://doi.org/10.1016/j.ijcard.2013.01.255)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Documented results

The information below preserves the method outputs for synthetic examples. It does not constitute independent clinical validation.

### 1

High risk: Early invasive strategy

| Result details | |
| --- | --- |
| MACE in 6 weeks | 50.1% |


### 2

Low risk: Consider discharge with negative serial troponins and outpatient follow-up

| Result details | |
| --- | --- |
| MACE in 6 weeks | 1.7% |


### 3

Moderate risk: Observation, serial troponin and noninvasive investigation

| Result details | |
| --- | --- |
| MACE in 6 weeks | 16.6% |

