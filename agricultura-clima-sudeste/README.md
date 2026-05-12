# Impacto Climático na Produção Agrícola do Sudeste Brasileiro

Análise exploratória sobre a relação entre variáveis climáticas e produção agrícola no Sudeste do Brasil entre 2013 e 2023.

O projeto cruza dados de produção agrícola com indicadores climáticos para investigar como chuva, temperatura média e períodos de estiagem aparecem associados ao comportamento de culturas relevantes para a região, como café, cana-de-açúcar, laranja e milho.

## Sobre o Projeto

A agricultura é diretamente influenciada por variações climáticas. No Sudeste brasileiro, mudanças nos padrões de chuva, temperatura e ocorrência de dias secos podem afetar a estabilidade da produção ao longo do tempo.

Este projeto usa dados públicos para transformar essa pergunta em uma análise visual e interpretativa. O objetivo não é provar causalidade, mas identificar padrões, levantar hipóteses e mostrar como dados podem apoiar discussões sobre vulnerabilidade climática na agricultura.

## Objetivos

- Analisar a evolução da produção agrícola no Sudeste brasileiro entre 2013 e 2023
- Identificar padrões nas variáveis climáticas do período
- Explorar a relação entre precipitação, temperatura, estiagem e produção agrícola
- Comparar o comportamento de café, cana-de-açúcar, laranja e milho
- Gerar insights exploratórios sobre possíveis vulnerabilidades climáticas na produção agrícola regional

## Dados Utilizados

### Fontes

- Produção agrícola: IBGE, Pesquisa Agrícola Municipal (PAM)
- Dados climáticos:
  - ERA5 / ECMWF, para precipitação e dias secos consecutivos
  - CRU TS / Climatic Research Unit, para temperatura média

### Recorte da análise

- Período: 2013 a 2023
- Região: Sudeste do Brasil
- Estados: São Paulo, Minas Gerais, Rio de Janeiro e Espírito Santo
- Culturas analisadas: café, cana-de-açúcar, laranja e milho

### Variáveis

- Quantidade produzida, em toneladas
- Temperatura média anual, em graus Celsius
- Precipitação total anual, em milímetros
- Dias secos consecutivos (CDD)

## Estrutura do Projeto

```text
agricultura-clima-sudeste/
|
├── data/
│   ├── raw/
│   │   └── .gitkeep
│   └── processed/
│       ├── agro_clima.csv
│       └── clima_brasil_2013_2023.csv
|
├── notebooks/
│   ├── 01_exploracao.ipynb
│   └── 02_chuva_producao_agricola_sudeste.ipynb
|
├── outputs/
│   └── figures/
│       ├── graf1.png
│       ├── graf2.png
│       ├── graf3.png
│       └── graf4.png
|
├── README.md
└── requirements.txt
```

## Notebooks

### 01_exploracao.ipynb

Notebook inicial de análise exploratória. Nele são avaliadas a estrutura do dataset, a ausência de valores nulos, estatísticas descritivas, concentração da produção por cultura e evolução de variáveis climáticas como dias secos consecutivos e temperatura média.

### 02_chuva_producao_agricola_sudeste.ipynb

Notebook focado na relação entre precipitação e produção agrícola. A análise compara as culturas por meio de gráficos de dispersão, calcula correlações de Spearman e aprofunda o recorte da laranja para observar a produção em diferentes faixas de chuva.

## Principais Resultados

### Produção agrícola

A cana-de-açúcar é a cultura dominante em volume no Sudeste, com aproximadamente 5,57 bilhões de toneladas produzidas no período analisado.

No mesmo recorte, os totais aproximados foram:

- Cana-de-açúcar: 5,57 bilhões de toneladas
- Laranja: 153,9 milhões de toneladas
- Milho: 129,2 milhões de toneladas
- Café: 29,2 milhões de toneladas

Esse contraste mostra que a produção regional é fortemente concentrada em cana-de-açúcar, enquanto as demais culturas ajudam a revelar diferenças de comportamento e sensibilidade dentro do conjunto analisado.

### Variáveis climáticas

Os dias secos consecutivos apresentaram variação importante ao longo do período:

- Média do período: cerca de 53 dias secos consecutivos
- Maior valor: 2020, com aproximadamente 62 dias
- Segundo maior valor: 2017, com aproximadamente 61 dias
- Menores valores: 2013 e 2014, com cerca de 42 dias

A temperatura média anual ficou relativamente estável, próxima de 25,7 graus Celsius, com maior valor em 2015 e menor valor em 2022.

### Relação entre chuva e produção

Na análise exploratória, todas as culturas apresentaram correlação negativa entre precipitação total anual e quantidade produzida:

- Milho: -0,56
- Laranja: -0,35
- Cana-de-açúcar: -0,26
- Café: -0,15

O milho apresentou a relação negativa mais forte no recorte analisado. A laranja também mostrou um padrão relevante e foi analisada em maior detalhe.

No caso da laranja, a precipitação variou de 1.428,39 mm a 1.873,10 mm. A maior média de produção apareceu na faixa de menor chuva, mas essa faixa possui apenas um registro. Por isso, o resultado deve ser lido como um indício exploratório, não como uma conclusão definitiva.

## Cuidados na Interpretação

Os resultados deste projeto devem ser interpretados com cautela. Correlação não significa causalidade, e a produção agrícola depende de diversos fatores além do clima, como:

- Área plantada
- Tecnologia e manejo agrícola
- Irrigação
- Solo
- Pragas e doenças
- Preços e condições de mercado
- Políticas públicas e decisões produtivas

Assim, o projeto funciona como uma análise exploratória para levantar hipóteses e orientar investigações futuras.

## Tecnologias Utilizadas

- Python
- Pandas
- Matplotlib
- NumPy
- Jupyter Notebook

## Como Executar

Clone o repositório:

```bash
git clone https://github.com/dariojunio/projects-data-analysis.git
cd projects-data-analysis/agricultura-clima-sudeste
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Abra os notebooks:

```bash
jupyter notebook notebooks/01_exploracao.ipynb
```

ou:

```bash
jupyter notebook notebooks/02_chuva_producao_agricola_sudeste.ipynb
```

Observação: dependendo da pasta a partir da qual o Jupyter Notebook for executado, pode ser necessário ajustar o caminho de leitura dos dados para `data/processed/agro_clima.csv`.

## Possíveis Próximos Passos

- Analisar produtividade, e não apenas produção total
- Comparar os impactos climáticos por cultura
- Investigar diferenças entre os estados do Sudeste
- Incluir área plantada e rendimento médio por hectare
- Testar defasagens entre clima e produção, considerando que efeitos climáticos podem aparecer em anos posteriores
- Criar modelos preditivos simples para estimar produção a partir de variáveis climáticas
- Expandir a análise para outras regiões do Brasil

## Autor

Dário Junio

## Licença

Este projeto está sob a licença MIT.

## Agradecimentos

- IBGE pela disponibilização dos dados da Pesquisa Agrícola Municipal
- ECMWF pelos dados climáticos do ERA5
- Climatic Research Unit pelos dados de temperatura do CRU TS
- Comunidade Python de ciência de dados
