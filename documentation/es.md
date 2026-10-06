<!-- ELUCENIA technical documentation · 4ts-trombocitopenia-por-heparina · es · no clinical/professional/rights approval -->

# Puntuación 4T (trombocitopenia inducida por heparina)

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/4ts-trombocitopenia-por-heparina)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Trombocitopenia

`trombo`

- `0` — Caída \< 30% o nadir \< 10.000/µL
- `1` — Caída del 30% al 50% o nadir de 10.000 a 19.000/µL
- `2` — Caída \> 50% y nadir ≥ 20.000/µL

### Momento de la caída de plaquetas

`tempo`

- `0` — Caída antes del día 4 sin exposición reciente
- `1` — Compatible con los días 5–10, pero incierto; después del día 10; o ≤ 1 día con heparina hace 30 a 100 días
- `2` — Inicio claro entre los días 5 y 10, o ≤ 1 día con exposición a heparina en los últimos 30 días

### Trombosis u otras secuelas

`trombose`

- `0` — Ninguna
- `1` — Trombosis progresiva o recurrente, lesión cutánea no necrótica o sospecha de trombosis
- `2` — Trombosis nueva confirmada, necrosis cutánea o reacción sistémica tras un bolo

### Otras causas de trombocitopenia

`outras`

- `0` — Definida
- `1` — Posible
- `2` — Ninguna aparente

## Edición del método

4Ts/Lo 2006: 4 dominios 0–2, total 0–8; contexto ASH 2018

## Fórmula documentada

Cuatro ítems, 0 a 2 cada uno: Trombocitopenia · Tiempo · Trombosis · oTras causas. Máximo: 8.

## Límites y población

Estima la probabilidad clínica preprueba ante sospecha de HIT tras exposición a heparina. Depende de la historia plaquetaria, temporal, trombótica y de causas alternativas. El resultado no confirma HIT; los valores predictivos variaron entre los escenarios estudiados.

## Referencias

- [Lo GK et al. Evaluation of pretest clinical score (4 T's) for the diagnosis of heparin-induced thrombocytopenia in two clinical settings. J Thromb Haemost, 2006.](https://doi.org/10.1111/j.1538-7836.2006.01787.x)

- [Cuker A et al. American Society of Hematology 2018 guidelines for management of venous thromboembolism: heparin-induced thrombocytopenia. Blood Adv, 2018.](https://doi.org/10.1182/bloodadvances.2018024489)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

La información siguiente conserva las salidas del método para ejemplos sintéticos. No constituye una validación clínica independiente.

### 1

Baja probabilidad de TIH (0 a 3 puntos)

ASH 2018: no dosar anticuerpos anti-PF4 y mantener la heparina, buscando otra causa.


### 2

Probabilidad intermedia (4 a 5 puntos)

Suspender toda heparina, iniciar anticoagulante no heparínico en dosis terapéutica y dosar anti-PF4.


### 3

Alta probabilidad (6 a 8 puntos)

Suspender toda heparina, iniciar anticoagulante no heparínico en dosis terapéutica y confirmar con anti-PF4 (y ensayo funcional).


### 4

Alta probabilidad (6 a 8 puntos)

Suspender toda heparina, iniciar anticoagulante no heparínico en dosis terapéutica y confirmar con anti-PF4 (y ensayo funcional).

