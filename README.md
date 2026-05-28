miniguia de SQL para Análise de Dadosn com Cathy Tanimura

Caderno Temático criado com NotebookLM | Desafio DIO


Contexto e Objetivos:
Este projeto foi desenvolvido como parte do desafio prático da DIO, com o objetivo de explorar o uso da Inteligência Artificial como ferramenta de aprendizagem ativa.

O tema escolhido foi SQL para Análise de Dados, com base no livro SQL for Data Analysis de Cathy Tanimura — referência consolidada no mercado de dados.

Objetivos de Estudo:

Compreender os fundamentos e a importância do SQL na análise de dados
Dominar recursos avançados como Window Functions e CTEs
Identificar e evitar os erros mais comuns de analistas iniciantes
Construir uma base sólida para atuar como Analista de Dados


Curadoria de Fontes:
As fontes abaixo foram selecionadas e utilizadas no NotebookLM:

https://www.barnesandnoble.com/w/sql-for-data-analysis-cathy-tanimura/1139320782

https://learnsql.com/blog/sql-beach-reads-2025/

https://www.kellyjadams.com/post/sql-for-data-analysis-book-review

https://medium.com/an-idea/lessons-from-sql-for-data-analysis-e3d727565e38

https://medium.com/@chinyereofforah50/31-day-book-review-challenge-on-cathy-tanimuras-sql-for-data-analysis-advanced-techniques-for-28f55d27e6ba

Prompt 1
Pergunta:

"Como Cathy Tanimura, explique o que é SQL e por que é essencial para análise de dados?"

Resposta obtida:
A IA respondeu com contexto histórico da carreira da autora, explicou o caráter declarativo do SQL, e destacou três pilares: poder computacional, padrão da indústria e estrutura de pensamento crítico. Trouxe também dicas práticas como perfilamento de dados, uso de CTEs e foco no impacto para o negócio.

Cicatriz:
A resposta foi muito boa na primeira tentativa. A persona da Cathy funcionou bem pois as fontes continham relatos da própria autora.

Prompt 2
Pergunta:

"Explique Window Functions com exemplos práticos para um analista iniciante."

Resposta obtida:
A IA explicou a cláusula OVER, PARTITION BY e ORDER BY. Apresentou três exemplos práticos: percent of total, comparação mês a mês com lag() e cálculo acumulado YTD com sum().
Cicatriz:
Precisei pedir para simplificar a linguagem técnica. A primeira versão estava muito densa para um iniciante. Ajustei o prompt adicionando "para um analista iniciante" e o resultado melhorou.

Prompt 3
Pergunta:

"Quais são os principais usos de GROUP BY e quando devo evitá-lo?"

Resposta obtida:
A IA apresentou três usos principais: perfilamento de dados, deduplicação e pivotamento. Indicou quando evitar: ao precisar preservar linhas originais (usar Window Functions) e ao calcular subtotais em vários níveis (usar ROLLUP, CUBE ou GROUPING SETS).
Cicatriz:
Resposta completa e objetiva sem necessidade de ajuste.

Prompt 4
Pergunta:

"Quais erros mais comuns analistas iniciantes cometem ao escrever SQL?"

Resposta obtida:
A IA listou 7 erros: rodar queries em produção, JOINs incorretos, código espaguete, ignorar divisão por zero, erro com BETWEEN, ordem errada no CASE e uso excessivo de UNION.
Cicatriz:
A resposta foi longa demais. Refinei o prompt pedindo "liste de forma objetiva" e a IA retornou em formato mais limpo.

Prompt 5
 Pergunta:

"Gere um glossário com os 10 conceitos mais importantes de SQL para análise de dados."

Resposta obtida:
Glossário completo com Window Functions, CTEs, GROUP BY e extensões, JOINs, CASE, COALESCE/NULLIF, Date Math, Regex, Subqueries e UNION/UNION ALL.
 Cicatriz:
Primeira resposta não tinha ordem de dificuldade. Pedi para reorganizar do mais básico ao mais avançado.

 Miniguia de Estudo:
 Resumos Estruturados:
O que é SQL?
SQL (Structured Query Language) é uma linguagem declarativa para comunicação com bancos de dados relacionais. Em vez de programar o passo a passo, você apenas especifica o resultado desejado e o banco de dados encontra o caminho mais eficiente.
Por que SQL é essencial para análise de dados?

A maioria dos dados do mundo está em bancos de dados relacionais
É o padrão da indústria — conecta-se com Python, R, Power BI e qualquer ferramenta de BI
Permite processar bilhões de registros aproveitando processamento distribuído
Exige pensamento crítico estruturado: limpar dados, séries temporais, coortes e testes A/B

Window Functions
Realizam cálculos em múltiplas linhas sem reduzir o número de linhas do resultado. Usam a cláusula OVER (PARTITION BY ... ORDER BY ...). Principais funções: lag, lead, rank, sum, avg.
CTEs (Common Table Expressions)
Tabelas temporárias definidas no início da query com WITH nome AS (...). Substituem subconsultas aninhadas, tornando o código mais legível e fácil de manter.
GROUP BY
Agrupa linhas para aplicar funções de agregação. Extensões como ROLLUP, CUBE e GROUPING SETS calculam múltiplos níveis de subtotal em uma única varredura.

Glossário:
SQL: Linguagem declarativa para consultar bancos de dados relacionais
  
SELECT: Comando para selecionar colunas de uma tabela

WHERE: Filtro de linhas aplicado antes da agregação

GROUP BY: Agrupa linhas para aplicar funções de agregação

HAVING: Filtro aplicado após a agregação

JOIN: Combina colunas de duas ou mais tabelas

CROSS JOIN: produto cartesiano entre duas tabelas

Window Function: Cálculo sobre múltiplas linhas sem colapsar o resultado

CTE: Tabela temporária nomeada definida com WITH

CASE: Lógica condicional If-Then-Else dentro do SQL

COALESCE: Substitui valores nulos por um valor padrão

NULLIF: Converte um valor específico em nulolag / leadBuscam valores de linhas anteriores ou posteriores

UNION / UNION ALL: Empilha resultados de múltiplas queries verticalmente

ROLLUP / CUBE: Extensões do GROUP BY para subtotais multidimensionais

date_trunc: Trunca timestamps para granularidade desejada (mês, ano)

SubqueryQuery: aninhada dentro de outra query

ETLExtract, Transform, Load : processo de tratamento de dados

Prompts Reutilizáveis para Revisão:
Use estes prompts para revisar o conteúdo em sessões futuras no NotebookLM ou em qualquer IA:
1. "Como Cathy Tanimura, explique [conceito] para um analista de dados iniciante."

2. "Crie um exemplo prático de [Window Function / CTE / GROUP BY] aplicado a um cenário de negócios."

3. "Quais são as diferenças entre [UNION x UNION ALL / GROUP BY x Window Function / DISTINCT x GROUP BY]?"

4. "Gere 5 perguntas de revisão sobre [tema] no nível iniciante a intermediário."

5. "Quais erros devo evitar ao usar [JOIN / CASE / BETWEEN] em SQL?"

6. "Explique quando devo usar CTE no lugar de subconsulta e por quê."

7. "Crie uma query SQL de exemplo usando Window Function para calcular crescimento mês a mês."

Sobre a Persona Utilizada:
Cathy Tanimura é analista de dados sênior, autora de SQL for Data Analysis (O'Reilly), e atuou em empresas como StubHub, Zynga, Strava e Summit Partners. É referência no uso de SQL aplicado a decisões de negócio.

Projeto desenvolvido para o Desafio de Projeto — DIO

Tema: SQL para Análise de Dados com NotebookLM
