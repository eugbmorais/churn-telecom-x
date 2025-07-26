# 📊 Projeto de Análise de Churn - TelecomX

Este repositório apresenta uma análise completa sobre o **Churn de clientes de uma empresa de telecomunicações**. O objetivo é entender os principais fatores que levam clientes a cancelarem seus serviços, por meio de **limpeza de dados**, **exploração estatística** e **visualizações gráficas**.

---

## 🎯 Objetivo

- Investigar o perfil dos clientes que abandonam o serviço (`churn = Yes`);
- Explorar o comportamento de variáveis numéricas e categóricas;
- Identificar padrões e tendências;
- Fornecer **recomendações práticas** para redução do churn.

---

## 📁 Estrutura do Projeto

- `notebook.ipynb`: Código em Python com extração de dados, tratamento, visualizações e análise final.
- Fonte dos dados: [TelecomX_Data.json](https://raw.githubusercontent.com/ingridcristh/challenge2-data-science/refs/heads/main/TelecomX_Data.json)

---

## 🛠️ Tecnologias Utilizadas

- Python 3.x  
- Pandas & NumPy  
- Matplotlib & Seaborn  
- Scikit-learn (MinMaxScaler)  
- Google Colab / Jupyter

---

## 📊 Etapas do Projeto

### 🔹 1. Extração dos Dados

Os dados foram carregados diretamente de uma API em formato JSON, contendo colunas aninhadas com informações do cliente, telefone, internet e conta.

### 🔹 2. Limpeza e Tratamento

- **Colunas aninhadas** foram normalizadas para facilitar a análise;
- **Renomeação e padronização** de nomes de colunas;
- Conversão de tipos e tratamento de valores nulos;
- Exclusão de inconsistências (ex: `charges.total` menor que `charges.monthly`);
- Criação de novas variáveis como `contas_diarias` e `contas_diarias_norm`.

### 🔹 3. Estatísticas e Distribuições

- Análise descritiva das variáveis numéricas e categóricas;
- Estatísticas como média, mediana, desvio padrão das faturas;
- Distribuição de `churn`, com **26,5% dos clientes cancelando** os serviços.

### 🔹 4. Visualizações

- 📉 Gráficos de barras para variáveis categóricas como `contract`, `paymentmethod`, `seniorcitizen`, etc.
- 📈 Histogramas e KDEs para variáveis contínuas como `charges.total` e `tenure`.
- 🔥 Mapa de calor de correlação entre variáveis numéricas.

---

## 📈 Principais Insights

- **Clientes com contratos mensais** têm maior chance de churn.
- **Idosos** (seniorcitizen) apresentaram maior fidelidade do que o esperado.
- Clientes com **curto tempo de permanência (tenure < 10 meses)** tendem a cancelar.
- Pagamento com **boleto eletrônico** está associado a maior churn.
- Serviços como **backup, suporte técnico e segurança** tendem a manter o cliente ativo.

---

## ✅ Recomendações

- Incentivar contratos anuais e de dois anos com descontos ou bônus;
- Investir em **onboarding eficaz** nos primeiros meses do cliente;
- Oferecer serviços complementares (ex: suporte técnico, segurança online);
- Estratégias de retenção específicas para usuários de boleto eletrônico.

---

## 🧠 Conclusão

Através da análise detalhada e visual dos dados, é possível identificar **padrões claros de evasão** e fornecer **insumos estratégicos** para melhorar a retenção. A empresa pode utilizar esse estudo como **base para modelos preditivos futuros** ou como suporte à tomada de decisão no marketing e atendimento.

---

## 📌 Dicionário de Dados (amostra)

| Coluna              | Descrição                                      |
|---------------------|-----------------------------------------------|
| `customer_id`       | ID único do cliente                           |
| `gender`            | Gênero do cliente                             |
| `seniorcitizen`     | Se o cliente é idoso (True/False)             |
| `partner`           | Se possui parceiro(a)                         |
| `dependents`        | Se possui dependentes                         |
| `tenure`            | Meses como cliente                            |
| `contract`          | Tipo de contrato (Mensal, Anual, etc.)        |
| `charges.monthly`   | Valor da fatura mensal                        |
| `charges.total`     | Valor total já pago pelo cliente              |
| `churn`             | Se cancelou os serviços (Yes/No)              |

---

## 📂 Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/seuusuario/projeto-churn-telecom.git
