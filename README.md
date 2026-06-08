[README.md](https://github.com/user-attachments/files/28726045/README.md)
# Interactive SQL Practice Lab

A self-contained, browser-based SQL practice environment for analyst interview prep. Three role-specific schemas, 90 problems, real-time answer checking — no server, no install, no signup.

🔗 **[Open the live demo →](https://chreyes1986.github.io/SQLite-Practice-module/)**

---

## What it is

A single HTML file you can open in any modern browser to practice SQL. It boots a SQLite database (compiled to WebAssembly) entirely client-side and lets you write queries against three realistic analyst schemas — flipping between them with a dropdown.

Problems mirror questions that actually come up in analyst interviews: no-show rates, cohort revenue analysis, ROI by channel, days-to-payment, lifetime value, ranking within partitions, time-between-events using `LAG`, and so on.

## Three roles, 90 problems

| Role | Tables | Problems |
|---|---|---|
| **Clinical Operations** | departments, providers, patients, appointments, encounters, diagnoses, procedures, insurance | 30 |
| **Financial Analysis** | departments, customers, products, orders, invoices, payments, expenses | 30 |
| **Marketing Analytics** | channels, campaigns, leads, customers, ad spend, conversions, email sends | 30 |

Each role has 10 problems per difficulty:

- **Beginner** — `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`, `DISTINCT`
- **Intermediate** — `JOIN`s, `GROUP BY`, aggregation, `HAVING`, conditional aggregation
- **Advanced** — window functions (`RANK`, `LAG`, `NTILE`), CTEs, self-joins, date math, Pareto and cohort analysis

## Features

- **Check Answer.** Runs your query and the reference solution against the same database, then compares results with smart row/column matching and a numeric tolerance.
- **Refresh data.** Regenerates the database with a new random seed — same questions, different numbers. Useful once you've memorized a query and want to confirm you actually understand the logic.
- **Progress tracking.** ✓ green = completed, ✓ yellow = attempted but not yet correct. Persists across reloads via `localStorage`.
- **Quick-load dropdown.** Jump to any problem directly from the editor toolbar.
- **Light / dark theme.** Toggle in the header. Defaults to a JetBrains/DataGrip-inspired dark; light mode is a warm off-white.
- **Schema reference.** Sidebar lists every table; click to expand columns and sample rows.
- **Reset progress.** Optional, from the About tab.

## Tech stack

- **HTML / CSS / vanilla JavaScript** — single file, no build step, no `npm install`
- **[sql.js](https://github.com/sql-js/sql.js)** — SQLite compiled to WebAssembly, runs entirely in the browser
- **[CodeMirror](https://codemirror.net/)** — SQL editor with syntax highlighting and keyboard shortcuts

## Built with Claude

This tool was built end-to-end with **[Claude](https://www.anthropic.com/claude)** (Anthropic's AI assistant) — iteratively, in conversation, across multiple sessions. Each feature was spec'd, scaffolded, tested, and refined. The whole thing is deliberately a single HTML file so it can be read top to bottom as a worked example of composing a non-trivial application alongside AI.

The interesting craft isn't *that* AI wrote code — it's how the work was broken down: defining clear sub-goals, validating each output (every one of the 90 SQL solutions was executed against generated data to confirm it actually returns the right rows), and directing the next iteration. That's the skill the project is meant to demonstrate, alongside the SQL itself.

## Run it locally

```bash
git clone https://github.com/Chreyes1986/SQLite-Practice-module.git
cd SQLite-Practice-module
open index.html   # or just double-click the file in your file manager
```

That's it. No server, no setup.

---

**Built by [Christian Reyes](https://github.com/Chreyes1986)** — Data Analyst · St. Cloud, FL  
[LinkedIn](https://www.linkedin.com/in/christian-reyes-7a7025370/) · [Portfolio](https://github.com/Chreyes1986)
