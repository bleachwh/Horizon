---
layout: default
title: "Horizon Summary: 2026-07-09 (ZH)"
date: 2026-07-09
lang: zh
---

> 从 33 条内容中筛选出 8 条重要资讯。

---

1. [TypeScript 7.0 发布：Go 重写带来最高 12 倍速度提升](#item-1) ⭐️ 10.0/10
2. [Bun 运行时从 Zig 重写为 Rust](#item-2) ⭐️ 9.0/10
3. [蚂蚁灵波开源 LingBot-Video，全球首个 MoE 具身视频基模](#item-3) ⭐️ 9.0/10
4. [欧盟议会批准聊天控制 1.0，允许大规模扫描](#item-4) ⭐️ 8.0/10
5. [Meta 发布开源权重 AI 模型 Muse Spark 1.1](#item-5) ⭐️ 8.0/10
6. [OpenAI 为 ChatGPT 语音模式推出 GPT-Live](#item-6) ⭐️ 8.0/10
7. [Talos-XII：用 Rust 手写自动求导和强化学习栈应用于抽卡建模](#item-7) ⭐️ 8.0/10
8. [LineageOS 推出网页刷机工具](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [TypeScript 7.0 发布：Go 重写带来最高 12 倍速度提升](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 10.0/10

微软正式发布 TypeScript 7.0，该版本用 Go 语言完整重写了编译器，实现了 8 到 12 倍的构建速度提升，并支持共享内存多线程。 这一重大发布通过大幅缩短构建时间显著提升了开发者效率，并展示了大规模 JavaScript/TypeScript 代码库编译器设计的重大转变。 新引入了 --checkers 和 --builders 参数以自定义并行度，并提供兼容包实现与 TypeScript 6 并存；但 Vue、Svelte 等嵌入式语言工具链因 API 尚未就绪，目前仍需使用旧版本。

telegram · zaihuapd · 7月9日 04:01

**背景**: TypeScript 是 JavaScript 的超集，提供静态类型检查，并编译为普通 JavaScript。原有的 TypeScript 编译器由 TypeScript 自身编写，运行在 Node.js 上。将其重写为 Go 语言（一种以高性能和并发支持著称的系统编程语言）可实现原生代码执行、更好的内存管理和高效的多线程，从而带来显著的速度提升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/">Announcing TypeScript 7.0 - TypeScript</a></li>
<li><a href="https://en.wikipedia.org/wiki/Language_Server_Protocol">Language Server Protocol - Wikipedia</a></li>
<li><a href="https://microsoft.github.io/language-server-protocol/">Official page for Language Server Protocol</a></li>

</ul>
</details>

**标签**: `#TypeScript`, `#Go`, `#Performance`, `#Microsoft`, `#Programming Language`

---

<a id="item-2"></a>
## [Bun 运行时从 Zig 重写为 Rust](https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/#atom-everything) ⭐️ 9.0/10

Jarred Sumner 宣布，原用 Zig 编写的流行 JavaScript 运行时 Bun 已完全用 Rust 重写，重写过程借助了 AI 编程代理，花费约 16.5 万美元的 token。新的基于 Rust 的 Bun 自 2026 年 6 月 17 日起已部署在 Claude Code 中，Linux 启动速度提升了 10%。 这表明借助 AI，对关键基础设施进行大规模重写现在变得可行，挑战了长期以来反对从头重写的原则。从 Zig 迁移到 Rust 解决了内存安全问题（如释放后使用、双重释放），可能使 Bun 对数百万用户更加稳定可靠。 重写消耗了 59 亿未缓存输入 token、6.9 亿输出 token 和 720 亿缓存输入 token 读取。Bun 的 TypeScript 测试套件包含一百万条断言，作为合规套件，通过代理工作流和对抗性代码审查实现了自动化移植。

rss · Simon Willison · 7月8日 23:57

**背景**: Bun 是一个快速的全能 JavaScript 运行时，集成了打包器、测试运行器和包管理器，旨在成为 Node.js 的直接替代品。它最初用 Zig 编写，Zig 是一种注重简洁和手动内存管理的系统编程语言。Rust 是另一种系统语言，通过其所有权模型和严格的编译器检查保证内存安全，防止释放后使用等常见错误。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bun_(software)">Bun (software) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>
<li><a href="https://bun.com/">Bun — A fast all-in-one JavaScript runtime</a></li>

</ul>
</details>

**标签**: `#Bun`, `#Rust`, `#Zig`, `#JavaScript runtime`, `#software engineering`

---

<a id="item-3"></a>
## [蚂蚁灵波开源 LingBot-Video，全球首个 MoE 具身视频基模](https://www.qbitai.com/2026/07/446458.html) ⭐️ 9.0/10

蚂蚁灵波开源了 LingBot-Video，这是全球首个基于混合专家（MoE）架构的具身智能视频生成基础模型。该模型总参数量为 30B，生成时仅激活约 3B，推理效率约为同等规模稠密模型的 3 倍。 这代表了具身 AI 和机器人视频生成领域的重大突破，证明了 MoE 可以在保持高质量的同时大幅降低计算成本。以 Apache 2.0 协议开源，将加速机器人动作预测、仿真数据生成和世界模型研究等方向的研究。 LingBot-Video 采用 DiT+MoE 架构，包含 128 个专家，top-8 路由（每层 13B 参数量中激活 1.4B），受 DeepSeek-V3 启发。它包含一个六奖励强化学习后训练系统，其中物理合理性奖励由 VLM 判断，并支持动作到视频模式，根据动作和手部姿态条件预测机器人执行轨迹。

telegram · zaihuapd · 7月9日 04:30

**背景**: 混合专家（MoE）是一种神经网络架构，将网络划分为多个专门的“专家”子网络，并通过门控机制为每个输入仅激活部分专家，从而平衡容量和成本。扩散变换器（DiT）用 Transformer 取代传统的 U-Net 骨干网络，在潜在空间中处理图像块，具有更好的可扩展性。具身智能是指通过传感器和致动器与物理世界交互的 AI 系统，常见于机器人领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://github.com/facebookresearch/dit">GitHub - facebookresearch/DiT: Official PyTorch Implementation of "Scalable Diffusion Models with Transformers" · GitHub</a></li>

</ul>
</details>

**社区讨论**: 社区讨论（来自 Reddit 评论）指出，尽管该模型在技术上令人印象深刻，但存在一些担忧：使用 VLM 判断物理合理性可能引发奖励破解问题；缺乏闭环机器人评估结果，引发了视频生成器与世界模型之间界限的讨论。该模型在 RBench 上获得平均最高分，但在依赖推理的维度上仍落后于闭源模型，且在其自己的评估中通用文本到视频任务仅排第二。

**标签**: `#具身智能`, `#MoE`, `#视频生成`, `#机器人`, `#开源`

---

<a id="item-4"></a>
## [欧盟议会批准聊天控制 1.0，允许大规模扫描](https://www.patrick-breyer.de/en/eu-parliament-greenlights-chat-control-1-0-breyer-our-children-lose-out/) ⭐️ 8.0/10

欧盟议会于 2025 年 7 月 5 日批准了聊天控制 1.0，允许美国科技公司在无需搜查令的情况下扫描私人消息，有效期至 2028 年，推翻了此前 3 月份的两次否决。 这一政策转变削弱了数字隐私，并为欧盟的大规模监控开创了先例，影响了 Instagram、Discord 和 Gmail 等平台上的数百万用户。 投票需要 361 票的绝对多数才能否决，但只有 314 名欧洲议会议员投反对票，276 票赞成，17 票弃权，因此否决动议失败。该措施采用客户端扫描技术，误报率很高。

hackernews · rapnie · 7月9日 11:03 · [社区讨论](https://news.ycombinator.com/item?id=48843923)

**背景**: 聊天控制是欧盟为打击儿童性虐待材料（CSAM）而提出的提案，要求科技公司扫描私人通信。客户端扫描（CSS）在用户设备上对消息加密前进行检查，引发隐私担忧。第一版聊天控制 1.0 最初是自愿的，但现在成为强制性措施，有效期至 2028 年。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.patrick-breyer.de/en/posts/chat-control/">Chat Control: The EU's CSAM scanner proposal</a></li>
<li><a href="https://fightchatcontrol.eu/chat-control-overview">Chat Control 1.0 vs 2.0 - Fight Chat Control</a></li>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control">Chat Control - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者对议会程序表示愤怒，指出多数投票的欧洲议会议员实际上反对该措施，但由于绝对多数要求而通过。一位评论者称其为“愚蠢的议会伎俩”，并警告这可能会使欧盟失去合法性。

**标签**: `#privacy`, `#surveillance`, `#EU regulation`, `#technology law`, `#mass scanning`

---

<a id="item-5"></a>
## [Meta 发布开源权重 AI 模型 Muse Spark 1.1](https://ai.meta.com/blog/introducing-muse-spark-meta-model-api/) ⭐️ 8.0/10

Meta 发布了新开源权重 AI 模型 Muse Spark 1.1，并提供 API 访问。该模型在 Terminal-Bench 2.1 等基准上进行了评估。 此次发布通过将开源权重模型商品化，挑战了专有编码模型的主导地位，可能降低开发者的成本。同时引发了关于评估标准和开源模型行业战略角色的讨论。 Muse Spark 1.1 是 1.0 的增量更新，拥有开源权重，可在自有硬件上运行。定价为输入/输出每百万 tokens $1.25/$4.5，缓存输入 $0.15。但社区成员指出报告中的评估方法可能存在缺陷，因其在 Terminal-Bench 2.1 任务中覆盖了资源上限（6 核 CPU、8GB 内存）。

hackernews · ot · 7月9日 14:10 · [社区讨论](https://news.ycombinator.com/item?id=48846184)

**背景**: 开源权重模型意味着核心组件（权重）公开发布，允许任何人下载、研究和修改（根据斯坦福 HAI 定义）。这类模型与 OpenAI 或 Anthropic 的封闭 API 形成对比。Meta 一直发布 Llama 等开源权重模型，以促进 AI 发展和竞争。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了对评估方法的担忧（GodelNumbering）、通过插件实现的实用集成（simonw）、战略商品化议论（jacobgold）、激进的定价（Tiberium）以及竞争格局的变化——xAI 和 Meta 如今具有竞争力（Sol-）。

**标签**: `#AI`, `#Meta`, `#large language models`, `#open source`, `#coding assistant`

---

<a id="item-6"></a>
## [OpenAI 为 ChatGPT 语音模式推出 GPT-Live](https://simonwillison.net/2026/Jul/8/introducing-gptlive/#atom-everything) ⭐️ 8.0/10

OpenAI 推出了 GPT-Live，这是 ChatGPT 语音模式的新模型，能够将复杂任务委托给后台的 GPT-5.5，同时保持对话流畅。 此次升级显著提升了 ChatGPT 语音模式的实用性，此前的旧模型基于 GPT-4o 时代，能力有限，新模型使其成为更强大的头脑风暴伙伴。 GPT-Live 可将需要网络搜索、深度推理或复杂工作的任务悄悄委托给 GPT-5.5，并将结果带回对话。预览版存在一个 bug，导致模型在非笑话时发笑，但 OpenAI 据称已进行调整。

rss · Simon Willison · 7月8日 23:20

**背景**: ChatGPT 语音模式允许用户与 AI 进行语音对话。此前它使用的是一个知识截止于 2024 年的旧模型，限制了其效果。GPT-Live 是一次重大升级，能够在不断用户体验的情况下实时将任务委托给更强大的模型。

**标签**: `#OpenAI`, `#GPT‑Live`, `#ChatGPT`, `#voice mode`, `#AI models`

---

<a id="item-7"></a>
## [Talos-XII：用 Rust 手写自动求导和强化学习栈应用于抽卡建模](https://www.reddit.com/r/MachineLearning/comments/1urvxgb/talosxii_handwritten_autograd_small_rlmlp_stack/) ⭐️ 8.0/10

一个名为 Talos-XII 的 Rust 项目实现了一个手写的自动求导引擎和强化学习栈（包括 Dueling DQN 和 PPO），用于建模《明日方舟：终末地》的抽卡概率，且未使用 PyTorch 或 ndarray 等外部 ML 框架。 该项目展示了紧凑型强化学习解决方案可以完全用 Rust 构建，为抽卡概率等特定领域模拟提供高性能和可移植性，并凸显了在受限环境下基于 CPU 的 ML 的潜力。 该栈包括一个自定义自动求导引擎（支持 SIMD 分发：AVX2、AVX-512、NEON）、Rayon 并行化模拟、BF16 推理缓存，以及一个名为 ACHF 的组件，自适应地混合密集和稀疏执行路径；作者寻求在 ARM、AVX-512 和 GPU 硬件上的基准数据。

reddit · r/MachineLearning · /u/zay0kami · 7月9日 16:52

**背景**: 自动求导（Autograd）是一种自动计算梯度的技术，对训练神经网络至关重要。强化学习通过最大化累积奖励来训练智能体做出决策。游戏中的抽卡系统基于概率抽取；神经网络可以建模隐藏偏差和超越静态表格的最优抽取策略。

**标签**: `#Rust`, `#autograd`, `#reinforcement learning`, `#gacha`, `#MLP`

---

<a id="item-8"></a>
## [LineageOS 推出网页刷机工具](https://www.androidauthority.com/lineageos-summertime-update-2026-3685112/) ⭐️ 8.0/10

LineageOS 在 2026 年夏季更新中推出了 Lineage Flash Tools，用户无需在本地安装 adb 和 fastboot，即可直接从浏览器中进行刷机。 这款基于网页的工具降低了用户安装自定义 ROM 的门槛，有望扩大 LineageOS 的覆盖面，让更多用户能够轻松完成刷机过程。 该工具支持 Fastboot、ADB 和三星 Odin 协议，需要使用支持 WebUSB 的 Chromium 内核浏览器（如 Chrome 或 Edge），并且仍需配合设备专属的 Wiki 安装指南使用。

telegram · zaihuapd · 7月9日 01:46

**背景**: 像 LineageOS 这样的自定义 ROM 可以替换 Android 设备的原生操作系统，通常提供更新的 Android 版本或额外功能。传统上，刷机需要安装 adb 和 fastboot 等命令行工具，这可能让新手望而却步。WebUSB 是一种 JavaScript API，允许网页通过支持的浏览器安全地与 USB 设备通信，从而实现了基于浏览器的设备管理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebUSB">WebUSB</a></li>
<li><a href="https://grokipedia.com/page/WebUSB">WebUSB</a></li>

</ul>
</details>

**标签**: `#LineageOS`, `#web flashing`, `#Android`, `#custom ROM`, `#open source`

---