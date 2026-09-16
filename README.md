# HDB v6.3 — Baseline readiness transparency

HDB now replaces unexplained empty baseline-derived fields with metric-specific progress.

- Dashboard: Baseline Readiness / Progress by test for Cognitive, Tapping and Memory.
- Each metric displays n/7 valid observations.
- Motor Pattern Score rows display BUILDING n/7 and explain when Change, adverse-z and Component become available.
- Metric Explorer applies the same progress logic to every catalogued metric/domain.
- If >=7 observations exist but robust baseline variability is zero, HDB explicitly reports that it is waiting for measurable baseline variability.

Why 7: five prior observations form the robust baseline and the latest two are reserved for persistence checking.

No scoring formula, threshold, test content or persistence rule changed.
