# Auto-Apply Setup — Two Paths to Automated Submission

You can do everything up to the final submit today (find → score → tailor → stage as Gmail
drafts). To automate the *submit* itself, pick one of these. **Option B is recommended for
your $300K+ exec search; Option A is only a wide secondary net.**

---

## ⭐ OPTION B (recommended) — Browser-automation MCP (Playwright)

This connects Claude to a real Chrome browser so it can fill **and submit** the *tailored*
applications this system already produces — automation *with* quality, not spam.

### 1. Install the Playwright MCP server
Microsoft's official server: https://github.com/microsoft/playwright-mcp

**Claude Desktop / Claude Code** — add to your MCP config
(`claude_desktop_config.json`, or this repo's `.mcp.json`):
```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@playwright/mcp@latest", "--browser", "chromium"]
    }
  }
}
```
Run it **headed** (visible browser) the first few times so you can watch and intervene:
add `"--headed"` to the args. Restart Claude after editing the config.

### 2. Log in once, in that browser
Start a session and have the browser open Indeed / LinkedIn / the ATS sites; **you** log in
(and clear MFA) in that controlled browser. The session persists, so the agent reuses your
authenticated state — your passwords are never typed into chat.

### 3. The "apply run" prompt (paste once connected)
> Using the Playwright MCP browser, work through `job-search/applications/apply-queue.csv`
> top to bottom. For each row with status=QUEUED: open apply_url, fill the form using my
> profile in `job-search/01-profile.md` and the cover letter named in cover_letter_ref,
> upload the résumé from Drive, **pause and show me the filled form for approval, then submit
> on my OK**. Mark the row APPLIED (with date) or NEEDS_ME (CAPTCHA/MFA/odd field) and move on.

### 4. Honest caveats
- **CAPTCHAs / MFA / "verify you're human"** will still need you — the agent pauses on these.
- ATS forms vary wildly (Workday, Greenhouse, Lever, iCIMS); expect some NEEDS_ME rows.
- **Keep the approval gate on** for exec roles — one bad auto-submit can cost you a role.
- Credentials live in *your* browser profile; don't run this on a shared machine.

### 5. How this system feeds it
- `applications/apply-queue.csv` — the work list (kept current by the daily engine).
- `04-cover-letter-templates.md` + the per-role drafts — the tailored copy.
- Google Drive "Nitin Sekhar - Executive Resume" — the résumé to upload.
- `01-profile.md` — answers for standard form fields (work auth, location, etc.).

---

## OPTION A — Mass auto-apply service (wide secondary net only)

⚠️ Volume tools send a *generic* application. For CISO/CIO/COO/fractional roles that can
**hurt** you. Use this **only** to cast a wide net on lower-priority / high-volume listings —
never as your primary channel for the $300K target roles.

### LoopCV (best free start) — https://www.loopcv.pro
1. Create account → upload the résumé PDF.
2. Build a "loop": keywords `CISO, VP Security, CIO, VP IT`; location `Remote` + `Dallas, TX`.
3. Set **manual-review mode** (don't blind-send); cap daily volume low (5–10).
4. Free tier = 10 apps/month; paid tiers add boards.

### LazyApply / Sonara — paid ($70–$100/yr)
- LazyApply: highest volume, Chrome extension drives Indeed/LinkedIn Easy Apply.
- Sonara: set-and-forget daily digest. Both send one generic résumé — keep them OFF your
  premium targets.

### Indeed's own auto-apply
In your Indeed account: complete your profile + résumé, turn on **job alerts**, and use
**Indeed Apply** (one-click) on matching roles. Indeed has no true "apply to everything
automatically" toggle for senior roles — Easy Apply still needs your click per job.

---

## Recommended model for you
1. **Option B (Playwright MCP)** submits the tailored applications this system stages — with a
   quick approval gate. Quality + automation.
2. Keep the **recruiter / networking** channel active (HIMSS JobMine, Ladders, fractional nets).
3. Optionally run **LoopCV free** as a wide net on lower-tier roles only.
4. **Skip** mass auto-apply on your $300K CISO/CIO/COO/fractional targets.
