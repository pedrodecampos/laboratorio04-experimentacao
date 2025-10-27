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

- Número de registros: 13
- Repositórios: awesome-python, tensorflow, pytorch, django, flask, requests, scikit-learn, pandas, matplotlib, numpy, scrapy, celery, sqlalchemy, fastapi, pytest
- Características principais:
  - Média de stars: 36,800
  - Forte presença em ciência de dados e web

### Grupo 2: JavaScript

- Número de registros: 31
- Repositórios: react, vue, next.js, gatsby, express, node, webpack, babel, jest, axios, lodash, moment, redux, webpack-dev-server, svelte, three.js, phaser, chart.js, d3, leaflet, marked, prettier, eslint, grunt
- Características principais:
  - Média de stars: 48,500
  - Dominância em frameworks front-end
  - Alta popularidade

### Grupo 3: Java

- Número de registros: 10
- Repositórios: java-design-patterns, spring-boot, hibernate, spring-framework, okhttp, guava, retrofit, butterknife, material-components, lombok, mockito, selenium
- Características principais:
  - Média de stars: 22,000
  - Uso em aplicações enterprise

### Grupo 4: Go

- Número de registros: 10
- Repositórios: kubernetes, docker, gin, prometheus, grafana, traefik, etcd, consul, viper, cobra, mockery, mux
- Características principais:
  - Média de stars: 37,700
  - Popularidade em ferramentas DevOps e infraestrutura

### Grupo 5: Outras Linguagens

- Número de registros: 36
- Linguagens: Assembly, TypeScript, Ruby, Scala, Rust, PHP
- Características principais:
  - Diversidade de casos de uso
  - Inclui linguagens especializadas
  - PHP: 10 repositórios
  - Rust: 10 repositórios
  - Ruby: 10 repositórios
  - Outras: 6 repositórios

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

- **Média de Stars**: 35,200
- **Mediana de Stars**: 21,000
- **Desvio Padrão**: ~27,500
- **Repositório com mais stars**: vue (190,000)
- **Repositório com menos stars**: ferris-says (1,800)

- **Média de Forks**: 8,500
- **Mediana de Forks**: 5,500
- **Repositório com mais forks**: tensorflow (86,000)

### Análise por Grupo

- **Linguagem Mais Popular (total de stars)**: JavaScript (mais repositórios)
- **Linguagem Mais Antiga**: linux (2005)
- **Linguagem Mais Nova**: fastapi (2018)
- **Maior Diversidade**: JavaScript (31 repositórios)
