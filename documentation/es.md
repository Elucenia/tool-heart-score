<!-- ELUCENIA technical documentation · heart-score · es · no clinical/professional/rights approval -->

# Puntuación HEART

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/heart-score)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Antecedentes

`h`

- `0` — Poco sospechosa
- `1` — Moderadamente sospechosa
- `2` — Muy sospechosa

### ECG

`e`

- `0` — Normal
- `1` — Alteración inespecífica de la repolarización
- `2` — Depresión significativa del ST

### Edad

`a`

- `0` — ≤ 45 años
- `1` — \> 45 y \< 65 años
- `2` — ≥ 65 años

### Factores de riesgo

`r`

- `0` — Ninguno
- `1` — 1 o 2
- `2` — ≥ 3 o enfermedad aterosclerótica conocida

### Troponina

`t`

- `0` — ≤ límite normal
- `1` — \> 1× y \< 3× el límite superior de la normalidad
- `2` — ≥ 3× el límite superior de la normalidad

## Edición del método

HEART/Backus 2013: 5 componentes de 0–2 puntos, total 0–10; edad ≤45, \>45 y \<65, ≥65 años; troponina ≤LSN, \>1×LSN y \<3×LSN, ≥3×LSN; no es el HEART Pathway con evaluación seriada

## Fórmula documentada

Suma de 0 a 2 por ítem: Historia, ECG, Age (edad), Risk factors (factores de riesgo), Troponina. Total de 0 a 10.

Factores de riesgo: hipertensión, dislipidemia, diabetes, obesidad (IMC \> 30), tabaquismo actual o reciente, antecedentes familiares de enfermedad coronaria precoz.

## Límites y población

El HEART original se estudió en urgencias en personas con dolor torácico y sospecha de síndrome coronario sin elevación del ST. Una puntuación baja no significa riesgo nulo y la suma original no equivale al HEART Pathway con evaluación seriada. La seguridad del alta, el momento de las troponinas y las exclusiones requieren el protocolo correspondiente.

## Referencias

- [Six AJ, Backus BE, Kelder JC. Chest pain in the emergency room: value of the HEART score. Neth Heart J, 2008.](https://doi.org/10.1007/BF03086144)

- [Backus BE et al. A prospective validation of the HEART score for chest pain patients at the emergency department. Int J Cardiol, 2013.](https://doi.org/10.1016/j.ijcard.2013.01.255)

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

Alto riesgo: estrategia invasiva precoz

| Detalles del resultado | |
| --- | --- |
| MACE a 6 semanas | 50,1% |


### 2

Bajo riesgo: considerar el alta con troponinas seriadas negativas y seguimiento ambulatorio

| Detalles del resultado | |
| --- | --- |
| MACE a 6 semanas | 1,7% |


### 3

Riesgo moderado: observación, troponina seriada e investigación no invasiva

| Detalles del resultado | |
| --- | --- |
| MACE a 6 semanas | 16,6% |

