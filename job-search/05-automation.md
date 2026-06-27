# Automation — How the daily engine runs itself

## The loop
A scheduled job re-invokes the **DAILY LOOP** section of `00-SUPER-PROMPT.md` every morning.
Each run: discovers new roles across all 3 lanes + executive boards, scores them, researches
the keepers, generates tailored resume pointers + cover letters, stages **ready-to-send Gmail
drafts** in label `JobSearch/ReadyToApply`, updates `applications/tracker.csv`, files Todoist
tasks, sweeps the inbox for recruiter replies, and sends you a one-screen digest.

## Schedule (active this session)
- **Daily 7:50am local** — full discovery + draft pipeline + digest.
- The cron is session-scoped (lives while this Claude session is alive) and recurring crons
  auto-expire after 7 days. To make it permanent across machines/sessions, re-arm it or run
  it as a durable scheduled task / external cron calling the same prompt.

## Your 2-minute daily routine
1. Open Gmail label **JobSearch/ReadyToApply**.
2. Skim each draft (score + why + tailored letter + apply link + which resume variant).
3. For keepers: click the apply link, paste the letter, attach the named resume variant, submit.
4. Anything you skip stays logged in `tracker.csv` so it's never re-surfaced.

## The autonomy boundary (why the final click is yours)
The connected tools **draft**, they don't **submit** ATS forms or send employer emails. And an
application is your name on the line — effectively irreversible. So the engine does 100% of the
finding/scoring/writing and stages everything; you approve a batch in ~2 min. Connect a
browser-automation tool later and the same pipeline can submit end-to-end.

## Re-arming / changing cadence
- Change time or frequency: ask "reschedule the job-search cron to <time>".
- Pause: ask "pause the job-search automation".
- Make durable: ask "make the job-search cron durable" (persists to `.claude/`).
