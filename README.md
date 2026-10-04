# BertholomusAI

**Reproducible distributed LLM inference, quantization research, and evidence-backed deployment recipes for NVIDIA GB10 / DGX Spark systems.**

We publish the receipts that matter: pinned revisions, integrity manifests, exact runtime formulas, bounded capability gates, concurrency/context evidence, restart proof, limitations, licensing, and upstream credits.

## Verified public work

| Project | Topology | Focus | GitHub | Hugging Face |
|---|---:|---|---|---|
| GLM-5.3 (full, 753B) EXL3 3.0 bpw | 4× GB10, TP4 | Our own quant; TensorFold engine branch; 1M context via context parallelism; MTP drafting; KL 0.109 vs BF16 | [Recipe + benchmarks](https://github.com/bertholomus/glm-5.3-tensorfold-tp4-4xgb10) | [Weights](https://huggingface.co/bertholomus/GLM-5.3-EXL3-3.0bpw) |
| DeepSeek-V4.1-Flash on TensorFold | 2× GB10, TP2 | Clean-room `deepseek_v41` model family for TensorFold; 1M window, vision, DSpark drafting, 4-stream concurrency | [Recipe](https://github.com/bertholomus/deepseek-v4.1-tensorfold-tp2-2xgb10) | [Card](https://huggingface.co/bertholomus/DeepSeek-V4.1-Flash-TensorFold-TP2-2xGB10) |
| DeepSeek-V4.1-Flash DSpark | 4× GB10, TP4 | SGLang recipe v1.1.6: measured deviations from upstream, 1M context, 8M-token shared KV pool, systemd lane | [Recipe + evidence](https://github.com/bertholomus/deepseek-v4.1-flash-dspark-tp4-4xgb10) | [Card](https://huggingface.co/bertholomus/DeepSeek-V4.1-Flash-DSpark-TP4-4xGB10-Recipe) |
| GLM-5.3-Flash NVFP4 | 4× GB10, TP4 | 1M-configured context, FP8 KV, DFlash2, tools, multimodal and long-context gates | [Recipe + evidence](https://github.com/bertholomus/glm-5.3-flash-nvfp4-gb10-tp4) | [Evidence card](https://huggingface.co/bertholomus/GLM-5.3-Flash-NVFP4-4xGB10-TP4) |
| DeepSeek V4 Flash Graph-8 | 4× GB10, TP4 | Four-node scaling, evidence and release recipe | [Repository](https://github.com/bertholomus/deepseek-v4-flash-0731-dspark-graph8-4xgb10) | [Model card](https://huggingface.co/bertholomus/DeepSeek-V4-Flash-0731-DSpark-Graph8-4xGB10) |
| DeepSeek V4 Flash Graph-8 | 2× GB10 | Reproducible two-node deployment and benchmarks | [Repository](https://github.com/bertholomus/deepseek-v4-flash-0731-dspark-graph8) | [Model card](https://huggingface.co/bertholomus/DeepSeek-V4-Flash-0731-DSpark-Graph8) |

## Engine work and upstream contributions

- **[TensorFold](https://github.com/bertholomus/TensorFold)** (fork of [ashhart/TensorFold](https://github.com/ashhart/TensorFold)): branch [`glm-dsa-tp4`](https://github.com/bertholomus/TensorFold/tree/glm-dsa-tp4) runs the full GLM-5.3 tensor-parallel over four Sparks; branch [`deepseek-v41-tp2`](https://github.com/bertholomus/TensorFold/tree/deepseek-v41-tp2) adds DeepSeek-V4.1-Flash over two. Both are intended for upstream.
- **[MiaAI-Lab/DeepSeek-v4.1-Flash-DGX-Sparks #10](https://github.com/MiaAI-Lab/DeepSeek-v4.1-Flash-DGX-Sparks/pull/10)**: per-node active InfiniBand HCA detection for TP4 boot on mixed-port fleets.
- **[NousResearch/hermes-agent #95120](https://github.com/NousResearch/hermes-agent/pull/95120)**: durable Discord thread rename and slash-command sync.

## Publication standard

- Attribute upstream models, checkpoints, runtimes, kernels, and recipe lineage.
- Separate configured capability from directly proven capability.
- Publish machine-readable evidence and known limitations alongside headline results.
- Never present third-party quantizations as BertholomusAI-created artifacts.
- Mirror weights only when provenance and redistribution rights are clear.
- Prefer exact revisions and hashes over mutable tags.

## Current research direction

- Full GLM-5.3 on four GB10 systems: faster prefill and vision for the non-Flash model.
- New model families and multi-node tensor parallelism for TensorFold on GB10.
- Full-download quantization workflows with explicit authorship and reproducibility.
- Speculative decoding, long-context validation, and safe production supervision.
- Hermes-native local-agent infrastructure.

Hugging Face: [huggingface.co/bertholomus](https://huggingface.co/bertholomus) · X: [@bertholomusai](https://x.com/bertholomusai)
