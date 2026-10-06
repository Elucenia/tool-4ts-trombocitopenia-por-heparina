<!-- ELUCENIA technical documentation · 4ts-trombocitopenia-por-heparina · en · no clinical/professional/rights approval -->

# 4Ts score (heparin-induced thrombocytopenia)

[conditions, sources and permissions](https://elucenia.org/en/tools/4ts-trombocitopenia-por-heparina)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Thrombocytopenia

`trombo`

- `0` — Fall \< 30% or nadir \< 10,000/µL
- `1` — Fall of 30% to 50% or nadir of 10,000 to 19,000/µL
- `2` — Fall \> 50% and nadir ≥ 20,000/µL

### Timing of platelet fall

`tempo`

- `0` — Fall before day 4 without recent exposure
- `1` — Compatible with days 5–10 but uncertain; after day 10; or ≤ 1 day with heparin exposure 30 to 100 days ago
- `2` — Clear onset between days 5 and 10, or ≤ 1 day with heparin exposure in the last 30 days

### Thrombosis or other sequelae

`trombose`

- `0` — None
- `1` — Progressive or recurrent thrombosis, non-necrotic skin lesion or suspected thrombosis
- `2` — New confirmed thrombosis, skin necrosis or systemic reaction after a bolus

### Other causes of thrombocytopenia

`outras`

- `0` — Definite
- `1` — Possible
- `2` — None apparent

## Method edition

4Ts/Lo 2006: 4 domains 0–2, total 0–8; ASH 2018 context

## Documented formula

Four items, 0 to 2 each: Thrombocytopenia · Timing · Thrombosis · oTher causes. Maximum: 8.

## Limits and population

Estimates clinical pretest probability in suspected HIT after heparin exposure. It depends on platelet, timing, thrombotic and alternative-cause history. The result does not confirm HIT; predictive values varied across the settings studied.

## References

- [Lo GK et al. Evaluation of pretest clinical score (4 T's) for the diagnosis of heparin-induced thrombocytopenia in two clinical settings. J Thromb Haemost, 2006.](https://doi.org/10.1111/j.1538-7836.2006.01787.x)

- [Cuker A et al. American Society of Hematology 2018 guidelines for management of venous thromboembolism: heparin-induced thrombocytopenia. Blood Adv, 2018.](https://doi.org/10.1182/bloodadvances.2018024489)

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

Low probability of HIT (0 to 3 points)

ASH 2018: do not measure anti-PF4 antibodies and continue heparin, looking for another cause.


### 2

Intermediate probability (4 to 5 points)

Stop all heparin, start a non-heparin anticoagulant at therapeutic dose, and measure anti-PF4.


### 3

High probability (6 to 8 points)

Stop all heparin, start a non-heparin anticoagulant at therapeutic dose, and confirm with anti-PF4 (and functional assay).


### 4

High probability (6 to 8 points)

Stop all heparin, start a non-heparin anticoagulant at therapeutic dose, and confirm with anti-PF4 (and functional assay).

