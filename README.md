### Hello, I'm Alex

AI and machine learning engineer building agentic systems and on-device AI.

#### Recent Milestones
- Joined two [vLLM Semantic Router](https://github.com/vllm-project/semantic-router) workgroups: **Router Models & Inference Runtime** and **Developer Experience & Ecosystem**
- Early access to vLLM-SR's [Decision 3.0](https://huggingface.co/collections/vllm-sr/decision-30): ported d3 to Core ML ([d3-coreml](https://huggingface.co/FluidInference/d3-coreml)) and wrote [Decision 3.0 on Apple Silicon](https://vllm-sr.ai/blog/decision-3-0-on-apple-silicon) for the vLLM-SR blog
- [Fluid Inference](https://github.com/FluidInference) was **acquired by Levenza**
- [FluidAudio](https://github.com/FluidInference/FluidAudio) supports dozens of commercial [applications](https://github.com/FluidInference/FluidAudio#showcase)
- **500,000+ monthly model downloads** across different Core ML models on [FluidInference](https://huggingface.co/FluidInference)
- Achieved over **2,000,000 total downloads** and peaked at **500,000 monthly downloads** for [Parakeet TDT V3 Core ML](https://huggingface.co/FluidInference/parakeet-tdt-0.6b-v3-coreml)
- **1,000+ Twitter [followers](https://x.com/Alex_tra_memory)**

#### What I Do
- AI Reseacher
- Finetuning PyTorch models to faster frameworks
- Real-time audio AI (transcription, speaker diarization, TTS, VAD, etc)

#### Contributions

**AI Work**
- [FluidAudio](https://github.com/FluidInference/FluidAudio) — speech AI SDK for iOS and macOS (**2.8K+ ⭐**)
- [FluidUse](https://github.com/FluidInference/FluidUse) — Core ML runtimes for decision models in Swift, including Decision 3.0 (`D3Manager`)
- [möbius](https://github.com/FluidInference/mobius) — model conversion and deployment across accelerators

**Some Experiment Highlights** (Swift runtimes in [FluidUse](https://github.com/FluidInference/FluidUse))
- [Decision 3.0](https://huggingface.co/FluidInference/d3-coreml) — d3-lite, nano and mini on Core ML; d3-lite triages 1,000 pull requests into vLLM-SR workgroups live on an M5 Pro at 0.12 s per PR, 8.3 PRs/s ([demo](https://x.com/Alex_tra_memory/status/2109343807854493724))
- [clef-text-0.6B](https://huggingface.co/FluidInference/clef-text-0.6b-coreml) — distilled Cloudflare's 9B clef-flash into a 0.6B decision model that runs 100% on the Apple Neural Engine; 1,000 support tickets triaged in 57 s on an M5 Pro, 48 ms per ticket, within a few points of the 9B on classification ([demo](https://x.com/Alex_tra_memory/status/2108959518386458695))
- [EmbeddingGemma 2](https://huggingface.co/FluidInference/embeddinggemma-2-coreml) — text encoder 100% on the Apple Neural Engine; sorts 10,080 posts into topics live at ~620/s on a MacBook, any topic splits into subtopics in under a second ([demo](https://x.com/Alex_tra_memory/status/2108391275560931355))
- [GLiNER2.5-Decide](https://huggingface.co/FluidInference/gliner2-5-decide-coreml) — Fastino's 340M decision model on Core ML: ~4× faster, ~5× less peak RAM, half the size ([demo](https://x.com/Alex_tra_memory/status/2103558426618163708))
- [laya](https://huggingface.co/FluidInference/laya-coreml) — Convai's typed decision model with 99.5% of ops on the Apple Neural Engine, 3.7 ms per decision on an M5 Pro ([demo](https://x.com/Alex_tra_memory/status/2102161088598970783))

**Apps and open-source collaborations**
- [SGLang](https://github.com/sgl-project/sglang) — fixed the diffusion LoRA merge cache silently reusing stale merged weights after an adapter is rewritten in place, with regression tests (**37K+ ⭐**)
- [Supertonic](https://github.com/supertone-inc/supertonic) — ported Supertonic 3 to Core ML for Apple Neural Engine inference on iOS and macOS (**13.7K+ ⭐**)
- [mlx-audio](https://github.com/Blaizzy/mlx-audio) — added Kokoro-82M v1.1 Mandarin support in MLX (**7.9K+ ⭐**)
- [vLLM Semantic Router](https://github.com/vllm-project/semantic-router) — workgroup member; wrote the [Decision 3.0 on Apple Silicon](https://vllm-sr.ai/blog/decision-3-0-on-apple-silicon) blog post (d3-lite, nano and mini on Core ML, matching upstream on JevBench and typed-decisions, 2.5–4× faster per request on a Mac); fixed external RAG result ranking across query windows, secured Playground feedback for read users, and hardened Dashboard API authorization with mutation-boundary rechecks (**6K+ ⭐**)
- [IREE](https://github.com/iree-org/iree) — fixed a global optimization crash and moved compiler passes into the main codegen tree (**3.9K+ ⭐**)
- [vLLM Production Stack](https://github.com/vllm-project/production-stack) — fixed router static service discovery to reject mismatched model list configs at startup instead of failing at request time (**2.6K+ ⭐**)
- [OpenOats](https://github.com/yazinsai/OpenOats) — contributed its horizontal wordmark for marketing materials (**2.5K+ ⭐**)
- [Jobpulse](https://jobpulse.fyi/) — built an AI-powered job search site for beginners that peaked at **10,000 monthly users**


#### Find me
[Resume](https://docs.google.com/presentation/d/1gTn48psTT_075OcYbSevkQwSSRC2b6ogUWI48x_UQ9M) · [Twitter](https://twitter.com/Alex_tra_memory) · [LinkedIn](https://www.linkedin.com/in/alexwengg) · [HuggingFace](https://huggingface.co/FluidInference)

---

![Swift](https://img.shields.io/badge/Swift-FA7343?style=for-the-badge&logo=swift&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![CoreML](https://img.shields.io/badge/CoreML-000000?style=for-the-badge&logo=apple&logoColor=white)
![MLX](https://img.shields.io/badge/MLX-5B21B6?style=for-the-badge&logo=apple&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX-005CED?style=for-the-badge&logo=onnx&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![Metal](https://img.shields.io/badge/Metal-000000?style=for-the-badge&logo=apple&logoColor=white)
![NeMo](https://img.shields.io/badge/NeMo-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
