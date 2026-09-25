# Press & Podcast Kit — prommer.net (prototype)

**Live:** https://themilkmanj.github.io/prommer-press-kit/ · **Proposed path:** `prommer.net/en/press-kit/`

## What
One static, single-file page (`index.html`, inline CSS + ~40 lines vanilla JS, no framework, no external requests) for one audience: **press & podcast bookers**. It answers what a producer needs in ~30 seconds: who Thomas is, what he talks about (pitchable angles), copy-paste bios in 3 lengths, fast facts/links, and a booking form.

## Why
We The Flywheel's product card lists "press and podcast bookers looking for a sharp POV on agentic operations" as a target market for prommer.net, but the site spreads across many identities (exec advisor, athlete, grooming, music) and the homepage is ~259 KB with no clear booking path. This page is the opposite: focused, fast, one CTA ("Book Thomas").

## Integration (proposed)
- Drop in as an Astro page at `/en/press-kit/` (canonical already set), link from `/en/tech/press/` and the homepage nav.
- Replace the `mailto:` prototype (`press@prommer.net` is a **placeholder**) with a `fetch()` POST to the WTF CRM (`api.tfw.bz`) → lead record + routing to the earned-media agent, with a human approving replies.
- Add PostHog events for `copy_bio_*` and `booking_submit` to measure the funnel.
- Localize via the existing 14-locale setup.
