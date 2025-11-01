# Caracterização do Dataset

## Descrição Geral

Este dataset contém informações sobre 100 repositórios populares do GitHub, representando projetos open-source de diferentes linguagens de programação. O objetivo é analisar as características e popularidade de projetos open-source.

## Tamanho do Dataset

- Número total de registros: 100 repositórios
- Número de atributos: 9 colunas

## Atributos Principais

- **repository_id**: Identificador único do repositório
- **name**: Nome do repositório no GitHub
- **language**: Linguagem de programação primária
- **stars**: Número total de stars
- **forks**: Número de forks
- **created_at**: Data de criação do repositório
- **size_kb**: Tamanho do repositório em kilobytes
- **has_wiki**: Se o repositório possui wiki
- **has_issues**: Se o repositório possui sistema de issues

## Particionamento do Dataset

O dataset foi particionado por linguagem de programação para permitir análises comparativas.

### Grupo 1: Python

- Número de registros: 15
- Repositórios: awesome-python, tensorflow, pytorch, django, flask, requests, scikit-learn, pandas, matplotlib, numpy, scrapy, celery, sqlalchemy, fastapi, pytest
- Características principais:
  - Média de stars: 49.200
  - Forte presença em ciência de dados, web e frameworks de machine learning

### Grupo 2: JavaScript

- Número de registros: 24
- Principais repositórios: react, vue, next.js, gatsby, express, node, webpack, babel, axios, jest, lodash, moment, redux, svelte, three.js, d3, chart.js, prettier, eslint, grunt (demais no dashboard)
- Características principais:
  - Média de stars: 67.063
  - Dominância de frameworks front-end e ferramentas do ecossistema web

### Grupo 3: Java

- Número de registros: 12
- Repositórios: java-design-patterns, spring-boot, spring-framework, hibernate, okhttp, guava, retrofit, butterknife, material-components, lombok, mockito, selenium
- Características principais:
  - Média de stars: 34.617
  - Forte associação a soluções enterprise e bibliotecas para APIs

### Grupo 4: Go

- Número de registros: 12
- Repositórios: kubernetes, docker, gin, prometheus, grafana, traefik, etcd, consul, viper, cobra, mockery, mux
- Características principais:
  - Média de stars: 42.983
  - Popularidade em ferramentas DevOps, observabilidade e infraestrutura

### Grupo 5: Outras Linguagens

- Número de registros: 37 (Assembly, PHP, Rust, Ruby, Scala, TypeScript)
- Destaques:
  - PHP: 12 repositórios (ex.: laravel, symfony, guzzle, phpunit)
  - Rust: 11 repositórios (ex.: tokio, actix-web, clap, wasm-pack)
  - Ruby: 11 repositórios (ex.: rails, devise, rspec, sidekiq)
  - Assembly, Scala e TypeScript contam com um repositório cada
- Características principais:
  - Ecossistema heterogêneo que cobre desde web até ferramentas de baixo nível

### Sprint 1 - Caracterização

1. **Card**: Total de Repositórios (100)

2. **Gráfico de Pizza**: Distribuição por Linguagem de Programação

3. **Gráfico de Barras**: Top 10 Repositórios por Número de Stars

4. **Gráfico de Barras**: Média de Stars por Linguagem de Programação

5. **Gráfico de Dispersão**: Relação entre Stars e Forks

6. **Gráfico de Linha**: Repositórios Criados por Ano

7. **Tabela**: Resumo por Linguagem (Contagem, Média e Soma de Stars)

8. **Controle de Filtro**: Por Linguagem (para interatividade)

## Métricas Estatísticas

### Estatísticas Gerais

- **Média de Stars**: 41.404
- **Mediana de Stars**: 32.000
- **Desvio Padrão**: 37.911
- **Repositório com mais stars**: vue (190.000)
- **Repositório com menos stars**: ferris-says (1.800)

- **Média de Forks**: 9.789
- **Mediana de Forks**: 5.400
- **Repositório com mais forks**: tensorflow (86.000)

### Análise por Grupo

- **Maior volume de stars (soma)**: JavaScript (1.609.500 stars em 24 repositórios)
- **Repositório mais antigo**: hibernate (Java, 2001)
- **Repositório mais recente**: fastapi (Python, 2018)
- **Maior diversidade de projetos**: JavaScript (24 repositórios em múltiplas categorias)
