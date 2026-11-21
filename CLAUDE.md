# GTM Context OS for Treford Business Suite

## Company

<!-- TODO: Fill after research -->
Treford: [one-line summary to add after research]

## How This Folder Works

- `context/icp/` — Ideal Customer Profile docs (firmographics, personas, pain points). Read before writing any outbound copy or campaign brief.
- `context/positioning/` — Positioning canvases, competitive comparisons, value props. Read before creating landing pages or pitch decks.
- `context/messaging/` — Messaging frameworks, taglines, proof points. Read before writing any customer-facing copy.
- `context/brand-kit/` — Voice guidelines, tone rules, visual identity notes. Read before producing any creative asset.
- `context/docs/research/` — Raw research notes, interview transcripts, market data. Read when building or updating any context doc.
- `knowledge-base/playbooks/` — Step-by-step GTM playbooks (outbound, inbound, launch). Read before executing any campaign.
- `knowledge-base/learnings/` — Post-mortems, experiment results, what-worked notes. Read when planning new experiments.
- `meetings/` — Meeting notes and action items. Read for decisions and commitments made.
- `output/campaigns/` — Finished campaign assets (emails, ads, landing page copy). Reference for consistency.
- `output/outbound/` — Outbound sequences, cold emails, LinkedIn messages. Reference for active outreach.
- `output/social/` — Social media posts and content. Reference for published social work.
- `output/data/` — Data exports, analysis outputs, reports. Reference for metrics and findings.
- `inspiration/` — Ads, emails, landing pages, and examples worth learning from. Read for creative reference.
- `tools/` — Automation configs, n8n workflows, scoring models. Read when building or debugging workflows.
- `weekly-priorities/` — Weekly priority files (YYYY-Www.md). Read at the start of every work session.
- `work-log/` — Timestamped change log per week (YYYY-Www.md). Append after every meaningful change.
- `.claude/skills/` — Custom Claude skills for this project.

## Rules

1. **Cite sources.** Every company fact must link to its source (URL, doc title, or interview date). Never invent numbers.
2. **No em dashes.** Use commas, colons, or separate sentences instead.
3. **Ask before sending.** Never send emails, publish content, or post to external services without explicit approval.
4. **Log everything.** After every meaningful change, append a timestamped entry to this week's `work-log/YYYY-Www.md`.
5. **Weekly priorities first.** Check `weekly-priorities/` at the start of each session.

## Tools

### Treg (CLI + MCP, paid data lookups)

- **What it does:** 4,200+ external tools across 136 providers (SEO/SERP, backlinks, social, enrichment, ads, scraping, generation). Credentials injected server-side.
- **Rule: Check the price before every call.** Run `treg catalog get <id>` to see the cost, and tell me before calling anything over $0.01.
- **Billing:** Pay-per-call against team prepaid balance. Run `treg balance` before large jobs.
- **Skill reference:** `.claude/skills/treg-tools.md` for full workflow and rules.

### Miro (MCP, diagrams)

- **What it does:** Create and edit diagrams, maps, and visual boards on Miro.
- **When to use:** GTM system maps, journey maps, workflow diagrams, anything visual that needs collaboration.

### Notion (MCP, finished docs)

- **What it does:** Publish finished documents to Notion for the team to read.
- **Rule:** GitHub stays the source of truth. Write and version everything here first, then push to Notion only when it is ready for others.
- **When to use:** Sharing completed context docs, playbooks, or briefs with the wider team.

### Skills (`.claude/skills/`)

- **signal-matrix** — Build ICP/signal matrices: segments, personas, and the signals that find them.
- **campaign-strategy** — Generate 15-25+ outbound campaign ideas with targeting, personalization, and priority tiers.
- **build-workflow-spec** — Turn one campaign idea into a full workflow spec (intent, signals, routing, cadence).
- **campaign-copy** — Write outbound copy for a workflow spec.
- **campaign-qa** — QA a Clay table or email campaign against its workflow spec.
- **campaign-contract** — Write the build sheet (contract.md) for one Clay campaign.
- **build-clay** — Build, audit, or repair a production Clay outbound workbook.
- **clay-build-plan** — Plan a Clay table build before executing it.
- **design-clay-table-json** — Write the Clay table JSON blueprint from a campaign contract.
- **import-clay-table** — Import a Clay table JSON into the workspace and prove it on a small run.
- **save-clay-schema** — Export an approved Clay table to the local registry.
- **export-tables** — Export Clay tables to local CSV files.
- **calculate-costs** — Report real dollar spend and credit usage of a Clay table's columns.
- **workspace-cost-audit** — Report what a Clay workspace spent in a month.
- **prompt-builder** — Build or repair a reusable prompt for Clay AI columns or other pipelines.
- **miro-gtm-flowchart** — Draw a GTM system as a flow chart on a Miro board.
- **inbox-placement-test** — Test email inbox placement.
- **agent-browser** — Browser automation: scrape, fill forms, click, screenshot.
- **crawl4ai** — Crawl web pages into clean Markdown or JSON (free, local).

### Playbooks (`knowledge-base/playbooks/`)

- **copy-frameworks.md** — Outbound copy frameworks and structures.
- **copy-iron-laws.md** — Non-negotiable rules for outbound copy.
- **copy-bans.yaml** — Banned words and phrases in outbound copy.
- **linkedin-dm-frameworks.md** — LinkedIn DM templates and frameworks.
- **signal-matrix-framework.md** — How to build a signal matrix from scratch.
- **workflow-anatomy.md** — Anatomy of an outbound workflow.
- **clay/** — Clay-specific playbooks and reference.
- **templates/** — Reusable templates.

### Tools (`tools/`)

- **agent-browser/** — Browser automation agent config.
- **crawl4ai/** — Crawl4ai runner config.
- **rex/** — Rex tool config.
