# Concept

Hook lädt `context/` folder in session context sobald eine session startet. 
In den folder kommen alle wichtigen PA conventionen :

- Zitat convention (typst enablement) => citation.md //Done
- Forschungsfrage bedeutung => research-question.md
- Gliederungsstruktur => structure.md
- argumentationsstrategie / roter faden => argumentation.md
- Quellensuche und verwaltung => sources.md

**Wichtig**: die context files MÜSSEN klein sein. Jeder Char kostet kontext in jeder session und jedem prompt

Wir nutzen Skills um den Zweck der jeweiligen Session zu bestimmen.
Claude sollte sich immer nur auf ein Kapitel fokussieren, außer anders verlangt.

# Neue Features

- Scraper Skill mit Playwright MCP //müssen wir drüber sprechen ob scrapen möglich sein sollte
- Quellensuch Skill/Agent
- Forschungsfrage Skill/Agent
- Struktur Skill/Agent
- Write Skill/Agent
- Review Skill/Agent council

# Verbesserungen

- Setup skill überarbeiten
- doctor command überarbeiten
- NLM-skill und typst skill anpassen auf use case

# Conventions

- Skills auf englisch für anweisungen
- Skills output standardmäßig deutsch
- MVP Scope: Auf DHBW und PA kontext zugeschnitten