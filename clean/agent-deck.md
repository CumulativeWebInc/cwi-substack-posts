A record label used to be a building full of people. Cumulative Web Inc decided it should be a system full of gear.

**Agent Deck** is the name Black gave the AI app that holds the whole thing together: the umbrella brand for the gear line — Signal Boy, the Gear Ledger, and eight department products — where every product is a SKU on the same shelf. Not eight startups. Not eight pilots. One deck, one release cadence, one standard: production software, tested, deployed, real.

## The department stack

CWI's agent company runs on eight departments: A&R, Marketing & Social, Sync & Licensing, Radio & Playlists, Press & PR, Content Studio, Data & Analytics, and Business Affairs. The products follow the same order, and they are built in dependency order on purpose — because a gear line that ignores its own dependencies is a gear line that breaks:

1. **Data & Analytics** — the foundation. Every downstream product reads from it.
2. **Business Affairs** — licensing terms and rights scaffolding before anyone pitches anything.
3. **A&R, Sync & Licensing, Press & PR** — the discovery-to-deal layer.
4. **Marketing & Social, Radio & Playlists** — distribution and audience reach.
5. **Content Studio** — creative output that assumes the pipeline above it already works.

Data goes first because nothing else can verify its own claims without it. Affairs goes second because rights questions are cheapest to answer before a pitch exists. The rest stack on top. This is boring architecture and that is the point — the boring part is what keeps every SKU honest about what it actually does.

## Every product is a SKU, not a demo

The standing rule on this gear line: real software, never simulations. Each department product is designed from day one as a licensable SKU — white-label ready, with a clear manifest of what it does, what it reads, and what it outputs. That discipline does two things at once. Internally, it forces every build to define its inputs and outputs instead of hand-waving. Externally, it means any product that proves itself in-house is already packaged for the world.

The builds are done at $0 and deployed on GitHub Pages — zero marginal cost per product, zero hosting bills to justify. When the cost of shipping is zero, the only reason a product doesn't exist is that nobody built it yet.

## The App Factory: two a week, every week

Keeping up with that is the **App Factory**, CWI's standing shipping schedule: a minimum of **two new production apps per week**, every Monday and Thursday, every week. Each one uses the catalog in some way — because the catalog is the asset the whole machine exists to serve, and software that doesn't touch it is a hobby.

The factory is the part of Agent Deck most people underestimate. It's easy to build a product; it's hard to build a release cadence that survives week eleven. The factory treats cadence as the product. Monday and Thursday are launch days. The standard doesn't move for the calendar.

## What this means for the artist

For That Boy Hi Hat, the catalog is the raw material and Agent Deck is the refinery. Sync discovery tools that read machine-verified metadata instead of guesses. Playlist infrastructure that verifies placements by scan instead of claims. Verification artifacts that let a supervisor confirm a catalog fact without calling a manager's bluff. Every piece of the deck exists to answer one question an artist's team never stops asking: *how do we get this music heard, and how do we prove what we say about it?*

Nothing here is speculative. The deck is the working answer — built, tested, shipped, and iterated in the open.

## The manifest

```json
{
  "name": "Agent Deck",
  "umbrella_brand": "Agent Deck — umbrella brand for the CWI gear line",
  "products": ["Signal Boy", "Gear Ledger", "8 department SKUs"],
  "departments": [
    "Data & Analytics",
    "Business Affairs",
    "A&R",
    "Sync & Licensing",
    "Press & PR",
    "Marketing & Social",
    "Radio & Playlists",
    "Content Studio"
  ],
  "build_order": "Data → Affairs → A&R/Sync/Press → Marketing/Radio → Studio",
  "factory_cadence": "2/week",
  "factory_schedule": "Monday + Thursday, every week",
  "license_note": "white-label/licensable SKUs",
  "unit_cost": "$0",
  "hosting": "GitHub Pages"
}
```

## Links & backup

- Org and all builds: https://github.com/CumulativeWebInc
- The Agent Deck umbrella is the Cumulative Web Inc gear line — watch the org for new SKUs every Monday and Thursday.

## Get the next drop

If you're following this build in public, subscribe to this Substack — every launch and lesson gets written up here. And star the org on GitHub ([github.com/CumulativeWebInc](https://github.com/CumulativeWebInc)) so the shipping cadence is visible in your feed.

What should the App Factory build next — which lane of the label needs gear the most?
