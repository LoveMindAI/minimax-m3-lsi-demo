# MiniMax M3 Life Story Interview Demo

This repo is a public-safe MiniMax M3 demo for the LoveMind Life Story Interview pipeline.

It is intentionally separate from the COLM reviewer materials repo. This one is for model readers, r/LocalLLaMA people, and anyone curious about how a newly released model handles synthetic psychometric-to-narrative generation.

## Start Here

- [Pretty reader](./index.html)
- [MiniMax M3 public packet](./packets/minimax_m3_public_packet/README.md)
- [Roxy side-by-side profile](./packets/minimax_m3_public_packet/side_by_side_profiles/roxy_saint_clair__interwoven_bio.md)
- [Roxy side-by-side LSI](./packets/minimax_m3_public_packet/side_by_side_lsis/roxy_saint_clair__interwoven_bio.md)
- [Downloadable packet zip](./downloads/minimax_m3_character_public_packet_20260531.zip)

## What Is Included

- MiniMax M3 regenerated synthetic profiles and 24-section LSIs for three fictional characters: Roxy Saint-Clair, Cillian Frost, and Haruki Minamoto.
- Earlier Gemma 4 31B and Opus 4.6 synthetic outputs for side-by-side comparison.
- Aggregate-only benchmark tables from a separate 50-person internal benchmark. No participant-level rows, real profiles, raw PIDs, or private narratives are included.
- Extra synthetic reference packets from earlier public demos, including Bud, Isolde, and Megyn variants.

## What The First Pass Suggests

MiniMax M3 writes unusually clean fictional life-story prose in this format. It also produces synthetic character profiles and LSIs that remain highly recoverable against the toy synthetic targets.

The more serious 50-person aggregate benchmark is mixed: MiniMax M3 profile generation scores strongly, but MiniMax-generated 4-part LSIs recover less psychometric signal than the current Gemini/Gemma/GPT/Qwen comparison band.

That makes the model interesting rather than solved. Great prose, strong profile encoding, and a weaker first LSI transfer than the best current lanes.

## Guardrails

The synthetic character rows are for public reading and model-comparison discussion only. They are not evidence for the paper.

The aggregate benchmark tables are public-safe summaries only. Individual participant rows and source materials are intentionally excluded.

MiniMax M3 was run as a new-model exploratory benchmark. Treat these as first-pass results, not a final verdict on the model.
