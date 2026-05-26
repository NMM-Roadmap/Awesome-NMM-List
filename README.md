<div align="center">

# Awesome Native Multimodal Modeling (NMM)

<p>
  <em>A curated reading list & model zoo for the era of <b>Born-Native</b> multimodal foundation models.</em>
</p>

<p>
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <img src="https://img.shields.io/badge/Paradigm-Born_Native-purple.svg" alt="Paradigm">
  <img src="https://img.shields.io/badge/Timeline-2023--2026-blue.svg" alt="Timeline">
  <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs welcome">
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License">
  <a href="https://github.com/NMM-Roadmap/Awesome-NMM-List"><img src="https://img.shields.io/github/stars/NMM-Roadmap/Awesome-NMM-List?style=social" alt="GitHub stars"></a>
</p>

<p>
  <b>📄 Companion paper:</b>
  <a href="https://arxiv.org/abs/2605.25343"><i>"Toward Native Multimodal Modeling: A Roadmap"</i></a>
</p>

<p>
  <a href="#-the-nmm-architectural-taxonomy">Taxonomy</a> ·
  <a href="#-1-multi-to-text-m2t-unimodal-generation">M2T</a> ·
  <a href="#-2-multi-to-target-m2g-scenario-based-generation">M2G</a> ·
  <a href="#-3-multi-to-multi-m2m-symmetric-modeling">M2M</a> ·
  <a href="#%EF%B8%8F-the-technical-roadmap-dimensions">Technical Roadmap</a> ·
  <a href="#-citation">Cite</a>
</p>

</div>

---

> This repository systematically tracks the structural transition from **Modular Assembly** — late-fusion / grafted compositions that suffer from a fundamental blindness to raw sensory signals — to **Native Multimodal Modeling (NMM)**, where multiple modalities are intrinsically integrated into a *unified transformer space* or *joint backbone*.
>
> ⭐ **Star** this repo to track the latest landmark works. **PRs are warmly welcomed** for any model we may have missed.

---

## 🗺️ The NMM Architectural Taxonomy

We formalize the NMM ecosystem through a dual-dimensional lens based on **Integration Depth** (mid-fusion vs. early-fusion) and **Functional Input–Output Duality**:

| # | Paradigm | Input → Output | Core Idea |
|---|---|---|---|
| 🟦 | **M2T** — Multi-to-Text | multimodal → text | Ground cross-modal inputs into purely linguistic responses for reasoning. |
| 🟩 | **M2G** — Multi-to-Target | multimodal → modality-specific | Direct synthesis of modality-specific outputs through native representations to achieve temporal & acoustic coherence. |
| 🟪 | **M2M** — Multi-to-Multi | multimodal → multimodal | A unified paradigm where understanding and generation naturally coexist as reciprocal projections within a single network. |

---

## 🟦 1. Multi-to-Text (M2T) Unimodal Generation

> *Native scaling frameworks that ground cross-modal inputs into linguistic streams for logical reasoning.*

### 🧱 Late-Fusion Baseline References
*Modularly assembled via shallow projectors; blind to raw sensory signals.*

- **LLaVA** [Liu *et al.*, 2023] — [`💻 GitHub`](https://github.com/haotian-liu/LLaVA) · [`📄 Paper`](https://arxiv.org/abs/2304.08485)
- **DeepSeek-VL** [Lu *et al.*, 2024] — [`💻 GitHub`](https://github.com/deepseek-ai/DeepSeek-VL) · [`📄 Paper`](https://arxiv.org/abs/2403.05525)
- **Qwen-Image** [Wu *et al.*, 2025] — [`💻 GitHub`](https://github.com/QwenLM/Qwen-Image) · [`🌐 Blog`](https://qwen.ai/blog?id=qwen-image)

### 🔗 Mid-Fusion (Naturally Interacted Regime)
*Foundational pioneers maintaining explicit, modality-aware boundaries.*

- **CogVLM** [Wang *et al.*, 2023] — [`💻 GitHub`](https://github.com/THUDM/CogVLM)
- **Qwen-Audio** [Chu *et al.*, 2023] — [`💻 GitHub`](https://github.com/QwenLM/Qwen-Audio) · [`🌐 Project Page`](https://qwen-audio.github.io/Qwen-Audio/)

*Massive state-of-the-art evolved mid-fusion architectures:*

- **Qwen2.5-VL** [Qwen Team, 2025] — [`💻 GitHub`](https://github.com/QwenLM/Qwen2.5-VL) · [`🌐 Blog`](https://qwen.ai/blog?id=qwen2.5-vl)
- **Qwen3-VL** [Qwen Team, 2025] — [`💻 GitHub`](https://github.com/QwenLM/Qwen3-VL) · [`📄 Paper`](https://arxiv.org/abs/2511.21631)
- **InternVL-3.5** [Chen *et al.*, 2025] — [`💻 GitHub`](https://github.com/OpenGVLab/InternVL) · [`🤗 HF Collection`](https://huggingface.co/collections/OpenGVLab/internvl35)

*Scale-driven industrial mid-fusion implementations:*

- **GLM-4.5V / GLM-V** [ZhipuAI, 2025–2026] — [`💻 GitHub`](https://github.com/zai-org/GLM-V) · [`🤗 HF Model`](https://huggingface.co/zai-org/GLM-4.5V)
- **Kimi K2 / K2.5** [Moonshot AI, 2025–2026] — [`🌐 Project Page`](https://moonshotai.github.io/Kimi-K2/) · [`💻 GitHub Org`](https://github.com/MoonshotAI)

### 🧬 Dense / Native M2T Scaling

- **MiniCPM-V 4.x** [Yu *et al.*, 2025] — [`💻 GitHub`](https://github.com/OpenBMB/MiniCPM-V)
- **Nemotron 3 Nano Omni** [NVIDIA, 2026] — [`💻 GitHub`](https://github.com/NVIDIA-NeMo/Nemotron) · [`📄 Paper`](https://arxiv.org/abs/2604.24954)
- **MiMo-V2.5** [Xiaomi MiMo Team, 2026] — [`💻 GitHub`](https://github.com/XiaomiMiMo) · [`🌐 Project Page`](https://mimo.xiaomi.com/mimo-v2-5)
- **Gemma-4** / **Qwen3.6** — *Timeline benchmarks driving advanced contextual reasoning (forthcoming).*

---

## 🟩 2. Multi-to-Target (M2G) Scenario-based Generation

> *Bypassing traditional post-hoc decoders to synthesize photorealistic spatiotemporal physics or continuous speech directly.*

### 🎬 Advanced Video / World Simulators

- **Wan 2.2-T2V-A14B** [Wan Team, 2025] — [`🤗 HF Model`](https://huggingface.co/Wan-AI/Wan2.2-T2V-A14B) — *Unifies video patches into native generation spaces with continuous physics.*
- **HunyuanVideo & HunyuanVideo-1.5** [Tencent, 2024–2025] — [`💻 GitHub`](https://github.com/Tencent-Hunyuan/HunyuanVideo) · [`🤗 HF Model (1.5)`](https://huggingface.co/tencent/HunyuanVideo-1.5)
- **Kling-Omni** [Kuaishou, 2025] — [`🌐 Project Page`](https://kling.ai/app)

### 🎙️ Speech-Centric Native Frameworks

- **OmniVoice** [Zhu *et al.*, 2026] — [`💻 GitHub`](https://github.com/k2-fsa/OmniVoice) · [`🌐 Project Page`](https://zhu-han.github.io/omnivoice/)
- **MiniCPM-o 2.6 / 4.5** [OpenBMB, 2025–2026] — [`🤗 HF Model`](https://huggingface.co/openbmb/MiniCPM-o-2_6) · [`💻 GitHub`](https://github.com/OpenBMB/MiniCPM-o)
- **Seedream 3.0** [Gao *et al.*, 2025] — [`📄 Tech Report`](https://arxiv.org/abs/2504.11346) · [`🌐 Project Page`](https://seed.bytedance.com/zh/tech/seedream3_0)
- **HiDream-I1** — [`💻 GitHub`](https://github.com/HiDream-ai/HiDream-I1)

### 📅 Timeline Milestone Generators

- **LTX-2 / LTX-Video** [Lightricks, 2024–2026] — [`💻 GitHub`](https://github.com/Lightricks/LTX-Video)
- **Ming-Flash-Omni** [Ant Group / inclusionAI, 2025] — [`💻 GitHub`](https://github.com/inclusionAI/Ming) · [`📄 Paper`](https://arxiv.org/abs/2510.24821)

---

## 🟪 3. Multi-to-Multi (M2M) Symmetric Modeling

> *Omni-directional unified spaces establishing a symmetric paradigm where comprehension and generation natively coexist.*

### 🔥 Early-Fusion (Native Convergent Regime)
*Born-native designs treating all modalities equivalently via one unified backbone & embedding space.*

- **Transfusion** [Zhou *et al.*, 2024] — [`📄 Paper`](https://arxiv.org/abs/2408.11039)
- **Chameleon** ★ [Meta AI, 2024] — [`💻 GitHub`](https://github.com/facebookresearch/chameleon) · [`📄 Paper`](https://arxiv.org/abs/2405.09818)
- **AnyGPT** ★ [Zhan *et al.*, 2024] — [`💻 GitHub`](https://github.com/OpenMOSS/AnyGPT) · [`📄 Paper`](https://arxiv.org/abs/2402.12226)

### 🔮 Early Unified Predictors

- **Moshi** ★ [Défossez *et al.*, 2024] — [`💻 GitHub`](https://github.com/kyutai-labs/moshi) · [`📄 Paper`](https://arxiv.org/abs/2410.00037) — *Real-time conversational audio-text dual-stream processing.*
- **Emu3 / Emu3.5** ★ [BAAI, 2024–2025] — [`🌐 Project Page`](https://emu.baai.ac.cn/) · [`📄 Paper`](https://arxiv.org/abs/2409.18869) — *Next-token sequence prediction unifying understanding and synthesis.*

### 🧩 Interleaved Sequence Modeling

- **BAGEL-7B** [ByteDance Seed Team, 2025] — [`🤗 HF Model`](https://huggingface.co/ByteDance-Seed/BAGEL-7B-MoT) · [`🌐 Project Page`](https://bagel-ai.org/) · [`📄 Paper`](https://arxiv.org/abs/2505.14683)
- **OneCAT-3B** [Meituan & SJTU, 2025] — [`💻 GitHub`](https://github.com/onecat-ai/onecat) · [`🤗 HF Model`](https://huggingface.co/onecat-ai/OneCAT-3B)
- **Show-o2-7B** [Xie *et al.*, 2025] — [`💻 GitHub`](https://github.com/showlab/Show-o) · [`📄 Paper`](https://arxiv.org/abs/2506.15564)

### 🌌 Bidirectional Unification Frontiers
*Collapsing representation boundaries.*

- **Janus-Pro** ★ [DeepSeek-AI, 2025] — [`🤗 HF Model`](https://huggingface.co/deepseek-ai/Janus-Pro-7B) · [`📄 Paper`](https://arxiv.org/abs/2501.17811)
- **Llama-4 Scout / Maverick** [Meta AI, 2025] — [`🌐 Llama Site`](https://www.llama.com/) — *Advanced interleaved-scale exploration.*
- **LLaDA-V** [Ml-GSAI, 2025] — [`💻 GitHub`](https://github.com/ML-GSAI/LLaDA-V) · [`🌐 Project Page`](https://ml-gsai.github.io/LLaDA-V-demo/) · [`📄 Paper`](https://arxiv.org/abs/2505.16933)
- **Lance** [ByteDance, 2026] — [`📄 Paper`](https://arxiv.org/abs/2605.18678) — *Leading edge of complete native convergence.*
- **TUNA-2** [Liu *et al.*, 2026] / **Mamoda 2.5** [Shi *et al.*, 2026] / **LongCat-Next** — *Forthcoming.*

> ★ *Denotes early exploratory or foundational dual-regime architectures.*

---

## 🛠️ The Technical Roadmap Dimensions

Following the systemic structure detailed across **Sections §3–§7** of the roadmap paper, the core components of the NMM lifecycle are curated below.

<table>
<tr>
  <td width="50%" valign="top">

### 🧩 1. Architecture · §3
- **Integration Depth Mapping** — Structural mechanics of joint multimodal backbones vs. single unified transformer spaces.
- **Input–Output Decoupling** — Eliminating modality-aware boundaries & shallow projectors.

  </td>
  <td width="50%" valign="top">

### 📊 2. Data Curriculum · §4
- **Interleaved Data Curricula** — Pre-training token mixtures combining web-scale text, audio waves, & video streams.
- **Post-Training Engineering** — Multi-modal instruction tuning & alignment token datasets.

  </td>
</tr>
<tr>
  <td width="50%" valign="top">

### 🎯 3. Training Strategies · §5
- **Multi-Objective Loss Recipes** — Unifying continuous-discrete objectives (autoregressive next-token prediction + diffusion steps).
- **Scaling Dynamics** — Computed token-allocation strategies to maintain gradient stability at the 1T+ MoE frontier.

  </td>
  <td width="50%" valign="top">

### ⚡ 4. Inference & Deployment · §6
- **Full-Duplex Orchestration** — Dynamic KV-cache eviction & multi-scale attention patterns for real-time interaction (<100 ms).
- **Hardware-Native Compilation** — Distributed CUDA compute kernels for unified cross-modal token routing.

  </td>
</tr>
<tr>
  <td colspan="2" valign="top">

### 🧪 5. Evaluation Benchmarks · §7
- **Symmetric Evaluation Matrices** — Benchmarking systems capable of examining interleaved multi-modal sequences without suffering from target-modality collapse.

  </td>
</tr>
</table>

---

## 🤝 Contributing

Contributions are very welcome! If a notable native multimodal model is missing or you find an outdated link, please open an Issue or send a Pull Request.

The preferred entry format is:

```markdown
- **<Model Name>** [<Authors / Team>, <Year>] — [`💻 GitHub`](https://...) · [`📄 Paper`](https://...)
```

---

## ✍️ Citation

If our formalization, taxonomy, or roadmap framework assists your research, please cite our definitive paper:

```bibtex
@article{TencentYoutuLab2026toward,
  title   = {Toward Native Multimodal Modeling: A Roadmap},
  author  = {Siyu An and Junru Lu and Junnan Dong and others},
  journal = {arXiv preprint},
  year    = {2026}
}
```

---

<div align="center">
  <sub>Maintained by the NMM-Roadmap community · Made with ❤️ for open multimodal research.</sub>
</div>
