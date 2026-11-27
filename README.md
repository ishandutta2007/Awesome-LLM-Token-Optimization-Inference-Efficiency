# Awesome-LLM-Token-Optimization-Inference-Efficiency

# Awesome-LLM-Token-Optimization-Inference-Efficiency



Top LLM Token Optimization Inference Efficiency (Opensource) 🌟 Star if you like it! 🌟



A curated list of top LLM token optimization frameworks, prompt compression & pruning engines, high-efficiency GPU/CPU inference runtimes, speculative decoding systems, and KV-cache reuse engines—featuring commercial SaaS/Hosted platforms alongside their open-source equivalents.



---



## Table of Contents



- [SaaS/Hosted Platforms](#saashosted-platforms)

- [Open-Source Equivalents & Tools](#open-source-equivalents--tools)

  - [Token Optimization, Prompt Compression & Pruning Engines](#token-optimization-prompt-compression--pruning-engines)

  - [High-Throughput GPU LLM Inference & Serving Engines](#high-throughput-gpu-llm-inference--serving-engines)

  - [Speculative Decoding & Fast Token Generation Frameworks](#speculative-decoding--fast-token-generation-frameworks)

  - [KV-Cache Compression, Paging & Prefix Reuse Systems](#kv-cache-compression-paging--prefix-reuse-systems)

  - [Constrained Decoding & Zero-Overhead Structured Output](#constrained-decoding--zero-overhead-structured-output)

- [Contributing](#contributing)



---



## SaaS/Hosted Platforms



Commercial, cloud-hosted ultra-fast inference clouds, specialized LPU/WSE/RDU hardware endpoints, and managed high-efficiency LLM serving APIs.



* **[GroqCloud (Groq LPU)](https://groq.com)** - Deterministic Language Processing Unit (LPU) cloud inference platform delivering hundreds of tokens per second with ultra-low time-to-first-token.

* **[Cerebras Inference Cloud](https://cerebras.ai)** - Wafer-Scale Engine (WSE) cloud platform eliminating off-chip memory bandwidth bottlenecks for massive token generation throughput.

* **[SambaNova Cloud](https://sambanova.ai)** - Enterprise AI inference cloud running on Reconfigurable Dataflow Units (RDUs) optimized for high-efficiency, long-context model serving.

* **[DeepSeek API & DeepSeek-V3 Engine](https://deepseek.com)** - Commercial API powered by Multi-Head Latent Attention (MLA), FP8 training/inference, and automatic disk context caching.

* **[Together Turbo (Together AI)](https://together.ai)** - Managed cloud inference engine combining FlashAttention-3, FP8 quantization, and speculative decoding for rapid token throughput.

* **[Fireworks AI (Fast Inference)](https://fireworks.ai)** - High-speed serverless and dedicated inference cloud utilizing custom CUDA kernels, multi-LoRA packing, and prompt caching.

* **[NVIDIA NIM (TensorRT-LLM Cloud)](https://nvidia.com)** - Enterprise managed microservices packaging TensorRT-LLM with FP8/INT4 quantization and in-flight batching.

* **[FriendliAI](https://friendli.ai)** - Managed high-efficiency LLM serving cloud featuring iteration-level continuous batching and adaptive GPU scheduling.

* **[Baseten](https://baseten.co)** - Commercial model serving infrastructure providing autoscaling GPU clusters, cold-start optimization, and TensorRT-LLM runtimes.

* **[Portkey](https://portkey.ai)** - Enterprise AI gateway offering semantic caching, fallback routing, and token budget governance across LLM providers.



---



## Open-Source Equivalents & Tools



Free and open-source software (FOSS) token optimizers, prompt compressors, PagedAttention/RadixAttention serving engines, speculative decoders, and KV-cache compressors.



### Token Optimization, Prompt Compression & Pruning Engines



* **[FreeToken (flashml-org)](https://github.com)** - Open-source token optimization and inference efficiency toolkit engineered to maximize token throughput and minimize redundant token overhead.

* **[LLMLingua & LongLLMLingua (Microsoft)](https://github.com)** - Industry-leading open-source prompt compression framework achieving up to 20x token reduction for RAG, CoT, and long-context prompts.

* **[Optillm](https://github.com)** - Open-source OpenAI-API-compatible optimizing inference proxy implementing 15+ test-time compute and decoding optimizations to elevate smaller models.

* **[Selective Context](https://github.com)** - Open-source utility pruning redundant lexical units in prompts based on self-information to accelerate prefill and reduce token count.

* **[TOON (Token-Oriented Object Notation)](https://github.com)** - Compact, human-readable open-source data serialization format replacing verbose JSON in LLM prompts to cut structural tokens by 30%–60%.

* **[DSPy (Stanford NLP)](https://github.com)** - Declarative open-source framework that algorithmically compiles concise, token-efficient prompts and weights for smaller models.



### High-Throughput GPU LLM Inference & Serving Engines



* **[vLLM (PagedAttention)](https://github.com)** - The industry-standard open-source high-throughput LLM serving engine maximizing GPU utilization via PagedAttention and continuous batching.

* **[TensorRT-LLM (NVIDIA)](https://github.com)** - Open-source C++/CUDA library compiling LLMs into optimized TensorRT engines with FP8/INT4 quantization, in-flight batching, and tensor parallelism.

* **[SGLang](https://github.com)** - Blazingly fast open-source serving runtime featuring RadixAttention automatic prefix caching and zero-overhead CPU scheduling.

* **[LMDeploy (InternLM)](https://github.com)** - High-efficiency open-source toolkit powered by the C++/CUDA TurboMind engine supporting persistent batching and online KV quantization.

* **[Text Generation Inference (TGI - Hugging Face)](https://github.com)** - Production-grade open-source Rust and Python serving toolkit with continuous batching, FlashAttention, and tensor parallelism.

* **[Aphrodite Engine](https://github.com)** - High-throughput open-source inference engine combining PagedAttention with extensive low-bit quantization formats (EXL2, AWQ, GPTQ, FP8).

* **[llama.cpp](https://github.com)** - Foundational open-source C/C++ inference engine enabling high-efficiency quantized execution across CPUs, NVIDIA/AMD GPUs, and Apple Metal.



### Speculative Decoding & Fast Token Generation Frameworks



* **[EAGLE / EAGLE-2 / EAGLE-3](https://github.com)** - State-of-the-art open-source speculative decoding framework accelerating LLM generation by 3x–5x via feature-level auto-regression.

* **[Medusa](https://github.com)** - Open-source framework adding extra decoding heads to LLMs to predict multiple tokens per step without needing a separate draft model.

* **[Lookahead Decoding](https://github.com)** - Exact, lossless open-source parallel decoding algorithm accelerating LLM inference without draft models or data stores.

* **[SpecForge (SGLang)](https://github.com)** - Open-source training and serving toolkit for building custom speculative decoding draft models tailored for high-throughput production.



### KV-Cache Compression, Paging & Prefix Reuse Systems



* **[LMCache](https://github.com)** - Open-source KV-cache storage and reuse engine sharing precomputed prompt KV states across GPU, CPU DRAM, and disk to slash prefill compute.

* **[Mooncake (Moonshot AI)](https://github.com)** - KVCache-centric disaggregated open-source serving architecture pooling distributed DRAM and SSD resources for high-efficiency inference.

* **[FlashInfer](https://github.com)** - High-performance open-source kernel library providing customized paged attention, cascade attention, and compressed KV-cache kernels.

* **[FlashAttention-3 (Tri Dao)](https://github.com)** - IO-aware exact attention CUDA kernels maximizing Tensor Core and HBM efficiency on Hopper/Blackwell GPUs.

* **[KIVI](https://github.com)** - Tuning-free asymmetric 2-bit KV-cache quantization framework slashing memory footprint and boosting batch size throughput.

* **[H2O (Heavy-Hitter Oracle)](https://github.com)** - Open-source KV-cache eviction policy retaining critical heavy-hitter tokens to reduce memory bandwidth bottlenecks.



### Constrained Decoding & Zero-Overhead Structured Output



* **[LLGuidance](https://github.com)** - Ultra-fast Rust-based context-free grammar (CFG) and JSON schema constraint engine with token fast-forwarding to skip boilerplate tokens.

* **[XGrammar (MLC)](https://github.com)** - High-speed open-source structured generation engine achieving near-zero overhead token masking for JSON and regex schemas.

* **[Outlines](https://github.com)** - Open-source structured text generation library using finite-state machines to guarantee valid schemas without wasted retry tokens.

* **[Guidance](https://github.com)** - Open-source constrained generation framework interleaving control logic and token fast-forwarding for efficient structured outputs.



---



## Contributing



Contributions are welcome! Feel free to open a Pull Request to add more open-source LLM token optimization tools, prompt compressors, high-efficiency inference engines, or speculative decoding frameworks.



1. Fork the repository.

2. Add your project under the appropriate category with a concise description.

3. Submit a Pull Request.
