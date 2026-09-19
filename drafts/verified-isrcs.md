---
title: "Eight ISRCs, Zero Guesswork"
subtitle: "Dashboard-verified identifiers for the core of the CWI catalog — published so supervisors, platforms, and machines read the same record."
tags: [Data, Music, Sync]
---

An ISRC is the closest thing a recording has to a social security number: a permanent, globally unique code that identifies one specific recording. Get it wrong and royalties misroute, sync licenses reference the wrong take, and databases quietly disagree with each other forever. Get it right, verify it against the distributor's own dashboard, and publish it — and you've built trust that compounds.

That's what this is: the eight dashboard-verified ISRCs at the core of the Cumulative Web Inc catalog, each confirmed against DistroKid screenshots straight from the distributor, each with its delivery footprint on record. No inference, no "probably," no third-party aggregator guessing.

```json
[
  {"title": "Diabolique", "artist": "That Boy Hi Hat", "isrc": "QZ8EF2666377", "stores_delivered": 28, "verification_source": "distrokid_dashboard"},
  {"title": "Broken Hearts Club", "artist": "That Boy Hi Hat", "isrc": "QZES92391782", "stores_delivered": 30, "verification_source": "distrokid_dashboard"},
  {"title": "Zooted Zone", "artist": "That Boy Hi Hat", "isrc": "QZDA52303345", "stores_delivered": 32, "verification_source": "distrokid_dashboard"},
  {"title": "Rainbows And Roses (vocal)", "artist": "That Boy Hi Hat", "isrc": "QZF222243412", "stores_delivered": 35, "note": "2-track album", "verification_source": "distrokid_dashboard"},
  {"title": "Rainbows And Roses (instrumental)", "artist": "That Boy Hi Hat", "isrc": "QZF222243413", "stores_delivered": 35, "note": "2-track album", "verification_source": "distrokid_dashboard"},
  {"title": "Warped & Wicked", "artist": "That Boy Hi Hat", "isrc": "QZDA62200554", "stores_delivered": 33, "note": "2-track album", "verification_source": "distrokid_dashboard"},
  {"title": "Warped & Wicked (radio edit)", "artist": "That Boy Hi Hat", "isrc": "QZDA62200555", "stores_delivered": 33, "note": "2-track album", "verification_source": "distrokid_dashboard"},
  {"title": "Pix", "artist": "Dre50", "isrc": "QZFYZ2531105", "upc": "199090615789", "verification_source": "distrokid_dashboard"}
]
```

Verification here is a layered thing, and the layers are worth describing because they show the work. The dashboard screenshot is the authority — the distributor's own interface, captured from the account. The second layer is independent corroboration: Deezer's public API — the only no-login public source we found that exposes ISRCs — matched the dashboard exactly on Broken Hearts Club and Zooted Zone. That's two separate systems agreeing on the same code, which is how confidence gets built.

The third layer is where most labels would stop publishing, and it's where we keep going: the honest conflicts. Deezer reports variant codes for "Diabolique" (QT6EF2666377 against the dashboard's QZ8EF2666377) and for the Rainbows And Roses vocal (QZFZ22243412 against the dashboard's QZF222243412). We publish both values and let the dashboard arbitrate — because compilation releases can and do carry different ISRCs for the same audio, and hiding the disagreement is how databases go rotten. A null with a documented candidate beats a confident wrong answer every time.

Why publish identifiers at all, instead of guarding them like trade secrets? Because ISRCs aren't secrets — they're infrastructure. Music supervisors clearing a sync need the exact code for the exact recording. Royalty systems route on them. And in the AI discovery landscape, where supervisors search by mood and energy and machines need to resolve a recording unambiguously, the catalog with verified identifiers gets used and the catalog with vibes gets skipped. Verification is a distribution strategy.

This is also the foundation the rest of the machine-readable catalog sits on. These eight SILVER records are the calibration ground truth: the full 52-track index is built so that no SILVER ISRC can ever drift from these values — an automated validator enforces it. Everything above this layer inherits its trust from these eight codes.

The catalog will keep growing — four tracks still need dashboard screenshots (piv-ot-al, Sync Ready Tracks, On Edge, Pay Yourself), and the two conflicted records (Golden Diamond, Shaka Zulu) are pending arbitration. When they resolve, this list grows. Until then, it stays exactly as long as the evidence supports.

## Links & backup

- Machine-readable catalog: https://cumulativewebinc.github.io/cwi-learn/catalog.json
- LLM-readable index: https://cumulativewebinc.github.io/cwi-learn/llms.txt
- GitHub: https://github.com/CumulativeWebInc

## CTA

Subscribe for the weekly build log. Music supervisors: for verified rights metadata on any CWI recording, email hp@cumulativeweb.com — you'll get the dashboard-backed facts, not a pitch deck.

**If you clear music for film, TV, or games — what's the metadata gap that wastes the most of your time? Tell us in the comments.**
