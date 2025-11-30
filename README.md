Projeto: Análise de Performance de Fornecedores com SQL e BigQuery
📘 Descrição do Projeto

Este projeto tem como objetivo analisar a performance de fornecedores utilizando Google BigQuery e SQL avançado.

Foi criado um ambiente de dados completo simulando operações reais de Supply Chain, contendo informações de:

Compras

Itens de ordem

Entregas

Faturas

Pagamentos

Avaliações de fornecedores

Produtos e categorias

Com esses dados, desenvolvi análises detalhadas de desempenho logístico, financeiro e operacional, consolidadas em uma visão final chamada:

🟦 vw_kpis_fornecedores
Uma visão única com todos os KPIs essenciais de fornecedores.

🗂 Estrutura do Projeto
/dataset
  ├── fornecedores.csv
  ├── faturas.csv
  ├── pagamentos.csv
  ├── entregas.csv
  ├── avaliacoes_fornecedor.csv
  ├── itens_ordem.csv
  ├── ordens_compra.csv
  ├── produtos.csv
  ├── categoria.csv

/sql
  ├── conciliacao_faturas_pagamentos.sql
  ├── lead_time.sql
  ├── produtos_mais_comprados.sql
  ├── top_fornecedores_valor.sql
  ├── view_final_kpis.sql

README.md

📊 Análises Desenvolvidas
1️⃣ Conciliação Financeira (Faturas x Pagamentos)

Objetivo: identificar diferenças entre o valor faturado e o valor pago, verificando inconsistências ou atrasos financeiros.

KPIs:

Total faturado

Total pago

Saldo pendente

Fornecedores com maiores divergências

Resultado:
✓ Identificação de fornecedores com alto saldo pendente, permitindo ações financeiras imediatas.

2️⃣ Lead Time Médio de Entrega

Cálculo do tempo médio entre envio e recebimento da mercadoria.

lead_time = DATE_DIFF(received_date, shipped_date, DAY)


KPIs:

Lead time médio por fornecedor

Ranking dos mais rápidos e mais lentos

Resultado:
✓ Fornecedores com lead time acima da média foram detectados, ajudando na gestão logística.

3️⃣ Produtos Mais Comprados

Análise da demanda por produto com base na soma das quantidades compradas.

KPIs:

Quantidade total por produto

Top 10 itens mais comprados

Resultado:
✓ Identificação dos itens críticos para reposição e negociação com fornecedores.

4️⃣ Top Fornecedores por Valor Total de Gasto

KPIs:

Total gasto por fornecedor

Ranking do maior para o menor

Resultado:
✓ Descoberta dos fornecedores mais estratégicos financeiramente.

🟦 5️⃣ VIEW Final – vw_kpis_fornecedores

A visão final consolida todos os KPIs em um único dataset:

📌 Indicadores Financeiros

total_faturas

total_pago

saldo_pendente

📌 Indicadores Logísticos

lead_time_medio

percentual_atraso

📌 Indicadores de Qualidade

media_qualidade

media_entrega

media_comunicacao

📌 Catálogo

quantidade de produtos fornecidos

📌 Identificação

supplier_id

supplier_name

Essa visão é ideal para:

✔ Dashboards no Looker / Power BI
✔ Monitoramento contínuo
✔ Decisões de compras
✔ Auditoria de fornecedores

🧠 Tecnologias Utilizadas

SQL avançado

Google BigQuery

Google Cloud Platform

Modelagem de dados

Views, CTEs, Window Functions, JOINs e agregações

🚀 Resultados Obtidos

✔ Fornecedores com maior volume de gastos
✔ Fornecedores com melhor/melhor performance logística
✔ Saldo financeiro pendente por fornecedor
✔ Produtos mais estratégicos por demanda
✔ Modelo consolidado de KPIs pronto para dashboards

Conclusão

Este projeto demonstra habilidades em:

Construção de pipelines analíticos no BigQuery

Manipulação e cruzamento de grandes volumes de dados

Criação de KPIs logísticos, financeiros e operacionais

Entrega de visão analítica completa para a área de Supply Chain
