---
layout: default
title: "Horizon Summary: 2026-10-28 (ZH)"
date: 2026-10-28
lang: zh
---

> 从 44 条内容中筛选出 8 条重要资讯。

---

1. [谷歌发布 Gemini 4 Carbon，号称最强前沿模型](#item-1) ⭐️ 9.0/10
2. [水印脚本意外触发“生物武器”内容分类器](#item-2) ⭐️ 8.0/10
3. [Apple 系统自带 git 仍信任已被吊销的 eMudhra 证书](#item-3) ⭐️ 8.0/10
4. [EmbeddingGemma-2 借助零训练零空间 PCA 登顶 MAEB 音频基准](#item-4) ⭐️ 8.0/10
5. [谷歌据称发布 Gemini 4 Argon，具身推理得分达 87%](#item-5) ⭐️ 8.0/10
6. [苹果发布配备 PROLED XDR 触控屏和更轻设计的 MacBook Pro](#item-6) ⭐️ 7.0/10
7. [Surge AI 发布 Dayjob: Tax 基准测试：最佳 AI 智能体仅通过 10.8% 的真实税务任务](#item-7) ⭐️ 7.0/10
8. [Emacs 迎来 50 岁生日：Hacker News 热议这款常青编辑器](#item-8) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [谷歌发布 Gemini 4 Carbon，号称最强前沿模型](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/) ⭐️ 9.0/10

谷歌 DeepMind 发布了 Gemini 4 Carbon，称其是迄今为止最强的模型，在网络安全能力与长时程智能体（agentic）任务上达到业界最先进水平。该消息迅速成为 Hacker News 上讨论最热烈的 AI 话题之一，获得约 753 分和 613 条评论。 此次发布表明谷歌希望继续站在大模型研发的最前沿，并且把 Carbon 的定位明确放在安全与长时间自主智能体任务上，而非通用对话。但这一公告也暴露出生态中的新问题：面对谷歌不断增多的模型名称与层级，用户越来越难以判断自己究竟能用上哪一个。 谷歌把网络安全与长时程智能体能力作为 Carbon 的核心卖点，Artificial Analysis 等第三方评测机构已经开始对“Gemini 4 Carbon (high)”这一配置进行基准测试。值得注意的是，公告公布了基准成绩却没有给出明确的公开发布时间，评论区也有人反映该模型在 Gemini 手机应用中尚不可选，应用内最新仍只到 3.8 Pro。

hackernews · acossta · 10月28日 17:01 · [社区讨论](https://news.ycombinator.com/item?id=50276792)

**背景**: Gemini 是谷歌 DeepMind 的旗舰大语言模型系列，与竞争对手一样按层级发布（如 Ultra、Pro、Flash），在能力、成本与延迟之间做权衡。前沿实验室通常会在模型正式开放前公布基准分数——即针对推理、编程、数学与安全等维度的标准化评测——以展示技术进展。谷歌还使用过“Argon”之类的额外代号，这让外界更难分辨各个模型的区别以及各自何时面向公众开放。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/">Introducing Gemini 4 Carbon</a></li>
<li><a href="https://artificialanalysis.ai/models/gemini-4-carbon">Gemini 4 Carbon (high) - Intelligence, Performance... | Artificial Analysis</a></li>
<li><a href="https://theresanaiforthat.com/model/gemini-4-carbon/">Gemini 4 Carbon | AI Model | There's An AI For That</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对谷歌的命名与层级感到困惑：有人调侃说，即便给他 100 美元并明确指示，他也只有大约 30% 的把握弄清如何向“Gemini 4 Argon”发起提示，因为他的应用里仍显示 3.8 Pro，角落里还有一个看不出含义的“Ultra”标签。也有人认为，在如此快速的竞争环境里，只公布基准却不发布模型几乎没有意义；还有人建议像 SEMVER 那样，把层级标准化为简单的 Ultra/Pro/Flash/Lite 四档。

**标签**: `#Gemini`, `#Google AI`, `#LLM`, `#model release`, `#benchmarks`

---

<a id="item-2"></a>
## [水印脚本意外触发“生物武器”内容分类器](https://nullpt.rs/fingerprinting-bioweapons) ⭐️ 8.0/10

nullpt.rs 上的一篇文章调查了一个指纹识别/水印脚本为何会让自动分类器把网页判定为与生物武器相关的内容。作者将这一误报追溯到脚本注入的混淆文本本身，使一个常规的反爬虫手段演变成了内容审核事件。 这一事件表明，反 LLM 抓取与水印手段可能与安全分类器发生冲突，导致正常页面被隔离、封禁或误分类。随着越来越多网站对爬虫部署对抗性混淆，此类误报很可能波及内容发布方、邮件网关以及所有依赖自动化内容过滤的系统。 触发原因似乎是水印脚本故意插入的怪异混淆字符串，其目的是让被抓取的副本仍可被追踪，而这些文本会被基于关键词或分类器的安全过滤器读作可疑内容。社区中的轶事表明，同样的机制会让企业邮件系统把带水印的文档投入无限期隔离。

hackernews · hazebooth · 10月28日 17:13 · [社区讨论](https://news.ycombinator.com/item?id=50276998)

**背景**: 这里的指纹识别与水印指的是向内容中嵌入隐藏且通常唯一的标记，以便追踪其来源或副本；在网络上，网站还会使用混淆的 JavaScript 和类似蜜罐的手段来识别或阻止自动化爬虫，包括 LLM 抓取器。自动化安全分类器会扫描文本是否属于大规模杀伤性武器等类别，它们依据的是表层模式而非真实意图，因此异常的混淆字符串看起来很可疑。网站指纹识别是一个相关但不同的研究领域，指从流量模式推断用户访问了哪些页面，其防御手段同样依赖对抗性扰动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2504.06575">[2504.06575] Defending LLM Watermarking Against Spoofing ... Defending LLM Watermarking Against Spoofing Attacks with ... Defending LLM Watermarking Against Spoofing Attacks with... CMU CSD PhD Blog - No Free Lunch in LLM Watermarking Machine never said that: Defending spoofing attacks by ... Securing Large Language Models: A Survey of Watermarking and ... From Intentions to Techniques: A Comprehensive Taxonomy and ...</a></li>
<li><a href="https://dl.acm.org/doi/10.1145/3243734.3278493">Adversarial Traces for Website Fingerprinting Defense</a></li>
<li><a href="https://github.com/WF-Attack-and-Defense/Awesome-WF-Security">Awesome Website Fingerprinting Attack and Defense Studies</a></li>

</ul>
</details>

**社区讨论**: 评论者很欣赏这次“侦探式”排查，并分享了自己的经历：有人提到忘记移除的禁运水印导致客户邮件系统将文档无限期隔离，还有人指出某个 HN 用户资料里藏有反 LLM 的“咒语”。整体氛围既对这种荒诞感到好笑，也认为混淆方与 LLM 爬虫之间正演变成一场分形般的军备竞赛，此外还有关于“关键词让人看起来像恐怖分子”的编程语言的玩笑。

**标签**: `#fingerprinting`, `#anti-LLM`, `#web-scraping`, `#obfuscation`, `#security`

---

<a id="item-3"></a>
## [Apple 系统自带 git 仍信任已被吊销的 eMudhra 证书](https://emudhra.we-have-a-problem.com/apple.html) ⭐️ 8.0/10

emudhra.we-have-a-problem.com 上的一份报告指出，Apple 系统自带的 git 以及其他 macOS 工具仍然信任那些私钥已被泄露的 eMudhra 中间 CA 证书，即便 eMudhra 已经吊销了它们。Apple 给出的唯一方案是用户自行执行的手动缓解措施（支持文档 149555），而该文章指出这种修改可能在后续 macOS 更新中被悄悄还原。 任何在 macOS 上使用 Apple 自带 git 的开发者，都可能在使用 HTTPS 克隆等 TLS 连接时面临中间人攻击风险，而且该漏洞可能在系统更新后悄然重现。这一事件也凸显出各操作系统的证书信任存储依然割裂，即便是在一家以安全为卖点的公司身上也是如此。 问题的根源在于 macOS 中部分工具依赖 OpenSSL/LibreSSL 风格的信任包（例如 /etc/ssl/cert.pem），而不是基于钥匙串的信任存储，因此从系统根证书列表中移除某个 CA 并不会影响它们。通过 Homebrew 安装 git 的用户可能不受影响，但这取决于其构建版本如何解析信任锚，应当实际验证而不能想当然。

hackernews · galadran · 10月28日 11:03 · [社区讨论](https://news.ycombinator.com/item?id=50271640)

**背景**: 证书颁发机构（CA）签发支撑 TLS 的数字证书，中间 CA 位于受信任的根证书与其签发的终端实体证书之间。一旦中间 CA 的私钥泄露，攻击者就能为任意域名伪造看似合法的证书，这正是此类 CA 会被吊销并在浏览器和操作系统中被标记为不信任的原因。印度 CA 机构 eMudhra 有八个中间 CA 的私钥被泄露并已将其吊销，但信任移除必须同步到应用程序使用的每一个信任存储，而 macOS 恰好有多个。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openjdk.org/emudhra">Compromised Certificates and OpenJDK Java Runtimes</a></li>
<li><a href="https://blog.talosintelligence.com/compromised-intermediate-certificates/">Compromised eMudhra intermediate certificates</a></li>
<li><a href="https://unit42.paloaltonetworks.com/emudhra-certificate-compromise/">EMudhra Intermediate CA Certificates Compromised</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者强调，问题远不止 git，因为许多 macOS 工具都会继承操作系统的信任存储；他们认为 Apple 这种手动、且会被系统更新还原的修复方式令人难以接受。不少人贴出 Apple 自己的支持文档 149555，并呼吁每位 Mac 开发者都去执行该补丁；还有一位评论者在没有证据的情况下猜测，这种弱密钥生成可能是蓄意为之。

**标签**: `#security`, `#macOS`, `#certificates`, `#git`, `#supply-chain`

---

<a id="item-4"></a>
## [EmbeddingGemma-2 借助零训练零空间 PCA 登顶 MAEB 音频基准](https://www.reddit.com/r/MachineLearning/comments/1xho7pr/r_taking_embeddinggemma2_577m_from_rank_26_to_1/) ⭐️ 8.0/10

Reddit 用户 JeanMichelRanu 的一项实验在完全不训练的情况下，把 google/embeddinggemma-2（577M）在 MAEB 上的宏平均分数从 49.3% 提升到 54.4%（+5.1 分）：做法是用 PCA 压缩第 2 层和第 6 层 Conformer 层的激活，再注入模型最终 768x512 投影矩阵的 256 维零空间中。该模型因此在 MAEB 纯音频榜从第 26 名升至第 1 名，在完整 MAEB 榜从第 16 名升至第 1 名，超过 8B–9B 的多模态模型，权重已发布为 BrunoHays/embeddinggemma-2-nullspace-audio。 这说明那些经过深度文本对齐的大型音频编码器，其中间层仍保留着大量未被利用的副语言信息——说话人、情感、音色——而最终对齐过程把这些信息丢掉了，并且这些信号可以在事后无需微调地回收。对嵌入模型从业者而言，这提示了一条无需训练即可专用化基础嵌入模型的低成本路径，也让人重新思考榜单提升是否必须以重训练为代价。 由于最终投影 W 是无非线性的 512 维到 768 维线性映射，文本向量始终只落在 512 维子空间中，剩下 256 个正交方向（即 W 的 SVD 给出的零空间）与所有文本嵌入严格正交，因此文本输出逐位不变，文本到音频检索的变化在 0.05 分以内。代价是音频分支必须使用全部 768 维（失去 512/256/128 的 Matryoshka 截断选项），而且注入的声学特征会在归一化后稀释语义成分，使 SIBFLEURS 口语主题分类从 57.2% 跌至 21.3%，MInDS14 口语意图从 97.6% 跌至 88.3%。

reddit · r/MachineLearning · /u/JeanMichelRanu · 10月28日 13:34

**背景**: EmbeddingGemma-2 是谷歌的开放嵌入模型，可原生把文本、图像、音频和视频映射进同一嵌入空间，并支持 Matryoshka 表示学习，即可从原生 768 维截断为 128、256 或 512 维。MAEB 是 MTEB 榜单上的音频基准，涵盖约 30 个任务，横跨检索、分类、聚类与重排序，且同时包含纯音频和音频-文本场景。Conformer 是谷歌提出的语音架构，把 CNN 模块与 Transformer 自注意力结合，兼顾音频序列的局部与全局结构。此前的逐层探针研究（如 Pasad 等）表明，说话人、韵律和语义属性在语音编码器的不同深度达到峰值，本实验正是利用了这一点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/google/embeddinggemma-2">google/ embeddinggemma - 2 · Hugging Face</a></li>
<li><a href="https://leaderboard.mteb.org/benchmark/MAEB(beta)">MAEB · MTEB Leaderboard</a></li>
<li><a href="https://arxiv.org/abs/2005.08100">[2005.08100] Conformer: Convolution-augmented Transformer for ... Conformer Architecture - emergentmind.com Conformer ASR Architecture - apxml.com Conformer: Convolution-augmented Transformer for Speech ... Conformer: Convolution-augmented Transformer for Speech ... Conformer: Convolution-augmented Transformer for Speech ...</a></li>

</ul>
</details>

**标签**: `#embedding-models`, `#audio-benchmarks`, `#PCA`, `#null-space`, `#representation-learning`

---

<a id="item-5"></a>
## [谷歌据称发布 Gemini 4 Argon，具身推理得分达 87%](https://t.me/zaihuapd/44764) ⭐️ 8.0/10

据报道，谷歌发布了新一代多模态推理模型 Gemini 4 Argon，在物理理解、代码生成与视觉语义推理方面均有增强。据称它在具身推理基准 ERQA 上仅凭纯推理就取得 87% 的得分，领先其他前沿模型，并且已通过 google-genai SDK 提供，输入价格为每百万 token 2 美元。 如果消息属实，这将标志着谷歌在具身推理与物理世界理解方面迈出重要一步，而这一能力正被各家前沿实验室视为连接多模态模型与真实机器人的关键桥梁。优异的 ERQA 成绩以及据称在真实机器人任务上的提升，将使 Gemini 直接加入瞄准机器人与具身智能市场的前沿模型竞争。 据称的机器人实测结果包括操控波士顿动力 Spot 四足机器人完成取物、投掷等任务，并能生成仿真数据，将真实机器人成功率从 56% 提升至 75%，同时把任务用时从 35 秒缩短至 24 秒。不过该消息仅来自一条 Telegram 帖子，没有附带可验证的来源，且原文中输出 token 的价格信息被截断。

telegram · zaihuapd · 10月28日 17:09

**背景**: ERQA（Embodied Reasoning Question Answer，具身推理问答）是一个约含 400 道多项选择视觉题的基准，用于测试模型能否对物理世界进行推理，包括从图像中推断空间布局、运动轨迹、动作以及物体状态。具身推理指的是智能体运用语言规划、空间推理与物理常识来感知并在环境中行动的能力，也是机器人在真实空间中执行指令的核心能力。波士顿动力的 Spot 是一款商用四足机器人，广泛用于现场巡检与工业监测，也常被用作机器人学习研究的测试平台。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/embodiedreasoning/ERQA">GitHub - embodiedreasoning/ ERQA : Embodied Reasoning Question...</a></li>
<li><a href="https://llm-stats.com/benchmarks/erqa">ERQA Leaderboard | LLM Stats</a></li>
<li><a href="https://bostondynamics.com/products/spot/">Spot | Boston Dynamics</a></li>

</ul>
</details>

**标签**: `#Gemini`, `#Google`, `#multimodal AI`, `#robotics`, `#embodied AI`

---

<a id="item-6"></a>
## [苹果发布配备 PROLED XDR 触控屏和更轻设计的 MacBook Pro](https://www.apple.com/macbook-pro/proled-xdr-display/) ⭐️ 7.0/10

苹果发布了新一代 MacBook Pro，首次在 Mac 产品线上引入触控屏，并搭载名为 PROLED XDR 的串联 OLED 显示屏。14 英寸和 16 英寸机型分别减重至 3.0 磅（1.36 公斤）和 4.0 磅（1.81 公斤），约轻 15%，机身也薄了将近 1 毫米。 这是苹果长期以来坚持不为 Mac 加入触控之后的一次重大转向，可能迫使 macOS 开发者和第三方应用重新考虑界面尺寸与手势支持。更轻的 OLED 设计也增强了 MacBook Pro 在移动专业工作流中的吸引力，尤其是在面对支持触控的 Windows 笔记本竞争时。 苹果称 PROLED XDR 显示屏可实现最高 1000 尼特全屏持续亮度、2000 尼特 HDR 和 SDR 峰值亮度，以及得益于逐像素 OLED 黑色表现的 10,000,000:1 对比度。触控支持手势和部分应用，但苹果将其定位为补充输入方式，而非取代键盘和触控板。

hackernews · etothet · 10月28日 17:10 · [社区讨论](https://news.ycombinator.com/item?id=50276940)

**背景**: PROLED XDR 是苹果为 MacBook Pro 新款串联 OLED 显示屏使用的品牌名称。OLED 面板每个像素自发光，不需要独立背光，因此能实现更深的黑色、更高对比度以及更薄更轻的屏幕；串联 OLED 则通过堆叠两层发光层来提升亮度和寿命。触控 Mac 多年来一直有传闻和用户需求，但苹果此前把触控留给 iPhone 和 iPad，并认为 macOS 是为触控板和鼠标这类间接输入设计的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.apple.com/macbook-pro/proled-xdr-display/pdf/PROLED_XDR_Display_Technical_Paper.pdf">PROLED XDR DISPLAY Technology Overview - Apple</a></li>
<li><a href="https://www.macobserver.com/news/macbook-pro-touch-macos-27/">How the touchscreen MacBook Pro works: gestures, apps and ...</a></li>
<li><a href="https://www.dpreview.com/news/the-macbook-pro-finally-gets-a-touchscreen/">Apple has finally added a touchscreen to the MacBook Pro</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论意见不一：有人主张给 macOS 加入触控会带来无法回避的界面问题，因为 Mac 的控件对手指来说太小；也有人对约 15%的减重和更薄 OLED 设计背后的工程实现表示赞赏。还有不少用户质疑触控在笔记本上是否真的实用、不喜欢屏幕上沾指纹，一位批评者则认为这次发布显示苹果在设计上投入的用心在减少。

**标签**: `#Apple`, `#MacBook Pro`, `#hardware`, `#touchscreen`, `#display technology`

---

<a id="item-7"></a>
## [Surge AI 发布 Dayjob: Tax 基准测试：最佳 AI 智能体仅通过 10.8% 的真实税务任务](https://surgehq.ai/blog/dayjob-tax) ⭐️ 7.0/10

Surge AI 发布了 DAYJOB: Tax 基准测试，包含 50 个专业税务任务，由 1,789 份贴近真实的客户文件构成，覆盖税务实践的八个领域，并按 95% 的严格评分标准判定通过与否。表现最好的 Claude Sonnet 5.5 也仅通过了 10.8% 的任务，领先于 GPT-6 Astra 的 4.8% 和 Gemini 4 Argon 的 3.2%。 税务申报是一个高风险且结果可验证的领域，错误会直接转化为金钱损失或合规风险，因此一个显示近乎全面失败的基准测试，为“智能体 AI 距离取代专业判断还有多远”设定了现实的标尺。它同时也向企业和工具开发者传递了一个明确信号：当前的瓶颈在于模型本身的能力，而不仅仅是文档处理。 这些任务在设计上刻意不在初始指令中完整说明关键决策，要求智能体自行推断客户的真实需求，并且评分采用 95% 的严格阈值，而非部分给分。DAYJOB: Tax 是 Surge 的 DAYJOB 系列第三个发布，此前已有医疗健康和金融两个基准。

hackernews · landonxi · 10月28日 15:46 · [社区讨论](https://news.ycombinator.com/item?id=50275626)

**背景**: AI 智能体是由大模型驱动的系统，能够读取文件、调用工具并围绕目标执行多步操作，而基准测试是研究者比较它们在真实工作中表现的方式。Surge AI 是一家提供人工标注训练与评测数据的数据与评估公司，因此其基准测试同时也是对自身任务设计能力的展示。税务申报之所以适合用于评测，是因为正确答案可以依据 IRS 表格、工作表和申报规则进行客观核验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://surgehq.ai/blog/dayjob-tax">DAYJOB: Tax — Benchmarking AI Agents on Professional Tax Work</a></li>
<li><a href="https://explainx.ai/blog/surge-ai-dayjob-tax-benchmark-50-tax-assignments-sonnet-5-5-10-8-percent-hn-2026">Dayjob: Tax Benchmark: Best AI Agent Passes 10.8% - explainx.ai</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者基本认为这些低分是可信的：有实践者称大模型确实能在跨境申报中发现真实错误，例如用错汇率，但也指出会计师本身会引入错误，导致退税额少了近 2000 美元。一个反复出现的批评针对方法论：有评论者认为该基准只是把文档丢给基础模型、几乎不提供工程化支撑，因此衡量的并非在良好搭建的运行框架下模型能做到什么。还有人分享了一个将 IRS 表格与工作表形式化为开放模型的社区项目，目前大约覆盖 60% 的美国联邦税务情形，有望成为已停办的 IRS Direct File 的替代方案。

**标签**: `#ai-agents`, `#benchmarking`, `#tax-software`, `#llm-evaluation`, `#hacker-news-discussion`

---

<a id="item-8"></a>
## [Emacs 迎来 50 岁生日：Hacker News 热议这款常青编辑器](https://www.technologyreview.com/2026/10/20/1145399/emacs-turns-50/) ⭐️ 7.0/10

一个纪念 Emacs 诞生 50 周年的 Hacker News 帖子获得了 391 分和 165 条评论，许多老用户分享了自己维护了三十年甚至更久的配置。讨论重点呈现了这款编辑器如何吸收 Evil 模式（模态编辑）、LSP 支持以及 AI 辅助工作流等较新的开发趋势。 Emacs 是软件史上最具影响力、生命周期最长的作品之一，因此半个世纪的持续使用对开源软件而言是一个重要的文化里程碑。它的存续也提供了一个范例：可扩展的架构如何让一款几十年前的工具，在 VS Code 和各类基于 Electron 的编辑器起落更替之中依然保持生命力。 评论者举出了这种适应能力的具体例子，包括把 Vim 风格模态编辑引入 Emacs 的 Evil 模式、作为日常工具的 Magit Git 界面和 ghostel 终端模拟器，以及较新的 vterm 和 eat 等终端方案。值得注意的是，该帖是一次社区回顾而非版本发布公告——这个周年纪念并没有伴随新版本或技术突破。

hackernews · internet_points · 10月28日 13:25 · [社区讨论](https://news.ycombinator.com/item?id=50273171)

**背景**: Emacs 是一款高度可扩展、自带文档的文本编辑器，其开发始于 1970 年代中期的麻省理工学院，主要作者是 Richard Stallman；今天的 GNU Emacs 使用 Emacs Lisp 进行脚本编写和配置，用户可以重塑编辑器的几乎每个部分。正是这种可扩展性，让人们半开玩笑地称它为“附带了一个文本编辑器的操作系统”，也让 org-mode（用于记笔记和日程规划）与 Magit（用于 Git）这类工具能在其中存在。Evil 模式是一个模拟 Vim 模态编辑键位的扩展包，而 LSP（语言服务器协议）则是微软提出的标准，让编辑器可以通过共享的语言服务器获得代码智能能力，Emacs 通过 Eglot 等包支持它。围绕周年纪念的讨论，正是聚焦于这些插件如何让一款 1970 年代的设计跟上现代工具链。

**社区讨论**: 整体情绪是怀旧而自豪的：一位用了三十多年的用户说其他编辑器来来去去，Emacs 却留了下来；另一位则称它比任何被推销为“未来编辑器”的东西都更现代，认为 Evil 模式让 Vim 变得更好、LSP 让它更强，而 vterm、eat、ghostel 等现代终端方案则回应了基于 Electron 的竞争者。还有人讲述了用 Emacs 写论文、收发邮件、写博客、记录时间乃至见证职业里程碑的经历；不过也有反对声音，一位评论者询问是否有人刻意保持极简配置，表示插件的复杂度和 org-mode“什么都能做所以什么都该用它做”的诱惑最终把其推向了 sam、Acme 这类更简单的 Plan 9 工具。

**标签**: `#emacs`, `#text-editors`, `#open-source`, `#developer-tools`, `#software-history`

---