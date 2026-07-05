---
layout: default
title: "Horizon Summary: 2026-07-05 (ZH)"
date: 2026-07-05
lang: zh
---

> 从 45 条内容中筛选出 8 条重要资讯。

---

1. [GitHub 仓库汇总泄露的 AI 系统提示](#item-1) ⭐️ 9.0/10
2. [Organic Maps 因治理问题遭遇社区分叉 CoMaps](#item-2) ⭐️ 8.0/10
3. [Shadcn/UI 将默认组件库从 Radix 切换到 Base UI](#item-3) ⭐️ 8.0/10
4. [欧盟理事会快速推进聊天控制 1.0](#item-4) ⭐️ 8.0/10
5. [sqlite-utils 4.0rc2 发布，大部分由 AI 编写](#item-5) ⭐️ 8.0/10
6. [新 Claude 模型在工具调用规范遵循上出现退化](#item-6) ⭐️ 8.0/10
7. [学生为突尼斯达里贾语构建开源机器翻译流水线](#item-7) ⭐️ 8.0/10
8. [基于内部置信度的小模型工具调用门控](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GitHub 仓库汇总泄露的 AI 系统提示](https://github.com/asgeirtj/system_prompts_leaks) ⭐️ 9.0/10

一个名为 'system_prompts_leaks' 的 GitHub 仓库收集了来自 Anthropic、OpenAI、Google 和 xAI 等多个主要 AI 提供商的泄露系统提示。该仓库在过去 24 小时内获得了 49 颗星，显示出社区的高度关注。 这一收集为塑造 AI 行为的隐藏指令提供了前所未有的透明度，对研究人员、开发者以及更广泛的 AI 社区具有重要价值。了解这些提示有助于改进提示工程，并揭示 AI 护栏的实施方式。 该仓库包含从 Anthropic 的 Claude Fable 5 和 Opus 4.8、OpenAI 的 ChatGPT 5.5 Thinking 和 GPT 5.5 Instant、Google 的 Gemini 3.5 Flash 和 3.1 Pro，以及 xAI 的 Grok 等模型中提取的系统提示。该集合会定期更新，并使用 JavaScript 编写。

ossinsight · asgeirtj · 7月5日 20:44

**背景**: 系统提示是在用户交互之前给 AI 模型的一组隐藏指令，用于定义其个性、规则和限制。这些提示相当于 AI 助手的“员工手册”，规定了它们的行为方式。泄露这些提示可以揭示公司如何控制其 AI 模型，为提示工程技术和模型安全措施提供洞见。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://instawhat.ai/glossary/system-prompt">What is System Prompt ? Plain English Definition | Instawhat. ai</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prompt_engineering">Prompt engineering - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI`, `#system prompts`, `#leaks`, `#prompt engineering`, `#transparency`

---

<a id="item-2"></a>
## [Organic Maps 因治理问题遭遇社区分叉 CoMaps](https://organicmaps.app/) ⭐️ 8.0/10

开源导航应用 Organic Maps 因治理不透明、包含非开源组件以及涉嫌滥用捐款等问题，社区推出了名为 CoMaps 的分叉版本。 这次分叉凸显了开源社区在透明度和控制权方面的紧张关系，可能会分裂用户群体，并影响其他自由开源软件项目的治理方式。 CoMaps 大约一年前创建，并已增加 CarPlay 仪表盘支持等功能；而 Organic Maps 仍包含非开源组件（例如采用非自由许可证的 .mwm 地图文件）。

hackernews · tosh · 7月5日 14:14 · [社区讨论](https://news.ycombinator.com/item?id=48794446)

**背景**: Organic Maps 是一款基于 OpenStreetMap 数据的免费离线导航应用，由前 MapsWithMe 开发者创立。它因注重隐私而广受欢迎，但近期被指控添加广告、将部分代码闭源以及滥用捐款。CoMaps 由寻求完全开放和透明的社区成员分叉而来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lwn.net/Articles/1024387/">CoMaps emerges as an Organic Maps fork [LWN.net]</a></li>
<li><a href="https://en.wikipedia.org/wiki/CoMaps">CoMaps - Wikipedia</a></li>
<li><a href="https://github.com/comaps/comaps">GitHub - comaps/comaps: A mirror of https://codeberg.org/comaps/comaps. CoMaps is a community fork of Organic Maps. Based on principles of openness & transparency, not-for-profit & in the public interest, community-driven & accountable, fully free and open source software! · GitHub</a></li>

</ul>
</details>

**社区讨论**: 社区评论观点两极分化：部分用户因 Organic Maps 领导层的恶意行为而建议改用 CoMaps，另一些用户则仍将其视为有用工具。此外，还有关于 Organic Maps 非开源组件以及 CoMaps 需要更多测试者的讨论。

**标签**: `#open-source`, `#maps`, `#privacy`, `#community-governance`

---

<a id="item-3"></a>
## [Shadcn/UI 将默认组件库从 Radix 切换到 Base UI](https://ui.shadcn.com/docs/changelog) ⭐️ 8.0/10

流行的 React UI 库 Shadcn/UI 已将其默认底层组件库从 Radix UI 切换为由 Uber 开发的 Base UI。这一改变影响了 shadcn/ui 所依赖的基础组件。 这一转变影响了依赖 shadcn/ui 的开发者，可能影响包体积、可访问性模式和定制方式。它也凸显了 React 生态中无样式组件库的不断演变。 Base UI 是由 Uber 开发的无样式、无头组件库，理念与 Radix 相似但 API 不同且更注重可组合性。这一切换可能需要现有 shadcn/ui 用户进行迁移工作，对包体积的具体影响取决于所使用的具体组件。

hackernews · dabinat · 7月5日 04:46 · [社区讨论](https://news.ycombinator.com/item?id=48791328)

**背景**: Shadcn/UI 是一组可直接复制粘贴的组件集合，最初基于 Radix UI 构建。Radix UI 提供无样式、可访问的基础组件，而 Base UI 则提供另一套架构不同的基础组件。这一变化反映了 shadcn/UI 维护者的战略决策，采用可能提供更好开发者体验或性能特性的库。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://base-ui.com/">Unstyled UI components for accessible design systems · Base UI</a></li>
<li><a href="https://shadcnspace.com/blog/radix-ui-vs-base-ui">Radix UI vs Base UI - Detailed Guide - shadcnspace.com</a></li>

</ul>
</details>

**社区讨论**: 社区评论反应不一：一些用户对公告的 AI 生成语气表示担忧，而另一些用户则讨论包体积、可维护性以及此类库中过度使用 div 的权衡。人们对这一变化既有谨慎接受，也有对其实际好处的怀疑。

**标签**: `#UI`, `#Shadcn`, `#Radix`, `#Base UI`, `#Web Development`

---

<a id="item-4"></a>
## [欧盟理事会快速推进聊天控制 1.0](https://www.heise.de/en/news/Chat-Control-1-0-EU-Council-forces-messenger-scans-via-fast-track-11353659.html) ⭐️ 8.0/10

欧盟理事会已快速推进聊天控制 1.0，该法规允许消息服务提供商在无需法院命令的情况下扫描用户聊天内容以查找儿童性虐待材料，续签了一项先前已到期的临时措施。 这一决定对欧盟范围内的隐私和加密产生了重大影响，因为它强制要求客户端扫描，这可能会削弱端到端加密并导致大规模监控，影响数百万用户，并为数字权利树立了一个令人担忧的先例。 快速推进的法规仅涉及聊天控制 1.0，其侵入性低于拟议的聊天控制 2.0（后者会明确针对 Signal 等加密通讯软件），但仍允许扫描未加密或富含元数据的通信内容。

hackernews · stavros · 7月5日 11:44 · [社区讨论](https://news.ycombinator.com/item?id=48793393)

**背景**: 聊天控制指欧盟通过要求消息服务扫描用户内容来打击儿童性虐待材料的提案。客户端扫描是一项关键技术，它在消息加密和发送前与已知非法内容数据库进行比对。隐私倡导者警告称，这会破坏加密技术并可能导致更广泛的监控。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.patrick-breyer.de/en/posts/chat-control/">Chat Control : The EU ’s CSAM scanner proposal – Patrick Breyer</a></li>
<li><a href="https://www.internetsociety.org/resources/doc/2020/fact-sheet-client-side-scanning/">Fact Sheet: Client - Side Scanning - Internet Society</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了强烈反对，许多人认为快速推进是对隐私和民主程序的漠视。一些人指出了一种失败主义的叙事，即该措施不可避免，而另一些人则强调缺乏透明度并敦促继续抵制。

**标签**: `#EU`, `#privacy`, `#surveillance`, `#chat control`, `#digital rights`

---

<a id="item-5"></a>
## [sqlite-utils 4.0rc2 发布，大部分由 AI 编写](https://simonwillison.net/2026/Jul/5/sqlite-utils/#atom-everything) ⭐️ 8.0/10

Simon Willison 发布了 sqlite-utils 4.0rc2，这是流行 SQLite 工具库的一个主要版本候选版本，其大部分代码由 Anthropic 的 Claude Fable AI 模型编写，成本约为 149.25 美元。 此次发布展示了一种突破性的软件开发方法，其中 AI 不仅能生成代码，还能识别关键错误，展示了 AI 辅助开发在降低成本和提高质量方面的潜力。 AI 发现 delete_where() 中存在一个严重错误，该错误使连接处于损坏的事务状态，导致数据丢失。通过 37 次提示和 34 次提交，AI 帮助修复了此问题及其他问题，在 30 个文件中增加了 1,321 行代码并删除了 190 行。

rss · Simon Willison · 7月5日 00:47

**背景**: sqlite-utils 是一个用于创建和操作 SQLite 数据库的 Python 库和命令行工具，在数据社区中广泛使用。Claude Fable 是 Anthropic 开发的最先进的大型语言模型，擅长代码生成和长周期任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sqlite-utils.datasette.io/">sqlite - utils</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>

</ul>
</details>

**标签**: `#sqlite-utils`, `#release`, `#AI-assisted development`, `#Simon Willison`, `#tools`

---

<a id="item-6"></a>
## [新 Claude 模型在工具调用规范遵循上出现退化](https://simonwillison.net/2026/Jul/4/better-models-worse-tools/#atom-everything) ⭐️ 8.0/10

Armin Ronacher 报告称，Anthropic 的新版 Claude 模型（Opus 4.8 和 Sonnet 5）会在工具调用参数中发明额外字段，导致被 Pi 编辑框架拒绝，而旧模型没有出现此问题。 这种反直觉的退化表明，模型升级可能会降低特定工具接口的可靠性，削弱对 AI 编程代理的信任，并迫使第三方工具进行适配或实现特定模型的变通方案。 该问题具体表现在 Pi 自定义编辑工具的`edits[]`数组中，模型添加了意外键。Armin 推测，Anthropic 针对 Claude Code 原生编辑工具的强化学习可能无意中鼓励了在其他模式中的幻觉行为。

rss · Simon Willison · 7月4日 22:53

**背景**: 大型语言模型（如 Claude 和 GPT-4）可以被赋予带有 JSON 模式（schema）的工具，用于执行代码编辑等操作。遵循定义模式的工具调用可靠性对于自主代理至关重要。Anthropic 的 Claude Code 和类似的编码框架使用专门的编辑工具，但针对一种工具模式的训练可能会损害在其他模式上的表现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://letsdatascience.com/news/newer-claude-models-show-tool-calling-regression-6f029d5f">Newer Claude Models Show Tool-Calling Regression | Let's Data Science</a></li>
<li><a href="https://github.com/anthropics/claude-code/issues/64235">Regression (since 2026-05-29): intermittent "tool call was malformed and could not be parsed" — tool_use block absent on a stop_reason=tool_use turn · Issue #64235 · anthropics/claude-code</a></li>

</ul>
</details>

**标签**: `#LLM`, `#tool-calling`, `#Claude`, `#AI reliability`

---

<a id="item-7"></a>
## [学生为突尼斯达里贾语构建开源机器翻译流水线](https://www.reddit.com/r/MachineLearning/comments/1uo92vz/i_built_an_open_fromscratch_mt_pipeline_parallel/) ⭐️ 8.0/10

一名 18 岁学生发布了为突尼斯达里贾语（阿拉伯语方言）构建的从零开始的开源机器翻译流水线，包括一个识别 Arabizi 的 SentencePiece 分词器和一个 Transformer 模型，以及约 553 个手工构建的平行语料对，BLEU 得分为 3.89。 该项目填补了突尼斯达里贾语在低资源 NLP 领域的重大空白——此前缺少开放的平行语料库和专用基线。它提供了一个诚实的起点，并邀请社区贡献以扩大数据集并提升性能。 分词器使用共享的 16k 词汇表，并将 Arabizi 数字（3、7、9、5）视为保护符号。约 15.6M 参数的编码器-解码器 Transformer 从清洗过的摩洛哥达里贾语迁移学习，然后在突尼斯语料上微调；项目指出小数据量（553 对）是主要瓶颈，而非架构。

reddit · r/MachineLearning · /u/Dhiadev-tn · 7月5日 18:08

**背景**: 突尼斯达里贾语使用 Arabizi 书写（拉丁字母加数字表示阿拉伯语音素，如 3 代表'ع'，7 代表'ح'），是一种 NLP 资源稀缺的阿拉伯方言。SentencePiece BPE 是一种用于神经文本处理的子词分词器，能处理原始文本并支持保护符号以保留特殊字符。该项目利用这些技术为低资源语言创建了机器翻译基线系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Arabic_chat_alphabet">Arabizi - Wikipedia</a></li>
<li><a href="https://github.com/google/sentencepiece">GitHub - google/sentencepiece: Unsupervised text tokenizer for Neural Network-based text generation. · GitHub</a></li>
<li><a href="https://www.emergentmind.com/topics/sentencepiece-bpe-tokenizer">SentencePiece BPE Tokenizer</a></li>

</ul>
</details>

**标签**: `#machine translation`, `#low-resource NLP`, `#Tunisian Darija`, `#open source`, `#transformer`

---

<a id="item-8"></a>
## [基于内部置信度的小模型工具调用门控](https://www.reddit.com/r/MachineLearning/comments/1unw5un/competence_gate_gating_tooluse_on_a_small_models/) ⭐️ 8.0/10

发布了一个 10MB 的 Qwen3.5-4B LoRA 适配器，它基于内部置信度信号而非口头置信度来门控工具调用，从而实现了更好的错误检测并减少了幻觉。 该方法通过使用内部激活来应对小型语言模型的一个关键局限——无法准确口头表达不确定性——从而提高了工具使用场景的可靠性，并减少了私有数据泄露。 该适配器在错误捕获方面比基础模型提高了 0.46 的 d′值，双信号版本将发送到公共搜索的私有查询从 22%降至 10%。它通过 MLX 在 Apple Silicon 上本地运行，并通过 GGUF 支持 llama.cpp/Ollama，提供粗略的置信带（grounded/declined/answered）。

reddit · r/MachineLearning · /u/Synthium- · 7月5日 07:49

**背景**: 小型语言模型即使在出错时也常常生成过于自信的回复，因为它们口头表达的置信度并不反映内部的不确定性。最近的研究表明，内部激活信号可以提供更准确的置信度估计，从而实现更好的工具使用决策。该适配器利用这种内部信号来判断模型是直接回答、搜索网络还是检索本地文档。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aldeiadaponte.com/how-large-language-models-communicate-uncertainty-and-where-they-fail">How Large Language Models Communicate Uncertainty and Where...</a></li>
<li><a href="https://brics-econ.org/how-large-language-models-handle-what-they-don-t-know-communicating-uncertainty">How Large Language Models Handle What They Don't Know...</a></li>
<li><a href="https://arxiv.org/html/2605.02241v3">Zero-Shot Confidence Estimation for Small LLMs: When Supervised Baselines Aren’t Worth Training</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#confidence estimation`, `#tool use`, `#small language models`, `#LoRA`

---