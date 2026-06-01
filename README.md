# MiniMax M3 Life Story Interview Demo

This repo is a public-safe MiniMax M3 and rival-model demo for the LoveMind Life Story Interview pipeline.

It is intentionally separate from the COLM reviewer materials repo. This one is for model readers, r/LocalLLaMA people, and anyone curious about how a newly released model handles synthetic psychometric-to-narrative generation.

## Start Here

- [Pretty reader](./index.html)
- [MiniMax M3 public packet](./packets/minimax_m3_public_packet/README.md)
- [MiniMax M3 Roxy side-by-side profile](./packets/minimax_m3_public_packet/side_by_side_profiles/roxy_saint_clair__interwoven_bio.md)
- [MiniMax M3 Roxy side-by-side LSI](./packets/minimax_m3_public_packet/side_by_side_lsis/roxy_saint_clair__interwoven_bio.md)
- [Rival Roxy profile side-by-side](./packets/minimax_m3_public_packet/rival_models_20260601/side_by_side_profiles/roxy_saint_clair__interwoven_bio.md)
- [Rival Roxy LSI side-by-side](./packets/minimax_m3_public_packet/rival_models_20260601/side_by_side_lsis/roxy_saint_clair__interwoven_bio.md)
- [Expanded OpenRouter benchmark digest](./packets/minimax_m3_public_packet/tables/expanded_openrouter_benchmark_digest_20260601.md)
- [Downloadable packet zip](./downloads/minimax_m3_character_public_packet_20260531.zip)

## What Is Included

- MiniMax M3 regenerated synthetic profiles and 24-section LSIs for three fictional characters: Roxy Saint-Clair, Cillian Frost, and Haruki Minamoto.
- Earlier Gemma 4 31B and Opus 4.6 synthetic outputs for side-by-side comparison.
- Rival synthetic profiles and LSIs from MiniMax M2.7, GLM 5.1, MiMo v2.5 Pro, Kimi K2.6, and Qwen 3.7 Max.
- Aggregate-only benchmark tables from a separate 50-person internal benchmark. No participant-level rows, real profiles, raw PIDs, or private narratives are included.
- Extra synthetic reference packets from earlier public demos, including Bud, Isolde, and Megyn variants.

## How The Synthetic Characters Were Made

The public examples start from fictional names, not real people. Opus and Gemini helped generate toy facts from names such as Roxy Saint-Clair, Cillian Frost, and Haruki Minamoto. Multiple model raters then reverse-coded those name-and-fact skeletons into dense toy psychometric targets. Finally, the tested models transformed those toy targets into conditioning portraits and 24-section Life Story Interviews.

The actual benchmark uses research-only psychometric profiles and life facts from real participants. Those materials are not public, so the fictional characters are a readable, non-private way to inspect model behaviour without exposing participant data.

## What The First Pass Suggests

MiniMax M3 writes unusually clean fictional life-story prose in this format. It also produces synthetic character profiles and LSIs that remain highly recoverable against the toy synthetic targets.

The more serious 50-person aggregate benchmark is mixed: MiniMax M3 profile generation scores strongly, but MiniMax-generated 4-part LSIs recover less psychometric signal than the current comparison band.

The expanded OpenRouter shootout was more interesting than expected. GLM 5.1 led the added rival set on 4-part LSI transfer under Gemini scoring at HEXACO r = 0.748 to 0.751. Qwen 3.7 Max and Kimi K2.6 were respectable. MiniMax M2.7 slightly beat MiniMax M3 on the 50-person LSI transfer slice, while MiMo v2.5 Pro looked strong on public synthetic characters but weaker on the real aggregate transfer benchmark.

That makes MiniMax M3 interesting rather than solved: great prose, strong profile encoding, and a weaker first LSI transfer than the best current lanes.

## Guardrails

The synthetic character rows are for public reading and model-comparison discussion only. They are not evidence for the paper.

The aggregate benchmark tables are public-safe summaries only. Individual participant rows and source materials are intentionally excluded.

MiniMax M3 and the added rivals were run as exploratory benchmarks. Treat these as first-pass results, not final verdicts on the models.

OpenRouter note: Kimi K2.6 worked cleanly with `reasoning.effort=none`. MiniMax M2.7 needed MiniMax's `reasoning_split` flag during generation; otherwise one synthetic profile call spent its whole budget in hidden reasoning and returned no final prose.
