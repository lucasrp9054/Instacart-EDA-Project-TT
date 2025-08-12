# Projeto 3: Análise Exploratória de Dados (AED) - Hábitos de Compra na Instacart

## Visão Geral

Este projeto apresenta uma Análise Exploratória de Dados (AED) sobre o conjunto de dados da Instacart, plataforma de entrega de supermercado. O objetivo foi realizar todo o ciclo de análise: desde a limpeza e pré-processamento dos dados até a geração de insights e visualizações sobre os hábitos de compra dos clientes.

## Objetivo

Limpar, preparar e analisar os dados da Instacart para responder perguntas de negócio sobre padrões de consumo dos clientes, como horários e dias de maior movimento, produtos mais populares e comportamento de recompra.

## Dados

O estudo utilizou cinco conjuntos de dados inter-relacionados:

- **instacart_orders.csv**: Informações sobre cada pedido (ID do pedido, ID do cliente, dia, hora).
- **order_products.csv**: Detalhes dos itens em cada pedido.
- **products.csv**: Informações sobre cada produto (nome, departamento, corredor).
- **aisles.csv**: Nomes dos corredores.
- **departments.csv**: Nomes dos departamentos.

## Metodologia e Etapas

### Pré-processamento de Dados

- **Tratamento de Duplicatas**: Identificação e remoção de registros duplicados, incluindo padrão de erro técnico que gerava duplicatas sistemáticas.
- **Valores Ausentes**: Estratégias de imputação específicas (ex: preenchimento com 0 para novos pedidos, mediana para dados de carrinho e 'Unknown' para nomes de produtos).
- **Correção de Tipos de Dados**: Otimização de memória e correção semântica, convertendo colunas para tipos apropriados (int, bool, category).
- **Junção de Tabelas**: Uso de `pd.merge()` para combinar as cinco tabelas em um DataFrame unificado.

### Análise Exploratória de Dados (AED)

A análise foi dividida em três níveis de complexidade:

- **Análise Temporal**: Padrões de compra por hora do dia, dia da semana e tempo de espera entre pedidos.
- **Análise de Produtos**: Produtos mais populares, mais recomprados e os primeiros adicionados ao carrinho.
- **Análise de Clientes**: Distribuição do número de pedidos por cliente e quantidade de itens por pedido.

## Habilidades e Ferramentas Aplicadas

- **Pandas**: Manipulação avançada de DataFrames (`merge`, `groupby`, `agg`, `value_counts`, tratamento de dados).
- **Matplotlib**: Visualizações como gráficos de barras e histogramas.
- **Análise Estatística**: Uso de `.describe()` para métricas descritivas.
- **Comunicação de Resultados**: Elaboração de conclusões claras para cada etapa da análise.

## Principais Conclusões

- Os clientes da Instacart seguem uma rotina de compras bem definida, com picos nos fins de semana e segundas-feiras, e ciclos de recompra de 7 e 30 dias.
- O carrinho é dominado por frutas e vegetais frescos, com forte preferência por produtos orgânicos. A banana é o produto mais popular.
- Foram identificadas anomalias, como taxas de recompra de 100%, destacando a importância de considerar o volume de dados ao interpretar proporções.
