# ⚡ PromptCraft for QA

**Turn rough work intent into expert-grade AI prompts — for QA & Test engineers.**

> 🔗 **Live app:** https://deepikasingh001.github.io/promptcraft-qa/

PromptCraft for QA is a login-free, zero-build web app that turns a short guided form
into a high-quality, structured prompt you can paste into ChatGPT, Claude, GitHub
Copilot, or Gemini. It's not a prompt library — it's a **guided prompt composer +
QA-workflow assistant + quality checker**.

Everything runs **100% locally in your browser**. No login, no server, no API key —
nothing you type ever leaves the page.

---

## Why

Most people still ask AI vague questions and get vague answers. QA work, however, maps
naturally to structured prompts (test cases, bug reports, automation, coverage, release
risk, regression, API testing). PromptCraft encodes that structure so you get
consistent, reusable, higher-quality output every time.

---

## Features

- **Guided builder** — pick your role, workflow, and inputs; get an expert prompt.
- **9 QA workflows:**
  - PRD / story → Test cases
  - PRD → Full test strategy & plan
  - API spec → API test suite
  - Automation script generation
  - Clean bug report
  - Risk-based regression plan
  - Release readiness / go–no-go
  - Test data generation
  - Defect RCA / root-cause analysis
- **6 generated outputs per run:**
  1. **Prompt** — Role · Goal · Context · Input · Instructions · Output format · Quality bar · Safety · Self-check
  2. **Why it works** — the reasoning behind each section
  3. **Follow-ups** — task-specific next prompts
  4. **Validation checklist** — auditable quality gates
  5. **Reusable template** — with `{{placeholders}}`
  6. **Quality score** — 0–100 across 7 rubric dimensions with improvement tips
- **Coverage contract** — functional, negative, boundary, security, performance,
  accessibility, regression, usability, integration, localization.
- **Adjustable depth** — quick / detailed / production-grade / interview-grade.
- **Output formats** — table, Gherkin/BDD, checklist, Jira tickets, Markdown, or code.
- **Safety guards** — no secrets, anonymize PII, company-safe mode.
- **One-click actions** — copy prompt, copy as Markdown, download `.txt`, or "Open in
  model" (copies the prompt and opens your chosen AI tool).
- **Accessible** — keyboard-navigable controls.

## Quality score

Every prompt is scored on seven dimensions:

| Dimension | Meaning |
|---|---|
| Role clarity | Is the AI's expert role defined? |
| Context | Is enough source material included? |
| Input clarity | Are the feature and artifacts clear? |
| Constraints | Are stack, rules, and coverage defined? |
| Output format | Is the final format specified? |
| Validation | Did we ask the AI to check assumptions/gaps? |
| Safety | Are secrets/PII handled? |

---

## Run it locally

No build step, no dependencies. Just open the file:

```bash
git clone https://github.com/DeepikaSingh001/promptcraft-qa.git
cd promptcraft-qa
open index.html      # macOS  (or double-click the file on any OS)
```

> **Note:** The "copy to clipboard" buttons need a secure context. They work from
> `file://`, `localhost`, and `https://`, but not from a plain `http://` host.

## Deploy

The app is a single static `index.html`, so it deploys anywhere. This repo is published
via **GitHub Pages** from the `main` branch root (`.nojekyll` is included so the site is
served as-is).

---

## Tech

- Single self-contained `index.html` (HTML + CSS + vanilla JS).
- Deterministic, template-based prompt composition — no external API calls.

## Roadmap

- Favorites / template library (localStorage) + last-form persistence
- "Improve my prompt" mode (paste an existing prompt → scored & rewritten)
- 👍/👎 feedback capture to validate prompt quality
- Second persona: Engineering / Engineering Leaders

## License

MIT
