**Open-source collaborations and apps**
- [vLLM](https://github.com/vllm-project/vllm) (**96K+ ⭐**) — 10 commits merged to `main`, in the top ~9% of its ~3,700 contributors
  <details><summary>PRs</summary>

  - Added NVIDIA Canary ([canary-1b-v2](https://huggingface.co/nvidia/canary-1b-v2)): speech recognition and X↔English speech translation in 25 European languages, served through the OpenAI-compatible audio API; output is token-identical to Transformers, with 12.34 WER on earnings22 ([#64215](https://github.com/vllm-project/vllm/pull/64215))
  - Made Canary transcription return a 400 when `language` is missing, instead of silently answering non-English audio in English, and added CI coverage for Canary translation ([#65445](https://github.com/vllm-project/vllm/pull/65445))
  - Built [vllm-parakeet-plugin](https://github.com/Alex-Wengg/vllm-parakeet-plugin) for NVIDIA Parakeet TDT v3 ([parakeet-tdt-0.6b-v3](https://huggingface.co/nvidia/parakeet-tdt-0.6b-v3)), now listed in vLLM's supported models ([#65005](https://github.com/vllm-project/vllm/pull/65005)): batched greedy TDT decoding on the GPU with its own CUDA graphs; 73/73 transcripts token-identical to Transformers, and LibriSpeech WER 1.93% / 3.61% through `vllm serve` (model card: 1.93% / 3.59%)
  - Built [vllm-nemotron-diarization-plugin](https://github.com/Alex-Wengg/vllm-nemotron-diarization-plugin) for NVIDIA [Nemotron-3-Diarization](https://huggingface.co/nvidia/Nemotron-3-Diarization), now listed in vLLM's supported models ([#65199](https://github.com/vllm-project/vllm/pull/65199)): speaker diarization of up to 8 speakers at 10 ms resolution through vLLM's `LLM` API with one `pip install`; logits within 2e-5 of Transformers, with identical speaker segments
  - Fixed `main`'s failing pre-commit after two merged PRs collided on Muse Spark's weight-loading hook, which also restored its ROCm monokernel path ([#65080](https://github.com/vllm-project/vllm/pull/65080))
  - Fixed chat derender misclassifying answers as reasoning: the reasoning and tool parsers never saw the prompt in the usual render → generate → derender flow, so they now fall back to the caller's prompt token IDs ([#63434](https://github.com/vllm-project/vllm/pull/63434))
  - Moved Gemma 4's image normalization from the CPU processor onto the GPU (`mm_device_do_normalize`), with a perplexity test against the CPU path ([#65577](https://github.com/vllm-project/vllm/pull/65577))
  - Extended GPU image normalization to Gemma 4 Unified (the 12B checkpoints), and turned back on 36 of its processor tests that CI had been skipping ([#65724](https://github.com/vllm-project/vllm/pull/65724))
  - Fixed CLIP and SigLIP returning a different embedding for text sent as chat `messages` than for the same text sent as `input`: the fallback chat template dropped the tokenizer's BOS/EOS, so each model now gets a template that keeps them ([#66417](https://github.com/vllm-project/vllm/pull/66417))
  - Fixed the same mismatch for SigLIP2: its checkpoints ship Gemma's chat template, which vLLM ranked above its own, so SigLIP models now use the SigLIP template and the NaFlex variants keep EOS too; also opened the matching fix on the Hugging Face Hub ([#66624](https://github.com/vllm-project/vllm/pull/66624), [Hub PR](https://huggingface.co/google/siglip2-base-patch16-224/discussions/23))

  </details>
- [SGLang](https://github.com/sgl-project/sglang) — fixed the diffusion LoRA merge cache silently reusing stale merged weights after an adapter is rewritten in place, with regression tests ([#44204](https://github.com/sgl-project/sglang/pull/44204)), and made a diffusion worker exit after an unrecoverable CUDA error, instead of serving on a broken device while /health still reported ok ([#45065](https://github.com/sgl-project/sglang/pull/45065)) (**40K+ ⭐**)
- <details><summary><a href="https://github.com/can1357/oh-my-pi">oh-my-pi</a> (<b>38K+ ⭐</b>) — 7 PRs merged to <code>main</code>, in the top ~8% of its ~850 PR authors</summary>

  - `lsp reload` now stops a superseded shared language server instead of leaving it running for 5 minutes ([#18254](https://github.com/can1357/oh-my-pi/pull/18254))
  - `omp stats` no longer re-parses every session after ZFS renumbers the filesystem's device ([#18536](https://github.com/can1357/oh-my-pi/pull/18536))
  - Rendered SVGs no longer drop their text when a generic font family names a font that isn't installed ([#18538](https://github.com/can1357/oh-my-pi/pull/18538))
  - `worktree add` no longer fails on read-only files copied from the source checkout ([#18537](https://github.com/can1357/oh-my-pi/pull/18537))
  - Prompt-history search no longer returns unrelated prompts for punctuated queries like `a/b` ([#19111](https://github.com/can1357/oh-my-pi/pull/19111))
  - ACP clients now see what background subagents spend ([#19113](https://github.com/can1357/oh-my-pi/pull/19113))
  - The browser tool records non-Error page rejections as JSON instead of a bare `Object` ([#18251](https://github.com/can1357/oh-my-pi/pull/18251))

  </details>
- [vLLM Semantic Router](https://github.com/vllm-project/semantic-router) (**6.4K+ ⭐**) — 6 commits merged to `main`, in the top ~22% of its ~290 contributors
  <details><summary>Workgroup member, Decision 3.0 Core ML port and blog post, trusted-gateway credentials, 3 fixes</summary>

  - Member of two [workgroups](https://vllm-sr.ai/community/work-groups): **Router Models & Inference Runtime** and **Developer Experience & Ecosystem**
  - Early access to [Decision 3.0](https://huggingface.co/collections/vllm-sr/decision-30): ported d3 to Core ML ([d3-coreml](https://huggingface.co/FluidInference/d3-coreml))
  - Wrote the [Decision 3.0 on Apple Silicon](https://vllm-sr.ai/blog/decision-3-0-on-apple-silicon) blog post: d3-lite, nano and mini on Core ML, matching upstream on JevBench and typed-decisions, 2.5–4× faster per request on a Mac ([#4905](https://github.com/vllm-project/semantic-router/pull/4905), [#4975](https://github.com/vllm-project/semantic-router/pull/4975))
  - Added trusted-gateway credentials: the Router forwards a credential the deployment injects only to backends marked as trusted gateways (LiteLLM/one-api style relays), never the client's raw `Authorization` header, and fails closed with a 401 ([#5144](https://github.com/vllm-project/semantic-router/pull/5144))
  - Fixed external RAG result ranking across query windows ([#3750](https://github.com/vllm-project/semantic-router/pull/3750))
  - Secured Playground feedback for read users ([#3755](https://github.com/vllm-project/semantic-router/pull/3755))
  - Hardened Dashboard API authorization with mutation-boundary rechecks ([a3174df](https://github.com/vllm-project/semantic-router/commit/a3174df365c496cbcc1f01ca6137061556618781))

  </details>

<details><summary><b>7 more:</b> Cua (32K+ ⭐), PEFT (21K+ ⭐), Supertonic (13.7K+ ⭐), NVIDIA Dynamo (8.4K+ ⭐), mlx-audio (8.2K+ ⭐), vLLM-Omni (7.7K+ ⭐), KServe (6.2K+ ⭐)</summary>

- [Cua](https://github.com/trycua/cua) — stopped the Windows driver from moving windows off their Task View virtual desktop when it clicks in the background; re-landed by a maintainer as [#7644](https://github.com/trycua/cua/pull/7644) with me as co-author, from [#5782](https://github.com/trycua/cua/pull/5782) (**32K+ ⭐**)
- [PEFT](https://github.com/huggingface/peft) — fixed FRoD and EVA initialization crashing on Apple Silicon, where MPS has no float64, and the 13 test failures Hugging Face's new macOS CI found ([#4102](https://github.com/huggingface/peft/pull/4102)) (**21K+ ⭐**)
- [Supertonic](https://github.com/supertone-oss-archive/supertonic) — ported Supertonic 3 to Core ML for Apple Neural Engine inference on iOS and macOS (conversion [mobius#64](https://github.com/FluidInference/mobius/pull/64), runtime [FluidAudio#617](https://github.com/FluidInference/FluidAudio/pull/617)) (**13.7K+ ⭐**)
- [NVIDIA Dynamo](https://github.com/ai-dynamo/dynamo) — improved disaggregated serving and inference infrastructure: made the prefill router fail closed with a retryable 503 while a target activates ([#16736](https://github.com/ai-dynamo/dynamo/pull/16736)), sized multimodal cache budgets for DeepStack embeddings ([#17249](https://github.com/ai-dynamo/dynamo/pull/17249)), fixed DCGM metrics scrape connection handling ([#17387](https://github.com/ai-dynamo/dynamo/pull/17387)), and made the profiler size Hub checkpoints from their weight files instead of a parameter-count estimate that overstated quantized models 2–3× ([#17563](https://github.com/ai-dynamo/dynamo/pull/17563)) (**8.4K+ ⭐**)
  <details><summary>Featured in ai-dynamo.org updates</summary>

  https://ai-dynamo.org/#updates

  <img width="996" height="703" alt="image" src="https://github.com/user-attachments/assets/0d6fceca-322d-4a5d-b6d5-8373f94bdc3b" />

  </details>
- [mlx-audio](https://github.com/Blaizzy/mlx-audio) — added Kokoro-82M v1.1 Mandarin support in MLX ([#341](https://github.com/Blaizzy/mlx-audio/pull/341)) (**8.2K+ ⭐**)
- [vLLM-Omni](https://github.com/vllm-project/vllm-omni) — added Kokoro-82M, the most-downloaded open TTS model, as a native single-stage TTS: loads hexgrad's checkpoint as-is with output identical to the reference package, all 54 voices in 9 languages, streaming behind an OpenAI-compatible endpoint ([#9637](https://github.com/vllm-project/vllm-omni/pull/9637)) (**7.7K+ ⭐**)
- [KServe](https://github.com/kserve/kserve) — made KEDA autoscaling honor the target type an InferenceService sets for External and PodMetric metrics, instead of silently defaulting to AverageValue ([#6185](https://github.com/kserve/kserve/pull/6185)), and fixed in-flight gRPC requests failing on SIGTERM by unloading models only after the servers drain ([#6488](https://github.com/kserve/kserve/pull/6488)) (**6.2K+ ⭐**)

</details>


**Projects I work on** — at [Fluid Inference](https://github.com/FluidInference), which was acquired by Levenza
- [FluidAudio](https://github.com/FluidInference/FluidAudio) — speech AI SDK for iOS and macOS (3.2K+ ⭐)
  - Supports dozens of commercial [applications](https://github.com/FluidInference/FluidAudio#showcase)
  - [Parakeet TDT V3 Core ML](https://huggingface.co/FluidInference/parakeet-tdt-0.6b-v3-coreml): nearly 3,000,000 total downloads, peaked at 500,000 monthly downloads
- [FluidUse](https://github.com/FluidInference/FluidUse) — Core ML runtimes for decision models in Swift, including Decision 3.0 (`D3Manager`)
  <details><summary>Some Experiment Highlights: laya, GLiNER2.5-Decide, EmbeddingGemma 2, clef-text-0.6B, Decision 3.0</summary>

  - [laya](https://huggingface.co/FluidInference/laya-coreml) — Convai's typed decision model with 99.5% of ops on the Apple Neural Engine, 3.7 ms per decision on an M5 Pro ([demo](https://x.com/Alex_tra_memory/status/2102161088598970783)) · 1,323 likes · 111 reposts · 120K views
    <details><summary>Reactions on X: jackzampolin, JiliJeanlouis, ClementDelangue, victormustar</summary>

    <table>
      <tr>
        <td align="center" valign="top"><a href="https://x.com/jackzampolin/status/2102441521048080627?s=20">@jackzampolin</a><br><img width="200" alt="image" src="https://github.com/user-attachments/assets/41622204-29e3-4eb7-9ebd-b1dd5bc76780" /></td>
        <td align="center" valign="top"><a href="https://x.com/JiliJeanlouis">@JiliJeanlouis</a><br><img width="200" alt="image" src="https://github.com/user-attachments/assets/7015727f-aca7-4d3c-820d-5ad907cab993" /></td>
        <td align="center" valign="top"><a href="https://x.com/ClementDelangue/reposts">@ClementDelangue reposts</a><br><img width="200" alt="image" src="https://github.com/user-attachments/assets/5a1038f2-a405-4f04-9080-54ec8f36a1cb" /></td>
        <td align="center" valign="top"><a href="https://x.com/victormustar">@victormustar</a><br><img width="200" alt="image" src="https://github.com/user-attachments/assets/0f93e41e-9dc7-4587-88a9-bb9a494f71f3" /></td>
      </tr>
    </table>

    </details>
  - [GLiNER2.5-Decide](https://huggingface.co/FluidInference/gliner2-5-decide-coreml) — Fastino's 340M decision model on Core ML: ~4× faster, ~5× less peak RAM, half the size ([demo](https://x.com/Alex_tra_memory/status/2103558426618163708)) · 880 likes · 83 reposts · 69K views
    <details><summary>Reactions on X: fastinoAI</summary>

    https://x.com/fastinoAI

    <img width="458" height="539" alt="image" src="https://github.com/user-attachments/assets/028204a7-aaa5-405d-8b84-195c22c9b7a9" />

    </details>
  - [EmbeddingGemma 2](https://huggingface.co/FluidInference/embeddinggemma-2-coreml) — text encoder 100% on the Apple Neural Engine; sorts 10,080 posts into topics live at ~620/s on a MacBook, any topic splits into subtopics in under a second ([demo](https://x.com/Alex_tra_memory/status/2108391275560931355)) · 693 likes · 51 reposts · 34K views
    <details><summary>Reactions on X: SeraAndroid, googlegemma</summary>

    https://x.com/SeraAndroid/status/2108629662238961694?s=20

    https://x.com/googlegemma/status/2115150306032193954

    <img width="447" height="528" alt="image" src="https://github.com/user-attachments/assets/247416a5-9d37-434f-8342-8a941799eebd" />

    <img width="443" height="450" alt="image" src="https://github.com/user-attachments/assets/2c3ad9bd-0bec-47e0-bac9-4d4dd1b45d06" />

    </details>
  - [clef-text-0.6B](https://huggingface.co/FluidInference/clef-text-0.6b-coreml) — distilled Cloudflare's 9B clef-flash into a 0.6B decision model that runs 100% on the Apple Neural Engine; 1,000 support tickets triaged in 57 s on an M5 Pro, 48 ms per ticket, within a few points of the 9B on classification ([demo](https://x.com/Alex_tra_memory/status/2108959518386458695)) · 494 likes · 45 reposts · 32K views
    <details><summary>Reactions on X: art_zucker, ClementDelangue</summary>

    <table>
      <tr>
        <td align="center" valign="top"><a href="https://x.com/art_zucker/reposts">@art_zucker reposts</a><br><img width="420" alt="image" src="https://github.com/user-attachments/assets/99e45041-eebe-47ca-ab36-5b586fddf701" /></td>
        <td align="center" valign="top"><a href="https://x.com/ClementDelangue/reposts">@ClementDelangue reposts</a><br><img width="420" alt="image" src="https://github.com/user-attachments/assets/ea4615e7-1522-4eed-8bf2-e7f43bc2d2ba" /></td>
      </tr>
    </table>

    </details>
  - [Decision 3.0](https://huggingface.co/FluidInference/d3-coreml) — d3-lite, nano and mini on Core ML; d3-lite triages 1,000 pull requests into vLLM-SR workgroups live on an M5 Pro at 0.12 s per PR, 8.3 PRs/s ([demo](https://x.com/Alex_tra_memory/status/2109343807854493724)) · 432 likes · 42 reposts · 28K views
    <details><summary>Reactions on X: ClementDelangue, victormustar</summary>

    <table>
      <tr>
        <td align="center" valign="top"><a href="https://x.com/ClementDelangue">@ClementDelangue</a><br><img width="420" alt="image" src="https://github.com/user-attachments/assets/c56da3f8-ad48-49bc-9b1a-81a64b4219f3" /></td>
        <td align="center" valign="top"><a href="https://x.com/victormustar">@victormustar</a><br><img width="420" alt="image" src="https://github.com/user-attachments/assets/7f8e330a-e2ac-4918-a135-5c60fb822ce9" /></td>
      </tr>
    </table>

    </details>

  </details>

  <details><summary>Its distilled & finetuned models brought 1,000+ Twitter <a href="https://x.com/Alex_tra_memory">followers</a> in <a href="https://x.com/Alex_tra_memory/status/2111887700282466530?s=20">1 month</a></summary>

  <img width="450" alt="1,001 Twitter followers" src="https://github.com/user-attachments/assets/02e74268-c2e9-4936-bf22-2eec2b5e6f48" />

  </details>
- [möbius](https://github.com/FluidInference/mobius) — model conversion and deployment across accelerators
  - 500,000+ monthly model downloads across the Core ML models on [FluidInference](https://huggingface.co/FluidInference)
