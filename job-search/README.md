# 🎯 Autonomous Executive Job-Search Engine — Nitin Sekhar

A self-running system that finds, scores, tailors, and stages applications for senior roles
(CISO / fractional vCISO / COO) across remote + Dallas-hybrid + light-travel, at a $300K+ floor.

## Start here
| File | What it is |
|---|---|
| **`00-SUPER-PROMPT.md`** | ⭐ The master prompt — paste it to run the whole engine. Plus the full menu of everything buildable. |
| `01-profile.md` | Your targeting config (grounded in your real Oracle/Cerner/Siemens history). |
| `02-opportunity-report.md` | Latest run's findings + the executive channels where your pipeline lives. |
| `04-cover-letter-templates.md` | Auto-fill cover letters + LinkedIn outreach, one per lane. |
| `05-automation.md` | How the daily cron runs and your 2-min/day routine. |
| `06-auto-apply-setup.md` | Two paths to automate *submission* (Playwright MCP ⭐ vs. mass auto-apply services). |
| `applications/apply-queue.csv` | The work list a browser-automation agent submits, top to bottom. |
| `playwright-mcp.config.sample.json` | Copy-paste MCP config to enable automated form submission. |
| `resume-variants/` | 3 ATS-tuned positionings: Security exec / Fractional / Operating exec. |
| `applications/tracker.csv` | System of record: every role, score, status, apply link. |

## What's live right now
- ✅ 3-lane discovery + scoring engine (Indeed + executive boards + fractional networks)
- ✅ Tailored resume variants + cover-letter factory
- ✅ Pipeline tracker + Todoist project
- ✅ Daily cron that re-runs the loop and stages ready-to-send Gmail drafts + a digest

## One honest caveat
The engine does 100% of finding/scoring/researching/writing and **stages every application as
a ready-to-send draft**. The final submit click is yours (the tools draft, they don't submit
ATS forms; and an application is irreversible). ~2 minutes/day to approve a batch.
