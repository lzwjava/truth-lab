# ⟡ Truth Lab

A one-person AI research lab run by [Zhiwei Li](https://lzwjava.com).

Pretraining small LLMs from scratch. Serving open models. Resurrecting second-hand GPUs.
Consulting on applied AI for real engineering teams. Every experiment run at real scale
and reported honestly — including the failures.

> Truth through compute — nothing but **truth**.

## What this lab does

| Focus | What that means in practice |
|---|---|
| **Training** | GPT-2 124M / 760M from zero (not from a checkpoint) on FineWeb, OpenWebText, Wikipedia, SEC filings. Token budgeting, training-run surgery, LoRA/SFT pipelines. |
| **Inference & serving** | vLLM, SGLang (from source), llama.cpp. Quantization, KV-cache tricks, batching — with real benchmark numbers on real GPUs. |
| **GPU & hardware** | Home-built compute from second-hand parts. BIOS archaeology, VRM teardowns, thermal measurements, and an honest fight with the electricity bill. |
| **Consulting** | Applied AI inside enterprises — agent automation, LLM integration, AI-assisted engineering. Deliverables are code, logs, and numbers. |

## Selected experiments

- **[SEC-EDGAR-GPT](https://github.com/lzwjava/sec-edgar-gpt)** — a 124M GPT-2 trained from scratch on 1.55B tokens of SEC filings in ~8 hours on a single RTX 4070 (val loss 2.28). Built end-to-end in 3 days; 200+ views inside a global bank.
- **[nanoGPT fork](https://github.com/lzwjava/nanoGPT)** — karpathy/nanoGPT extended over 45 commits with FineWeb-Edu / OpenWebText / Wikipedia pipelines, six VRAM-scaled configs, and inline tensor-shape annotations.
- **[52 GB home cluster](https://github.com/lzwjava/truth-lab)** — three second-hand datacenter workstations (M40 12 GB + M40 24 GB + P100 16 GB) coaxed into life for ~100 CNY per GB of VRAM.
- **[zz](https://github.com/lzwjava/zz)** — dataset utilities: resumable FineWeb downloads, memory-safe parquet extraction, tokenization, training-duration math.
- **[FluxReel](https://github.com/lzwjava/flux-reel)** — one-line topic → 15-second vertical video on an AMD Radeon under ROCm. AMD AI DevMaster Hackathon Completion Award.

Full lab notebook (13+ training runs with statuses, hardware, and steps) lives on the [site](https://lzwjava.com).

## Hardware

- Home: RTX 4070 (12 GB) + M40 12 GB + M40 24 GB + P100 16 GB = **52 GB of CUDA VRAM**
- Cloud: NVIDIA H200 (141 GB HBM3e, RunPod/DigitalOcean), AMD MI300X (192 GB HBM3, AMD Developer Cloud)

## This repo

A single-file static site (`index.html`) — dark, minimal, typographic. No build step, no dependencies.
Bilingual (EN/ZH) with a language switcher. Open it directly, or host it anywhere.

```bash
# serve locally
python3 -m http.server 8000
```

## Contact

Open for scoped experiments and consulting engagements. Reply within a couple of days;
expect a well-thought paragraph, not a fast buzzword.
