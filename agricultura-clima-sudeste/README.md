# Impacto Climático na Produção Agrícola do Sudeste Brasileiro

Análise exploratória sobre a relação entre variáveis climáticas e produção agrícola no Sudeste do Brasil entre **2013 e 2023**.

O projeto investiga como temperatura, precipitação e períodos de estiagem se relacionam com a produção de culturas relevantes para a região, como **café**, **cana-de-açúcar**, **laranja** e **milho**.

## Sobre o Projeto

A agricultura é diretamente influenciada por variações climáticas. No Sudeste brasileiro, mudanças em padrões de chuva, temperatura média e ocorrência de dias secos podem afetar tanto a produtividade quanto a estabilidade da produção ao longo do tempo.

Este projeto busca explorar esses dados de forma visual e interpretativa, conectando indicadores climáticos com a evolução da produção agrícola regional.

## Objetivos

- Analisar a evolução da produção agrícola no Sudeste brasileiro entre **2013 e 2023**
- Identificar padrões nas variáveis climáticas do período
- Explorar a relação entre chuva, temperatura, estiagem e produção agrícola
- Comparar o comportamento das principais culturas analisadas
- Gerar insights sobre possíveis vulnerabilidades climáticas na produção agrícola

## Dados Utilizados

### Fontes

- **Produção Agrícola:** IBGE, Pesquisa Agrícola Municipal, PAM
- **Dados Climáticos:**
  - ERA5, ECMWF, para precipitação e dias secos consecutivos
  - CRU TS, Climatic Research Unit, para temperatura média

### Variáveis Agrícolas

- Quantidade produzida, em toneladas
- Culturas analisadas:
  - Café
  - Cana-de-açúcar
  - Laranja
  - Milho

### Variáveis Climáticas

- Temperatura média anual, em °C
- Precipitação total anual, em mm
- Dias secos consecutivos, CDD

### Recorte da Análise

- **Período:** 2013 a 2023
- **Região:** Sudeste do Brasil
- **Estados:** São Paulo, Minas Gerais, Rio de Janeiro e Espírito Santo

## Estrutura do Projeto

```text
agricultura-clima-sudeste/
│
├── data/
│   ├── raw/                          # Dados originais
│   └── processed/                    # Dados tratados e consolidados
│       └── dataset_agricultura_clima_completo.csv
│
├── notebooks/
│   ├── 01_exploracao.ipynb
│   └── 02_analise_chuva_producao_agricola_sudeste.ipynb
│
├── outputs/
│   └── figures/                      # Gráficos gerados nas análises
│
├── README.md
└── requirements.txt
```

## Notebooks

### 01_exploracao.ipynb

Notebook inicial de análise exploratória, focado em entender a estrutura do dataset, descrever as variáveis principais e observar padrões gerais da produção agrícola e dos indicadores climáticos.

### 02_analise_chuva_producao_agricola_sudeste.ipynb

Notebook focado na relação entre **chuva** e **produção agrícola**, explorando como a precipitação se comporta ao longo do período e como ela pode se relacionar com diferentes culturas analisadas.

## Principais Resultados

### Produção Agrícola

A **cana-de-açúcar** aparece como a cultura de maior volume produtivo no Sudeste, com participação muito superior às demais culturas analisadas. Esse comportamento mostra o peso da cultura na produção regional e ajuda a explicar sua influência no volume total observado.

Em contraste, culturas como **café**, **laranja** e **milho** apresentam volumes menores, mas continuam relevantes para entender a diversidade agrícola da região e sua possível sensibilidade a variações climáticas.

### Variáveis Climáticas

Os dados climáticos mostram oscilações importantes ao longo do período. A análise considera indicadores como **temperatura média**, **precipitação total anual** e **dias secos consecutivos**, permitindo observar tanto padrões gerais quanto anos de maior pressão climática.

Os períodos com maior número de dias secos consecutivos indicam possíveis momentos de estresse hídrico, especialmente relevantes para culturas mais dependentes da regularidade das chuvas.

### Relação entre Chuva e Produção

A análise da precipitação permite investigar se anos com maior ou menor volume de chuva coincidem com mudanças na produção agrícola. Essa relação não deve ser interpretada de forma isolada, já que produtividade também depende de fatores como tecnologia, manejo, solo, irrigação e mercado.

Ainda assim, observar a chuva em conjunto com a produção ajuda a levantar hipóteses importantes sobre vulnerabilidade climática e estabilidade produtiva no Sudeste brasileiro.

## Tecnologias Utilizadas

- **Python 3.x**
- **Pandas** para manipulação e análise dos dados
- **Matplotlib** para visualização dos dados
- **Jupyter Notebook** para desenvolvimento e documentação da análise

## Como Executar

### Pré-requisitos

Instale as dependências do projeto:

```bash
pip install -r requirements.txt
```

### Execução

Clone o repositório:

```bash
git clone https://github.com/seu-usuario/agricultura-clima-sudeste.git
cd agricultura-clima-sudeste
```

Abra os notebooks:

```bash
jupyter notebook notebooks/01_exploracao.ipynb
```

ou

```bash
jupyter notebook notebooks/02_analise_chuva_producao_agricola_sudeste.ipynb
```

## Possíveis Próximos Passos

- Analisar correlações entre variáveis climáticas e produção agrícola
- Comparar os impactos climáticos por cultura
- Investigar diferenças entre os estados do Sudeste
- Criar modelos preditivos simples para estimar produção a partir de variáveis climáticas
- Expandir a análise para outras regiões do Brasil

## Autor

**Dário Junio**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/dariojunio)

## Licença

Este projeto está sob a licença MIT.

## Agradecimentos

- IBGE pela disponibilização dos dados da Pesquisa Agrícola Municipal
- ECMWF pelos dados climáticos do ERA5
- Climatic Research Unit pelos dados de temperatura do CRU TS
- Comunidade Python de ciência de dados
