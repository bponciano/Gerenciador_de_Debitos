# 📊 Gerenciador de Débitos com Persistência em JSON

> Sistema de controle financeiro com modelagem estruturada de dados e persistência local.  
> Demonstra organização de estado, regras de negócio e manipulação de dados estruturados.

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Tkinter](https://img.shields.io/badge/Tkinter-Tkcalendar-brightgreen?style=for-the-badge)

## 🎯 Objetivo do Projeto

Desenvolver um sistema simples de gestão de débitos para clientes, permitindo registrar compras, pagamentos, consultar extratos e calcular saldos consolidados.

O projeto foi construído para demonstrar:

- Modelagem de dados estruturados  
- Aplicação de regras de negócio financeiras  
- Persistência de dados em formato JSON  
- Organização lógica de informações com integridade de chave  

Simula o comportamento de um sistema financeiro simplificado, base para evolução futura para banco relacional.

## 🏗 Arquitetura da Solução
```
Interface Gráfica (Tkinter)
↓
Camada de Regras de Negócio (Funções Python)
↓
Estrutura de Dados (Dicionário + Lista de Transações)
↓
Persistência Local (dados.json)
```

## ⚙️ Stack Tecnológica

- Python 3  
- Tkinter (GUI)  
- tkcalendar (DateEntry)  
- JSON (persistência documental)  

## 🔄 Pipeline de Dados

### 1️⃣ Registro de Cliente
- Normalização de chave com `.lower()`  
- Estruturação inicial:
  - Nome de exibição  
  - Saldo devedor  
  - Lista de transações  

---

### 2️⃣ Registro de Transações
- Tipos:
  - Compra (incrementa saldo)  
  - Pagamento (decrementa saldo)  
- Armazenamento estruturado:
  - Tipo  
  - Data  
  - Valor  
- Atualização automática do saldo  

---

### 3️⃣ Persistência
- Serialização com `json.dump`  
- Armazenamento em `dados.json`  
- Salvamento automático a cada modificação  

---

### 4️⃣ Consulta e Extração
- Geração de extrato formatado  
- Exportação para `.txt`  
- Cálculo de saldo total consolidado  
- Listagem dinâmica em tabela GUI  

## 🧠 Conceitos Aplicados

- Modelagem de dados com dicionários aninhados  
- Manipulação de listas estruturadas  
- Serialização e desserialização JSON  
- Controle de estado em memória  
- Regras de negócio financeiras  
- Validação de entrada de dados  
- Organização modular de funções  
- Estrutura semelhante a banco documental  

## 📊 Aplicações Analíticas

- Controle financeiro de pequenos negócios  
- Base para migração para SQLite ou PostgreSQL  
- Exportação para CSV para análise com Pandas  
- Integração futura com dashboards (Power BI / Streamlit)  
- Simulação de estrutura NoSQL documental  

## 🚀 Evoluções Futuras

- Migração para banco relacional (SQLite)  
- Separação em camadas (MVC)  
- Implementação de logs de auditoria  
- API REST para consumo externo  
- Controle de autenticação  
- Containerização da aplicação  
- Versão web com Flask ou FastAPI  

## 👨‍💻 Autor

**Breno Ponciano**  
Foco em Análise e Engenharia de Dados  