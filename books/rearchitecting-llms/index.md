---
layout: default
title: Rearchitecting LLMs — Pere Martra
description: A practical guide to turning large pre-trained language models into small, efficient models specialized for a domain.
image: /assets/images/cover.jpg
image_alt: Cover of Rearchitecting LLMs
---

<header class="book-header">
  <div class="book-intro">
    <h1>Rearchitecting LLMs</h1>
    <p class="subtitle">Structural techniques for efficient models</p>
    <p class="meta">Manning Early Access Program (MEAP), since January 2026. Publication estimated for Spring 2027.</p>
    <p class="cta"><a class="button" rel="sponsored noopener" href="https://hubs.la/Q040tvsK0">Read it at Manning</a></p>
    <p class="note">Affiliate link: I may earn a commission on purchases.</p>
  </div>
  <img class="cover" src="{{ '/assets/images/cover.jpg' | relative_url }}" width="720" height="922" alt="Cover of Rearchitecting LLMs">
</header>

<section markdown="1">

## About the book

A practical guide to turning large pre-trained language models into small, efficient models specialized for a domain. Instead of treating a model as a black box, the book works on its architecture: removing the layers and neurons that do not contribute to the goal (depth and width pruning), recovering capability through knowledge distillation, and specializing the result with LoRA-based fine-tuning. It also introduces methods of my own, such as fair pruning, which reduces bias at the neuron level, and adaptive attention bypass for dynamic inference.

</section>

<section markdown="1">

## Why I wrote it

It grew out of my own optimization projects, where the techniques were scattered across papers, often without reproducible code. The book unifies them into a coherent, practical pipeline. [Read the preface →](https://livebook.manning.com/book/rearchitecting-llms/welcome)

</section>

<section markdown="1">

## Built on published research

The core techniques are similar in spirit to those behind NVIDIA's Minitron and Mistral's Ministral model families. The book adapts them to smaller models, limited data and modest GPUs. The main papers behind each chapter are listed below.

</section>

<section markdown="1">

## Who it's for

AI, ML and data engineers who know Python and want to go beyond fine-tuning, with some knowledge of PyTorch and curiosity about what happens inside a transformer.

</section>

<section markdown="1">

## Hands-on

Every chapter comes with notebooks that run on the free tier of Google Colab, using open models such as Llama, Gemma and Qwen.

</section>

<section markdown="1">

## Chapters published so far

### Part 1 · Foundations

- 1 · Why rearchitecting LLMs matters — The case for specialized models over generic LLMs
- 2 · [An end-to-end rearchitecting project](https://github.com/peremartra/Rearchitecting-LLMs/blob/main/CH02) — Full pipeline: prune and recover
- 3 · [A blueprint to modern transformers](https://github.com/peremartra/Rearchitecting-LLMs/blob/main/CH03) — GLU architectures, attention, and model internals
{: .chapters}

### Part 2 · Hands-on optimization

- 4 · [Building smaller and faster LLMs with depth pruning](https://github.com/peremartra/Rearchitecting-LLMs/blob/main/CH04) — Block removal, capturing block importance with Python hooks, evaluating pruning
- 5 · [Shaping model architectures via width pruning](https://github.com/peremartra/Rearchitecting-LLMs/blob/main/CH05) — GLU neuron selection, data-driven pruning strategies
- 6 · [Knowledge recovery through distillation](https://github.com/peremartra/Rearchitecting-LLMs/blob/main/CH06) — Recovering capability after structural compression
- 7 · [Model specialization](https://github.com/peremartra/Rearchitecting-LLMs/blob/main/CH07) — LoRA / DoRA fine-tuning and quantization for domain tasks
- 8 · [Attention optimization](https://github.com/peremartra/Rearchitecting-LLMs/blob/main/CH08) — KV cache, attention bypass, inference acceleration
- 9 · [Dynamic routing with Mixture of Experts](https://github.com/peremartra/Rearchitecting-LLMs/blob/main/CH09) — Mixture of Experts (MoE) adapted to SLMs
{: .chapters}

### Part 3 · Beyond the black box

- 10 · [Exploring the transformer black box](https://github.com/peremartra/Rearchitecting-LLMs/blob/main/CH10) — Activation analysis and behavioral interpretability
{: .chapters}

More chapters are being written and will be added here as they are published.

</section>

<section markdown="1">

## Papers behind each chapter

### 1 · Why rearchitecting LLMs matters

- [FineScope: Precision Pruning for Domain-Specialized Large Language Models Using SAE-Guided Self-Data Cultivation](https://arxiv.org/abs/2505.00624)
- [LLM Pruning and Distillation in Practice: The Minitron Approach](https://arxiv.org/abs/2408.11796)
{: .papers}

### 2 · An end-to-end rearchitecting project

- [Shortened LLaMA: Depth Pruning for Large Language Models with Comparison of Retraining Methods](https://arxiv.org/abs/2402.02834)
{: .papers}

### 3 · A blueprint to modern transformers

- [Attention Is All You Need](https://dl.acm.org/doi/10.5555/3295222.3295349)
- [Fast Transformer Decoding: One Write-Head is All You Need](https://arxiv.org/abs/1911.02150)
- [GQA: Training Generalized Multi-Query Transformer Models from Multi-Head Checkpoints](https://arxiv.org/abs/2305.13245)
- [GLU Variants Improve Transformer](https://arxiv.org/abs/2002.05202)
- [Exploring GLU Expansion Ratios: Structured Pruning in Llama-3.2 Models](https://osf.io/preprints/osf/qgxea)
{: .papers}

### 4 · Building smaller and faster LLMs with depth pruning

- [ShortGPT: Layers in Large Language Models are More Redundant Than You Expect](https://arxiv.org/abs/2403.03853)
- [Shortened LLaMA: Depth Pruning for Large Language Models with Comparison of Retraining Methods](https://arxiv.org/abs/2402.02834)
{: .papers}

### 5 · Shaping model architectures via width pruning

- [Dependency-Aware Semi-Structured Sparsity of GLU Variants in Large Language Models](https://arxiv.org/abs/2405.01943)
- [CFSP: An Efficient Structured Pruning Framework for LLMs with Coarse-to-Fine Activation Information](https://arxiv.org/abs/2409.13199)
- [Fragile Knowledge, Robust Instruction-Following: The Width Pruning Dichotomy in Llama-3.2](https://arxiv.org/abs/2512.22671)
{: .papers}

### 6 · Knowledge recovery through distillation

- [Distillation Dynamics: Towards Understanding Feature-Based Distillation in Vision Transformers](https://arxiv.org/abs/2511.06848)
- [DistiLLM-2: A Contrastive Approach Boosts the Distillation of LLMs](https://arxiv.org/abs/2503.07067)
- [LLM Pruning and Distillation in Practice: The Minitron Approach](https://arxiv.org/abs/2408.11796)
- [Ministral 3](https://arxiv.org/abs/2601.08584)
{: .papers}

### 7 · Model specialization

- [LoRA: Low-Rank Adaptation of Large Language Models](https://arxiv.org/abs/2106.09685)
- [QLoRA: Efficient Finetuning of Quantized LLMs](https://arxiv.org/abs/2305.14314)
- [DoRA: Weight-Decomposed Low-Rank Adaptation](https://arxiv.org/abs/2402.09353)
- [Fine-Tuning LLMs on Small Medical Datasets: Text Classification and Normalization Effectiveness on Cardiology reports and Discharge records](https://arxiv.org/abs/2503.21349)
{: .papers}

### 8 · Attention optimization

- [What Matters in Transformers? Not All Attention is Needed](https://arxiv.org/abs/2406.15786)
{: .papers}

### 9 · Dynamic routing with Mixture of Experts

- [Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://arxiv.org/abs/1701.06538)
- [Mixtral of Experts](https://arxiv.org/abs/2401.04088)
- [Sparse Upcycling: Training Mixture-of-Experts from Dense Checkpoints](https://arxiv.org/abs/2212.05055)
{: .papers}

### 10 · Exploring the transformer black box

- [Eliciting Latent Predictions from Transformers with the Tuned Lens](https://arxiv.org/abs/2303.08112)
{: .papers}

</section>

<section markdown="1">

## Companion resources

- [Code and notebooks](https://github.com/peremartra/Rearchitecting-LLMs)
- [Hands-on labs](https://github.com/peremartra/Rearchitecting-LLMs/discussions?discussions_q=is%3Aopen+label%3A%22hands-on+labs%22) (GitHub Discussions)
- [Companion models](https://huggingface.co/collections/oopere/rearchitecting-llms) (Hugging Face collection)
- [OptiPFair library](https://github.com/peremartra/optipfair)
- Related research: [Fairness Pruning, arXiv:2607.28319](https://arxiv.org/abs/2607.28319)
{: .resources}

</section>

<section markdown="1">

## Cite the book

Martra, P. (2026). Rearchitecting LLMs: Structural techniques for efficient models. Manning Publications. ISBN 9781633434332. (Manning Early Access Program)
{: .citation}

</section>
