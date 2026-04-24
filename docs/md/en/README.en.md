![Thiago Caja Dev Header](../../assets/img/thiagocajadev-github-header-banner-v1.png)

# Welcome <img src="https://user-images.githubusercontent.com/74038190/213844263-a8897a51-32f4-4b3b-b5c2-e1528b89f6f3.png" width="50px" alt="Hand Wave" />

[**🇧🇷 Versão em Português**](../../../README.md)

Hello **Dev**, **Tech Recruiter**, and **code enthusiast**!

I'm **Thiago Cajá**. I started in Technology in **2007**, initially working in technical support and server administration. It was by creating my first `.bat` scripts to automate repetitive tasks that I realized the value of efficiency and saving time. Since then, I have always strived for continuous improvement.

I explored various languages like Java, VB, and PHP before finding my home in the **.NET (C#)** ecosystem. Leading a support team (**Helpdesk**) taught me a life lesson: a problem is never just about the computer or the system. Code is simply a tool to solve real people's pain points and ensure processes flow smoothly.

Today, I work with a **modern stack** (**.NET**, **React**, **Docker**, **Postgres**), blending software engineering solidity with the agility of the **AI-Native** world. My goal is to build robust and secure systems, always aiming to simplify and facilitate the daily routines of developers and users.

I will never know all the answers, but I know how to research and search for alternatives. I would hardly consider myself a Senior or Specialist. I prefer to be a **Problem Solver**.

> [!IMPORTANT]
> **"Avoid the complex, prefer the simple and sophisticated"**

[![Status](https://img.shields.io/badge/Status-Available%20for%20Projects-success?style=for-the-badge&logo=github)](mailto:contato@thiagocaja.dev)

<details>
<summary><b> 📖 A bit more about me</b></summary>

### My values

Values that guide my journey: **Humility**, **Hard Work**, **Sincerity**, and **Dedication**.
<br>

This is my favorite "social network" by far! More code and less small talk 😄.
<br>

My life purpose is to help. I follow this path through IT, fixing and building things.
<br>

> **"In times of AI, practice EI (Emotional Intelligence)."**
>
> Artificial Intelligence is an incredible tool and amplifies you, but decisions should be made based on data, not guesswork.

Are you starting to use the SDD (Spec-Driven Development) methodology in your projects?
This guide can help you [specdrivenguide.org](https://specdrivenguide.org). Come join us!
<br>

Lately, I've been doing a "thought dump" on my [blog](https://thiagocaja.dev).

---

</details>

<details>
<summary><b> 🎨 UI/UX Design Thinking</b></summary>

### Visual architecture

> "Design the solution. It has to be easy to use."

Before any line of code, I think about the interface with **technical empathy**: focusing on productivity for those developing the frontend and real usability for those using the product.

I use **Design Thinking** to define what matters. I maintain the scope under a clear and functional hierarchy:

| Category        | Tokens and elements                                                       |
| :-------------- | :------------------------------------------------------------------------ |
| **Foundations** | Mobile/Desktop first · Colors · Typography · Spacings · Shadows · Borders |
| **Assets**      | Icons · Images · Videos · Audio · Documents                               |
| **Interface**   | Links · Buttons · Forms · Tables · Charts · Maps                          |

### Theme systems (Light & Dark)

Alternating between themes requires rigorous contrast control to avoid visual fatigue. I apply the concept of <b>surface + luminance</b> to ensure depth.

> Each element lives at a specific depth. Components that stay "inside" others move up a level and gain more <b>luminance</b> (perceived brightness), preserving the base color. This maintains natural depth in both light and dark modes.

<img src="../../assets/img/theme-light-dark.gif" alt="Light and Dark theme example" />

### Styling

Attention to detail defines retention. I use modern tools (Tailwind CSS, Shadcn UI, Lucide) to create interfaces that look current and professional. Updated aesthetics are not just "eye candy"; they facilitate system adoption.

- Fluxes that guide the user intuitively toward the objective.
- Balance between visual density and whitespace.
- Standardized grid and spacings.
- Logical content division (steps, tabs, modals).

### Anti-patterns (UI/UX)

A bad experience is a cost for support and churn. Some points I treat as red flags:

- <b>Information overload</b>: Overloaded screens that confuse the focus.
- <b>Dense tables</b>: Long lists without pagination, filters, or search.
- <b>Visual pollution</b>: Excessively vibrant colors or lack of contrast.
- <b>Decorative animations</b>: Movements that do not communicate state or feedback.
- <b>Rigidity</b>: Use of fixed pixels where the layout should be fluid.
- <b>Platform bias</b>: Designing thinking only of one ecosystem (Apple/Android).

These are some details I consider important, I won't extend too much to avoid being tiring. If you want to talk about code, just continue to the next topic.

---

</details>

<details>
<summary><b> 👨🏻‍💻 Let's talk about code</b></summary>

### Narrative code

> "Good code is code that tells a story linearly."

It must follow a narrative, showing step-by-step what is happening. Applications are built to solve problems, so the code should reflect that.

Programming is the last stage. First, the process is defined. Then comes planning and which tasks to execute, reducing the chance of failure.

> **"Process alignment is fundamental to the success of a project."**

`PROCESS` → `PLANNING` → `TASKS` → `PROGRAMMING` → `TESTS` → `DELIVERY`

When I'm working on a project, I need to think about how it will be executed, maintained, and evolved. The next developer who works on it should understand the code without difficulty and rely on documentation that clarifies technical decisions. The best professionals are those who **generate value for the business and people**.
<br>

```js
// ✅ Narrative Code
// Orchestrator at the top, details below (Step-down Rule), visual density, and expressive names.

// Simplified example. The code tells the story without needing comments.

await completeSale(123);

async function completeSale(orderId) {
  const orderDetails = findOrder(orderId);
  if (invalidOrder(orderDetails)) return;

  const invoiceIssued = issueInvoice(orderDetails);
  return invoiceIssued;
}

// Function details always below the main flow

function findOrder(orderId) {
  const orderDetails = database.findByCode(orderId);
  return orderDetails;
}

function invalidOrder(orderDetails) {
  if (orderDetails === null || orderDetails.items.length === 0) return true;

  if (orderDetails.customer.overdue) return notifyOverdue(orderDetails);

  return false;
}

function issueInvoice(orderDetails) {
  applyDiscounts(orderDetails);

  const invoice = saveOrder(orderDetails);
  return invoice;
}
```

The focus of the code above is not the application itself, but rather to demonstrate narrative code. In the next topic, I will talk about **anti-patterns** and **patterns** that I strive to apply in projects.

> 👨🏻‍💻 I've gathered my best code styling practices in a dedicated repository. If you'd like to check it out, visit [code-style](https://github.com/thiagocajadev/code-style)

---

</details>

<details>
<summary><b>⚠️ Anti-Patterns and Patterns</b></summary>

### Anti-Pattern: Spaghetti Code

I believe that no one knows or knows everything. We are human beings and this is a normal characteristic. However, one thing is certain: avoid what can cause problems.

```js
// ❌ Spaghetti version of the previous example, with code all mixed up and without concepts.

completeSale(123);

function completeSale(x) {
  let result;
  // bad names
  let p = findOrder(x);

  if (p != null) {
    if (p.items && p.items.length > 0) {
      if (!p.c.overdue) {
        // starts doing a bunch of things in the middle
        if (p.total > 100) {
          p.discount = 10;
        } else {
          p.discount = 0;
        }

        apply(p);

        function apply(p) {
          if (p.discount) {
            p.total = p.total - p.discount;
          }
        }

        let saved = saveOrder(p);

        if (saved) {
          result = saved;

          // random logic in the middle
          if (Math.random() > 0.5) {
            console.log("Random log");
          } else {
            console.warn("Another log");
          }
        } else {
          result = null;
        }
      } else {
        // more nested logic with function in the middle
        notify(orderDetails);
        result = false;

        // bad names and mixed language
        function notify(p) {
          console.log("overdue customer", p?.customer?.name);
          return true;
        }
      }
    } else {
      result = undefined;
    }
  } else {
    result = null;
  }

  // dead/confusing code
  if (false) {
    console.log("never executes");
  }

  return result;

  function save(p) {
    if (!p) return;
    if (p.total < 0) return null;
    return { ...p, saved: true };
  }
}
```

Well, there's no way to watch this torture. That's why it's good to avoid this kind of code as much as possible. I know that in times past we have all written bad code, but today with the knowledge available, it's possible to do better.

### 🚫 ANTI-PATTERNS

Key points:

1. Chaotic flow control
2. Mixed responsibilities
3. Lack of clear data and return contract

#### Naming and readability

- Names without meaning (`x`, `p`, `c`, `apply`)
- Mixed languages
- Lack of explicit intention in identifiers

#### Flow control

- Excessive nesting (`if` inside `if`)
- Lack of early return
- Scattered conditional logic that is hard to follow
- Use of `!=` (implicit coercion)

#### Return and contract

- Multiple return types (`null`, `undefined`, `false`, object)
- Lack of clear return contract
- Flow based on `null`/`undefined`

#### Structure and design

- Function with multiple responsibilities
- Business rules mixed with persistence and logging
- Functions declared inside others unnecessarily (`apply`, `notify`, `save`)
- Unused function (dead code)
- Unreachable code (`if (false)`)

#### State and mutability

- Shared mutable variable (`result`)
- Direct object mutation (`p.total`, `p.discount`)
- Strong structural coupling (`p.c.overdue`)

#### Side effects and unpredictability

- Side effects in the middle of logic (`console.log`, `console.warn`)
- Non-deterministic behavior (`Math.random()`)

---

Below are some more common anti-patterns in real projects:

#### Data modeling and contract

- Pure boolean (`true/false`) instead of structured Result
- Multiple return types (null / undefined / false / object)
- Inflated “MegaResult” with meta/status
- Empty fields in the envelope (`meta: {}`, `data: {}`)
- Mixing domain with transport (ex: Result + statusCode)
- `meta` as generic dump
- Return with anonymous object without clear contract

#### Incorrectly coupled UI / Frontend

- Direct fetch in the component
- Scattered API (without `apiClient`)
- Logic inside `useEffect`
- Data transformation inside the UI
- `try/catch` scattered in the UI
- Result in the UI state
- Complex inline return (direct JSX without composition)
- Multiple sources of truth in state

#### Code design

- Overly generic functions (`handle`, `process`, etc.)
- Functions with multiple responsibilities
- Heavy ViewModel / unnecessary layer
- Redundant Action (simple CRUD without value)
- Structure duplication between layers
- Cache coupled to the core
- Overengineering (abstraction without necessity)

#### Flow and control

- Exceptions as normal flow
- Chaotic conditional logic
- Lack of early return
- Dead / unreachable code

#### Consistency and clarity

- Names without intention
- Mixed languages
- Internal structures exposed (high coupling)
- Side effects mixed with business rules

---

### ✅ Patterns: Clean Code

Conventions, patterns, and principles are always better in the long run. If they were invented, it's because they make sense and solve real problems.

```js
// ✅ Narrative Code
// Orchestrator at the top, details below (Step-down Rule), visual density, and expressive names.

await completeSale(123);

async function completeSale(orderId) {
  const orderDetails = findOrder(orderId);
  if (invalidOrder(orderDetails)) return;

  const invoiceIssued = issueInvoice(orderDetails);
  return invoiceIssued;
}

function findOrder(orderId) {
  const orderDetails = database.findByCode(orderId);
  return orderDetails;
}

function invalidOrder(orderDetails) {
  if (orderDetails === null || orderDetails.items.length === 0) return true;
  if (orderDetails.customer.overdue) return notifyOverdue(orderDetails);

  return false;
}

function issueInvoice(orderDetails) {
  applyDiscounts(orderDetails);

  const invoice = saveOrder(orderDetails);
  return invoice;
}
```

Practically the same code, easier to understand and maintain. Following methodologies and "alphabet soup" like DDD, TDD, BDD, SOLID, SRP, SOLID, YAGNI, etc... is important, but it's not the main focus. The main focus is writing clean and legible code.

### ☑️ Patterns

Key points:

1. Simple and predictable flow
2. Separation of responsibilities
3. Clear and consistent contracts

#### Naming and readability

- Descriptive names with clear intention (`order`, `customer`, `calculateDiscount`)
- Consistency of language in the code
- Self-explanatory functions and variables

#### Flow control

- Use of early return to simplify reading
- Reduced nesting (flat code)
- Explicit and predictable conditions (`===`, `!==`)
- Linear and easy-to-follow flow

#### Return and contract

- Consistent return (always the same format)
- Use of well-defined Result/DTO
- Avoid `null`/`undefined` as flow control
- Explicit contracts between functions

#### Structure and design

- Functions with single responsibility (SRP)
- Clear separation of responsibilities (domain, persistence, side effects)
- Small, reusable, and testable functions
- Removal of dead code
- Function declaration at the appropriate level (outside when possible)

#### State and mutability

- Preference for immutability
- Avoid direct mutation of shared objects
- Variables with minimum scope and preferably `const`
- Access through clear interfaces (low coupling)

#### Side effects and unpredictability

- Isolated side effects (logs, IO, etc.)
- Pure functions whenever possible
- Deterministic behavior (no randomness in the core)

#### Data modeling and contract

- Structured and typed Result
- Consistent and predictable return
- Separation between domain and transport (ex: DTO ≠ HTTP)
- Clear contracts between layers
- Lean structures (no empty fields)
- Meaningful data (no generic `meta`)

#### Well-structured UI / Frontend

- Use of centralized `apiClient`
- Fetch outside the component (services/hooks)
- `useEffect` only for real effects (not business rules)
- UI focused on rendering
- Centralized error handling
- State with a single source of truth
- Small and composite components

#### Code design

- Specific functions named by intention
- Clear separation of layers
- Simplicity before abstraction
- Reuse without coupling
- Consistent structure between layers
- Cache decoupled from core

#### Flow and control

- Use of guard clauses (early return)
- Predictable and linear flow
- Explicit error handling
- Elimination of dead code

#### Consistency and clarity

- Defined naming pattern
- Cohesive and legible code
- Low coupling between structures
- Isolated and explicit side effects

That's it! Now with a broader perspective and a focus on project and people management, let's talk about governance in the next topic.

---

</details>

<details>
<summary><b>🏛️ Governance</b></summary>

### Technical Governance

Governing means having control over the project and ensuring its lifecycle. Tools like indicators and monitoring provide the basis for decision-making, directing the ideal actions at the right time.

If I have the vision that something has started to degrade and needs more resources, I can adjust it before there is an impact.

To have governance, we apply laws. The ones I consider fundamental and strive to apply:

<p align="left"><img src="https://img.shields.io/badge/%F0%9F%94%92_Hardening-Deny--by--Default-9c4a3f?style=for-the-badge" alt="Hardening - Deny-by-Default" /> <img src="https://img.shields.io/badge/%F0%9F%9A%A6_Resilience-Failure_as_Value-4a6b8c?style=for-the-badge" alt="Resilience - Failure as value" /> <img src="https://img.shields.io/badge/%F0%9F%8C%8A_The_Cascade-Narrative_Code-5b8c6a?style=for-the-badge" alt="The Cascade - Narrative Code" /> <img src="https://img.shields.io/badge/%F0%9F%92%8E_Visual_Excellence-Design_as_Code-6d5d83?style=for-the-badge" alt="Visual Excellence - Design as Code" /></p>

| Law                   | Strategic Commentary                                                 |
| :-------------------- | :------------------------------------------------------------------- |
| **Hardening**         | **Deep Security**: Data shielding and a _Deny-by-Default_ posture.   |
| **Resilience**        | **Failure Management**: Centralizes and standardizes error handling. |
| **The Cascade**       | **Narrative Code**: Code executes the process step-by-step linearly. |
| **Visual Excellence** | **Intuitive Design**: Beautiful and easy-to-use interfaces.          |

**Going deeper into philosophy, convictions, and standards (RFC/ISO) that underpin decision-making**: [Governance Details](GOVERNANCE-DETAILS.md)

With an understanding of governance, we move on to managing the **Software Development Life Cycle (SDLC)**.

### Software Development Life Cycle - SDLC

For healthy development, we need to distinguish between two moments:

**Project: The Birth**
It is an effort with a beginning, middle, and end. The focus is to transform an idea into a functional product. A good project is born foreseeing sustainability, avoiding that today's haste becomes tomorrow's technical debt and excessive cost.

**Process: Life Goes On**
It is a cyclic and permanent flow. While the project delivers the solution, the process ensures that the product continues to evolve and generate value. It is the routine that keeps the software updated, secure, and efficient for both the investor and the user.

Below I list 8 steps I consider fundamental for healthy development:

`FOUNDATION` → `SECURITY` → `CONTINUOUS INTEGRATION` → `ACCESS CONTROL` → `APP INTERFACE` → `DOMAIN` → `PRODUCTION` → `OPERATIONS`

**Explaining each step in detail**: [SDLC Trail Details](SDLC-DETAILS.md)

For each stage of this cycle, it is ideal to define a methodology as a guide. Below I talk about the choice of **Spec-Driven Development (SDD)**.

### Spec-Driven Development - SDD

> **"The specification drives the code, not the contrary."**

Now with a view of processes, there's nothing better than defining the work methodology. I see that the market is moving towards an **AI-Native** workflow. **SDD** - Spec-Driven Development, is a promising path for the Developer to act in partnership with AI Agents. Below are the main phases of this approach:

**5-Phase Pipeline**:
`SPECIFICATION` → `PLANNING` → `PROGRAMMING` → `TESTS` → `DELIVERY`

- **Explaining each phase and how to apply it**: [SDD Details](SDD-DETAILS.md)
- **An example of a Specification**: [Spec Example](SPEC-EXAMPLE.md)

Spec-Driven is a type of **Harnessing**, which uses specification concepts for AI-Native applications. A good developer follows the evolution of methodologies and additions. I always think about adding improvements to my workflow, multiplying them with other Devs.

---

</details>

<details>
<summary><b>💻 My Stack</b></summary>

### Backend & Core

![.NET](https://img.shields.io/badge/.NET-7e2bb3?style=for-the-badge&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-68217A?style=for-the-badge&logo=csharp&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Hono](https://img.shields.io/badge/Hono-E36002?style=for-the-badge&logo=hono&logoColor=white)
![Minimal APIs](https://img.shields.io/badge/Minimal_APIs-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Entity Framework](https://img.shields.io/badge/Entity_Framework-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Dapper](https://img.shields.io/badge/Dapper-4B32C3?style=for-the-badge&logo=dotnet&logoColor=white)

### Frontend & UI

![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Blazor](https://img.shields.io/badge/Blazor-5C2D91?style=for-the-badge&logo=blazor&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

### Database & Cloud

![Postgres](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

### Patterns & Quality

![Clean Code](https://img.shields.io/badge/Clean_Code-051937?style=for-the-badge&logo=readthedocs&logoColor=61DAFB)
![SOLID](https://img.shields.io/badge/SOLID-008793?style=for-the-badge&logo=codefactor&logoColor=white)
![TDD](https://img.shields.io/badge/TDD-E34F26?style=for-the-badge&logo=testinglibrary&logoColor=white)
![Result Pattern](https://img.shields.io/badge/Result_Pattern-e94560?style=for-the-badge&logo=codefactor&logoColor=white)
![DDD](https://img.shields.io/badge/DDD-f5a623?style=for-the-badge&logo=diagram&logoColor=black)

---

</details>

<details>
<summary><b>🤖 AIs & Tools</b></summary>

### Generative AI

[![AntiGravity](https://img.shields.io/badge/AntiGravity-000000?style=for-the-badge&logo=google&logoColor=white)](https://deepmind.google/technologies/gemini/)
[![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white)](https://anthropic.com/claude)
[![ChatGPT Plus](https://img.shields.io/badge/ChatGPT_Plus-10a37f?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/chatgpt)
[![DeepSeek](https://img.shields.io/badge/DeepSeek-000000?style=for-the-badge&logo=deepnote&logoColor=white)](https://www.deepseek.com/)

### Dev Tools & Terminal

[![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://code.visualstudio.com/)
[![JetBrains Rider](https://img.shields.io/badge/JetBrains_Rider-000000?style=for-the-badge&logo=jetbrains&logoColor=white)](https://www.jetbrains.com/rider/)
[![Starship](https://img.shields.io/badge/Starship-FF4081?style=for-the-badge&logo=starship&logoColor=white)](https://starship.rs/)
[![Docker Desktop](https://img.shields.io/badge/Docker_Desktop-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/products/docker-desktop/)

---

</details>

<details>
<summary><b>📚 Learning & Tips</b></summary>

### Continuous Learning

- [curso.dev](https://curso.dev) → JavaScript, Next.js, Postgres, React
- [balta.io](https://balta.io) → .NET Universe
- [Anthropic](https://www.anthropic.com/learn) → AI Courses

### Tips for your GitHub Profile

- [Profile Header](https://leviarista.github.io/github-profile-header-generator/)
- [Technology Shields](https://shields.io/)
- [Statistics and cards](https://github.com/anuraghazra/github-readme-stats)
- [Trophies & Games](https://profile-readme-generator.com/)

</details>

---

# 📫 Contact

<p align="left">
  <a href="mailto:contato@thiagocaja.dev"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0yMiA2YzAtMS4xLS45LTItMi0ySDRDMi45IDQgMiA0LjkgMiA2djEyYzAgMS4xLjkgMiAyIDJoMTZjMS4xIDAgMi0uOSAyLTJWNnptLTIgMC04IDUtOC01hDE2em0wIDEySDRWOGw4IDUgOC01djEweiIvPjwvc3ZnPg==&logoColor=white" alt="Email" /></a>
  <a href="https://linkedin.com/in/thiagocajadev"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0yMC40NDcgMjAuNDUySDE2Ljg5di01LjU2OWMwLTEuMzI4LS4wMjctMy4wMzktMS44NTItMy4wMzktMS44NTMgMC0yLjEzNiAxLjQ0NS0yLjEzNiAyLjkzOXY1LjY2OUgxMC4zNTRWOUgxMi4zNTRWMTBhLjA0OS4wNDkgMCAwIDAgLjA0OSAwYy40NzctLjkgMS42MzctMS44NTIgMy4zNy0xLjg1MiAzLjYwMSAwIDQuMjY4IDIuMzcgNC4yNjggNS40NTV2Ni4yODh6TTUuMzM3IDcuNDMzYy0xLjE0NCAwLTIuMDYzLS45MjYtMi4wNjMtMi4wNjUgMC0xLjEzOC45Mi0yLjA2MyAyLjA2My0yLjA2MyAxLjE0IDAgMi4wNjMuOTI1IDIuMDYzIDIuMDYzIDAgMS4xMzktLjkyMyAyLjA2NS0yLjA2MyAyLjA2NXpNNy4xMTkgMjAuNDUySDMuNTU0VjloMy41NjV2MTEuNDUyWiIvPjwvc3ZnPg==&logoColor=white" alt="LinkedIn" /></a>
</p>

# 📈 Stats

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

# 📌 Featured Projects

[![Code Style](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=code-style&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/code-style)
[![SDG Agents CLI](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=sdg-agents-cli&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/sdg-agents-cli)
[![Match Themes](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=match-themes&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/match-themes)
[![PayCheck BR](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=PayCheckBR&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/PayCheckBR)
[![Clone Tabnews](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=clone-tabnews&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/clone-tabnews)
[![Starship Bash](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=terminal-bash-one-dark-starship-profile&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/terminal-bash-one-dark-starship-profile)
[![Balta IO - BlazorIBGE](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=BlazorChallengeIBGEv2&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/BlazorChallengeIBGEv2)
[![Fleet MGMT](https://github-readme-stats-v1-thiagocajadev.vercel.app/api/pin/?username=thiagocajadev&repo=FleetMGMT&description_lines_count=2&hide_border=true&theme=discord_old_blurple&cache_seconds=604800)](https://github.com/thiagocajadev/FleetMGMT)
