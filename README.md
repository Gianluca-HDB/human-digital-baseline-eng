# HDB v6.7.4 — Metric Explorer Test Separation

UI-only integrity patch.

Metric Explorer now separates the three test families:
- Cognitive test
- Tapping test
- Memory check

This does NOT change the analytical multidomain labels used elsewhere:
- Cognition remains Cognition
- tapping metrics remain Motor
- memory metrics remain Memory

No raw data, baseline calculation, 10-observation readiness rule, 7+3 design,
persistence rule, test protocol, or Motor Pattern Score formula/weights changed.

Baseline algorithm remains:
HDB-BASELINE:v6.7.3-dual-adaptive-exclude3-initial7-min10
