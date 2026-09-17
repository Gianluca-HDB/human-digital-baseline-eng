# HDB v6.7 — Research Integrity

Changes:
- Raw tapping timestamps and available pointer-pressure arrays are preserved inside every new historical tapping record.
- Raw Cognitive and Memory trial arrays are also copied into their historical session records.
- Reproducible Research Dataset JSON export separates raw observations, derived metrics, protocol IDs, metadata and contextual logs.
- Session metadata includes app version, timestamp/time band/timezone, browser/platform/language, screen/viewport/pixel ratio, touch capability, orientation and other exposed technical context.
- Tapping 2.2 now uses: pre-test instructions -> explicit START RIGHT/LEFT HAND -> fixed 3–2–1 countdown -> automatic 15 s acquisition beginning at GO.
- START/countdown touches are not recorded as taps.
- Because v6.7 starts the acquisition window at GO while older tapping versions started timing on the first tap, v6.7 tapping baseline/scoring uses only v6.7-compatible tapping observations. Older observations are preserved in storage and exports but are not pooled into the new tapping baseline.
- Motor Pattern Score weights remain 35/20/20/10/10/5 and scoring never rewrites raw observations.

QA:
Final browser logic audit passed on desktop, iPad-size and mobile-size Chromium viewports, including START/countdown behavior, raw-history persistence, metadata, reproducible export availability, and protocol-compatibility separation. The sandbox test uses an in-memory localStorage shim; do a final manual GitHub Pages/iPad Safari persistence smoke test before formal data collection.
