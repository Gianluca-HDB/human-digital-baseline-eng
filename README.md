# HDB v6.2.3 — QA checked

Full static and browser UI audit completed.

Fixes:
- Data Collection starts hidden, so cold load shows Overview only.
- About and Data Collection now use the same primary-screen router.
- `.hidden` remains enforced with `!important`.
- Cognitive, Tapping and Memory instruction gates remain in place.
- Completed-test return architecture remains in place.

Validation:
- JavaScript syntax: PASS
- Duplicate HTML IDs: PASS
- Browser UI assertions: 27/27 PASS across desktop, iPad-size and mobile-size Chromium viewports
- Cold load, Data Collection, all three instruction screens and all three START transitions passed.

Scientific protocols and scoring formulas are unchanged.
