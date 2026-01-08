# 🧠 TEDAS — - Tecnologias Disruptivas Aplicadas à Saúde no Estado do Ceará
**Baseado no dataset MIMIC-IV**

##  Visão Geral
Este projeto tem como objetivo o desenvolvimento de um pipeline de ciência de dados para **detecção precoce de sepse**, utilizando dados clínicos reais do dataset **MIMIC-IV**. O foco não está apenas na modelagem, mas principalmente na **estruturação temporal dos dados**, engenharia de atributos e avaliação adequada do problema clínico.

A sepse é uma condição crítica em que **falsos negativos têm alto custo**, o que motivou decisões específicas de modelagem e escolha de métricas.
<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/dbe1e9fd-ec1a-42af-9594-bed6648f3edc" />

---

##  Objetivos
- Construir uma **base estruturada** a partir da MIMIC-IV.
- Aplicar **engenharia de atributos temporais** com janelas de tempo.
- Desenvolver modelos preditivos para **identificação precoce de sepse**.
- Avaliar os modelos com foco em **métricas clinicamente relevantes**, como recall.



##  Dataset
- **Fonte:** MIMIC-IV (Medical Information Mart for Intensive Care)
- **Tipo:** Dados clínicos reais de UTI
- **Características:**
  - Dados temporais e multivariados
  - Sinais vitais, eventos clínicos e informações demográficas
  - Alta dimensionalidade e presença de dados ausentes


##  Pipeline do Projeto

### 1. Extração e Integração dos Dados
- Seleção e junção de múltiplas tabelas da MIMIC-IV
- Padronização de identificadores e timestamps

### 2. Limpeza e Pré-processamento
- Tratamento de valores ausentes
- Remoção de inconsistências e outliers clínicos
- Normalização de variáveis contínuas

### 3. Engenharia de Atributos Temporais
- Criação de janelas de tempo deslizantes
- Agregações estatísticas (média, máximo, mínimo, tendência)
- Representação da evolução clínica do paciente

### 4. Modelagem Preditiva
- **Logistic Regression** como baseline interpretável
- **LSTM** para captura de dependências temporais
- Comparação entre modelos

### 5. Avaliação
- Métricas: Recall, Precision, Accuracy
- Ênfase em **recall**, visando reduzir falsos negativos

##  Resultados (Resumo)
- Modelos capazes de capturar padrões temporais relevantes para sepse.
- Melhor desempenho obtido quando variáveis temporais são consideradas.
- Evidência de que a estruturação correta dos dados impacta mais do que a escolha do algoritmo.

##  Principais Aprendizados
- Dados clínicos exigem **decisões orientadas ao domínio**, não apenas métricas genéricas.
- A engenharia de atributos temporais é crucial em problemas de saúde.
- Métricas devem refletir o **custo real do erro**, especialmente em contextos críticos.



##  Tecnologias Utilizadas
- Python
- Pandas, NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib, Seaborn



## 📌 Observação
Este projeto é de caráter acadêmico e experimental, utilizando dados anonimizados e respeitando as diretrizes de uso da MIMIC-IV.
