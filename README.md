# Awesome Native Multimodal Modeling (NMM) 🚀

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Formally Defined](https://img.shields.io/badge/Paradigm-Born_Native-purple.svg)]()
[![Chronological Tracking](https://img.shields.io/badge/Timeline-2023--2026-blue.svg)]()
[![GitHub stars](https://img.shields.io/github/stars/NMM-Roadmap/Awesome-NMM-List?style=social)](https://github.com/NMM-Roadmap/Awesome-NMM-List)

> A curated repository for the landmark paper: **"Toward Native Multimodal Modeling: A Roadmap"**.
>
> This repository systematically tracks the structural transition from **Modular Assembly** (late-fusion/grafted compositions that suffer from a fundamental blindness to raw sensory signals) to **Native Multimodal Modeling (NMM)**, where multiple modalities are intrinsically integrated into unified transformer spaces or joint backbones.

---

## 🗺️ The NMM Architectural Taxonomy

We formalize the NMM ecosystem through a dual-dimensional lens based on **Integration Depth** (Mid-fusion vs. Early-fusion) and **Functional Input-Output Duality**:

1. **Multi-to-Text (M2T) Unimodal Generation**: Grounding cross-modal inputs into purely linguistic responses for reasoning.
2. **Multi-to-Target (M2G) Scenario-based Generation**: Direct synthesis of modality-specific outputs through native representations to achieve temporal and acoustic coherence.
3. **Multi-to-Multi (M2M) Symmetric Modeling**: A unified paradigm where understanding and generation naturally coexist as reciprocal projections within a single network.

---

## 🟦 1. Multi-to-Text (M2T) Unimodal Generation
*Native scaling frameworks that ground cross-modal inputs into linguistic streams for logical reasoning.*

* **Late-Fusion Baseline References**: 
  * **LLaVA** [Zhang et al., 2024], **DeepSeek-VL** [Lu et al., 2024], **Qwen-Image** [Wu et al., 2025] — Modularly assembled via shallow projectors; blind to raw sensory signals.
* **Mid-Fusion (Naturally Interacted Regime)**: 
  * **CogVLM** [Wang et al., 2023], **Qwen-Audio** [Chu et al., 2023] — Foundational pioneers maintaining explicit, modality-aware boundaries.
  * **Qwen2.5-VL** [Qwen Team, 2025], **Qwen3-VL** [Qwen Team, 2025], **InternVL-3.5** [Chen et al., 2025] — Massive state-of-the-art evolved mid-fusion architectures.
  * **GLM-5V-Turbo** [ZhipuAI, 2026], **Kimi K2.5** [Kimi Team et al., 2026] — Scale-driven industrial mid-fusion implementations.
* **Dense/Native M2T Scaling**:
  * **MiniCPM-V-4.6** [Yu et al., 2025], **Nemotron3-Nano-Omni** [NVIDIA et al., 2026], **MiMo-V2.5** [Xiaomi MiMo Team, 2026].
  * **Gemma-4** / **Qwen3.6** — Timeline benchmarks driving advanced contextual reasoning.

---

## 🟩 2. Multi-to-Target (M2G) Scenario-based Generation
*Bypassing traditional post-hoc decoders to synthesize photorealistic spatiotemporal physics or continuous speech directly.*

* **Advanced Video World Simulators**:
  * **Wan2.2-T2V-A14B** [Wan Team, 2025] & **Wan2.2** — Unifying video patches into native generation spaces with continuous physics.
  * **HunyuanVideo-1.5** [Wu et al., 2025] & **Hunyuan-Video** — Scaling spatial-temporal cinematic consistency.
  * **Kling-Omni** & **Kling Team** [2025] — High-density motion trajectory simulation.
* **Speech-Centric Native Frameworks**:
  * **OmniVoice** [Zhu et al., 2026], **MiniCPM-o-4.5** [OpenBMB Team, 2026], **Seedream3.0** [Gao et al., 2025], **HiDream-01**.
* **Timeline Milestone Generators**:
  * **LTX-2.2** / **LTX-2.3** / **Ming-Flash** — Accelerating dense scenario-specific generations.

---

## 🟪 3. Multi-to-Multi (M2M) Symmetric Modeling
*Omni-directional unified spaces establishing a symmetric paradigm where comprehension and generation natively coexist.*

* **Early-Fusion (Native Convergent Regime)**:
  * **Transfusion** [Zhou et al., 2024], **Chameleon*** [Meta AI, 2024], **AnyGPT*** [Zhan et al., 2024] — Born-native designs treating all modalities equivalently via one unified backbone and embedding space.
* **Early Unified Predictors**:
  * **Moshi*** [Défossez et al., 2024] — Real-time conversational audio-text dual-stream processing.
  * **Emu3.5*** [Cui et al., 2025] — Next-token sequence prediction unifying understanding and synthesis.
* **Interleaved Sequence Modeling**:
  * **BAGEL-7B** [ByteDance Seed Team, 2025], **OneCAT-3B** [SVAIL Team, 2025], **Show-o2-7B** [Xie et al., 2025].
* **Bidirectional Unification Frontiers**:
  * **Janus-Pro*** [DeepSeek-AI, 2025], **TUNA-2** [Liu et al., 2026], **Mamoda2.5** [Shi et al., 2026] — Collapsing representation boundaries.
  * **Llama-4-Scout / Maverick** (2025) — Advanced interleaved scale exploration.
  * **LLaDA2.0-Uni**, **LongCat-Next**, & **Lance** (2026) — Leading edge of complete native convergence.

*\* Note: Denotes early exploratory or foundational dual-regime architectures.*

---

## 🛠️ The Technical Roadmap Dimensions

Following the systemic structure detailed across **Sections §3 to §7** of the roadmap paper, the core components of the NMM lifecycle are curated below:

### 🧩 1. Architecture (§3)
* **Integration Depth Mapping**: Structural mechanics of joint multimodal backbones versus single unified transformer spaces.
* **Input-Output Decoupling**: Eliminating modality-aware boundaries and shallow projectors.

### 📊 2. Data Curriculum (§4)
* **Interleaved Data Curricula**: Pre-training token mixtures combining massive web-scale text, audio wave, and video streams.
* **Post-Training Engineering**: Multi-modal instruction tuning and alignment token datasets.

### 🎯 3. Training Strategies (§5)
* **Multi-Objective Loss Recipes**: Unifying continuous-discrete objectives (autoregressive next-token prediction and diffusion steps).
* **Scaling Dynamics**: Computed token allocation strategies to maintain gradient stability at the 1T+ MoE frontier.

### ⚡ 4. Inference & Deployment (§6)
* **Full-Duplex Orchestration**: Dynamic KV-cache eviction and multi-scale attention patterns for real-time interaction (<100ms).
* **Hardware-Native Compilation**: Distributed CUDA compute kernels for unified cross-modal token routing.

### 🧪 5. Evaluation Benchmarks (§7)
* **Symmetric Evaluation Matrices**: Benchmarking systems capable of examining interleaved multi-modal sequences without suffering from target modality collapse.

---

## ✍️ Citation

If our formalization, taxonomy, or roadmap framework assists your research, please cite our definitive paper:

```latex
@article{TencentYoutuLab2026toward,
  title={Toward Native Multimodal Modeling: A Roadmap},
  author={Siyu An, Junru Lu, Junnan Dong, et al.},
  journal={arXiv preprin},
  year={2026}
}
