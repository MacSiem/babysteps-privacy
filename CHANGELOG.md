# Changelog

## 2026-11-14 — translations (BabySteps 2.1.0, document version unchanged)

- Full translations of the privacy policy, terms and data-deletion page into de, es, fr, ja, ko, pt (Brazilian), uk and zh (Simplified): `/<lang>/`, `/<lang>/terms/`, `/<lang>/delete-data/` (the former redirect pages `/de/` ... `/zh/` become full policy pages). Document version stays 14 November 2026 (BabySteps 2.1.0).
- Language switcher and `hreflang` added to the PL/EN pages (no change to PL/EN content); `/pl/`, `/en/`, `#pl`, `#en`, `/terms/#pl|#en`, `/delete-data/` unchanged.
- Each translation carries a note that it is provided for convenience and the Polish version prevails (the existing documents state no binding version; to be confirmed by the owner).

## 2026-11-14 — BabySteps 2.1.0

Document version 14 November 2026 for the privacy policy (PL/EN), the terms and the new data-deletion page `delete-data/`. Publication is the owner's authorized push to `main`; record the public readback separately.

- Privacy policy: sign-in (Apple or Google) is optional and never required; sign-in data held on the server (internal profile ID, Apple/Google provider ID, e-mail or Private Relay address, dates); Sign in with Apple on Android through the browser (token, authorization code and one-time ticket held at most 5 minutes); Apple access revocation attempted on deletion for iPhone and Android sign-in; creating a family space requires Premium or an active trial, joining is free; data-deletion section (`#usuwanie-danych` / `#data-deletion`) covering in-app "Delete my data" without sign-in, e-mail requests for users without the app, and deleting iCloud/Drive copies with provider tools.
- Data-deletion page `delete-data/` (PL/EN, Play Console deletion URL), linked from policy section 14. It lists the four items exactly as on the app screen ("Data on this phone", "All BabySteps backups in iCloud", "All BabySteps backups in Google Drive", "Data on the BabySteps server and family membership"), states that a backup item deletes all BabySteps backups in that provider account including other families' backups, and that backups in another provider account are deleted with the provider's tools.
- Terms: section 4 (family space requires Premium or trial) and section 7 ("Delete my data"); document version 14 November 2026.
- Matching store declarations are drafted in the app sprint file `release/PRIVACY-FORMS-210.md`.

## Earlier unreleased notes

- Prepare the 2026-11-02 PL/EN full-release draft: optional Drive/CloudKit/file backups, encrypted Apple authorization and revocation, family entitlement links, photo retention and metadata retained after account deletion. Publication and final app/backend qualification remain open.

- Complete matching PL/EN Apple CloudKit backup, account binding, cloud key access and separate deletion disclosures; prepare the effective legal-document version for guarded publication.

- Prepare BabySteps service terms in Polish and English, with family/content rights, the actual Drive/key model, phrase-file exports, deletion, store subscriptions, consumer rights and support. Keep the Apple Standard EULA, add privacy-page navigation, and require full review and guarded publication.

- Align the PL/EN privacy draft with the Google Drive backup model: its key is stored beside the backup, Google can access its content, and phrase-encrypted file export is separate. Document optional due date/corrected-age fields and Drive deletion; language entry points target the matching bilingual section. Publication and full privacy acceptance remain gated.

- Add static-site preview, publishing and redirect documentation.
- Record that the site requires no environment variables.

Historical publication entries require verified release notes; the policy content date is not publication evidence.
