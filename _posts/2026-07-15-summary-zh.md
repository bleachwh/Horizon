---
layout: default
title: "Horizon Summary: 2026-07-15 (ZH)"
date: 2026-07-15
lang: zh
---

> 从 36 条内容中筛选出 8 条重要资讯。

---

1. [Stripe 与 Advent 联合收购 PayPal，出价超 530 亿美元](#item-1) ⭐️ 9.0/10
2. [利用 Claude 的 web_fetch 漏洞窃取隐私数据](#item-2) ⭐️ 9.0/10
3. [Inkling：一款支持音频的全新开放权重多模态 AI 模型](#item-3) ⭐️ 8.0/10
4. [26B 大模型在无 GPU 的旧 CPU 上以 5 tok/s 运行](#item-4) ⭐️ 8.0/10
5. [Telegram 推出机器人后端无服务器平台](#item-5) ⭐️ 8.0/10
6. [通过哈达玛积聚类解缠卷积神经元](#item-6) ⭐️ 8.0/10
7. [DeepSeek 计划 2027 年上市，寻求 710 亿美元估值融资](#item-7) ⭐️ 8.0/10
8. [DeepSeek 首轮融资超 500 亿元，采用特殊架构保持创始人控制](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Stripe 与 Advent 联合收购 PayPal，出价超 530 亿美元](https://www.reuters.com/business/finance/stripe-advent-offer-buy-paypal-more-than-53-billion-sources-say-2026-07-15/) ⭐️ 9.0/10

据知情人士透露，Stripe 与私募股权公司 Advent International 已联合出价超过 530 亿美元收购 PayPal，此举可能打造在线支付领域的巨头。 此次合并将整合 Stripe 的支付基础设施与 PayPal 的消费者品牌及 Venmo/Braintree，因市场集中度而引发反垄断担忧。这可能会显著改变非面对面卡支付的竞争格局，对商家和消费者产生深远影响。 出价对 PayPal 估值超过 530 亿美元，为满足反垄断监管，交易可能需要剥离 Venmo 和 Braintree 等资产。Stripe 本身是估值约 700 亿美元的支付处理巨头，而 Advent 是一家管理资产超 560 亿美元的全球私募股权公司。

hackernews · rvz · 7月15日 03:32 · [社区讨论](https://news.ycombinator.com/item?id=48915953)

**背景**: PayPal 是在线支付领域的长期领导者，旗下拥有 PayPal Checkout、Venmo 和 Braintree 等服务。Stripe 是一家较新的、面向开发者的支付平台，深受初创企业和大型企业欢迎。Advent International 是一家专注于成长型公司投资的私募股权公司。支付行业的整合因非面对面卡交易市场份额过高而引发反垄断问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Advent_International">Advent International - Wikipedia</a></li>
<li><a href="https://www.adventinternational.com/">Advent International - A leading global private equity investor</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了强烈担忧：有人担心若 Braintree 并入 Stripe 会导致手续费上涨，还有人指出 Stripe 对成人用品和大麻相关业务的政策比 PayPal 更严格。评论者还担心失去支付选择权以及账户被标记的风险增加，有人指出非面对面卡支付的赫芬达尔-赫希曼指数将“高得离谱”。

**标签**: `#acquisition`, `#PayPal`, `#Stripe`, `#payments`, `#antitrust`

---

<a id="item-2"></a>
## [利用 Claude 的 web_fetch 漏洞窃取隐私数据](https://simonwillison.net/2026/Jul/15/claude-web-fetch-exfiltration/#atom-everything) ⭐️ 9.0/10

安全研究员 Ayush Paul 发现 Claude 的 web_fetch 工具存在一个漏洞，他通过一个恶意蜜罐网站上的嵌套链接，诱使 AI 泄露用户的私人数据，如姓名、城市和雇主。 此次攻击绕过了 Anthropic 设计的安全保护，表明即使是精心设计的针对提示注入和数据窃取的防御措施，也可能被允许操作的创造性链式利用所击败，凸显了保护 AI 代理安全的持续挑战。 该漏洞允许 web_fetch 跟随之前获取的页面中嵌入的链接，攻击者利用这一点创建了一个字母序列，逐步提取用户记忆数据。Anthropic 已在内部发现此问题，并通过移除该能力关闭了漏洞，因此未支付漏洞赏金。

rss · Simon Willison · 7月15日 14:21

**背景**: AI 代理的'致命三重奏'指的是同时具备访问私有数据、接触不可信外部内容和执行出站操作的能力。Claude 的 web_fetch 工具设计为只能获取用户明确提供或由 web_search 工具返回的 URL，从而防止动态构造恶意 URL。然而，通过允许访问获取页面内的链接，一个蜜罐网站得以逐步诱骗代理窃取数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/agents-and-tools/tool-use/web-fetch-tool">Web fetch tool - Claude Platform Docs</a></li>
<li><a href="https://simonwillison.net/2025/Sep/10/claude-web-fetch-tool/">Claude API: Web fetch tool</a></li>
<li><a href="https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/">The lethal trifecta for AI agents: private data, untrusted content, and external communication</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#prompt injection`, `#Claude`, `#security`, `#data exfiltration`

---

<a id="item-3"></a>
## [Inkling：一款支持音频的全新开放权重多模态 AI 模型](https://thinkingmachines.ai/news/introducing-inkling/) ⭐️ 8.0/10

Thinking Machines AI 发布了 Inkling，这是一个开放权重的多模态模型，可接受文本、图像和音频输入并生成文本输出，定位为具有竞争力的开源替代方案，引起了社区的浓厚兴趣。 Inkling 填补了美国开源多模态模型在音频支持方面的空白，使企业能够以更低成本微调和定制模型以满足特定任务需求，并减少对闭源或外国模型的依赖。 Inkling 支持 100 万 token 的上下文窗口，并可在 Tinker 平台上进行微调，社区已将其移植到 llama.cpp 和 GGUF 格式，便于本地部署。它并非综合能力最强的模型，但结合了多模态能力、高效推理和可定制性。

hackernews · vimarsh6739 · 7月15日 18:12 · [社区讨论](https://news.ycombinator.com/item?id=48924912)

**背景**: 开放权重模型允许任何人下载和使用神经网络训练好的参数（权重），从而实现修改、微调和本地部署。多模态模型能够处理多种数据类型，例如文本、图像和音频，扩展了其在内容分析和智能体系统等实际任务中的适用性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://thinkingmachines.ai/model-card/inkling/">Inkling Model Card - Thinking Machines Lab</a></li>
<li><a href="https://huggingface.co/thinkingmachines/Inkling-NVFP4">thinkingmachines/ Inkling -NVFP4 · Hugging Face</a></li>

</ul>
</details>

**社区讨论**: 社区成员对 Inkling 表现出热情，一些人认为它可能成为美国对 DeepSeek 等中国开源模型的回应。其他人则强调其在企业微调和本地部署方面的潜力，但也有部分人希望看到详细的音频性能基准测试。

**标签**: `#open-source`, `#multimodal`, `#AI model`, `#audio`, `#machine learning`

---

<a id="item-4"></a>
## [26B 大模型在无 GPU 的旧 CPU 上以 5 tok/s 运行](https://www.neomindlabs.com/2026/06/08/running-gemma-4-26b-at-5-tokens-sec-on-a-13-year-old-xeon-with-no-gpu/) ⭐️ 8.0/10

一个 260 亿参数的 Gemma 4 模型在无 GPU 的 13 年老款 Intel Xeon CPU 上成功以每秒 5 个 token 运行，展示了在过时硬件上进行本地推理的可行性。 这一成就挑战了运行大型语言模型必须配备强大 GPU 的假设，可能让更多人无需昂贵硬件就能使用 AI。它还突显了持续优化的成果，使 CPU 推理对资源有限的爱好者和研究者更具实用性。 使用的模型是 Google DeepMind 的 Gemma 4 26B，一个 260 亿参数的开源权重模型。CPU 是 13 年前的 Xeon（例如 E5-2670 时代），在没有 GPU 加速的情况下实现了每秒 5 个 token 的推理速度，很可能借助了量化和高效的 CPU 内核。

hackernews · neomindryan · 7月15日 15:34 · [社区讨论](https://news.ycombinator.com/item?id=48922434)

**背景**: 像 Gemma 这样的大型语言模型通常需要 GPU 来运行，因为它们需要大量并行计算。然而，最近在模型量化、剪枝和针对 CPU 的推理库方面的优化，使得在消费级 CPU 上运行较小的 LLM 成为可能，尽管速度较慢。Gemma 4 是 Google DeepMind 基于 Gemini 技术的最新开源权重模型，设计上轻量但功能强大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gemma_(LLM)">Gemma (LLM)</a></li>
<li><a href="https://arxiv.org/abs/2406.07553">[2406.07553] Inference Acceleration for Large Language Models on CPUs</a></li>

</ul>
</details>

**社区讨论**: 社区成员发表了不同看法：有人预测到 2027 年中，超过 200B 参数的 MoE 模型可以在消费级硬件上运行，并以在 MacBook 上本地运行 Qwen3.6-35B-A3B 为例。另一些人则争论成本效益，指出使用推理服务商的费用可能比本地电费更便宜。有用户报告在类似的老 CPU 上达到更高的速度（8-12 tok/s），而另一人指出双 Xeon 系统的电力成本与云定价相当但速度更慢。

**标签**: `#LLM`, `#local inference`, `#CPU inference`, `#Gemma`, `#optimization`

---

<a id="item-5"></a>
## [Telegram 推出机器人后端无服务器平台](https://core.telegram.org/bots/serverless) ⭐️ 8.0/10

Telegram 正式推出无服务器平台，开发者可通过一条命令 npx tgcloud push 将 JavaScript 模块直接部署到 Telegram 基础设施上，用于机器人和 Mini App 后端，并自带 SQLite 数据库。 这简化了机器人开发，无需管理服务器、容器或扩容，可能降低创建复杂 Telegram 机器人和 Mini App 的门槛，并促进 Telegram 生态系统的创新。 代码运行在靠近 Bot API 的隔离 V8 沙箱中，内置 SQLite 数据库提供持久化存储，但执行时间、存储和数据库大小等配额尚未公布。

hackernews · soheilpro · 7月15日 10:06 · [社区讨论](https://news.ycombinator.com/item?id=48918534)

**背景**: 无服务器计算允许开发者在不配置或管理服务器的情况下运行代码，由云提供商处理扩容和维护。Telegram 的 Bot API 长期以来支持交互式机器人，但之前需要开发者自行托管后端服务器。这个新平台是向 Telegram 内完全集成机器人托管迈出的重要一步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://core.telegram.org/bots/serverless">Telegram Serverless</a></li>

</ul>
</details>

**社区讨论**: 社区成员对实际限制如执行时间、存储配额和 SQLite 数据库大小上限感到好奇，也存在关于集成外部服务的秘密管理问题，同时定价问题尚未得到解答。

**标签**: `#Telegram`, `#serverless`, `#bots`, `#JavaScript`, `#development`

---

<a id="item-6"></a>
## [通过哈达玛积聚类解缠卷积神经元](https://www.reddit.com/r/MachineLearning/comments/1uwya70/mechanistic_interpretability_a_first_paper_on/) ⭐️ 8.0/10

一种新方法利用哈达玛积聚类来解缠 InceptionV1 中单个卷积神经元检测到的模式，揭示了高激活集群（如汽车、猫、狗）和低激活集群（如字母、人脸）的存在，并有证据显示梯度下降将权重分布在依赖神经元之间。 这项工作通过提供分析多义神经元的技术推进了机械可解释性，有助于理解神经网络内部机制并提高模型透明度。它还强调了神经元行为超出简单特征检测的复杂性。 该方法专注于 InceptionV1 的 mixed4e 层中的 1x1 卷积神经元；将感受野与神经元权重的哈达玛积进行聚类，以揭示不同的模式组。作者注意到，低激活集群涉及多个依赖神经元在相同概念上激活，且正负权重分布平衡。

reddit · r/MachineLearning · /u/narang_27 · 7月15日 06:59

**背景**: 机械可解释性旨在通过分析内部结构来逆向工程神经网络。多义神经元对多个无关特征产生响应，使分析复杂化。哈达玛积是逐元素矩阵乘法，常用于神经网络的门控机制。这项工作通过对哈达玛积进行聚类来解缠此类神经元。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanistic_interpretability">Mechanistic interpretability</a></li>
<li><a href="https://en.wikipedia.org/wiki/Hadamard_product_(matrices)">Hadamard product (matrices) - Wikipedia</a></li>
<li><a href="https://www.simonsfoundation.org/2017/06/13/untangling-neurons/">Untangling Neurons | Simons Foundation</a></li>

</ul>
</details>

**标签**: `#mechanistic interpretability`, `#neuron disentangling`, `#convolutional neural networks`, `#interpretability`, `#deep learning`

---

<a id="item-7"></a>
## [DeepSeek 计划 2027 年上市，寻求 710 亿美元估值融资](https://t.me/zaihuapd/42577) ⭐️ 8.0/10

DeepSeek 已启动 IPO 筹备，最快今年底或明年初提交申请，目标 2027 年上市。公司同时寻求新一轮私募融资，投前估值至少 4800 亿元人民币（约 710 亿美元）。 这标志着中国领先的人工智能公司之一的重要里程碑，反映了投资者对 AI 行业的强劲信心和快速增长。高估值和上市计划表明 DeepSeek 有全球扩张并与主要 AI 模型竞争的雄心。 DeepSeek 于 6 月初完成了首轮外部融资，从腾讯和宁德时代等投资者处筹集了 7 亿美元。新一轮融资目标至少 100 亿元，最终金额可能因投资者数量而翻数倍。

telegram · zaihuapd · 7月15日 07:04

**背景**: DeepSeek 是一家总部位于杭州的中国人工智能公司，由对冲基金 High-Flyer 创立，以开发大型语言模型（如 DeepSeek-V3）而闻名。投前估值是指公司在获得新投资前的价值，常用于风险投资中确定股权分配。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://www.investopedia.com/terms/p/premoneyvaluation.asp">investopedia.com/terms/p/premoneyvaluation.asp</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#IPO`, `#AI funding`, `#valuation`, `#business`

---

<a id="item-8"></a>
## [DeepSeek 首轮融资超 500 亿元，采用特殊架构保持创始人控制](https://t.me/zaihuapd/42589) ⭐️ 8.0/10

DeepSeek 完成首轮融资，筹得逾 500 亿元人民币（约 74 亿美元），估值超过 500 亿美元。公司采用特殊架构，投资者需将资金投入由 CEO 梁文锋管理的有限合伙企业，而非直接投资 DeepSeek，并需接受五年锁定期且不享有表决权。 此轮巨额融资凸显了投资者对 DeepSeek AI 潜力的强烈信心，而独特的治理结构为中国 AI 初创公司在大量资本涌入时保持创始人控制权树立了先例。 CEO 梁文锋在本轮融资中个人投资 200 亿元。腾讯和宁德时代分别考虑或计划投资 100 亿元和 50 亿元，可能成为最大的外部投资者。DeepSeek 对此暂未置评。

telegram · zaihuapd · 7月15日 12:56

**背景**: 在中国科技行业，初创公司常采用可变利益实体（VIE）或有限合伙结构来分离经济权利与投票权，使创始人能在融资的同时保持控制权。DeepSeek 采用由 CEO 管理的有限合伙企业是实现这一策略的一种变体。这种结构确保尽管有大量外部投资，关键战略决策仍由创始人掌控。

**标签**: `#AI`, `#Funding`, `#DeepSeek`, `#Venture Capital`, `#Governance`

---