# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/),
and this project adheres to [Semantic Versioning](https://semver.org/).

## [Unreleased]

### Added

- Set the `Projetos em Destaque` / `Featured Projects` block to eight pinned cards in both READMEs, in the order the developer chose: Code Style, DoDocs, Spec-Driven Guide, Spec-Driven Guide Prompts, PayCheck BR, League Teamfight Mode, Clone TabNews and Balta Projects Archive. Clone TabNews and Balta sit at positions seven and eight so they land on the same row of the two-column grid.
- Indexed fifteen public repositories with description, homepage and topics through `gh repo edit`, raising the topic count from zero to 191. Six repositories had an empty homepage field while their production site was live, and `do-docs` pointed at the upstream pmndrs site instead of its own.
- Added governance philosophy document (`docs/md/pt-br/GOVERNANCA-DETALHES.md` and `docs/md/en/GOVERNANCE-DETAILS.md`) covering convictions, staff engineer mindset, landing/onboarding, ADRs, auditable process, and standards (RFC/ISO/OWASP/SemVer/Conventional Commits) as a basis for decision-making.
- Linked the new governance details document from both READMEs (pt-br and en) under the Governance section.
- Added the "Conheça meu trabalho" / "Get to know my work" section to both READMEs (pt-br and en), linking the Frontend Showcase (`fs.thiagocaja.dev`) and the Backend Showcase (`bs.thiagocaja.dev`) as portfolio evidence of fullstack delivery.

### Fixed

- Passed the writing soul over three prose blocks in both READMEs: the intro, the interface-detail paragraph, and the closing line of the personal-details section. Dropped two banned adverbs from the English file, softened an absolute stated without data into a frequency claim, and stated the point directly where the text had used a binary contrast about interface aesthetics. `writing-lint.mjs` reports no hits on README.md, README.en.md and CHANGELOG.md.
- Removed the eight cards that no longer matched the profile, including `sdg-agents-cli`, which had been renamed to `spec-driven-guide` and rendered a broken card in the English README.
- Rewrote every public repository description under `writing-soul.md`. Twelve carried an em dash, banned in both lexicons, and `code-style` personified an artifact by calling its documentation alive. The two Spec-Driven Guide repositories ship in English, the rest in Brazilian Portuguese, as declared by the developer. `writing-lint.mjs` reports no hits on the twenty-three descriptions.
- Left the eight historic repositories without topics on the developer's call: they record the start of his web work and do not compete for search.
- Restructured the "Minha Stack" / "My Stack" section in both READMEs from four combined groups into ten stackable ones (Languages, Backend, Frontend, Database, Cloud & containers, Security, Code quality, Principles, Patterns, Processes), adding VB.NET, SQL, Bootstrap, Bulma, MySQL, MariaDB, Oracle, Firebird, AWS, Azure, the OWASP/JWT/JOSE/OAuth/OpenID Connect/TLS security badges, the Zod/Biome/Prettier/ESLint/dotnet format/EditorConfig tooling badges, Strategy/Repository/Unit of Work/Specification/CQRS, and BDD/BPM/SDD/Conventional Commits/SemVer/RFC.
- Expanded the Principles block in both READMEs to eleven badges grouped by scope: Clean Code and Clean Architecture open the row as the reference pair, followed by the KISS/YAGNI/DRY heuristics, then SOLID and one badge per principle (SRP, OCP, LSP, ISP, DIP). Each group carries its own descending tonal ramp.
- Applied a descending tonal ramp to the Patterns badges so the six no longer share one flat color.
- Reorganized "IAs & Ferramentas" / "AIs & Tools" into "IA & Ferramentas" / "AI & Tools" with four groups: Generative AI (Claude Code first, then Gemini, Kimi, ChatGPT Plus, DeepSeek), IDEs & editors (Antigravity moved here, Visual Studio added), Database tools (SSMS, DBeaver, pgAdmin), and Terminal & runtime.
- Added a "Gestão de projetos" / "Project Management" section to both READMEs covering Jira, Confluence, Google Keep, Markdown, and MDX.
- Renamed "Aprendizado & Dicas" / "Learning & Tips" to "Aprendizado & Comunidade" / "Learning & Community"; the section body is unchanged.
- Closed the intro of both READMEs on "Meu propósito é Resolver Problemas" / "My purpose is to Solve Problems", dropping the sentence that ranked the author below senior before any evidence was shown.
- Fixed spelling in both READMEs: "melhoria continua" to "contínua", "fluído" to "fluido", "Raíz" to "Raiz", and the English "Fluxes that guide" to "Flows that guide".
- Fixed thirteen shields.io badges whose icons stopped rendering after simple-icons dropped trademark-restricted brand slugs. `css3` now uses `css`, C# uses `dotnet`, RFC uses `readthedocs`, and DDD uses `diagramsdotnet`. SQL Server, SSMS, Oracle, Firebird, AWS, Azure, VS Code, Visual Studio, and ChatGPT Plus carry an inline base64 SVG (database cylinder, cloud, code brackets, spark), so every badge in the file renders an icon.
- Rewrote the Anti-Patterns and Patterns section in both READMEs (pt-br and en) as paired problem/fix tables aligned with the blog post "Anti-Patterns: evite problemas conhecidos", replacing the separate anti-pattern and pattern bullet lists; the rewritten example now uses a structured `Result` contract, and each table row matches the shown code.
- Renamed the "Cascade / Narrative Code" governance law to "Narrative / Documentative Code" (badge and table) in both READMEs.
- Fixed "Código Narrativor" typo in `docs/md/pt-br/SDD-DETALHES.md`.
- Fixed Mermaid diagram syntax in `docs/md/pt-br/SDD-DETALHES.md` and `docs/md/en/SDD-DETAILS.md` by quoting labels with parentheses.
- Refactored UI/UX Design Thinking section with a focus on scannability and "Writing Soul" tone.
- Synchronized English README with all Portuguese version improvements.
- Updated code nomenclature from "Lexical Scoping" to "Step-down Rule" (Regra do Degrau).
- Fixed theme demonstration GIF path in READMEs.
- Synchronized 6 divergences between EN and PT READMEs: AI/EI blockquote, missing `findOrder` function in two narrative code examples, inconsistent bullet markers, "Estatistics" typo, and Governance emoji (🏛️).
- Replaced `delinquent` / `notifyDelinquency` with neutral `overdue` / `notifyOverdue` in the English README narrative code examples.
