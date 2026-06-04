# Life Story Model Specimens public packet - 2026-06-04

This packet supports the public GitHub Pages reader in this repo. It is public-safe: no participant-level PARSEL rows, PIDs, raw profiles, biographical facts, conversation text, or generated participant narratives are included.

## Tables

- `tables/full_n290_profile_and_lsi_digest.tsv`: full 290-person aggregate digest for Gemma 4 31B and Gemma 4 12B where complete runs exist.
- `tables/openrouter_50pid_interwoven_digest.tsv`: public-safe 50-PID exploratory slice for MiniMax M3 and nearby OpenRouter rivals, using Gemini 3 Flash as scorer.
- Synthetic character recovery tables copied from the earlier MiniMax M3 packet and the Gemma 4 12B public-safe sandbox.

## Synthetic Characters

The fictional examples use names and invented facts only. They are included so readers can inspect prose without exposing research participants.

Gemma 4 12B public-safe synthetic artifacts are under `synthetic_characters/gemma4_12b_public_safe/`. The older MiniMax M3, Gemma 4 31B, Opus 4.6, and rival-model artifacts remain in `../minimax_m3_public_packet/`.

## Metric Denominators

- `HEXACO6`: mean correlation across the six HEXACO domain targets.
- `Beyond10`: mean correlation across ten additional continuous targets in the public scoring set.
- `Continuous16`: mean correlation across HEXACO6 + Beyond10.
- `SVO`: correlation on the Social Value Orientation angle target, reported separately.

All public tables are aggregate-only.
