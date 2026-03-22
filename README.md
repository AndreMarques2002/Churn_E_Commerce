# 🛒 E-commerce Customer Churn Prediction: Uma Abordagem Orientada a Dados

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine_Learning-orange?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Wrangling-green?logo=pandas&logoColor=white)](https://pandas.pydata.org/)

## 📌 O Problema de Negócio
No setor de varejo e e-commerce, o custo de aquisição de um novo cliente (CAC) é significativamente maior do que o custo de retenção. O "Churn" (cancelamento ou abandono da plataforma) representa uma perda direta de receita e diminuição do *Lifetime Value* (LTV). 

O objetivo deste projeto é desenvolver um modelo preditivo de Machine Learning capaz de identificar proativamente clientes com alta probabilidade de abandonar a plataforma, permitindo que as equipes de Marketing e CRM atuem com campanhas de retenção direcionadas antes que a perda se concretize.

## 📊 O Conjunto de Dados
Os dados utilizados simulam o banco de dados transacional e comportamental de um e-commerce, contendo informações sobre:
* **Demografia:** Estado civil, gênero, localização.
* **Comportamento no App:** Horas gastas no aplicativo, número de dispositivos registrados.
* **Histórico Transacional:** Dias desde a última compra, uso de cupons, categoria preferida.
* **Métricas de Satisfação:** Reclamações abertas, pontuação de satisfação.

## 🛠️ Arquitetura e Tecnologias Utilizadas
Este projeto simula o início de uma esteira analítica moderna, com os dados modelados em Python podendo ser facilmente integrados a pipelines em nuvem (GCP) e dashboards executivos (Power BI).

* **Linguagem:** Python
* **Manipulação de Dados:** Pandas, NumPy
* **Visualização:** Matplotlib, Seaborn
* **Modelagem Preditiva:** Scikit-Learn (Random Forest Classifier)

## 🧠 Metodologia Aplicada
1. **Data Wrangling:** Tratamento de valores nulos utilizando a mediana para evitar distorções por outliers e remoção de colunas não preditivas (ID).
2. **Análise Exploratória (EDA):** Identificação visual de padrões de cancelamento cruzando variáveis demográficas e comportamentais.
3. **Feature Engineering:** Transformação de variáveis categóricas via *One-Hot Encoding*.
4. **Machine Learning:** Treinamento de um algoritmo *Random Forest*. A escolha deste modelo se deu pela sua robustez contra outliers e excelente capacidade de explicabilidade (*Feature Importance*).

## 📈 Resultados e Métricas de Negócio
No contexto de Churn, o erro mais caro para a empresa é o **Falso Negativo** (o modelo prever que o cliente vai ficar, mas ele sai), resultando em perda de receita sem nenhuma tentativa de retenção. 

Por isso, o modelo foi otimizado com foco na métrica de **Recall**, garantindo a captura da maior quantidade possível de clientes em risco.

* **Insights da Importância das Variáveis (Feature Importance):**
  O modelo revelou matematicamente que o **Tempo de Casa (Tenure)** e a **Abertura de Reclamações (Complain)** são os maiores preditores de abandono.

## 💡 Recomendações Estratégicas
Com base nas predições geradas, sugere-se as seguintes ações para a operação:
1. **Fila Prioritária de SAC (Red Tag):** Clientes que abrem reclamações (`Complain = 1`) possuem uma taxa de churn drasticamente maior. O atendimento a esses clientes deve ser priorizado com políticas agressivas de reversão.
2. **Onboarding Gamificado:** Como o baixo tempo de casa (`Tenure`) é um forte indicativo de saída, sugere-se a criação de um programa de incentivos para as primeiras 3 compras, visando fidelizar o cliente na fase mais crítica.

## 🚀 Como Executar o Projeto
1. Clone este repositório:
   ```bash
   git clone [https://github.com/SeuUsuario/ecommerce-churn-prediction.git](https://github.com/SeuUsuario/ecommerce-churn-prediction.git)

2. Instale as dependências:

   ```bash
   pip install -r requirements.txt

3. Execute o notebook churn_analysis_model.ipynb para visualizar todo o pipeline de dados e os gráficos gerados.

