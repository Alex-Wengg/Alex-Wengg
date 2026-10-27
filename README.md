### Hello, I'm Alex

AI and machine learning engineer building agentic systems and inference engines from client side to server side.

#### What I Do
- AI Researcher
- Finetuning PyTorch models to faster frameworks
- Distilled decision models for inference or games like mario
- Real-time audio AI (transcription, speaker diarization, TTS, VAD, etc)
- Server-side LLM serving: request routing, disaggregated prefill/decode, and diffusion serving in vLLM, SGLang and NVIDIA Dynamo
- Inference Engineering, On-Device ML Engineering, Server-Side ML Engineering, Performance Engineering, Agentic Engineering, ML Engineering

#### Contributions

**Projects I work on** — at [Fluid Inference](https://github.com/FluidInference), which was **acquired by Levenza**
- [FluidAudio](https://github.com/FluidInference/FluidAudio) — speech AI SDK for iOS and macOS (**3.2K+ ⭐**)
  - Supports dozens of commercial [applications](https://github.com/FluidInference/FluidAudio#showcase)
  - [Parakeet TDT V3 Core ML](https://huggingface.co/FluidInference/parakeet-tdt-0.6b-v3-coreml): over **2,000,000 total downloads**, peaked at **500,000 monthly downloads**
- [FluidUse](https://github.com/FluidInference/FluidUse) — Core ML runtimes for decision models in Swift, including Decision 3.0 (`D3Manager`)
  - Its distilled & finetuned models brought 1,000+ Twitter [followers](https://x.com/Alex_tra_memory) in [1 month](https://x.com/Alex_tra_memory/status/2111887700282466530?s=20)
- [möbius](https://github.com/FluidInference/mobius) — model conversion and deployment across accelerators
  - **500,000+ monthly model downloads** across the Core ML models on [FluidInference](https://huggingface.co/FluidInference)

<img width="450" alt="1,001 Twitter followers" src="https://github.com/user-attachments/assets/02e74268-c2e9-4936-bf22-2eec2b5e6f48" />

**Open-source collaborations and apps**
- [SGLang](https://github.com/sgl-project/sglang) — fixed the diffusion LoRA merge cache silently reusing stale merged weights after an adapter is rewritten in place, with regression tests ([#44204](https://github.com/sgl-project/sglang/pull/44204)) (**38K+ ⭐**)
- [Supertonic](https://github.com/supertone-oss-archive/supertonic) — ported Supertonic 3 to Core ML for Apple Neural Engine inference on iOS and macOS (conversion [mobius#64](https://github.com/FluidInference/mobius/pull/64), runtime [FluidAudio#617](https://github.com/FluidInference/FluidAudio/pull/617)) (**13.7K+ ⭐**)
- [NVIDIA Dynamo](https://github.com/ai-dynamo/dynamo) — made the disaggregated-serving prefill router fail closed with a retryable 503 while a prefill target is still activating, instead of silently sending requests to decode-only workers ([#16736](https://github.com/ai-dynamo/dynamo/pull/16736)) (**8.4K+ ⭐**)
- [mlx-audio](https://github.com/Blaizzy/mlx-audio) — added Kokoro-82M v1.1 Mandarin support in MLX ([#341](https://github.com/Blaizzy/mlx-audio/pull/341)) (**8.1K+ ⭐**)
- [vLLM Semantic Router](https://github.com/vllm-project/semantic-router) (**6.3K+ ⭐**)
  - Member of two [workgroups](https://vllm-sr.ai/community/work-groups): **Router Models & Inference Runtime** and **Developer Experience & Ecosystem**
  - Early access to [Decision 3.0](https://huggingface.co/collections/vllm-sr/decision-30): ported d3 to Core ML ([d3-coreml](https://huggingface.co/FluidInference/d3-coreml))
  - Wrote the [Decision 3.0 on Apple Silicon](https://vllm-sr.ai/blog/decision-3-0-on-apple-silicon) blog post: d3-lite, nano and mini on Core ML, matching upstream on JevBench and typed-decisions, 2.5–4× faster per request on a Mac ([#4905](https://github.com/vllm-project/semantic-router/pull/4905), [#4975](https://github.com/vllm-project/semantic-router/pull/4975))
  - Fixed external RAG result ranking across query windows ([#3750](https://github.com/vllm-project/semantic-router/pull/3750))
  - Secured Playground feedback for read users ([#3755](https://github.com/vllm-project/semantic-router/pull/3755))
  - Hardened Dashboard API authorization with mutation-boundary rechecks ([a3174df](https://github.com/vllm-project/semantic-router/commit/a3174df365c496cbcc1f01ca6137061556618781))
- [KServe](https://github.com/kserve/kserve) — made KEDA autoscaling honor the target type an InferenceService sets for External and PodMetric metrics, instead of silently defaulting to AverageValue ([#6185](https://github.com/kserve/kserve/pull/6185)) (**6.1K+ ⭐**)
- [IREE](https://github.com/iree-org/iree) (**4K+ ⭐**)
  - Fixed a global optimization crash in RaiseSpecialOps ([#24626](https://github.com/iree-org/iree/pull/24626))
  - Moved compiler passes into the main codegen tree and retired the `iree-dialects` directory ([#24501](https://github.com/iree-org/iree/pull/24501), [#24543](https://github.com/iree-org/iree/pull/24543), [#24612](https://github.com/iree-org/iree/pull/24612))
- [AgentENV](https://github.com/kvcache-ai/AgentENV) — fixed the ublk storage daemon leaking block devices when a client times out before receiving its device handoff, by rolling back undelivered handoffs ([#431](https://github.com/kvcache-ai/AgentENV/pull/431)) 
- [vLLM Production Stack](https://github.com/vllm-project/production-stack) — fixed router static service discovery to reject mismatched model list configs at startup instead of failing at request time ([#1084](https://github.com/vllm-project/production-stack/pull/1084)) 
- [OpenOats](https://github.com/yazinsai/OpenOats) — contributed its horizontal wordmark for marketing materials 
- [Emmy](https://github.com/cloudrift-ai/emmy) — CloudRift's GPU compiler for LLM inference: made kernel lowering fail loudly instead of silently returning an unwritten output when a fused kernel drops a declared store ([#1257](https://github.com/cloudrift-ai/emmy/pull/1257)); fixing permutes that silently compiled as reshapes is in review ([#1280](https://github.com/cloudrift-ai/emmy/pull/1280))

**Some Experiment Highlights** (Swift runtimes in [FluidUse](https://github.com/FluidInference/FluidUse))
- [laya](https://huggingface.co/FluidInference/laya-coreml) — Convai's typed decision model with 99.5% of ops on the Apple Neural Engine, 3.7 ms per decision on an M5 Pro ([demo](https://x.com/Alex_tra_memory/status/2102161088598970783)) · 1,323 likes · 111 reposts · 120K views

<table>
  <tr>
    <td align="center" valign="top"><a href="https://x.com/jackzampolin/status/2102441521048080627?s=20">@jackzampolin</a><br><img width="200" alt="image" src="https://github.com/user-attachments/assets/41622204-29e3-4eb7-9ebd-b1dd5bc76780" /></td>
    <td align="center" valign="top"><a href="https://x.com/JiliJeanlouis">@JiliJeanlouis</a><br><img width="200" alt="image" src="https://github.com/user-attachments/assets/7015727f-aca7-4d3c-820d-5ad907cab993" /></td>
    <td align="center" valign="top"><a href="https://x.com/ClementDelangue/reposts">@ClementDelangue reposts</a><br><img width="200" alt="image" src="https://github.com/user-attachments/assets/5a1038f2-a405-4f04-9080-54ec8f36a1cb" /></td>
    <td align="center" valign="top"><a href="https://x.com/victormustar">@victormustar</a><br><img width="200" alt="image" src="https://github.com/user-attachments/assets/0f93e41e-9dc7-4587-88a9-bb9a494f71f3" /></td>
  </tr>
</table>

- [GLiNER2.5-Decide](https://huggingface.co/FluidInference/gliner2-5-decide-coreml) — Fastino's 340M decision model on Core ML: ~4× faster, ~5× less peak RAM, half the size ([demo](https://x.com/Alex_tra_memory/status/2103558426618163708)) · 880 likes · 83 reposts · 69K views

https://x.com/fastinoAI

<img width="458" height="539" alt="image" src="https://github.com/user-attachments/assets/028204a7-aaa5-405d-8b84-195c22c9b7a9" />

- [EmbeddingGemma 2](https://huggingface.co/FluidInference/embeddinggemma-2-coreml) — text encoder 100% on the Apple Neural Engine; sorts 10,080 posts into topics live at ~620/s on a MacBook, any topic splits into subtopics in under a second ([demo](https://x.com/Alex_tra_memory/status/2108391275560931355)) · 693 likes · 51 reposts · 34K views

https://x.com/SeraAndroid/status/2108629662238961694?s=20

https://x.com/googlegemma/status/2115150306032193954

<img width="447" height="528" alt="image" src="https://github.com/user-attachments/assets/247416a5-9d37-434f-8342-8a941799eebd" />


<img width="443" height="450" alt="image" src="https://github.com/user-attachments/assets/2c3ad9bd-0bec-47e0-bac9-4d4dd1b45d06" />

- [clef-text-0.6B](https://huggingface.co/FluidInference/clef-text-0.6b-coreml) — distilled Cloudflare's 9B clef-flash into a 0.6B decision model that runs 100% on the Apple Neural Engine; 1,000 support tickets triaged in 57 s on an M5 Pro, 48 ms per ticket, within a few points of the 9B on classification ([demo](https://x.com/Alex_tra_memory/status/2108959518386458695)) · 494 likes · 45 reposts · 32K views

<table>
  <tr>
    <td align="center" valign="top"><a href="https://x.com/art_zucker/reposts">@art_zucker reposts</a><br><img width="420" alt="image" src="https://github.com/user-attachments/assets/99e45041-eebe-47ca-ab36-5b586fddf701" /></td>
    <td align="center" valign="top"><a href="https://x.com/ClementDelangue/reposts">@ClementDelangue reposts</a><br><img width="420" alt="image" src="https://github.com/user-attachments/assets/ea4615e7-1522-4eed-8bf2-e7f43bc2d2ba" /></td>
  </tr>
</table>

- [Decision 3.0](https://huggingface.co/FluidInference/d3-coreml) — d3-lite, nano and mini on Core ML; d3-lite triages 1,000 pull requests into vLLM-SR workgroups live on an M5 Pro at 0.12 s per PR, 8.3 PRs/s ([demo](https://x.com/Alex_tra_memory/status/2109343807854493724)) · 432 likes · 42 reposts · 28K views

<table>
  <tr>
    <td align="center" valign="top"><a href="https://x.com/ClementDelangue">@ClementDelangue</a><br><img width="420" alt="image" src="https://github.com/user-attachments/assets/c56da3f8-ad48-49bc-9b1a-81a64b4219f3" /></td>
    <td align="center" valign="top"><a href="https://x.com/victormustar">@victormustar</a><br><img width="420" alt="image" src="https://github.com/user-attachments/assets/7f8e330a-e2ac-4918-a135-5c60fb822ce9" /></td>
  </tr>
</table>


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
