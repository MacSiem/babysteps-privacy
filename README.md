# BabySteps privacy policy

Static source for the BabySteps privacy-policy page. `index.html` contains Polish and English sections (`#pl`, `#en`); `pl/` and `en/` are redirect pages to `/#pl` and `/#en`. The eight further app languages have full translated pages (from the English text; Polish is the binding version, each page says so):

| Language | Policy | Terms | Data deletion |
|---|---|---|---|
| pl / en | `/#pl` `/#en` (`/pl/` `/en/`) | `/terms/#pl` `/terms/#en` | `/delete-data/#pl` `/delete-data/#en` |
| de es fr ja ko pt (pt-BR) uk zh (zh-Hans) | `/<lang>/` | `/<lang>/terms/` | `/<lang>/delete-data/` |

All pages carry a language switcher and `hreflang` alternates (x-default is the PL/EN page). Translations were produced from the English text, with app screen and button names taken verbatim from the app locale files (`deleteData.*` and settings strings); when the app strings change, update the pages. Any content change must be made in PL, EN and all eight translations together.

## Data-deletion page

`delete-data/index.html` is a small bilingual (PL/EN) page, translated for the eight further languages at `/<lang>/delete-data/`, with the data-deletion instructions that accompany policy section 14, used as the Play Console data-deletion URL (`https://macsiem.github.io/babysteps-privacy/delete-data/`). Its item names and effects follow the app screen "Delete my data" (`src/screens/DeleteDataScreen.tsx` and the `deleteData` locale strings); keep them in step with the app. Include it in the post-publication readback with the root page, terms and the ten redirects.

## Terms of service

`terms/index.html` contains the matching Polish and English BabySteps service terms. It supplements store terms; the Apple Standard EULA remains in place. Privacy navigation links to both sections. The other eight UI locales have translated terms at `/<lang>/terms/` (non-binding translations; the Polish version is binding). The published terms have an effective document version of 2026-10-06. A read-only check on 2026-10-10 confirmed that the canonical terms and policy match the approved source commit `8f4961f`. No custom EULA has been entered in App Store Connect.

## Stack and local preview

Plain HTML and inline CSS. No package manifest, dependency installation, npm scripts, generated site or build step is present in this repository.

Open `index.html` directly, or use a Python 3 static server from the repository root:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/` to inspect the policy and its `#pl` and `#en` sections. Locale redirects lead to the canonical public URL even during local preview; check their HTML targets separately. Python is an optional preview tool, not a project dependency.

## Updating and publishing

This repository contains the Polish and English BabySteps privacy policy, language redirects, and terms. The policy describes optional cloud/file backups, Apple authorization and revocation, family features, and data retention.

Edit the Polish and English policy sections together, including the visible last-updated date when the policy content changes. Keep redirect targets and canonical links consistent. Check the root page, language anchors and all ten redirect pages before publishing.

GitHub Pages settings read on 2026-10-03 identify a legacy Pages build from the root (`/`) of `main`, with HTTPS enforced. There is no tracked deployment workflow or deploy script. A push or merge to the publishing branch can change the public policy; it requires the owner's release authorization and publish guard. Recheck Pages settings before publishing. After publication, read back the canonical policy and redirects; a commit or dispatch does not establish that the public page changed.

## Configuration and history

The static site has no evidenced environment variables or secrets. `.env.example` therefore records that no entries are required; never put credentials into policy HTML. `CHANGELOG.md` tracks unreleased documentation changes and future policy releases. The current document version is 14 November 2026 (BabySteps 2.1.0) for the policy, the terms and the data-deletion page; all public paths (policy, terms and data-deletion page in PL/EN, the `pl/` and `en/` redirects and the 24 translated pages `/<lang>/`, `/<lang>/terms/`, `/<lang>/delete-data/`) belong in its readback. Earlier versions: the policy displayed `2026-10-29` and the service terms `2026-10-06`. The policy publication on 2026-10-29 was read back successfully and matched approved source `5cccf4a`. All twelve public paths (policy, terms and ten locale redirects) returned HTTP 200 and matched source commit `8f4961f` on 2026-10-10. The dates shown in the documents identify their content version; the verification date records the public readback.

## Links

- [Canonical privacy policy](https://macsiem.github.io/babysteps-privacy/)
- [Privacy and support contact](mailto:mail@macsiem.dev)
- [MacSiem.dev](https://macsiem.dev/)
- [Policy source repository](https://github.com/MacSiem/babysteps-privacy)
- [Pair worker source repository](https://github.com/MacSiem/babysteps-pair-worker)

The worker link above identifies source, not verified live service status. Operational Sentry details belong in the private app and worker documentation; this static policy site has no Sentry integration or credentials.
