# Global Retail Connect

### Dashboard Link : 

## Descrição do Problema

A **Global Retail Connect** é uma varejista em expansão que lida com um volume crescente de transações e dados de clientes. Apesar do faturamento bruto estar na casa dos $2.8 milhões, a diretoria sente que não tem clareza sobre quem é o seu cliente ideal e por que as margens de lucro oscilam tanto entre os meses.  

O Problema:  
Atualmente, as decisões de marketing e estoque são tomadas com base em intuição, e não em dados. Isso gerou três incertezas críticas:

Ineficiência de Margem:  
O custo dos produtos vendidos (CPV) consome 53,16% da receita, mas não se sabe se isso é um padrão saudável ou um gargalo operacional.

Desconhecimento do Perfil:  
A empresa não sabe se deve focar em campanhas para jovens ou para o público maduro, nem se o estado civil impacta o ticket médio.

Risco de Concentração:  
Existe a suspeita de que a receita dependa de pouquíssimos clientes e de apenas um ou dois produtos (como o iPhone 6), o que torna o negócio vulnerável.

O Objetivo:  
Desenvolver um ecossistema de dashboards que transforme esses dados brutos em decisões estratégicas, permitindo identificar grupos de clientes subexplorados e otimizar a relação Custo vs. Receita


### Etapas Seguidas 

ETL e Tratamento de Dados (Power Query):

Conexão e Limpeza:  
Os dados foram carregados de arquivos distintos CSV e submetidos a uma análise de qualidade de colunas (Column Quality/Profile) para identificar nulos e inconsistências.

Tabela dClientes (Enriquecimento):  
Criação da coluna de **Idade** dinâmica, por meio da coluna de **Nascimento** para permitir análises demográficas e segmentação comportamental.

Agrupamento por **Faixa Etária** para facilitar a leitura visual do comportamento de consumo.

Implementação de uma **Coluna de Ordem** customizada para garantir que os gráficos de idade seguissem uma sequência lógica e não alfabética.

Modelagem de Dados:  
Estruturação do modelo em Star Schema (Esquema Estrela), garantindo performance e integridade referencial entre as tabelas de dimensões e fatos.

Desenvolvimento de Cálculos (DAX):  
Criação de medidas fundamentais como Faturamento Total, CPV e Ticket Médio.

Desenvolvimento de indicadores de eficiência, como a Margem de Lucro (%) e a Representatividade do Custo.

# Business Insights

Snapshot do Dashboard (Visualização e Design)

Aba Overview: Focada em indicadores macro de faturamento e saúde financeira.

![OverView](https://github.com/ZeyOliveira/retail-performance-analytics/blob/main/imagens/overview_.png)

Aba Operacional (Custos): Detalhamento da eficiência logística e concentração de capital em produtos.

![Custos](https://github.com/ZeyOliveira/retail-performance-analytics/blob/main/imagens/custos_.png)

Aba Customer Insights: Análise demográfica e comportamental para segmentação de público.

![Customers](https://github.com/ZeyOliveira/retail-performance-analytics/blob/main/imagens/custumers_insi.png)


---

**Insights de Negócio e Storytelling**  
- Eficiência Operacional e Margem

**Pergunta:** Por que o lucro não cresce proporcionalmente à receita?

Através da análise de Representatividade do Custo (53,16%), identificamos que o custo variável acompanha o faturamento de forma agressiva. Em meses de pico, como Outubro ($395k de receita), o custo subiu para $242,7k, comprimindo a margem de contribuição.

---

**Análise de Risco e Concentração**

**Pergunta:** O faturamento da empresa está vulnerável?

Sim. O Ranking de Concentração de Capital revela que o iPhone 6 e a Câmera Canon a1 somam quase $800k de investimento. Uma quebra de estoque ou queda na demanda desses itens impactaria severamente o fluxo de caixa.

---

**Perfil do Consumidor e Segmentação**

**Pergunta:** Qual o perfil do cliente que gera maior valor?

Identificamos que clientes casados representam 57,91% do faturamento. Além disso, o grupo de 36-50 anos é o motor da empresa ($1.2M), enquanto o grupo 51+ apresenta uma oportunidade de expansão, pois possui alto potencial e menor faturamento atual ($766k).

# Conclusão

A análise revelou que a empresa possui forte dependência de poucos produtos e concentração relevante em determinados perfis de clientes, aumentando o risco operacional e comercial da operação.

Além disso, a relação entre crescimento de receita e expansão do CPV demonstra a necessidade de monitoramento contínuo das margens operacionais para evitar deterioração da lucratividade.

Com a implementação deste ecossistema analítico, a Global Retail Connect passa a ter capacidade de:

- Monitorar performance financeira em tempo real
- Identificar concentração de risco
- Segmentar clientes com maior precisão
- Apoiar decisões de marketing e estoque orientadas por dados
