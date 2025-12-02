## Desafio Telecom X BR
## 📈 Análise Exploratória de Dados sobre Evasão de Clientes (Churn) - Tech Foundation : Especialização Data Science - Módulo : Aprendendo a Fazer ETL (Oracle Next Education G9 BR)
Este projeto, o segundo da terceira etapa na Tech Foundation 2 do ONE (Oracle Next Education) G9 BR, tem como objetivo realizar uma análise detalhada sobre possíveis motivos da evasão de clientes. Desenvolvido em Python no ambiente Google Colab, o notebook permite extrair dados da API, processar e tranformar o dataset, visualizar métricas importantes, identificar padrões e gerar insights para posterior modelagem preditiva e tomada de decisão.

---

## 📌 Objetivo

Utilizando Python e suas principais bibliotecas, coletar, tratar e analisar dados, extraindo insights valiosos para que os demais colegas da equipe de Data Science, avancem para modelos preditivos e consigam desenvolver estratégias para reduzir a evasão (Churn).

---


## 🛠️ Tecnologias Utilizadas

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-purple?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?logo=matplotlib&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-teal?logo=seaborn&logoColor=white)

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

## 💡 Etapas do Projeto :

1. Importação e carga dos dados
2. Limpeza e padronização
3. Análise Descritiva
4. Análise do Churn
5. Matriz de Correlação
6. ETAPA EXTRA — Análise Avançada de Correlação
7. Conclusões
8. Ações recomendadas

---

## 📊 Visualizações & Insights :

1. Distribuição do Churn — Proporção de clientes que permaneceram vs. saíram.
Insight: 26% da base churnou; variável desbalanceada, exige cuidado nas métricas de modelo. 
2. Churn por Tipo de Contrato — Comparação de taxas de evasão entre Month-to-month, One year, Two year.
Insight: Contratos Month-to-month apresentam a maior taxa de churn — fidelização reduz evasão.
3. Tenure x Churn (Boxplot) — Distribuição do tempo de permanência por grupo (churn/no churn).
Insight: Clientes com tenure baixo concentram a maior parte do churn — onboarding crítico nos primeiros meses.
4. Custo Mensal x Churn (Boxplot) — Comparação do ticket médio mensal entre quem ficou e quem saiu.
Insight: Existe tendência de churn maior entre clientes com Custo Mensal elevado — sensibilidade a preço.
5. Total de Serviços Contratados x Churn — Quantos addons/serviços cada cliente usa vs. churn.
Insight: Maior número de serviços = menor churn. Engajamento por serviços protege contra evasão.

---

## 📎 Como Executar o Projeto

Instale as dependências:

pip install pandas matplotlib seaborn


Abra o notebook:

jupyter notebook

Execute as células na ordem.

---

## 📬 Contato

Projeto desenvolvido por Marcus  
📧 Email: [mclguedes@gmail.com]  
📱 LinkedIn: [https://www.linkedin.com/in/marcusguedes]
