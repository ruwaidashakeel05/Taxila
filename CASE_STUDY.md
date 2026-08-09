# Case Study: Project Takshashila — Making a UNESCO Heritage Dispute Legible to the Public

**Live artifact:** https://ruwaidashakeel05.github.io/Taxila/
**Repo:** [add your repo URL]

## Problem

Taxila, Pakistan is a 2,600-year-old UNESCO World Heritage site currently under active
UNESCO review — in July 2026, UNESCO warned Pakistan to reverse conservation work at two
of its component sites (Sirkap and Mohra Moradu) or risk the site being placed on the
List of World Heritage in Danger. This is exactly the kind of live, specialist story
that stays buried in UNESCO reporting and Pakistani press coverage unless someone
translates it for a general audience. The problem: build a public-facing artifact that
makes both the history of Taxila and the current preservation dispute understandable
and engaging to people who aren't heritage specialists — day-trippers, diaspora
Buddhist visitors, and heritage/conservation students alike.

## My Role

I built and then rigorously QA'd the site myself across several polish passes:

- Researched and wrote the history, timeline, and current-dispute sections, sourcing
  every claim to a checkable reference.
- Built the interactive layer: a Three.js 3D reconstruction of a Gandharan monastery
  courtyard (toggling reconstructed vs. ruined state) and a client-side photo-to-point-cloud
  tool using a monocular depth heuristic.
- Manually tested every interactive element myself in a fresh browser and on mobile —
  this is what caught a real bug: a caption referencing a `.ply` file as "the source
  project" with no actual link. I fixed the wording.
- Published the site publicly on GitHub Pages (it started as a local, unhosted file),
  and added meta tags, a map-load fallback, and a "last verified" date stamp on the
  UNESCO claim so readers know exactly how current the dispute information is.

## Evidence

- Live site: https://ruwaidashakeel05.github.io/Taxila/
- Generated `.ply` point cloud file (structurally validated: 5,919 vertices, header
  count matched data rows, RGB and depth values in expected range) — [link/attach]
- Screenshot of the rendered point cloud in the site's 3D viewer — [attach]
- Commit history: [link]
- Public write-up / walkthrough (README): [link]

## Process

1. Drafted the initial site content and interactive tools.
2. Had it reviewed against a certificate-readiness rubric, which surfaced the unlinked
   `.ply` reference and missing hosting.
3. Fixed the hosting, fixed the copy bug, and fact-checked the central UNESCO claim
   against multiple independent July 2026 news sources before trusting it in the copy.
4. Generated a real photo → point cloud output and structurally validated it rather
   than assuming the tool worked.
5. Re-tested every interactive element end to end — 3D toggle, photo tool, map, route
   link — in a fresh/incognito browser and on mobile before considering it done.

AI (Claude) was used as a reviewer and pair-programmer throughout — auditing the site
against rubrics, fact-checking the UNESCO claim, and structurally validating the `.ply`
file — not to generate the project's research or decisions from scratch.

## Result

A public, working, sourced site that turns a specialist UNESCO preservation dispute into
something a general visitor can actually understand — including a hands-on tool that
lets anyone experience, in miniature, what it takes to document a heritage site
digitally. The unlinked-evidence bug I found and fixed is a small but real example of
the exact integrity problem PMW's review process is designed to catch — I caught it in
my own work before a mentor had to.

## What I Learned

[Add 1-2 honest sentences — e.g. what you learned about the limits of monocular depth
estimation vs. real photogrammetry, or about the importance of testing your own claims
before publishing them, or about how contested a "simple" restoration decision can be
once you research it properly.]

## Next Improvements

- Rehost or directly link the reconstruction-model source files instead of referencing
  them by filename only.
- Add automated link-checking so the source log doesn't silently go stale.
- Extend the photo tool with guidance on what kinds of photos produce the cleanest
  point clouds.

---
**Work window:** [start–end time]
**Hours claimed:** [≤2.5]
