# CLAUDE.md - Open-Source Audio Multimodals

## Project Purpose

This repository is an analysis and data-gathering project for **multimodal models with audio support**—a small but significant subclassification of AI models. The focus is on models that can process audio tokens natively and understand them in conjunction with text prompts.

## Key Concepts

### Audio Multimodal vs Traditional STT

**Traditional STT (e.g., Whisper):**
- Converts speech to text
- Requires post-processing chain for formatting, punctuation, summarization
- Pipeline: STT → VAD → Punctuation restoration → LLM for formatting

**Audio Multimodal:**
- Processes audio tokens with native understanding
- Accepts text prompts to guide output
- Single unified inference for transcription + formatting + analysis
- Example: Gemini 2/2.5/3 audio modality

### Why This Matters

1. **Simplified engineering**: No need to chain multiple models
2. **Prompt-guided transcription**: Can format output, summarize, detect accents, describe voice characteristics
3. **Long-form support**: Tested with 1-hour recordings on Gemini 3
4. **Unified endpoint**: Single API call replaces complex pipelines

## Repository Structure

```
/
├── repo-plan/              # Planning notes and transcripts
├── data/                   # CSV/JSON exports from Hugging Face
│   ├── raw/                # Direct API exports
│   └── processed/          # Cleaned/analyzed data
└── analysis/               # Findings and comparisons
```

## Data Sources

- **Hugging Face API**: Multimodal category models with audio support
- **Model metadata**: Parameter counts, quantization variants
- Current count: ~151 models (vs ~2,500 ASR models on HF)

## Working With This Repo

### Analysis Goals

1. Identify unique base models (filter out quantizations/variants)
2. Catalog parameter sizes for local deployment planning
3. Find candidates for local transcription workflows
4. Track the evolution of this model category

### Notable Models to Investigate

- Qwen2 Audio 7B (instruct version, GGUF available)
- Step Audio with LLaMA 3.2
- Long-tail models from emerging developers (e.g., Soundwave)

## Context

This category is classified under "multimodal" on Hugging Face, not "audio"—reflecting that these are fundamentally different from ASR models. The audio aspect of multimodal has received less attention than vision/image modalities, making this a less-explored but promising area.

## Updates

The field moves quickly—timestamps are important. This repository will be periodically updated as new models emerge and analysis progresses.

*Created: December 7, 2025*
