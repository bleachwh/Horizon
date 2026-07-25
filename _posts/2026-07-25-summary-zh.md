---
layout: default
title: "Horizon Summary: 2026-07-25 (ZH)"
date: 2026-07-25
lang: zh
---

> 从 24 条内容中筛选出 8 条重要资讯。

---

1. [vLLM v0.26.0 发布，支持 Inkling 模型并优化 DeepSeek-V4](#item-1) ⭐️ 9.0/10
2. [sglang v0.5.16 发布：DSpark 推测解码与 Inkling 模型支持](#item-2) ⭐️ 8.0/10
3. [开源权重 AI 迎来其 Kubernetes 时刻](#item-3) ⭐️ 8.0/10
4. [Anthropic 发布 Claude Opus 5，性能领先且价格减半](#item-4) ⭐️ 8.0/10
5. [AMD 打破 CUDA 护城河之困：智能核生成与生产困境](#item-5) ⭐️ 8.0/10
6. [中国对携程处以 51.79 亿元反垄断罚款](#item-6) ⭐️ 8.0/10
7. [安卓可能限制设备端 ADB，引发争议](#item-7) ⭐️ 7.0/10
8. [上海携程商务因数据出境违规被罚 1000 万元](#item-8) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 发布，支持 Inkling 模型并优化 DeepSeek-V4](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 9.0/10

vLLM 0.26.0 版本新增了对 Inkling 模型家族的支持，对 DeepSeek-V4 进行了性能优化，增加了 fp32 lm_head 以提升生成精度，并支持按 KV 缓存组选择注意力后端。 该版本显著扩展了 vLLM 的模型兼容性和推理效率，通过为 DeepSeek-V4 和 Inkling 等先进模型提供更快、更准确的生成能力，惠及整个 LLM 生态系统。 v0.26.0 共有来自 212 位贡献者的 411 次提交，包括为 DeepSeek-V4 设计的专用路由内核，端到端 TPOT 提升 2.94%，以及对 Inkling 家族的 piecewise CUDA graph 支持。此外，还完善了 KV 卸载与分层辅助存储功能，并为 Rust 前端提供了多模态支持。

github · khluu · 7月25日 10:38

**背景**: vLLM 是一个开源的高吞吐量 LLM 推理引擎，针对服务大型语言模型优化内存和计算。Inkling 模型由 Thinking Machines Lab 开发，是一个 975B 参数的混合专家（MoE）Transformer，支持高达 100 万令牌的上下文。Piecewise CUDA graph 将模型计算拆分为多个部分，从而实现原本不支持的组件的 CUDA 图捕获。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://docs.sglang.io/docs/advanced_features/piecewise_cuda_graph">Piecewise CUDA Graph - SGLang Documentation</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#GPU optimization`, `#release notes`

---

<a id="item-2"></a>
## [sglang v0.5.16 发布：DSpark 推测解码与 Inkling 模型支持](https://github.com/sgl-project/sglang/releases/tag/v0.5.16) ⭐️ 8.0/10

sglang v0.5.16 引入了 DSpark 置信度驱动的推测解码，在 DeepSeek-V4-Pro 上达到 383.7 tok/s，并新增对 975B 参数 Inkling 多模态 MoE 模型的支持，输入吞吐量高达 71.7k tok/s。 这些创新显著提升了 LLM 推理效率，尤其适用于大型 MoE 模型和长上下文场景，有望降低服务成本并实现更响应的 AI 应用。 DSpark 使用置信头自适应调整验证窗口而非固定长度草稿；Inkling 结合滑动窗口、全注意力和 Mamba2 线性注意力，支持 1M token 上下文和 NVFP4 MoE。该版本还移除了实验性的 QServe 和 FBGEMM FP8 量化路径。

github · Qiaolin-Yu · 7月25日 00:13

**背景**: 推测解码通过使用草稿模型预测 token，再由目标模型并行验证来加速 LLM 推理。传统方法使用固定长度草稿，效率不高。DSpark 根据草稿的置信度动态调整验证窗口。MoE（混合专家）模型每 token 仅激活部分参数，从而支持大规模扩展；Inkling 是 Thinking Machines Lab 开发的 975B 参数多模态 MoE 模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2607.05147">DSpark : Confidence -Scheduled Speculative Decoding with...</a></li>
<li><a href="https://thinkingmachines.ai/model-card/inkling/">Inkling Model Card - Thinking Machines Lab</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#LLM inference`, `#sglang`, `#model serving`, `#open-source`

---

<a id="item-3"></a>
## [开源权重 AI 迎来其 Kubernetes 时刻](https://tobi.knaup.me/2026-07-25-open-weight-ai-is-having-its-kubernetes-moment/) ⭐️ 8.0/10

开源权重 AI 模型正在成为类似 Kubernetes 的基础设施层，推动人工智能的更广泛访问与创新。 这一转变使 AI 民主化，减少了对专有模型的依赖，并可能催生类似 Kubernetes 在云原生计算中的生态增长，影响监管与定价。 讨论包括从技术上看无法按来源封禁模型（权重只是数字），以及开源权重模型为推理成本提供合理基线，从而需要更清晰的代币经济学。

hackernews · tknaup · 7月25日 14:49 · [社区讨论](https://news.ycombinator.com/item?id=49048034)

**背景**: 开源权重 AI 模型公开了其训练参数，任何人都可以下载并运行，这与封闭模型不同。Kubernetes 是一个开源容器编排平台，已成为管理云原生应用的标准。这个类比表明，开源权重模型同样可能成为基础设施标准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://openrouter.ai/blog/insights/the-open-weight-models-that-matter-june-2026/">The Open Weight Models that Matter: June 2026 — OpenRouter Blog</a></li>
<li><a href="https://www.recordinglaw.com/ai-open-source-model-licensing-legal-guide/">AI Model Licensing: Legal Rules for Open-Source Attribution | Recording Law</a></li>

</ul>
</details>

**社区讨论**: 评论者讨论了封禁中国模型的可行性（认为因权重匿名性而不可行），凸显了对代币经济学定价的困惑，并呼吁美国实验室以宽松许可证发布更多前沿开源权重模型。

**标签**: `#open-weight AI`, `#AI infrastructure`, `#Kubernetes`, `#AI regulation`, `#model licensing`

---

<a id="item-4"></a>
## [Anthropic 发布 Claude Opus 5，性能领先且价格减半](https://simonwillison.net/2026/Jul/24/introducing-claude-opus-5/#atom-everything) ⭐️ 8.0/10

Anthropic 发布了 Claude Opus 5，这是一款新的人工智能模型，以更先进的 Claude Fable 5 一半的价格在 Artificial Analysis 排行榜上位居首位，并且具备主动能力，例如自行编写计算机视觉管道来解决问题。 Claude Opus 5 以显著更低的成本提供了前沿水平的智能，使高级 AI 更易获取且更具竞争力，特别是对于长期运行的智能体和编码任务，可能重塑大语言模型市场。 Claude Opus 5 的定价与其前代 Opus 4.8 相同，并提供“快速模式”，费用为基础模型的两倍；它在未经过利用训练的情况下显示了改进的漏洞检测能力，并且据报道是 Anthropic 迄今为止最不易被提示注入的模型。

rss · Simon Willison · 7月24日 23:48

**背景**: Claude 是 Anthropic 开发的一系列大语言模型，通常按层级发布：Haiku、Sonnet 和 Opus（能力最强）。2026 年，Anthropic 推出了更强大的 Mythos 和 Fable 层级。主动模型能够独立解决问题，例如在未明确指令的情况下自行生成视觉处理管道等子工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-opus-5">Introducing Claude Opus 5 \ Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Opus">Claude Opus</a></li>
<li><a href="https://artificialanalysis.ai/">AI Model & API Providers Analysis | Artificial Analysis</a></li>

</ul>
</details>

**社区讨论**: Boris Cherny 称赞 Opus 5 是迄今为止最不易被提示注入的模型，强调其在评估和红队测试中均表现出鲁棒性，这解决了一个关键的安全问题。

**标签**: `#AI`, `#Anthropic`, `#Claude`, `#Large Language Models`, `#Machine Learning`

---

<a id="item-5"></a>
## [AMD 打破 CUDA 护城河之困：智能核生成与生产困境](https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing) ⭐️ 8.0/10

Semianalysis 的分析揭示了 AMD 在挑战 NVIDIA CUDA 主导地位时面临的技术和运营障碍，重点指出了智能核生成、软件质量以及 MI455X 'Helios'系统的生产爬坡问题。 这很重要，因为 AMD 能否提供有竞争力的 GPU 软件生态系统对于 AI 硬件市场的多样性和定价至关重要。打破 CUDA 护城河的成功或失败将影响整个 AI 硬件供应链和企业采用。 分析特别提到'智能核生成'作为一条潜在路径，即利用 LLM 驱动的代理自动生成优化的 GPU 内核，但指出 AMD 的内部开发集群不稳定，MI455X 的生产爬坡被描述为'地狱'，并出现了高达 105%的财务工程折扣。

rss · Semianalysis · 7月25日 00:33

**背景**: CUDA 是 NVIDIA 专有的并行计算平台和 API，可实现高性能 GPU 计算，形成了锁定用户的软件护城河。AMD 一直试图用其 ROCm 软件栈与之竞争，但在易用性、内核优化和生产可扩展性方面面临挑战。智能核生成指利用自主 LLM 代理迭代生成并优化特定硬件的计算内核，可能减少手动调优的需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/agentic-kernel-generation">Agentic Kernel Generation</a></li>
<li><a href="https://www.storagereview.com/news/amd-mi455x-and-helios-432gb-hbm4-72-gpu-racks-and-a-real-answer-to-vera-rubin">AMD MI455X and Helios: 432GB HBM4, 72-GPU Racks, and a Real Answer to ...</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/amd-touts-instinct-mi430x-mi440x-and-mi455x-ai-accelerators-and-helios-rack-scale-ai-architecture-at-ces-full-mi400-series-family-fulfills-a-broad-range-of-infrastructure-and-customer-requirements">AMD touts Instinct MI430X, MI440X, and MI455X AI accelerators and ...</a></li>

</ul>
</details>

**标签**: `#AMD`, `#CUDA`, `#AI Hardware`, `#GPU Computing`, `#Software Ecosystem`

---

<a id="item-6"></a>
## [中国对携程处以 51.79 亿元反垄断罚款](https://t.me/zaihuapd/42767) ⭐️ 8.0/10

7 月 25 日，国家市场监督管理总局对携程集团有限公司滥用市场支配地位实施垄断行为作出行政处罚，没收违法所得并处以罚款，合计 51.79 亿元。 这是中国科技领域最大的反垄断罚款之一，标志着监管力度加强，并将影响在线旅游市场的未来竞争格局。 处罚包括没收违法所得 16.58 亿元和罚款 35.21 亿元，合计 51.79 亿元。同时责令携程退还强制扣除酒店经营者的订单储备金 1.22 亿元，并全面整改。

telegram · zaihuapd · 7月25日 11:56

**背景**: 中国的《反垄断法》禁止具有市场支配地位的公司进行不公平定价或独家交易等滥用行为。携程是中国在线旅游平台的主导者，此案反映了政府加强监管大型科技公司、促进公平竞争的广泛努力。

**标签**: `#antitrust`, `#regulation`, `#Ctrip`, `#China`, `#monopoly`

---

<a id="item-7"></a>
## [安卓可能限制设备端 ADB，引发争议](https://kitsumed.github.io/blog/posts/android-may-soon-restrict-on-device-adb/) ⭐️ 7.0/10

谷歌正在考虑对安卓进行一项更改，限制在设备端使用 Android Debug Bridge (ADB)，这意味着用户将无法在没有连接主机电脑的情况下直接在设备上运行 ADB 命令。此潜在限制旨在防止恶意应用滥用 ADB 进行未经授权的访问，但引发了依赖 ADB 进行合法调试和自定义的开发者的批评。 这一变化可能显著影响安卓的开放性，因为 ADB 是开发者和高级用户进行调试、侧载应用和访问高级功能的关键工具。如果实施，将使安卓在限制用户控制方面更接近 iOS，可能削弱该平台对开发者和爱好者的吸引力。 该限制特别针对设备端 ADB 访问，即允许在设备自身的终端上直接运行 ADB 命令。这与通过 USB 或无线从电脑连接的 ADB 不同。提案包括允许用户将特定 IP 地址或接口列入白名单以保留一定灵活性。

hackernews · shscs911 · 7月25日 06:57 · [社区讨论](https://news.ycombinator.com/item?id=49045159)

**背景**: Android Debug Bridge (ADB) 是一个多功能命令行工具，允许开发者与安卓设备进行通信，用于调试、安装应用和运行 shell 命令。它采用客户端-服务器架构：设备上的守护进程通过 USB 或 TCP 连接到主机 PC 上的服务器。设备端 ADB（设备自身作为主机）不太常见，但用于自动化和本地调试。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Android_Debug_Bridge">Android Debug Bridge - Wikipedia</a></li>
<li><a href="https://developer.android.com/tools/adb">Android Debug Bridge ( adb ) | Android Studio | Android Developers</a></li>

</ul>
</details>

**社区讨论**: 社区评论显示出分歧：一些人认为这一变化没有必要，因为攻击向量需要启用开发者选项和远程 ADB，只影响一小部分用户。另一些人则将其视为谷歌锁定安卓趋势的一部分，有评论者预测未来限制可能要求放弃身份并每年付费。也有挫败感，认为谷歌可能忽略有价值的反馈并锁定问题。

**标签**: `#Android`, `#ADB`, `#security`, `#developer tools`, `#Google`

---

<a id="item-8"></a>
## [上海携程商务因数据出境违规被罚 1000 万元](https://t.me/zaihuapd/42758) ⭐️ 7.0/10

2024 年 6 月 13 日，上海网信办公示，上海携程商务有限公司因未落实数据出境安全评估要求、违法出境个人信息，被罚款 1000 万元，并责令限期改正。 这是中国数据合规执法的重要案例，表明监管机构对跨境数据流动的严格态度，对在华运营的互联网企业有警示作用。 罚款金额为 1000 万元人民币，企业已配合整改。今年以来网信部门已发现部分民生领域互联网企业仍存在类似违规行为，将持续加大执法力度。

telegram · zaihuapd · 7月25日 02:24

**背景**: 根据《数据出境安全评估办法》，数据处理者向境外提供重要数据或达到一定规模的个人信息时，应当申报数据出境安全评估。该办法旨在防范数据出境安全风险，保障数据依法有序自由流动。上海携程商务作为个人信息处理者，未履行评估义务即向境外传输数据，因而受罚。

<details><summary>参考链接</summary>
<ul>
<li><a href="http://aq.juming.cn/show/403.html">aq.juming.cn/show/403.html</a></li>
<li><a href="https://www.400hl.com/help/419.htm">400hl.com/help/419.htm</a></li>

</ul>
</details>

**标签**: `#data privacy`, `#regulation`, `#China`, `#data export`, `#fine`

---