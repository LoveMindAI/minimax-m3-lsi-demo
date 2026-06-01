# MiniMax M3 Synthetic Character LSI Packet

Built: 2026-05-31. Expanded: 2026-06-01.

This is a public-safe toy packet for MiniMax M3 and several rival models. It uses three fictional, name-first characters from the earlier LocalLLaMA-facing demo: Cillian Frost, Haruki Minamoto, and Roxy Saint-Clair. No real PARSEL participant profiles, PIDs, rows, or narratives are included.

The fictional characters were created for public inspection. We started with names, used Opus and Gemini to generate toy facts, reverse-coded the resulting name-and-fact skeletons with multiple model raters into dense toy psychometric targets, then asked each generator to transform those targets into conditioning portraits and 24-section Life Story Interviews. The actual research benchmark uses research-only real participant profiles and life facts, so those source materials stay private.

## What Changed

- Re-generated the two synthetic conditioning portraits for each character with MiniMax M3: psychometric-only and interwoven-biography.
- Generated matching 24-section fictional LSIs with MiniMax M3.
- Kept the earlier Gemma 4 31B and Opus 4.6 synthetic outputs beside the MiniMax versions for quick side-by-side reading.
- Scored the synthetic outputs against the public synthetic name/fact targets using Sonnet 4.6, Gemini 3 Flash, Grok 4.20, and MiniMax M3.
- Added aggregate-only MiniMax M3 benchmark tables from the separate 50-person internal benchmark.
- Added rival synthetic outputs from MiniMax M2.7, GLM 5.1, MiMo v2.5 Pro, Kimi K2.6, and Qwen 3.7 Max, scored with Gemini 3 Flash.
- Added aggregate-only expanded OpenRouter benchmark tables for the same rival set. MiniMax M3 scoring was smoke-tested but too slow for the first public drop, so the comparable expanded rows use Gemini 3 Flash scoring.

## Quick Read

On these synthetic characters, MiniMax M3 profile recovery against the synthetic name/fact targets lands at HEXACO r = 0.930 to 0.971. Its generated LSIs land at HEXACO r = 0.886 to 0.977. Treat these as toy-readability checks, not paper evidence.

The aggregate 50-person benchmark is included only as summary tables. In that benchmark, MiniMax M3 profiles scored strongly under Gemini 3 Flash (HEXACO r = 0.880 to 0.884), while MiniMax-generated 4-part LSIs were below the Gemini/Gemma/GPT/Qwen headline band (HEXACO r = 0.632 to 0.636 under Gemini scoring).

In the expanded OpenRouter 50-person benchmark, GLM 5.1 was the strongest added rival on 4-part LSI transfer under Gemini scoring (HEXACO r = 0.748 to 0.751). Qwen 3.7 Max and Kimi K2.6 were next. MiniMax M2.7 landed slightly above MiniMax M3 on 4-part LSI transfer, while MiMo v2.5 Pro was strong on synthetic-character readability but weaker on the real aggregate transfer slice.

## Folder Map

- `side_by_side_profiles/`: Gemma 4 31B, Opus 4.6, and MiniMax M3 profiles beside each other.
- `side_by_side_lsis/`: matching full LSI transcripts beside each other.
- `minimax_profiles/`: MiniMax M3 profile outputs only.
- `minimax_lsi_transcripts/`: MiniMax M3 LSI outputs only.
- `original_reference_profiles/` and `original_reference_lsis/`: the earlier synthetic reference outputs.
- `tables/synthetic_character_profile_recovery.tsv`: consensus recovery for profile outputs.
- `tables/synthetic_character_lsi_recovery.tsv`: consensus recovery for LSI outputs.
- `tables/synthetic_character_scores_by_scorer.tsv`: per-scorer synthetic recovery.
- `rival_models_20260601/`: rival model profiles, LSIs, and side-by-side Markdown readers.
- `tables/rival_synthetic_character_profile_recovery_20260601.tsv`: public synthetic profile recovery for the rival set.
- `tables/rival_synthetic_character_lsi_recovery_20260601.tsv`: public synthetic LSI recovery for the rival set.
- `tables/expanded_openrouter_benchmark_digest_20260601.md`: human-readable aggregate digest for the expanded 50-person OpenRouter benchmark.
- `tables/expanded_openrouter_benchmark_summary_20260601.tsv`: aggregate-only rows for the expanded 50-person OpenRouter benchmark.
- `tables/expanded_generation_behavior_correlations_public_20260601.tsv`: exploratory public-safe generation-behaviour correlations.
- `tables/canonical_4part_generator_comparison_with_minimax.tsv`: aggregate 4-part generator comparison, public-safe.
- `tables/minimax_m3_50pid_aggregate_only.tsv`: aggregate MiniMax M3 benchmark rows only.

## Guardrails

This packet is for public readability and model-comparison discussion. The fictional character rows are not evidence for the LSI paper. The 50-person benchmark tables are aggregate-only; individual rows and all real source materials are intentionally excluded.

Provider note: Kimi K2.6 worked cleanly on OpenRouter with `reasoning.effort=none`. MiniMax M2.7 needed MiniMax's `reasoning_split` flag for generation; without it, one synthetic profile call spent the full budget on hidden reasoning and returned no final prose.
