# Project Takshashila — Taxila, Pakistan

**Live site:** https://ruwaidashakeel05.github.io/Taxila/

A public heritage-awareness page about Taxila, Pakistan — a 2,600-year-old UNESCO World
Heritage site currently under active UNESCO review over 2026 conservation work at two of
its component sites. Built as coursework for a heritage/preservation learning track,
submitted here as the public write-up for Extension Sprint 6.

## What I built

- A researched, sourced page covering Taxila's history, timeline, and the July 2026
  UNESCO warning over cement/masonry work at Sirkap and Mohra Moradu.
- An interactive Three.js 3D reconstruction of a Gandharan monastery courtyard, toggling
  between a "reconstructed, c. 150 CE" view and "as found today."
- A client-side tool that turns any uploaded photo into a downloadable point cloud
  (`.ply` file), using a monocular depth heuristic — **not** real photogrammetry or
  multi-view Structure-from-Motion. It estimates depth from brightness (sky/foreground
  separation), edge strength, and vertical position. This was a deliberate choice: I
  tested real photogrammetry against the site photos first and it wasn't viable at this
  scope, so the heuristic is explicitly labelled as illustrative, not measured geometry.
- A sourced reference/source-log section, a Gandhara-region learning route with an
  embedded Google Maps link, and an interactive "Stupa Anatomy" diagram.

## What worked, what didn't, what I fixed

- The 3D scene and photo-to-point-cloud tool work end to end — I tested this myself,
  not just in my own dev environment. I opened the live link fresh, uploaded a real
  photo, and generated a genuine `.ply` file to confirm the pipeline produces usable
  output and not just an on-screen render.
- I found and fixed a real bug during review: the page referenced a `.ply` file
  (`output/jaulian_monastery_taxila.ply`) as "the source project" with no actual link —
  a dangling, unverifiable claim. I fixed the wording so it no longer points at
  unlinked evidence.
- I structurally validated a generated `.ply` file myself: 5,919 vertices, header count
  matching the actual data rows, all RGB values in range, depth values consistent with
  the code's expected range. That file is attached as evidence below.
- Initial version of the site was a local HTML file with no public hosting — I published
  it live on GitHub Pages so it's actually reachable, and added meta tags, a map-load
  fallback, and a "last verified" date stamp on the UNESCO claim so it's clear the
  conservation story is current, not archival.

## What AI helped with

I used Claude (Anthropic) as a reviewer and pair-programmer for the polish pass, not to
generate the project from scratch:
- Auditing the live site against the module rubric and flagging the unlinked `.ply`
  reference and missing process evidence.
- Fact-checking the central UNESCO claim against multiple independent July 2026 news
  sources before trusting it in the copy.
- Structurally validating the `.ply` file's header/data integrity.
- Helping draft this write-up and the accompanying mentor note, from notes and decisions
  that were mine.

All wording changes were reviewed by me and confirmed on the live site before publishing.

## Evidence

- Live site: https://ruwaidashakeel05.github.io/Taxila/
- Generated point cloud file: `pointcloud.ply` (attached to submission)
- Screenshot of rendered point cloud in the site's 3D viewer (attached to submission)

## Connection to PreserveMy.World

Taxila is a live, current case study in what "preservation" actually means and who gets
to decide — the same underlying question PreserveMy.World is built around. This project
is meant to make that tension legible to a general audience (day-trippers, diaspora
Buddhist visitors, heritage students) rather than leaving it in specialist UNESCO
reporting. The photo-to-point-cloud tool also demonstrates, at small scale, how
accessible client-side tools can lower the barrier for ordinary visitors to contribute
lightweight documentation of heritage sites — a small piece of the youth-led,
public-storytelling model PMW is trying to scale.

## What I'd improve next

- Rehost or properly link the reconstruction-model source files instead of referencing
  them by filename only.
- Add automated link-checking so the source log doesn't silently go stale.
- Extend the photo tool with a simple in-browser guide for what kinds of photos produce
  the cleanest point clouds.

---
**Work window:** [add exact dates/times]
**Hours claimed:** [add, ≤4]
