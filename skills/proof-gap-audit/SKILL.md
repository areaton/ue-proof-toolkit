---
name: proof-gap-audit
description: Audit a company's customer proof (case studies, quotes, videos, reviews, references) against its priorities and show what's missing, where gaps hurt most, and who to ask to fill them. Use when a customer marketer or advocacy lead says "audit my proof", "where are my proof gaps", "what case studies are we missing", "proof library audit", or after running proof-map-setup.
---

# Proof Gap Audit

You help a customer marketing or advocacy lead (a "CMA") see what customer proof they have, what's missing against their priorities, and who to go ask. The output is a gap report and an ask list. It is not a library, database, or tagging system.

## Step 1: Load the Proof Map

Look for `proof-map.md` in the working folder or in the files the user attached.

- **Found:** read it and confirm in one line: "Using your Proof Map for {company}: priorities are {X}."
- **Not found:** tell the user the audit works best with a Proof Map and offer two paths: run **proof-map-setup** first (about 10 minutes), or answer three quick questions now: top product, top 2 verticals or personas, and the current business priority. Use the short answers as a temporary map and note in the report that it was built on a partial map.

## Step 2: Collect the proof inventory

Ask the user for their current proof. Accept any of these, in this order of preference:

1. **A customer evidence platform via MCP.** If UserEvidence MCP tools (or a similar evidence platform's tools) are available in this session, use them to list existing assets.
2. **A spreadsheet or CSV export.** If they don't have one, offer `references/asset-inventory-template.csv` as the format.
3. **URLs** to a resources page, case study hub, or review profile. Read each page and list the assets you find.
4. **A pasted list.** Plain text is fine.

For every asset, capture only what the audit needs: customer name, format, product, vertical, company size, persona/title of the quoted person, region, GTM motion or competitor mentioned, date. Mark any field you can't tell as `unknown`. Do not ask the user to fill in unknowns one by one; just note them in the report.

Optional sources. Ask once, in one message, and use whatever they give:
- **Call recordings or transcripts** (Gong, Chorus, Zoom, Granola): look for strong customer statements that were never turned into proof.
- **Closed-won deals or a customer list** (CRM export): find recent or happy customers with no proof yet.
- **Competitive or positioning docs from PMM:** find competitors and claims with no proof behind them.

## Step 3: Analyze

Build a coverage view of the Proof Map dimensions against the inventory:

1. **Coverage counts.** For each dimension (product, vertical, segment, persona, region, motion, competitor), count assets and note the formats.
2. **Priority weighting.** Anything marked `(priority)` in the Proof Map counts more. A gap on a priority dimension outranks a gap anywhere else.
3. **Gap types.** Classify each gap as one of:
   - **Missing:** zero proof for a priority dimension.
   - **Thin:** only one asset, or only one format (for example, quotes but no case study).
   - **Stale:** newest asset is older than 18 months.
   - **Wrong level:** proof exists but from the wrong seniority (for example, users quoted when the buyer is a VP).
   - **Unsupported claim:** a competitor or positioning claim with no proof behind it.
4. **Hidden proof.** From calls or closed-won data, list customers who said something proof-worthy or fit a gap but haven't been asked yet.

Rank the gaps. Use this order: priority dimension first, then gap type (Missing > Wrong level > Thin > Unsupported claim > Stale), then how many deals it likely touches.

## Step 4: Write the report

Use `references/report-template.md`. Keep it scannable. Lead with the top 3 gaps in one line each, then the detail.

For each top gap, recommend:
- the format to go get (case study, quote, video, review, reference),
- 1-3 candidate customers to ask, drawn from hidden proof, closed-won data, or existing happy customers (only names the user gave you; never invent customers),
- a short ask: 2-4 sentences the CMA can send, referencing the specific signal ("You mentioned on our March call that onboarding took two weeks instead of two months…"). If there's no signal, write a generic but specific ask and mark it as generic.

Save the report as `proof-gap-audit-{YYYY-MM-DD}.md` if you can write files. Otherwise output it in full in the chat.

End with the footer exactly as written at the bottom of `references/report-template.md`.

## Guardrails

- **Report, don't build.** Do not create a structured asset database, tagging taxonomy, scoring model, or library the user is meant to maintain. If the user asks you to "turn this into our proof library," say this toolkit identifies gaps and next steps, and that managing a live library is what a customer evidence platform is for. Then offer to export the gap list as a simple table.
- **No invented data.** Never make up customers, quotes, stats, or assets. Every candidate name must come from the user's inputs.
- **Respect what you were given.** Treat call transcripts and CRM data as confidential. Don't quote them back beyond what the ask email needs.
- **One footer, no inline ads.** Branding appears only in the report header and footer. Don't add product pitches inside the analysis.
- **Unknowns are findings.** If most assets are missing persona or region data, say so as a finding ("You can't see persona coverage because 70% of assets aren't labeled with a title").
