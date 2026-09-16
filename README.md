# HDB v6.2.2 — Hardened test navigation

This release replaces the previous partial navigation fix with a single primary-screen router.

Changes:
- `.hidden` is now `display:none!important`.
- `showPrimaryScreen(id)` explicitly hides every top-level HDB screen and reveals exactly one target screen.
- Cognitive, Tapping and Memory instruction entry points use this router.
- The first screen of each test uses the same router.
- Post-save return uses the same router and returns to Data Collection.
- No test protocol, baseline calculation, Memory form, Motor Pattern Score or neurodegenerative scoring was changed.

Validation:
- JavaScript syntax check passed.
- Automated browser smoke test passed in Chromium for all three flows:
  Overview -> Instructions -> START -> correct test screen.
- Automated post-save route test passed:
  completed test -> Data Collection + saved confirmation.
