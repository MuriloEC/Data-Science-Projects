# 📊 Análise de Desempenho e Tratamento de Dados - E-commerce

Este repositório contém um script em Python focado na **Engenharia, Tratamento de Dados e Análise Exploratória (EDA)** de um histórico de vendas de e-commerce. O grande diferencial deste projeto é o foco na **interpretação de negócio**, conectando métricas técnicas e manipulação de dados a decisões estratégicas corporativas (como logística, marketing e gestão de estoque).

## 🚀 Objetivo do Projeto

Transformar dados brutos de vendas em inteligência comercial, permitindo que gestores respondam a perguntas críticas como:
* Quais são as categorias de produtos que sustentam o faturamento da empresa?
* Quais produtos específicos possuem maior giro de estoque?
* Como as vendas se comportam ao longo dos meses (sazonalidade comercial)?

---

## 🛠️ Arquitetura do Script e Visão de Negócio

O código está estruturado em três fases fundamentais:

### 1. Diagnóstico e Saúde do Negócio 
* **Ação:** Verificação de valores nulos (`.isnull()`) e registros duplicados (`.duplicated()`).
* **Impacto de Negócio:** Garante a confiabilidade do relatório financeiro. Dados duplicados inflam artificialmente o faturamento reportado, enquanto dados nulos apontam falhas de integração nos sistemas de checkout (ex: vendas sem rastreio de canal ou preço).

### 2. Engenharia e Higienização de Dados 
* **Sazonalidade:** Extração de `ano`, `mes` e `dia` a partir da data de venda para identificar os melhores momentos para campanhas de marketing (ex: picos de vendas no início do mês).
* **Organização de Portfólio:** Separação da string combinada `produto,categoria` em duas variáveis distintas. Isso permite uma análise macro (por departamento) e uma análise micro (por SKU).
* **Otimização:** Conversão correta dos tipos de dados para evitar cálculos matemáticos inválidos sobre identificadores textuais (como IDs e canais de venda).