---
layout: default
title: "Horizon Summary: 2026-07-07 (ZH)"
date: 2026-07-07
lang: zh
---

> 从 42 条内容中筛选出 8 条重要资讯。

---

1. [欧盟议会推进有争议的聊天监控法](#item-1) ⭐️ 9.0/10
2. [微软解雇 id Software 的 idTech 团队](#item-2) ⭐️ 9.0/10
3. [MIRA：面向火箭联盟的开源 50 亿参数世界模型](#item-3) ⭐️ 9.0/10
4. [中国拟投 2 万亿元建设全国算力网络](#item-4) ⭐️ 9.0/10
5. [潜伏 16 年的 KVM 漏洞 Januscape 可让虚拟机逃逸至宿主机](#item-5) ⭐️ 9.0/10
6. [DeepSeek 自研 AI 芯片以减少对英伟达和华为依赖](#item-6) ⭐️ 9.0/10
7. [欧盟聊天控制提案概述](#item-7) ⭐️ 8.0/10
8. [sqlite-utils 4.0 发布，支持数据库模式迁移](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [欧盟议会推进有争议的聊天监控法](https://www.heise.de/en/news/Showdown-in-Strasbourg-The-unexpected-return-of-Chat-Control-1-0-11356680.html) ⭐️ 9.0/10

欧盟议会通过程序性操作将聊天监控提案推进至二读阶段，若要对法案进行修改或否决需获得绝对多数（361 票），而通过法案只需出席议员的简单多数。 该法律将强制对私人通信进行大规模监控，可能破坏加密技术并损害所有欧盟公民的数字隐私。程序性操作引发了对民主合法性的担忧，因许多议员已开始休暑假，支持者更容易推动法案通过。 二读阶段要求所有 720 名议员的绝对多数（361 票）才能修改或否决法案，但只需出席议员的简单多数即可通过。投票定于周四进行，批评者指出历史上夏季休会前的最后一次会议出席率较低。

hackernews · miroljub · 7月7日 15:16 · [社区讨论](https://news.ycombinator.com/item?id=48819008)

**背景**: 聊天监控（Chat Control），正式名称为欧盟 CSA 法规，是一项旨在检测私人通信中儿童性虐待材料（CSAM）的提案。批评者认为目前没有技术能在不产生高错误率的情况下检测 CSAM，会导致大量误报并对无辜用户进行大规模监控。该法律此前曾被否决，但通过程序性调整重新提出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control">Chat Control - Wikipedia</a></li>
<li><a href="https://edri.org/our-work/chat-control-what-is-actually-going-on/">Chat Control: What is actually going on? - European Digital Rights (EDRi)</a></li>
<li><a href="https://fightchatcontrol.eu/">Fight Chat Control - Protect Digital Privacy in the EU</a></li>

</ul>
</details>

**社区讨论**: 评论者强烈反对这一程序性操作，有人引用让-克洛德·容克曾说的策略：反复推动法律直到通过。其他评论指出周四前很难再找到 60 张反对票，一些人对他们投票反对该措施的议员表示赞赏。

**标签**: `#surveillance`, `#EU`, `#privacy`, `#policy`, `#democracy`

---

<a id="item-2"></a>
## [微软解雇 id Software 的 idTech 团队](https://gamefromscratch.com/microsoft-fire-idtech-team-at-id-software/) ⭐️ 9.0/10

微软解雇了 id Software 的整个 idTech 引擎团队，这标志着该公司可能放弃自研引擎，转而使用 Unreal Engine 5。 此举可能进一步巩固 Epic Games 在游戏引擎市场的主导地位，减少行业技术多样性，并可能损害 id Software 独特的游戏手感。 idTech 团队曾负责开发用于《毁灭战士》和《雷神之锤》等标志性游戏的专有引擎。微软的裁员意味着未来 id Software 的游戏可能将使用 Unreal Engine。

hackernews · bauc · 7月7日 15:33 · [社区讨论](https://news.ycombinator.com/item?id=48819244)

**背景**: id Software 自 1993 年《毁灭战士》首次使用 id Tech 系列引擎以来，一直以创建有影响力的游戏引擎而闻名。idTech 引擎因其性能和图形能力备受赞誉，是该工作室的关键差异化优势。微软于 2021 年收购了 id Software 的母公司 ZeniMax。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Id_Tech">id Tech - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 许多评论者批评这一决定，称其短视，并警告可能导致 Epic Games 在游戏引擎领域形成垄断。有人认为 id Software 独特的技术文化是其过去成功的关键，而工具的同质化将损害未来作品的质量。

**标签**: `#game engines`, `#Microsoft`, `#id Software`, `#layoffs`, `#Unreal Engine`

---

<a id="item-3"></a>
## [MIRA：面向火箭联盟的开源 50 亿参数世界模型](https://www.reddit.com/r/MachineLearning/comments/1upofuw/mira_multiplayer_interactive_world_models_trained/) ⭐️ 9.0/10

General Intuition、Kyutai 和 Epic Games 联合发布了 MIRA，这是一个拥有 50 亿参数的多玩家交互式世界模型，基于 10,000 小时的合成《火箭联盟》数据训练而成。该模型可在单个 NVIDIA B200 GPU 上以 20 FPS 的速度支持四人游戏，并附有可玩演示、技术报告和开源代码仓库。 MIRA 代表了多玩家游戏开源世界模型的重要进步，可能加速游戏人工智能和强化学习领域的研究。其开源发布使研究人员和开发者能够实验并基于大规模交互式世界模型进行构建。 该模型拥有 50 亿参数，基于 10,000 小时的《火箭联盟》合成游戏数据训练而成。在 NVIDIA B200 GPU 上，它可支持最多四名玩家以每秒 20 帧的速度进行交互，同时还发布了 1,000 小时的四人游戏数据集。

reddit · r/MachineLearning · /u/MasterScrat · 7月7日 07:59

**背景**: 人工智能中的世界模型是一种学习环境内部表示并预测环境如何随动作变化的系统。这对于强化学习和规划至关重要，因为它允许智能体无需真实世界交互即可模拟结果。NVIDIA B200 是 Blackwell 架构的高性能 GPU，专为密集型 AI 工作负载设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/World_model_(artificial_intelligence)">World model (artificial intelligence) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nvidia_B200">Nvidia B200</a></li>

</ul>
</details>

**标签**: `#world models`, `#game AI`, `#large-scale models`, `#reinforcement learning`, `#open source`

---

<a id="item-4"></a>
## [中国拟投 2 万亿元建设全国算力网络](https://t.me/zaihuapd/42399) ⭐️ 9.0/10

中国宣布计划在未来五年投入约 2 万亿元（2950 亿美元），建设全国互联数据中心网络，优先采用华为等本土供应商的 AI 芯片，占比至少 80%。 这项巨额投资旨在减少中国对英伟达、AMD 等美国芯片制造商的依赖，同时将区域算力资源整合为统一网络，以支持 AI 发展，让企业和公共部门更容易获得高性能计算。 该计划是北京“六网”基础设施战略的关键一环，由中国电信、中国联通等国有电信企业运营主要设施。它们已推出 Token 套餐，将算力像移动数据一样打包销售，最低 9.9 元可购 1000 万 Token，降低了 AI 模型使用成本。

telegram · zaihuapd · 7月7日 04:45

**背景**: 全国算力网络连接分布式数据中心和计算资源，实现算力的高效调度和供给，类似于电网输送电力。这一概念是中国数字经济的关键，而基于 Token 的定价模式允许用户按需购买算力，使企业和个人负担得起 AI 计算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://m.21jingji.com/article/20240517/2bc881b0c920056fbd20ac926093d25d_zaker.html">构建全国一体化算力网：多方参与打破“算力孤岛” - 21世纪经济报道</a></li>
<li><a href="https://www.asiainfo.com/zh_cn/content_4527.html">专家解读：加快构建全国一体化算力网络-亚信科技</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#computing network`, `#China`, `#AI chips`, `#geopolitics`

---

<a id="item-5"></a>
## [潜伏 16 年的 KVM 漏洞 Januscape 可让虚拟机逃逸至宿主机](https://github.com/V4bel/Januscape) ⭐️ 9.0/10

安全研究人员公开了 Januscape（CVE-2026-53359）漏洞，这是 KVM 影子 MMU 中的一个释放后使用漏洞，同时影响 Intel 和 AMD x86 系统，并且发布了概念验证(PoC)利用代码，可从客户机内部使宿主机内核崩溃。 该漏洞打破了虚拟机与宿主机之间的隔离，对广泛使用 KVM 的多租户云环境构成直接威胁，攻击者通过客户机访问权限可逃逸至宿主机，进而危害其他虚拟机或整个云基础设施。 该漏洞自 2010 年起就存在于 Linux 内核中，曾在 Google 的 kvmCTF 竞赛中被用作零日攻击。在 RHEL 等发行版中，本地普通用户还可利用该漏洞在宿主机上提权至 root。

telegram · zaihuapd · 7月7日 10:14

**背景**: KVM（基于内核的虚拟机）依赖硬件辅助的嵌套页表（EPT/NPT）或软件影子页表来管理客户机内存。影子 MMU 维护着镜像客户机页表的影子页表，但该子系统中的释放后使用漏洞可导致内存损坏。Januscape 是首个同时在 Intel 和 AMD 平台上工作的 KVM/x86 虚拟机逃逸漏洞，凸显了潜伏 16 年的严重设计缺陷。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/07/16-year-old-linux-kvm-flaw-lets-guest.html">16-Year-Old Linux KVM Flaw Lets Guest VMs Escape to Host on Intel and AMD x86 Systems</a></li>
<li><a href="https://docs.kernel.org/virt/kvm/x86/mmu.html">The x86 kvm shadow mmu — The Linux Kernel documentation</a></li>

</ul>
</details>

**标签**: `#security`, `#kvm`, `#vulnerability`, `#cloud`, `#cve`

---

<a id="item-6"></a>
## [DeepSeek 自研 AI 芯片以减少对英伟达和华为依赖](https://www.reuters.com/world/china/chinas-deepseek-developing-its-own-ai-chip-sources-say-2026-07-07/) ⭐️ 9.0/10

据三位知情人士透露，中国 AI 公司 DeepSeek 正在自研 AI 推理芯片，以减少对英伟达和华为芯片的依赖。该芯片项目始于约一年前，目前仍处于早期阶段，DeepSeek 已开始招聘芯片设计工程师并与代工厂接洽。 此举可能重塑 AI 芯片供应链，降低 DeepSeek 因美国对英伟达和华为芯片出口管制而面临的脆弱性。这凸显了中国 AI 公司为保障供应安全和竞争优势而自研芯片的趋势。 该芯片专为 AI 推理阶段设计，即已训练模型为用户生成回答的环节，而非模型训练。DeepSeek 此前依赖英伟达 H800 GPU 和华为昇腾芯片，但美国出口管制迫使该公司寻求替代方案。

telegram · zaihuapd · 7月7日 11:08

**背景**: 英伟达 H800 是基于 Hopper 架构的数据中心 GPU，用于 AI 训练和推理。美国出口管制限制了对中国销售先进的英伟达芯片，促使中国 AI 公司探索华为昇腾芯片或自研方案。DeepSeek 创始人梁文锋在 2024 年一次罕见采访中承认，芯片管制是公司面临的挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/NVIDIA_H800_GPU">NVIDIA H800 GPU</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#DeepSeek`, `#export controls`, `#semiconductors`, `#AI inference`

---

<a id="item-7"></a>
## [欧盟聊天控制提案概述](https://fightchatcontrol.eu/chat-control-overview) ⭐️ 8.0/10

该文章概述了欧盟聊天控制 1.0 和 2.0 提案，这些提案旨在扫描私人消息以查找儿童性虐待材料，引发了严重的隐私和加密担忧。 这些提案可能会强制对私人通信进行大规模监控，破坏整个欧盟的端到端加密和用户隐私。该立法对软件工程师、平台提供商和基本权利具有重大影响。 聊天控制 1.0 允许在电子隐私规则的临时豁免下自愿扫描消息，而聊天控制 2.0 则提议强制扫描。扫描可通过客户端扫描或要求在加密系统中设置后门来实现。

hackernews · gasull · 7月7日 14:23 · [社区讨论](https://news.ycombinator.com/item?id=48818311)

**背景**: 聊天控制指的是欧盟针对在线儿童性虐待材料（CSAM）的立法努力。1.0 版为提供商自愿扫描提供了临时法律依据；2.0 版旨在建立永久性的强制制度。批评者认为这些提案威胁隐私、加密和民主监督。

**社区讨论**: 评论者普遍反对这些提案，将其描述为监控国家措施和对民主的威胁。一位评论者指出，即使在聊天控制 1.0 到期后，大型科技公司仍继续扫描消息而没有法律授权，突显出持续的隐私侵犯。

**标签**: `#privacy`, `#surveillance`, `#encryption`, `#EU legislation`, `#child safety`

---

<a id="item-8"></a>
## [sqlite-utils 4.0 发布，支持数据库模式迁移](https://simonwillison.net/2026/Jul/7/sqlite-utils-4/#atom-everything) ⭐️ 8.0/10

sqlite-utils 4.0 已发布，新增了数据库模式迁移、通过新 db.atomic() 方法实现的嵌套事务以及对复合外键的支持。 这一重大版本升级增加了管理 SQLite 模式演进的关键功能，使使用 sqlite-utils 进行数据库操作的开发者受益，尤其是在 Datasette 生态系统中。 迁移在 Python 文件中使用 sqlite-utils 库的 table.transform() 方法定义，该方法实现了 SQLite 推荐的创建新表、复制数据并重命名的模式。升级还包括升级指南中详述的破坏性变更。

rss · Simon Willison · 7月7日 19:32

**背景**: sqlite-utils 是一个命令行工具和 Python 库，用于创建、查询和转换 SQLite 数据库。4.0 版本是自 2020 年 3.0 以来的首个主要版本。在此之前，模式迁移需要手动或借助外部工具。新的迁移系统利用了库现有的 transform 功能。

**标签**: `#sqlite-utils`, `#database migrations`, `#SQLite`, `#Datasette`, `#Python`

---