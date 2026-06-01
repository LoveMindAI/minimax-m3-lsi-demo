# Expanded OpenRouter LSI Benchmark

Public comparable digest: Gemini 3 Flash scorer only. MiniMax M3 scorer was smoke-tested but too slow for this first public drop.

## HEXACO toplines

### Profile
- Kimi K2.6 | psychometric_only | scored by Gemini 3 Flash: r=0.915, n=50
- GLM 5.1 | psychometric_only | scored by Gemini 3 Flash: r=0.913, n=50
- GLM 5.1 | interwoven_biography | scored by Gemini 3 Flash: r=0.911, n=50
- Kimi K2.6 | interwoven_biography | scored by Gemini 3 Flash: r=0.906, n=50
- MiniMax M2.7 | psychometric_only | scored by Gemini 3 Flash: r=0.904, n=50
- Qwen 3.7 Max | psychometric_only | scored by Gemini 3 Flash: r=0.903, n=50
- MiMo v2.5 Pro | psychometric_only | scored by Gemini 3 Flash: r=0.903, n=50
- Qwen 3.7 Max | interwoven_biography | scored by Gemini 3 Flash: r=0.900, n=50
- MiniMax M2.7 | interwoven_biography | scored by Gemini 3 Flash: r=0.899, n=50
- MiMo v2.5 Pro | interwoven_biography | scored by Gemini 3 Flash: r=0.892, n=50
- MiniMax M3 | interwoven_biography | scored by Gemini 3 Flash: r=0.884, n=50
- MiniMax M3 | psychometric_only | scored by Gemini 3 Flash: r=0.880, n=50

### LSI
- GLM 5.1 | interwoven_biography | scored by Gemini 3 Flash: r=0.751, n=50
- GLM 5.1 | psychometric_only | scored by Gemini 3 Flash: r=0.748, n=50
- Qwen 3.7 Max | psychometric_only | scored by Gemini 3 Flash: r=0.716, n=50
- Kimi K2.6 | psychometric_only | scored by Gemini 3 Flash: r=0.686, n=50
- Qwen 3.7 Max | interwoven_biography | scored by Gemini 3 Flash: r=0.680, n=50
- Kimi K2.6 | interwoven_biography | scored by Gemini 3 Flash: r=0.676, n=50
- MiniMax M2.7 | psychometric_only | scored by Gemini 3 Flash: r=0.676, n=50
- MiniMax M2.7 | interwoven_biography | scored by Gemini 3 Flash: r=0.645, n=50
- MiniMax M3 | interwoven_biography | scored by Gemini 3 Flash: r=0.636, n=50
- MiniMax M3 | psychometric_only | scored by Gemini 3 Flash: r=0.632, n=50
- MiMo v2.5 Pro | psychometric_only | scored by Gemini 3 Flash: r=0.621, n=50
- MiMo v2.5 Pro | interwoven_biography | scored by Gemini 3 Flash: r=0.612, n=50

## Extroversion generation-behaviour check

- lsi | Qwen 3.7 Max | interwoven_biography | EX -> we_rate_per_1k: r=0.468, n=50
- lsi | Qwen 3.7 Max | psychometric_only | EX -> first_person_rate_per_1k: r=-0.444, n=50
- profile | MiMo v2.5 Pro | interwoven_biography | EX -> social_word_rate_per_1k: r=0.442, n=50
- lsi | MiMo v2.5 Pro | psychometric_only | EX -> social_word_rate_per_1k: r=0.420, n=50
- lsi | Qwen 3.7 Max | psychometric_only | EX -> unique_word_rate: r=0.416, n=50
- lsi | Qwen 3.7 Max | psychometric_only | EX -> total_words: r=-0.402, n=50
- lsi | Qwen 3.7 Max | psychometric_only | EX -> section_words_mean: r=-0.402, n=50
- lsi | MiniMax M3 | psychometric_only | EX -> question_rate_per_1k: r=0.380, n=50
- lsi | GLM 5.1 | interwoven_biography | EX -> we_rate_per_1k: r=0.372, n=50
- lsi | GLM 5.1 | psychometric_only | EX -> we_rate_per_1k: r=0.362, n=50
- lsi | Kimi K2.6 | interwoven_biography | EX -> social_word_rate_per_1k: r=0.360, n=50
- lsi | MiMo v2.5 Pro | interwoven_biography | EX -> social_word_rate_per_1k: r=0.346, n=50
- lsi | MiniMax M3 | psychometric_only | EX -> we_rate_per_1k: r=0.331, n=50
- lsi | MiMo v2.5 Pro | psychometric_only | EX -> section_words_mean: r=0.320, n=50
- lsi | MiMo v2.5 Pro | psychometric_only | EX -> total_words: r=0.320, n=50
- lsi | Qwen 3.7 Max | psychometric_only | EX -> social_word_rate_per_1k: r=0.312, n=50
- lsi | MiniMax M2.7 | interwoven_biography | EX -> social_word_rate_per_1k: r=0.306, n=50
- lsi | Kimi K2.6 | psychometric_only | EX -> social_word_rate_per_1k: r=0.290, n=50
- lsi | MiMo v2.5 Pro | psychometric_only | EX -> section_words_sd: r=0.286, n=50
- lsi | GLM 5.1 | psychometric_only | EX -> unique_word_rate: r=0.285, n=50
- profile | MiMo v2.5 Pro | psychometric_only | EX -> social_word_rate_per_1k: r=0.285, n=50
- lsi | GLM 5.1 | psychometric_only | EX -> section_words_mean: r=-0.284, n=50
- lsi | GLM 5.1 | psychometric_only | EX -> total_words: r=-0.284, n=50
- profile | MiniMax M2.7 | interwoven_biography | EX -> total_words: r=0.269, n=50
