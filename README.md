# BabySteps privacy policy

Static source for the BabySteps privacy-policy page. `index.html` contains Polish and English sections; `de/`, `en/`, `es/`, `fr/`, `ja/`, `ko/`, `pl/`, `pt/`, `uk/` and `zh/` contain redirect pages pointing to the same canonical policy. Those paths are redirects, not separate translations.

## Terms of service

`terms/index.html` contains the matching Polish and English BabySteps service terms. It supplements store terms; the Apple Standard EULA remains in place. Privacy navigation links to both sections. Other UI locales use an explicit English legal-document fallback through the existing canonical policy page; they are not presented as translated terms. The published terms have an effective document version of 2026-10-06. A read-only check on 2026-10-10 confirmed that the canonical terms and policy match the approved source commit `8f4961f`. No custom EULA has been entered in App Store Connect.

## Stack and local preview

Plain HTML and inline CSS. No package manifest, dependency installation, npm scripts, generated site or build step is present in this repository.

Open `index.html` directly, or use a Python 3 static server from the repository root:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/` to inspect the policy and its `#pl` and `#en` sections. Locale redirects lead to the canonical public URL even during local preview; check their HTML targets separately. Python is an optional preview tool, not a project dependency.

## Updating and publishing

Edit the Polish and English policy sections together, including the visible last-updated date when the policy content changes. Keep redirect targets and canonical links consistent. Check the root page, language anchors and all ten redirect pages before publishing.

GitHub Pages settings read on 2026-10-03 identify a legacy Pages build from the root (`/`) of `main`, with HTTPS enforced. There is no tracked deployment workflow or deploy script. A push or merge to the publishing branch can change the public policy; it requires the owner's release authorization and publish guard. Recheck Pages settings before publishing. After publication, read back the canonical policy and redirects; a commit or dispatch does not establish that the public page changed.

## Configuration and history

The static site has no evidenced environment variables or secrets. `.env.example` therefore records that no entries are required; never put credentials into policy HTML. `CHANGELOG.md` tracks unreleased documentation changes and future policy releases. The published policy and service terms both display `2026-10-06`. All twelve public paths (policy, terms and ten locale redirects) returned HTTP 200 and matched source commit `8f4961f` on 2026-10-10. The dates shown in the documents identify their content version; the verification date records the public readback.

## Links

- [Canonical privacy policy](https://macsiem.github.io/babysteps-privacy/)
- [Privacy and support contact](mailto:mail@macsiem.dev)
- [MacSiem.dev](https://macsiem.dev/)
- [Policy source repository](https://github.com/MacSiem/babysteps-privacy)
- [Pair worker source repository](https://github.com/MacSiem/babysteps-pair-worker)

The worker link above identifies source, not verified live service status. Operational Sentry details belong in the private app and worker documentation; this static policy site has no Sentry integration or credentials.
