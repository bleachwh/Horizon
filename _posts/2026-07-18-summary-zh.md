---
layout: default
title: "Horizon Summary: 2026-07-18 (ZH)"
date: 2026-07-18
lang: zh
---

> 从 33 条内容中筛选出 8 条重要资讯。

---

1. [Kimi K3：开源 2.8 万亿参数模型登顶前端代码竞技场](#item-1) ⭐️ 10.0/10
2. [LG 显示器通过 Windows Update 静默安装软件](#item-2) ⭐️ 9.0/10
3. [特朗普政府拟设类似 FINRA 的机构审查顶尖 AI 模型](#item-3) ⭐️ 9.0/10
4. [GPT-5.6 据称通过提示解决凸优化领域 30 年未解猜想](#item-4) ⭐️ 8.0/10
5. [StackOverflow 衰落可视化：AI 与社区壁垒](#item-5) ⭐️ 8.0/10
6. [公然的无意义 AI 内容赢得 2.5 万美元 Kaggle 大奖，引发赛事诚信争议](#item-6) ⭐️ 8.0/10
7. [豆包手机转向 MCP，备货量增至数十万台](#item-7) ⭐️ 8.0/10
8. [Meta 拟向 Anthropic 出租 AI 算力](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Kimi K3：开源 2.8 万亿参数模型登顶前端代码竞技场](https://t.me/zaihuapd/42637) ⭐️ 10.0/10

月之暗面发布了 Kimi K3，这是全球首个开源的 2.8 万亿参数模型。它在 Frontend Code Arena 基准测试中以 1679 分排名第一，超越了 Claude Fable 5，从第 18 名跃升至榜首。 这一发布标志着开源 AI 的一个重要里程碑，表明大规模模型可以开源并与专有系统竞争。Kimi K3 新颖的注意力架构可能影响未来的模型设计，尤其是在编码和长上下文任务方面。 Kimi K3 使用了 Kimi Delta Attention (KDA)，这是一种线性注意力机制，通过逐通道衰减扩展了 Gated DeltaNet，以及 Attention Residuals，它允许各层有条件地聚合来自之前层的信息。它还具备原生视觉能力和 100 万 token 的上下文窗口。

telegram · zaihuapd · 7月18日 02:29

**背景**: 大型语言模型通常使用全注意力机制训练，其计算量随序列长度呈二次增长。像 KDA 这样的线性注意力机制旨在降低这种复杂度，同时保持表达能力。像 Kimi K3 这样的开源模型使研究人员和开发者能够研究和调整最先进的架构，而无需依赖专有 API。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/moonshot-releases-2-8-trillion-parameter-kimi-k3">China's 2.8-trillion-parameter Kimi K3 beats Claude Fable 5 in Frontend Code Arena benchmark— Moonshot AI delivers largest open-weight AI model ever, as China works around U.S. compute limits | Tom's Hardware</a></li>
<li><a href="https://arxiv.org/abs/2510.26692">Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://arxiv.org/pdf/2603.15031">ATTENTION RESIDUALS TECHNICAL REPORT OF ATTENTION RESIDUALS Kimi Team</a></li>

</ul>
</details>

**标签**: `#open-source`, `#large language model`, `#AI benchmark`, `#attention mechanism`

---

<a id="item-2"></a>
## [LG 显示器通过 Windows Update 静默安装软件](https://videocardz.com/newz/lg-monitors-silently-install-software-through-windows-update-without-user-consent) ⭐️ 9.0/10

LG 显示器在无需用户同意的情况下，通过 Windows Update 的驱动程序交付机制在 Windows 系统上安装厂商软件，一旦通过 HDMI 连接显示器或即使已连接旧款显示器也会触发。 这带来了重大的安全和隐私风险，因为该软件拥有完全的系统访问权限、每次启动时运行，且无需用户交互即可安装，损害了用户对 Windows 更新和硬件厂商实践的信任。 该软件通过微软 WHQL 流程被归类为驱动程序，从而可以通过 Windows Update 自动分发；它具有互联网访问权限且未沙箱化，实质上如同来自第三方厂商的恶意软件。

hackernews · baranul · 7月18日 10:21 · [社区讨论](https://news.ycombinator.com/item?id=48956688)

**背景**: Windows 更新可以自动下载和安装硬件设备的驱动程序更新，包括经过 WHQL 签名的驱动。WHQL（Windows 硬件质量实验室）测试验证驱动通过特定测试，但并不一定阻止分发捆绑了不需要应用的软件。该机制本用于驱动更新，但可能被滥用安装无关的厂商软件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/windows-hardware/drivers/dashboard/understanding-windows-update-automatic-and-optional-rules-for-driver-distribution">Understanding Windows Update rules for driver distribution - Windows drivers | Microsoft Learn</a></li>
<li><a href="https://en.wikipedia.org/wiki/WHQL_Testing">WHQL Testing - Wikipedia</a></li>
<li><a href="https://support.microsoft.com/en-us/windows/update-drivers-through-device-manager-in-windows-ec62f46c-ff14-c91d-eead-d7126dc1f7b6">Update drivers through Device Manager in Windows - Microsoft Support</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了愤怒，指出 Windows 本身应负责任，因为它会自动从设备元数据安装软件。多位用户分享了通过组策略或设备安装设置阻止自动下载驱动相关应用的解决方法。讨论凸显了对 Windows 驱动许可模式的广泛批评，该模式允许任何 WHQL 签名包在未经用户批准的情况下安装。

**标签**: `#security`, `#privacy`, `#windows`, `#lg`, `#driver`

---

<a id="item-3"></a>
## [特朗普政府拟设类似 FINRA 的机构审查顶尖 AI 模型](https://www.bloomberg.com/news/articles/2026-07-17/us-considers-creating-finra-like-watchdog-to-vet-top-ai-models) ⭐️ 9.0/10

特朗普政府正考虑设立一个类似金融业监管局（FINRA）的独立监管机构，负责审查顶尖人工智能模型的安全性。该提案由财政部长斯科特·贝森特牵头制定，旨在回应业界对当前临时管控措施的不满。 此举可能深刻重塑美国的 AI 治理格局，让华尔街和硅谷在安全标准制定上拥有更大发言权，同时可能使监管更加结构化。这标志着美国向类似证券市场监管的行业资助监管模式转变。 拟议的机构将向证券交易委员会（SEC）汇报，并由行业资助，类似 FINRA。该计划与 Google DeepMind 首席执行官德米斯·哈萨比斯本周提出的建议方向一致，但尚未经总统特朗普审阅，框架仍可能调整。

telegram · zaihuapd · 7月18日 05:45

**背景**: FINRA 是一家私营的自我监管组织，负责监管美国的经纪公司和交易所市场，向 SEC 汇报。特朗普政府此前曾因要求 Anthropic 和 OpenAI 等 AI 公司修改或推迟模型发布而遭到反对。当前提案旨在建立一个更可预测且行业参与的监管框架。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://brokercheck.finra.org/">brokercheck. finra .org</a></li>
<li><a href="https://www.mg21.com/finra.html/finra-2">FINRA | 美股之家 - 港股美股开户投资百科全书</a></li>
<li><a href="https://news.pconline.com.cn/2146/21461651.html">美国白宫内部就 AI ...</a></li>

</ul>
</details>

**标签**: `#AI监管`, `#特朗普政府`, `#FINRA`, `#人工智能安全`, `#政策`

---

<a id="item-4"></a>
## [GPT-5.6 据称通过提示解决凸优化领域 30 年未解猜想](https://old.reddit.com/r/math/comments/1uxj3cy/after_openais_cdc_proof_announcement_gpt56_used_a/) ⭐️ 8.0/10

根据一个引发广泛讨论的 Reddit 帖子，OpenAI 的 GPT-5.6（Sol Pro 版本）仅通过一个提示就解决了一个关于凸利普希茨函数在球域上优化问题时间复杂度的、存在 30 年的凸优化猜想。 这表明大型语言模型现在能够处理优化理论中长期存在的专业问题，可能加速研究进展，并将人类数学家的角色转向更具创新性的方法。 该解决方案使用的是 GPT-5.6 Sol Pro，而非更强大的、近期证明了循环双覆盖猜想的 Sol Ultra 模型。该猜想专注于解决凸利普希茨优化问题的上界，该结果被认为是真实但小众的贡献。

hackernews · mbustamanter · 7月18日 13:00 · [社区讨论](https://news.ycombinator.com/item?id=48957779)

**背景**: 凸优化是优化理论的一个分支，研究在凸集上最小化凸函数，广泛应用于机器学习、工程和经济学。此猜想涉及球域上利普希茨函数这类问题的最坏情况时间复杂性，这个空白已存在约 30 年。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=48957779">GPT-5.6 used a prompt to close a 30-year gap in convex optimization | Hacker News</a></li>
<li><a href="https://openai.com/index/model-disproves-discrete-geometry-conjecture/">An OpenAI model has disproved a central conjecture in discrete geometry | OpenAI</a></li>
<li><a href="https://mlq.ai/news/openai-claims-gpt-56-sol-ultra-solved-50-year-old-math-conjecture-in-under-an-hour/">OpenAI Claims GPT-5.6 Sol Ultra Solved 50-Year-Old Math Conjecture in Under an Hour | MLQ News</a></li>

</ul>
</details>

**社区讨论**: 社区评论指出，该猜想比最近的循环双覆盖证明更为小众，但仍是一个真正的贡献。一些人对廉价智能表示惊叹，而另一些人质疑其实用影响，并讨论了模型版本（Sol Pro 与 Ultra）。还有关于此类证明是否标志着人类研究者的低垂果实终结的辩论。

**标签**: `#AI`, `#optimization`, `#convex optimization`, `#GPT-5.6`, `#machine learning`

---

<a id="item-5"></a>
## [StackOverflow 衰落可视化：AI 与社区壁垒](https://data.stackexchange.com/stackoverflow/query/1953768#graph) ⭐️ 8.0/10

Stack Exchange 数据浏览器中的一条查询显示，StackOverflow 的活动自 2014 年左右达到峰值后急剧下降，并在 ChatGPT 等 AI 编程助手兴起后加速衰退。 这一趋势凸显了 AI 工具如何重塑知识共享平台，并揭示了长期存在的社区治理问题使 StackOverflow 容易受到颠覆。 衰退在 AI 成为主流之前就已开始，但严格的审核、排他性政策以及 2021 年被 Prosus 收购等因素进一步削弱了用户参与度。

hackernews · secretslol · 7月18日 11:12 · [社区讨论](https://news.ycombinator.com/item?id=48956949)

**背景**: StackOverflow 是一个面向程序员的问答平台，以其禁止讨论的严格规则和对新提问者的高门槛而闻名。像 ChatGPT 这样的 AI 聊天助手现在能提供直接、对话式的答案，减少了用户访问 StackOverflow 死板格式的需求。

**社区讨论**: 评论者指出该网站的排他性文化、缺乏社区感以及 Prosus 收购的影响。有人提到，在服务条款允许将内容用于 AI 训练后，用户删除了自己的贡献。

**标签**: `#StackOverflow`, `#AI`, `#community`, `#Q&A platforms`, `#decline`

---

<a id="item-6"></a>
## [公然的无意义 AI 内容赢得 2.5 万美元 Kaggle 大奖，引发赛事诚信争议](https://www.reddit.com/r/MachineLearning/comments/1uzyf66/did_blatant_ai_slop_just_win_a_25k_usd_deepmind/) ⭐️ 8.0/10

一位 Reddit 用户出示证据，指出在谷歌 DeepMind 赞助的 Kaggle 挑战赛“衡量通向 AGI 的进展——认知能力”中，一个毫无意义的提交获得了 2.5 万美元大奖，并质疑评审过程的严谨性。 这一事件对备受瞩目的 AI 竞赛的评审标准提出了质疑，可能损害 Kaggle 和 DeepMind 在基准开发工作方面的公信力。 该提交旨在测试大型语言模型（LLM）在接收其他 LLM 的不同观点后是否会改变自身判断，但其论文被描述为“情绪化的混乱一团”，包含无根据的声明和毫无意义的数字生成机器。

reddit · r/MachineLearning · /u/TheWerkmeister · 7月18日 15:10

**背景**: 该 Kaggle 竞赛总奖金池为 20 万美元，要求参与者设计基于认知科学的新型 AI 基准，以衡量通向 AGI 的进展。认知基准通常以人类认知为基础，评估 AI 系统在推理、适应性等多个维度上的表现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/googledeepmind_how-do-we-measure-progress-toward-agi-it-activity-7439782084551806976-0e2M">How do we measure progress toward AGI ? It takes a village – and...</a></li>
<li><a href="https://ailearninghubhq.beehiiv.com/p/google-deepmind-wants-you-to-help-measure-agi">Google DeepMind Wants You to Help Measure AGI</a></li>
<li><a href="https://www.edtechinnovationhub.com/news/google-deepmind-and-kaggle-open-agi-benchmark-contest-with-200000-prize-pool">Google DeepMind AGI benchmark... — EdTech Innovation Hub</a></li>

</ul>
</details>

**标签**: `#Kaggle`, `#DeepMind`, `#AI benchmarks`, `#competition integrity`, `#machine learning`

---

<a id="item-7"></a>
## [豆包手机转向 MCP，备货量增至数十万台](https://www.latepost.com/news/dj_detail?id=3648) ⭐️ 8.0/10

豆包手机将放弃对阿里、腾讯等头部应用的 GUI 自动化操作，转而要求这些应用自行提供 MCP 服务并开放数据与操控权限。同时，备货量从此前的 3 万台提升至数十万台。 这一战略转变与行业趋势一致，苹果和谷歌也在转向开放 MCP 框架，同时表明对 AI 手机助手规模化的信心增强。如果成功，它可能通过让超级应用合作而非抵抗，重塑移动 AI 生态系统。 豆包手机助手软件于 2025 年 7 月 15 日获得生成式人工智能服务备案，并于 2025 年 12 月首次发布技术预览版。此前使用 GUI 自动化时曾遭微信和淘宝封禁，促成了基于 MCP 的新策略。

telegram · zaihuapd · 7月18日 00:29

**背景**: MCP（模型上下文协议）是 Anthropic 于 2024 年 11 月推出的开放标准，旨在规范 AI 系统与外部工具和数据源的连接方式，常被形容为“AI 的 USB-C 端口”。苹果和谷歌也已采用类似框架，表明行业正从脆弱的 GUI 自动化转向基于 API 的协作式 AI 助手接口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol</a></li>
<li><a href="https://modelcontextprotocol.io/">What is the Model Context Protocol (MCP)? - Model Context Protocol</a></li>

</ul>
</details>

**标签**: `#AI`, `#mobile assistants`, `#MCP`, `#strategy`, `#ecosystem`

---

<a id="item-8"></a>
## [Meta 拟向 Anthropic 出租 AI 算力](https://www.nytimes.com/2026/07/17/technology/meta-anthropic-ai-computing-power.html) ⭐️ 8.0/10

Meta 正与 Anthropic 进行早期谈判，拟将其 AI 数据中心的算力出租给后者，潜在交易规模两年内达 100 亿美元。Anthropic 于 2026 年 6 月提出该方案，Meta 正在评估。 该交易凸显了 AI 算力的高度稀缺性，并使 Meta 能够将闲置算力变现，或可缓解投资者对其巨额基础设施支出的担忧。同时，它为领先的 AI 初创公司 Anthropic 确保了关键算力。 根据拟议协议，Anthropic 将按月付款，双方均可提前退出。谈判尚处早期阶段，未必能最终成交。Meta 今年计划投入高达 1450 亿美元，其中大量用于 AI 与数据中心建设。

telegram · zaihuapd · 7月18日 01:14

**背景**: AI 算力是训练和运行大型语言模型 (LLM) 及其他 AI 系统的关键资源。需求激增，已超过主要云提供商的供应能力。Meta 一直在大力建设其 AI 基础设施，从而产生了可能出租给其他人的闲置算力。

**标签**: `#AI compute`, `#Meta`, `#Anthropic`, `#data centers`, `#business deal`

---