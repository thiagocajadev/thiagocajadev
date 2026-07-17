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
<summary><b>💼 Get to know my work</b></summary>

### Portfolio projects

See how I build complete applications, applying **security and compliance checklists**:

- [Frontend Showcase](https://fs.thiagocaja.dev) → Modern, clean, and responsive screens, aiming for the best possible user experience.

- [Backend Showcase](https://bs.thiagocaja.dev) → Best practices in APIs, serving data securely to both frontend and mobile.

- [Meu time joga](https://meutimejoga.org) → AI Chat specialized in football, as well as data and statistics of clubs and national teams.

- [Spec-Driven Guide](https://specdrivenguide.org) → Guide to Development guided by specifications to work with AI.

- [Code Style](https://thiagocajadev.github.io/code-style) → My style of writing and maintaining code.

- [Thiago Cajá Developer](https://thiagocaja.dev) → Personal website, presenting my portfolio and blog.

---

</details>

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

### Anti-patterns: avoid known problems

**Anti-patterns** are solutions that look reasonable while you write them and create work later, when you read, change, or trust what's there. Many come from the solution and tooling limits of each era, and when the same problem reappears across different teams and languages, someone gives it a name.

Below is a spaghetti example, followed by the swaps I make to solve each point.

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

### 🚫 Anti-patterns in the example, by category

In the code above, to reach the discount rule you go down four levels of `if`. To know what the function returns, you trace the five assignments to `result`. The `save` function at the bottom is never called, and `Math.random()` swaps the log on each run. Below, each row links what's in this code to what I use instead.

#### Naming and readability

| In the code above                                           | What I use instead                                         |
| :---------------------------------------------------------- | :--------------------------------------------------------- |
| `x`, `p`, `c`: a single letter doesn't say what it holds     | `orderId`, `orderDetails`: the name carries the intent      |
| `apply`, `notify`, `save`: verbs too vague to say what they touch | A verb that names the action: `applyDiscounts`, `notifyOverdue` |
| The name doesn't explain, so a comment above has to          | An expressive name, and the comment loses its purpose      |

#### Flow control

| In the code above                                           | What I use instead                                         |
| :---------------------------------------------------------- | :--------------------------------------------------------- |
| Three nested `if`s hide the rule at the fourth level         | A guard clause at the entry, with success on the first level |
| `p != null` compares with coercion, treating `null` and `undefined` as equal | `order?.items ?? []` normalizes the missing case, no fragile `null` comparison |
| The sale decision split across distant blocks                | One guard per decision, in the order they happen           |

#### Return and contract

| In the code above                                           | What I use instead                                         |
| :---------------------------------------------------------- | :--------------------------------------------------------- |
| Returns `null`, `undefined`, `false`, or an object, depending on the path | One format, the same across every path                     |
| The caller tests null step by step to deduce what happened   | A `Result` with `status` and `reason` answers it           |
| `false` doesn't tell why the sale didn't go through          | The reason travels with the outcome: `CUSTOMER_OVERDUE`    |

#### Structure and design

| In the code above                                           | What I use instead                                         |
| :---------------------------------------------------------- | :--------------------------------------------------------- |
| One function finds, validates, computes discount, saves, and logs | One responsibility per function, one abstraction level at a time |
| Rule, persistence, and log in the same block                 | Domain separated from saving and from the side effect      |
| `apply`, `notify`, `save` loose in the middle of the flow    | Helpers right below their caller, in call order            |
| `save` with no caller and `if (false)` unreachable           | I delete it in the commit where I find it. Git keeps the history. |

#### State and mutability

| In the code above                                           | What I use instead                                         |
| :---------------------------------------------------------- | :--------------------------------------------------------- |
| `let result` reassigned at five points                       | `const` by default: one value, assigned once               |
| `p.total` and `p.discount` changed on a `p` that came from outside | The function returns the discounted order, without touching the original |
| `p.c.overdue`: to know what `c` is, I open `findOrder`       | `orderDetails.customer.overdue` reads without leaving the file |

#### Side effects and predictability

| In the code above                                           | What I use instead                                         |
| :---------------------------------------------------------- | :--------------------------------------------------------- |
| `console.log` and `console.warn` in the middle of the calculation | An effect with its own name and place: `notifyOverdue`     |
| `Math.random()` decides the log: same sale, different outputs | A deterministic rule: same input, same output              |
| Testing requires running what the function saves and prints  | Calculation isolated from the effect, and the test calls only the calculation |

### 🚫 Other common anti-patterns

Outside spaghetti, these show up often. Each one, alone, looks harmless, and that's why they pass review.

#### Data modeling and contract

| The bad pattern                                             | What I use instead                                         |
| :---------------------------------------------------------- | :--------------------------------------------------------- |
| `true`/`false` as the answer to a business operation         | A structured `Result`: the outcome plus the reason         |
| Different return types in the same function                  | One format                                                 |
| Result object with empty fields to keep the shape (`meta: {}`, `data: {}`) | Only the fields that outcome fills                         |
| `Result` carrying an HTTP `statusCode`                       | The rule returns the outcome, and the edge translates it into an HTTP status |
| Anonymous object return, built differently on each call      | One named format, the same in all                          |

#### UI doing what isn't its job

| The bad pattern                                             | What I use instead                                         |
| :---------------------------------------------------------- | :--------------------------------------------------------- |
| `fetch` written inside the component                         | The call lives in an `apiClient`, the single point that talks to the server |
| API calls scattered, each with its own config                | One `apiClient`, with base URL, headers, and error handling |
| Business rule inside `useEffect`                             | The rule stays on the server or in its own module. The component displays. |
| Raw data reaching the screen and being transformed there     | The data arrives in the shape the screen draws             |
| `try/catch` repeated on every screen                         | Error handled at the edge, once                            |
| Several sources of truth for the same data in state          | One source of truth, and the rest derives from it          |

#### Code design

| The bad pattern                                             | What I use instead                                         |
| :---------------------------------------------------------- | :--------------------------------------------------------- |
| Generic names: `handle`, `process`, `manage`                 | A verb that says what the function does: `calculateTotal`, `issueInvoice` |
| A function with more than one clear responsibility           | One responsibility per function, and the name fits without an "and" in it |
| The same structure duplicated across layers                  | Rule of three: extract on the third occurrence, not the first |
| Cache mixed with the business rule                           | Cache at the edge, around the rule. The rule is written without naming the cache. |
| Abstraction built for a case that doesn't exist yet          | Write it when the second case arrives                      |

#### Flow and control

| The bad pattern                                             | What I use instead                                         |
| :---------------------------------------------------------- | :--------------------------------------------------------- |
| Exception as normal flow, for example throwing to signal "not found" | Explicit `null` or `Result`. Exception stays for a real error. |
| Nesting where a guard clause would fit                       | A guard clause at the entry                                |
| Dead code and unreachable branches                           | Delete it                                                  |

---

### ✅ The same code, rewritten

The choices are the ones in the right column: orchestrator at the top, small helpers extracted right below in call order (Step-down Rule), visual density, and names that state the intent.

```js
// ✅ Narrative code
// Orchestrator at the top, helpers extracted below in call order
// (Step-down Rule), visual density, and expressive names.

const SALE_APPROVED = "APPROVED";
const SALE_REJECTED = "REJECTED";

const sale = await completeSale(123);

async function completeSale(orderId) {
  const orderDetails = await findOrder(orderId);

  if (!hasBillableItems(orderDetails)) {
    const saleWithoutItems = rejectSale("ORDER_WITHOUT_ITEMS");
    return saleWithoutItems;
  }

  if (orderDetails.customer.overdue) {
    notifyOverdue(orderDetails);

    const blockedSale = rejectSale("CUSTOMER_OVERDUE");
    return blockedSale;
  }

  const invoice = await issueInvoice(orderDetails);
  const completedSale = approveSale(invoice);
  return completedSale;
}

async function findOrder(orderId) {
  const orderDetails = await database.findByCode(orderId);
  return orderDetails;
}

function hasBillableItems(order) {
  const items = order?.items ?? [];
  const hasAnyItem = items.length > 0;

  return hasAnyItem;
}

function rejectSale(reason) {
  const sale = { status: SALE_REJECTED, reason, invoice: null };
  return sale;
}

async function issueInvoice(order) {
  const discountedOrder = applyDiscounts(order);
  const invoice = await saveOrder(discountedOrder);

  return invoice;
}

function approveSale(invoice) {
  const sale = { status: SALE_APPROVED, reason: null, invoice };
  return sale;
}
```

The main flow is four steps, read top to bottom: find the order, reject if it has no item, reject if the customer is overdue, invoice. Each `return` has a named `const` right above it, so the name says which of the three outcomes it is.

The negation in the `if` inverts the logic on purpose. `hasBillableItems` is named in the positive (it asks whether the order has an item), and the check uses `if (!hasBillableItems(...))`: if it has none, reject and leave. Handling the invalid case first and returning there keeps the success path unindented, at the base level. It's a common guard pattern, and the line reads like a sentence: if the order has no billable items, reject the sale.

The contract is now a single one. In all three paths, the function returns an object with `status`, `reason`, and `invoice`. The caller reads `sale.status` and knows what happened, and on rejection the `reason` says which rule blocked the sale. The helpers sit right below the orchestrator, at module level and in call order. Extracted this way, each one grows and gets its own test as the flow expands. `applyDiscounts` returns the order with the discount applied instead of changing what it received, so no function changes an object that came from outside.

`async` stays only on the functions that wait on I/O (data access outside the program, like a database or disk). `findOrder` reads the database and `issueInvoice` saves the invoice; both return a promise, so the orchestrator `await`s them. The ones that only compute in memory (`hasBillableItems`, `rejectSale`, `approveSale`) stay synchronous. Marking everything `async` out of habit erases the cue for which functions wait.

Following alphabet soup like DDD, TDD, SOLID, and YAGNI helps, but it's not the starting point. The starting point is writing code the next person can read. The acronyms give proper names to habits you'll already be practicing by the time you reach them.

> 👨🏻‍💻 The full walkthrough, with the concepts and the step by step, is in [Anti-Patterns: avoid known problems](https://thiagocaja.dev/blog/anti-patterns-evite-problemas-conhecidos/).

That's it! Now with a broader perspective and a focus on project and people management, let's talk about governance in the next topic.

---

</details>

<details>
<summary><b>🏛️ Governance</b></summary>

### Technical Governance

Governing means having control over the project and ensuring its lifecycle. Tools like indicators and monitoring provide the basis for decision-making, directing the ideal actions at the right time.

If I have the vision that something has started to degrade and needs more resources, I can adjust it before there is an impact.

To have governance, we apply laws. The ones I consider fundamental and strive to apply:

<p align="left"><img src="https://img.shields.io/badge/%F0%9F%94%92_Hardening-Deny--by--Default-9c4a3f?style=for-the-badge" alt="Hardening - Deny-by-Default" /> <img src="https://img.shields.io/badge/%F0%9F%9A%A6_Resilience-Failure_as_Value-4a6b8c?style=for-the-badge" alt="Resilience - Failure as value" /> <img src="https://img.shields.io/badge/%F0%9F%93%96_Narrative-Documentative_Code-5b8c6a?style=for-the-badge" alt="Narrative - Documentative Code" /> <img src="https://img.shields.io/badge/%F0%9F%92%8E_Visual_Excellence-Design_as_Code-6d5d83?style=for-the-badge" alt="Visual Excellence - Design as Code" /></p>

| Law                   | Strategic Commentary                                                 |
| :-------------------- | :------------------------------------------------------------------- |
| **Hardening**         | **Deep Security**: Data shielding and a _Deny-by-Default_ posture.   |
| **Resilience**        | **Failure Management**: Centralizes and standardizes error handling. |
| **Narrative**         | **Documentative Code**: Code executes the process step-by-step, linearly. |
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

### Content Recommendations

#### Educational

- [Filipe Deschamps](https://www.youtube.com/@FilipeDeschamps) → Teaches JS and web dev with cinematic narrative and impeccable didactics
- [Andre Balta](https://www.youtube.com/@baltaio) → Reference for .NET, C# and LLM integration
- [CFTV](https://www.youtube.com/@codigofontetv) → Gabriel Fróes and Vanessa Weber cover tech news and concepts in an accessible way
- [Renato Augusto](https://www.youtube.com/@RenatoAugustoTech) → Reference for System Architecture

#### UI/UX Design Thinking

- [Ryan Dutra](https://www.youtube.com/designfromhuman) → Philosophy, psychology and decision-making applied to design
- [Maiane Gabriele](https://www.youtube.com/@maianegabrielle) → Free Figma courses, UI/UX reviews and design error analysis in practice
- [Andrey Knabbenn](https://www.youtube.com/@andreyknabbenn) → Practical UI/UX, Figma and product design tutorials
- [Kole Jain](https://www.youtube.com/@KoleJain) → Advanced UI/UX and web design tips focused on SaaS and freelancing

#### Raw & Unfiltered

- [Fábio Akita](https://www.youtube.com/@Akitando) → Proves points A to Z, straight and unfiltered
- [Mano Deyvin](https://www.youtube.com/@manodeyvin) → Tips, acid commentary and the day-to-day of programming
- [Lucas Montano](https://www.youtube.com/@lucasmontano) → Covers current programming topics with a roots-first mindset

#### Artificial Intelligence & LLM

- [Igor Oliveira](https://www.youtube.com/channel/UCVttJS9LLVAN6cdApvXJnZQ) → Tests and compares AI models: local, open source and project-integrated
- [Pasquadev](https://www.youtube.com/@pasquadev) → Spec-driven development (SDD) and AI agents in real-world workflows
- [Deborah Folloni](https://www.youtube.com/@deborahfolloni) → Building products with AI by a founder with an exit, including responsible vibe coding

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
