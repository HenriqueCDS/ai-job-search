# Search Queries for Job Scraper

<!-- SETUP: Customize these queries based on your skills, target roles, and location -->

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Shipped country-agnostic CLIs include `linkedin-search` and `freehire-search`; Danish demos and any skill you add with `/add-portal` are included the same way. You do **not** need a matching `site:` line below for those CLIs to run.

The `site:` query templates in this file are the **WebSearch fallback** — for portals without a CLI, company career pages, or when a CLI fails.

> Portais dinamarqueses (`jobindex-search`, `jobbank-search`, `jobdanmark-search`, `jobnet-search`) não se aplicam ao mercado brasileiro — ignore os resultados deles ou remova as skills.

## Search Sites

Primary (Brazilian job boards):
- **linkedin.com/jobs** — LinkedIn (também coberto pelo CLI `linkedin-search`)
- **gupy.io** — Gupy (ATS usado pela maioria das empresas de tecnologia no Brasil)
- **catho.com.br** — Catho
- **br.indeed.com** — Indeed Brasil
- **freehire-search** — CLI genérico, útil para páginas de carreira de empresas

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for known target companies

## Query Categories

Queries are grouped by priority. Each query should be combined with your location terms
(São Paulo, Campinas, or "remoto") where the site supports it.

### Priority 1: Desenvolvedor Back End (Python / Java)

Sua direção de carreira mais forte e desejada.

```
site:linkedin.com/jobs "Desenvolvedor Back End" OR "Desenvolvedor Backend" Python OR Java Brasil
site:linkedin.com/jobs "Backend Developer" Python OR Java Brasil
site:gupy.io "desenvolvedor back end" OR "desenvolvedor backend" python OR java
site:catho.com.br "desenvolvedor backend" python OR java
site:br.indeed.com "desenvolvedor backend" python OR java
"desenvolvedor back end" python OR java "São Paulo" OR Campinas OR remoto
```

### Priority 2: Desenvolvedor Python

Termo direto que costuma aparecer isolado nas vagas.

```
site:linkedin.com/jobs "Desenvolvedor Python" Brasil
site:linkedin.com/jobs "Python Developer" Brasil
site:gupy.io "desenvolvedor python"
site:catho.com.br "desenvolvedor python"
site:br.indeed.com "desenvolvedor python"
"desenvolvedor python" "São Paulo" OR Campinas OR remoto
```

### Priority 3: Engenheiro de Software / Analista de Sistemas

Títulos amplos que cobrem backend e integração de sistemas.

```
site:linkedin.com/jobs "Engenheiro de Software" OR "Software Engineer" Python OR Java Brasil
site:linkedin.com/jobs "Analista de Sistemas" OR "Analista Desenvolvedor" Brasil
site:gupy.io "engenheiro de software" OR "analista de sistemas"
site:catho.com.br "engenheiro de software" OR "analista de sistemas"
site:br.indeed.com "engenheiro de software" OR "analista de sistemas"
"engenheiro de software" OR "analista de sistemas" "São Paulo" OR Campinas OR remoto
```

### Priority 4: Engenheiro de Dados / ETL

Sua expertise de domínio (pipelines, Pandas, integração de bases).

```
site:linkedin.com/jobs "engenheiro de dados" OR "data engineer" ETL OR Python Brasil
site:gupy.io "engenheiro de dados" ETL OR python
site:catho.com.br "engenheiro de dados" ETL
site:br.indeed.com "engenheiro de dados" ETL
"engenheiro de dados" OR "analista de dados" ETL "São Paulo" OR Campinas OR remoto
```

### Priority 5: AI / ML Engineer (RAG, LangChain)

Roles adjacentes, aproveitando os projetos pessoais de RAG.

```
site:linkedin.com/jobs "AI Engineer" OR "engenheiro de IA" LangChain OR RAG Brasil
site:linkedin.com/jobs "machine learning engineer" python Brasil
site:gupy.io "engenheiro de ia" OR "ai engineer" OR langchain
"IA generativa" OR RAG OR LangChain desenvolvedor "São Paulo" OR remoto
```

### Priority 6: Desenvolvedor Front End / Full Stack

Rede mais ampla, aproveitando React / JavaScript / TypeScript.

```
site:linkedin.com/jobs "Desenvolvedor Front End" OR "Frontend Developer" React Brasil
site:linkedin.com/jobs "desenvolvedor full stack" python OR java OR react Brasil
site:gupy.io "desenvolvedor front end" OR "desenvolvedor full stack" react
site:catho.com.br "desenvolvedor front end" OR "desenvolvedor full stack"
site:br.indeed.com "desenvolvedor front end" OR "desenvolvedor full stack"
"desenvolvedor front end" OR "desenvolvedor full stack" "São Paulo" OR Campinas OR remoto
```

## Location Filter

When evaluating results, verify the job location fits one of these tiers:

- **Ideal:** Remoto (qualquer lugar do Brasil, qualquer distância) — sempre aceitável
- **Ideal:** Hortolândia, SP e região; Campinas, SP e Região Metropolitana de Campinas
  (Sumaré, Valinhos, Indaiatuba, Americana, Paulínia) — presencial/híbrido
- **Aceitável:** Região Metropolitana de São Paulo (capital e Grande SP) — presencial ou híbrido
- **Aceitável:** Interior de SP no eixo Campinas–São Paulo (Jundiaí, Vinhedo, Louveira)
- **Muito longe:** Vagas presenciais fora do estado de SP ou fora dos eixos acima
  (salvo exceção justificada, ex.: híbrido com baixa frequência)

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape [focus_area]" -> relevant category queries + custom focus-specific queries
