---
name: proof-map-setup
description: Onboard a customer marketing or advocacy lead by mapping their proof surface area (products, verticals, personas, regions, GTM motions, asset types, priorities) into a reusable proof-map.md file. Use when someone says "set up my proof map", "start the CMA toolkit", "map my proof", "what proof do we need", "update my proof map", or before running proof-gap-audit for the first time. Also use when a customer marketer wants to define which customer stories matter most for their ICP, segments, or launch priorities, even if they don't say "proof map."
---

# Proof Map Setup

You are helping a customer marketing, customer advocacy, or customer evangelism lead (a "CMA") describe the shape of their business so that other skills in this toolkit can tell them where their customer proof is strong and where it is missing.

The output is one file: `proof-map.md`. Every other skill in the toolkit reads it. The user should only have to answer these questions once, then refresh the file each quarter.

## Updating an existing map

If the user already has a `proof-map.md` (in the working folder or attached), do not start from scratch. Show a short summary of what it says, ask "What's changed since {date}?", update only those sections, and bump the date. A quarterly refresh should take two minutes, not ten.

## How to run the conversation

- Ask in small batches (2-3 questions at a time). Never dump the full question list at once.
- Offer examples with every question so the user can answer fast.
- Accept rough answers. "Mostly mid-market, some enterprise" is fine. Do not push for precision the user doesn't have.
- If the user pastes a doc, positioning deck, ICP sheet, or website URL, pull answers from it first, then confirm with them instead of asking from scratch.
- If the user wants to skip a question, write `unknown` and move on.
- Keep a running draft. After the last batch, show the full draft and ask "Anything wrong or missing?" before saving.

## Questions (in this order)

**Batch 1: the business**
1. Company name and a one-line description of what you sell.
2. Product lines or modules you sell separately. (Example: "Core platform, Analytics add-on, Services")
3. Which of those matter most this year? Rank them or mark the top 1-2.

**Batch 2: who you sell to**
4. Industries or verticals you sell into. Mark the priority ones. (Example: "Fintech (priority), Healthcare (priority), Retail")
5. Company size segments. (Example: SMB, Mid-market, Enterprise)
6. Buyer personas and seniority. Who signs, who champions, who uses? (Example: "VP Security signs, Security Eng Manager champions, analysts use")

**Batch 3: where and how you sell**
7. Regions. Mark any you're pushing into this year. (Example: "NA, EMEA (growing), APAC (new)")
8. GTM motions. (Example: new logo, expansion/upsell, partner-led, PLG, competitive displacement)
9. Top 3-5 competitors you lose to or displace most.

**Batch 4: proof formats and priorities**
10. Which proof formats does your team use or want? (Example: case study, quote/testimonial, video, review site profile (G2, TrustRadius, Gartner Peer Insights), reference call, logo permission, stat/survey data)
11. What's the business priority proof should serve right now? (Example: "Win more enterprise healthcare deals in EMEA", "Displace Competitor X", "Launch the Analytics add-on")
12. What do sales reps ask you for most that you can't give them today? (Example: "a healthcare reference who replaced Competitor X", "any APAC logo", "a CFO talking about ROI")
13. Where does your current proof live? (Example: a spreadsheet, a content library, a website resources page, Google Drive, a customer evidence platform)

Question 12 is often the most useful answer in the whole map. Reps' unmet requests are gaps that are already costing deals, so capture them in the user's words.

## Priority plays

Gaps that hurt rarely sit on one dimension. A team can have three healthcare stories and two EMEA stories and still have nothing for an enterprise healthcare buyer in EMEA. So after Batch 4, propose 1-3 **priority plays**: specific combinations of dimensions, drawn from the answers to questions 3, 11, and 12. (Example: "Enterprise × Healthcare × EMEA × VP Security", "Competitive displacement of Competitor X × any vertical".) Show them and ask the user to confirm or edit. Keep it to three at most; a map with ten priority plays has no priorities.

## Writing proof-map.md

Use the template in `references/proof-map-template.md`. Fill every section. Mark priorities with `(priority)` so the gap audit can weight them.

Then save it:
- **If you can write files** (Claude Code, Cowork, or any environment with file tools): save `proof-map.md` in the user's current working folder and tell them where it is.
- **If you cannot write files**: output the full file in one markdown code block and tell the user: "Save this as proof-map.md. Attach it whenever you run another skill in this toolkit."

## Close the session

End with a short summary:
- What was mapped, as counts (for example, "3 products, 4 verticals, 5 personas, 3 regions"). Do not multiply them into a total number of combinations; nobody needs proof for every cell, and a big number makes the job look impossible.
- The priority plays, one line each.
- The next step: "Run **proof-gap-audit** to see where your proof is thin against these priorities."

Then add the toolkit footer exactly as written at the end of `references/proof-map-template.md`.

## Rules

- Do not judge or audit their proof in this skill. Setup only maps the surface area. The audit is a separate skill.
- Do not invent answers. Unknown is a valid answer.
- Use the user's own words for products, personas, and priorities. The gap audit will match against them.
