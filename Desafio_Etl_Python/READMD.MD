# 📘 ETL – Pipeline de Dados Minerais 

## 🎯 Objetivo Central do Pipeline

O objetivo é **converter dados brutos de volume e valor em indicadores de performance percentual (contribuição do 100% total)**. Isso permite uma análise comparativa clara da importância volumétrica e de receita de cada mineral por **UF** e **Ano base**.



## ℹ️ Fonte de Dados e Escopo

Os dados são provenientes do **Relatório Anual de Lavra (RAL)** da Agência Nacional de Mineração (ANM).
- [Acesse o relatório completo](https://dados.gov.br/dados/conjuntos-dados/anuario-mineral-brasileiro-amb)


- Conteúdo: Produção Bruta (ROM), Produção Beneficiada, Água Mineral e Destinações (vendas, transferências, consumo). 
- Abrangência: A série de dados contempla o ano-base 2010 em diante.  
- Nota de Qualidade: A ANM informa que a fonte são dados declaratórios (das mineradoras), sujeitos a ajustes e depurações pelo corpo técnico. Inconsistências originais são tratadas no pipeline.



## 🏗️ As Camadas e o Processo de Transformação

### 🥉 Camada Bronze (Bruta)

- Conteúdo: Cópia fiel e bruta dos CSVs originais.
- Processamento: Apenas a leitur e a conversão inicial de strings (substituição de vírgula por ponto) para preparar a tipagem.

### 🥈 Camada Prata (Limpa)

- Conteúdo: Dados limpos e prontos para a agregação.
- Processamento:
  1. Tipagem: Conversão de métricas (`Valor Venda (R$)`, etc.) para o tipo `float`. 
  2. Qualidade: Remoção de duplicatas e garantia de que `'Ano base'` é um inteiro.  


### 🥇 Camada Ouro (Métricas Analíticas)

- Esta camada é onde o valor analítico é criado, através da combinação das **Partes** (Substâncias) com os **Totais** (Geral).


## 🟡 Resultado Final

O dataset consolidado permite:

- comparação imediata da participação de cada substância no volume total produzido;
- análise da participação na receita total de vendas;
- uso direto em dashboards e modelos analíticos.

O produto final é um conjunto de métricas padronizadas, confiáveis e prontas para consumo.

