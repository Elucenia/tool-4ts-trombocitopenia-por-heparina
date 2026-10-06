<!-- ELUCENIA technical documentation · 4ts-trombocitopenia-por-heparina · pt-BR · no clinical/professional/rights approval -->

# Escore 4T (trombocitopenia induzida por heparina)

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/4ts-trombocitopenia-por-heparina)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Trombocitopenia

`trombo`

- `0` — Queda \< 30% ou nadir \< 10.000/µL
- `1` — Queda de 30% a 50% ou nadir de 10.000 a 19.000/µL
- `2` — Queda \> 50% e nadir ≥ 20.000/µL

### Tempo da queda das plaquetas

`tempo`

- `0` — Queda antes do 4º dia sem exposição recente
- `1` — Compatível com 5º–10º dia, mas incerto; após o 10º dia; ou ≤ 1 dia com heparina há 30 a 100 dias
- `2` — Início claro entre o 5º e o 10º dia, ou ≤ 1 dia com heparina nos últimos 30 dias

### Trombose ou outras sequelas

`trombose`

- `0` — Nenhuma
- `1` — Trombose progressiva ou recorrente, lesão de pele não necrótica ou trombose suspeita
- `2` — Trombose nova confirmada, necrose de pele ou reação sistêmica após bolus

### Outras causas de plaquetopenia

`outras`

- `0` — Definida
- `1` — Possível
- `2` — Nenhuma aparente

## Edição do método

4 Ts/Lo 2006:4 domínios 0–2, total 0–8; contexto ASH 2018

## Fórmula documentada

Quatro itens, de 0 a 2 pontos cada: Trombocitopenia · Tempo · Trombose · ouTras causas. Máximo: 8.

## Limites e população

Estima probabilidade clínica pré-teste em suspeita de HIT após exposição à heparina. Depende da história plaquetária, temporal, trombótica e de causas alternativas. O resultado não confirma HIT; os valores preditivos variaram entre cenários estudados.

## Referências

- [Lo GK et al. Evaluation of pretest clinical score (4 T's) for the diagnosis of heparin-induced thrombocytopenia in two clinical settings. J Thromb Haemost, 2006.](https://doi.org/10.1111/j.1538-7836.2006.01787.x)

- [Cuker A et al. American Society of Hematology 2018 guidelines for management of venous thromboembolism: heparin-induced thrombocytopenia. Blood Adv, 2018.](https://doi.org/10.1182/bloodadvances.2018024489)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

As informações abaixo preservam as saídas do método para exemplos sintéticos. Não constituem validação clínica independente.

### 1

Baixa probabilidade de TIH (0 a 3 pontos)

ASH 2018: não dosar anticorpos anti-PF4 e manter a heparina, buscando outra causa.


### 2

Probabilidade intermediária (4 a 5 pontos)

Suspender toda heparina, iniciar anticoagulante não heparínico em dose terapêutica e dosar anti-PF4.


### 3

Alta probabilidade (6 a 8 pontos)

Suspender toda heparina, iniciar anticoagulante não heparínico em dose terapêutica e confirmar com anti-PF4 (e ensaio funcional).


### 4

Alta probabilidade (6 a 8 pontos)

Suspender toda heparina, iniciar anticoagulante não heparínico em dose terapêutica e confirmar com anti-PF4 (e ensaio funcional).

