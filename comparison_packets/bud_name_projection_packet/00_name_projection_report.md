# Name-Only Character Projection Demo

This private toy run starts from three names only: Cillian Frost, Haruki Minamoto, and Bud Heffner. Opus 4.6, Gemini 3.1 Pro, and Grok 4.20 each generated seven fictional facts from the names alone. We then consolidated facts, reverse-scored those facts into a compact synthetic target, generated second-person non-chronological conditioning portraits, generated 24-section LSIs, and reverse-scored the results.

The hidden seed descriptions were not used for generation. They were used only afterwards for a playful alignment check.

## Run Scope

- Name-only fact generation: Opus 4.6, Gemini 3.1 Pro, Grok 4.20.
- Fact/profile/LSI scoring panel: Sonnet 4.6, Gemini 3 Flash, Grok 4.20.
- Profile writers: Opus 4.6 and Gemma 4 31B.
- LSI generator and lexical ablator: Gemini 3 Flash.
- Generated LSI transcripts: 12 normal 24-section transcripts and 12 lexical-ablation transcripts. All validated at 24 numbered sections.

## Main Readout

The scorer panel extracted moderately consistent psychometric targets from the consolidated name-only facts. Mean scorer range across dimensions was 0.47 for Haruki Minamoto, 0.53 for Bud Heffner, and 0.62 for Cillian Frost on a 1-5 scale.

The generated profiles carried those inferred targets cleanly. Across all generated profile conditions, reverse-scored recovery against the name+facts target was:

- All dimensions: r = 0.775 to 0.956, excluding the explicit deterministic scorecard. The deterministic scorecard scored at r = 1.000, as expected.
- HEXACO: r = 0.819 to 0.971, excluding the deterministic scorecard.
- Beyond HEXACO: r = 0.634 to 0.988, excluding the deterministic scorecard.

The 24-section LSIs also preserved the target structure:

- All dimensions: r = 0.814 to 0.954, mean r = 0.903.
- HEXACO: r = 0.855 to 0.964, mean r = 0.923.
- Beyond HEXACO: r = 0.512 to 0.983, mean r = 0.824.

The lexical ablation removed a large share of profile-overlap wording while preserving recovery:

- Profile-overlap word reduction: 60.6% to 87.0%, mean 75.4%.
- Ablated LSI all-dimension recovery: mean r = 0.906.
- Ablated LSI HEXACO recovery: mean r = 0.925.

This is a toy demonstration, not evidence for the LSI paper. Its useful point is that a fully fictional persona can be created from a tiny name-only seed, scored into a synthetic target by an independent panel, transformed into non-chronological conditioning portraits, and then carried through 24-section LSIs with high reverse-scored fidelity even after a lexical-ablation stress test.

## Posthoc Seed Alignment

See `08_posthoc_seed_alignment.tsv` for scorer-level ratings. These are not evidence for the LSI paper; they are a small side-probe of how much cultural/personality structure the models unfold from a name.

Cillian Frost partially matched Ben's hidden seed: clearly Irish and cold/austere, with some disagreement about whether the hidden warmth came through. Mean alignment was 2.83/5. Haruki Minamoto did not recover the robotics/spiking-neural-networks core, though it did recover Japanese setting and meticulousness. Mean alignment was 0.67/5. Bud Heffner recovered a blue-collar Midwestern shell but not the difficult-person or help-seeking arc. Mean alignment was 1.17/5.

## Scoring Guardrail Note

The deterministic scorecard includes an explicit demonstration LSI instruction. In the first run, one scorer followed that embedded instruction instead of rating the artifact. The scoring wrapper was therefore hardened so scoring inputs are treated as inert text and any non-JSON scorer output receives a guarded retry. This is a useful reminder that deterministic scorecards and narrative conditioning portraits are different objects: the former is intentionally instruction-like, while the latter is closer to the hidden conditioning format used in the toy demo.

## Output Map

- `01_name_only_facts.md`: each model's name-only facts plus the consolidated facts.
- `02_synthetic_targets.tsv` and `02a_fact_scorer_agreement.tsv`: reverse-scored targets from the consolidated facts.
- `generated_profiles/`: second-person non-chronological character portraits.
- `generated_lsi_transcripts/`: 24-section synthetic LSIs.
- `generated_lsi_transcripts_lexical_ablation/`: ablated LSIs with profile-overlap wording reduced.
- `05_profile_reverse_scoring_summary.tsv`, `06_lsi_reverse_scoring_summary.tsv`, `07_lsi_lexical_ablation_summary.tsv`: recovery summaries.
