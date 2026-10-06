<!-- ELUCENIA technical documentation · heart-score · pt-BR · no clinical/professional/rights approval -->

# Escore HEART

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/heart-score)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### História

`h`

- `0` — Pouco suspeita
- `1` — Moderadamente suspeita
- `2` — Muito suspeita

### ECG

`e`

- `0` — Normal
- `1` — Alteração de repolarização inespecífica
- `2` — Infradesnível do ST significativo

### Idade

`a`

- `0` — ≤ 45 anos
- `1` — \> 45 e \< 65 anos
- `2` — ≥ 65 anos

### Fatores de risco

`r`

- `0` — Nenhum
- `1` — 1 ou 2
- `2` — ≥ 3 ou doença aterosclerótica conhecida

### Troponina

`t`

- `0` — ≤ limite normal
- `1` — \> 1× e \< 3× o limite normal
- `2` — ≥ 3× o limite normal

## Edição do método

HEART/Backus 2013: 5 componentes de 0–2 pontos, total 0–10; idade ≤45, \>45 e \<65, ≥65 anos; troponina ≤LSN, \>1×LSN e \<3×LSN, ≥3×LSN; sem HEART Pathway seriado

## Fórmula documentada

Soma de 0 a 2 pontos em cada item: História, ECG, Age (idade), Risk factors e Troponina. Total de 0 a 10.

Fatores de risco: hipertensão, dislipidemia, diabetes, obesidade (IMC \> 30), tabagismo atual ou recente, história familiar de DAC precoce.

## Limites e população

O HEART original foi estudado na emergência em pessoas com dor torácica e suspeita de síndrome coronariana sem supradesnível. Baixo escore não significa risco zero, e a soma original não é equivalente ao HEART Pathway com avaliação seriada. Segurança de alta, momento das troponinas e exclusões exigem o protocolo correspondente.

## Referências

- [Six AJ, Backus BE, Kelder JC. Chest pain in the emergency room: value of the HEART score. Neth Heart J, 2008.](https://doi.org/10.1007/BF03086144)

- [Backus BE et al. A prospective validation of the HEART score for chest pain patients at the emergency department. Int J Cardiol, 2013.](https://doi.org/10.1016/j.ijcard.2013.01.255)

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

Alto risco: Estratégia invasiva precoce

| Detalhes do resultado | |
| --- | --- |
| MACE em 6 semanas | 50,1% |


### 2

Baixo risco: Considerar alta com troponinas seriadas negativas e seguimento ambulatorial

| Detalhes do resultado | |
| --- | --- |
| MACE em 6 semanas | 1,7% |


### 3

Risco moderado: Observação, troponina seriada e investigação não invasiva

| Detalhes do resultado | |
| --- | --- |
| MACE em 6 semanas | 16,6% |

