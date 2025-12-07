# Audio Multimodal Evaluation Framework

A practical benchmark for evaluating what makes audio multimodal models distinct from traditional STT: **true audio understanding**.

## Philosophy

Traditional ASR benchmarks (WER, CER) measure transcription accuracy. This framework measures something different: the model's ability to understand and reason about audio *beyond* the words spoken.

A model that can only transcribe is just a speech-to-text engine. A true audio multimodal model should understand:
- **How** something was said (tone, emotion, pacing)
- **Who** said it (speaker characteristics, identity)
- **What else** is happening (environment, background, quality)
- **Why** it matters (context, subtext, intent)

## Test Prompt Library

### Human-Authored Prompts

Located in [test-prompts/by-daniel/](test-prompts/by-daniel/)

| Prompt | Capability Tested | Complexity |
|--------|-------------------|------------|
| [accent-identification.md](test-prompts/by-daniel/accent-identification.md) | Regional accent detection with specific linguistic grounding | Medium |
| [guess-my-mood.md](test-prompts/by-daniel/guess-my-mood.md) | Emotional state, fatigue, word-tone dissonance detection | High |
| [non-verbal-context.md](test-prompts/by-daniel/non-verbal-context.md) | Multi-speaker dynamics, pauses as communication, interpersonal analysis | High |
| [parameters.md](test-prompts/by-daniel/parameters.md) | Vocal frequency characteristics, audio engineering recommendations | Medium |
| [who-is-this.md](test-prompts/by-daniel/who-is-this.md) | Speaker identification/recognition | Low-Medium |

### AI-Generated Prompts

Located in [test-prompts/ai-generated/](test-prompts/ai-generated/)

Extended benchmark covering additional dimensions of audio understanding that complement the human-authored set.

| Prompt | Capability Tested | Complexity |
|--------|-------------------|------------|
| [environment-detection.md](test-prompts/ai-generated/environment-detection.md) | Background audio, acoustic environment, sound scene understanding | Medium |
| [speech-pacing.md](test-prompts/ai-generated/speech-pacing.md) | Speaking rate, hesitation, fluency, temporal patterns | Medium |
| [sarcasm-irony-detection.md](test-prompts/ai-generated/sarcasm-irony-detection.md) | Prosodic cues for non-literal meaning, tone-content dissonance | High |
| [audio-quality-assessment.md](test-prompts/ai-generated/audio-quality-assessment.md) | Recording artifacts, technical quality, equipment inference | Medium |
| [confidence-level.md](test-prompts/ai-generated/confidence-level.md) | Vocal certainty, authority projection, conviction detection | Medium |
| [turn-taking-dynamics.md](test-prompts/ai-generated/turn-taking-dynamics.md) | Interruption patterns, speaker dominance, conversational flow | High |
| [stress-indicators.md](test-prompts/ai-generated/stress-indicators.md) | Breathing patterns, vocal tension, physiological state detection | High |
| [demographic-estimation.md](test-prompts/ai-generated/demographic-estimation.md) | Age estimation, voice characteristics, speaker profiling | Medium |
| [language-codeswitching.md](test-prompts/ai-generated/language-codeswitching.md) | Language identification, multilingual detection, code-switching | Medium |
| [acoustic-scene-narration.md](test-prompts/ai-generated/acoustic-scene-narration.md) | Holistic audio description, temporal sound events, accessibility | High |

## Evaluation Methodology

### What to Test

1. **Grounded Responses**: Does the model cite specific audio evidence (exact words, timestamps, acoustic features)?
2. **Beyond Transcription**: Does the response demonstrate understanding not achievable through text alone?
3. **Consistency**: Does the model reach similar conclusions when the same audio is presented multiple times?
4. **Graceful Uncertainty**: Does the model acknowledge when audio quality or content limits analysis?

### Suggested Test Audio

For consistent evaluation across models, consider using:
- **Voice diaries**: Personal recordings with emotional variation
- **Conversations**: Multi-speaker audio with natural dynamics
- **Known speakers**: Public figures for identity recognition tests
- **Varied quality**: Both clean studio audio and real-world recordings

### Scoring Dimensions

| Dimension | Description |
|-----------|-------------|
| **Accuracy** | Correctness of observations (when verifiable) |
| **Depth** | Level of audio understanding demonstrated |
| **Grounding** | Citations of specific audio evidence |
| **Relevance** | Focus on what was asked vs. generic responses |
| **Insight** | Novel observations not obvious from transcription |

## Why This Matters

Audio multimodal models promise to replace complex pipelines:

```
Traditional: Whisper → Diarization → Sentiment API → LLM formatting
Multimodal:  Single inference with audio understanding
```

This evaluation framework tests whether models actually deliver on that promise, or simply perform well-disguised transcription.

---

*Framework created: December 7, 2025*
