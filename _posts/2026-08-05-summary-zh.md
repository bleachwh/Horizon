---
layout: default
title: "Horizon Summary: 2026-08-05 (ZH)"
date: 2026-08-05
lang: zh
---

> 从 34 条内容中筛选出 8 条重要资讯。

---

1. [谷歌 DeepMind 重组：哈萨比斯转任主席，杰夫·迪恩离职](#item-1) ⭐️ 9.0/10
2. [ChainDrop 蠕虫攻陷 npm 逾 1300 个包](#item-2) ⭐️ 9.0/10
3. [FFmpeg 9.0 发布：新增动画 WebP、Vulkan 滤镜与 ONNX Runtime 后端](#item-3) ⭐️ 9.0/10
4. [Discovery Loop 旨在自动化机器学习研究的实验循环](#item-4) ⭐️ 8.0/10
5. [Cloudflare OS：面向代理、应用和工作的开放平台](#item-5) ⭐️ 8.0/10
6. [DeepMind 立场论文：LLM 无法实现科学发现飞跃](#item-6) ⭐️ 8.0/10
7. [新墨西哥州民用飞机坠毁疑与军用 GPS 干扰相关](#item-7) ⭐️ 8.0/10
8. [LLM 0.32 新增推理踪迹、OpenAI Responses 与服务端工具](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [谷歌 DeepMind 重组：哈萨比斯转任主席，杰夫·迪恩离职](https://blog.google/company-news/inside-google/message-ceo/next-chapter-ai-momentum/) ⭐️ 9.0/10

2026 年 8 月 5 日，谷歌宣布了 DeepMind 的重大领导层变动：首席执行官戴密斯·哈萨比斯将转任主席，而杰夫·迪恩和桑杰·格马沃特在任职 27 年后离职。迪恩和格马沃特将联合奥里奥尔·比尼亚尔斯和郭克雷共同创立一家新的公益公司 Discovery Loop。 这标志着谷歌 DeepMind 黄金时代的结束，也凸显了谷歌 AI 部门更广泛的人才外流，可能削弱其相对于竞争对手的竞争地位。Discovery Loop 旨在加速人工智能在科学和工程领域的发现，这可能重塑 AI 初创企业的格局。 Discovery Loop 由杰夫·迪恩、桑杰·格马沃特、奥里奥尔·比尼亚尔斯和郭克雷共同创立，首轮融资由 Radical Ventures 和 Khosla Ventures 联合领投。值得注意的是，Alphabet 参与了本轮融资，而消息公布后谷歌股价下跌了 5%。

hackernews · colesantiago · 8月5日 16:05 · [社区讨论](https://news.ycombinator.com/item?id=49184755)

**背景**: 戴密斯·哈萨比斯是 DeepMind 的联合创始人，谷歌于 2014 年收购了该公司，他领导团队取得了 AlphaGo 和 AlphaFold 等突破。杰夫·迪恩是传奇的谷歌工程师，共同创建了 MapReduce、Bigtable 和 TensorFlow 等基础技术，并担任谷歌首席科学家。Discovery Loop 是一家公益公司，专注于自动化机器学习、科学和工程，建立在创始人的深厚技术专长之上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://x.com/JeffDean/status/2085034604172603724">Announcing Discovery Loop! I am very excited to announce that, along ...</a></li>
<li><a href="https://techcrunch.com/2026/08/05/jeff-dean-and-other-top-ai-researchers-are-leaving-google-to-launch-their-own-startup/">Jeff Dean and other top AI researchers are leaving Google to ...</a></li>
<li><a href="https://www.wired.com/story/jeff-dean-google-discovery-loop-startup/">Google’s Top AI Brains Are Leaving to Launch Discovery Loop ...</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体上是震惊和担忧，多位评论者称这些离职是“黄金时代的终结”。一些人指出，更大新闻是杰夫·迪恩和桑杰·格马沃特的离开，而非戴密斯·哈萨比斯的角色变动；另一些人则指出，谷歌正经历知名 AI 研究人员大规模外流且缺乏同等重量级人才补充，表明公司环境存在问题。谷歌股价下跌 5%也被引证为创始人对公司具有重大价值的体现。

**标签**: `#Google DeepMind`, `#AI leadership`, `#Jeff Dean`, `#Demis Hassabis`, `#talent exodus`

---

<a id="item-2"></a>
## [ChainDrop 蠕虫攻陷 npm 逾 1300 个包](https://www.bleepingcomputer.com/news/security/massive-chaindrop-npm-supply-chain-attack-infects-hundreds-of-packages/) ⭐️ 9.0/10

自我传播的 ChainDrop 蠕虫已感染超过 1300 个 npm 包，包括 Keyv、Cacheable 等热门缓存库，合计月下载量达 20 亿次。攻击始于黑客攻破 Keyv 维护者的 GitHub 账号，并通过自动化的 GitHub Actions 发布看似正常的版本进行扩散。 这是一次至关重要的供应链攻击，因为它破坏了广泛使用的开源组件，使得攻击者能够窃取凭证并进一步渗透到众多企业的下游项目中。这凸显了自动化构建流水线和维护者账号可能被利用来大规模分发恶意软件。 被投毒的包内包含 setup.mjs 投放器和 Math_Symbol.js 窃密脚本，在 npm install 时自动执行，窃取 GitHub、npm、AWS、Kubernetes 等凭证。恶意版本通过合法的 GitHub Actions 工作流发布，带有有效来源证明；域名 npm-cache[.]com 可作为失陷指标，管理员应将受影响系统视为已被完全攻破，并轮换所有令牌。

telegram · zaihuapd · 8月5日 03:04

**背景**: npm 是 JavaScript 生态系统的包管理器，托管着数百万个开发者构建应用所依赖的包。针对 npm 的供应链攻击通常涉及攻破维护者账号或劫持热门包，注入恶意代码，使其他开发者安装或构建时自动执行。此次 ChainDrop 事件发生在 2025 年 9 月和 11 月的 Shai-Hulud 蠕虫攻击之后，表明 npm 仓库中的自我传播蠕虫依然是一个持续且不断增长的威胁。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.microsoft.com/en-us/security/blog/2026/08/04/chaindrop-supply-chain-compromise-anatomy-self-propagating-worm/">ChainDrop supply chain compromise: Anatomy of a self-propagating worm | Microsoft Security Blog</a></li>
<li><a href="https://www.stepsecurity.io/blog/chaindrop-npm-worm">ChainDrop npm Worm: Bun-loaded CI/CD credential harvester with Ethereum dead-drop C2 - StepSecurity</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/massive-chaindrop-npm-supply-chain-attack-infects-hundreds-of-packages/">Massive ChainDrop npm supply-chain attack infects hundreds of packages</a></li>

</ul>
</details>

**标签**: `#security`, `#npm`, `#supply-chain`, `#malware`, `#credential-theft`

---

<a id="item-3"></a>
## [FFmpeg 9.0 发布：新增动画 WebP、Vulkan 滤镜与 ONNX Runtime 后端](https://news.ycombinator.com/item?id=49166202) ⭐️ 9.0/10

FFmpeg 9.0 正式发布，新增动画 WebP 解码器与分离器、v360_vulkan GPU 滤镜、Playdate 视频编码器与封装器、支持 DAB+ 的 HE-AAC 960 解码、transpose_cuda 滤镜、AMF 帧率转换器滤镜，以及 ONNX Runtime DNN 后端。开发团队还通过 Anthropic 的开源计划使用 Claude AI 协助查找缺失的向后移植。 这一大版本发布扩展了 FFmpeg 的 GPU 加速与 AI 推理能力，使高级视频处理更加普及。在向后移植中使用 AI 也标志着开源项目可以利用生成式模型来加速维护工作的转变。 值得注意的新增内容包括：v360_vulkan 滤镜可在 GPU 上处理 360 度投影；Playdate 视频编码器；以及为 dnn_processing 滤镜新增的 ONNX Runtime 后端，支持硬件加速的神经网络推理。该版本还包含用于 DAB+ 广播的 HE-AAC 960 解码和支持 AMD GPU 的 AMF 帧率转换器滤镜。

telegram · zaihuapd · 8月5日 10:32

**背景**: FFmpeg 是一个广泛使用的开源多媒体框架，用于处理视频、音频等数据流。其基于 Vulkan 的滤镜通过 GPU 计算着色器运行，可为 VR 和沉浸式媒体工作流带来显著性能提升。ONNX Runtime 是一个跨平台的推理加速器，支持 PyTorch、TensorFlow 等框架的模型；将其作为 DNN 后端后，FFmpeg 可以在 CPU、GPU 和 NPU 上运行神经网络。Playdate 是 Panic 推出的带摇杆的掌上游戏机，其视频格式 .pdv 可通过 Playorama 等工具生成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sourcefeed.dev/a/ffmpeg-90-bets-the-gpu-stack-on-vulkan">FFmpeg 9.0 Bets the GPU Stack on Vulkan — SourceFeed</a></li>
<li><a href="https://github.com/microsoft/onnxruntime">GitHub - microsoft/onnxruntime: ONNX Runtime: cross-platform ... Intel - oneDNN | onnxruntime AMD Contributes ONNX Runtime Backend To FFmpeg DNN Filter ONNX Runtime | Home onnx/docs/ImplementingAnOnnxBackend.md at main · onnx/onnx nn.backends.onnx API Reference | Ultralytics</a></li>
<li><a href="https://www.playorama.app/encoder/">PDV Playdate Video Encoder- Playorama - HTeuMeuLeu</a></li>

</ul>
</details>

**标签**: `#FFmpeg`, `#multimedia`, `#video processing`, `#release`, `#AI-assisted development`

---

<a id="item-4"></a>
## [Discovery Loop 旨在自动化机器学习研究的实验循环](https://www.discoveryloop.com/) ⭐️ 8.0/10

Discovery Loop 是一个新项目，提出自动化科学和工程领域的实验循环，最初聚焦于机器学习研究和工程。其目标是结合机器学习专业知识和大型系统来加速实验。 自动化实验可以通过在更短时间内测试更多假设来大幅加速机器学习研究。这也顺应了 AI 驱动科学发现的更广泛趋势，可能影响机器学习以外的领域，例如美国国家工程院（NAE）的十四项重大挑战问题。 该项目强调要做好这件事，需要在机器学习和大型系统方面都具备深厚的专业知识。尽管最初聚焦于 ML 研究和工程，Discovery Loop 相信该方法有助于解决 NAE 十四项重大挑战问题中几乎所有重要的子问题。

hackernews · xtreak29 · 8月5日 16:19 · [社区讨论](https://news.ycombinator.com/item?id=49184960)

**背景**: 传统科学实验需要人工形成假设、设计实验、收集数据并解读结果，这是一个缓慢且劳动密集的过程。近年来大语言模型和 AI 智能体的进展催生了像 Karpathy 的 AutoResearch 这样的努力，探索 LLM 如何直接参与实验循环。Discovery Loop 似乎是这一想法的机构级、大规模版本，提议在多个领域自动化实验循环。这一方法顺应了 AI 驱动研究自动化工具日益增长的趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mljar.com/blog/autoresearch-karpathy-autonomous-ai-research/">AutoResearch by Karpathy and the Future of Autonomous AI Research</a></li>
<li><a href="https://dl.acm.org/doi/full/10.1145/3802133.3802134">Autonomous Research Loops: An LLM-Agent Framework for End-to ...</a></li>

</ul>
</details>

**社区讨论**: 评论者将 Discovery Loop 与 Karpathy 的 AutoResearch 进行比较，指出它类似于大规模机构化的版本，还有人提到 Karpathy 关于异步、大规模协作智能体的想法。一些人对如何自动化物理实验表示怀疑，认为现实世界的实验需要具身性，另一些人则嘲讽其使命陈述充满术语且晦涩难懂。

**标签**: `#AI research`, `#automation`, `#machine learning`, `#research tools`, `#experimentation`

---

<a id="item-5"></a>
## [Cloudflare OS：面向代理、应用和工作的开放平台](https://blog.cloudflare.com/cloudflare-os/) ⭐️ 8.0/10

Cloudflare 发布了 Cloudflare OS，这是一个开源平台，为每个人提供围绕公司上下文、工具和规则构建的代理（agent）和工作空间。它基于 Cloudflare Workers 构建并深度利用 AI，被描述为使用 Workers 和 AI 重制的 Sandstorm.io。 这是 Cloudflare 将边缘计算平台与 AI 代理趋势相结合的重大战略举措，可能开创企业级“AI 操作系统”的新品类。它可能改变公司部署代理工作流的方式，但也引发了对供应商锁定以及“OS”一词含义的担忧。 Cloudflare OS 是开源的，旨在围绕公司自身的上下文、工具和规则进行定制。该平台基于 Cloudflare Workers 构建，允许开发者在 330 多个城市的边缘运行代码；Cloudflare 工程师 Kenton Varda 指出，这是他十年前创业项目 Sandstorm.io 的重制版。

hackernews · speckx · 8月5日 13:58 · [社区讨论](https://news.ycombinator.com/item?id=49182996)

**背景**: Cloudflare 是一家重要的互联网基础设施公司，以 CDN、安全和边缘计算服务闻名；其 Workers 平台提供边缘无服务器执行能力。近年来，Cloudflare 将 AI 集成到其基础设施中，如今正积极进入新兴的 AI 代理市场——即能够使用工具并采取行动以实现目标的软件。“AI 操作系统”的概念仍然很新，Cloudflare OS 是首批将代理、应用和工作整合到单一开放平台的尝试之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/cloudflare-os/">Cloudflare OS : an open platform for agents, apps, and work</a></li>
<li><a href="https://os.cloudflare.app/">Cloudflare OS</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cloudflare,_Inc.">Cloudflare, Inc.</a></li>

</ul>
</details>

**社区讨论**: 社区反应褒贬不一：有人对这一概念感到兴奋，将其与 Smalltalk 或 Lisp 环境相类比；也有人担心供应商锁定，并批评在名称中使用“OS”。有评论者引用了 Kenton Varda 的推文，指出 Cloudflare OS 实际上是他早年创业项目 Sandstorm.io 的现代重制版，这为公告增加了背景。总体而言，既有人对 AI 集成平台表示热情，也有人对 Cloudflare 的命名和生态系统锁定持怀疑态度。

**标签**: `#Cloudflare`, `#platform`, `#AI`, `#agents`, `#Workers`

---

<a id="item-6"></a>
## [DeepMind 立场论文：LLM 无法实现科学发现飞跃](https://openreview.net/challenge?redirect=%2Fforum%3Fid%3DklU4737opt) ⭐️ 8.0/10

DeepMind 的 Tom Zahavy 发表立场论文《LLMs Can't Jump》，认为大语言模型在做出根本性科学发现所需的直觉跳跃方面存在固有局限。该论文在 OpenReview 上引发广泛讨论，获得 149 条评论和 216 个评分点。 这一论点之所以重要，是因为它质疑了“扩大 LLM 规模将加速科学突破”的主流乐观看法。它还引发了关于“语言本身是否是一种有损的经验编码”的深入讨论，这对 AI 推理的边界具有深远影响。 这篇立场论文由 DeepMind 的 Tom Zahavy 撰写，在 OpenReview 上获得 8.0/10 的评分。值得注意的是，作者后来在 Twitter 上澄清，论文并不认为 LLM 永远不会做出真正的科学发现，以此反驳一些将其解读为“DeepMind 对 AI 科学泼冷水”的说法。

hackernews · theanonymousone · 8月5日 11:01 · [社区讨论](https://news.ycombinator.com/item?id=49181083)

**背景**: 像 GPT-4 这样的 LLM 在海量文本上训练，擅长模式匹配，但它们能否完成定义科学突破的“直觉飞跃”仍是一个开放问题。论文标题引用了“计算机能在国际象棋上击败人类，但在跆拳道上却打不过人类”的名言，用以说明狭窄任务能力与通用智能之间的区别。

**社区讨论**: 评论者提出了多种观点：有人认为语言本质上是对人类经验的一种有损编码，还有人指出爱因斯坦工作的通俗叙述过于简化。作者本人也参与讨论，澄清论文被一些人误读为“LLM 永远不能为科学做贡献”。

**标签**: `#LLM`, `#AI research`, `#scientific discovery`, `#position paper`, `#DeepMind`

---

<a id="item-7"></a>
## [新墨西哥州民用飞机坠毁疑与军用 GPS 干扰相关](https://www.wired.com/story/a-civilian-plane-crashed-in-new-mexico-was-the-militarys-tech-to-blame/) ⭐️ 8.0/10

《连线》杂志的一篇报道审视了新墨西哥州的一起民用飞机坠毁事件，美国国家运输安全委员会（NTSB）的初步报告认为该事件可能与军用 GPS 干扰有关。不过，专家评论指出，机组人员决策失误以及 GPS 冗余能力丧失也是促成因素。 这起事件凸显了一种日益严峻的安全隐患：军用 GPS 干扰可能无意中扰乱民用飞机的导航。同时，它也提醒人们，过度依赖 GPS 可能会削弱飞行员在卫星信号失效时所需的传统导航技能和冗余保障。 坠机发生在无月光的夜晚、地形多山的地区，NTSB 初步报告将 GPS 干扰列为一项因素。分析人士指出，民航客机拥有不依赖 GPS 的 DME/DME 三角定位来实现区域导航（RNAV），但机组人员显然未能有效利用替代导航设备。

hackernews · dzdt · 8月5日 11:03 · [社区讨论](https://news.ycombinator.com/item?id=49181099)

**背景**: GPS 干扰是指故意发射无线电信号，压制来自卫星的微弱导航信号，使接收机无法定位。民航业越来越依赖 GPS，但仍保留着 VOR、DME 和惯性导航等备用系统。美国联邦航空管理局（FAA）发布了关于 GPS/GNSS 干扰与欺骗的资源指南，而军方经常测试 GPS 拒止系统，这些测试可能波及民用空域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPS_jamming">GPS jamming</a></li>
<li><a href="https://www.faa.gov/about/office_org/headquarters_offices/avs/offices/afx/afs/afs400/afs410/GNSS/GPS_GNSS_Interference_Resource_Guide.pdf">GPS and GNSS Interference Resource Guide</a></li>
<li><a href="https://www.flightradar24.com/data/gps-jamming">GPS jamming & interference map | Flightradar24</a></li>

</ul>
</details>

**社区讨论**: 评论者大多认为 GPS 干扰是促成因素之一，但有些人认为飞行员负主要责任。一位 GPS 干扰研究者指出机组人员做出了错误选择，而一位飞行员回忆称 GPS 干扰的航行通告（NOTAM）很常见，飞行员接受过应对此类故障的训练。一位航空公司机长强调，在无月光的夜晚对山区地形进行目视进近风险很高，按 121 部规则运行的航班在这种条件下可能无法合法放行。

**标签**: `#GPS interference`, `#aviation safety`, `#military technology`, `#NTSB`, `#navigation`

---

<a id="item-8"></a>
## [LLM 0.32 新增推理踪迹、OpenAI Responses 与服务端工具](https://simonwillison.net/2026/Aug/4/new-release-of-llm/#atom-everything) ⭐️ 8.0/10

Simon Willison 发布了 LLM 0.32，这是该命令行工具的一次重大升级，新增了可见的推理踪迹、对 OpenAI Responses API 的支持，以及 CodeInterpreter 和 WebSearch 等服务端工具，并将 GPT-5.6 Luna 设为新的默认模型。 该版本显著提升了命令行用户使用 LLM 的透明度和功能性，让开发者更容易查看推理踪迹，也无需复杂配置即可使用服务端工具。同时，它使 LLM 与现代化的 OpenAI Responses API 保持一致，增强了对智能体工作流的兼容性。 推理踪迹默认输出到标准错误流，可通过 -R/--hide-reasoning 标志隐藏。llm-anthropic 插件也获得重大更新，新增了 WebSearch、WebFetch、CodeExecution 和 AnthropicMCP 工具；新的“llm openai endpoint”命令则可在不记录日志的情况下，向任意兼容 OpenAI 的端点发起一次性提示。

rss · Simon Willison · 8月4日 23:58

**背景**: LLM 是 Simon Willison 开发的一款流行的开源命令行工具，用户可以在终端中用它向多种大语言模型运行提示。推理踪迹指推理模型在给出最终答案之前生成的思维链 token，现在 LLM 默认会显示这些踪迹。OpenAI Responses API 是 OpenAI 于 2025 年发布的开发者接口，它将模型响应与内置工具（如网络搜索和代码执行）结合，简化了智能体应用的开发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/simonw/llm">GitHub - simonw/llm: Access large language models from the command-line · GitHub</a></li>
<li><a href="https://developers.openai.com/api/reference/responses/overview">Responses Overview | OpenAI API Reference</a></li>
<li><a href="https://simonwillison.net/2025/May/27/llm-tools/">Large Language Models can run tools in your terminal with LLM 0.26</a></li>

</ul>
</details>

**标签**: `#LLM`, `#OpenAI`, `#developer-tools`, `#AI`, `#Python`

---