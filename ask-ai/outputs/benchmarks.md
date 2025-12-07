# Benchmarks for Audio Transcription Modalities

*Generated: December 7, 2025 by Claude Code, Opus 4.5*

This document identifies existing benchmarks and leaderboards for evaluating each transcription workflow.

---

## Workflow A: Raw ASR Benchmarks

Traditional speech recognition benchmarks focused on transcription accuracy.

### Primary Metrics

| Metric | Description | Standard |
|--------|-------------|----------|
| **WER** (Word Error Rate) | (S+D+I)/N | Lower is better, <5% excellent |
| **CER** (Character Error Rate) | Character-level WER | Used for non-English, tonal languages |
| **RTF** (Real-Time Factor) | Processing time / audio duration | <1.0 = real-time capable |

### Established Benchmarks

| Benchmark | Domain | Size | Link |
|-----------|--------|------|------|
| **LibriSpeech** | Audiobooks | 960h | [openslr.org/12](https://www.openslr.org/12/) |
| **Common Voice** | Crowdsourced | 2,500h+ | [commonvoice.mozilla.org](https://commonvoice.mozilla.org/) |
| **GigaSpeech** | Multi-domain | 10,000h | [github.com/SpeechColab/GigaSpeech](https://github.com/SpeechColab/GigaSpeech) |
| **VoxPopuli** | EU Parliament | 400k+ hours | [github.com/facebookresearch/voxpopuli](https://github.com/facebookresearch/voxpopuli) |
| **FLEURS** | Multilingual | 102 languages | [huggingface.co/datasets/google/fleurs](https://huggingface.co/datasets/google/fleurs) |
| **TED-LIUM 3** | TED Talks | 452h | [openslr.org/51](https://www.openslr.org/51/) |
| **AMI Corpus** | Meetings | 100h | [groups.inf.ed.ac.uk/ami/corpus](https://groups.inf.ed.ac.uk/ami/corpus/) |
| **CHiME Challenge** | Noisy speech | Various | [chimechallenge.org](https://www.chimechallenge.org/) |
| **Earnings-22** | Financial calls | 119h | [github.com/revdotcom/speech-datasets](https://github.com/revdotcom/speech-datasets) |
| **SPGISpeech** | Financial | 5,000h | [datasets.kensho.com/datasets/spgispeech](https://datasets.kensho.com/datasets/spgispeech) |

### Active Leaderboards

| Leaderboard | Maintained By | Link |
|-------------|---------------|------|
| **Open ASR Leaderboard** | Hugging Face | [huggingface.co/spaces/hf-audio/open_asr_leaderboard](https://huggingface.co/spaces/hf-audio/open_asr_leaderboard) |
| **Papers With Code - ASR** | Papers With Code | [paperswithcode.com/task/speech-recognition](https://paperswithcode.com/task/speech-recognition) |
| **ESB Benchmark** | Hugging Face | [huggingface.co/spaces/esb/leaderboard](https://huggingface.co/spaces/esb/leaderboard) |

---

## Workflow B: Pipeline/Cascaded Benchmarks

Two-stage systems use ASR benchmarks for stage 1, plus text quality metrics for stage 2.

### ASR Stage

Use benchmarks from Workflow A above.

### LLM Text Quality (Established Metrics)

| Metric | Description | Reference |
|--------|-------------|-----------|
| **BLEU** | N-gram overlap | [aclweb.org/anthology/P02-1040](https://aclweb.org/anthology/P02-1040/) |
| **ROUGE** | Recall-oriented summarization | [aclweb.org/anthology/W04-1013](https://aclweb.org/anthology/W04-1013/) |
| **BERTScore** | Semantic similarity | [github.com/Tiiiger/bert_score](https://github.com/Tiiiger/bert_score) |
| **METEOR** | Alignment-based | [aclweb.org/anthology/W05-0909](https://aclweb.org/anthology/W05-0909/) |

### Readability Metrics (Standard)

| Metric | Description |
|--------|-------------|
| **Flesch-Kincaid** | Grade level readability |
| **Gunning Fog Index** | Text complexity |
| **SMOG Index** | Years of education needed |

### Note on Pipeline Benchmarks

No standardized end-to-end benchmarks exist specifically for ASR+LLM pipelines. Evaluation typically uses ASR metrics on intermediate output and summarization/editing metrics on final output separately.

---

## Workflow C: Audio Multimodal Benchmarks

Native audio understanding benchmarks are emerging but less mature than ASR benchmarks.

### Audio-Language Understanding Benchmarks

| Benchmark | Focus | Link |
|-----------|-------|------|
| **AIR-Bench** | Audio Information Retrieval | [github.com/OFA-Sys/AIR-Bench](https://github.com/OFA-Sys/AIR-Bench) |
| **AudioBench** | Comprehensive audio understanding | [github.com/AudioLLMs/AudioBench](https://github.com/AudioLLMs/AudioBench) |
| **Dynamic-SUPERB** | Diverse speech tasks | [github.com/dynamic-superb/dynamic-superb](https://github.com/dynamic-superb/dynamic-superb) |
| **MMAU** | Multimodal Audio Understanding | [sakshi113.github.io/mmau_homepage](https://sakshi113.github.io/mmau_homepage/) |
| **AudioCaps** | Audio captioning | [audiocaps.github.io](https://audiocaps.github.io/) |
| **Clotho** | Audio captioning | [zenodo.org/record/3490684](https://zenodo.org/record/3490684) |

### Speech-Specific Benchmarks

| Benchmark | Task | Link |
|-----------|------|------|
| **Spoken-SQuAD** | Speech QA | [github.com/chiahsuan156/Spoken-SQuAD](https://github.com/chiahsuan156/Spoken-SQuAD) |
| **SLUE** | Spoken Language Understanding | [asappresearch.github.io/slue-toolkit](https://asappresearch.github.io/slue-toolkit/) |
| **SUPERB** | Speech processing | [superbbenchmark.org](https://superbbenchmark.org/) |
| **ML-SUPERB** | Multilingual speech | [github.com/espnet/espnet](https://github.com/espnet/espnet) |

### Audio Classification Benchmarks

| Benchmark | Domain | Link |
|-----------|--------|------|
| **ESC-50** | Environmental sounds | [github.com/karolpiczak/ESC-50](https://github.com/karolpiczak/ESC-50) |
| **AudioSet** | General audio | [research.google.com/audioset](https://research.google.com/audioset/) |
| **VoxCeleb** | Speaker recognition | [robots.ox.ac.uk/~vgg/data/voxceleb](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/) |
| **IEMOCAP** | Speech emotion | [sail.usc.edu/iemocap](https://sail.usc.edu/iemocap/) |
| **MusicCaps** | Music understanding | [kaggle.com/datasets/googleai/musiccaps](https://www.kaggle.com/datasets/googleai/musiccaps) |

### Audio Multimodal Leaderboards

| Leaderboard | Focus | Link |
|-------------|-------|------|
| **AudioBench Leaderboard** | Audio LLMs | [huggingface.co/spaces/AudioLLMs/AudioBench-Leaderboard](https://huggingface.co/spaces/AudioLLMs/AudioBench-Leaderboard) |
| **SUPERB Leaderboard** | Speech tasks | [superbbenchmark.org/leaderboard](https://superbbenchmark.org/leaderboard) |
| **Papers With Code - Audio** | Multiple tasks | [paperswithcode.com/area/audio](https://paperswithcode.com/area/audio) |

---

## Benchmark Gaps

The following evaluation needs lack standardized benchmarks as of December 2025:

| Gap | Description |
|-----|-------------|
| **Prompt-guided transcription** | No benchmark for instruction-following in audio-to-text |
| **Long-form audio** | Most benchmarks use clips <30s; limited 1hr+ evaluation |
| **Real-world dictation** | Academic datasets use prepared speech, not off-the-cuff |
| **Cross-modal reasoning** | Audio + vision + text combined understanding |

---

## Where to Track Benchmark Progress

| Resource | Type | Link |
|----------|------|------|
| **Papers With Code** | Benchmark aggregator | [paperswithcode.com](https://paperswithcode.com/) |
| **Hugging Face Spaces** | Community leaderboards | [huggingface.co/spaces](https://huggingface.co/spaces) |
| **arXiv cs.SD** | Speech/audio papers | [arxiv.org/list/cs.SD/recent](https://arxiv.org/list/cs.SD/recent) |
| **arXiv eess.AS** | Audio/speech engineering | [arxiv.org/list/eess.AS/recent](https://arxiv.org/list/eess.AS/recent) |
