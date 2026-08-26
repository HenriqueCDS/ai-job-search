# Search Queries for Job Scraper

<!-- SETUP: Customize these queries based on your skills, target roles, and location -->

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Shipped country-agnostic CLIs include `linkedin-search` and `freehire-search`; Danish demos and any skill you add with `/add-portal` are included the same way. You do **not** need a matching `site:` line below for those CLIs to run.

The `site:` query templates in this file are the **WebSearch fallback** — for portals without a CLI, company career pages, or when a CLI fails.

## Search Sites

Primary (your market's job boards - scaffold one with `/add-portal`):
- **linkedin.com/jobs** - LinkedIn job listings (filter: Brasil / Campinas-SP); also covered by `linkedin-search` CLI
- **Gupy, Catho, InfoJobs** - major Brazilian job boards (candidate for `/add-portal` scaffolding)
- **freehire-search** - shipped country-agnostic CLI, useful fallback for direct company career pages

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for known target companies

## Query Categories

Queries are grouped by priority. Each query should be combined with your location terms (e.g. your city, region, or metro area) where the site supports it.

### Priority 1: Desenvolvedor Backend (Python/Java)

These match your strongest and most desired career direction.

```
site:linkedin.com/jobs "Desenvolvedor Backend" Python Brasil
site:linkedin.com/jobs "Backend Developer" Java Brasil
"desenvolvedor backend" python OR java Campinas OR remoto
```

### Priority 2: Engenheiro de Dados / ETL

These match your domain expertise.

```
site:linkedin.com/jobs "engenheiro de dados" ETL Brasil
site:linkedin.com/jobs "data engineer" python Brasil
"engenheiro de dados" OR "analista de dados" ETL Campinas OR remoto
```

### Priority 3: AI/ML Engineer (RAG, LangChain)

Adjacent roles you could pivot into, leveraging personal RAG project experience.

```
site:linkedin.com/jobs "AI Engineer" OR "engenheiro de IA" LangChain Brasil
site:linkedin.com/jobs "machine learning engineer" python Brasil
"IA generativa" OR RAG OR LangChain desenvolvedor Brasil
```

### Priority 4: Full Stack

Wider net leveraging frontend experience (React/JS/PHP) alongside backend.

```
site:linkedin.com/jobs "desenvolvedor full stack" python OR java Brasil
site:linkedin.com/jobs "full stack developer" react Brasil
"desenvolvedor full stack" Campinas OR remoto
```

## Location Filter

When evaluating results, verify the job location is within reasonable commute distance from your home. Define acceptable areas:
- Hortolândia, SP and surrounding areas
- Campinas, SP (presencial/híbrido)
- Região Metropolitana de Campinas (Sumaré, Valinhos, Indaiatuba, Americana)
- Remoto (qualquer lugar do Brasil) - sempre aceitável
- Vagas presenciais fora da região de Campinas (muito longe, salvo exceção justificada)

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape [focus_area]" -> relevant category queries + custom focus-specific queries
