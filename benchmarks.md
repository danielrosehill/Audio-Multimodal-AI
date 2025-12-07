# Audio Multimodal Benchmarks

*Last updated: December 7, 2025*

This page covers key benchmarks for evaluating audio multimodal models—focusing on the unified audio understanding capabilities that distinguish these models from traditional ASR.

---

## MSEB (Massive Sound Embedding Benchmark)

**Developer:** Google Research
**Presented:** NeurIPS 2025
**License:** Apache 2.0

The definitive open-source platform for measuring machine sound intelligence. MSEB provides a unified framework for evaluating how well AI models understand audio across diverse, real-world scenarios.

### Eight Core Capabilities

| Capability | Application | Type |
|------------|-------------|------|
| **Retrieval** | Voice search | Semantic |
| **Reasoning** | Intelligent assistants | Semantic |
| **Classification** | Monitoring/security | Acoustic |
| **Transcription** | Speech-to-text | Semantic |
| **Segmentation** | Indexing important terms | Semantic |
| **Clustering** | Organizing sound samples | Acoustic |
| **Reranking** | Refining text hypotheses | Semantic |
| **Reconstruction** | Regenerating audio from embeddings | Acoustic |

### Key Findings

Research using MSEB revealed five major limitations in current sound-processing AI:

1. **ASR transcription bottlenecks** semantic understanding
2. **Cascade models optimize for wrong metrics**
3. **Performance varies drastically across languages**
4. **Robustness degrades significantly under noise**
5. **Simple tasks don't require complex models**

### Links

- [Google Research Blog](https://research.google/blog/from-waveforms-to-wisdom-the-new-benchmark-for-auditory-intelligence/)
- [GitHub Repository](https://github.com/google-research/mseb)

---

## Audio Multimodal Leaderboards

| Leaderboard | Focus | Link |
|-------------|-------|------|
| **AudioBench** | Comprehensive audio LLM evaluation | [HF Leaderboard](https://huggingface.co/spaces/AudioLLMs/AudioBench-Leaderboard) |
| **SUPERB** | Speech processing tasks | [superbbenchmark.org](https://superbbenchmark.org/leaderboard) |
| **Open ASR Leaderboard** | Speech recognition | [HF Leaderboard](https://huggingface.co/spaces/hf-audio/open_asr_leaderboard) |

---

## Audio Understanding Benchmarks

| Benchmark | Focus | Link |
|-----------|-------|------|
| **AIR-Bench** | Audio Information Retrieval | [GitHub](https://github.com/OFA-Sys/AIR-Bench) |
| **AudioBench** | Comprehensive audio understanding | [GitHub](https://github.com/AudioLLMs/AudioBench) |
| **Dynamic-SUPERB** | Diverse speech tasks | [GitHub](https://github.com/dynamic-superb/dynamic-superb) |
| **MMAU** | Multimodal Audio Understanding | [Homepage](https://sakshi113.github.io/mmau_homepage/) |

---

## Traditional ASR Benchmarks

For comparison with classic speech recognition:

| Benchmark | Domain | Size |
|-----------|--------|------|
| **LibriSpeech** | Audiobooks | 960h |
| **Common Voice** | Crowdsourced | 2,500h+ |
| **GigaSpeech** | Multi-domain | 10,000h |
| **FLEURS** | Multilingual (102 languages) | Various |

---

## Benchmark Gaps

As of December 2025, standardized benchmarks are still lacking for:

- **Prompt-guided transcription** — Instruction-following in audio-to-text
- **Long-form audio** — Most benchmarks use <30s clips; limited 1hr+ evaluation
- **Real-world dictation** — Academic datasets use prepared speech, not spontaneous
- **Cross-modal reasoning** — Audio + vision + text combined understanding

---

## Additional Resources

See [ask-ai/outputs/benchmarks.md](ask-ai/outputs/benchmarks.md) for a comprehensive list of benchmarks organized by workflow type (raw ASR, pipeline, multimodal).

---

*The benchmark landscape is evolving rapidly as audio multimodal becomes a distinct research focus.*
