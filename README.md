# Open-Source Audio Multimodals

Collection of open-source multimodal models with audio support, focusing on models that can process audio tokens and understand them in conjunction with text prompts.

## Overview

This repository catalogs and analyzes a relatively small but significant subclassification of multimodal models: those with native audio support. As of December 7, 2025, these models are classified on Hugging Face under the "multimodal" category rather than the "audio" category—an interesting distinction that reflects their fundamentally different architecture from traditional ASR models.

## Why Audio Multimodal Matters

### Classic STT vs. Audio Multimodal

The audio category on Hugging Face includes ASR (Automatic Speech Recognition) models like Whisper, Parakeet, and Wav2Vec, along with supporting components (diarization, VAD, punctuation restoration). These are powerful but follow a traditional pipeline approach.

**Audio multimodal models** are fundamentally different:
- **Native audio understanding**: Process audio tokens directly alongside text prompts
- **Unified inference**: Single API call handles transcription, formatting, and summarization
- **Prompt-guided processing**: Can be instructed to analyze accents, describe voices, or format output

### Practical Advantages

Instead of chaining: `Whisper → GPT-4 → Formatting`

Audio multimodal enables: `Single API call with system prompt → Formatted output`

**Use cases:**
- Voice journals with structured formatting
- Conference call summarization
- Accent/voice analysis
- Long-form audio processing (tested with 1-hour recordings)

## Repository Contents

### Data

- **CSV/JSON exports** from Hugging Face API
- **Model metadata** including parameter counts (essential for local deployment planning)
- Both raw and processed datasets

### Examples (Open Source Only)

- Qwen2 Audio 7B (+ instruct version, GGUF quantizations)
 
## Future of Voice AI

Audio multimodal represents what may be the successor to first-wave STT models. The ability to handle transcription, cleanup, and formatting in a single unified inference process—without the complexity of VAD, punctuation restoration, and post-processing chains—makes this an elegant and powerful approach to voice AI.

## Updates

This repository will be periodically updated as the field evolves. Given the rapid pace of AI development, timestamps are included throughout.

---

*Created: December 7, 2025*
