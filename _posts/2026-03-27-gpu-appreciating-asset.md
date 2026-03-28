---
layout: post
title: "GPU逆向升值 / The Paradox of GPU Appreciation"
date: 2026-03-27
categories: [GPU, AI, Economics]
---

<style>
.lang-toggle { display: flex; gap: 10px; margin-bottom: 20px; }
.lang-toggle button { padding: 8px 16px; border: 1px solid #ccc; background: #f5f5f5; cursor: pointer; border-radius: 4px; }
.lang-toggle button.active { background: #333; color: #fff; border-color: #333; }
.lang-content { display: none; }
.lang-content.active { display: block; }
</style>

<div class="lang-toggle">
  <button onclick="switchLang('zh')" id="btn-zh" class="active">中文</button>
  <button onclick="switchLang('en')" id="btn-en">English</button>
</div>

<div id="content-zh" class="lang-content active" markdown="1">

**先一句话总结：** H100发布三四年了，价格反而更贵了——因为同样的硬件跑出了更聪明的AI，单位GPU产出的智能价值在涨。

## 一个违反直觉的现象

最近看了SemiAnalysis的一份报告，发现了一个非常有意思的现象：NVIDIA H100 GPU发布已经三四年了，它的价格不但没有下降，**反而比以前还要更贵了**。

2025年底到2026年初，H100租赁价格出现了**约10%的跳涨**，购买价格依然稳定在$25,000-$40,000的高位。二手市场上更是供不应求。

这在任何一个传统硬件领域都是不可思议的。我们从小到大接触的规律是：电子产品买来就开始贬值，三年后基本不值钱了。手机如此，电脑如此，服务器也是如此。但AI GPU打破了这个规律。

## 核心原因：同样的硬件，跑出了更聪明的AI

SemiAnalysis给的原因非常有意思：**同一块H100，现在跑的Model比以前更加的聪明了**。因为它更加聪明了，所以它在单位GPU上产生的智能的Token会更好，那它的价格就相应地提升了。

用一个简单的公式来表达：

> **GPU价值 = 产出的智能水平 × 每美元产出的Token量**

当"智能水平"这一侧不断提升——通过更好的模型架构、训练方法、推理优化——每个GPU小时的价值就在上涨。价值上涨，价格自然水涨船高。

## 跟传统软硬件的根本区别

这确实跟我们传统的软件和硬件的开发是不一样的。

**传统逻辑是这样的：** 当你的硬件过时了之后，你不能跑最新的软件，那你的硬件就基本报废了。你的老iPhone跑新iOS会卡顿，你的老电脑玩不了新游戏。硬件的价值取决于它能不能"跟上"软件的步伐。

**但AI GPU完全反过来了：** 新的Model不但能在老硬件上跑，而且跑得更聪明。不是像以前一样，新的软件就没法在老的硬件上跑，而且就算跑也很慢。

为什么会这样？因为以前的软件更多的不是智能，而是说它的**功能的多少**，以及**速度的快慢**、**处理速度的快慢**。一旦硬件的处理速度和功能支持跟不上，旧硬件就被淘汰了。

而AI的核心指标是**智能程度**。同样一块H100，2023年跑GPT-3.5级别的模型，2026年可以跑远超GPT-4级别的模型。硬件没变，但它产出的"智能"大幅提升了。

| | 传统硬件 | AI GPU |
|---|---|---|
| **软件演进** | 新软件需要新硬件 | 新模型在老硬件上跑得更好 |
| **价值走向** | 快速贬值 | 可能升值或保值 |
| **核心指标** | 功能数量、处理速度 | 单位算力的智能水平 |
| **旧硬件命运** | 跑不动新软件→淘汰 | 跑更聪明的模型→仍然有价值 |

## 中国开源模型的关键推动

这个现象背后有一个重要推手：**中国的开源AI社区**。

由于芯片出口管制，DeepSeek、通义千问（Qwen）等团队受限于算力，他们做了很多在已有的硬件、老的硬件上的优化。这种限制反而逼出了大量效率创新：

- **模型架构优化** — MoE、GQA等技术，用更少的计算量达到更高的智能水平
- **训练效率优化** — 更好的学习率调度、数据筛选、训练策略
- **推理优化** — 量化、投机解码等技术让老GPU也能高效运行新模型
- **知识蒸馏** — 小模型也能有大模型的水准

这样让老的硬件可以跑更加聪明的软件。跟传统的"新软件在老硬件上跑不动"的逻辑完全相反。

## 这意味着什么？

- **对投资者：** 传统的3-5年折旧模型可能严重低估了AI GPU的实际价值。亚马逊已经修改了GPU的折旧年限。
- **对AI行业：** 每一次算法进步，不仅让新芯片受益，也让所有已部署的老芯片增值——这是一个正向飞轮。
- **对科技生态：** AI GPU可能正在成为一种新的资产类别，更像是"生产性不动产"——价值不取决于建筑年龄，而取决于租户的生产力。

## 展望

当然，H100不可能永远升值。随着Blackwell、Rubin等新架构的推出，H100终将在性价比上被超越。但这个底层逻辑可能会长期存在：**在AI时代，硬件的价值越来越由软件的智能水平决定，而不仅仅是硬件本身的规格。**

所以我觉得这是个很有趣的现象。GPU看起来确实是不同的打法。

</div>

<div id="content-en" class="lang-content" markdown="1">

**TL;DR:** The H100 is more expensive 3-4 years after launch — because the same hardware now runs much smarter AI, increasing the intelligence value per GPU.

## A Counterintuitive Phenomenon

A recent SemiAnalysis report highlighted a fascinating observation: the NVIDIA H100 GPU, released in 2022, is **more expensive today in 2026 than it was at launch**. H100 rental prices spiked roughly **10% between late 2025 and early 2026**, and purchase prices remain stubbornly high at $25,000–$40,000. Demand in the secondary market continues to outstrip supply.

This runs counter to everything we know about technology hardware. In every previous era, a three-year-old chip is discounted, obsolete, and headed for the recycling bin. But AI GPUs have broken this rule.

## The Core Insight: Same Hardware, Smarter AI

The reason, as SemiAnalysis explains, is deceptively simple: **the same H100 is now running far smarter models than when it was first released**. Because the models are smarter, the quality of intelligent tokens produced per GPU is much better — so the price goes up accordingly.

A simple equation:

> **GPU Value = Intelligence of Output × Tokens Generated Per Dollar**

When the "intelligence" side keeps increasing — through better architectures, training methods, and inference optimizations — the value of each GPU hour goes up. And if value goes up, so does the price the market is willing to pay.

## A Fundamental Break from Traditional Hardware

This is fundamentally different from how traditional software and hardware development works.

**The old logic:** When your hardware becomes outdated and can't run the latest software, it's essentially worthless. Your old iPhone crawls on new iOS. Your aging PC can't handle the latest games. The hardware's value depends entirely on whether it can "keep up."

**AI GPUs flip this entirely:** New models not only run on old hardware — they run *smarter* on it. This is the opposite of traditional software, where new versions are slower or can't run at all on old hardware.

Why? Because traditional software was primarily about **feature count** and **processing speed**. Once the hardware couldn't keep up with speed and feature requirements, it was obsolete.

But the core metric for AI is **intelligence quality**. The same H100 that ran GPT-3.5-class models in 2023 can now run models far exceeding GPT-4 in 2026. The hardware hasn't changed. The intelligence it produces has transformed.

| | Traditional Hardware | AI GPU |
|---|---|---|
| **Software evolution** | New software requires new hardware | New models run better on old hardware |
| **Value over time** | Rapid depreciation | Can appreciate or hold value |
| **Key metric** | Feature count, processing speed | Intelligence per compute unit |
| **Old hardware fate** | Can't run new software → obsolete | Runs smarter models → still valuable |

## China's Open Source Efficiency Revolution

A key driver of this phenomenon is the explosion of efficient open-source models — many from China. Companies like **DeepSeek** and **Alibaba (Qwen)** have been operating under severe compute constraints due to US export controls. This limitation has, paradoxically, become a superpower.

Because these teams can't simply throw more hardware at the problem, they've invested heavily in optimizations that make older hardware run smarter models:

- **Architectural efficiency** — MoE, grouped-query attention, and techniques that extract more intelligence from fewer FLOPs
- **Training optimization** — Better learning rate schedules, data curation, and training recipes
- **Inference optimization** — Quantization, speculative decoding, and KV-cache tricks for older GPUs
- **Knowledge distillation** — Smaller models punching far above their weight class

The result: old hardware isn't obsolete — it runs smarter software. The exact opposite of the traditional paradigm.

## What This Means

- **For investors:** Traditional 3-5 year depreciation models may dramatically understate AI GPU value. Amazon has already revised useful life estimates for AI hardware.
- **For the AI industry:** Every algorithmic improvement retroactively increases the value of *every chip already deployed* — a powerful flywheel.
- **For the tech ecosystem:** AI GPUs may be emerging as a new asset class — more like productive real estate, where value depends not on age but on the productivity of what runs on it.

## Looking Ahead

Of course, the H100 can't appreciate forever. Newer architectures like Blackwell and Rubin will eventually offer dramatically better performance-per-watt. But the underlying principle may endure: **in the AI era, hardware value is increasingly determined by software intelligence, not hardware specs alone.**

This is a genuinely different playbook. And it's a fascinating one to watch unfold.

</div>

<script>
function switchLang(lang) {
  document.querySelectorAll('.lang-content').forEach(el => el.classList.remove('active'));
  document.querySelectorAll('.lang-toggle button').forEach(el => el.classList.remove('active'));
  document.getElementById('content-' + lang).classList.add('active');
  document.getElementById('btn-' + lang).classList.add('active');
}
</script>
