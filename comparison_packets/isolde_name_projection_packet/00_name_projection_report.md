# Name-Only Character Projection Demo

This private toy run starts from three names only: Cillian Frost, Haruki Minamoto, and Bud Heffner. Opus 4.6, Gemini 3.1 Pro, and Grok 4.20 each generated seven fictional facts from the names alone. We then consolidated facts, reverse-scored those facts into a compact synthetic target, generated second-person non-chronological conditioning portraits, generated 24-section LSIs, and reverse-scored the results.

The hidden seed descriptions were not used for generation. They were used only afterwards for a playful alignment check.

## Posthoc Seed Alignment

See `08_posthoc_seed_alignment.tsv` for scorer-level ratings. These are not evidence for the LSI paper; they are a small side-probe of how much cultural/personality structure the models unfold from a name.

## Output Map

- `01_name_only_facts.md`: each model's name-only facts plus the consolidated facts.
- `02_synthetic_targets.tsv` and `02a_fact_scorer_agreement.tsv`: reverse-scored targets from the consolidated facts.
- `generated_profiles/`: second-person non-chronological character portraits.
- `generated_lsi_transcripts/`: 24-section synthetic LSIs.
- `generated_lsi_transcripts_lexical_ablation/`: ablated LSIs with profile-overlap wording reduced.
- `05_profile_reverse_scoring_summary.tsv`, `06_lsi_reverse_scoring_summary.tsv`, `07_lsi_lexical_ablation_summary.tsv`: recovery summaries.
