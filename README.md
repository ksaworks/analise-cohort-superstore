📊 Análise de Cohort - SuperStore

📌 Contexto

A SuperStore, uma das maiores redes de supermercados do país, enfrenta desafios relacionados à retenção de clientes e à melhoria das suas estratégias de vendas. A empresa possui dados ricos sobre seus clientes, pedidos, localizações e produtos, mas precisa de uma análise detalhada para tomar decisões baseadas em dados.

O time de gestão identificou três áreas principais para foco:

Retenção de Clientes: Monitorar a interação de clientes ao longo do tempo (Análise de Cohort).

🎯 Objetivo

Como Analista de Dados, minha missão foi resolver os problemas de negócio utilizando o Excel como ferramenta principal. O projeto responde às seguintes perguntas:

✅ Qual é a retenção de clientes ao longo dos meses?
✅ Quais cohorts apresentam maior retenção?
✅ Existem fatores sazonais que impactam a retenção?

🛠 Resolução do Problema

📂 Parte 1: Análise de Cohort

🔹 1. Preparação dos Dados

Importei o arquivo orders.csv para o Excel.

Verifiquei que as colunas principais estavam corretamente formatadas:

Order ID

Order Date

Customer ID

Sales

🔹 2. Identificação do Mês de Aquisição

Adicionei uma coluna "Mês de Aquisição" com a fórmula:

=TEXTO([Order Date]; "AAAA-MM")

Criei uma Tabela Dinâmica para determinar o primeiro mês de compra de cada cliente:

Linhas: Customer ID

Valores: Mínimo de Order Date

🔹 3. Construção da Tabela de Cohort

Criei uma tabela com:

Linhas: Mês de Aquisição

Colunas: Meses decorridos (0, 1, 2...)

Preenchi a tabela contando o número de clientes que realizaram compras em cada mês subsequente ao mês de aquisição.

🔹 4. Criação do Heatmap de Retenção

Dividi cada valor pelo total de clientes no Mês de Aquisição para calcular a taxa de retenção.

Apliquei formatação condicional para destacar os padrões de retenção.

📈 Conclusão da Análise

🔹 Qual é a retenção de clientes ao longo dos meses?

Melhor Cohort em 6 meses: O grupo de clientes adquiridos em maio de 2014 (2014-05) apresentou a melhor retenção após seis meses, com 11% de clientes ainda ativos.

Melhor Cohort em 12 meses: O cohort de junho de 2014 (2014-06) manteve uma retenção média de 9% após um ano.

🔹 Quais cohorts apresentam maior retenção?

Melhor Cohort em 1 mês: O cohort de novembro de 2014 (2014-11) teve a maior retenção no primeiro mês, atingindo 25%.

🔹 Existem fatores sazonais que impactam a retenção?

Black Friday, impulsionando o volume de compras.
Cupom de 25% de desconto na primeira compra, incentivando novos clientes.

🖩 Fórmulas Utilizadas

Identificação do Mês de Aquisição:

=TEXTO([Order Date]; "AAAA-MM")

Mínimo de Order Date por Cliente:

=MínimoSes([Order Date]; [Customer ID])

Extração de Ano e Mês:

=ESQUERDO([Order Date]; 7)

Extração do Mês:

=DIREITO([Order Date]; 2)

Lista de Clientes Únicos:

=ÚNICO([Customer ID])

Unificação de Tabelas:

=PROCV([Customer ID]; [Tabela_Clientes]; 2; FALSO)

🚀 Tecnologias Utilizadas

📊 Microsoft Excel (Tabelas Dinâmicas, PROCV, Formatação Condicional)

🔥 Heatmap para visualização de retenção

📚 Aprendizados

✅ Construção de uma análise de Cohort utilizando Excel
✅ Extração e tratamento de dados de clientes
✅ Aplicação de fórmulas avançadas para análise de dados
✅ Visualização de retenção com heatmap

📌 Sobre o Projeto

Este projeto faz parte do curso Comunidade DS, onde desenvolvemos um portfólio para prática de análise de dados no Excel.

📢 Se este repositório foi útil, não esqueça de dar um ⭐ no GitHub! 🚀
