# Review notes: proof-map-setup and proof-gap-audit (v0.1.0 draft)

Reviewed October 16, 2026. Delete this file before release.

## How these were tested

We walked both skills through a realistic practitioner scenario: a mid-size security vendor whose priority is winning enterprise healthcare deals in EMEA, with 14 assets in a spreadsheet, 30 G2 reviews, and a closed-won export. The changes below came from places where the original skills would have produced a report that looked right but sent the CMA after the wrong thing. They have not yet been run as installed skills in a fresh session, so a live run is the next step.

## What held up

The setup and audit split is right, the batching and "accept rough answers" guidance in setup is exactly how a good intake call runs, and the "report, don't build" guardrail is the single most important line in the toolkit. The gap types, the no-invented-customers rule, and treating unknowns as findings all stay as written.

## Changes to proof-map-setup

**Priority plays.** This is the biggest change. The original audit counts proof one dimension at a time, so in our test it reported healthcare as covered (three assets) and EMEA as covered (two assets) while the company had zero proof from an enterprise healthcare customer in EMEA, which was their stated priority. Setup now proposes one to three specific combinations from the user's answers and asks them to confirm, and the audit checks those intersections first. This is also the "product line 3 in APAC" scenario from the original planning conversation, which the first draft didn't actually catch.

**New question 12: what sales asks for that you can't provide.** Any CMA can answer this instantly, and it's the highest-signal input in the whole map because those gaps are already costing deals. The audit uses it as a ranking boost.

**Update mode.** The README says "refresh quarterly," but the skill would have rerun all 13 questions. It now loads the existing map and asks what changed.

**Closing summary.** The original multiplied dimensions into a total ("3 × 4 × 5 × 3"), which reads as 180 cells to fill and makes the job look impossible. It now reports counts and the priority plays.

Minor: removed "peer-review" from the formats list since it duplicated review sites, and added Gartner Peer Insights as an example.

## Changes to proof-gap-audit

**Priority play coverage and near matches.** The audit checks each priority play for full matches, then lists near matches (assets that hit every dimension but one). Near matches are often the fastest fix, since an update interview or a quote from a different persona at a customer you already have is far easier than a new story.

**Review sites summarized per platform.** In the test, 30 G2 reviews counted as 30 assets made nearly every dimension look covered. Reviews now roll up to one line per platform, and duplicate quotes across library, site, and reviews are merged. Duplicate review-sourced assets are a common real-world library problem, so this matters even for UE users pulling through the MCP.

**At risk status.** Proof from a churned customer or a quoted person who has left is worse than no proof, because a rep can send it into a deal. The audit now asks for churned customers and departed contacts and flags this, ranked just below Missing.

**In progress status.** Without knowing what's already in production, the audit recommended filling gaps the CMA was already filling. It now asks, and those gaps drop out of the top list.

**Asks matched to customer tenure.** The original pulled candidates from closed-won deals and could recommend asking a two-week-old customer for a case study. Brand-new customers get a "why we chose you" quote, review, or logo ask; customers with outcomes get case studies and references. Practitioners will notice this one immediately, since it's the difference between a tool that understands the job and one that doesn't.

**Who sends the ask.** The original draft ask read "You mentioned on our March call...," but the CMA usually wasn't on that call; the AE or CSM was. Each gap now names the sender, and the draft is written for that person.

**Over-tapped advocates.** Customers appearing in four or more assets get flagged so the CMA spreads asks around instead of burning out their best advocates.

**Large URL inventories.** The skill reads a resources hub's index first and only opens individual pages when it needs a field for a priority play, so a 60-asset hub doesn't mean 60 page reads.

**MCP first, without asking.** If a UE (or other evidence platform) MCP is connected, the audit uses it directly instead of asking the user where their proof lives.

## The UE lead: one decision for you

The original kept branding to the header and footer, which is the right instinct. We added a "Next run" section at the end of the report. It always tells the user when to rerun. If (and only if) the inventory came from a spreadsheet, URLs, or a paste, it adds one sentence noting that teams with a customer evidence platform can run this against a live, tagged library. That's the moment the user has just felt the pain of rebuilding the inventory, so it reads as a helpful observation rather than an ad, and it never appears for UE customers. It's a single line in `report-template.md` if you'd rather cut it. The guardrail was updated to allow it explicitly, so the model doesn't add pitches anywhere else.

## Files changed

`skills/proof-map-setup/SKILL.md`, `skills/proof-map-setup/references/proof-map-template.md`, `skills/proof-gap-audit/SKILL.md`, `skills/proof-gap-audit/references/report-template.md`, `skills/proof-gap-audit/references/asset-inventory-template.csv` (added a `status` column), `README.md` (question count and quick start), `CHANGELOG.md`.
