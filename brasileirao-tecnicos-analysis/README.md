# Brasileirão Série A - Análise de Técnicos (2016–2025)

Análise exploratória do Campeonato Brasileiro Série A com foco no 
desempenho e aproveitamento de técnicos ao longo de 10 temporadas.

## Pergunta central
Quais técnicos tiveram o melhor aproveitamento no Brasileirão entre 
2016 e 2025, e a permanência no cargo está associada a melhores resultados?

## Principais achados
- **3.799 partidas** analisadas, com **34 clubes** e **497 técnicos** 
  diferentes registrados no período
- O fator mando de campo é expressivo: times mandantes venceram **47.8%** 
  das partidas, contra apenas **25%** dos visitantes
- **Palmeiras (210)** e **Flamengo (206)** dominam em vitórias absolutas, 
  bem acima do terceiro colocado Atlético-MG (164)
- Técnicos com 50+ jogos têm média de aproveitamento de **41.2%**, 
  contra **34.4%** da média geral - permanência está associada a resultados
- **Renato Gaúcho no Grêmio** é o caso de maior longevidade: 231 jogos 
  com 44.6% de aproveitamento
- **Abel Ferreira no Palmeiras** combina volume (152 jogos) com o melhor 
  aproveitamento entre técnicos de longa data: **53.3%**

## Notebooks
| Notebook | Descrição |
|---|---|
| `01_exploracao.ipynb` | Inspeção do dataset, distribuição de resultados e top 5 clubes |
| `02_aproveitamento_tecnicos.ipynb` | Métrica de aproveitamento por técnico/clube, scatter plot e ranking |

## Tecnologias
Python · Pandas · NumPy · Matplotlib

## Dataset
[Campeonato Brasileiro Série A - Kaggle](https://www.kaggle.com/datasets/adaoduque/campeonato-brasileiro-serie-a)
