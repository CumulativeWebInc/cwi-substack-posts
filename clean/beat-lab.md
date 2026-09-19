Most of what a catalog needs done to a recording — stems, a broadcast-clean edit, a sync-ready prep — has historically meant opening a DAW, calling an engineer, or paying a service. **CWI Beat Lab** moves that work into the browser.

Live now at https://cumulativewebinc.github.io/cwi-beat-lab/, the Beat Lab is a browser-based stem lab for the CWI catalog: **stem separation**, **radio-clean editing** (explicit-content interval detection for broadcast-ready versions), and **sync-ready audio prep**. No install, no account, no bill. Built at $0, tests green 71/71, deployed on GitHub Pages.

## What it actually does

Three capabilities, each solving a real catalog problem:

**Stem separation.** Feed it a track; get back separated elements — drums, vocals, bass, and the rest — for remix work, sync stems, or reference. And here is the honesty clause the whole lab is built around: DSP-separated outputs are **always labeled as estimates, never studio stems.** Separation algorithms reconstruct; they do not retrieve. A lab that presents an estimate as a stem is a lab that will eventually burn a supervisor who trusted it. The Beat Lab labels its outputs for what they are.

**Radio-clean editing.** Explicit-content interval detection maps where a track's language blocks broadcast use — and that map is the first step toward a clean edit that can actually air. Radio still reaches people streaming doesn't, and every sync brief that mentions broadcast needs the clean version to exist, not to be theoretically possible.

**Sync-ready prep.** The last mile between a finished record and a deliverable: audio shaped and verified so that when a supervisor says yes, the file you send is already the file they need.

## The worked example: "Broken Hearts Club"

Theory is cheap, so the lab was proven on a real record. **"Broken Hearts Club" (ISRC QZES92391782)** — verified from Black's DistroKid dashboard — was run through the Beat Lab's radio-clean analysis. The result: a concrete interval map showing exactly where the track stands relative to broadcast standards, produced from the actual released audio, not from a guess about the lyrics.

That single run is worth more than a feature list. It demonstrates the workflow the lab exists for: take a catalog track, run the analysis, get a machine-readable answer about what it would take to make it air-ready. Repeat across the catalog. What comes out is not a folder of files but a body of knowledge — which tracks are broadcast-ready, which need edits, and where.

## The honesty rules

Two principles govern everything the lab does, and both are printed on the tin:

1. **DSP-separated outputs are estimates, never studio stems.** Separation is reconstruction. The lab never pretends otherwise, and neither should anyone quoting its results.
2. **Tests green or it doesn't ship.** 71/71. The Beat Lab doesn't ask for trust; it asks to be run.

This is the CWI build philosophy in miniature: real software, never simulations; verified numbers, never vibes; $0 marginal cost, so there's no price tag gatekeeping who gets to prep a catalog. If you're an independent label sitting on recordings that were never cleaned, never stemmed, never prepped — the wall was never the work. The wall was the price of the tools. The Beat Lab removes the wall.

## The manifest

```json
{
  "name": "CWI Beat Lab",
  "product": "browser-based stem lab for the catalog",
  "live_url": "https://cumulativewebinc.github.io/cwi-beat-lab/",
  "repo": "https://github.com/CumulativeWebInc/cwi-beat-lab",
  "capabilities": ["stem separation", "radio-clean editing", "sync-ready prep"],
  "worked_example": {
    "track": "Broken Hearts Club",
    "isrc": "QZES92391782",
    "analysis": "radio-clean interval detection"
  },
  "honesty_rule": "DSP-separated outputs labeled as estimates, never studio stems",
  "tests": "71/71",
  "unit_cost": "$0",
  "hosting": "GitHub Pages"
}
```

## Links & backup

- Try it live: https://cumulativewebinc.github.io/cwi-beat-lab/
- Source and issues: https://github.com/CumulativeWebInc/cwi-beat-lab
- Org and all builds: https://github.com/CumulativeWebInc

## Take the lab for a spin

Subscribe for the next Beat Lab upgrades — new capabilities ship under the App Factory's two-a-week cadence. Then open the lab, run a track, and star the repo ([cwi-beat-lab](https://github.com/CumulativeWebInc/cwi-beat-lab)) if it does something your studio charges for.

Producers and engineers: what catalog task do you still do in a DAW that should have been a browser tool years ago?
