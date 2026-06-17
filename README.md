# RunDrill Strategic Management

> **© 2026 Mikhail Podgurskiy / RunDrill — proprietary, all rights reserved.** No use, copying, or distribution without written permission. Licensing & contact: mikhail@viewflow.io

A **strategic-management assistant** for business owners — not a course, an assistant. It runs a proven
**16-step strategy process** *for* you, one step at a time, so you never juggle a pile of prompts or
lose the thread. It runs inside your AI agent (Claude, Codex, Gemini/Antigravity) and is backed by the
[RunDrill](https://rundrill.com) MCP engine, which holds your place in the process.

## What it does

It interviews you for your **company context**, then walks the process step by step — at each step it
does the work (running web research inline where needed), gives you a short summary, saves the full
**artifact as a Word document (.docx)** in your project folder (Markdown fallback only if the host
can't produce Word), and waits for you to review and correct it before moving on. Your strategy is
assembled only from artifacts you've **verified**.

The 16 steps:

1. **Company context** — a master profile of your business (the source of truth for every later step)
2. **Diagnostics** — strategy audit · competitor recon · VRIO resource analysis
3. **Research** (optional) — quantitative industry baseline · foresight: drivers & key uncertainties
4. **Choice** — market & customer-pain research · business model (as-is/to-be) · customer-development
   plan · strategy options
5. **Cascade** — Balanced-Scorecard strategy map · KPI or OKR
6. **Plan** — Hoshin X-matrix · initiative decomposition into projects
7. **Rhythm** — a 12-month management-review calendar · KPI benchmark (optional)

Talks to you in **Russian**.

> Based on the UIB "Стратегический менеджмент для бизнеса" module (2026), Игорь Палкин.

## Install

This repo is its own marketplace — the catalog lives alongside the plugin.

**Claude Code / Desktop**
```
/plugin marketplace add kmmbvnr/strategic-management
/plugin install rundrill-strategic-management@strategic-management
/reload-plugins        # → /strategy-assistant is live
```

**Codex**
```
codex plugin marketplace add kmmbvnr/strategic-management
codex plugin install rundrill-strategic-management
```

**Google Antigravity** — drop this folder into `~/.gemini/config/plugins/` (or a workspace
`.agents/plugins/`).

On first use the assistant asks you to **authorize** the RunDrill MCP server once (a browser sign-in);
after that your place in the process is remembered across sessions.

## How it works

The assistant is the voice; the MCP server is the source of truth. Three tools drive the pipeline:
`status` (where you are), `next` (the current step's prompt + run-it contract), and `record` (save the
company context, mark a step verified, skip an optional step, revise an earlier one). The server is
served at `https://mcp.rundrill.com/strat/strategic-management`.

## License

Proprietary — all rights reserved. See [LICENSE](./LICENSE). No use without written permission.
