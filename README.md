![Thiago Caja Dev Header](docs/assets/img/thiagocajadev-github-header-banner-v8.png)

# Seja bem-vindo(a) <img src="https://user-images.githubusercontent.com/74038190/213844263-a8897a51-32f4-4b3b-b5c2-e1528b89f6f3.png" width="50px" alt="Hand Wave" />

[**🇺🇸 English Version**](docs/md/README.en.md)

Olá **Dev**, **Tech Recruiter** e **entusiasta do código**!

Sou o **Thiago Cajá**, Desenvolvedor de Software com trajetória iniciada em **2007**. Minha jornada na tecnologia é marcada por uma evolução contínua: comecei na base da pirâmide com suporte técnico e configuração de servidores, onde a necessidade de automação me levou aos primeiros scripts `.bat`.

Ao longo dos anos, naveguei por diversos ecossistemas como Java Swing, VB/VB.NET e PHP, até me especializar na solidez do **.NET (C#)**, evoluindo de soluções Desktop para a Web. Essa bagagem técnica é complementada por uma experiência em **Gestão de Suporte (Helpdesk)**, o que me conferiu uma visão consultiva e estratégica sobre o ciclo de vida do software e a experiência do usuário.

Hoje, mantenho uma **stack flexível e moderna** (.NET, React, JS/TS, Docker, Postgres), estudando diariamente para garantir que minhas entregas unam a robustez da engenharia tradicional com a agilidade das tendências AI-Native.

> [!IMPORTANT]
> **"Evite o complexo, prefira o simples e sofisticado"**

Valores que guiam minha jornada: **Humildade**, **Trabalho**, **Sinceridade** e **Dedicação**.

Essa aqui é a minha "rede social" favorita de longe! Mais códigos e menos papo furado 😄.

Meu propósito de vida é ajudar. Percorro esse caminho via TI, consertando e construindo coisas.

Ultimamente faço um `dump` dos pensamentos, escrevendo no meu [blog](https://thiagocaja.dev).

[![Status](https://img.shields.io/badge/Status-Dispon%C3%ADvel%20para%20Projetos-success?style=for-the-badge&logo=github)](mailto:contato@thiagocaja.dev)

### As 4 Leis (Technical Governance)

Aplico estas leis como minha base de **governança técnica** em cada novo projeto, garantindo que o bootstrap (o setup inicial e a definição da arquitetura base) e a evolução de sistemas sigam padrões de excelência desde o primeiro dia:

<p align="left"><img src="https://img.shields.io/badge/%F0%9F%94%92_Hardening-Deny--by--Default-9c4a3f?style=for-the-badge" alt="Hardening - Deny-by-Default" /> <img src="https://img.shields.io/badge/%F0%9F%9A%A6_Resilience-Failure_as_Value-4a6b8c?style=for-the-badge" alt="Resilience - Failure as Value" /> <img src="https://img.shields.io/badge/%F0%9F%8C%8A_The_Cascade-Storytelling_Code-5b8c6a?style=for-the-badge" alt="The Cascade - Storytelling Code" /> <img src="https://img.shields.io/badge/%F0%9F%92%8E_Visual_Excellence-Design_as_Code-6d5d83?style=for-the-badge" alt="Visual Excellence - Design as Code" /></p>

| Lei                   | Comentário Estratégico                                                                                                                                                        |
| :-------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Hardening**         | **Segurança Profunda**: Blindagem de dados e postura _Deny-by-Default_. A segurança não é um "anexo", é o alicerce de qualquer arquitetura séria.                             |
| **Resilience**        | **Gestão de Falhas**: Implementação de _Result Pattern_ para tratar erros como valores de primeira classe, evitando exceções genéricas e garantindo rastreabilidade.          |
| **The Cascade**       | **Código Fluido**: Aplicação de _Top-Down_ e _SLAP_ para que o código possa ser lido como um livro, reduzindo a carga cognitiva de quem o mantém.                             |
| **Visual Excellence** | **Design as Code**: A estética e a precisão da interface são a camada de confiança final. Se o visual é descuidado, o usuário projeta essa dúvida na segurança e performance. |

# SDD: Spec Driven Development

> **"A especificação guia o código, não o contrário."**

Procuro alinhar minha rotina com um fluxo **AI-Native** baseado em **SDD**: a especificação estratégica (`SPEC.md`) precede o primeiro commit. Atuo como o arquiteto que traduz necessidades de negócio em especificações precisas, orquestrando Agentes de IA para uma entrega de alta fidelidade.

**O Ciclo SDLC (5 Fases)**: Minha metodologia segue um ciclo de alta disciplina dividido em 5 etapas obrigatórias:

`SPEC` (O Contrato) → `PLAN` (A Estratégia) → `CODE` (A Execução) → `TEST` (A Verificação) → `END` (A Entrega).

- **Governança**: Veja como aplico este ciclo na [Governança deste Perfil (GOVERNANCE.md)](docs/md/GOVERNANCE.md).
- **Evidência**: Explore uma [Spec de Exemplo (SPEC_SAMPLE.md)](docs/md/SPEC_SAMPLE.md) de um serviço de background real.

**Visão de Futuro**: Acredito que o papel do desenvolvedor moderno está evoluindo para a escrita de especificações precisas e a curadoria técnica. O futuro do desenvolvimento tende a ser a arte de definir, analisar e aprovar o que os **Agentes de IA** escrevem, garantindo que cada linha de código reflita fielmente as regras de negócio e os objetivos do projeto.

**Maturidade e Adaptabilidade**: Acompanho e estudo constantemente novas metodologias e tendências, adaptando-as ao meu fluxo de trabalho para ganhar eficiência, mas sem abrir mão dos processos e fundamentos tradicionais de engenharia que garantem a solidez de um projeto a longo prazo.

- **Fluxo do Pensamento**: Métodos curtos, retorno direto e clareza narrativa.
- **Orquestração GenAI**: **AntiGravity**, **Claude Code** e **Gemini** como copilotos de hardening.
- **Responsabilidade**: Curadoria humana e senso crítico em 100% das entregas.

<details>
  <summary>Conheça mais detalhes da minha metodologia de trabalho (SDD & Pipeline) ⬇️</summary>

## O Conceito Raiz (Input → Process → Output)

Encaro o desenvolvimento como um processo estruturado de transformação de dados e contextos:

```mermaid
flowchart LR
 subgraph Input
    Context -.-> Modeling
 end
 subgraph Output
    Modeling -.-> Processing -.-> Result
 end
```

1. **Entendimento do contexto**: Qual problema estamos resolvendo?
2. **Modelagem das entradas (inputs)**: Organização e estruturação das informações.
3. **Processamento e entrega das saídas (outputs)**: Clareza, eficiência e propósito.

---

## A Esteira de Engenharia (Pipeline 01 a 08)

Minha entrega de valor é baseada em uma esteira de 8 fases de maturidade técnica que garantem que um projeto nasça e cresça com padrões de **Staff Engineering**.

**01. Foundation → 02. Security → 03. CI/CD → 04. RBAC → 05. UI/UX → 06. Domain → 07. Readiness → 08. Ops**

> Para o detalhamento técnico e o meu **Guia de Boas Práticas** de cada fase, consulte o arquivo oficial de Governança:
>
> 📂 **[Manual de Governança (PIPELINE.md)](docs/md/PIPELINE.md)**

</details>

# Aprendizado Contínuo

Me mantenho atualizado com os conteúdos em que acredito:

- [curso.dev](https://curso.dev) → ecossistema Node.js/TypeScript
- [balta.io](https://balta.io) → universo .NET
- [Anthropic](https://www.anthropic.com/learn) → cursos de IA

Sou um eterno pesquisador. Não tenho a pretensão de saber tudo, mas sou movido pela dedicação constante em aprender e dominar aquilo que ainda desconheço. Gosto de compartilhar tudo o que descubro.

<details>
<summary>Eu compartilho mesmo 🙂! Veja aqui dicas pra personalizar seu perfil ⬇️.</summary>
<br>

- [Header do perfil](https://leviarista.github.io/github-profile-header-generator/)
- [Escudos de tecnologia](https://shields.io/)
- [Estatísticas e cards personalizados](https://github.com/anuraghazra/github-readme-stats)
- [Troféus, PacMan, Snake e outros](https://profile-readme-generator.com/)
<br>
</details>

**Posso ajudar em algo?** É só chamar.
<br>

# 📫 Contact

[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0yMiA2YzAtMS4xLS45LTItMi0ySDRDMi45IDQgMiA0LjkgMiA2djEyYzAgMS4xLjkgMiAyIDJoMTZjMS4xIDAgMi0uOSAyLTJWNnptLTIgMC04IDUtOC01aDE2em0wIDEySDRWOGw4IDUgOC01djEweiIvPjwvc3ZnPg==&logoColor=white)](mailto:contato@thiagocaja.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0yMC40NDcgMjAuNDUySDE2Ljg5di01LjU2OWMwLTEuMzI4LS4wMjctMy4wMzktMS44NTItMy4wMzktMS44NTMgMC0yLjEzNiAxLjQ0NS0yLjEzNiAyLjkzOXY1LjY2OUgxMC4zNTRWOUgxMi4zNTRWMTBhLjA0OS4wNDkgMCAwIDAgLjA0OSAwYy40NzctLjkgMS42MzctMS44NTIgMy4zNy0xLjg1MiAzLjYwMSAwIDQuMjY4IDIuMzcgNC4yNjggNS40NTV2Ni4yODh6TTUuMzM3IDcuNDMzYy0xLjE0NCAwLTIuMDYzLS45MjYtMi4wNjMtMi4wNjUgMC0xLjEzOC45Mi0yLjA2MyAyLjA2My0yLjA2MyAxLjE0IDAgMi4wNjMuOTI1IDIuMDYzIDIuMDYzIDAgMS4xMzktLjkyMyAyLjA2NS0yLjA2MyAyLjA2NXpNNy4xMTkgMjAuNDUySDMuNTU0VjloMy41NjV2MTEuNDUyWiIvPjwvc3ZnPg==&logoColor=white)](https://linkedin.com/in/thiagocajadev)

# 💻 Stack

### Backend

![.NET](https://img.shields.io/badge/.NET-7e2bb3?style=for-the-badge&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-68217A?style=for-the-badge&logo=csharp&logoColor=white)
![Minimal APIs](https://img.shields.io/badge/Minimal_APIs-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Entity Framework](https://img.shields.io/badge/Entity_Framework-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Dapper](https://img.shields.io/badge/Dapper-4B32C3?style=for-the-badge&logo=dotnet&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Hono](https://img.shields.io/badge/Hono-E36002?style=for-the-badge&logo=hono&logoColor=white)

### Frontend

![Blazor](https://img.shields.io/badge/Blazor-5C2D91?style=for-the-badge&logo=blazor&logoColor=white)
![Razor Views](https://img.shields.io/badge/Razor_Views-68217A?style=for-the-badge&logo=dotnet&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)

### Database

![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Postgres](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)

### DevOps & Cloud

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Azure DevOps](https://img.shields.io/badge/Azure_DevOps-0078D7?style=for-the-badge&logo=azuredevops&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Cloudflare Workers](https://img.shields.io/badge/Workers-F38020?style=for-the-badge&logo=cloudflareworkers&logoColor=white)
![Cloudflare Pages](https://img.shields.io/badge/Pages-F38020?style=for-the-badge&logo=cloudflarepages&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)

### Quality & Testing

![Jest](https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![TDD](https://img.shields.io/badge/TDD-E34F26?style=for-the-badge&logo=testinglibrary&logoColor=white)
![BDD](https://img.shields.io/badge/BDD-23D18B?style=for-the-badge&logo=cucumber&logoColor=white)
![Conventional Commits](https://img.shields.io/badge/Conventional_Commits-FE5196?style=for-the-badge&logo=conventionalcommits&logoColor=white)
![GitBook](https://img.shields.io/badge/GitBook-3884FF?style=for-the-badge&logo=gitbook&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)
![Confluence](https://img.shields.io/badge/Confluence-172B4D?style=for-the-badge&logo=confluence&logoColor=white)

### Princípios & Padrões

![Clean Code](https://img.shields.io/badge/Clean_Code-051937?style=for-the-badge&logo=readthedocs&logoColor=61DAFB)
![SOLID](https://img.shields.io/badge/SOLID-008793?style=for-the-badge&logo=codefactor&logoColor=white)
![KISS](https://img.shields.io/badge/KISS-004d7a?style=for-the-badge&logo=gnuemacs&logoColor=white)
![YAGNI](https://img.shields.io/badge/YAGNI-1a1a2e?style=for-the-badge&logo=gnuemacs&logoColor=white)
![DRY](https://img.shields.io/badge/DRY-16213e?style=for-the-badge&logo=gnuemacs&logoColor=white)
![SLAP](https://img.shields.io/badge/SLAP-0f3460?style=for-the-badge&logo=readthedocs&logoColor=white)
![Vertical Style](https://img.shields.io/badge/Vertical_Style-533483?style=for-the-badge&logo=readthedocs&logoColor=white)
![Result Pattern](https://img.shields.io/badge/Result_Pattern-e94560?style=for-the-badge&logo=codefactor&logoColor=white)
![Dependency Injection](https://img.shields.io/badge/Dependency_Injection-00bf72?style=for-the-badge&logo=influxdb&logoColor=white)
![Rich Domains](https://img.shields.io/badge/Rich_Domains-a8eb12?style=for-the-badge&logo=googledomains&logoColor=black)
![DDD](https://img.shields.io/badge/DDD-f5a623?style=for-the-badge&logo=diagram&logoColor=black)

# 🤖 Inteligência Artificial Generativa

[![AntiGravity](https://img.shields.io/badge/AntiGravity-000000?style=for-the-badge&logo=google&logoColor=white)](https://deepmind.google/technologies/gemini/)
[![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white)](https://anthropic.com/claude)
[![NotebookLM / Gemini](https://img.shields.io/badge/NotebookLM_/_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://deepmind.google/technologies/gemini/)
[![SDD Spec Driven](https://img.shields.io/badge/SDD-Spec_Driven-blue?style=for-the-badge&logo=read-the-docs&logoColor=white)](https://github.com/thiagocajadev)
[![ChatGPT Plus](https://img.shields.io/badge/ChatGPT_Plus-10a37f?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/chatgpt)
[![DeepSeek](https://img.shields.io/badge/DeepSeek-000000?style=for-the-badge&logo=deepnote&logoColor=white)](https://www.deepseek.com/)

# 🛠️ Ferramentas

### Aplicativos & Produtividade

[![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://code.visualstudio.com/)
[![JetBrains Rider](https://img.shields.io/badge/JetBrains_Rider-000000?style=for-the-badge&logo=jetbrains&logoColor=white)](https://www.jetbrains.com/rider/)
[![Visual Studio](https://img.shields.io/badge/Visual_Studio-5C2D91?style=for-the-badge&logo=visual-studio&logoColor=white)](https://visualstudio.microsoft.com/)
[![Bash](https://img.shields.io/badge/Bash-2C8EBB?style=for-the-badge&logo=gnubash&logoColor=white)](https://www.gnu.org/software/bash/)
[![PowerShell](https://img.shields.io/badge/PowerShell-0078D7?style=for-the-badge&logo=powershell&logoColor=white)](https://learn.microsoft.com/powershell/)
[![Chrome DevTools](https://img.shields.io/badge/DevTools-4285F4?style=for-the-badge&logo=google-chrome&logoColor=white)](https://developer.chrome.com/docs/devtools/)
[![Azure Data Studio](https://img.shields.io/badge/Azure_Data_Studio-0066B8?style=for-the-badge&logo=microsoftazure&logoColor=white)](https://learn.microsoft.com/en-us/sql/azure-data-studio/)
[![SSMS](https://img.shields.io/badge/SQL_Server_Management_Studio-BB0A30?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)](https://learn.microsoft.com/en-us/sql/ssms/)
[![Docker Desktop](https://img.shields.io/badge/Docker_Desktop-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/products/docker-desktop/)
[![Notepad++](https://img.shields.io/badge/Notepad++-8BC34A?style=for-the-badge&logo=notepadplusplus&logoColor=black)](https://notepad-plus-plus.org/)
[![Canva](https://img.shields.io/badge/Canva-00BFA6?style=for-the-badge&logo=canva&logoColor=white)](https://www.canva.com/)
[![Excalidraw](https://img.shields.io/badge/Excalidraw-5865F2?style=for-the-badge&logo=excalidraw&logoColor=white)](https://excalidraw.com/)
[![Draw.io](https://img.shields.io/badge/Draw.io-F08705?style=for-the-badge&logo=diagramsdotnet&logoColor=white)](https://app.diagrams.net/)

### Terminal & Customização

[![JetBrains Mono](https://img.shields.io/badge/JetBrains_Mono-333333?style=for-the-badge&logo=jetbrains&logoColor=white)](https://www.jetbrains.com/pt-br/lp/mono/)
[![JetBrainsMono Nerd Font](https://img.shields.io/badge/Nerd_Font-444444?style=for-the-badge&logo=nerdfonts&logoColor=white)](https://www.nerdfonts.com/font-downloads)
[![One Dark Pro](https://img.shields.io/badge/One_Dark_Pro-282C34?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://github.com/Binaryify/OneDark-Pro)
[![Starship](https://img.shields.io/badge/Starship-FF4081?style=for-the-badge&logo=starship&logoColor=white)](https://starship.rs/)

# 📈 Estatísticas

<div>
  <img align="center" src="https://visitor-badge.laobi.icu/badge?page_id=thiagocajadev.thiagocajadev&left_color=dodgerblue&right_color=slategray" alt="Visitor Counter" />
</div>
<br>

<span>
  <img height="200" src="https://github-readme-stats-v1-thiagocajadev.vercel.app/api?username=thiagocajadev&include_all_commits=true&show=prs_merged_percentage&hide=contribs&show_icons=true&hide_border=true&theme=github_dark_dimmed&rank_icon=github&cache_seconds=604800" />
</span>
<span>
  <img height="200" src="https://github-readme-stats-v1-thiagocajadev.vercel.app/api/top-langs?username=thiagocajadev&layout=compact&langs_count=8&card_width=370&hide_border=true&theme=github_dark_dimmed&cache_seconds=604800" />
</span>
<br><br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/thiagocajadev/thiagocajadev/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/thiagocajadev/thiagocajadev/output/pacman-contribution-graph.svg">
  <img alt="pacman contribution graph" src="https://raw.githubusercontent.com/thiagocajadev/thiagocajadev/output/pacman-contribution-graph.svg">
</picture>

# 📌 Projetos em Destaque

[![MVP Portfolio Finance Dash](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=mvp-finance-dashboard&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/mvp-finance-dashboard)
[![Code Conventions](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=code-conventions&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/code-conventions)
[![SQL Conventions](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=sql-conventions&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/sql-conventions)
[![Clone Tabnews](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=clone-tabnews&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/clone-tabnews)
[![Starship Bash](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=terminal-bash-one-dark-starship-profile&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/terminal-bash-one-dark-starship-profile)
[![PayCheck BR](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=PayCheckBR&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/PayCheckBR)
[![Balta IO - BlazorIBGE](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=BlazorChallengeIBGEv2&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/BlazorChallengeIBGEv2)
[![Fleet MGMT](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=FleetMGMT&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/FleetMGMT)
