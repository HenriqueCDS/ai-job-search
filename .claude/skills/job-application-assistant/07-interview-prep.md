---
framework_version: 1.0.0
---

# Interview Preparation Guide

<!-- SETUP: STAR examples are personalized by running /setup based on your actual experience -->

## STAR Format

Structure answers as: **Situation** (context), **Task** (your responsibility), **Action** (what you did), **Result** (outcome).

Keep answers to 1-2 minutes. Be specific. End with what you learned or would do differently.

## Ready-Made STAR Examples

### 1. Automação da sincronização de matrículas no Canvas LMS (Automação/Python)
**S:** A equipe gastava tempo significativo conferindo manualmente matrículas e sincronizações entre o Canvas LMS e as bases institucionais.
**T:** Reduzir o esforço manual da equipe sem comprometer a integridade dos dados acadêmicos.
**A:** Desenvolvi automações em Python integradas à API REST do Canvas para criação de salas, sincronização de matrículas e auditoria de acessos, além de rotinas em Jupyter Notebook que comparam dados do Canvas com bases institucionais em CSV.
**R:** Eliminou o retrabalho de conferência manual e reduziu o tempo das rotinas operacionais da equipe.
**Use for:** "Fale sobre uma vez que você automatizou um processo", "Como você lida com trabalho repetitivo?"

### 2. Pipeline de ETL para integridade de dados acadêmicos (ETL/Confiabilidade)
**S:** O Canvas LMS processa mais de 150.000 registros acadêmicos por ciclo letivo, com risco de inconsistências entre sistemas.
**T:** Garantir a integridade desses registros ao longo do ciclo letivo.
**A:** Implementei pipelines de ETL em Python e Pandas com regras de validação, tratamento de inconsistências e conciliação entre bases.
**R:** Assegurou a integridade de mais de 150.000 registros acadêmicos por ciclo letivo, sustentando o Canvas LMS para 16.500 alunos e docentes.
**Use for:** "Descreva um projeto de dados que você liderou", "Como você garante qualidade de dados?"

### 3. Agente de RAG para suporte acadêmico (ia-agent-puc-digital) (IA aplicada/Projeto pessoal)
**S:** Interesse pessoal em aplicar IA generativa a um problema real de suporte acadêmico, fora do escopo do cargo formal.
**T:** Construir um agente de RAG funcional, com qualidade de produção (testes, containerização).
**A:** Desenvolvi um agente em Python (FastAPI, LangChain) com ingestão idempotente de PDFs, embeddings locais, busca por similaridade em pgvector, cache de respostas em Postgres, integração com a API Gemini e cobertura de 25 testes automatizados (pytest); ambiente containerizado com Docker.
**R:** Projeto funcional publicado no GitHub, demonstrando aplicação prática de RAG/LangChain além do escopo do trabalho diário.
**Use for:** "Fale sobre um projeto de IA que você construiu", "Como você aprende novas tecnologias por conta própria?"

### 4. Migração de lançamentos manuais para integração automatizada com NetSuite (Integração de sistemas/Java)
**S:** Na FUNCAMP, processos de negócio dependiam de lançamentos manuais recorrentes entre sistemas internos e o ERP NetSuite.
**T:** Eliminar esse trabalho manual através de integração automatizada.
**A:** Desenvolvi scripts de integração em Java que substituíram os lançamentos manuais recorrentes.
**R:** Reduziu o esforço manual da equipe e o risco de erro humano nos lançamentos.
**Use for:** "Descreva uma integração de sistemas que você construiu", "Como você lida com sistemas legados?"

## Common Tough Questions

### "Why did you leave [previous company]?"
> [PREPARE YOUR ANSWER - be honest, forward-looking, no negativity about former employer]

### "You don't have [specific skill/experience]."
> [PREPARE YOUR ANSWER - acknowledge the gap, bridge to adjacent experience, show willingness to learn]

### "Where do you see yourself in 5 years?"
> [PREPARE YOUR ANSWER - show ambition aligned with the role's growth path]

### "What's your biggest weakness?"
> [PREPARE YOUR ANSWER - genuine weakness with concrete mitigation strategy]

### "Why this company specifically?"
> Customize per company. Must reference: specific projects, company values, market position, or team structure. Never give a generic answer.

## Questions You Should Ask Interviewers

### About the Role
- "What does a typical week look like in this role?"
- "What would success look like in the first 6 months?"
- "What's the biggest challenge the team is facing right now?"

### About the Team
- "How big is the team, and how do you divide work?"
- "What does the development/project lifecycle look like, from idea to production?"
- "How do you onboard new team members?"

### About Tech & Growth
- "What's your current tech stack for [relevant area]?"
- "Is there room to grow into more architectural or strategic decisions?"
- "How does the team stay current with new tools and methods?"

### About Culture (use these to prevent disappointment)
- "How would you describe the team culture?"
- "What does professional development look like here?"
- "Is there flexibility for remote/hybrid work?"
- "What's the balance between development/new projects and maintenance work?"
- "How would you describe the leadership style in this team?"
- "What do people who thrive here have in common?"

## Phone/Video Interview Tips
- Have STAR examples written out (use this file)
- Keep a glass of water nearby
- Smile when speaking (it changes your tone)
- Ask for clarification if a question is vague
- It's OK to take 5 seconds to think before answering
- End with: "Is there anything else you'd like to know about my background?"

## After the Application (Best Practice)

### Follow-Up Etiquette
- **Don't call to "stand out"** or to learn more about the role post-submission - this risks a negative impression
- If the employer specified a timeline, respect it and wait
- If no timeline was given and significant time has passed (2+ weeks), a brief call to ask about status is acceptable
- If you have genuinely new, relevant information to share, a short follow-up is fine

### Thank-You Notes
- When you receive any update (interview invitation, rejection, or status update), send a brief thank-you message
- Express appreciation for their time and the process
- Keep it short (2-3 sentences)

## Roleplay Guidelines
When the user asks for interview practice:
1. Ask which role/company to simulate
2. Start with easy warm-up questions ("Tell me about yourself")
3. Progress to role-specific technical questions
4. Include 1-2 behavioral questions using the competencies from the job posting
5. End with a tough question or curveball
6. After each answer, give brief feedback: what worked, what to sharpen
7. Suggest which STAR example would work best for each question
