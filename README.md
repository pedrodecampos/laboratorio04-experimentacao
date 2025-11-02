# Laboratório 04 - Visualização de Dados com BI

## Objetivo

Criar um dashboard utilizando Google Data Studio para apresentar resultados de experimentação baseado em repositórios do GitHub.

## Dataset

- **Arquivo**: `data/dataset.csv`
- **Registros**: 100 repositórios do GitHub
- **Atributos**: 9 colunas (ID, nome, linguagem, stars, forks, data de criação, tamanho, wiki, issues)
- **Tipo**: Análise de projetos open-source por linguagem de programação
- **Origem**: Os dados foram obtidos via GitHub REST API v3 em outubro de 2025.
- **Link Google Looker Studio**: https://lookerstudio.google.com/s/o0OkPZ8rG-A

## Estrutura do Projeto

```
lab4/
├── README.md
├── data/
│   └── dataset.csv                # Dataset com 100 repositórios GitHub
├── docs/
│   ├── caracterizacao.md          # Caracterização do dataset
│   └── perguntas_pesquisa.md      # Template para RQs (Sprint 2)
└── dashboard/                     # Arquivos do dashboard
    └── [dashboard do Google Data Studio]
```

## Sprint 1: Caracterização do Dataset

### Visualizações Criadas

1. Card: Total de Repositórios (100)
2. Pizza: Distribuição por Linguagem
3. Barras: Top Repositórios por Stars
4. Barras: Média de Stars por Linguagem
5. Dispersão: Stars vs Forks
6. Linha: Repositórios por Ano
7. Tabela: Resumo por Linguagem

### Entregáveis Sprint 1

- Dashboard criado no Google Data Studio
- 7 visualizações de caracterização
- Dashboard exportado como PDF
- Apresentação preparada (máx 15 min)

## Próximas Sprints

- **Sprint 2**: Visualizações para RQ1 e RQ2
- **Sprint 3**: Dashboard final + Artigo TIS6 atualizado

## Ferramenta Utilizada

**Google Data Studio** (atual Looker Studio)

- Interface web
- Gratuito
- Fácil compartilhamento
