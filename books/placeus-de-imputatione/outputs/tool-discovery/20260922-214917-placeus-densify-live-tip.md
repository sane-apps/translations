# Tool Discovery Receipt

- Generated: 2026-09-22T21:49:15-04:00
- Query: placeus densify live tip
- Project root: `/Users/stephansmac/SaneApps/clients/translations/books/placeus-de-imputatione`
- JSON receipt: `/Users/stephansmac/SaneApps/clients/translations/books/placeus-de-imputatione/outputs/tool-discovery/20260922-214917-placeus-densify-live-tip.json`

## Recommendation
Existing path found. Reuse or extend what is already here before adding a new tool.

## Canonical Tool Paths
- **Tool discovery and canonical path selection**
  - Command: `ruby scripts/SaneMaster.rb tool_discovery --query "..."`
  - Why: Proof step before claiming a tool is missing or inventing a workaround.
  - Source: `scripts/SaneMaster.rb tool_discovery`

## Skills Registry
- `/Users/stephansmac/.codex/SKILLS_REGISTRY.md:31` | `status` | live project state across sources, including distribution/listing lanes | "what's the status", "where are we", "catch me up", "what's actually going on" |
- `/Users/stephansmac/.codex/SKILLS_REGISTRY.md:82` - ask where the failure lives or what path is authoritative -> `codebase-explorer`

## Global Skills
- `/Users/stephansmac/.agents/skills/firecrawl-agent/SKILL.md:18` - You want the AI to figure out where the data lives
- `/Users/stephansmac/.codex/skills/status/SKILL.md:33` Read `~/SaneApps/meta/PROJECT_MAP.md` for the roster. Cover **every live bucket** listed there, not only `apps/`:
- `/Users/stephansmac/.codex/skills/status/SKILL.md:45` Prefer live git + live public channels over handoff:
- `/Users/stephansmac/.codex/skills/status/SKILL.md:50` - for shippable apps: live appcast / dist ZIP vs tagged version when a release question is open
- `/Users/stephansmac/.codex/skills/status/SKILL.md:54` Skip `archive/` and `outputs/`. Skip a repo that is clean, on the last release tag (or matching live appcast), and has no customer-facing unreleased work. Do not trust stale PROJECT_MAP “not released” notes over live appcast/dist.
- `/Users/stephansmac/.codex/skills/email-ops/SKILL.md:27` auth, reconciliation, attachments, delivery verification, and support GitHub context.
- `/Users/stephansmac/.codex/skills/email-ops/SKILL.md:69` If a customer purchased before licensing was live and no key exists, use `legacy-license-recover <id>` after `review`. It verifies the legacy order, reuses or creates the real one-time 100% LemonSqueezy recovery code, writes the approved draft/evidence bundle, runs `reconcile` + `verify-facts`, and stops before approval/send.
- `/Users/stephansmac/.codex/skills/email-ops/SKILL.md:138` - **LemonSqueezy webhook:** /webhook/lemonsqueezy (purchase delivery emails)
- `/Users/stephansmac/.codex/skills/critic/SKILL.md:77` - first gather the live bug-family context from the relevant status/handoff/issues/research sources
- `/Users/stephansmac/.codex/skills/critic/SKILL.md:83` 1. live cluster confirmation
- `/Users/stephansmac/.codex/skills/evolve/SKILL.md:12` - Read the current AGENTS.md, handoff, skill registry, dependency baseline and the live client tool surface. Use `ruby ~/SaneApps/infra/SaneProcess/scripts/SaneMaster.rb tool_discovery --query "the actual question"` and reuse its receipt.
- `/Users/stephansmac/.agents/skills/firecrawl-browser/SKILL.md:57` | `--ttl <seconds>`            | Session time-to-live                               |

## Local Code
No matches.

## Project Docs
No matches.

## Health Checks
- MCP health: failed
- Project validation report: failed
- Validation verdict: n/a
