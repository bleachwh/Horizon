---
layout: default
title: "Horizon Summary: 2026-10-30 (ZH)"
date: 2026-10-30
lang: zh
---

> 从 33 条内容中筛选出 8 条重要资讯。

---

1. [Cursor 市场上的篡改版 Claude Code 扩展植入攻击者 SSH 密钥](#item-1) ⭐️ 8.0/10
2. [Northflank 遭遇安全入侵，成为 as-a-service 厂商连环攻击的最新一例](#item-2) ⭐️ 8.0/10
3. [Nesformer 在约 1GB 的 Qwen 权重中塞进了一台可运行的 NES](#item-3) ⭐️ 8.0/10
4. [Azure 最薄弱环节：五起完整跨租户入侵](#item-4) ⭐️ 8.0/10
5. [DeepSeek 二轮融资 1055 亿元，估值超 6155 亿元](#item-5) ⭐️ 8.0/10
6. [Tangled 推出基于 AT Protocol 的联邦式代码托管平台](#item-6) ⭐️ 7.0/10
7. [AI 不会取代 SRE，而是在悄悄让其技能退化](#item-7) ⭐️ 7.0/10
8. [Reddit 帖文称友人伪造实验结果仍被 AAAI 录用，引发学术诚信争议](#item-8) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Cursor 市场上的篡改版 Claude Code 扩展植入攻击者 SSH 密钥](https://phorion.io/blog/offical-claude-code-vsx-compromise/) ⭐️ 8.0/10

一个被篡改的 Claude Code VS Code 扩展被发布到 Cursor 市场（内容同步自 Open VSX 注册表），该扩展会悄悄把一枚标记为 “svc-telemetry” 的攻击者 SSH 公钥追加到用户的 ~/.ssh/authorized_keys 文件中。Cursor 表示这个被恶意修改的扩展在周四太平洋时间约凌晨 2:27 至下午 1:35 期间存在于其市场上，而 Anthropic 声明通过其官方渠道分发的版本未受影响。 这是一起针对广泛使用的 AI 编程工具的供应链攻击：IDE 扩展以开发者自身权限运行，因此一个被污染的插件条目就可能让攻击者获得对开发者机器的持久化远程 shell 访问能力，并进而触及企业代码库和 CI 凭证。这也让人们对 Open VSX 等第三方扩展注册表（它们为 Cursor 这类替代市场提供内容）的安全审核机制产生质疑。 检测方法很直接：在 macOS 上运行 `grep -qs svc-telemetry ~/.ssh/authorized_keys`（Windows 上有对应命令）即可判断恶意密钥是否被写入，受影响的用户应从 authorized_keys 中删除该行。据 Anthropic 工程师 Felix Rieseberg 说明，被篡改的构建并非由 Anthropic 制作或发布，仅影响 Cursor 用户；不过社区成员指出，从公开报道来看，Open VSX 与微软官方 VS Code 市场之间的确切影响范围仍不清晰。

hackernews · _chall · 10月30日 07:09 · [社区讨论](https://news.ycombinator.com/item?id=50300683)

**背景**: Claude Code 是 Anthropic 推出的智能体式编程工具，可在终端运行并与 IDE 集成；与许多 AI 编程工具一样，它以 VS Code 扩展形式分发，而这类扩展本质上是一段由编辑器加载、以用户自身操作系统权限运行的 JavaScript 代码。Cursor 是一款面向 AI 的代码编辑器，拥有自己的插件市场，其扩展来源是 Open VSX 注册表而非微软专有的 VS Code 市场——这种设计扩大了分发渠道，但把信任转移到了一个审查相对薄弱的流水线上。~/.ssh/authorized_keys 文件列出了被允许通过 SSH 登录该机器的公钥，因此任何能把密钥追加进去的人，都能以该用户身份远程登录。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cursor.com/marketplace">Cursor Marketplace | Cursor Plugins</a></li>
<li><a href="https://superuser.com/questions/1667117/ssh-authorized-keys-file-location-and-permissions">ssh authorized _ keys file location and permissions - Super User</a></li>
<li><a href="https://github.com/anthropics/claude-code">GitHub - anthropics/ claude - code : Claude Code is an agentic coding ...</a></li>

</ul>
</details>

**社区讨论**: 评论者主要围绕责任归属和实际处置展开讨论：一位 Anthropic 工程师澄清此事属于 Cursor 市场发布环节被入侵，而非 Anthropic 系统被攻破；用户转发了检测与清理命令；也有人引用了路透社关于约 11 小时暴露窗口的时间线。整体情绪对影响范围说明不清表示不满，多位读者质疑为何没有更醒目地附上详细描述 SSH 密钥植入机制的 Phorion 原始报道。

**标签**: `#security`, `#supply-chain-attack`, `#claude-code`, `#cursor-marketplace`, `#vs-code-extension`

---

<a id="item-2"></a>
## [Northflank 遭遇安全入侵，成为 as-a-service 厂商连环攻击的最新一例](https://status.northflank.com/) ⭐️ 8.0/10

多租户平台即服务（PaaS）提供商 Northflank 通过其状态页面披露了一起安全入侵事件，成为近期一系列针对 as-a-service 厂商的攻击中的最新一例。Hacker News 的评论者统计称，仅自 9 月以来就至少发生了六起快节奏攻击，涉及 PingCAP/TiDB、Fireworks AI、Zeabur、OpenCode Console、Railway，如今又加上 Northflank。 多起入侵密集出现，说明这可能是一场针对中小型基础设施厂商的系统性攻击活动，而非孤立事件，这可能促使企业客户重新回流到安全保证更强的超大规模云厂商。任何在托管平台上部署工作负载或存放密钥的人，都应重新评估自己对服务商的信任程度。 评论者指出，在 Northflank 这起事件中，攻击者似乎并未接触到客户的代码和二进制文件；但一位开发者认为真正的暴露面仍是环境变量中的密钥，并介绍了自己的做法：加密环境变量，再把解密密钥硬编码进自己的二进制文件中，作为一种实用的缓解手段。也有人警告技术防御可能越来越难以招架，认为行为安全、零信任以及刻意增加的摩擦将是未来的方向。

hackernews · js4ever · 10月30日 15:10 · [社区讨论](https://news.ycombinator.com/item?id=50305025)

**背景**: Northflank 是一个“开发者优先”的 PaaS，既保留了托管平台的简洁性，又具备 Kubernetes 的灵活性，团队可以在它的托管云、客户自有云账户或受支持的 Kubernetes 集群上部署工作负载。多租户是 PaaS 模式的核心，意味着众多客户的工作负载与密钥运行在共享基础设施之上，因此租户隔离与密钥管理成为关键的安全边界。历史经验表明，厂商被入侵是数据泄露的重要来源：第三方与供应链事件在数据泄露中占比很高，而且一旦厂商被攻破，其持有的凭据、密钥和令牌都应被视为永久泄露。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://northflank.com/blog/what-is-paas-hosting">What is PaaS hosting? Benefits and how it works | Blog — Northflank</a></li>
<li><a href="https://northflank.com/blog/best-paas-for-enterprises">Best PaaS for enterprises in 2026 | Blog — Northflank</a></li>
<li><a href="https://www.datafence.ai/blog/supply-chain-security-vendor-breaches">Supply Chain Security: The Vendor Breach Threat</a></li>

</ul>
</details>

**社区讨论**: 这条获得 325 分、243 条评论的讨论把该事件视为一场全行业的信息安全紧急状况，而非普通的八卦：有评论者呼吁，任何运行类 SaaS 工作负载的团队都应因此警醒。一种反复出现的观点是，基础设施初创公司会在企业订单上输给超大规模云厂商，因为“再好用的体验也替代不了安全性”；另一些人则在讨论一个技术安全不再可行的未来，防御将转向行为控制与刻意的减速机制。也有读者只是问了一句“Northflank 是什么”，这本身就说明该领域涌入的新厂商之多。

**标签**: `#security-breach`, `#cloud-infrastructure`, `#PaaS`, `#multi-tenancy`, `#vendor-trust`

---

<a id="item-3"></a>
## [Nesformer 在约 1GB 的 Qwen 权重中塞进了一台可运行的 NES](https://github.com/dbreunig/nesformer) ⭐️ 8.0/10

开发者 Drew Breunig 发布了名为 "nesformer" 的项目，把一台可运行的任天堂娱乐系统（NES）——包括 6502 CPU 和内存——编码进了约 1GB 的 Qwen3.5 模型权重之中，而不是写成普通程序。据作者所说，这些权重与配套代码是由 Anthropic 的 Opus 5.5 仅凭两条提示词生成的：一条指向早前的 "qwenputer" 文章，另一条则询问能否用同样的技巧来模拟 NES 硬件。 该项目是一个极具冲击力的概念验证：神经网络权重可以充当通用的计算基底，承载解释器或虚拟机，而不只是用来预测文本。它同时为「基于大模型的计算」与确定性程序之间在速度和能耗上的差距，提供了一个具体且可量化的参照。 据报道，该模拟器的运行速度比真实 NES 硬件慢 150–290 倍；内存状态并非放在外部缓冲区，而是借助 gated DeltaNet 一类的架构保存在模型内部。它严格来说只是一个实验性演示——并不能真的用来玩游戏——但确实能够端到端地启动真实 ROM。

hackernews · dbreunig · 10月30日 16:40 · [社区讨论](https://news.ycombinator.com/item?id=50306442)

**背景**: Qwen 是阿里巴巴的开源权重大模型系列，其参数张量通常只用于预测下一个 token。从原理上说，Transformer 的注意力和 MLP 层是通用函数逼近器，因此已有研究者尝试训练它们复现 WebAssembly 之类虚拟机的状态转移。NES 模拟之所以是这类实验的经典小目标，是因为该主机的 Ricoh 2A03（一枚 6502 内核）和内存映射简单且文档完备，爱好者早已在软件和 MiSTer 这类 FPGA 上重新实现过它。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.machucavalley.tech/blog/nintendo-nes-qwen-weights-nesformer/">Ghost in the Machine: A Nintendo NES Now Lives Inside LLM ...</a></li>
<li><a href="https://www.zenteck.com.br/en/blog/can-you-play-super-mario-inside-llm-weights-meet-nesformer">Play NES Inside AI Weights with Nesformer — Zenteck</a></li>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论区热情高涨但也保持清醒：armcat 认为该技术有朝一日能把小型虚拟机——Python 解释器、shell、sed、grep——直接编译进模型权重，让工具调用通过矩阵乘法完成，而非缓慢的自回归 token 输出。pbohun 强调了它与普通程序之间巨大的算力差距，jacquesm 则称这个 hack 令人愉快，但从效率角度看相当可怕。cafebeen 则对内存（而非仅仅是 CPU）也在权重内部被模拟感到意外。

**标签**: `#LLM`, `#emulation`, `#Nintendo Entertainment System`, `#model weights`, `#AI-assisted coding`

---

<a id="item-4"></a>
## [Azure 最薄弱环节：五起完整跨租户入侵](https://www.binarysecurity.no/posts/2026/10/one-root-case) ⭐️ 8.0/10

Binary Security 的一名研究员发布详细报告，披露了五个可导致 Microsoft Azure 完整跨租户入侵的不同漏洞，并引发了对云隔离机制和微软披露处理方式的担忧。 跨租户隔离是公有云的基础安全承诺；一旦漏洞允许一个客户访问另一个租户的资源，就可能影响任何 Azure 客户，并削弱对微软云边界控制的信任。 据披露，这些问题属于不安全的直接对象引用（IDOR）和路径遍历等反复出现的漏洞类别，报告还建议通过为资源名称增加随机性来缓解。社区讨论还提到，当攻击者知道另一个租户的 ID 时，adminconsent 回调可被伪造，并指出微软文档警告不要使用租户 ID 参数进行身份验证。

hackernews · swq115 · 10月30日 10:06 · [社区讨论](https://news.ycombinator.com/item?id=50301854)

**背景**: Microsoft Azure 将客户组织为租户，Microsoft Entra ID 与 Azure 基于角色的访问控制负责在组织之间实施租户级隔离。B2B 协作等跨租户访问功能提供受控共享，但其底层隔离模型假定一个租户不能直接访问另一个租户的资源。IDOR 是一种访问控制漏洞：应用程序暴露出内部对象引用（如数据库键或资源 ID），却没有验证请求者是否有权访问该对象。路径遍历是一种相关的 Web 漏洞，攻击者通过构造文件路径逃逸出预期目录或资源边界。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/azure/security/fundamentals/isolation-choices">Isolation in the Azure public cloud | Microsoft Learn</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/Security/Attacks/IDOR">Insecure Direct Object Reference (IDOR) - Security | MDN</a></li>
<li><a href="https://docs.azure.cn/en-us/entra/external-id/cross-tenant-access-overview">Cross-tenant access overview | Azure Docs</a></li>

</ul>
</details>

**社区讨论**: 评论者对这项研究表示敬佩，但对 Azure 的跨租户安全记录提出尖锐批评，有人称 Azure 在跨租户泄露方面“远超”竞争对手，也有人质疑企业为何仍选择它。多位评论者聚焦微软的应对，批评文档警告和为资源名称增加随机性属于薄弱或“安全靠隐蔽”的缓解措施。还有讨论希望给提交内容标注日期，因为如今漏洞披露显得接连不断。

**标签**: `#Azure`, `#cloud security`, `#vulnerability research`, `#cross-tenant`, `#IDOR`

---

<a id="item-5"></a>
## [DeepSeek 二轮融资 1055 亿元，估值超 6155 亿元](https://www.theinformation.com/articles/behind-deepseeks-16-billion-funding-chinese-tech-titans-state-players) ⭐️ 8.0/10

据 The Information 披露，DeepSeek（深度求索）完成第二轮融资，规模约 1055 亿元人民币（约合 158 亿美元），投后估值突破 6155 亿元，近 30 家投资方参与。其中腾讯出资 100 亿元，宁德时代及董事长曾毓群合计出资 100 亿元，长鑫存储、中芯国际、美团、vivo、小红书等也出现在投资方名单中。 这是中国 AI 领域迄今规模最大的私募融资之一，说明 DeepSeek 已从一家初创公司升级为国家战略级资产，并把大型科技公司与半导体企业一并拉入股东阵营。国资背景资金占比从首轮的约 2% 跃升至本轮的约 27%，表明在美国出口管制和与 OpenAI、Anthropic 竞争加剧的背景下，中国正有意把资源集中扶持一家本土前沿模型领军者。 1055 亿元这一数字来自多轮调整：本轮募资目标最初定为 500 亿元，后上调至约 1000 亿元，而今年 6 月完成的首轮融资规模约为 510 亿元。投资方既包括互联网平台（腾讯、美团、vivo、小红书），也包括半导体产业链企业（中芯国际、存储厂商长鑫存储），后者可能关系到 DeepSeek 获取算力与内存资源的能力。

telegram · zaihuapd · 10月30日 12:37

**背景**: DeepSeek（深度求索）是一家位于杭州的人工智能与大语言模型公司，脱胎于 2015 年由浙江大学工程师创立的量化对冲基金幻方量化，因以异常低的训练成本发布高性能开放权重模型而为全球所知。长鑫存储是中国领先的国产 DRAM 内存制造商，中芯国际则是中国最大的晶圆代工厂，二者都是中国推动半导体自主可控的核心力量，因此它们出现在 AI 融资名单中颇具象征意义。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finance.sina.com.cn/tech/roll/2026-10-30/doc-iniwywtu2232220.shtml">消息称DeepSeek二轮融资1055亿元 估值已突破6155亿元</a></li>
<li><a href="https://news.qq.com/rain/a/20261030A08Y1300">DeepSeek 第二轮融资1055亿元 估值6155亿元_腾讯新闻</a></li>
<li><a href="https://zh.wikipedia.org/wiki/深度求索">深度求索 - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AI funding`, `#China tech`, `#state investment`, `#AI industry`

---

<a id="item-6"></a>
## [Tangled 推出基于 AT Protocol 的联邦式代码托管平台](https://tangled.org/blog/forge/) ⭐️ 7.0/10

Tangled 发布博客文章，宣布以“首个真正联邦化的代码托管平台”的定位重新出发：AT Protocol 的 lexicon 已经稳定，整体架构与界面全面重做，用户既可以自托管整套服务，也可以只托管其中一部分（例如 Git 托管或 CI runner）。团队还上线了组织（organizations）支持，并表示私有仓库将在接下来的一两周内推出。 在 GitHub 等中心化平台主导代码托管的当下，一个允许开发者自建服务器、同时又能与其他实例上的开发者无缝协作的平台，为摆脱平台锁定和单点故障提供了现实可行的出路。由于基于 AT Protocol，用户可以用 Bluesky 账号登录并直接继承已有的社交关系图谱，这使得项目和开发者的发现与关注比孤立的自托管平台容易得多。 公告强调了一种务实的“按需采用”模式：你可以只自托管想要的部分，比如 Git 托管或 CI runner，也可以托管包括 API 服务器和前端界面在内的全部组件。联合创始人确认 lexicon 已最终定稿，但有评论者追问 issue、pull request 和 comment 记录是否已从用户作用域移到仓库作用域——对于任何想构建可互操作平台或镜像的人来说，这是个关键细节。

hackernews · zlliang · 10月30日 15:44 · [社区讨论](https://news.ycombinator.com/item?id=50305573)

**背景**: 代码托管平台（code forge）指的是 GitHub、GitLab 这类把 Git 仓库托管与 issue、pull request、代码审查、CI 结合在一起的服务。“联邦化”意味着服务不依赖单一中心服务器：众多独立运营的实例通过共享协议互联互通，就像电子邮件或 Mastodon 那样。Tangled 构建在 AT Protocol（ATProto）之上，这是 Bluesky 背后的开放、由 schema 驱动的标准，把可自验证的记录存储在个人数据服务器上，从而实现可迁移的身份与数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tangled.org/blog/forge/">The federated code forge · The Tangled Blog</a></li>
<li><a href="https://nordictech.news/p/tangled-eur-3-8m-federated-github-alternative">Tangled Raises EUR 3.8M to Build a Federated GitHub Rival</a></li>
<li><a href="https://atproto.com/guides/overview">Protocol Overview - AT Protocol</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论整体热情积极，联合创始人亲自答疑，有用户表示打算把项目从 Gitea 迁到 Tangled，只保留 GitHub 用于曝光和备份。也有人提出界面批评，认为首页时间线信息过于密集，并建议把个人主页的活动图表简化成 GitHub 那种用户熟悉的贡献方格；还有评论指出 Tangled 已融资 380 万欧元，另有人询问仓库作用域下的记录问题，以便让自己开发的平台与之互操作。

**标签**: `#federated code hosting`, `#Git`, `#AT Protocol`, `#self-hosting`, `#developer tools`

---

<a id="item-7"></a>
## [AI 不会取代 SRE，而是在悄悄让其技能退化](https://newsletter.signoz.io/p/ai-isnt-replacing-sres-its-deskilling) ⭐️ 7.0/10

SigNoz 的一篇通讯文章指出，AI 对站点可靠性工程（SRE）的真正威胁并非取代岗位，而是“去技能化”——即侵蚀让 SRE 得以有效工作的深层系统理解能力。文章建议，SRE 团队可以像美国联邦航空管理局（FAA）要求飞行员保持手动飞行时长那样，把某些故障演练指定为“人工练习”机会，即便 AI 完全有能力处理。 如果工程师越来越多地把调试与故障响应交给 AI 智能体，团队可能会丧失诊断新型故障、以及理解“没人真正弄懂的系统”所需的隐性知识。这会影响每一家采用 AIOps 式自动化运维的组织，也引发了一个问题：可靠性技能应当如何被保留和培养。 文章借用了航空自动驾驶的类比，指出监管机构至今仍强制要求手动飞行时长，正是因为自动化会侵蚀实操技能；同时认为由 AI 构建的系统在出问题时尤其难以推理排查。需要说明的是，这是一篇观点文章而非研究论文，其论断主要建立在类比与轶事之上，而非对技能退化的量化证据。

hackernews · dorianniemiec · 10月30日 15:52 · [社区讨论](https://news.ycombinator.com/item?id=50305693)

**背景**: 站点可靠性工程（SRE）是由 Google 开创的一门学科，软件工程师负责保障大型服务的可用性与性能，常见实践包括服务水平指标（SLI）、服务水平目标（SLO）、错误预算以及无责复盘。AIOps 指把人工智能、机器学习和大数据分析应用于监控、异常检测、自动化修复等 IT 运维任务。而“去技能化”是一个更早的经济学概念，描述新技术的引入如何侵蚀操作者的专业技能知识。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Site_reliability_engineering">Site reliability engineering - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/AIOps">AIOps - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Deskilling">Deskilling - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同航空类比很贴切，有人指出航空业用了几十年研究如何在自动化程度提高的同时避免人为失误。也有人提出反驳：一位工程师表示 Claude 在 AWS 调试上已强于自己、速度快约 10 倍；另一位认为 Terraform 早已让基础设施工作去技能化，重点应放在用 AI 冲刺“五个九”的可用性而非保留手工技能；还有怀疑者坚持认为，AI 生成的应用根本谈不上真正的理解。

**标签**: `#SRE`, `#AI/ML`, `#DevOps`, `#automation`, `#skill-desksilling`

---

<a id="item-8"></a>
## [Reddit 帖文称友人伪造实验结果仍被 AAAI 录用，引发学术诚信争议](https://www.reddit.com/r/MachineLearning/comments/1xj8tvc/freind_of_mine_published_a_paper_with_fabricated/) ⭐️ 7.0/10

一位 Reddit 用户在 r/MachineLearning 发帖称，其朋友在做差距分析（gap analysis）项目时发现自己的结果不如原论文亮眼，于是直接编造并抬高了指标数据，而这篇论文竟然被 AAAI 录用。发帖者表示自己曾与另外两人辛苦完成一篇优化方向的论文并被 ACL 接收，但看到造假论文进入他心目中更“高级”的会议后感到极度愤怒。 这篇帖文之所以引发共鸣，是因为它暗示顶级 AI 会议的同行评审可能无法识别赤裸裸的数据造假，从而动摇人们对已发表基准结果的信任，也动摇会议作为博士生录取与招聘“信用背书”的作用。即便它只是一则未经证实的轶事，也助长了关于机器学习研究可复现性、审稿人超负荷与激励机制的持续讨论。 帖文没有给出论文标题、作者姓名、投稿年份或具体被篡改的指标，也没有任何独立渠道核实该说法——整件事只是单个 Reddit 用户的二手叙述。此外，帖文把同行评审与数据审计混为一谈：审稿人通常只看到 PDF，而非原始代码或实验日志，而正式的复现性检查在 AI 会议上往往稀少且多为自愿性质。

reddit · r/MachineLearning · /u/Tonka-Jahari-Pizza · 10月30日 07:25

**背景**: AAAI 是历史最悠久、最具影响力的 AI 会议之一，首届于 1980 年在斯坦福举办，在 Google Scholar 的 H5 指数排名中与 NeurIPS、ICML、ICLR 同处 AI 刊物的第一梯队，并同样使用自动化系统为论文分配审稿人。ACL 则是计算语言学协会的旗舰会议，也是自然语言处理领域的主会场。这类会议的同行评审通常采用单盲或双盲、由志愿者承担，审稿人依据论文文本判断结论，而不会重跑实验。按通行的学术诚信规范，编造或篡改结果属于明确的研究不端行为，但其发现通常依赖发表后的审查、举报或复现失败，而非评审环节本身。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AAAI_Conference_on_Artificial_Intelligence">AAAI Conference on Artificial Intelligence</a></li>
<li><a href="https://grokipedia.com/page/AAAI_Conference_on_Artificial_Intelligence">AAAI Conference on Artificial Intelligence</a></li>

</ul>
</details>

**标签**: `#academic integrity`, `#peer review`, `#research misconduct`, `#machine learning conferences`, `#reproducibility`

---