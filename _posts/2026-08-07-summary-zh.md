---
layout: default
title: "Horizon Summary: 2026-08-07 (ZH)"
date: 2026-08-07
lang: zh
---

> 从 33 条内容中筛选出 8 条重要资讯。

---

1. [甲骨文禁止将 AI 生成的代码贡献给 OpenJDK](#item-1) ⭐️ 8.0/10
2. [科技从业者对职业失去信心](#item-2) ⭐️ 8.0/10
3. [pgrust 利用 SIMD 与算子融合让 Postgres 分析查询提速 300 倍](#item-3) ⭐️ 8.0/10
4. [与爬虫搏斗一年：150 万页网站遭遇机器人流量](#item-4) ⭐️ 8.0/10
5. [Wyzer：用编排式编程防止分布式死锁的新语言](#item-5) ⭐️ 8.0/10
6. [新墨西哥州法院命令 Meta 支付 5.67 亿美元，因其危害儿童心理健康](#item-6) ⭐️ 8.0/10
7. [Gemini 遇困，谷歌云却因 AI 受益](#item-7) ⭐️ 8.0/10
8. [美国审查中国 AI 企业海外获取英伟达芯片渠道](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [甲骨文禁止将 AI 生成的代码贡献给 OpenJDK](https://app.dealroom.co/news/feed/oracle-bans-ai-generated-code-from-openjdk-despite-ellison-s-claim-oracle-isn-t-writing-its-own-code) ⭐️ 8.0/10

甲骨文（Oracle）已推出一项临时政策，禁止将 AI 生成的代码贡献给 OpenJDK。该政策目前由甲骨文法务团队最终敲定，其公开目标是保护项目完整性并规避法律风险。 这一政策直接影响 OpenJDK 社区，并为其他正在应对 AI 生成贡献的开源项目树立了先例。它凸显了 AI 代码给协作开发带来的日益增长的法律与审查负担挑战。 这项临时政策明确禁止 AI 生成的代码，理由是“人类审查者的时间本来就有限”。甲骨文的律师正在起草最终版本，表明该公司采取了与以往 Java 版权纠纷类似的谨慎法律立场。

hackernews · delduca · 8月7日 17:36 · [社区讨论](https://news.ycombinator.com/item?id=49213754)

**背景**: OpenJDK 是 Java 平台标准版（Java SE）的自由开源实现，由 Sun Microsystems 于 2006 年发起，在被甲骨文收购后由其维护。自 Java 7 起，它一直是 Java SE 的官方参考实现，并被企业广泛使用。这项新政策反映了整个行业在借助 AI 提高生产力与确保代码来源法律明确性之间的矛盾。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenJDK">OpenJDK</a></li>
<li><a href="https://grokipedia.com/page/OpenJDK">OpenJDK</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，甲骨文一面大力投资 AI，一面却禁止 OpenJDK 使用 AI 代码，这颇具讽刺意味。一些人认为该政策作为规避法律与审查负担的举措是合理的，但也有不少人质疑其可执行性，并怀疑最终政策不会更好。

**标签**: `#OpenJDK`, `#Oracle`, `#AI Policy`, `#Open Source`, `#Legal`

---

<a id="item-2"></a>
## [科技从业者对职业失去信心](https://www.noemamag.com/why-is-everyone-in-tech-so-sad/) ⭐️ 8.0/10

《Noema》杂志发表文章《为什么科技行业的人都这么悲伤？》，探讨科技工作者中广泛存在的不满与职业信念丧失。这篇文章引发了热烈讨论，评论达到 257 条。 这之所以重要，是因为它反映了最具影响力的行业之一的显著文化转变，可能影响创新、人才留存和心理健康。高参与度（159 分）表明它与从业者产生了强烈共鸣。 这篇评分 8.0/10 的文章引用了印刷行业衰落等历史类比，以及关于职业倦怠的个人反思。评论者还讨论了网络的毒性、“K 型”经济以及逃避到简单职业的虚幻想法。

hackernews · RickJWagner · 8月7日 12:42 · [社区讨论](https://news.ycombinator.com/item?id=49209539)

**背景**: 科技行业长期以来被视为理想职业，但近年来关于职业倦怠、裁员和理想幻灭的报道不断增多。这篇文章契合了这一情绪，而评论区则将当下与印刷等手艺行业的衰落历史进行对比。

**社区讨论**: 评论者深度参与，分享个人经历和历史类比；一些人认为这种现象并非新鲜事，另一些人则突出强调现代网络的毒性和经济限制。总体情绪表明人们与文章论点产生了强烈共鸣。

**标签**: `#tech culture`, `#burnout`, `#career`, `#software engineering`, `#mental health`

---

<a id="item-3"></a>
## [pgrust 利用 SIMD 与算子融合让 Postgres 分析查询提速 300 倍](https://malisper.me/how-we-made-postgres-hundreds-of-times-faster-the-query-engine/) ⭐️ 8.0/10

pgrust 是一个用 Rust 重写 PostgreSQL 的实验性项目，声称其分析查询速度比标准 Postgres 最多快 300 倍。这一提速来自批处理、算子融合和 SIMD 指令；该项目目前能通过 Postgres 回归测试，并借助形式化验证与模糊测试保障正确性。 如果该方案经得起验证，pgrust 表明基于 Rust 的重写可以在保持兼容性的同时超越成熟的 C 语言数据库引擎，这可能影响 Postgres 未来的开发方向，或催生替代性查询引擎设计。它能在不脱离 Postgres 生态的前提下，为分析型负载带来显著性能提升。 这篇文章详述了三项技术：批处理（分块处理数据）、算子融合（合并相邻算子以减少开销）以及 SIMD（单条指令处理多个数据元素）。作者强调正确性是第一优先级，目前已证明 1000 多个用户可见函数与 Postgres 逻辑完全一致，并进行了差分模糊测试。

hackernews · poly2it · 8月7日 11:00 · [社区讨论](https://news.ycombinator.com/item?id=49208535)

**背景**: PostgreSQL 是一款广泛使用的开源关系型数据库，其查询引擎通常采用基于拉取的迭代器模型逐行处理数据，在处理大规模分析查询时会产生较高开销。pgrust 是用 Rust 对 PostgreSQL 进行的实验性重写，目标是尽量贴近 Postgres 行为，同时为深度优化打开空间。批处理、算子融合与 SIMD 都是现代列式及向量化查询引擎中的常用技术——批处理能摊薄逐行成本，算子融合避免中间结果物化，SIMD 则利用 CPU 的并行处理能力。这也是 ClickHouse 等高性能数据库所采用的路线，而 pgrust 声称在这些技术下比 ClickHouse 更快。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pgrust.com/">pgrust — postgres, rewritten in rust</a></li>
<li><a href="https://github.com/malisper/pgrust">GitHub - malisper/ pgrust : Postgres rewritten in Rust , now faster than...</a></li>

</ul>
</details>

**社区讨论**: 作者回应了最大的疑虑——可信度——介绍了形式化验证和差分模糊测试。评论者对自适应规划的前景感到兴奋，但也有多人表示怀疑：社区不太可能采用非官方 Postgres 团队开发的重写版本，因为生态成熟度、长期维护和支持都很关键。还有轻松的评论调侃 GROUP BY 的速度问题。

**标签**: `#postgres`, `#query-engine`, `#SIMD`, `#performance`, `#analytics`

---

<a id="item-4"></a>
## [与爬虫搏斗一年：150 万页网站遭遇机器人流量](https://patronview.com/news/99-percent-of-my-website-traffic-is-bots/) ⭐️ 8.0/10

作者发布了一篇回顾文章，详细讲述在一家拥有 150 万页面的网站上与爬虫搏斗一年的经历，结果显示超过 99%的流量都是机器人。他们尝试了多种缓解方案，并记录了一次糟糕的流量高峰如何让原本约 90 美元的月度账单暴增约 500%。 这件事很重要，因为它量化了开放网络上机器人流量的规模，并揭示了各种缓解策略的代价——从基础设施成本上升，到对 Cloudflare 等中心化提供商的依赖。独立网站运营者和公共数据发布者可以借鉴这些经验，更明智地决定如何管理机器人流量。 作者平常每月的基础设施账单约为 90 美元，但一次糟糕的流量高峰月让账单上涨约 500%，部分原因是 Cloudflare D1 的费用高得惊人。有评论者报告称，Claude 的搜索机器人在 72 小时内抓取了约 20.5 万个页面，却只带来 1 次引荐；作者也坦承自己的网站同样在抓取公开文档。

hackernews · petercooper · 8月7日 14:51 · [社区讨论](https://news.ycombinator.com/item?id=49211386)

**背景**: 爬虫和机器人会用大量请求淹没网站、扭曲统计数字并推高托管成本，因此站长通常会部署反爬系统。常见技术包括 TLS 指纹识别（在运行 JavaScript 之前即根据握手特征识别客户端）、JavaScript 挑战（要求访问者“证明自己是人类”）以及数据中心 IP 段识别（用于标记代理或 VPN 流量）。许多网站将这类过滤工作外包给 Cloudflare 等服务，这也意味着“谁能访问网站”的决策被集中到了大公司手中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://webunlocker.com/learn/tls-fingerprints">TLS Fingerprint Testing - How Anti- Bot Systems Detect Automation</a></li>
<li><a href="https://hackernoon.com/bypassing-javascript-challenges-for-effective-web-scraping">Bypassing JavaScript Challenges for Effective Web Scraping | HackerNoon</a></li>
<li><a href="https://www.ipqualityscore.com/free-ip-lookup-proxy-vpn-test">Proxy Detection Test | Detect Proxies With Our IP Lookup</a></li>

</ul>
</details>

**社区讨论**: 社区评论以务实为主：有人担心把访问决策外包给 Cloudflare 的问题，也有人推荐 Anubis——一种适用于未使用 CDN 的网站的工作量证明方案。有评论者建议放弃 D1、改用静态站点来控制成本；还有人抱怨 AI 搜索机器人消耗了大量带宽却几乎不带来任何引荐流量。

**标签**: `#web scraping`, `#bot mitigation`, `#Cloudflare`, `#DevOps`, `#performance`

---

<a id="item-5"></a>
## [Wyzer：用编排式编程防止分布式死锁的新语言](https://github.com/Wyzer-Lang/wyzer) ⭐️ 8.0/10

Wyzer 是一门静态类型、编译型编程语言，它将编排式编程（choreographic programming）与 Perceus 内存模型结合，用于防止分布式死锁和协议不匹配。作者表示，经过约五个月的研究和数周开发，0.1.0 版本即将发布。 在 Rust 等主流语言中，分布式死锁和跨服务协议错误仍然非常难以处理，因为这些语言主要关注内存安全。Wyzer 是一次早期且雄心勃勃的尝试，旨在将编排式编程从学术界带入实用语言，有望为生态系统补充分布式系统层面的安全性。 Wyzer 用线性/仿射类型（linear/affine types）和 Perceus 引用计数取代了 Rust 风格的借用检查，作者称这对 LSP 工具来说在计算上更容易理解。该项目仍处于早期阶段；README 介绍了基本语法，但社区成员指出它尚未充分解释编排式编程或 Perceus。

hackernews · v0id_isgood · 8月7日 12:28 · [社区讨论](https://news.ycombinator.com/item?id=49209385)

**背景**: 编排式编程是一种分布式系统范式：程序员将整个系统的交互写成单一“编舞”（choreography），编译器再将其投影为每个参与者可执行的代码，从而保证每次发送都有对应的接收，并在编舞范围内避免死锁。Perceus 是 Koka 语言使用的一种精确引用计数算法，可以无需垃圾回收器而直接编译到 C，并实现“函数式但原地”的内存复用。面向资源的编程（resource-oriented programming）将线性类型与所有权规则结合以安全地管理资源，Wyzer 将这些技术一同使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Choreographic_programming">Choreographic programming</a></li>
<li><a href="https://www.microsoft.com/en-us/research/publication/perceus-garbage-free-reference-counting-with-reuse/">Perceus : Garbage Free Reference Counting with... - Microsoft Research</a></li>
<li><a href="https://en.wikipedia.org/wiki/Resource-oriented_computing">Resource-oriented computing - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上对 Wyzer 的雄心和保守的语法表示赞赏，但多人表示 README 和文档没有突出真正新颖的部分，例如编排式编程和 Perceus。有用户要求给出具体示例，展示如何保证无死锁；也有人将 Wyzer 的编排式特性与 Next.js、Dioxus 中的 server functions 相比较。整体氛围是建设性的：改进文档和示例，让想法更清晰。

**标签**: `#programming-language`, `#distributed-systems`, `#choreographic-programming`, `#static-typing`, `#memory-management`

---

<a id="item-6"></a>
## [新墨西哥州法院命令 Meta 支付 5.67 亿美元，因其危害儿童心理健康](https://www.theguardian.com/technology/2026/aug/06/new-mexico-court-meta) ⭐️ 8.0/10

新墨西哥州一家法院裁定，Meta 必须为其社交媒体平台对儿童心理健康造成的伤害支付 5.67 亿美元。该裁决还要求该公司为未成年用户做出改变。 这是一项具有里程碑意义的裁决，让大型科技公司为影响儿童心理健康的算法伤害承担法律责任。它可能为其他司法管辖区树立先例，并加大社交媒体平台为加强儿童安全保护而重新设计产品的压力。 该判决依据新墨西哥州的公共妨害法（NMSA 1978 § 30-8-1），法院认定 Meta 故意制造了危害公众健康和福利的公共妨害。报道的金额略有差异：标题称用于青少年心理健康基金的金额为 5.67 亿美元，而另一些媒体则称总额为 9.42 亿美元，可能反映了不同的损害赔偿部分。

hackernews · boplicity · 8月7日 00:06 · [社区讨论](https://news.ycombinator.com/item?id=49204352)

**背景**: 社交媒体平台（如 Meta 旗下的 Instagram 和 Facebook）一直被广泛批评使用令人上瘾的算法，可能对青少年的心理健康产生负面影响，包括增加焦虑和抑郁。新墨西哥州是一个相对较小的州，因此与 Meta 在该州的收入相比，如此规模的判决意义重大，法律专家认为它可能会鼓励其他地区对科技公司采取类似行动。

**社区讨论**: 评论者普遍认为这一裁决是积极的，但也指出该金额只是 Meta 全球收入的一小部分。有评论者指出，对于像新墨西哥州这样人口约 200 万的小辖区来说，9.42 亿美元的判决是巨大的；还有评论者强调了 Meta 违反的具体公共妨害法。有人批评 Reels 和 TikTok 等短视频功能的成瘾性，也有人质疑这样的罚款是否足以改变企业行为。

**标签**: `#Meta`, `#legal`, `#mental health`, `#regulation`, `#social media`

---

<a id="item-7"></a>
## [Gemini 遇困，谷歌云却因 AI 受益](https://newsletter.semianalysis.com/p/gemini-is-cooked-but-gcp-is-cooking) ⭐️ 8.0/10

Semianalysis 的一份新分析认为，谷歌的 Gemini AI 模型在竞争中处境艰难，而谷歌云（GCP）却因 AI 需求的激增而获得短期收益。文章将此描述为 DeepMind 的长期失利，反而成为 GCP 的短期获利。 该分析揭示了谷歌内部的一种战略分化：DeepMind 难以与对手抗衡，可能削弱谷歌在 AI 领域的长期领导地位，尽管 GCP 受 AI 推动的云收入提供了短期的财务缓冲。这对投资者、AI 观察者以及押注谷歌 AI 生态的企业客户都很重要。 该报告将 GCP 的增长视为一种短期收益，掩盖了 DeepMind 的长期失败，表明企业 AI 需求正在流向谷歌的云基础设施，尽管 Gemini 仍落后于 OpenAI 等竞争对手。这暗示谷歌的前沿模型研究与云端商业化战略之间可能存在错位。

rss · Semianalysis · 8月7日 02:32

**背景**: Gemini 是谷歌旗下旗舰大语言模型系列，与 OpenAI 的 GPT 系列及 Anthropic 的 Claude 竞争。GCP（谷歌云平台）是谷歌的云计算部门，受益于企业采用 AI 服务。DeepMind 是谷歌的 AI 研究实验室，负责开发 Gemini 及其他突破性技术。该分析默认读者熟悉谷歌内部的公司架构以及 AI 行业的竞争格局。

**标签**: `#AI`, `#Google Cloud`, `#Gemini`, `#Industry Analysis`

---

<a id="item-8"></a>
## [美国审查中国 AI 企业海外获取英伟达芯片渠道](https://www.bloomberg.com/news/articles/2026-08-07/us-reviews-china-s-offshore-access-to-nvidia-chips-after-ai-breakthroughs) ⭐️ 8.0/10

美国商务部工业与安全局（BIS）已对中国 AI 企业如何在海外获取和使用英伟达芯片展开系统性审查，涵盖通过租用他国算力进行远程访问的方式。此次审查是在美方指控月之暗面的 Kimi K3 模型涉嫌非法获取英伟达芯片并经泰国远程访问之后启动的。 此举可能导致美国出口管制从实体芯片扩大到远程云计算访问，重塑中国 AI 企业使用全球算力基础设施的方式。这也标志着中美科技紧张局势升级，并可能影响主要云服务商和半导体供应链。 据报道，BIS 正在整理两份名单：一是涉嫌存在将受限芯片走私入境中国的黑市所在国，二是中国企业远程租用芯片的国家。由于远程访问本身并不违法，BIS 是否有权限制此类云计算协议仍存疑；美国众议院已通过两党法案拟明确授予该权力，但预计会遭到英伟达等科技公司反对。

telegram · zaihuapd · 8月7日 11:18

**背景**: 美国为减缓中国在 AI 军事与技术领域的进步，限制向中国出口先进英伟达芯片，但中国企业通过租用海外数据中心或经由第三国走私芯片等方式寻找规避途径。远程云计算访问让中国企业无需实体进口即可使用最先进的英伟达硬件，这是监管机构目前正在审查的漏洞。据报道，阿里巴巴通过开曼实体控制的新加坡壳公司，经正被美方调查的 Megaspeed 使用位于马来西亚的英伟达芯片。

**标签**: `#AI`, `#Nvidia`, `#export-controls`, `#China`, `#semiconductors`

---