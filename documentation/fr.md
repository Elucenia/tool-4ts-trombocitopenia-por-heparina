<!-- ELUCENIA technical documentation · 4ts-trombocitopenia-por-heparina · fr · no clinical/professional/rights approval -->

# Score 4T (thrombopénie induite par l’héparine)

[conditions, sources et autorisations](https://elucenia.org/fr/outils/4ts-trombocitopenia-por-heparina)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Thrombopénie

`trombo`

- `0` — Chute \< 30 % ou nadir \< 10 000/µL
- `1` — Chute de 30 % à 50 % ou nadir de 10 000 à 19 000/µL
- `2` — Chute \> 50 % et nadir ≥ 20 000/µL

### Délai de chute des plaquettes

`tempo`

- `0` — Chute avant le 4e jour sans exposition récente
- `1` — Compatible avec les jours 5–10 mais incertain ; après le 10e jour ; ou ≤ 1 jour avec exposition à l’héparine il y a 30 à 100 jours
- `2` — Début net entre le 5e et le 10e jour, ou ≤ 1 jour avec exposition à l’héparine dans les 30 derniers jours

### Thrombose ou autres séquelles

`trombose`

- `0` — Aucune
- `1` — Thrombose progressive ou récidivante, lésion cutanée non nécrotique ou suspicion de thrombose
- `2` — Nouvelle thrombose confirmée, nécrose cutanée ou réaction systémique après bolus

### Autres causes de thrombopénie

`outras`

- `0` — Certaine
- `1` — Possible
- `2` — Aucune apparente

## Édition de la méthode

4Ts/Lo 2006 : 4 domaines 0–2, total 0–8 ; contexte ASH 2018

## Formule documentée

Quatre items, 0 à 2 chacun : Thrombopénie · Temporalité · Thrombose · auTres causes. Maximum : 8.

## Limites et population

Estime la probabilité clinique prétest en cas de suspicion de TIH après exposition à l’héparine. Dépend de l’histoire plaquettaire, temporelle et thrombotique, et des causes alternatives. Le résultat ne confirme pas une TIH ; les valeurs prédictives variaient selon les contextes étudiés.

## Références

- [Lo GK et al. Evaluation of pretest clinical score (4 T's) for the diagnosis of heparin-induced thrombocytopenia in two clinical settings. J Thromb Haemost, 2006.](https://doi.org/10.1111/j.1538-7836.2006.01787.x)

- [Cuker A et al. American Society of Hematology 2018 guidelines for management of venous thromboembolism: heparin-induced thrombocytopenia. Blood Adv, 2018.](https://doi.org/10.1182/bloodadvances.2018024489)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Résultats documentés

Les informations ci-dessous conservent les sorties de la méthode pour des exemples synthétiques. Elles ne constituent pas une validation clinique indépendante.

### 1

Faible probabilité de TIH (0 à 3 points)

ASH 2018 : ne pas doser les anticorps anti-PF4 et maintenir l’héparine, en recherchant une autre cause.


### 2

Probabilité intermédiaire (4 à 5 points)

Arrêter toute héparine, instaurer un anticoagulant non héparinique à dose thérapeutique et doser les anti-PF4.


### 3

Probabilité élevée (6 à 8 points)

Arrêter toute héparine, instaurer un anticoagulant non héparinique à dose thérapeutique et confirmer par anti-PF4 (et test fonctionnel).


### 4

Probabilité élevée (6 à 8 points)

Arrêter toute héparine, instaurer un anticoagulant non héparinique à dose thérapeutique et confirmer par anti-PF4 (et test fonctionnel).

