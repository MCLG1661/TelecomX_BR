## Desafio Telecom X BR
## 📈 Análise Exploratória de Dados sobre Evasão de Clientes (Churn) - Tech Foundation : Especialização Data Science - Módulo : Aprendendo a Fazer ETL (Oracle Next Education G9 BR)
Este projeto, o segundo da terceira etapa na Tech Foundation 2 do ONE (Oracle Next Education) G9 BR, tem como objetivo realizar uma análise detalhada sobre possíveis motivos da evasão de clientes. Desenvolvido em Python no ambiente Google Colab, o notebook permite extrair dados da API, processar e tranformar o dataset, visualizar métricas importantes, identificar padrões e gerar insights para posterior modelagem preditiva e tomada de decisão.

---

## 📌 Objetivo

Utilizando Python e suas principais bibliotecas, coletar, tratar e analisar dados. Extraindo insights valiosos para que os demais colegas da equipe de Data Science, avancem para modelos preditivos e consigam desenvolver estratégias para reduzir a evasão (Churn).

---

## 🛠️ Tecnologias Utilizadas

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-purple?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?logo=matplotlib&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-teal?logo=seaborn&logoColor=white)

---

## 🔍 Etapas (Análise da distribuição da variável alvo (Churn) para entender o equilíbrio entre clientes que ficaram e os que cancelaram.)

1. Importação e carga dos dados

Leitura da base via pandas.

Verificação inicial com head(), info() e describe().

2. Limpeza e padronização

Ajuste de strings (lower, replace, strip).

Conversão de variáveis numéricas.

Tratamento de missing values.

Ajuste de inconsistências (gênero, contrato, serviços).

3. Análise Descritiva

Estatísticas de distribuição usando .describe().

Avaliação de variáveis importantes (idade, tenure, monthly charges etc.).

4. Análise do Churn

Visualização da proporção churn vs não churn.

Gráficos de barras para variáveis categóricas:

tipo de contrato

método de pagamento

gênero

serviços adicionais

internet, addon, segurança etc.

5. Matriz de Correlação

Seleção apenas de colunas numéricas.

Cálculo da matriz de correlação.

Heatmap para identificar variáveis relevantes.

---

## 🎯 Objetivo da etapa:

Garantir que os dados estejam prontos para serem explorados de forma mais profunda, além de fornecer uma visão inicial das variáveis que poderão influenciar a evasão dos clientes.

---

## 📊 Distribuição do Churn

Proporção (%)
<table> <tr> <th>Churn</th> <th>Proporção</th> </tr> <tr> <td>No</td> <td>71.2%</td> </tr> <tr> <td>Yes</td> <td>25.7%</td> </tr> <tr> <td>Nulo*</td> <td>3.1%</td> </tr> </table>

Cerca de 3% dos registros apresentam valores nulos ou inconsistentes.

---

## Contagem Absoluta
<table> <tr> <th>Churn</th> <th>Contagem</th> </tr> <tr> <td>No</td> <td>5174</td> </tr> <tr> <td>Yes</td> <td>1869</td> </tr> </table>

---

## 📝 Resumo da Análise de Churn – Telecom X BR (Principais Insights da EDA)

- A base contém 7.267 clientes, dos quais 26,5% evadiram. Trata-se de um índice elevado e que indica oportunidades de ação estratégica.

- Os principais fatores associados ao churn foram :

1 - Tipo de contrato : clientes Month-to-month apresentam a maior taxa de churn, enquanto contratos anuais têm as menores taxas.

2 - Serviços de segurança online e suporte técnico: clientes sem OnlineSecurity e sem TechSupport têm churn significativamente maior.

3 - Formas de pagamento: o método Electronic Check concentra a maior proporção de evasão.

4 - Tempo de casa (tenure): clientes com menos meses de serviço apresentam maior probabilidade de evasão.

5 - Mensalidade (Monthly Charges): valores mais altos estão associados a maior churn.

Esses padrões sugerem que ações de retenção devem priorizar clientes com contrato mensal, sem serviços complementares e com mensalidades mais altas, especialmente nos primeiros meses de relacionamento.

---

## 📋 Estatísticas Gerais do Dataset

🔠 Variáveis Categóricas (Resumo)
<table> <tr> <th>Coluna</th> <th>Categorias</th> <th>Mais Comum</th> <th>Frequência</th> </tr> <tr> <td>gender</td> <td>2</td> <td>Male</td> <td>3675</td> </tr> <tr> <td>Partner</td> <td>2</td> <td>No</td> <td>3749</td> </tr> <tr> <td>InternetService</td> <td>3</td> <td>Fiber optic</td> <td>3198</td> </tr> <tr> <td>Contract</td> <td>3</td> <td>Month-to-month</td> <td>4005</td> </tr> <tr> <td>PaymentMethod</td> <td>4</td> <td>Electronic check</td> <td>2445</td> </tr> </table>

🔢 Variáveis Numéricas (Resumo)
<table> <tr> <th>Coluna</th> <th>Média</th> <th>Desvio Padrão</th> <th>Mín.</th> <th>Q1</th> <th>Mediana</th> <th>Q3</th> <th>Máx.</th> </tr> <tr> <td>SeniorCitizen</td> <td>0.163</td> <td>0.369</td> <td>0.0</td> <td>0.0</td> <td>0.0</td> <td>0.0</td> <td>1.0</td> </tr> <tr> <td>tenure</td> <td>32.35</td> <td>24.57</td> <td>0.0</td> <td>9.0</td> <td>29.0</td> <td>55.0</td> <td>72.0</td> </tr> <tr> <td>Monthly</td> <td>64.72</td> <td>30.13</td> <td>18.25</td> <td>35.43</td> <td>70.30</td> <td>89.88</td> <td>118.75</td> </tr> <tr> <td>Total</td> <td>2280.63</td> <td>2268.63</td> <td>18.8</td> <td>400.23</td> <td>1391.00</td> <td>3785.30</td> <td>8684.8</td> </tr> </table>

---

## 📎 Como Executar o Projeto

Instale as dependências:

pip install pandas matplotlib seaborn


Abra o notebook:

jupyter notebook


Execute as células na ordem.

---

## 📂 Estrutura do Projeto

telecomx-churn/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   ├── raw/                  # dados originais (não editar)
│   │   └── TelecomX_Data.json
│   ├── interim/              # dados parcialmente processados (opcional)
│   └── processed/            # dataset final pronto para modelagem
│       └── telecomx_limpo.csv
├── notebooks/
│   ├── 01_data_loading.ipynb         # ETAPA 1-4: extração, limpeza inicial
│   ├── 02_data_cleaning_etl.ipynb    # ETAPA 4B e 5 (ajustes, Contas_Diarias)
│   ├── 03_eda.ipynb                  # ETAPA 6-8: análise descritiva e gráficos
│   └── 04_correlation_and_insights.ipynb  # ETAPA 9-10: correlações e conclusões
├── src/
│   ├── __init__.py
│   ├── data.py               # funções para carregar / salvar / transformar
│   ├── cleaning.py           # funções reutilizáveis de limpeza e padronização
│   ├── features.py           # funções de feature engineering (Contas_Diarias, bins)
│   └── viz.py                # funções que geram gráficos (reutilizáveis)
├── reports/
│   ├── figures/              # imagens geradas (png) para README ou relatório
│   └── final_report.md       # relatório sumarizado (pode ser movido pro README)
├── docs/
│   └── data_dictionary.md    # dicionário de dados e definições das colunas
├── tests/                    # testes unitários (opcional mas recomendado)
│   └── test_data.py
└── notebooks_export/         # versões exportadas (html/pdf) dos notebooks


---

## 📬 Contato

Projeto desenvolvido por Marcus  
📧 Email: [mclguedes@gmail.com]  
📱 LinkedIn: [https://www.linkedin.com/in/marcusguedes]
