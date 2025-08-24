# Análise de Estabelecimentos com Vínculo Ativo - RJ e SP (2019-2023)

Este repositório contém um script em Python para consultar e extrair dados da **RAIS (Relação Anual de Informações Sociais)**, usando **BigQuery** e **pandas**, focando nos estabelecimentos com trabalhadores com vínculo ativo nas cidades do **Rio de Janeiro** e **São Paulo**, no período de **2019 a 2023**.

## Dataset

- **Origem:** [Base dos Dados](https://basedosdados.org/dataset/br-rais)  
- **Projeto BigQuery:** `basedosdados`  
- **Conjunto de dados:** `br_me_rais`  
- **Tabela:** `microdados_estabelecimentos`  

O dataset contém informações detalhadas sobre estabelecimentos e vínculos de trabalhadores, incluindo:

- Ano de referência (`ano`)
- Identificação do município (`id_municipio`)
- UF (`sigla_uf`)
- Natureza do estabelecimento (`natureza_estabelecimento`, `natureza_juridica`)
- Quantidade de vínculos ativos (`quantidade_vinculos_ativos`)
- Classificação CNAE (`cnae_1`, `cnae_2`, `cnae_2_subclasse`)

## Objetivo

Extrair uma tabela com os **estabelecimentos ativos em RJ e SP** entre **2019 e 2023**, incluindo apenas aqueles com **trabalhadores com vínculo ativo**.

## Como usar

### 1. Pré-requisitos

- Python 3.9+  
- Bibliotecas: `pandas`, `pandas-gbq`, `google-cloud-bigquery`  
```bash
pip install pandas pandas-gbq google-cloud-bigquery
