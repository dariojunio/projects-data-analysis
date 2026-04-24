# Impacto Climático na Produção Agrícola do Sudeste Brasileiro

Análise exploratória da relação entre variáveis climáticas e produção agrícola no Sudeste do Brasil (2013-2023).

## Sobre o Projeto

Este projeto investiga como variações climáticas (temperatura, precipitação e períodos de estiagem) afetam a produção das principais culturas agrícolas do Sudeste brasileiro: café, cana-de-açúcar, laranja e milho.

### Objetivos

- Analisar a evolução da produção agrícola no Sudeste entre 2013 e 2023
- Identificar padrões e tendências nas variáveis climáticas do período
- Explorar possíveis correlações entre clima e produtividade agrícola
- Gerar insights sobre a vulnerabilidade climática de diferentes culturas

## Dados

### Fontes

- **Produção Agrícola**: IBGE - Pesquisa Agrícola Municipal (PAM)
- **Dados Climáticos**: 
  - ERA5 (ECMWF) - Precipitação e CDD
  - CRU TS (Climatic Research Unit) - Temperatura

### Variáveis

**Agrícolas:**
- Quantidade produzida (toneladas)
- Culturas: Café, Cana-de-açúcar, Laranja, Milho

**Climáticas:**
- Temperatura média anual (°C)
- Precipitação total anual (mm)
- Dias secos consecutivos - CDD (dias)

**Período**: 2013 a 2023 (11 anos)  
**Região**: Sudeste (SP, MG, RJ, ES)

## Estrutura do Projeto

```
agricultura-clima-sudeste/
│
├── data/
│   ├── raw/                          # Dados originais (não processados)
│   └── processed/                    # Dados limpos e consolidados
│       └── dataset_agricultura_clima_completo.csv
│
├── notebooks/
│   └── 01_exploracao.ipynb          # Análise exploratória inicial
│
├── outputs/
│   └── figures/                      # Gráficos e visualizações
│
├── README.md
└── requirements.txt
```

## Principais Resultados

### Produção Agrícola

- **Cana-de-açúcar** domina a produção do Sudeste com mais de 5 bilhões de toneladas no período
- **Laranja** e **Café** representam culturas importantes mas com volumes significativamente menores
- Produção total apresenta tendência de crescimento no período analisado

### Variabilidade Climática

**Dias Secos Consecutivos (CDD):**
- Média histórica: 53 dias
- Anos extremos de seca: 2020 (62 dias) e 2017 (61 dias)
- Aumento aparente na variabilidade climática nos últimos anos

**Temperatura:**
- Média do período: 25,7°C
- Variação térmica relativamente estável (amplitude de 0,5°C)
- Ano mais quente: 2015 (26,0°C)

## Tecnologias Utilizadas

- **Python 3.x**
- **Pandas** - Manipulação e análise de dados
- **Matplotlib** - Visualização de dados
- **Jupyter Notebook** - Desenvolvimento e documentação

## Como Executar

### Pré-requisitos

```bash
pip install -r requirements.txt
```

### Execução

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/agricultura-clima-sudeste.git
cd agricultura-clima-sudeste
```

2. Instale as dependências:
```bash
pip install -r requirements.txt
```

3. Abra o notebook:
```bash
jupyter notebook notebooks/01_exploracao.ipynb
```

## Autor

**Dário Junio**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/dariojunio)

## Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

## Agradecimentos

- IBGE pela disponibilização dos dados de produção agrícola
- ECMWF (ERA5) e CRU pelos dados climáticos
- Comunidade Python de ciência de dados
