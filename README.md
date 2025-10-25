# 🩺 CP5 - Predição de Diabetes com IA

Este projeto tem como objetivo desenvolver um **modelo de classificação supervisionado** para prever o risco de diabetes em indivíduos com base em indicadores de saúde pública. Utilizando técnicas de **Machine Learning**, o projeto busca auxiliar em diagnósticos preventivos, contribuindo para a identificação precoce da doença.

---

## 📋 Sumário

- [🎯 Objetivo](#-objetivo)
- [📊 Dataset](#-dataset)
- [🚀 Execução pelo Google Colab](#-execução-pelo-google-colab)
- [🛠️ Pré-processamento](#️-pré-processamento)
- [🤖 Modelos Utilizados](#-modelos-utilizados)
- [📈 Resultados](#-resultados)
- [📁 Estrutura do Projeto](#-estrutura-do-projeto)
- [📌 Conclusão](#-conclusão)

---

## 🎯 Objetivo

Desenvolver um modelo de **classificação binária** capaz de prever se um indivíduo tem ou não risco de diabetes, utilizando dados de saúde pública. A identificação precoce pode reduzir complicações e custos de tratamento, tornando a análise mais rápida e acessível.

---

## 📊 Dataset

- **Fonte:** [Diabetes Health Indicators Dataset - Kaggle](https://www.kaggle.com/datasets/mohankrishnathalla/diabetes-health-indicators-dataset)
- **Download:** [Baixar Dataset](https://www.kaggle.com/datasets/mohankrishnathalla/diabetes-health-indicators-dataset?resource=download)
- **Tamanho:** Mais de 250.000 registros
- **Variáveis:** 31 indicadores de saúde, incluindo:
  - `age`, `bmi`, `glucose_fasting`, `hba1c`, `diagnosed_diabetes` (target), entre outros.

### Exemplo de Variáveis:
| Variável | Tipo | Descrição |
|----------|------|-----------|
| diagnosed_diabetes | Binária | 0 = Não diabético, 1 = Diabético |
| bmi | Numérica | Índice de Massa Corporal |
| hba1c | Numérica | Hemoglobina glicada |
| glucose_fasting | Numérica | Glicemia em jejum |

---

## 🚀 Execução pelo Google Colab

### ⚡ Execução Rápida (10-15 minutos)

#### Passo 1: Acesse o Google Colab
- Vá para [Google Colab](https://colab.research.google.com/)
- Faça login com sua conta Google

#### Passo 2: Carregue o Notebook
- **Opção A (Upload):** 
  - Clique em **"File"** → **"Upload notebook"**
  - Faça upload do arquivo `CP_IA_Laura.ipynb`
- **Opção B (GitHub):**
  - **"File"** → **"Open notebook"** → **"GitHub"**
  - Cole a URL do repositório

#### Passo 3: Baixe o Dataset
- Acesse: [Kaggle Dataset Download](https://www.kaggle.com/datasets/mohankrishnathalla/diabetes-health-indicators-dataset?resource=download)
- Faça login no Kaggle
- Baixe o arquivo `diabetes_dataset.csv`

#### Passo 4: Execute as Células em Ordem
Execute cada célula sequencialmente clicando no botão **▶️**:

1. **✅ Células 1-3:** Importação de bibliotecas (já instaladas no Colab)
2. **📁 Célula 4:** Upload do dataset
   - Clique em **"Choose File"**
   - Selecione `diabetes_dataset.csv`
   - Aguarde o upload
3. **🔍 Células 5-8:** Análise exploratória dos dados
4. **🧹 Células 9-10:** Pré-processamento e preparação
5. **🤖 Células 11-13:** Treinamento dos modelos (2-5 minutos)
6. **📊 Células 14-15:** Resultados e visualizações

---

## 🛠️ Pré-processamento

- **Verificação de valores ausentes:** Nenhum valor ausente encontrado
- **Tratamento de outliers:** Aplicação do método IQR
- **Normalização:** Padronização com `StandardScaler`
- **Divisão dos dados:** 80% treino, 20% teste

---

## 🤖 Modelos Utilizados

Foram testados e comparados 4 algoritmos de classificação:

1. **📊 Regressão Logística** - Probabilidades de risco
2. **👥 K-Nearest Neighbors (KNN)** - Similaridade entre pacientes
3. **🌳 Árvore de Decisão** - Regras claras interpretáveis
4. **🌲 Random Forest** - Combinação de múltiplas árvores

---

## 📈 Resultados

### 🏆 Desempenho dos Modelos (Ordenados por F1-Score)

| Modelo | Acurácia | Precisão | Recall | F1-Score |
|--------|----------|----------|--------|----------|
| Random Forest | 0.9997 | 1.0000 | 0.9995 | 0.9998 |
| Árvore de Decisão | 0.9993 | 0.9993 | 0.9996 | 0.9994 |
| Regressão Logística | 0.9981 | 0.9997 | 0.9971 | 0.9984 |
| KNN | 0.9835 | 0.9914 | 0.9805 | 0.9859 |

### 🎯 Melhor Modelo: **Random Forest**

- **Matriz de Confusão:**
  - ✅ Verdadeiros Negativos: 7.424
  - ✅ Verdadeiros Positivos: 10.693
  - ❌ Falsos Positivos: 0
  - ❌ Falsos Negativos: 0

---

## 📁 Estrutura do Projeto

```
cp5-predicao-diabetes/
│
├── CP_IA_Laura.ipynb          # Notebook principal completo
├── diabetes_dataset.csv        # Dataset (baixar do Kaggle)
└── README.md                  # Este arquivo
```

### 📦 Dependências (Já Instaladas no Colab)
- pandas • numpy • matplotlib • seaborn • scikit-learn

---

## 📌 Conclusão

- ✅ **Random Forest** obteve melhor performance: **99.98% F1-Score**
- ✅ Todos os modelos superaram **98% de acurácia**
- ✅ Demonstração prática do potencial da IA em saúde
- ✅ Execução simplificada via Google Colab

### 🎯 Melhorias Futuras
- Otimização de hiperparâmetros com GridSearchCV
- Implementação de validação cruzada
- Análise de importância de features
- Teste com outros algoritmos (XGBoost, SVM)

---

## ⏱️ Tempo de Execução Estimado

| Etapa | Tempo |
|-------|-------|
| Upload e configuração | 2-3 minutos |
| Análise exploratória | 1-2 minutos |
| Treinamento dos modelos | 2-5 minutos |
| Total | **5-10 minutos** |

---

**Desenvolvido por:** Laura Lopes  
**Disciplina:** Inteligência Artificial  
**Plataforma:** Google Colab 📚✨

---
