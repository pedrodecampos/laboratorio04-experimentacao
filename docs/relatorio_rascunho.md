# Relatório Parcial — Repositórios Populares do GitHub

## 1. Introdução

A plataforma GitHub consolidou-se como o principal ambiente para colaboração em projetos de software livre, reunindo milhões de repositórios e contribuidores. Repositórios populares funcionam como núcleos de inovação tecnológica, influenciando práticas de desenvolvimento, padrões de qualidade e ecossistemas de ferramentas. Compreender quais fatores se relacionam com o engajamento em projetos de grande visibilidade pode apoiar estudantes e profissionais na escolha de comunidades de prática, além de orientar mantenedores quanto a estratégias de crescimento.

Este trabalho constrói um dashboard exploratório com base em um conjunto de repositórios amplamente reconhecidos, permitindo investigar como linguagens, idade dos projetos e outros atributos se articulam com métricas de popularidade (estrelas, forks) e colaboração (issues abertas, wiki habilitada). O relatório acompanha esse dashboard, descrevendo a base utilizada, os procedimentos analíticos adotados e os principais resultados observados.

## 2. Metodologia e Descrição da Base

### 2.1 Origem dos Dados

A base `dataset.csv` disponibiliza metadados de 100 repositórios relevantes coletados a partir da API pública do GitHub. Para este rascunho, consideramos que os projetos foram selecionados manualmente entre listas públicas de “repositórios populares” até junho de 2024, priorizando diversidade em linguagens e domínios de aplicação.

### 2.2 Campos Disponíveis

Cada registro contém:

- `repository_id`: identificador numérico sequencial.
- `name`: nome do repositório no GitHub.
- `language`: linguagem principal identificada pela plataforma.
- `stars`: número de estrelas.
- `forks`: número de forks.
- `created_at`: data de criação do repositório.
- `size_kb`: tamanho aproximado do repositório em kilobytes.
- `has_wiki`: indicador booleano da presença de wiki.
- `has_issues`: indicador booleano de issues habilitadas.

### 2.3 Processamento e Métricas Derivadas

Para alimentar o dashboard, planejamos derivar as seguintes métricas:

- Idade do repositório (anos) a partir de `created_at`.
- Médias, medianas e distribuição de `stars` e `forks` agrupadas por `language`.
- Percentual de repositórios com wiki e issues habilitadas por linguagem.
- Taxa de crescimento aproximada (`forks`/idade) como proxy de adoção.

O pré-processamento será realizado em Python (pandas), com limpeza de formatos de data e normalização booleana. As visualizações serão construídas com bibliotecas como Plotly ou Altair para facilitar a incorporação no dashboard.

## 3. Resultados (Previstos no Dashboard)

### 3.1 Linguagem e Engajamento

O dashboard incluirá gráficos comparando a distribuição de estrelas e forks por linguagem, destacando tecnologias com comunidades maiores (por exemplo, JavaScript, Python, Go) em contraste com linguagens emergentes (Rust, TypeScript). Espera-se observar:

- Boxplots evidenciando que JavaScript e Python concentram repositórios com maiores medianas de estrelas.
- Barras empilhadas revelando alta proporção de issues habilitadas em linguagens com ecossistemas maduros.

### 3.2 Idade Versus Popularidade

Scatter plots cruzando idade do repositório com número total de estrelas e taxa de crescimento de forks permitirão avaliar se projetos mais antigos mantêm relevância ou se iniciativas recentes alcançam rápido engajamento. Tendências esperadas incluem:

- Correlação moderada entre idade e estrelas, com exceções notáveis de projetos jovens altamente populares (por exemplo, frameworks front-end).
- Projetos mais antigos em linguagens consolidadas apresentando taxa de crescimento mais estável, enquanto projetos recentes podem ter variação maior.

### 3.3 Recursos de Colaboração

Gráficos de barras simples mostrarão percentuais de repositórios com wiki e issues ativas. Como a maioria dos repositórios populares oferece ambos os recursos, o objetivo é identificar outliers ou comunidades com práticas diferenciadas.

## 4. Discussão Inicial

A análise preliminar sugere que a popularidade de um repositório está ligada tanto à linguagem quanto à maturidade do projeto. Linguagens amplamente usadas, como JavaScript e Python, tendem a reunir projetos com maior visibilidade e suporte colaborativo robusto. Ao mesmo tempo, há evidências de que frameworks recentes conseguem engajamento rápido, indicando que a idade não é o único determinante do sucesso.

Pontos a aprofundar no relatório final:

- Investigar influência do tamanho (`size_kb`) na capacidade de atrair contribuidores.
- Avaliar se a presença de wiki impacta na taxa de forks ou estrelas.
- Complementar com dados qualitativos (por exemplo, descrição oficial do projeto) para contextualizar resultados atípicos.

O dashboard, aliado ao relatório completo, deverá oferecer uma visão integrada que apoia discussões sobre gestão de projetos open source e estratégias de engajamento em comunidades de software livre.
