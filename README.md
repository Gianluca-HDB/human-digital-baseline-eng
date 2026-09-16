# HDB v6.2.1 — Navigation bugfix

Fixes the issue visible on iPad where tapping Cognitive test, Tapping test or Memory check left the Data Collection/Overview screen visible instead of opening the new instruction screen.

Cause:
- the screen-hiding helper targeted `body > section`
- HDB's primary screens are actually direct children of `.card`
- therefore the current screen was not being hidden before the instruction screen was revealed

Fix:
- primary screen navigation now targets `.card > section`
- pre-test instruction screens open correctly
- START launches the selected test
- after a completed test is saved, HDB returns directly to Data Collection
- deterministic top-of-page positioning added for iPad/Safari

No cognitive, tapping, memory, baseline, Motor Pattern Score or neurodegenerative scoring protocol was changed.
