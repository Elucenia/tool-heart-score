<!-- ELUCENIA technical documentation · heart-score · fr · no clinical/professional/rights approval -->

# Score HEART

[conditions, sources et autorisations](https://elucenia.org/fr/outils/heart-score)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Antécédents

`h`

- `0` — Peu suspecte
- `1` — Modérément suspecte
- `2` — Très suspecte

### ECG

`e`

- `0` — Normal
- `1` — Anomalie non spécifique de la repolarisation
- `2` — Sous-décalage significatif du ST

### Âge

`a`

- `0` — ≤ 45 ans
- `1` — \> 45 et \< 65 ans
- `2` — ≥ 65 ans

### Facteurs de risque

`r`

- `0` — Aucun
- `1` — 1 ou 2
- `2` — ≥ 3 ou maladie athéroscléreuse connue

### Troponine

`t`

- `0` — ≤ limite normale
- `1` — \> 1× et \< 3× la limite supérieure de la normale
- `2` — ≥ 3× la limite supérieure de la normale

## Édition de la méthode

HEART/Backus 2013 : 5 composantes cotées de 0–2 points, total 0–10 ; âge ≤45, \>45 et \<65, ≥65 ans ; troponine ≤LSN, \>1×LSN et \<3×LSN, ≥3×LSN ; ce n’est pas le HEART Pathway avec évaluations répétées

## Formule documentée

Somme de 0 à 2 points par item : Histoire, ECG, Age (âge), Risk factors (facteurs de risque), Troponine. Total de 0 à 10.

Facteurs de risque : hypertension, dyslipidémie, diabète, obésité (IMC \> 30), tabagisme actuel ou récent, antécédents familiaux de coronaropathie précoce.

## Limites et population

Le HEART original a été étudié aux urgences chez des personnes présentant une douleur thoracique et une suspicion de syndrome coronarien sans sus-décalage ST. Un faible score ne signifie pas un risque nul, et la somme originale n’est pas équivalente au HEART Pathway avec évaluations répétées. La sécurité d’une sortie, le moment des dosages de troponine et les exclusions exigent le protocole correspondant.

## Références

- [Six AJ, Backus BE, Kelder JC. Chest pain in the emergency room: value of the HEART score. Neth Heart J, 2008.](https://doi.org/10.1007/BF03086144)

- [Backus BE et al. A prospective validation of the HEART score for chest pain patients at the emergency department. Int J Cardiol, 2013.](https://doi.org/10.1016/j.ijcard.2013.01.255)

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
