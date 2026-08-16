---
layout: default
title: "Horizon Summary: 2026-08-16 (ZH)"
date: 2026-08-16
lang: zh
---

> 从 26 条内容中筛选出 8 条重要资讯。

---

1. [Anthropic 发布 Claude 模型官方系统提示词](#item-1) ⭐️ 9.0/10
2. [培育新想法诞生的心境](#item-2) ⭐️ 8.0/10
3. [重新审视高效通道注意力：跨通道交互的核心假设存疑](#item-3) ⭐️ 8.0/10
4. [Anthropic 第二季营收暴涨 14 倍超 115 亿美元，IPO 在即](#item-4) ⭐️ 8.0/10
5. [Firefox for iOS 新增原生广告拦截功能](#item-5) ⭐️ 7.0/10
6. [怪词“肾脏失望”暴露论文 AI 改写问题](#item-6) ⭐️ 7.0/10
7. [达里奥·阿莫迪：公众对 AI 的不信任是信任危机，而非营销问题](#item-7) ⭐️ 7.0/10
8. [SSOG-Attention：可分离高斯和实现次二次注意力](#item-8) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Anthropic 发布 Claude 模型官方系统提示词](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 9.0/10

Anthropic 已在官方文档网站发布了 Claude 模型所用系统提示词，公开了塑造助手行为和安全响应的底层指令。这是一次罕见的透明度举措，因为这些提示词通常属于保密内容。 这种透明度让开发者、研究人员和用户能够清楚看到 Claude 是如何被引导的，包括安全权衡与任务优先级之间如何平衡。此举为通常对系统提示词保密的 AI 行业树立了宝贵先例，并可能影响其他实验室的问责方式。 这些系统提示词包含细致入微的指令，例如当用户处于危机状态时，优先考虑其福祉而非完成任务，以及要求 Claude 先核实图像是否真的存在，而不是默认已有图像。提示词是按版本管理的，并且会随模型发布而变化，社区成员通过跟踪 diff 凸显了这一点。

hackernews · tosh · 8月16日 12:48 · [社区讨论](https://news.ycombinator.com/item?id=49319556)

**背景**: 系统提示词是在任何用户交互之前提供给大语言模型的特殊指令，用于定义其角色、人设、行为边界和响应特征，相当于塑造模型输出的“路线图”。Anthropic 决定公开这些提示词，为外界了解生产级 LLM 行为是如何被设计出来的提供了一扇窗口；不过这些提示词只是训练与对齐这一庞大体系中的一层。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://promptengineering.org/system-prompts-in-large-language-models/">System Prompts in Large Language Models</a></li>
<li><a href="https://tetrate.io/learn/ai/system-prompts-guide">System Prompts: Design Patterns and Best Practices</a></li>

</ul>
</details>

**社区讨论**: 社区反响热烈：Simon Willison 创建了提示词变更的 Git 历史，并指出了诸如新模型引用等有趣的补充。其他人则就特定安全指令的含义展开争论，有人称赞危机响应优先级的设定，也有人质疑为何如此强大的模型仍需要“检查是否上传了图片”这类基础指令。另有一条评论对论坛移除负面 AI 报道提出了审查方面的担忧。

**标签**: `#AI`, `#Claude`, `#system prompts`, `#LLM`, `#transparency`

---

<a id="item-2"></a>
## [培育新想法诞生的心境](https://www.henrikkarlsson.xyz/p/good-ideas) ⭐️ 8.0/10

2023 年，Henrik Karlsson 发表了一篇文章，主张新想法是脆弱的，需要独处和内在动机才能存活并成长。文章提供了一个培育新想法诞生之心理状态的框架。 这篇文章之所以重要，是因为它提供了一种关于创造力的心态视角，对软件工程师和研究人员尤其有启发意义，促使人们反思环境如何滋养或扼杀新想法。社区的热烈反响表明，这一话题与正在攻克难题的人们产生了深刻共鸣。 文章强调，新想法很容易被嘲笑、干扰或过早商业化所扼杀，并观察到许多人在年轻时期更容易产生最好的想法，这可能与大脑可塑性有关。文章还讨论了独处与协作之间的平衡，认为合适的伙伴关系同样有价值。

hackernews · felixbraun · 8月15日 20:54 · [社区讨论](https://news.ycombinator.com/item?id=49314235)

**背景**: 这篇文章属于关于创造力与深度思考的一类写作文体，探讨突破性想法究竟如何诞生。许多科学和艺术突破的记述都强调，这类想法往往出现在不受打扰的反思期间，而非高压或竞争激烈的环境中。文章延续了这一传统，考察了使这种反思成为可能的内心条件，例如独处和内在动机。

**社区讨论**: 评论区整体对文章表示赞赏，但围绕“独处是产生新想法的核心条件”这一观点展开了辩论。有评论者结合个人经历证实新想法的脆弱性，也有人举出学术实验室的反例，认为紧密协作同样重要。反复出现的一个主题是：需要在独处与合适的协作环境之间取得平衡。

**标签**: `#creativity`, `#ideas`, `#deep work`, `#thinking`, `#personal development`

---

<a id="item-3"></a>
## [重新审视高效通道注意力：跨通道交互的核心假设存疑](https://www.reddit.com/r/MachineLearning/comments/1vptaw9/revisiting_the_efficient_channel_attention_paper/) ⭐️ 8.0/10

一篇 Reddit 帖子重新审视了高效通道注意力（ECA）论文，认为其关于局部跨通道交互重要性的核心假设在概念上存在缺陷。作者利用国际象棋残局库证明，kernel 大小为 k=1 的 ECA 与 k=3 的表现几乎一样好，这与论文声称的机制相矛盾。 ECA-Net 被引用数千次，在计算机视觉领域被广泛使用，因此质疑其概念基础会影响未来注意力模块的设计。实证结果表明，简单的逐通道门控可能与更复杂的跨通道策略同样有效。 实验使用 6 子国际象棋残局库作为基准，从完整的 370 万个局面中采样，避免了数据集偏差。结果显示 ECA(k=3)准确率为 96.68%，ECA(k=1)为 96.61%，逐通道门控为 96.65%，表明跨通道交互并非性能提升的主要来源。

reddit · r/MachineLearning · /u/arkuto · 8月16日 10:13

**背景**: 通道注意力机制如 Squeeze-and-Excitation（SE）通过全局平均池化后接一个小型隐藏层来重新校准特征通道。ECA 改为对通道均值应用一维卷积以避免降维，但通道是无序的特征维度，对它们做卷积等于假设了一个不存在的拓扑结构。国际象棋残局库提供了一个完整且无偏的评估环境，因为所有可能的局面都已知，这与 CIFAR-10 等采样图像数据集不同。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/1910.03151">[1910.03151] ECA-Net: Efficient Channel Attention for Deep Convolutional Neural Networks</a></li>
<li><a href="https://www.shadecoder.com/topics/efficient-channel-attention-a-comprehensive-guide-for-2025">Efficient Channel Attention: A Comprehensive Guide for 2025 ...</a></li>
<li><a href="https://d2l.ai/chapter_convolutional-neural-networks/channels.html">7.4. Multiple Input and Multiple Output Channels — Dive into Deep Learning 1.0.3 documentation</a></li>

</ul>
</details>

**标签**: `#deep learning`, `#attention mechanisms`, `#computer vision`, `#model efficiency`, `#research critique`

---

<a id="item-4"></a>
## [Anthropic 第二季营收暴涨 14 倍超 115 亿美元，IPO 在即](https://www.cnbc.com/2026/08/15/anthropic-revenue-jumps-to-over-11point5-billion-in-q2-report.html) ⭐️ 8.0/10

Anthropic 第二季初步营收超过 115 亿美元，同比增长逾 14 倍，高于去年同期的 7.87 亿美元与 2026 年第一季的 47.3 亿美元。当季调整后营业利润转正，公司正在筹备可能于今秋启动的大型 IPO。 这一强劲的营收增长和盈利路径表明，Anthropic 已成功将其 AI 业务商业化。计划中的 IPO 可能是科技领域规模最大的之一，将成为衡量投资者对 AI 公司兴趣的关键指标。 这些为初步数据，仍可能调整。Anthropic 2026 年第一季营收为 47.3 亿美元，去年同期第二季营收为 7.87 亿美元。据报公司正筹备可能于今秋举行的大型 IPO。

telegram · zaihuapd · 8月16日 07:26

**背景**: Anthropic 是一家由前 OpenAI 研究人员创立的 AI 安全与研究公司，以其 Claude 系列大语言模型著称。该公司通过订阅计划和开发者 API 销售 AI 服务，与 OpenAI 和 Google 等竞争。此次营收暴增反映了企业界对生成式 AI 工具的旺盛需求。对于一家在算力和研发上大量投入的初创公司来说，实现调整后营业利润转正是一项重要里程碑。

**标签**: `#Anthropic`, `#Revenue`, `#IPO`, `#AI Industry`, `#Business News`

---

<a id="item-5"></a>
## [Firefox for iOS 新增原生广告拦截功能](https://support.mozilla.org/en-US/kb/block-ads-firefox-ios) ⭐️ 7.0/10

Mozilla 已在 Firefox for iOS 中推出原生广告拦截器，让 iPhone 和 iPad 用户无需安装单独的应用即可直接在浏览器中屏蔽广告。该功能增强了 Firefox 在苹果移动平台上的隐私工具。 由于所有 iOS 浏览器都必须使用 WebKit，Firefox 此前依赖 Firefox Focus 等单独应用或第三方内容拦截器来绕开限制。内置拦截器可改善隐私、提升页面加载速度并减少数据流量——对 Firefox 数百万移动用户来说是一次有意义的升级，也是行业向浏览器内置广告拦截转变的又一例证。 该拦截器使用 Apple 的 Safari 内容拦截 API，向基于 WebKit 的浏览器提供拦截规则列表。由于 App Store 的要求，Firefox for iOS 仍使用 WebKit 而非 Mozilla 的 Gecko 引擎；一些用户指出，其广告拦截效果可能不如桌面端 uBlock Origin 等完整扩展那样彻底。

hackernews · pentagrama · 8月16日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=49319633)

**背景**: iOS 浏览器必须使用 Apple 的 WebKit 引擎，因此 Firefox for iOS 在底层与 Safari 非常相似。内容拦截器是 Safari 应用扩展，通过规则屏蔽广告、跟踪器及其他内容。Mozilla 的隐私浏览器 Firefox Focus 自 2010 年代末起就通过该机制提供系统级广告拦截。Mozilla 还表示希望将自有 Gecko 引擎带到 iOS，但在当前平台规则下仍难以实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.apple.com/documentation/SafariServices/creating-a-content-blocker">Creating a content blocker | Apple Developer Documentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Firefox_for_iOS">Firefox - Wikipedia</a></li>
<li><a href="https://9to5mac.com/2023/02/14/mozilla-firefox-without-webkit-iphone/">Mozilla CEO teases iPhone browser without WebKit: ‘We’re always kind of working on it’ - 9to5Mac</a></li>

</ul>
</details>

**社区讨论**: 评论者指出 Firefox Focus 在 iOS 上早已提供系统级广告拦截，这次只是将功能整合进来更方便；还有用户推荐 Safari 的 uBlock Origin Lite 作为替代。一位用户发现 Firefox for iOS 的广告突然重新出现，询问其他人是否有同样情况；还有不少人期待 Mozilla 的 Gecko 引擎登上 iOS。总体反应积极，技术用户还讨论了历史与生态背景。

**标签**: `#Firefox`, `#iOS`, `#adblock`, `#privacy`, `#browser`

---

<a id="item-6"></a>
## [怪词“肾脏失望”暴露论文 AI 改写问题](https://scholar.google.com/scholar?q=%22kidney+disappointment%22) ⭐️ 7.0/10

越来越多研究论文中出现“肾脏失望”替代“肾衰竭”这类荒谬的“扭曲短语”，这些短语由用于规避抄袭检测的 AI 改写工具生成。这一现象已在多家知名期刊中出现，引发了对论文诚信的担忧。 这凸显了学术出版中日益严重的诚信危机：AI 文本改写工具让作者能掩盖抄袭内容，产生荒谬术语，甚至能通过同行评审。这动摇了人们对科学文献的信任，并迫使期刊采用更强的 AI 检测与筛查措施。 扭曲短语包括“counterfeit consciousness”代替“artificial intelligence”、“bosom peril”代替“breast cancer”等怪异替换，通常由回译或改写工具产生。2021 年一篇 arXiv 论文首次系统描述了该现象，2026 年 Retraction Watch 的报道指出，在更正和撤稿中仍能看到它们。

hackernews · Alifatisk · 8月16日 12:22 · [社区讨论](https://news.ycombinator.com/item?id=49319389)

**背景**: 扭曲短语是指文本经过 AI 改写工具或翻译软件处理后出现的生硬、无意义的词语替换，目的是规避抄袭检测。该术语由 2021 年一篇 arXiv 论文提出，此后在科学期刊文章中屡有发现。Quillbot、Scribbr 等工具被学生和写作者广泛使用来改写文本，但在学术场景中，它们可能产生难以阅读或误导性的语言。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tortured_phrase">Tortured phrase</a></li>
<li><a href="https://arxiv.org/abs/2107.06751">[2107.06751] Tortured phrases: A dubious writing style ...</a></li>
<li><a href="https://retractionwatch.com/2026/02/18/correction-retraction-tortured-phrases-llm-text-spinners/">Correction to a retraction highlights tortured phrases have ...</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了实例并就成因展开讨论：有人认为是 AI 改写所致，也有人认为是非英语母语者的翻译问题，并引用“水羊”（water goat）代替“液压锤”（hydraulic ram）等历史案例。一位评论者指出，“肾脏失望”早在 2021 年就已出现，当时现代大语言模型尚未普及，因此更可能源于翻译而非 AI 生成。

**标签**: `#AI`, `#academic publishing`, `#scientific integrity`, `#language models`, `#plagiarism`

---

<a id="item-7"></a>
## [达里奥·阿莫迪：公众对 AI 的不信任是信任危机，而非营销问题](https://simonwillison.net/2026/Aug/16/dario-amodei/) ⭐️ 7.0/10

Anthropic 首席执行官达里奥·阿莫迪表示，公众对 AI 的不信任源于对机构更广泛的信任危机，而非 AI 领袖的警告；真正能重建信任的是实际成就（如治愈癌症），而非营销。他直接否定了光鲜的营销活动，认为“AI 将治愈癌症”这种说法更多是陈词滥调而非鼓舞人心。 这一观点意义重大，因为它反驳了“AI 领袖的风险警告是公众反弹主因”的说法，并将责任转向 AI 公司需交付切实利益。作为 AI 领域领军人物，阿莫迪的看法可能影响 Anthropic 乃至整个行业应对公众疑虑的方式。 阿莫迪承认，对包括 Anthropic 在内的 AI 公司最准确的批评是尚未兑现造福世界的重大承诺。他明确否定了营销作为解决方案，称普通人不信任企业、政府和科技行业，源于数十年来感觉被欺骗的经历。

rss · Simon Willison · 8月16日 15:05

**背景**: 达里奥·阿莫迪是 Anthropic 公司的首席执行官，该公司开发了 Claude 大语言模型，他本人一直是 AI 风险的重要警示者。此番言论回应了“这类警告加剧公众对 AI 负面看法”的批评。他将不信任归因于公众对机构长期以来的怀疑，认为只有实际成就而非宣传话术才能重建公众信心。

**标签**: `#AI`, `#public trust`, `#anthropic`, `#dario amodei`, `#AI policy`

---

<a id="item-8"></a>
## [SSOG-Attention：可分离高斯和实现次二次注意力](https://www.reddit.com/r/MachineLearning/comments/1vpt6ay/ssogattention_sum_of_separable_gaussians_as_a/) ⭐️ 7.0/10

该帖子介绍了 SSOG-Attention，一种用可分离高斯和替代缩放点积注意力（SDPA）的新型注意力机制。它在 CIFAR-100 和 ImageNet 上实现了 O(N√N·d)的复杂度，并报告了与 SDPA 相当或更优的性能。 这解决了 Transformer 中的一个关键扩展瓶颈，即标准注意力的 O(N²·d)复杂度限制了序列长度。如果结果可靠，SSOG 可以为长上下文模型带来更高效的训练和推理。 该方法为每个注意力头学习少量高斯原子，并根据查询标记对其进行几何引导，从而可以分解为可分离求和。项目提供了开源仓库和博客文章，包含消融实验和收敛性对比。

reddit · r/MachineLearning · /u/4rtemi5 · 8月16日 10:06

**背景**: 标准的缩放点积注意力（SDPA）计算所有标记对之间的相似度分数，导致序列长度上的二次复杂度。为了克服这一瓶颈，研究者们探索了线性注意力、状态空间模型和稀疏注意力等次二次注意力机制。SSOG 是这一家族的新成员，利用高斯核高效地近似注意力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.lesswrong.com/posts/kpSXeMcthtHgnwMx3/debunking-claims-about-subquadratic-attention">Debunking claims about subquadratic attention</a></li>
<li><a href="https://www.mindstudio.ai/blog/what-is-sub-quadratic-sparse-attention-subq">What Is Sub-Quadratic Sparse Attention? How SubQ's 12M Token Context Works | MindStudio</a></li>

</ul>
</details>

**标签**: `#attention mechanisms`, `#efficient transformers`, `#machine learning`, `#sub-quadratic complexity`, `#gaussian kernels`

---