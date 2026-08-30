# BertholomusAI

**Reproducible distributed LLM inference, quantization research, and evidence-backed deployment recipes for NVIDIA GB10 / DGX Spark systems.**

We publish the receipts that matter: pinned revisions, integrity manifests, exact runtime formulas, bounded capability gates, concurrency/context evidence, restart proof, limitations, licensing, and upstream credits.

## Verified public work

| Project | Topology | Focus | GitHub | Hugging Face |
|---|---:|---|---|---|
| GLM-5.3-Flash NVFP4 | 4× GB10, TP4 | 1M-configured context, FP8 KV, DFlash2, tools, multimodal and long-context gates | [Recipe + evidence](https://github.com/bertholomus/glm-5.3-flash-nvfp4-gb10-tp4) | [Evidence card](https://huggingface.co/bertholomus/GLM-5.3-Flash-NVFP4-4xGB10-TP4) |
| DeepSeek V4 Flash Graph-8 | 2× GB10 | Reproducible two-node deployment and benchmarks | [Repository](https://github.com/bertholomus/deepseek-v4-flash-0731-dspark-graph8) | [Model card](https://huggingface.co/bertholomus/DeepSeek-V4-Flash-0731-DSpark-Graph8) |
| DeepSeek V4 Flash Graph-8 | 4× GB10, TP4 | Four-node scaling, evidence and release recipe | [Repository](https://github.com/bertholomus/deepseek-v4-flash-0731-dspark-graph8-4xgb10) | [Model card](https://huggingface.co/bertholomus/DeepSeek-V4-Flash-0731-DSpark-Graph8-4xGB10) |

## Publication standard

- Attribute upstream models, checkpoints, runtimes, kernels, and recipe lineage.
- Separate configured capability from directly proven capability.
- Publish machine-readable evidence and known limitations alongside headline results.
- Never present third-party quantizations as BertholomusAI-created artifacts.
- Mirror weights only when provenance and redistribution rights are clear.
- Prefer exact revisions and hashes over mutable tags.

## Current research direction

- GLM-5.3 distributed inference on GB10 systems.
- Full-download quantization workflows with explicit authorship and reproducibility.
- Speculative decoding, long-context validation, and safe production supervision.
- Hermes-native local-agent infrastructure.

Hugging Face: [huggingface.co/bertholomus](https://huggingface.co/bertholomus) · X: [@bertholomusai](https://x.com/bertholomusai)
