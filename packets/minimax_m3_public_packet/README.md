# MiniMax M3 Synthetic Character LSI Packet

Built: 2026-05-31

This is a public-safe toy packet for MiniMax M3. It uses three fictional, name-only characters from the earlier LocalLLaMA-facing demo: Cillian Frost, Haruki Minamoto, and Roxy Saint-Clair. No real PARSEL participant profiles, PIDs, rows, or narratives are included.

## What Changed

- Re-generated the two synthetic conditioning portraits for each character with MiniMax M3: psychometric-only and interwoven-biography.
- Generated matching 24-section fictional LSIs with MiniMax M3.
- Kept the earlier Gemma 4 31B and Opus 4.6 synthetic outputs beside the MiniMax versions for quick side-by-side reading.
- Scored the synthetic outputs against the public synthetic name/fact targets using Sonnet 4.6, Gemini 3 Flash, Grok 4.20, and MiniMax M3.
- Added aggregate-only MiniMax M3 benchmark tables from the separate 50-person internal benchmark.

## Quick Read

On these synthetic characters, MiniMax M3 profile recovery against the synthetic name/fact targets lands at HEXACO r = 0.930 to 0.971. Its generated LSIs land at HEXACO r = 0.886 to 0.977. Treat these as toy-readability checks, not paper evidence.

The aggregate 50-person benchmark is included only as summary tables. In that benchmark, MiniMax M3 profiles scored strongly under Gemini 3 Flash (HEXACO r = 0.880 to 0.884), while MiniMax-generated 4-part LSIs were below the Gemini/Gemma/GPT/Qwen headline band (HEXACO r = 0.632 to 0.636 under Gemini scoring).

## Folder Map

- `side_by_side_profiles/`: Gemma 4 31B, Opus 4.6, and MiniMax M3 profiles beside each other.
- `side_by_side_lsis/`: matching full LSI transcripts beside each other.
- `minimax_profiles/`: MiniMax M3 profile outputs only.
- `minimax_lsi_transcripts/`: MiniMax M3 LSI outputs only.
- `original_reference_profiles/` and `original_reference_lsis/`: the earlier synthetic reference outputs.
- `tables/synthetic_character_profile_recovery.tsv`: consensus recovery for profile outputs.
- `tables/synthetic_character_lsi_recovery.tsv`: consensus recovery for LSI outputs.
- `tables/synthetic_character_scores_by_scorer.tsv`: per-scorer synthetic recovery.
- `tables/canonical_4part_generator_comparison_with_minimax.tsv`: aggregate 4-part generator comparison, public-safe.
- `tables/minimax_m3_50pid_aggregate_only.tsv`: aggregate MiniMax M3 benchmark rows only.

## Guardrails

This packet is for public readability and model-comparison discussion. The fictional character rows are not evidence for the LSI paper. The 50-person benchmark tables are aggregate-only; individual rows and all real source materials are intentionally excluded.
