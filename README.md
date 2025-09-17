# 📊 Projeto de Análise de Dados

Este projeto tem como objetivo analisar uma base de clientes, identificar problemas nos dados e investigar as causas de cancelamento do serviço.  
A análise foi feita em **Python** utilizando **Jupyter Notebook**.

---

## 🛠️ Instalação das dependências

Para rodar o projeto, instale as bibliotecas necessárias:
pip install pandas openpyxl numpy nbformat plotly ipykernel

---


## 🚀 Passo a Passo da Análise

### 🔹 Passo 1: Importar a base de dados
- Importação da biblioteca Pandas para ler o arquivo csv 'cancelamentos'

---

### 🔹 Passo 2: Visualizar a base de dados
- Objetivos:
  - Entender as informações contidas
  - Encontrar possíveis problemas nos dados  

---

### 🔹 Passo 3: Resolver problemas da base
- Problemas encontrados:
  - Informações inúteis -> uso do 'drop' para eliminar a coluna de 'CustomerID' que é irrelevante para a análise
  - Informações vazias -> uso do 'info()' para apurar possíveis informações faltantes
  - Informações no formato errado  
- Como os dados vazios eram poucos, foram **descartados** usando 'dropna()' sem que houvesse prejuízo para a análise.

---

### 🔹 Passo 4: Análise Exploratória Inicial
- Percentual de clientes que cancelaram: 56,7%
- Percentual de clientes que não cancelaram: 43,3%

---

### 🔹 Passo 5: Identificação das causas de cancelamento
- Análise do impacto de cada coluna no cancelamento
- Criação e exibição de gráficos interativos com a biblioteca Plotly

---

### 🔹 Passo 6: Testes de cenários
Simulações aplicadas:
1. Call Center
    - Condição: ligações callcenter <= 4
    - Resultado: 64% não cancelaram | 36% cancelaram

2. Atraso no pagamento
    - Condição: dias de atraso <= 20
    - Resultado: 73% não cancelaram | 27% cancelaram

3. Tipo de contrato
    - Condição: contrato != mensal
    - Resultado: 82% não cancelaram | 18% cancelaram

---

### ✅ Conclusão

O projeto mostrou que:
  - Call center, atrasos no pagamento e contrato mensal são fatores determinantes para o cancelamento.
  - A exclusão desses problemas melhora significativamente a retenção de clientes.
