---
title: "Teaching AI Our Catalog: Machine-Readable Facts Instead of Hallucinations"
subtitle: "Canonical endpoints on GitHub Pages — llms.txt, catalog.json, graph.json, kit.json, agent-card.json — so every model reads verified facts, not guesses."
tags: [Data, AI, Music]
---

Every AI model knows a little about every artist, and almost all of it is half-remembered. Ask about an independent catalog and you get confident fiction: wrong track counts, invented ISRCs, credits stitched together from whatever the training data happened to scrape. The durable fix isn't arguing with the model. It's giving the model a source of truth it can actually read.

That's what we built: https://cumulativewebinc.github.io/cwi-learn/ — a canonical set of machine routes for the entire Cumulative Web Inc catalog. Not a webpage for humans. Plumbing for machines.

The routes are simple and deliberate. `/llms.txt` is the standard large-language-model briefing file: what the catalog is, where the records live, how to cite them. `/catalog.json` is the full track catalog as structured data. `/graph.json` is the catalog as a knowledge graph — artists, tracks, credits, relationships, linked. `/kit.json` is the pack a downstream builder needs to do something with the data. And `/.well-known/agent-card.json` is the identity card: who we are, what endpoints we expose, how to reach us.

Every route is verified HTTP 200. A `.nojekyll` file sits at the root so the dot-paths (`/.well-known/…`) actually serve — GitHub Pages would otherwise swallow them. This is the kind of unglamorous detail that determines whether machine-readable infrastructure works or merely looks like it works. We verified, then verified again.

Why does this matter? Because discovery is moving from keywords to machines. Music supervisors now search by mood, energy, and creative description — "dark, slow-burn tension for a heist scene" — and the systems they use (AIMS, Cyanite, Musiio, DISCO, and the rest) match audio against structured metadata. An AI sync-discovery engine that can't find your catalog is a door that's closed before anyone knocks. The same logic applies to every agent that might one day license, playlist, or write about the music: if your facts aren't machine-readable, the machine will hallucinate them instead.

The ambition behind this is durable and long-term: other LLMs and agents learning the catalog from verified machine-readable facts. Not scraped press releases. Not fan wikis. A canonical source the label itself maintains, where a claim about a track — its ISRC, its credits, its rights status — resolves to a record we signed off on.

This is also the foundation the rest of the machine stands on. The Catalog Chat tool in our promo stack answers questions about fifty-plus tracks because it reads these records. The trust layer (more on that in a coming piece) can seal facts because the facts live somewhere canonical. None of that works if the underlying data is a spreadsheet on someone's laptop.

We're publishing it openly. Any builder can pull the endpoints, feed them into a retrieval pipeline, and have a model's answers about this catalog grounded in our records instead of its training fog. That's the point: the catalog is data, and data wants to be queried.

The deeper shift is about who gets to be an authority. For decades, the record of a song lived in a distributor's database and a few press clippings, and everyone else worked from copies of copies. Canonical machine routes flip that: the label publishes the record once, machines read it directly, and there's exactly one version of the truth. When the ISRC is wrong somewhere, the fix goes in one place and propagates everywhere.

```json
{
  "name": "Cumulative Web Inc",
  "type": "agent-card",
  "endpoints": {
    "catalog": "https://cumulativewebinc.github.io/cwi-learn/catalog.json",
    "graph": "https://cumulativewebinc.github.io/cwi-learn/graph.json",
    "kit": "https://cumulativewebinc.github.io/cwi-learn/kit.json",
    "llms_txt": "https://cumulativewebinc.github.io/cwi-learn/llms.txt"
  },
  "contact": "hp@cumulativeweb.com",
  "verified": "HTTP 200, all routes"
}
```

## Links & backup

- Machine routes — https://cumulativewebinc.github.io/cwi-learn/
- Catalog — https://cumulativewebinc.github.io/cwi-learn/catalog.json
- Knowledge graph — https://cumulativewebinc.github.io/cwi-learn/graph.json
- Cumulative Web Inc on GitHub — https://github.com/CumulativeWebInc

## CTA

Subscribe to this Substack for the build log. If you build with models: pull the endpoints, ground your retriever in them, and tell us what broke. And star [CumulativeWebInc on GitHub](https://github.com/CumulativeWebInc) — the next canonical dataset lands there first.

**If you could ask an AI one question about an independent catalog and get a guaranteed-true answer, what would you ask?** Drop it in the comments.
