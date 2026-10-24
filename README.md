### Hello, I'm Alex

AI and machine learning engineer building agentic systems and on-device AI.

#### Recent Milestones
- Joined two vLLM Semantic Router [workgroups](https://vllm-sr.ai/community/work-groups): **Router Models & Inference Runtime** and **Developer Experience & Ecosystem**
- Early access to vLLM-SR's [Decision 3.0](https://huggingface.co/collections/vllm-sr/decision-30): ported d3 to Core ML ([d3-coreml](https://huggingface.co/FluidInference/d3-coreml)) and wrote [Decision 3.0 on Apple Silicon](https://vllm-sr.ai/blog/decision-3-0-on-apple-silicon) for the vLLM-SR blog
- [Fluid Inference](https://github.com/FluidInference) was **acquired by Levenza**
- [FluidAudio](https://github.com/FluidInference/FluidAudio) supports dozens of commercial [applications](https://github.com/FluidInference/FluidAudio#showcase)
- **500,000+ monthly model downloads** across different Core ML models on [FluidInference](https://huggingface.co/FluidInference)
- Achieved over **2,000,000 total downloads** and peaked **500,000 monthly downloads** for [Parakeet TDT V3 Core ML](https://huggingface.co/FluidInference/parakeet-tdt-0.6b-v3-coreml)
- 1,000+ Twitter [followers](https://x.com/Alex_tra_memory) in [1 month](https://x.com/Alex_tra_memory/status/2111887700282466530?s=20) thanks to [FluidUse](https://github.com/FluidInference/FluidUse) distilled & finetuned models 

<img width="900" height="816" alt="image" src="https://github.com/user-attachments/assets/02e74268-c2e9-4936-bf22-2eec2b5e6f48" />


#### What I Do
- AI Reseacher
- Finetuning PyTorch models to faster frameworks
- Distilled decision models for inference or games like mario
- Real-time audio AI (transcription, speaker diarization, TTS, VAD, etc)
- Inference Engineering, On-Device ML Engineering, Performance Engineering, Agentic Engineering, ML Engineering

#### Contributions

**AI Work**
- [FluidAudio](https://github.com/FluidInference/FluidAudio) — speech AI SDK for iOS and macOS (**2.8K+ ⭐**)
- [FluidUse](https://github.com/FluidInference/FluidUse) — Core ML runtimes for decision models in Swift, including Decision 3.0 (`D3Manager`)
- [möbius](https://github.com/FluidInference/mobius) — model conversion and deployment across accelerators

**Some Experiment Highlights** (Swift runtimes in [FluidUse](https://github.com/FluidInference/FluidUse))
- [Decision 3.0](https://huggingface.co/FluidInference/d3-coreml) — d3-lite, nano and mini on Core ML; d3-lite triages 1,000 pull requests into vLLM-SR workgroups live on an M5 Pro at 0.12 s per PR, 8.3 PRs/s ([demo](https://x.com/Alex_tra_memory/status/2109343807854493724))

https://x.com/ClementDelangue

<img width="455" height="570" alt="image" src="https://github.com/user-attachments/assets/c56da3f8-ad48-49bc-9b1a-81a64b4219f3" />

https://x.com/victormustar

<img width="467" height="564" alt="image" src="https://github.com/user-attachments/assets/7f8e330a-e2ac-4918-a135-5c60fb822ce9" />



- [clef-text-0.6B](https://huggingface.co/FluidInference/clef-text-0.6b-coreml) — distilled Cloudflare's 9B clef-flash into a 0.6B decision model that runs 100% on the Apple Neural Engine; 1,000 support tickets triaged in 57 s on an M5 Pro, 48 ms per ticket, within a few points of the 9B on classification ([demo](https://x.com/Alex_tra_memory/status/2108959518386458695))

https://x.com/art_zucker/reposts

<img width="448" height="538" alt="image" src="https://github.com/user-attachments/assets/99e45041-eebe-47ca-ab36-5b586fddf701" />


- [EmbeddingGemma 2](https://huggingface.co/FluidInference/embeddinggemma-2-coreml) — text encoder 100% on the Apple Neural Engine; sorts 10,080 posts into topics live at ~620/s on a MacBook, any topic splits into subtopics in under a second ([demo](https://x.com/Alex_tra_memory/status/2108391275560931355))

https://x.com/SeraAndroid/status/2108629662238961694?s=20

<img width="443" height="450" alt="image" src="https://github.com/user-attachments/assets/2c3ad9bd-0bec-47e0-bac9-4d4dd1b45d06" />


- [GLiNER2.5-Decide](https://huggingface.co/FluidInference/gliner2-5-decide-coreml) — Fastino's 340M decision model on Core ML: ~4× faster, ~5× less peak RAM, half the size ([demo](https://x.com/Alex_tra_memory/status/2103558426618163708))

https://x.com/fastinoAI

<img width="458" height="539" alt="image" src="https://github.com/user-attachments/assets/028204a7-aaa5-405d-8b84-195c22c9b7a9" />


- [laya](https://huggingface.co/FluidInference/laya-coreml) — Convai's typed decision model with 99.5% of ops on the Apple Neural Engine, 3.7 ms per decision on an M5 Pro ([demo](https://x.com/Alex_tra_memory/status/2102161088598970783))

https://x.com/jackzampolin/status/2102441521048080627?s=20

<img width="433" height="530" alt="image" src="https://github.com/user-attachments/assets/41622204-29e3-4eb7-9ebd-b1dd5bc76780" />

https://x.com/JiliJeanlouis 

<img width="442" height="686" alt="image" src="https://github.com/user-attachments/assets/7015727f-aca7-4d3c-820d-5ad907cab993" />

https://x.com/ClementDelangue/reposts

<img width="449" height="685" alt="image" src="https://github.com/user-attachments/assets/5a1038f2-a405-4f04-9080-54ec8f36a1cb" />

https://x.com/victormustar

<img width="457" height="694" alt="image" src="https://github.com/user-attachments/assets/0f93e41e-9dc7-4587-88a9-bb9a494f71f3" />


**Apps and open-source collaborations**
- [SGLang](https://github.com/sgl-project/sglang) — fixed the diffusion LoRA merge cache silently reusing stale merged weights after an adapter is rewritten in place, with regression tests (**37K+ ⭐**)
- [Supertonic](https://github.com/supertone-inc/supertonic) — ported Supertonic 3 to Core ML for Apple Neural Engine inference on iOS and macOS (**13.7K+ ⭐**)
- [NVIDIA Dynamo](https://github.com/ai-dynamo/dynamo) — made the disaggregated-serving prefill router [fail closed](https://github.com/ai-dynamo/dynamo/pull/16736) with a retryable 503 while a prefill target is still activating, instead of silently sending requests to decode-only workers (**8.3K+ ⭐**)
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
