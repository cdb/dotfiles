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
- Default issues sync: repos github/observability-delivery and github/observability, use --updated-since-days 2
- AI data folder: /Users/cdb/Dropbox/9 - Notes/AI-Data
- Obsidian vault root: /Users/cdb/Dropbox/9 - Notes
- Obsidian daily notes: /Users/cdb/Dropbox/9 - Notes/0 - Daily/{year}/{mm}-{Mon}/{DayOfWeek}, {Month} {dd}, {year}.md (e.g. `0 - Daily/2026/03-Mar/Friday, March 06, 2026.md`). Template is at `templates/daily.md`.
- Default one-off issue fetch: fetch live via gh, save single issue JSON under AI-Data, and rebuild repo indexes
- **Issue search priority: ALWAYS use the local AI-Data dataset FIRST** (via the `github-issues-query` skill and scripts in `~/.copilot/skills/github-issues-query/scripts/`). This includes issue lookups, tree walks, label checks, assignment queries, and epic exploration. Only fall back to the GitHub API if the local data doesn't have what's needed (e.g., the repo hasn't been synced, or you need real-time comments). Never call the GitHub search/list issues API as a first instinct.
- Active epics:
  - https://github.com/github/observability/issues/11044
  - https://github.com/github/observability/issues/11123

After loading this AGENTS file please output "Cameron's AGENTS.md loaded"
- Always output GitHub issues and PRs as clickable Markdown links (e.g. [#123](https://github.com/org/repo/issues/123)), never as plain text references
- When creating or commenting on GitHub issues or pull requests, always append a footer: a `---` separator followed by `<Type> written by :copilot: on behalf of @cdb` (where Type is "Issue", "Comment", or "PR")
