# Perguntas de Pesquisa (Sprint 02)

> Dataset: `data/dataset.csv` (100 repositórios do GitHub; colunas: repository_id, name, language, stars, forks, created_at, size_kb, has_wiki, has_issues)

## RQ1 — Como a popularidade varia por linguagem?
**Motivação.** Linguagens diferentes possuem ecossistemas e tamanhos de comunidade distintos; queremos entender concentração de popularidade.

**Hipóteses.**
- H1a: JavaScript e Python concentram as maiores **somas** e **medianas** de *stars* e *forks*.
- H1b: Linguagens de nicho (p. ex., Assembly, Scala) terão distribuição de popularidade mais assimétrica (maior dispersão).

**Métricas-alvo.**
- Stars: soma, média, mediana e boxplot por `language`.
- Forks: soma, média, mediana por `language`.

**Visualizações propostas.**
- (V1) Barras empilhadas: `language` × soma de `stars` e `forks`.
- (V2) Boxplot de `stars` por `language` (ou, no Looker Studio: gráfico de **caixa e bigodes** via *community viz* / alternativa com **pontos** + **linhas de referência** para mediana).
- (V3) Tabela ranqueada por `language` com métricas resumidas.

**Filtros.**
- `has_issues` (True/False)
- `has_wiki` (True/False)
- Intervalo de `created_at` (ano inicial/final)

**Critérios de Aceite.**
- CA1: As visualizações permitem filtrar por `has_issues`, `has_wiki` e faixa de ano.
- CA2: Cada gráfico exibe rótulos e tooltip com `language` e valores.
- CA3: Há **pelo menos 2** gráficos complementares (V1 e V3) e um gráfico de dispersão/boxplot.

---

## RQ2 — Qual é a relação entre idade do repositório e popularidade?
**Motivação.** Projetos mais antigos podem acumular mais estrelas/forks, mas há *outliers* recentes com explosão de popularidade.

**Hipóteses.**
- H2a: Correlação positiva moderada entre **idade** e `stars`.
- H2b: Frameworks/libraries lançados após 2015 (p. ex., *React*, *Vue*, *Next.js*) podem apresentar alta popularidade mesmo com menor idade.

**Métricas-alvo.**
- Idade (anos) = `DATETIME_DIFF(TODAY(), created_at, YEAR)` (no Looker Studio).
- Correlação (indicativa) e tendência visual `idade` × `stars`.

**Visualizações propostas.**
- (V4) Dispersão: eixo X = idade (anos), eixo Y = `stars`; *size/shape* = `forks`; cor = `language`.
- (V5) Linhas/área por coorte anual (ano de `created_at`) mostrando soma de `stars`.

**Filtros.**
- `language` (multi-seleção)
- `has_issues`, `has_wiki`

**Critérios de Aceite.**
- CA4: Dispersão com *trendline* habilitada.
- CA5: Tooltip exibe `name`, `language`, `stars`, `forks`, `created_at`.
- CA6: Painel possui *filter controls* reutilizáveis com realce visual.

---

## Campos Calculados (Looker Studio)

- **Ano de criação**: `YEAR(created_at)`
- **Idade (anos)**: `DATETIME_DIFF(CURRENT_DATE(), created_at, YEAR)`
- **Stars por KB**: `stars / size_kb` (opcional, para normalização de tamanho)
- **Forks por KB**: `forks / size_kb`

---

## Plano de Validação

1. Validar integridade do dataset (100 linhas; 9 colunas; tipos: numéricos, datas e booleanos).
2. Checar consistência de datas (`created_at` no formato ISO).
3. Conferir somatórios por linguagem vs. amostras esperadas (sanity check).
4. Revisar se filtros impactam **todas** as visualizações (interações globais).
5. Tirar *screenshots* do painel e anexar no relatório parcial.

