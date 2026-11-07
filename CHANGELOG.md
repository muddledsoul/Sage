# Changelog

Versions follow [semver](https://semver.org): MAJOR.MINOR.PATCH. Every release is tagged in git (`v1.2.0`) and shown at the bottom of the app.

## How to release
1. Bump `APP_VERSION` and `APP_BUILD` in `index.html` and `version` in `version.json` (keep them equal).
2. Add an entry below.
3. Commit, then `git tag -a vX.Y.Z -m "..."` and `git push --follow-tags`.

Open copies of the app check `version.json` when brought to the front and offer an **Update** button when a newer version is live.

## 1.4.0 — 2026-11-07
- Product photos no longer fall back to swatches when a store blocks its images: each photo tries the store link, then an image relay (images.weserv.nl), then the product page's preview image (via microlink.io), before showing a swatch.
- The listing finder now copies photo links from the page instead of guessing, and keeps backups.

## 1.3.0 — 2026-11-07
- Sizes are set as ranges: a from/to dropdown per category with real size steps (dresses 00–16, shoes 5–12 in halves, denim 23–34, letter sizes). One size or a span like 2–4 or 8.5–9.

## 1.2.0 — 2026-11-07
- Version number, build date and mode shown at the bottom of the app.
- Update check: the app offers to reload when a newer version is deployed.
- CHANGELOG and tagged releases.

## 1.1.0 — 2026-11-07
- Real listings: each pick and hand-picked photo is searched, its product page opened, and the listing photo, current price and buy link pulled in.
- Listed price shown on cards; "Search again" for pieces without a match.

## 1.0.0 — 2026-11-07
- First release: style profile, daily picks, saves, lists, Sage's Hand Picked from photos.
- Standalone mode for GitHub Pages using your Claude API key, with web search.
- Seeded with the Macy's Herald Square trip photos.
