# UserEvidence CMA Toolkit

Claude skills for customer marketing, customer advocacy, and customer evangelism teams. Map the proof your business needs, then find out what's missing and who to ask.

## What's inside (v0.1.0)

| Skill | What it does | When to run it |
| --- | --- | --- |
| `proof-map-setup` | Asks ~12 questions about your products, verticals, personas, regions, and priorities. Saves `proof-map.md`. | Once, then quarterly |
| `proof-gap-audit` | Compares your existing proof to your Proof Map. Returns your top gaps, hidden proof from calls and closed-won deals, and draft asks. | Monthly or quarterly |

More skills are coming (weekly happy-customer digest, advocate ask drafter). Watch or star this repo to get them.

## Install

**Claude Code (plugin, auto-updates)**
```
/plugin marketplace add DemandLoops/ue-cma-toolkit
/plugin install cma-toolkit@userevidence
```

**Claude.ai or Claude desktop (skills upload)**
1. Download `proof-map-setup.zip` and `proof-gap-audit.zip` from the latest release.
2. Upload each one in Claude's skills settings.
3. Start a chat and say "set up my proof map."

## Quick start
1. Say **"set up my proof map."** Answer the questions (about 10 minutes).
2. Gather your proof: a spreadsheet, a resources page URL, or an export. A CSV template is in `skills/proof-gap-audit/references/`.
3. Say **"run a proof gap audit."** Attach call transcripts or a closed-won list if you want hidden-proof suggestions.

## Works with or without UserEvidence
The skills run on spreadsheets, URLs, and pasted lists. If you use UserEvidence, they'll read your library through the UserEvidence MCP.

## Updates
See `CHANGELOG.md`. Plugin installs update automatically; skill uploads need a re-download.

---
Built by [UserEvidence](https://userevidence.com/?utm_source=cma-toolkit&utm_medium=github&utm_campaign=readme).
