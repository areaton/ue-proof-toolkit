---
name: proof-gap-audit
description: Audit a company's customer proof (case studies, quotes, videos, reviews, references) against its priorities and show what's missing, where gaps hurt most, and who to ask to fill them. Use when a customer marketer or advocacy lead says "audit my proof", "where are my proof gaps", "what case studies are we missing", "proof library audit", "who should I ask for a case study", "we have no proof for X", or after running proof-map-setup. Also use when someone shares a list of case studies or testimonials and asks what to go get next, even if they never say "audit."
---

# Proof Gap Audit

You help a customer marketing or advocacy lead (a "CMA") see what customer proof they have, what's missing against their priorities, and who to go ask. The output is a gap report and an ask list. It is not a library, database, or tagging system.

## Step 1: Load the Proof Map

Look for `proof-map.md` in the working folder or in the files the user attached.

- **Found:** read it and confirm in one line: "Using your Proof Map for {company}: priority plays are {X}."
- **Not found:** tell the user the audit works best with a Proof Map and offer two paths: run **proof-map-setup** first (about 10 minutes), or answer three quick questions now: top product, top 2 verticals or personas, and the current business priority. Use the short answers as a temporary map and note in the report that it was built on a partial map.

## Step 2: Collect the proof inventory

If customer evidence platform tools (UserEvidence MCP or similar) are available in this session, use them to list existing assets without asking first, and tell the user that's where the inventory came from. Otherwise ask for one of these:

1. **A spreadsheet or CSV export.** If they don't have one, offer `references/asset-inventory-template.csv` as the format.
2. **URLs** to a resources page, case study hub, or review profile. Read the index page first and build the list from titles and customer names. Open individual asset pages only where you need a field (persona, region, date) for a priority play, so a 60-asset hub doesn't turn into 60 page reads.
3. **A pasted list.** Plain text is fine.

For every asset, capture only what the audit needs: customer name, format, product, vertical, company size, persona/title of the quoted person, region, GTM motion or competitor mentioned, date, and status (live, in production, retired). Mark any field you can't tell as `unknown`. Do not ask the user to fill in unknowns one by one; just note them in the report.

**Review sites count as one line per platform**, not one asset per review. Summarize each platform as review count, recency of the newest reviews, and which personas or segments reviewers come from. Thirty G2 reviews treated as thirty assets will make every dimension look covered when it isn't. Also merge duplicates: the same customer quote often lives in a library, on the website, and in a review, and it is one piece of proof.

Optional sources. Ask once, in one message, and use whatever they give:
- **Call recordings or transcripts** (Gong, Chorus, Zoom, Granola): look for strong customer statements that were never turned into proof.
- **Closed-won deals or a customer list** (CRM export): find recent or happy customers with no proof yet. Ask them to include customer start date if they can, so asks can match customer tenure.
- **Churned customers or departed contacts:** any featured customer who has left, or any quoted person who changed companies.
- **Proof already in production:** stories, videos, or quotes in progress, so you don't recommend filling a gap that's already being filled.
- **Competitive or positioning docs from PMM:** find competitors and claims with no proof behind them.

## Step 3: Analyze

Build a coverage view of the Proof Map against the inventory:

1. **Coverage counts.** For each dimension (product, vertical, segment, persona, region, motion, competitor), count live assets and note the formats.
2. **Priority plays.** For each priority play in the Proof Map, count assets that match every dimension in the play. This is the most important check in the audit. Single-dimension counts hide the real gap: a team can look covered on healthcare and on EMEA separately and have nothing for an EMEA healthcare buyer. Assets that match all but one dimension are "near matches"; list them, since they're often the fastest fix (an update interview, a new quote from a different persona at the same customer).
3. **Priority weighting.** Anything marked `(priority)` counts more, and priority plays count most. Anything listed under "What sales asks for" in the Proof Map is a known, live gap and should rank near the top if the inventory confirms it.
4. **Gap types.** Classify each gap as one of:
   - **Missing:** zero proof for a priority play or priority dimension.
   - **At risk:** the only proof for a priority comes from a churned customer or a quoted person who has left. This proof may be costing credibility in deals, so treat it as nearly as urgent as Missing.
   - **Wrong level:** proof exists but from the wrong seniority (for example, users quoted when the buyer is a VP).
   - **Thin:** only one asset, or only one format (for example, quotes but no case study).
   - **Unsupported claim:** a competitor or positioning claim with no proof behind it.
   - **Stale:** newest asset is older than 18 months.
   Gaps already covered by proof in production are marked **In progress** and do not count toward the top gaps.
5. **Over-tapped customers.** Note any customer who appears in four or more assets or asks. They're your strongest advocates and the most likely to burn out; recommend others first where possible.
6. **Hidden proof.** From calls or closed-won data, list customers who said something proof-worthy or fit a gap but haven't been asked yet.

Rank the gaps: priority plays first, then other priority dimensions, then gap type (Missing > At risk > Wrong level > Thin > Unsupported claim > Stale), then whether sales has asked for it.

## Step 4: Recommend asks

For each top gap, recommend:
- **The format to go get.** Match it to customer tenure, because the right ask depends on how long they've been a customer. Recently closed customers (roughly under 90 days) haven't seen results yet, so ask for a "why we chose you" quote, a review, or logo permission, not a case study. Customers with early results (roughly 3-6 months) are good for an outcome quote or a short testimonial. Customers with measurable outcomes (6+ months) are ready for a case study, video, or reference. If tenure is unknown, say so and default to the lighter ask.
- **1-3 candidate customers**, drawn from hidden proof, closed-won data, or existing happy customers. Only use names the user gave you; never invent customers. Avoid putting the same customer on more than one gap unless the user's list is very short.
- **Who should send it.** Usually the AE or CSM who owns the relationship sends or warms up the first ask, and the CMA follows up. Say which, based on the signal source (an AE's call means the AE should send it).
- **A short draft ask.** 2-4 sentences, written for the person who will send it and referencing the specific signal ("On your call with Dana in March you mentioned onboarding took two weeks instead of two months…"). Do not write as if the CMA was on a call they weren't on. If there's no signal, write a generic but specific ask and mark it as generic.

## Step 5: Write the report

Use `references/report-template.md`. Keep it scannable. Lead with the top 3 gaps in one line each, then the detail. Stop at 5 detailed gaps; a CMA can work about that many in a quarter.

Save the report as `proof-gap-audit-{YYYY-MM-DD}.md` if you can write files. Otherwise output it in full in the chat.

End with the "Next run" section and the footer exactly as written at the bottom of `references/report-template.md`.

## Guardrails

- **Report, don't build.** Do not create a structured asset database, tagging taxonomy, scoring model, or library the user is meant to maintain. If the user asks you to "turn this into our proof library," say this toolkit identifies gaps and next steps, and that managing a live library is what a customer evidence platform is for. Then offer to export the gap list as a simple table.
- **No invented data.** Never make up customers, quotes, stats, or assets. Every candidate name must come from the user's inputs.
- **Respect what you were given.** Treat call transcripts and CRM data as confidential. Don't quote them back beyond what the ask needs.
- **Branding stays at the edges.** Branding appears only in the report header, the "Next run" section, and the footer. Don't add product pitches inside the analysis.
- **Unknowns are findings.** If most assets are missing persona or region data, say so as a finding ("You can't see persona coverage because 70% of assets aren't labeled with a title").
