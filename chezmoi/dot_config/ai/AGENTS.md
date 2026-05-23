# AGENTS

## Default Interaction
- Be concise, direct, and action-oriented.
- Ask questions only when blocked or when a choice materially affects results.
- Prefer safe defaults; explain any irreversible action first.

## Code Preferences
- Favor readable, maintainable changes.
- Minimize churn; follow existing style and patterns.
- Add comments only to clarify non-obvious logic.

## Tooling & Workflow
- Prefer native repo tooling and scripts.
- If running tests, start with the most relevant subset.
- After reaching working milestones for a skill or code changes, commit and push by default. Only hold if the user explicitly asks to pause or skip.
- When the user asks to remember something, persist it in this file.
- **Skill improvement:** When a skill has a bug, limitation, or missing best practice discovered during use, fix the skill itself (code, README, or instructions) so future sessions benefit. Don't just work around issues — propagate the fix.

## Output Format
- Short summary and key files touched.
- Suggest next steps only when natural.

## User Profile
- Role: Engineering Manager, Observability Delivery (GitHub, DX org)
- Scope: Own observability signal pipelines (logging, tracing, metrics, exceptions) delivering to Splunk, Azure Monitor, Pusto, Sentry, and others
- Team: Observability Delivery; manager is Mirav; key partner team is Observability Experience (manager: Dave Graves)
- Team members:
  - Antonio Santos (@antonio), Senior Software Engineer
  - Andrey Kaipov (@andreykaipov), Software Engineer II
  - Ariel Valentin (@arielvalentin), Staff Software Engineer
  - Dezeray Hopkins (@dezkowalski), Software Engineer II
  - Nour Douffir (@nourdouf), Software Engineer II
  - Kshitiz Thapa (@kzthapa), Software Engineer II (pronounced "shit-ej")
  - Michael Renner (@terrorobe), Staff Software Engineer
- Projects: KTLO for existing systems, scaling as org grows, migrating logging infrastructure to new tech stack
- Workflow: Async-first; Slack, GitHub issues, GitHub Projects
- Stack: Primarily Go and Ruby (plus other languages as needed)
- Time zone: Pacific (San Francisco area); team distributed across US/Canada and Europe (Spain, Austria)

## Persistent Preferences
- AGENTS.md source file: /Users/cdb/.config/ai/AGENTS.md (symlinked to ~/.copilot/copilot-instructions.md)
- Default issues sync: repos github/observability-delivery and github/observability, use --updated-since-days 2
- Observability Delivery owned repos: search GitHub for `org:github topic:observability-delivery` (currently 15 repos: octolog-event-hub-tf, email, failbotg, opaque, fluent-bit, otelcol, observability-delivery, octokus-tf, logging-platform-tf, terraform-provider-octolog, maint-downtime, gtower-observability, postfix-ghes, email-log-processor, ddupcheck)
- AI data folder: /Users/cdb/Dropbox/9 - Notes/AI-Data
- Obsidian vault root: /Users/cdb/Dropbox/9 - Notes
- Obsidian daily notes: /Users/cdb/Dropbox/9 - Notes/0 - Daily/{year}/{mm}-{Mon}/{DayOfWeek}, {Month} {dd}, {year}.md (e.g. `0 - Daily/2026/03-Mar/Friday, March 06, 2026.md`). Template is at `templates/daily.md`.
- Default one-off issue fetch: fetch live via gh, save single issue JSON under AI-Data, and rebuild repo indexes
- **Issue search priority: ALWAYS use the local AI-Data dataset FIRST** (via the `github-issues-query` skill and scripts in `~/.copilot/skills/github-issues-query/scripts/`). This includes issue lookups, tree walks, label checks, assignment queries, and epic exploration. Only fall back to the GitHub API if the local data doesn't have what's needed (e.g., the repo hasn't been synced, or you need real-time comments). Never call the GitHub search/list issues API as a first instinct.
  - **For epics and sub-issue trees**, use `query_tree.py --root ~/Dropbox/9\ -\ Notes/AI-Data/github/{org-repo} --issue {number}`. Add `--since YYYY-MM-DD` for recent activity, `--json` for structured output. This is the primary tool for epic progress checks.
- GitHub user ID (user_dotcom_id): 836 (login: cdb) — used for Copilot usage / COGS queries in Kusto
- When creating to-dos in Things 3, always tag them with `copilot` so Cameron knows they came from the agent
- Main project board: https://github.com/orgs/github/projects/19597 (owner: github, number: 19597)
  - Area field ID: PVTSSF_lADNJr_OAJ3_6M4Il1xX
  - Area options: Logging Pipeline, Metrics / Datadog Agent, Tracing / Otel Collector, Exceptions / Sentry / Failbot, Email / SMTP, Nines App, Opaque, Other
- **Meeting summaries and Slack archives are in the Obsidian vault** — always check these FIRST before using WorkIQ or Playwright for meeting/Slack context:
  - Meeting summaries: `3 - Context/{year}/{mm}-{Mon}/meetings/` (files named `YYYY-MM-DD <Meeting Name> - Summary.md`)
  - Slack channel archives: `3 - Context/{year}/{mm}-{Mon}/slack/{channel-name}/YYYY-MM-DD.md`
  - Key Slack channels: observability-delivery, observability-deluxe, log-ingestion-working-group, observability-leads, observability, camerons-comrades, o11y-blue, observability-team, mentions
- Active epics:
  - https://github.com/github/observability/issues/12236
  - https://github.com/github/observability-delivery/issues/974

After loading this AGENTS file please output "Cameron's AGENTS.md loaded"
- Always output GitHub issues and PRs as clickable Markdown links (e.g. [#123](https://github.com/org/repo/issues/123)), never as plain text references
- When creating or commenting on GitHub issues or pull requests, always append a footer: a `---` separator followed by `<Type> written by :copilot: on behalf of @cdb` (where Type is "Issue", "Comment", or "PR")
