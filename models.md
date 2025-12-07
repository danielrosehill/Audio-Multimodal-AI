# Featured Audio Multimodal Models

*Last updated: December 7, 2025*

This page highlights the most notable open-source and open-weight multimodal models with native audio support. These models process audio tokens directly alongside text prompts, enabling prompt-guided transcription, analysis, and formatting in a single inference pass.

---

## Voxtral

**Developer:** Mistral AI
**Released:** July 2025
**Variants:** Voxtral (24B), Voxtral Mini (3B)
**License:** Apache 2.0

Mistral's frontier open-source speech understanding models. Goes beyond traditional ASR by incorporating semantic understanding and language comprehension. The Mini variant is specifically designed for local and edge deployments.

**Key features:**
- 32k token context window (up to 30 minutes of audio)
- Native multilingual support with automatic language detection
- Built-in Q&A and summarization without separate models
- Direct function-calling triggered by spoken intent
- Retains text understanding from language model backbone

**Links:**
- [Website](https://mistral.ai/news/voxtral)
- [Hugging Face](https://huggingface.co/mistralai)

---

## Qwen2-Audio

**Developer:** Alibaba (Qwen Team)
**Parameters:** 7B
**Variants:** Base, Instruct
**Quantizations:** GGUF available

Currently one of the most practical open-source options for local deployment. The instruct variant is specifically tuned for following transcription and analysis prompts.

**Key features:**
- Strong multilingual support
- Prompt-guided transcription and formatting
- GGUF quantizations enable consumer hardware deployment
- Active community with llama.cpp support

**Links:**
- [Qwen2-Audio-7B](https://huggingface.co/Qwen/Qwen2-Audio-7B)
- [Qwen2-Audio-7B-Instruct](https://huggingface.co/Qwen/Qwen2-Audio-7B-Instruct)

---

## Kimi-Audio

**Developer:** Moonshot AI (Kimi)
**Architecture:** Native audio multimodal

Kimi-Audio extends Moonshot AI's Kimi model family with audio modality support. Part of the growing ecosystem of Chinese AI labs producing competitive open-weight models.

**Key features:**
- Native audio understanding
- Long-context audio processing
- Integrated with Kimi's strong reasoning capabilities

**Links:**
- [GitHub](https://github.com/MoonshotAI/Kimi-Audio)
- [Hugging Face](https://huggingface.co/moonshotai)

---

## Phi-4-Multimodal-Instruct

**Developer:** Microsoft
**Parameters:** ~14B (multimodal variant)
**Architecture:** Phi-4 base with multimodal extensions

Microsoft's Phi-4 multimodal variant includes audio support, continuing the Phi series' focus on efficient, high-capability small models. Designed for instruction-following across modalities.

**Key features:**
- Efficient parameter count for capability level
- Strong instruction-following
- Audio + vision + text multimodal
- MIT license for commercial use

**Links:**
- [Phi-4-multimodal-instruct](https://huggingface.co/microsoft/Phi-4-multimodal-instruct)

---

## Ultravox

**Developer:** Fixie.ai
**Variants:** Multiple backbones (Llama 3.3, Gemma 3, Qwen 3)
**Parameters:** 1B - 27B (depending on backbone)
**License:** Open source

A multimodal Speech LLM that understands speech directly without a separate ASR stage. Uses a multimodal projector to convert audio directly into LLM embedding space, enabling significantly faster response times than traditional ASR+LLM pipelines.

**Key features:**
- ~150ms time-to-first-token on A100 GPU
- Multiple backbone options (Llama, Gemma, Qwen)
- Built on Whisper Large V3 Turbo audio encoder (fine-tuned)
- Real-time voice agent capabilities
- Speech-to-speech translation support

**Latest (v0.6):**
- Improved Hindi language understanding
- Better background noise and audio quality robustness
- New Gemma 3 and Qwen 3 variants

**Links:**
- [Website](https://ultravox.ai/)
- [GitHub](https://github.com/fixie-ai/ultravox)
- [Hugging Face](https://huggingface.co/fixie-ai)

---

## Closed Source / API-Only

For completeness, here are the leading proprietary audio multimodal models available via API.

### Google Gemini

**Models:** Gemini 2.0 Flash, Gemini 2.5 Pro, Gemini 3
**Access:** Google AI Studio, Vertex AI

Google's Gemini family has had native audio support since 2.0. Particularly strong for long-form audio processing—tested successfully with 1-hour recordings. Gemini 3 (December 2025) represents the latest iteration.

**Key features:**
- Native audio token processing
- Long-context audio support
- Prompt-guided transcription and analysis
- Integrated with Google Cloud ecosystem

### OpenAI

**Models:** GPT-4o, GPT-4o Audio Preview
**Access:** OpenAI API

GPT-4o introduced native audio understanding with voice mode. The Audio Preview variant provides direct audio token processing for developers.

**Key features:**
- Audio input/output capabilities
- Voice mode for conversational AI
- Integration with OpenAI ecosystem
- Real-time API for voice applications

---

## Model Comparison

| Model | Developer | Parameters | Quantized Options | License |
|-------|-----------|------------|-------------------|---------|
| Voxtral | Mistral AI | 3B / 24B | TBD | Apache 2.0 |
| Qwen2-Audio | Alibaba | 7B | GGUF | Qwen License |
| Kimi-Audio | Moonshot AI | TBD | TBD | TBD |
| Phi-4-Multimodal | Microsoft | ~14B | TBD | MIT |
| Ultravox | Fixie.ai | 1B - 27B | - | Open Source |

---

## Selection Considerations

**For local deployment on consumer hardware:**
- Qwen2-Audio-7B-Instruct with GGUF quantization is currently the most practical option
- Voxtral Mini (3B) designed specifically for edge deployment

**For maximum capability:**
- Voxtral (24B) for frontier performance
- Phi-4-Multimodal-Instruct offers strong performance with reasonable resource requirements

**For real-time voice agents:**
- Ultravox optimized for low latency (~150ms TTFT)

**For Mistral ecosystem integration:**
- Voxtral provides native compatibility with Mistral tooling

---

## Other Notable Models

See [ask-ai/outputs/models.md](ask-ai/outputs/models.md) for a comprehensive list including:
- SALMONN (ByteDance)
- Step-Audio
- SpeechGPT
- Audio-Flamingo
- And more research/emerging models

---

## Resources

- [Awesome-Audio-LLM](https://github.com/AudioLLMs/Awesome-Audio-LLM) - Curated list of audio LLM research and models
- [Hugging Face audio-text-to-text models](https://huggingface.co/models?pipeline_tag=audio-text-to-text&sort=downloads) - Browse latest models

---

*This list focuses on production-ready or near-production models. The field evolves rapidly.*
