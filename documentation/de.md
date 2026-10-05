<!-- ELUCENIA technical documentation · heart-score · de · no clinical/professional/rights approval -->

# HEART-Score

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/heart-score)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Anamnese

`h`

- `0` — Geringer Verdacht
- `1` — Mäßig verdächtig
- `2` — Stark verdächtig

### EKG

`e`

- `0` — Normal
- `1` — Unspezifische Repolarisationsstörung
- `2` — Signifikante ST-Senkung

### Alter

`a`

- `0` — ≤ 45 Jahre
- `1` — \> 45 und \< 65 Jahre
- `2` — ≥ 65 Jahre

### Risikofaktoren

`r`

- `0` — Keiner
- `1` — 1 oder 2
- `2` — ≥ 3 oder bekannte atherosklerotische Erkrankung

### Troponin

`t`

- `0` — ≤ Normgrenze
- `1` — \> 1× und \< 3× die obere Normgrenze
- `2` — ≥ 3× die obere Normgrenze

## Fassung der Methode

HEART/Backus 2013: 5 Komponenten mit 0–2 Punkten, insgesamt 0–10; Alter ≤45, \>45 und \<65, ≥65 Jahre; Troponin ≤obere Normgrenze, \>1×obere Normgrenze und \<3×obere Normgrenze, ≥3×obere Normgrenze; nicht der HEART Pathway mit serieller Untersuchung

## Dokumentierte Formel

Je Merkmal 0 bis 2 Punkte: History (Anamnese), EKG, Age (Alter), Risk factors (Risikofaktoren), Troponin. Gesamt 0 bis 10.

Risikofaktoren: Hypertonie, Dyslipidämie, Diabetes, Adipositas (BMI \> 30), aktuelles oder kürzliches Rauchen, familiäre vorzeitige KHK.

## Grenzen und Population

Der ursprüngliche HEART wurde bei Notfallpatienten mit Brustschmerzen und Verdacht auf ein Koronarsyndrom ohne ST-Hebung untersucht. Ein niedriger Score bedeutet kein Nullrisiko; die Originalsumme entspricht nicht dem HEART Pathway mit serieller Beurteilung. Entlassungssicherheit, Troponinzeitpunkte und Ausschlüsse erfordern das entsprechende Protokoll.

## Referenzen

- [Six AJ, Backus BE, Kelder JC. Chest pain in the emergency room: value of the HEART score. Neth Heart J, 2008.](https://doi.org/10.1007/BF03086144)

- [Backus BE et al. A prospective validation of the HEART score for chest pain patients at the emergency department. Int J Cardiol, 2013.](https://doi.org/10.1016/j.ijcard.2013.01.255)

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
