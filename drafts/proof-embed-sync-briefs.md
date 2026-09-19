---
title: "Proof, Not Hype: The Sync Verification Stack"
subtitle: "Two products, one doctrine — every catalog claim a supervisor can check before they ever email us back."
tags: ["Software", "Sync", "Data"]
---

Sync pitching runs on adjectives. "Huge sync potential." "Perfect for film." "One of the hottest records of the year." Supervisors have heard all of it, believed none of it, and the catalogs that win are the ones that arrive with something better than a paragraph: **verifiable proof.**

Cumulative Web Inc's sync verification stack is two products built to do exactly that — give a music supervisor evidence-tiered proof of catalog claims instead of hype. Both are live, both are tested, and both carry kill rules with dates, because tools that don't get used don't deserve to exist.

## Catalog Proof Embed

The **Catalog Proof Embed** (https://cumulativewebinc.github.io/cwi-proof-embed/) is the shareable unit of proof: an embeddable artifact that carries a catalog claim together with the evidence behind it. The idea is disarmingly simple — instead of telling a supervisor a track is verified, you hand them the verification itself, in a form they can check.

The specs: repo at https://github.com/CumulativeWebInc/cwi-proof-embed, **35/35 tests green**, built at $0 on GitHub Pages. And the accountability clause: **fewer than 10 third-party embeds by December 18, 2026, and the lane dies.** That's not marketing copy — it's a kill rule. If supervisors aren't embedding the proof, the proof isn't useful enough, and the honest move is to kill it and build what is. The rule is public because the failure mode of software without a kill rule is a portfolio of dashboards nobody opens.

## Sync Briefs

The **Sync Briefs** (https://cumulativewebinc.github.io/cwi-sync-briefs/) are the other half of the stack: nine evidence-tiered sync briefs, each one a structured pitch artifact that organizes a catalog claim by the strength of the evidence behind it. Not all proof is equal — a DistroKid-dashboard ISRC sits at a different tier than a scraped public page, and a brief that hides that difference is a brief that lies by formatting. The tiering is the product.

The specs: repo at https://github.com/CumulativeWebInc/cwi-sync-briefs, **20/20 tests green**, nine briefs live. Kill rule: **fewer than 25 briefs by December 18, 2026.** Nine exist now; the rule says twenty-five or the lane closes. Kill rules aren't pessimism — they're how you keep a build honest about the difference between activity and results.

## Why evidence tiers matter

The music industry's credibility problem in sync isn't that catalogs lie — it's that catalogs present every claim at the same confidence level. The stream count from a distributor dashboard and the stream count from a screenshot of a screenshot get the same font, the same placement, the same weight. A supervisor who's been burned once learns to discount everything by half. Everybody loses.

Evidence tiering fixes this at the artifact level. When a brief distinguishes between what was verified from the distributor, what was verified from a public source, and what's a claim awaiting verification, the supervisor doesn't have to guess — and the catalog that plays straight earns the trust that compounds. Proof is a marketing strategy. It's just one that only works if the proof is real.

This is the through-line of the whole Agent Deck gear line: verified or it didn't happen. The Beat Lab labels estimates as estimates. CueFinder builds on verified metadata. The proof stack exists because the industry standard — adjectives — was never a standard at all.

## The manifest

```json
{
  "products": [
    {
      "name": "Catalog Proof Embed",
      "live_url": "https://cumulativewebinc.github.io/cwi-proof-embed/",
      "repo": "https://github.com/CumulativeWebInc/cwi-proof-embed",
      "tests": "35/35",
      "kill_rule": "fewer than 10 third-party embeds by 2026-12-18"
    },
    {
      "name": "Sync Briefs",
      "live_url": "https://cumulativewebinc.github.io/cwi-sync-briefs/",
      "repo": "https://github.com/CumulativeWebInc/cwi-sync-briefs",
      "tests": "20/20",
      "briefs": 9,
      "evidence_tiers": true,
      "kill_rule": "fewer than 25 briefs by 2026-12-18"
    }
  ],
  "doctrine": "evidence-tiered proof, not hype",
  "unit_cost": "$0",
  "hosting": "GitHub Pages"
}
```

## Links & backup

- Proof Embed, live: https://cumulativewebinc.github.io/cwi-proof-embed/
- Proof Embed, source: https://github.com/CumulativeWebInc/cwi-proof-embed
- Sync Briefs, live: https://cumulativewebinc.github.io/cwi-sync-briefs/
- Sync Briefs, source: https://github.com/CumulativeWebInc/cwi-sync-briefs
- Org and all builds: https://github.com/CumulativeWebInc

## Bring the evidence

Subscribe for the kill-rule verdicts — December 18 gets written up honestly either way. Star both repos ([cwi-proof-embed](https://github.com/CumulativeWebInc/cwi-proof-embed), [cwi-sync-briefs](https://github.com/CumulativeWebInc/cwi-sync-briefs)) if verifiable beats hype in your book. And supervisors: bring us a claim you'd want proven — **hp@cumulativeweb.com**.

What's the biggest claim a catalog ever made to you that you wish had come with proof attached?
