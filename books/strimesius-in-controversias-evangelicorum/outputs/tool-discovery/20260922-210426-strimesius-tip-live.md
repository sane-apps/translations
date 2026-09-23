# Tool Discovery Receipt

- Generated: 2026-09-22T21:04:25-04:00
- Query: strimesius tip live
- Project root: `/Users/stephansmac/SaneApps/clients/translations/books/strimesius-in-controversias-evangelicorum`
- JSON receipt: `/Users/stephansmac/SaneApps/clients/translations/books/strimesius-in-controversias-evangelicorum/outputs/tool-discovery/20260922-210426-strimesius-tip-live.json`

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
- `/Users/stephansmac/.codex/skills/evolve/SKILL.md:12` - Read the current AGENTS.md, handoff, skill registry, dependency baseline and the live client tool surface. Use `ruby ~/SaneApps/infra/SaneProcess/scripts/SaneMaster.rb tool_discovery --query "the actual question"` and reuse its receipt.
- `/Users/stephansmac/.codex/skills/email-ops/SKILL.md:27` auth, reconciliation, attachments, delivery verification, and support GitHub context.
- `/Users/stephansmac/.codex/skills/email-ops/SKILL.md:69` If a customer purchased before licensing was live and no key exists, use `legacy-license-recover <id>` after `review`. It verifies the legacy order, reuses or creates the real one-time 100% LemonSqueezy recovery code, writes the approved draft/evidence bundle, runs `reconcile` + `verify-facts`, and stops before approval/send.
- `/Users/stephansmac/.codex/skills/email-ops/SKILL.md:138` - **LemonSqueezy webhook:** /webhook/lemonsqueezy (purchase delivery emails)
- `/Users/stephansmac/.codex/skills/macos-permissions/SKILL.md:22` 3. Attach saved live app logs before launch/relaunch. Run one app/flow at a time through the canonical wrapper. Request only missing permissions the selected feature actually needs, sequentially, within existing session authorization. Do not request every permission at startup.
- `/Users/stephansmac/.codex/skills/macos-permissions/SKILL.md:25` 6. **Re-read the live dialog/app after every permission action, including an owner-reported grant.** Verify the prompt is gone, refresh the target app's current authorization, then test the real feature and inspect its result. A click return, closed dialog, cached receipt, or “granted” report alone is not feature success. Relaunch only the affected app through its wrapper if observed state requires it, preserving logs and identity.
- `/Users/stephansmac/.codex/skills/website-audit/SKILL.md:23` Audit both source and live behavior:
- `/Users/stephansmac/.codex/skills/website-audit/SKILL.md:26` - live domain: CNAME, canonical URL, or SaneProcess product config
- `/Users/stephansmac/.codex/skills/website-audit/SKILL.md:47` Use canonical commands for live business signals:
- `/Users/stephansmac/.codex/skills/website-audit/SKILL.md:71` - Find all live website directories when the user says "our websites".
- `/Users/stephansmac/.codex/skills/website-audit/SKILL.md:87` 4. Verify live surfaces.

## Local Code
No matches.

## Project Docs
No matches.

## Health Checks
- MCP health: failed
- Project validation report: failed
- Validation verdict: n/a
