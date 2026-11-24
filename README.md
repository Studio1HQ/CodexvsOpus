<div align="center">

<img src="https://raw.githubusercontent.com/Studio1HQ/Studio1HQ/main/assets/banners/CodexvsOpus.webp" alt="Codex 5.3 vs Claude Opus 4.6: Two coding models given the same dashboard and log analysis tasks" width="100%" />

<br />
<br />

# Codex 5.3 vs Claude Opus 4.6

### Two coding models given the same dashboard and log analysis tasks

Side-by-side output from GPT 5.3 Codex and Claude Opus 4.6: a SaaS dashboard built by each, plus an application log analysis report, scripts and charts produced by Opus.

<br />

[![Built by Studio1](https://img.shields.io/badge/Built_by_Studio1-f97316?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNjAgMTYwIiBmaWxsPSJub25lIj48cGF0aCBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTAgMzVDMCAxNi42ODA3IDE0LjA3NDQgMS42NDg0NCAzMiAwLjEyNjk1M1YxNDFINTEuMDUyM0M1Mi40MzA4IDEzNy4zNDQgNTQuNzQ0NiAxMzMuNjg5IDU3Ljk5MzggMTMwLjAzM0M2MS4xNDQ2IDEyNi41MDggNjQuNjg5MiAxMjMuNDQgNjguNjI3NyAxMjAuODI5QzcyLjU2NjIgMTE4LjM0OSA3Ni4zNTY5IDExNi43ODIgODAgMTE2LjEyOVY4Ni43NTQ0Qzc1LjQ3MDggODcuOTI5MiA3MS4zODQ2IDg5LjY5MTkgNjcuNzQxNSA5Mi4wNDE1QzY0IDk0LjUyMjUgNjAuNzUwOCA5Ny40NiA1Ny45OTM4IDEwMC44NTRDNTYuNTM0NSAxMDIuNzIgNTUuMjU0NSAxMDQuNjU5IDU0LjE1MzkgMTA2LjY3MVYwSDEyNUMxNDQuMzMgMCAxNjAgMTUuNjY5OSAxNjAgMzVWMTI1QzE2MCAxNDQuMzMgMTQ0LjMzIDE2MCAxMjUgMTYwSDEyNFYxOEgxMDQuOTQ4QzEwMy41NjkgMjEuNjgxNiAxMDEuMjU1IDI1LjM2MjggOTguMDA2MiAyOS4wNDQ0Qzk0Ljg1NTQgMzIuNTk0MiA5MS4zMTA4IDM1LjY4NDEgODcuMzcyMyAzOC4zMTRDODMuNDMzOCA0MC44MTIgNzkuNjQzMSA0Mi4zODk2IDc2IDQzLjA0NzRWNzIuNjMwNEM4MC41MjkyIDcxLjQ0NzMgODQuNjE1NCA2OS42NzI0IDg4LjI1ODUgNjcuMzA1N0M5MiA2NC44MDc2IDk1LjI0OTIgNjEuODQ5MSA5OC4wMDYyIDU4LjQzMDdDOTkuNDY1NSA1Ni41NTEzIDEwMC43NDUgNTQuNTk4NiAxMDEuODQ2IDUyLjU3MjNWMTYwSDM1QzE1LjY3IDE2MCAwIDE0NC4zMyAwIDEyNVYzNVoiIGZpbGw9IiNmZmZmZmYiLz48L3N2Zz4K)](https://studio1hq.com)

[More examples](https://github.com/Studio1HQ) &nbsp;·&nbsp; [studio1hq.com](https://studio1hq.com)

</div>

<br />

## Overview

This repo compares the output of GPT 5.3 Codex and Claude Opus 4.6 on coding tasks. Both models built a SaaS dashboard, and Opus 4.6 also analyzed a sample application log file and produced a report and charts. Everything is kept as the models produced it, so you can run the demos and read the reports yourself.

The prompts are not stored in the repo. The tasks below are described from the output.

## Features

- **GPT 5.3 Codex dashboard**: a plain HTML, CSS and JavaScript "Northstar SaaS" dashboard with a sidebar and four metric cards (monthly revenue, active users, churn rate, open tickets).
- **Opus 4.6 dashboard**: a React and TypeScript dashboard built with Vite, with `Sidebar`, `Header` and `MetricCard` components and sample metrics such as revenue, active users and orders.
- **Log analysis scripts**: `analyze_logs.py` loads `sample_application_logs.xlsx` with pandas and computes statistics. `create_visualizations.py` renders charts with matplotlib and seaborn.
- **Written reports**: `ANALYSIS_SUMMARY.md`, `Application_Logs_Analysis_Report.md` and `KEY_METRICS_TABLE.txt` summarize the results, for example the error rate, response times and error rate by request type.

## Tech stack

| Layer | Tool |
| --- | --- |
| Models compared | GPT 5.3 Codex, Claude Opus 4.6 |
| Codex demo | HTML, CSS, JavaScript (ES modules) |
| Opus demo | [React](https://react.dev) 19, TypeScript, [Vite](https://vite.dev) |
| Log analysis | Python, [pandas](https://pandas.pydata.org), matplotlib, seaborn |

## Getting started

### Prerequisites

- Node.js 18 or later for the Opus dashboard
- Python 3 with pandas, openpyxl, matplotlib and seaborn for the log analysis scripts
- Any static file server for the Codex dashboard (it loads `src/main.js` as a module)

### Installation

```bash
git clone https://github.com/Studio1HQ/CodexvsOpus.git
cd CodexvsOpus
```

### Run

Opus 4.6 dashboard:

```bash
cd "Opus 4.6 Demo"
npm install
npm run dev
```

The other scripts are `npm run build`, `npm run lint` and `npm run preview`.

GPT 5.3 Codex dashboard: serve the `GPT 5.3 Codex Demo` folder with a static server, for example `npx serve "GPT 5.3 Codex Demo"`, and open it in the browser.

Log analysis: the scripts read `sample_application_logs.xlsx` from the working directory, so copy it next to the scripts or run them from the repo root.

```bash
pip install pandas openpyxl matplotlib seaborn
python "Opus 4.6 Data/analyze_logs.py"
python "Opus 4.6 Data/create_visualizations.py"
```

## How it works

```text
GPT 5.3 Codex Demo/   index.html, styles.css, src/main.js
Opus 4.6 Demo/        Vite React app (src/components: Header, Sidebar, MetricCard)
Opus 4.6 Data/        analyze_logs.py, create_visualizations.py, reports
sample_application_logs.xlsx   Input data, 50 requests over 3 days
```

The sample log file has 50 requests between February 1 and 3, 2026. Opus's summary reports a 50% error rate, an average response time of about 1,107 ms and the highest error rates on `GET /reports`, `GET /login` and `POST /order`.

## Resources

- [Claude Code](https://claude.com/claude-code): Anthropic's coding agent, for working with Claude models in the terminal.

<br />

---

<div align="center">

<a href="https://studio1hq.com">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Studio1HQ/website/main/brand/studio1-logo-on-dark.svg" />
    <img src="https://raw.githubusercontent.com/Studio1HQ/website/main/brand/studio1-logo-on-light.svg" alt="Studio1" width="160" />
  </picture>
</a>

Built by **[Studio1](https://studio1hq.com)**, the technical content and DevRel partner for devtool teams.<br />
Browse more open-source examples at [github.com/Studio1HQ](https://github.com/Studio1HQ).

[![Website](https://img.shields.io/badge/studio1hq.com-0b0807?style=for-the-badge&logo=googlechrome&logoColor=white)](https://studio1hq.com)
[![Book a call](https://img.shields.io/badge/Book_a_strategy_call-f97316?style=for-the-badge&logo=googlecalendar&logoColor=white)](https://cal.com/studio1/collab)
[![X](https://img.shields.io/badge/%40Studio1HQ-141414?style=for-the-badge&logo=x&logoColor=white)](https://x.com/Studio1HQ)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/company/studio1hq/)

<sub><a href="https://studio1hq.com">studio1hq.com</a> · Technical content, docs, video and DevRel for devtools</sub>

</div>
