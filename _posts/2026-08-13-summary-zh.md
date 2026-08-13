---
layout: default
title: "Horizon Summary: 2026-08-13 (ZH)"
date: 2026-08-13
lang: zh
---

> 从 32 条内容中筛选出 8 条重要资讯。

---

1. [DRAM 意面化：逆向内存寻址的新工具](#item-1) ⭐️ 9.0/10
2. [DeepSeek 发布 Harness 框架并开放 V4-Pro-0813 权重](#item-2) ⭐️ 9.0/10
3. [OpenAI 与 Cerebras 发布 GPT-5.6 Sol Ultrafast，推理速度最高提升 11 倍](#item-3) ⭐️ 8.0/10
4. [DeepMind 发布手语转文字模型 SL2T，落地 Pixel 11](#item-4) ⭐️ 8.0/10
5. [OpenAI 升级 ChatGPT：推出 GPT-5.6 Sol，扩大 Luna 免费使用权限](#item-5) ⭐️ 8.0/10
6. [谷歌发布 Gemini 3.6 Flash，并启动 Gemini 4 预训练](#item-6) ⭐️ 8.0/10
7. [Gemini 3.7 Flash](#item-7) ⭐️ 7.0/10
8. [DeepSeek V4 Pro 0813 现已通过 OpenRouter API 提供](#item-8) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [DRAM 意面化：逆向内存寻址的新工具](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 9.0/10

安全研究员 Christopher Domas 发布了一款名为 skitter-creek-bath-salts 的新工具，可逆向工程 AMD Family 16h CPU 的 DRAM 寻址，揭示底层内存结构。该工具在 AMD Family 16h 上开发并测试，这是最后一代其数据手册记载了 DRAM 控制器转换寄存器且表明这些寄存器无法锁定的处理器。 这暴露了硬件级攻击的一个巨大攻击面，可能让 ring-0 根权限访问隐藏在“负环”区域的功能。它可能影响依赖 DRAM 混淆性的主机安全和其他系统。 该工具目前适用于 AMD Family 16h CPU（2013 年的 Jaguar 架构）。说明指出 Zen 3 的内存控制器寄存器基地址不同，因此具体方法可能无法直接移植。

hackernews · matt_d · 8月13日 14:17 · [社区讨论](https://news.ycombinator.com/item?id=49286341)

**背景**: DRAM 寻址很复杂，因为内存被组织为通道、rank、bank 和 row，而物理地址到这些结构的映射通常是未文档化的。逆向该映射可以揭示如何针对特定内存位置进行攻击，正如之前的 DRAMA 等工作所示。该工具基于这一思路，利用老款 AMD CPU 的文档化转换寄存器来揭示寻址方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=49286341">Spaghettifying DRAM | Hacker News</a></li>
<li><a href="https://gruss.cc/files/drama.pdf">DRAMA: Exploiting DRAM Addressing</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论对这项研究表现出热情，用户称赞 Christopher Domas 之前的演讲。一些用户担心这可能会影响主机安全，另一些则询问对 Zen 3 等新款 CPU 的兼容性。

**标签**: `#security`, `#DRAM`, `#hardware`, `#reverse-engineering`, `#exploitation`

---

<a id="item-2"></a>
## [DeepSeek 发布 Harness 框架并开放 V4-Pro-0813 权重](https://mp.weixin.qq.com/s/mANdGRI4fO_sEbC1ECEoZQ) ⭐️ 9.0/10

DeepSeek 宣布推出 DeepSeek Harness 的开发者预览版，这是一款采用 MIT 协议的开源智能体框架，同时在 Hugging Face 上开放了 DeepSeek-V4-Pro-0813 模型权重。该框架采用“一切皆插件”的架构，提供标准、PTC、极简和创造四种运行模式。 此次发布意义重大，因为它将高度灵活的插件式智能体框架与开放权重的前沿模型相结合，为开发者提供了前所未有的控制力和透明度。MIT 协议和可追踪的会话日志可能使 DeepSeek 的产品与那些限制访问其追踪记录的专有美国模型区分开来。 Harness 基于 Cordis v4 框架构建，支持插件热重载和动态启用/禁用，包括 UI 组件和状态清理。Hugging Face 页面一度返回 404 错误，后来已恢复；该项目被描述为早期开发者预览版，预计会有破坏性变更。

telegram · zaihuapd · 8月13日 12:39

**背景**: DeepSeek 是一家以开放权重大语言模型著称的中国 AI 公司。这里的“harness”是指编排 AI 智能体的应用，负责管理模型、工具、会话、沙箱、存储、调度和 UI。PTC（Programmatic Tool Calling，程序化工具调用）模式让模型生成一段代码来编排多个工具调用，从而减少往返次数。Cordis 是一个用于可组合应用的元框架，提供插件生命周期管理和上下文隔离。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepseek.com/harness/en/">DeepSeek Harness developer preview: Everything is a plugin</a></li>
<li><a href="https://github.com/cordiverse/cordis">GitHub - cordiverse/cordis: Meta-Framework of Spatiotemporal ...</a></li>
<li><a href="https://deepseek-code.com/">DeepSeek Harness - Deepseek AI Coding Agent | deepseek ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者称赞可追踪的会话日志是“杀手级功能”，认为美国模型无法提供这一点；DeepSeek Harness 的一位作者确认这是早期开发者预览版并欢迎反馈。也有人对“一切皆插件”的做法表示怀疑，称已产生“插件疲劳”；还有人对底层 Cordis 论文的实际价值表示质疑。

**标签**: `#DeepSeek`, `#AI`, `#Open Source`, `#LLM`, `#Model Release`

---

<a id="item-3"></a>
## [OpenAI 与 Cerebras 发布 GPT-5.6 Sol Ultrafast，推理速度最高提升 11 倍](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 8.0/10

OpenAI 和 Cerebras 宣布推出 GPT-5.6 Sol Ultrafast，这是一个由 Cerebras 硬件驱动的新 API 服务层级，每秒最多可生成 750 个输出 token。两家公司称其推理速度比标准处理快 7–11 倍，准确性相当，例如在大约 11 小时内回答了全部 2500 道 HLE 问题。 这一合作将前沿模型智能引入对延迟敏感的应用，可能改变实时编码助手、智能体工作流和企业决策。这也加剧了围绕推理速度的竞争，使软硬件协同设计成为 AI 实验室和芯片厂商的战略优势。 值得注意的是，OpenAI 和 Cerebras 的公告都没有明确表示 Ultrafast 生成的结果与标准版 GPT-5.6 Sol 完全相同，也没有公布新层级的价格。速度对比依赖于内部评估或 Artificial Analysis 的报告，一些评论者认为这些证据无法证明两者性能完全一致。

hackernews · pr337h4m · 8月13日 18:10 · [社区讨论](https://news.ycombinator.com/item?id=49289844)

**背景**: Cerebras Systems 设计晶圆级引擎（WSE），这是全球最大的 AI 处理器，并提供用于训练和推理的云 API。GPT-5.6 Sol 是 OpenAI 的旗舰推理模型，面向复杂编码和智能体任务。Ultrafast 模式利用 Cerebras 硬件消除瓶颈，提供高 token 吞吐量，使前沿模型适用于实时场景。HLE（人类终极考试）是一个用于测试前沿知识的严苛基准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://openai.com/index/previewing-ultrafast/">Previewing Ultrafast mode: GPT - 5 . 6 Sol at up to 14X the... | OpenAI</a></li>
<li><a href="https://www.cerebras.ai/press-release/cerebras-announces-third-generation-wafer-scale-engine">Cerebras Systems Unveils World’s Fastest AI Chip with ...</a></li>

</ul>
</details>

**社区讨论**: 评论者对速度感到兴奋，但对性能是否真正达到标准模型水平表示怀疑，指出缺乏明确的等同性声明。有人指出未公布价格，可能意味着价格昂贵或仍在探询市场反应；另一些人则认为更快的推理被低估，并就推理级别提出问题。

**标签**: `#AI`, `#Inference Speed`, `#OpenAI`, `#Cerebras`, `#Hardware`

---

<a id="item-4"></a>
## [DeepMind 发布手语转文字模型 SL2T，落地 Pixel 11](https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/) ⭐️ 8.0/10

谷歌 DeepMind 发布了大规模多语言手语转文字模型 SL2T，并首次将其部署到消费产品中。该模型为 Pixel 11 上的 Gboard 和 Live Transcribe 提供手语转文字功能，初期支持美国手语（ASL）转英语。 这标志着大规模手语 AI 模型首次进入主流消费手机功能，有望改善全球约 7000 万聋人和听障人士的无障碍体验。它还在 FLEURS-ASL 基准上大幅刷新了手语翻译的纪录，树立了新标杆。 SL2T 使用超过 10 万小时、涵盖 50 多种手语的数据进行训练。它在 FLEURS-ASL 基准上的零样本得分为 70 BLEURT，远高于此前纪录；为保护隐私，该模型只处理手部和身体姿态关键点，不读取原始视频。

telegram · zaihuapd · 8月13日 08:55

**背景**: 与口语语言相比，手语翻译长期以来在 AI 研究中被忽视。FLEURS-ASL 是一个将多语言评估套件 FLORES/FLEURS 扩展到美国手语的基准，由持证聋人译员创建。BLEURT 是一种基于学习的评估指标，用于衡量生成译文与人类质量判断的匹配程度，分数越高表示流畅度和语义保留越好。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/">Putting sign language AI into users’ hands — Google DeepMind</a></li>
<li><a href="https://en.cryptonomist.ch/2026/08/13/sign-language-ai-translation-slt2/">Sign Language AI Translation: Google's Breakthrough with SL2T ...</a></li>
<li><a href="https://arxiv.org/abs/2408.13585">FLEURS-ASL: Including American Sign Language in Massively ... [PDF] FLEURS-ASL: Including American Sign Language in ... Title:FLEURS-ASL: Including American Sign Language in ... (PDF) FLEURS-ASL: Including American Sign Language in ... AITopics | FLEURS-ASL: Including American Sign Language in ... FLEURS-ASL: Including American Sign Language in Massively ...</a></li>

</ul>
</details>

**标签**: `#sign language`, `#AI`, `#DeepMind`, `#accessibility`, `#speech-to-text`

---

<a id="item-5"></a>
## [OpenAI 升级 ChatGPT：推出 GPT-5.6 Sol，扩大 Luna 免费使用权限](https://t.me/zaihuapd/43176) ⭐️ 8.0/10

OpenAI 已为 Plus 和 Pro 用户更新 ChatGPT 中的 GPT-5.6 Sol，新增滑块控制推理深度；本周起免费用户默认使用 GPT-5.6 Luna，下周起可无限文本对话，并新增 Think 按钮。 此次更新大幅扩大了免费用户对更强大 GPT-5.6 模型的访问权限，同时让付费用户能精细控制推理强度，这可能加剧 AI 助手间的竞争，并让普通用户更容易用上先进 AI 功能。 GPT-5.6 是一个包含 Luna、Terra 和 Sol 三个变体的模型系列，按能力从低到高排列。OpenAI 的内部评估显示，在财经、医疗和法律问题上，GPT-5.6 Luna 的事实错误比之前的 GPT 模型更少。

telegram · zaihuapd · 8月13日 17:04

**背景**: GPT-5.6 系列由 OpenAI 于 2026 年 7 月 9 日发布，设计目标是支撑企业办公、编程、科学研究和网络安全。由于政府限制，其公开发布起初受到约束。ChatGPT 中新增的 Think 按钮用于应对需要深度推理的复杂问题，与付费用户的推理深度滑块相辅相成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6_Sol">GPT-5.6 Sol</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6_Luna">GPT-5.6 Luna</a></li>
<li><a href="https://openai.com/index/improving-gpt-5-6-sol-in-chatgpt/">Improving GPT ‑ 5 . 6 Sol in ChatGPT—and expanding access... | OpenAI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#ChatGPT`, `#GPT-5.6`, `#AI`, `#Model Release`

---

<a id="item-6"></a>
## [谷歌发布 Gemini 3.6 Flash，并启动 Gemini 4 预训练](https://t.me/zaihuapd/43177) ⭐️ 8.0/10

谷歌发布了 Gemini 3.6 Flash，称其相比 Gemini 3.5 Flash 将输出 Token 减少 17%，并能通过更少的推理步骤和工具调用完成多步任务。谷歌同时披露，下一代模型 Gemini 4 的预训练已经启动。 此次发布表明谷歌正在大力提升模型效率与智能体能力，同时保持 API 定价具有竞争力；Gemini 4 的预告也显示前沿模型竞争正在快速迭代。依赖谷歌 AI API 的开发者和企业将受益于更低的 Token 成本和更强的代码生成与计算机操作能力。 公告显示，Gemini 3.6 Flash 增强了代码生成、知识工作和计算机操作能力，知识截止日期更新至 2026 年 3 月。其 API 定价为每百万输入 Token 1.5 美元、每百万输出 Token 7.5 美元；谷歌还面向高吞吐、低延迟场景推出了 Gemini 3.5 Flash。

telegram · zaihuapd · 8月13日 17:32

**背景**: 大型语言模型在处理文本前会先把文本切分为 Token（如单词、字符组合或标点等小单元），因此“输出 Token”指的是模型生成的文本量。工具调用（Tool calling）让模型能够与外部 API 和系统交互以获取数据或执行操作，从而减少完成复杂任务所需的模型调用次数。计算机操作能力则指 AI 智能体可以像人一样操作电脑软件（例如查看屏幕、移动鼠标、点击按钮）来完成跨应用的工作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/dotnet/ai/conceptual/understanding-tokens">Understanding tokens - .NET | Microsoft Learn</a></li>
<li><a href="https://www.kore.ai/ai-glossary/tool-calling">What Is tool calling in AI and why does it matter?</a></li>
<li><a href="https://cua.ai/docs/concepts/what-is-computer-use">Computer use: how AI agents operate computers | Cua docs</a></li>

</ul>
</details>

**标签**: `#AI`, `#Google`, `#Gemini`, `#LLM`, `#Model Release`

---

<a id="item-7"></a>
## [Gemini 3.7 Flash](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 7.0/10

谷歌推出 Gemini 3.7 Flash，这是一款新的大型语言模型，具备改进的视觉和代码生成能力，引发了社区的积极讨论。

hackernews · thisisauserid · 8月13日 17:23 · [社区讨论](https://news.ycombinator.com/item?id=49289112)

**标签**: `#AI`, `#Gemini`, `#Google`, `#LLM`, `#Model Release`

---

<a id="item-8"></a>
## [DeepSeek V4 Pro 0813 现已通过 OpenRouter API 提供](https://simonwillison.net/2026/Aug/12/deepseek-v4-pro-0813/) ⭐️ 7.0/10

DeepSeek V4 Pro 0813（DeepSeek Pro 系列的最新快照）已于 2026 年 8 月 12 日起通过 OpenRouter API 提供。该版本支持思考与非思考模式，但开源权重是否会发布仍未确认。 此次发布延续了 DeepSeek 快速的迭代节奏，并让开发者能够通过 OpenRouter 的统一接口立即使用。鉴于 DeepSeek 此前曾开放权重，本次模型的授权决定将对开源 AI 生态产生重大影响。 模型信息显示，DeepSeek V4 Pro 0813 提供 100 万 token 的上下文窗口、最高 38.4 万 token 的输出，定价为每百万输入 token 0.43 美元、每百万输出 token 0.87 美元。Simon Willison 还发现，在低、中、高三种推理级别下，模型生成的图像差异极大——他表示这是其他模型未曾出现过的行为。

rss · Simon Willison · 8月12日 23:59

**背景**: DeepSeek 是一家中国 AI 实验室，以发布开放权重模型著称，包括 2026 年 4 月的 DeepSeek-V4-Pro 和 7 月的 DeepSeek-V4-Flash-0731。OpenRouter 是一个统一的 API 网关，让开发者通过单一接口访问多家 LLM，并将请求路由到实际供应商。所谓“推理级别”控制模型在响应前投入多少推理时计算量，通常借助思维链（chain-of-thought）等技术实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://models.dev/models/deepseek/deepseek-v4-pro-0813/">DeepSeek V 4 Pro 0813 pricing, providers, and specs | Models .dev</a></li>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>
<li><a href="https://huggingface.co/multimodalart/DeepSeek-V4-Pro-0813">multimodalart/ DeepSeek - V 4 - Pro - 0813 · Hugging Face</a></li>

</ul>
</details>

**标签**: `#deepseek`, `#ai`, `#llm`, `#api`, `#open-source`

---