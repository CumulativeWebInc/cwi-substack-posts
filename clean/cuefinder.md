There is a quiet fact the sync industry figured out years ago and the metadata world is only now catching up to: **music supervisors search by mood, energy, and creative description — not by keyword tags.**

A supervisor cutting a trailer doesn't type "alt-rap 92 BPM." They describe a feeling: a slow-burn threat with a grinning hook. A montage that climbs. A needle drop that lands the joke and breaks the tension. The systems that serve them have adapted, and the catalog metadata that feeds those systems has not. That gap is the entire reason CueFinder exists.

## The landscape it was built for

The discovery layer of modern sync is a crowded field, and it's worth naming: **AIMS, Cyanite.ai, Harmix, Musiio, Supe, SourceAudio SonicSearch, DISCO, SyncIt, Viola, SoSyncable, Zen Music Group, DropCue** — plus the catalog infrastructure most labels already live in. The through-line across all of them is a shift from classification to description. The winning search is no longer the one with the cleanest genre taxonomy; it's the one whose track records carry the richest creative surface: sonic descriptors, BPM, moods, instrumentation, scene use-cases, lyrics, credits, and — critically — machine-readable rights metadata.

Genre tags are dying as a search primitive. Rich descriptors are the search primitive now. A catalog that describes its tracks the way supervisors think is a catalog that gets found. A catalog that files them under "Hip-Hop / Rap" and stops there is a catalog that stays invisible.

## CueFinder: CWI's answer

**CueFinder** is Cumulative Web Inc's AI sync-discovery engine, commissioned September 16, 2026 under the App Factory — the same shipping cadence that launches two production apps a week, every week, against the catalog. Its job is exactly the shift described above: take a catalog and make it machine-discoverable in the language supervisors actually search in.

The design principle is simple enough to say in one sentence: **a track should be findable by the feeling it creates and the scene it fits, not by the folder it's filed in.** That means:

- **Mood and energy descriptors** that match how briefs are written — tension, lift, menace, euphoria — instead of genre labels.
- **Sonic surface data**: BPM, instrumentation, production texture. The details a music editor reaches for when the clock is running.
- **Scene use-cases**: what kind of picture this track belongs under, stated plainly enough to be searchable.
- **Lyrics and credits**: the narrative content and the chain of who made it.
- **Machine-readable rights**: because discovery without clear rights is a recommendation, not an option.

## Infrastructure, not a pitch

Be clear about what CueFinder is and isn't. It isn't finished, it has no users, and nobody has adopted it — and it is not being presented as otherwise. It is **infrastructure built for where supervisor search is going**, built at $0, the same way every CWI product is built. The bet is directional: the catalogs that win the next decade of sync are the catalogs machines can read.

That bet is why CueFinder sits inside the Agent Deck gear line rather than standing alone. It reads the same verified metadata the rest of the deck produces — the same provenance discipline, the same demand that a claim be checkable before it's pitchable. Discovery built on verified data is a tool. Discovery built on adjectives is a demo.

## Why this matters for independent catalogs

The major publishers have entire teams translating their catalogs into supervisor language. Independent catalogs — the ones this Substack is written from — don't. That asymmetry is exactly what software is for. CueFinder is the independent catalog's answer to the department-of-sync the majors take for granted: a standing engine that keeps the catalog described, rights-tagged, and searchable while the artist goes back to making records.

The keyword-tag era asked the catalog to file itself. The descriptor era asks it to explain itself. CueFinder is the machine that does the explaining.

## The manifest

```json
{
  "name": "CueFinder",
  "product": "AI sync-discovery engine",
  "problem": "keyword-tag search is dying",
  "shift": "supervisors search by mood/energy/creative description, not genre tags",
  "mechanism": "mood/energy/scene descriptors + machine-readable rights",
  "inputs": ["sonic descriptors", "BPM", "moods", "instrumentation", "scene use-cases", "lyrics", "credits", "rights metadata"],
  "landscape": ["AIMS", "Cyanite.ai", "Harmix", "Musiio", "Supe", "SourceAudio SonicSearch", "DISCO", "SyncIt", "Viola", "SoSyncable", "Zen Music Group", "DropCue"],
  "status": "in development",
  "commissioned": "2026-09-16",
  "program": "App Factory",
  "unit_cost": "$0"
}
```

## Links & backup

- Org and all builds: https://github.com/CumulativeWebInc
- Part of the Agent Deck gear line — umbrella brand for CWI's licensable software.

## Talk to the machine

Subscribe for the build log as CueFinder takes shape — every milestone gets written up here. And if you're a music supervisor: the door is open. Email **hp@cumulativeweb.com** with the kind of search that keyword tags never solved for you, and let's see whether the catalog answers it.

Supervisors: what's the strangest description-based search you ever ran — and did anything in your library actually answer it?
