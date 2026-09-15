# Modelo de Dados Star Schema e D_Calendário no Power BI

Projeto de reestruturação de modelagem de dados e criação de inteligência temporal no Power BI Desktop, aplicando as melhores práticas de *Star Schema* (Esquema em Estrela) e desenvolvimento DAX.

## 📌 Objetivo
Transformar uma base plana única (`financials`) em um modelo relacional otimizado, separando tabelas de dimensões da tabela fato principal (`Fato_vendas`) e criando uma tabela de calendário contínua.

## 🛠️ Etapas do Projeto
1. **Tratamento e Modelagem no Power Query**:
   * Criação da chave composta `ID_categoria` (`Country` + `Segment`) para estabelecimento de relacionamento $1:*$.
   * Limpeza de redundâncias e estruturação da tabela `Fato_vendas`.
2. **Criação da Dimensão Calendário (DAX)**:
   * Construção da `D_Calendário` dinâmica com `ADDCOLUMNS` e `CALENDAR`.
   * Ajuste de ordenação de meses (`Mês Nome` por `Mês Num`) e marcação da tabela como Tabela de Data.

## 📊 Estrutura do Modelo
* **Fato**: `Fato_vendas`
* **Dimensões**: `D_produtos`, `D_categoria`, `D_desconto`, `D_Calendário`
