# My Development Pipeline (8 Steps)

This guide documents how I organize a software project from its inception to continuous operation. It's not a rigid formula, it's the pattern that helps me remember what truly matters.

The order follows a logic. Each step creates the foundation for the next to function securely. However, every project has its context: a CLI tool might not need access control, while a SaaS needs the full pipeline. Use what makes sense, in the order that makes sense.

`FOUNDATION` → `SECURITY` → `CONTINUOUS INTEGRATION` → `ACCESS CONTROL` → `APP INTERFACE` → `DOMAIN` → `PRODUCTION` → `OPERATIONS`

> Note: The order may vary depending on the type of project, scope, and team division. The important thing is to have clarity on each stage and ensure that all are executed.

---

## 01 — Foundation

Before any business code, the project needs a structure that any developer—including myself six months from now—can understand and run without having to ask anything.

- `.editorconfig` and linter configured. No "it works on my machine" excuses.
- `README.md` with real setup instructions—not the showcase version, the functional one.
- Hardened `.gitignore`: `.env*`, build artifacts, IDE folders. No secrets enter the history.
- Environment variables centralized in `.env` with validation at startup.
- `/health` route from the very first commit. If it doesn't boot cleanly, I already know where to look.
- Entry file (`Program.cs`, `main.ts`, or equivalent) as an orchestrator—it shows the flow, it doesn't implement details.
- Setup scripts that run with a single command (`npm run dev`, `dev.sh`). This reduces friction and standardizes the workflow.

**Done when:** Anyone on the team can clone, configure, and run the project in less than 5 minutes.

---

## 02 — Observability and Security

Security is not a feature. It is the layer that protects everything that comes after.

This phase exists because I've seen projects break in production without leaving a trace. Logs without context are useless. Requests without IDs are a diagnostic nightmare.

- Validation of all external inputs at the boundary (body, query params, headers). Invalid data is rejected before entering the system.
- Structured JSON logs with request ID, timestamp, and severity. Never log secrets or personal data.
- `/health` route validating connectivity with dependencies (database, cache, external services).
- Security headers: HSTS, CSP, rate limiting. Protection before it's needed, not after.
- If applicable: distributed tracing (OpenTelemetry) to follow a request between services.

**Done when:** I can answer "is the application healthy?" and "what happened to request X?" without opening the code.

---

## 03 — CI/CD Pipeline (Continuous Integration)

Delivering code safely is not luck. It is well-configured automation.

The objective is simple: broken code does not reach production. Human review is for business logic, not for verifying if the build passes.

- Defined environments: local, staging, production. Documented differences between them.
- Secrets managed in the right place (CI secrets, vault). Nothing hardcoded.
- CI active on every PR: linter + tests + build. PR blocked if any gate fails.
- CD defined: how the code goes from PR to staging and then to production. Automated staging, production with approval when necessary.

**Done when:** A PR cannot be merged without passing all gates. Deployment to staging is a single action.

---

## 04 — Access Control (When applicable)

Authentication and authorization define who sees what. This isn't an implementation detail—it's an architectural decision that affects everything that follows.

Before building any feature that depends on permissions, I need to know: who can do what and why.

- Identity strategy defined for the context: Magic Link for low friction, OAuth for B2B, passkeys for critical security.
- Roles and permissions modeled from the beginning. Start simple (admin/user) and expand when necessary. Default: deny by default.
- Secure tokens: HttpOnly cookies for web, short-lived JWTs with refresh rotation. Protection against XSS and CSRF.
- User CRUD as the first real feature—the one that exercises the full pipeline from end to end.

**Done when:** I can create a user, authenticate, access a protected route, and be rejected on a route without permission.

---

## 05 — Design System and Interface (When applicable)

An inconsistent interface sends a clear message to the user: nobody reviewed this carefully.

A Design System is not just frontend "fluff", it's what prevents every developer from inventing a different button.

- Design tokens defined: colors, spacing (4/8px system), typography, borders.
- Light and dark themes. CSS variables or a utility system (e.g., Tailwind).
- Guaranteed WCAG contrast. Accessibility is not optional, it's respect for the user.
- Base components (Button, Input, Card, Modal) built before specific screens.

**Done when:** A new screen can be built with existing tokens and components, without ad-hoc styling.

---

## 06 — Feature Evolution (Domain)

This is where the real business code comes in. And it's where most projects accumulate technical debt when there is no discipline.

No complex logic is coded without a prior specification that validates the business rules. The code follows the spec, not the contrary.

- Domain modeling first: entities, value objects, aggregates. Names in business language, not technical jargon.
- Use cases as orchestrators: they call validators, domain logic, and repositories. No implementation details mixed in.
- Feature flags for anything risky or incomplete. Deploy to production disabled, validate, then enable.
- Continuous refactoring: if a module has grown beyond its responsibility, split it now. There is no such thing as a "refactoring sprint" that fixes it later.

**Done when:** Each feature is isolated, testable, and can be rolled back or disabled independently.

---

## 07 — Production Readiness

Before going live, there is a checklist that must be verified. Always.

Deploying on a Friday night without a rollback plan is not bravery, it's recklessness.

- Pre-deploy checklist: environment variables configured, secrets rotated, dependencies updated, debug flags removed.
- Migrations tested in staging with a documented rollback plan. Data integrity validated.
- Smoke tests in staging: main flow, error flows, edge cases.
- Defined deployment strategy: blue/green, canary, or rolling. Rollback planned for under 5 minutes.

**Done when:** Production is live, monitored, and there is a documented way to roll back in less than 5 minutes.

---

## 08 — Operational Governance

The system has gone to production. Now begins the part that lasts forever.

Monitoring is not optional, it's what differentiates a professional system from one where "we find out when it goes down."

- Active monitoring in the first 24-48 hours after deployment: error rate, latency, resource usage.
- Incident protocol defined: who is notified, how triage is done, where to communicate.
- For critical issues: fast fix if small, rollback if large. The decision must be documented.
- CHANGELOG updated with what changed and why. Facilitates audits and communication with stakeholders.
- Post-mortems focused on the system, never on blaming people. What happened, why it happened, what changes.

**Done when:** The team responds to a production issue without panic. Each incident makes the system more robust.

---

_Signed by: Thiago Cajaíba - Developer_
