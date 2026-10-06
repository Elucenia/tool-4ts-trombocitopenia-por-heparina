<!-- ELUCENIA technical documentation · 4ts-trombocitopenia-por-heparina · de · no clinical/professional/rights approval -->

# 4T-Score (heparininduzierte Thrombozytopenie)

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/4ts-trombocitopenia-por-heparina)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Thrombozytopenie

`trombo`

- `0` — Abfall \< 30 % oder Nadir \< 10.000/µL
- `1` — Abfall von 30 % bis 50 % oder Nadir von 10.000 bis 19.000/µL
- `2` — Abfall \> 50 % und Nadir ≥ 20.000/µL

### Zeitpunkt des Thrombozytenabfalls

`tempo`

- `0` — Abfall vor Tag 4 ohne kürzliche Exposition
- `1` — Mit Tag 5–10 vereinbar, aber unsicher; nach Tag 10; oder ≤ 1 Tag bei Heparinexposition vor 30 bis 100 Tagen
- `2` — Klarer Beginn zwischen Tag 5 und 10 oder ≤ 1 Tag bei Heparinexposition in den letzten 30 Tagen

### Thrombose oder andere Folgeerscheinungen

`trombose`

- `0` — Keine
- `1` — Fortschreitende oder rezidivierende Thrombose, nichtnekrotische Hautläsion oder Thromboseverdacht
- `2` — Neue bestätigte Thrombose, Hautnekrose oder systemische Reaktion nach Bolus

### Andere Ursachen der Thrombozytopenie

`outras`

- `0` — Gesichert
- `1` — Möglich
- `2` — Keine erkennbar

## Fassung der Methode

4Ts/Lo 2006: 4 Bereiche 0–2, Gesamt 0–8; ASH 2018-Kontext

## Dokumentierte Formel

Vier Items, jeweils 0 bis 2: Thrombozytopenie · Timing · Thrombose · andere Ursachen (T). Höchstens: 8.

## Grenzen und Population

Schätzt die klinische Vortestwahrscheinlichkeit bei Verdacht auf HIT nach Heparinexposition. Hängt vom Thrombozytenverlauf, zeitlichen Ablauf, Thrombosegeschehen und alternativen Ursachen ab. Das Ergebnis bestätigt keine HIT; Vorhersagewerte unterschieden sich zwischen den untersuchten Situationen.

## Referenzen

- [Lo GK et al. Evaluation of pretest clinical score (4 T's) for the diagnosis of heparin-induced thrombocytopenia in two clinical settings. J Thromb Haemost, 2006.](https://doi.org/10.1111/j.1538-7836.2006.01787.x)

- [Cuker A et al. American Society of Hematology 2018 guidelines for management of venous thromboembolism: heparin-induced thrombocytopenia. Blood Adv, 2018.](https://doi.org/10.1182/bloodadvances.2018024489)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Dokumentierte Ergebnisse

Die folgenden Angaben bewahren die Ausgaben der Methode für synthetische Beispiele. Sie stellen keine unabhängige klinische Validierung dar.

### 1

Geringe Wahrscheinlichkeit für HIT (0 bis 3 Punkte)

ASH 2018: keine Anti-PF4-Antikörper bestimmen und Heparin fortführen, nach einer anderen Ursache suchen.


### 2

Mittlere Wahrscheinlichkeit (4 bis 5 Punkte)

Jegliches Heparin absetzen, einen nicht-heparinischen Antikoagulans in therapeutischer Dosis beginnen und Anti-PF4 bestimmen.


### 3

Hohe Wahrscheinlichkeit (6 bis 8 Punkte)

Jegliches Heparin absetzen, einen nicht-heparinischen Antikoagulans in therapeutischer Dosis beginnen und mit Anti-PF4 (und Funktionstest) bestätigen.


### 4

Hohe Wahrscheinlichkeit (6 bis 8 Punkte)

Jegliches Heparin absetzen, einen nicht-heparinischen Antikoagulans in therapeutischer Dosis beginnen und mit Anti-PF4 (und Funktionstest) bestätigen.

