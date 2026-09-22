### Hello, I'm Alex

I build fast, private AI that runs on your device. My work spans speech models on the Apple Neural Engine, browser inference with WebGPU, and small models that can act in Mac apps.

#### Recent work
- Built [FluidAudio](https://github.com/FluidInference/FluidAudio), a Swift SDK for local transcription, text-to-speech, voice activity detection, and speaker diarization, now used by [many apps](https://github.com/FluidInference/FluidAudio#showcase).
- Brought local speech AI to the browser with [FluidAudio Web](https://github.com/FluidInference/fluidaudio-web): hand-written WebGPU and WASM kernels for ASR, TTS, VAD, and diarization. Its [documented Parakeet benchmark](https://github.com/FluidInference/fluidaudio-web#fluidaudio-web) transcribes one hour of audio in about 12 seconds in Chrome on macOS.
- Released [FluidUse](https://github.com/FluidInference/FluidUse), which uses a small Core ML model and the macOS Accessibility API to fill forms in running apps entirely on-device.
- My [Core ML models](https://huggingface.co/FluidInference) previously reached **500,000+ downloads in a month** across the collection; [Parakeet TDT v3](https://huggingface.co/FluidInference/parakeet-tdt-0.6b-v3-coreml) passed **1 million total downloads** and peaked at **500,000 in a month**.

#### What I Do
- Convert and optimize PyTorch models for Core ML and the Apple Neural Engine
- Build real-time speech systems for transcription, speaker diarization, TTS, and VAD
- Develop local inference tools across Apple silicon, WebGPU, and other accelerators

#### Contributions

**On-device AI and developer tools**
- [FluidAudio](https://github.com/FluidInference/FluidAudio) — speech AI SDK for iOS and macOS
- [FluidAudio Web](https://github.com/FluidInference/fluidaudio-web) — local speech AI in the browser with WebGPU and WebAssembly
- [FluidUse](https://github.com/FluidInference/FluidUse) — on-device computer use for Mac apps
- [möbius](https://github.com/FluidInference/mobius) — model conversion and deployment across accelerators
- [text-processing-rs](https://github.com/FluidInference/text-processing-rs) — Rust text normalization for ASR and TTS
- [fluidaudio-rs](https://github.com/FluidInference/fluidaudio-rs) and [react-native-fluidaudio](https://github.com/FluidInference/react-native-fluidaudio) — Rust and React Native integrations for FluidAudio
- [FluidVad](https://github.com/FluidInference/FluidVad) — lightweight voice activity detection for Electron apps
- [fluidtop](https://github.com/FluidInference/fluidtop) — macOS performance monitoring for AI workloads
- [mlx-mdx](https://github.com/FluidInference/mlx-mdx) — local document-to-Markdown conversion with MLX

**Apps and open-source collaborations**
- [swift-scribe](https://github.com/FluidInference/swift-scribe) — local dictation and summarization for Apple devices
- [mlx-audio](https://github.com/Blaizzy/mlx-audio) — speech processing with Apple MLX
- [OpenOats](https://github.com/yazinsai/OpenOats) — local meeting transcription
- [vLLM Semantic Router](https://github.com/vllm-project/semantic-router) — [merged fixes](https://github.com/vllm-project/semantic-router/pulls?q=is%3Apr+author%3AAlex-Wengg+is%3Amerged) for RAG result ranking and Playground feedback
- [Supertonic](https://github.com/supertone-inc/supertonic) — multilingual TTS support on iOS
- [Jobpulse](https://jobpulse.fyi/) — AI-powered job search for beginners


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
