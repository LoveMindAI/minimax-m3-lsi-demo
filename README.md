# Trait-to-Life-Story Benchmark

Model specimens from the LoveMind Life Story Interview pipeline, centered on Gemma 4 31B, Gemma 4 12B, and MiniMax M3.

This repo began as a MiniMax M3 public demo. It is now a broader reader and aggregate benchmark packet for newly released models tested on a loose public spin-off of our paper, [Stories of Your Life as Others](https://arxiv.org/abs/2604.06071).

The real benchmark draws on PARSEL, the multimodal partner-selection dataset introduced by Tiffany Matej Hrkalovic, Bernd Dudzik, Daniel Balliet, and Hayley Hung. Tiffany Matej Hrkalovic is also the anchor author of Stories of Your Life as Others.

## Start Here

- [LoveMind AI](https://lovemind.ai)
- [Landing page](./index.html)
- [PARSEL paper](https://research.vu.nl/ws/portalfiles/portal/463222040/PARSEL_A_Multimodal_Dataset_for_Modeling_Decision-Making_Processes_Involved_in_Selecting_Partners_for_Joint_Tasks.pdf)
- [New public packet](./packets/life_story_model_specimens_20260604/README.md)
- [Full N=290 aggregate table](./packets/life_story_model_specimens_20260604/tables/full_n290_profile_and_lsi_digest.tsv)
- [50-PID OpenRouter exploratory table](./packets/life_story_model_specimens_20260604/tables/openrouter_50pid_interwoven_digest.tsv)

## What Is Included

- Aggregate-only recovery tables for profile generation and 4-part interwoven Life Story Interviews.
- Full 290-person aggregate rows where complete runs exist, including Gemma 4 31B and Gemma 4 12B.
- A separate 50-PID exploratory comparison slice for MiniMax M3 and nearby OpenRouter rivals.
- Fictional synthetic character examples for Roxy Saint-Clair, Cillian Frost, and Haruki Minamoto.
- Gemma 4 12B synthetic character profiles and LSIs copied into the new packet.
- Earlier Gemma 4 31B, Opus 4.6, MiniMax M3, and rival synthetic examples retained for side-by-side reading.

## What Is Not Included

PARSEL is a research-only dataset containing real participants' psychometric profiles, basic biographical facts, and short conversational materials. Those participant-level materials are not public.

This repo does not include participant rows, PIDs, raw psychometric profiles, private biographical facts, real conversation text, or generated narratives tied to real participants. The benchmark tables are aggregate-only. The readable examples use fictional characters.

## How The Synthetic Characters Were Made

The public examples start from fictional names, not real people. Opus and Gemini helped generate toy facts from names such as Roxy Saint-Clair, Cillian Frost, and Haruki Minamoto. Multiple model raters then reverse-coded those name-and-fact skeletons into dense toy psychometric targets. Finally, the tested models transformed those toy targets into conditioning profiles and Life Story Interview narratives.

The actual benchmark uses research-only psychometric profiles and life facts from 290 real PARSEL participants. The fictional characters are a readable substitute for prose inspection, not paper evidence.

## Metric Denominators

- `HEXACO6`: mean correlation across the six HEXACO domain targets.
- `Beyond10`: mean correlation across ten additional continuous targets in the public scoring set.
- `Continuous16`: mean correlation across `HEXACO6` plus `Beyond10`.
- `SVO`: Social Value Orientation angle, reported separately.

All public benchmark values are aggregate correlations, not individual predictions.

## Guardrails

These are first-pass exploratory model specimens, not a formal public leaderboard. The full paper and rebuttal analyses use stricter private pipelines, additional controls, and participant-protection constraints that are not reproduced here.
