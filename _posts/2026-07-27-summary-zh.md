---
layout: default
title: "Horizon Summary: 2026-07-27 (ZH)"
date: 2026-07-27
lang: zh
---

> 从 29 条内容中筛选出 8 条重要资讯。

---

1. [Moonshot AI 在 HuggingFace 上发布 3T 参数模型 Kimi-K3](#item-1) ⭐️ 9.0/10
2. [Fastjson 1.x 曝无 gadget 高危 RCE 漏洞](#item-2) ⭐️ 9.0/10
3. [vLLM v0.26.0 发布，支持 Inkling 并优化 DeepSeek-V4](#item-3) ⭐️ 8.0/10
4. [长鑫存储涨价加剧华为关系紧张](#item-4) ⭐️ 8.0/10
5. [谷歌宣布 Gemini 4 预训练，称最具雄心](#item-5) ⭐️ 8.0/10
6. [中芯国际测试中国首台国产 DUV 光刻机](#item-6) ⭐️ 8.0/10
7. [论坛项目用 HTMX 替换 React，获社区好评](#item-7) ⭐️ 7.0/10
8. [端到端边缘 ML 平台 SensorForge 发布，自带自动标注功能](#item-8) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Moonshot AI 在 HuggingFace 上发布 3T 参数模型 Kimi-K3](https://huggingface.co/moonshotai/Kimi-K3) ⭐️ 9.0/10

Moonshot AI 在 HuggingFace 上发布了 Kimi-K3，一个拥有约 2.8 万亿参数的多模态大模型，采用开放权重并支持原生 mxfp4 量化。 作为目前最大的开放权重模型，Kimi-K3 在 AI 规模和可访问性方面树立了新标杆，使初创企业能够定制和微调模型，同时保留知识产权主权，并推动定价和托管服务的竞争。 Kimi-K3 在 mxfp4 下托管需要约 1.5TB 显存（生产环境可能需要 16 块 B200 GPU），其商业许可规定当累计年收入超过 2000 万美元时需与 Moonshot AI 另行签署协议。

hackernews · nateb2022 · 7月27日 06:18 · [社区讨论](https://news.ycombinator.com/item?id=49065752)

**背景**: 大语言模型以参数量衡量，参数越多通常性能越强。Kimi-K3 拥有 2.8 万亿参数，属于最大的开放权重模型之一。开放权重允许开发者下载并修改模型权重，从而实现基于专有数据的定制和微调，这对寻求差异化和数据主权的初创企业至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cy9w4q8pgp0o">China's Moonshot AI claims Kimi K3 can rival OpenAI and Anthropic</a></li>
<li><a href="https://openrouter.ai/moonshotai/kimi-k3">Kimi K3 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://fortune.com/2026/07/16/moonshots-kimi-k3-pushes-chinese-ai-into-fable-level-territory/">Moonshot’s Kimi K3 pushes Chinese AI into Fable-level territory | Fortune</a></li>

</ul>
</details>

**社区讨论**: 社区评论集中讨论了托管 3T 模型的高成本（估计输入每百万 token 3 美元，输出每百万 token 15 美元）和显存需求（mxfp4 下 1.5TB）。许多人强调定制潜力和 IP 主权是真正的价值所在，而其他人则质疑许可条款将免费商业使用限制在年收入 2000 万美元以内。

**标签**: `#AI`, `#LLM`, `#open-source`, `#huggingface`, `#multimodal`

---

<a id="item-2"></a>
## [Fastjson 1.x 曝无 gadget 高危 RCE 漏洞](https://t.me/zaihuapd/42797) ⭐️ 9.0/10

安全研究人员 Kirill Firsov 披露，Fastjson 1.x 版本 1.2.68 至 1.2.83 存在远程代码执行漏洞，该漏洞无需开启 autoType 也无需依赖 classpath gadget，可在 JDK 8、17 和 21 上利用。 该漏洞影响广泛使用的 Java JSON 库 Fastjson，且由于 Fastjson 1.x 已停止维护，官方不会发布补丁，用户必须升级到 Fastjson2 才能确保安全，影响极为严重。 该漏洞无需开启 autoType 或依赖任何特定的 gadget 链，利用难度较低。研究人员确认 1.2.68 至 1.2.83 版本受影响，且可在 JDK 8、17、21 等多个版本上利用。

telegram · zaihuapd · 7月27日 10:31

**背景**: Fastjson 是阿里巴巴开发的 Java 常用 JSON 库。反序列化漏洞通常依赖“gadget 链”实现代码执行。AutoType 是 Fastjson 支持多态反序列化的特性，常被作为攻击入口。Fastjson 1.x 已于 2024 年 10 月停止维护，不再发布安全补丁，用户必须迁移到 Fastjson2。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/07/fastjson-1x-rce-vulnerability-targeted.html">Fastjson 1.x RCE Vulnerability Targeted in Attacks With No Patched Available</a></li>
<li><a href="https://jfrog.com/blog/cve-2022-25845-analyzing-the-fastjson-auto-type-bypass-rce-vulnerability/">CVE-2022-25845 - Fastjson RCE vulnerability analysis</a></li>
<li><a href="https://protodoc.io/alibaba/fastjson2/readme">Readme - alibaba/ fastjson 2 - protodoc.io</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#RCE`, `#Java`, `#Fastjson`

---

<a id="item-3"></a>
## [vLLM v0.26.0 发布，支持 Inkling 并优化 DeepSeek-V4](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 引入对 Inkling 模型家族的全面支持，对 DeepSeek-V4 的重大性能提升，为生成模型添加 fp32 lm_head 支持，以及支持按 KV 缓存组选择灵活的注意力后端。 此次发布显著扩展了 vLLM 对前沿架构（如 Inkling）的支持，同时提升了 DeepSeek-V4 等大型模型的推理性能，惠及更广泛的 AI 部署生态。 该版本包含来自 212 位贡献者的 411 次提交，包括分段 CUDA 图支持、Hopper FA4 相对注意力、Inkling 的 MTP=1 推测解码，以及针对 DeepSeek-V4 的专用路由内核，可将端到端 TPOT 提升最多 2.94%。

github · khluu · 7月27日 01:06

**背景**: vLLM 是一个开源、高吞吐量的 LLM 服务系统，专注于优化推理内存和速度。Inkling 是一个 9750 亿参数的混合专家模型，拥有 410 亿活跃参数，支持 100 万 token 的上下文窗口。Flash Attention 4 引入了算法与内核流水线协同设计，以适应 Hopper GPU 上的非对称硬件缩放，从而实现更高效的注意力计算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://modal.com/blog/reverse-engineer-flash-attention-4">We reverse-engineered Flash Attention 4</a></li>
<li><a href="https://medium.com/practical-llm-systems/i-tested-mtp-speculative-decoding-on-two-qwen-models-one-was-a-trap-46c2dfe584c7">I Tested MTP Speculative Decoding on Two Qwen Models... | Medium</a></li>

</ul>
</details>

**标签**: `#LLM`, `#vLLM`, `#inference`, `#performance`, `#open-source`

---

<a id="item-4"></a>
## [长鑫存储涨价加剧华为关系紧张](https://t.me/zaihuapd/42788) ⭐️ 8.0/10

存储芯片厂商长鑫存储因 AI 数据中心需求激增而对华为涨价，双方矛盾在 6 月进一步升级：与华为关系密切的设备商新凯来的工程师被要求离开长鑫位于合肥的核心研发区域。 该事件表明，随着 AI 需求赋予长鑫存储等存储供应商更强的议价能力，中国半导体供应链内部摩擦加剧，可能影响华为为其 AI 基础设施获取关键 DRAM 芯片。 长鑫存储现已成为全球第四大 DRAM 制造商，其市场地位使其能够涨价。华为曾要求缓解成本上升但遭拒绝，工程师被驱逐事件进一步表明关系恶化。

telegram · zaihuapd · 7月27日 03:17

**背景**: DRAM 芯片是用于服务器、个人电脑和 AI 数据中心的关键内存组件。长鑫存储是成立于 2016 年的中国领先 DRAM 制造商，华为是其重要客户。近期 AI 基础设施部署激增带动内存需求，使供应商获得了更强定价能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cxmt.com/en/">About cxmt - cxmt</a></li>
<li><a href="https://invest-nav.com/tools/investment-handbook/memory-storage-chain/cxmt-and-china-dram/">长 鑫 存 储 与中国 DRAM ... | 投资导航</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#AI`, `#Huawei`, `#storage chips`, `#supply chain`

---

<a id="item-5"></a>
## [谷歌宣布 Gemini 4 预训练，称最具雄心](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

谷歌 CEO Sundar Pichai 在 Alphabet 2026 年第二季度财报电话会议上透露，Gemini 4 已开始预训练，称其为公司迄今为止最具雄心的预训练项目，计划于 2026 年底发布。 这标志着谷歌持续大力投资前沿 AI，旨在与 GPT-5 或 Claude 4 等领先模型竞争。成功的 Gemini 4 可能巩固谷歌在 AI 竞赛中的地位，并推动大型语言模型的边界。 Pichai 强调，计算资源将优先用于前沿 AGI 研发，以确保 Gemini 4 发布时仍处于行业前沿。此外，Gemini 3.x Flash 系列将保持几乎每月一次的迭代频率，重点提升智能编码能力。

telegram · zaihuapd · 7月27日 04:06

**背景**: Gemini 是 Google DeepMind 开发的多模态大型语言模型系列，是 LaMDA 和 PaLM 2 的继任者。预训练是模型从海量数据中学习模式的资源密集型初始阶段；Gemini 4 的预训练被描述为谷歌迄今为止最具雄心的项目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gemini_2.5_Flash_Image">Gemini 2.5 Flash Image</a></li>
<li><a href="https://aiweekly.co/alerts/google-launches-gemini-36-flash-teases-gemini-4-pre-training">Google launches Gemini 3.6 Flash, teases Gemini 4 pre-training | AI Weekly</a></li>

</ul>
</details>

**标签**: `#Google`, `#AI`, `#Gemini 4`, `#large language model`, `#pre-training`

---

<a id="item-6"></a>
## [中芯国际测试中国首台国产 DUV 光刻机](https://t.me/zaihuapd/42800) ⭐️ 8.0/10

中芯国际已开始试运行中国首台国产深紫外（DUV）光刻机，该设备由上海初创公司宇量昇研发。该机器正在用于生产 28 纳米芯片，并试图通过多重图形化工艺实现 7 纳米甚至 5 纳米。 这标志着中国在半导体自给自足进程中迈出重要一步，有可能在西方出口管制下减少对荷兰 ASML 设备的依赖。如果成功，可能重塑全球芯片供应链，加速中国的先进制造能力。 该 DUV 光刻机的大部分零部件已实现国产化，但部分关键部件仍依赖进口。初期良率预计较低，实现稳定良率的量产可能需要一到两年，商业化量产可能要到 2027 年左右。

telegram · zaihuapd · 7月27日 14:10

**背景**: DUV（深紫外）光刻是半导体制造中的关键步骤，用于在硅晶圆上刻画电路。中国目前最先进的芯片仍依赖荷兰 ASML 的 DUV 设备，而用于 7 纳米以下节点的 EUV 光刻机则被禁止对华销售。多重图形化光刻通过使用多个掩模和刻蚀步骤，实现比单次曝光更精细的特征，但增加了成本和复杂度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cloudadvent.com/get_news/info/3574.html">China's DUV Lithography Machine Breakthrough: Breaking Western...</a></li>
<li><a href="https://min.news/en/digital/0f6b59b4f9f4346928c71bc30fa0125e.html">DUV lithography machine has changed! What are the roads for China...</a></li>
<li><a href="https://lifeboat.com/blog/2025/10/netherlands-tightens-export-restrictions-on-microchip-machines-mainly-targeting-asml">Netherlands tightens export restrictions on microchip machines , mainly...</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#lithography`, `#SMIC`, `#DUV`, `#China tech`

---

<a id="item-7"></a>
## [论坛项目用 HTMX 替换 React，获社区好评](https://misago-project.org/t/removing-reactjs-from-the-codebase-and-adapting-htmx-for-ui-interactivity/1267/) ⭐️ 7.0/10

一位开发者分享了从 Misago 论坛项目中移除 React.js 并采用 HTMX 进行 UI 交互的经验，认为 HTMX 架构更简单，更符合服务器端渲染。 此次迁移反映了向以服务器为中心的前端解决方案发展的趋势，尤其适用于论坛等以内容为主的应用，可降低 JavaScript 复杂性。 论坛软件用 HTMX 替换了 React，利用 HTML 属性实现服务器端局部更新，避免了完整的客户端 JavaScript 框架。

hackernews · Ralfp · 7月27日 09:58 · [社区讨论](https://news.ycombinator.com/item?id=49067301)

**背景**: HTMX 是一个轻量级 JavaScript 库，允许开发者直接从 HTML 访问现代浏览器功能，如 AJAX、CSS 过渡、WebSocket 和服务器发送事件。它强调服务器端渲染和渐进增强，与 React 等管理虚拟 DOM 的重型前端框架形成对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://htmx.org/">htmx - high power tools for html</a></li>
<li><a href="https://en.wikipedia.org/wiki/Htmx">htmx - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区评论普遍支持，用户认为 HTMX 非常适合论坛等服务器端渲染应用。一些人指出在丰富交互方面的局限性，如滚动位置重置，而另一些人建议将 HTMX 与小型 Vue/React 组件结合以处理复杂交互。

**标签**: `#htmx`, `#react`, `#web development`, `#frontend architecture`, `#server-side rendering`

---

<a id="item-8"></a>
## [端到端边缘 ML 平台 SensorForge 发布，自带自动标注功能](https://www.reddit.com/r/MachineLearning/comments/1v7nudc/recent_project_i_worked_on_end_to_end_edge_ml/) ⭐️ 7.0/10

一位 Reddit 用户发布了开源端到端边缘机器学习平台 SensorForge，该平台可从原始传感器数据直接部署模型到微控制器，并包含时间序列数据自动标注工具和信号分析聊天机器人。 该平台通过自动化传感器数据的标注过程，解决了 tinyML 领域的一个主要痛点，简化了开发者构建和部署边缘 AI 应用的工作，有望加速物联网和可穿戴设备的开发。 SensorForge 是免费开源的，专为时间序列传感器数据设计，包含自动标注器以简化数据准备，以及一个直接分析信号数据的聊天机器人。作者表示自动标注器目前效果不错，但仍有改进空间。

reddit · r/MachineLearning · /u/No-Bug-4879 · 7月27日 02:38

**背景**: TinyML（微型机器学习）是一个专注于在低功耗微控制器和边缘设备上部署模型的机器学习领域，可实现低延迟的本地推理。tinyML 的一个关键挑战是对时间序列传感器数据进行标注，这一过程通常手动且耗时。虽然已有 Label Studio 等标注工具，但 SensorForge 将标注功能集成到了端到端的流程中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TinyML">TinyML</a></li>
<li><a href="https://labelstud.io/templates/time_series">Label Studio — Time Series Data Labeling Template</a></li>

</ul>
</details>

**标签**: `#edge ML`, `#tinyML`, `#open-source`, `#sensor data`, `#auto-labeling`

---