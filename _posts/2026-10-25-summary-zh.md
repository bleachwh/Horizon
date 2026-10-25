---
layout: default
title: "Horizon Summary: 2026-10-25 (ZH)"
date: 2026-10-25
lang: zh
---

> 从 27 条内容中筛选出 8 条重要资讯。

---

1. [十年前的 CNN 在皮肤癌诊断上击败前沿大模型](#item-1) ⭐️ 8.0/10
2. [PHP 紧急修复两项严重未授权远程代码执行漏洞，敦促用户立即升级](#item-2) ⭐️ 8.0/10
3. [Cerebras 详解如何在 WSE-3 晶圆上运行万亿参数模型推理](#item-3) ⭐️ 7.0/10
4. [苹果将于周三发布首款触屏 MacBook Pro](#item-4) ⭐️ 7.0/10
5. [俄勒冈警方对一名警员记录开价 250 万美元](#item-5) ⭐️ 6.0/10
6. [FOSDEM 演讲“我拒绝接受被审查的互联网”引发热议](#item-6) ⭐️ 6.0/10
7. [AI 的使用让加州大学伯克利分校数学教授认为批改作业“毫无意义”](#item-7) ⭐️ 6.0/10
8. [fheroes2：用 C++ 开源重制《魔法门之英雄无敌 II》游戏引擎](#item-8) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [十年前的 CNN 在皮肤癌诊断上击败前沿大模型](https://lynchlab.net/llm-skin-cancer) ⭐️ 8.0/10

Lynch Lab 的一篇博文称，一个大约诞生于 2015 年的 Inception v3 卷积神经网络，在 ISIC Archive 的 68,011 张皮肤镜与临床图像上微调后，在 200 个病灶的测试集上识别皮肤病变的表现优于两个前沿大语言模型。作者在单块 H100 GPU 上微调了全部层，并在评估前从训练集和验证集中剔除了所有测试病灶及其同一患者的图像。 这一结果推动了当前的一场争论：对于医学图像分类这类狭窄而高风险的专门任务，通用前沿大模型究竟是不是合适的工具，还是小而专的模型依然更强、成本也低得多。它同时也引出了比较方法本身的问题——针对某一狭窄标签集调优的基准测试，未必能反映真实的临床价值。 该网络从基于日常照片的 ImageNet 预训练权重出发，被适配到一个约十余个皮肤科类别的狭窄标签预测任务上，且仅在 200 个留出病灶上评估。Hacker News 上的批评者认为这套设置本质上属于“刷榜”（benchmaxxing），因为一个专门拟合该标签集的模型，几乎必然会战胜一个把这个任务视为训练语料中沧海一粟的通用大模型。

hackernews · sungam · 10月25日 17:15 · [社区讨论](https://news.ycombinator.com/item?id=50233779)

**背景**: 卷积神经网络（CNN）是一种面向图像等网格状数据的深度学习架构，其共享的卷积滤波器在输入上滑动以检测边缘、纹理等特征，长期是计算机视觉与医学图像分析领域事实上的标准方案。前沿大语言模型则是在语言及相关模态上处于规模与能力前沿的生成式模型，参数量通常高达数百亿，且训练数据广泛而通用。ISIC Archive 是一个大型公开的皮肤镜与临床皮肤图像集合，被广泛用于训练和评测皮肤病变分类器，例如谷歌在 2015 年发布的 CNN 架构 Inception v3。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Convolutional_neural_network">Convolutional neural network</a></li>
<li><a href="https://www.emergentmind.com/topics/frontier-large-language-models-llms">Frontier Large Language Models - emergentmind.com</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者大多并不意外，他们认为任何规模化应用都应采用架构合适的专用分类器，准确性会更高，而大语言模型最大的价值在于把构建这类专用模型的成本降到接近于零。也有不少人批评这项对比过于以基准为中心：一位曾开发出排行榜第一模型的评论者指出，一个针对狭窄标签任务专门拟合的简单模型胜出毫不奇怪，并质疑为何不去适配谷歌 MedSigLIP 这类开放权重的医学图像-文本嵌入模型；还有人把这一结果比作计算器在算术上击败大模型。

**标签**: `#machine learning`, `#medical AI`, `#LLMs`, `#CNNs`, `#benchmark evaluation`

---

<a id="item-2"></a>
## [PHP 紧急修复两项严重未授权远程代码执行漏洞，敦促用户立即升级](https://t.me/zaihuapd/44678) ⭐️ 8.0/10

PHP 团队发布紧急安全更新，修复两项严重漏洞，攻击者可无需任何登录认证即远程执行任意代码，两项漏洞的 CVSS 4.0 评分均为 9.2 分。官方敦促用户立即升级到 PHP 8.5.12、8.4.27、8.3.36 或 8.2.35。 这些漏洞几乎影响所有处理网页请求的 PHP 部署方式，因此在完成修补之前，互联网上大量服务端基础设施都处于暴露状态。由于利用漏洞无需任何凭据，任何面向公网的 PHP 站点或应用都可能成为攻击目标，打补丁已成为必须立刻执行的运维优先事项。 公告涉及的部署方式包括 PHP-FPM、Apache 的 mod_php、php-cgi、FrankenPHP 和 LiteSpeed，其中 mod_php 风险最高，因为已有验证表明攻击可在网站自身的业务代码运行之前就被触发。这一“先于应用执行”的触发点意味着常规的应用层防护可能根本没有机会检查恶意请求。

telegram · zaihuapd · 10月25日 02:42

**背景**: PHP 是一种服务端脚本语言，驱动着互联网上很大一部分网站，它通过若干被称为 SAPI 的不同接口运行在 Web 服务器之中。PHP-FPM 是常与 Nginx 等服务器配合使用的 FastCGI 进程管理器，mod_php 把解释器直接嵌入 Apache，php-cgi 是较老的 CGI 可执行程序，FrankenPHP 是基于 Caddy 构建、内嵌官方 PHP 解释器的新式 Go 应用服务器，LiteSpeed 则使用自家的 PHP 集成方式。CVSS 4.0 是通用漏洞评分系统的最新版本，9.2 的基线分数属于“严重”级别；而“未授权远程代码执行”意味着攻击者不需要任何账号或登录，就能在服务器上运行自己的代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PHP-FPM">PHP-FPM</a></li>
<li><a href="https://grokipedia.com/page/FrankenPHP">FrankenPHP</a></li>
<li><a href="https://www.linkedin.com/pulse/cvss-40-whats-new-mend-io">CVSS 4 . 0 — What’s New?</a></li>

</ul>
</details>

**标签**: `#security`, `#php`, `#vulnerability`, `#rce`, `#patching`

---

<a id="item-3"></a>
## [Cerebras 详解如何在 WSE-3 晶圆上运行万亿参数模型推理](https://www.cerebras.ai/blog/how-we-deploy-trillion-parameter-frontier-models-on-cerebras) ⭐️ 7.0/10

在 10 月 22 日发布的一篇工程博客中，Cerebras 详细介绍了如何将万亿参数级别的前沿模型映射到其第三代晶圆级引擎 WSE-3T 上，并以一个横跨 59 片晶圆的示例部署说明其可稳定达到约每秒 1000 至 2000+个 token 的推理速度。这是该公司首次公开、系统地解释如何把远超单片晶圆片上内存容量的超大模型切分并跨晶圆流式运行。 这篇文章正面回应了外界对晶圆级推理最常见的质疑——单片晶圆的片上 SRAM 根本装不下万亿参数模型——并把讨论焦点从“单芯片内存”转向“多晶圆横向扩展”。如果所宣称的吞吐量在生产负载下依然成立，那么对于对延迟敏感的前沿模型服务场景，企业就多了一个相对 GPU 集群的可信替代方案，而这也正是 Cerebras 试图与英伟达、Groq 形成差异化的方向。 59 片晶圆的配置只是示例性说明，并非固定的产品规格；Cerebras 也提示，相对于 GPU 系统的实测加速幅度会因工作负载、配置、测试日期和所用模型而异，这意味着文中亮眼的 token 速率属于厂商自报的最佳情况。该方案依赖对模型权重进行切分并在晶圆之间流式传输激活值，因此真正的瓶颈并非原始算力，而是互连带宽与晶圆间的调度效率。

hackernews · gmays · 10月25日 01:33 · [社区讨论](https://news.ycombinator.com/item?id=50227356)

**背景**: Cerebras 研发的晶圆级引擎（Wafer-Scale Engine）不把晶圆切割成众多小芯片，而是让整片 300 毫米硅晶圆作为一颗芯片工作；当前的 WSE-3 系列在 5 纳米工艺上集成了约 4 万亿个晶体管、超过 90 万个计算核心，算力约 250 千万亿次浮点运算，并采用“就地失效”设计，绕过有缺陷的核心而不是整片报废。由于全部算力位于同一块硅片上，核心之间的内存带宽远高于 GPU 集群，这正是 Cerebras 主张晶圆级硬件能突破制约大模型推理的“内存墙”的原因。而参数规模达到万亿级的模型无法装进任何单片晶圆的片上内存，因此必须把模型分散到多片晶圆上——这篇博客讲的正是这件事。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cerebras.ai/blog/how-we-deploy-trillion-parameter-frontier-models-on-cerebras">How Cerebras Deploys Trillion-Parameter AI Models</a></li>
<li><a href="https://www.cerebras.ai/chip">Cerebras WSE-3 Turbo | Wafer - Scale AI Chip</a></li>
<li><a href="https://www.remio.ai/post/cerebras-deploys-trillion-parameter-ai-models-across-wafers-shifting-the-inferen">Cerebras Deploys Trillion-Parameter AI Models Across Wafers ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论呈现分歧：不少人称赞 Cerebras 硬件的原始速度，但抱怨公众可用的模型目录（如 GPT-OSS-120B、Qwen 27B）远未达到前沿水准，一位有过合作经历的用户甚至评价该公司“技术惊艳、团队却令人费解地不给力”。也有人担忧产能问题，认为 Cerebras 既造不出足够多的巨型晶圆节点，也没有 OpenAI 那样的资金规模，因此只能推出廉价“尝鲜”套餐而无法真正扩容；此外还有评论就数据如何在二维处理单元网格中流动提出了技术疑问。

**标签**: `#Cerebras`, `#AI infrastructure`, `#LLM inference`, `#wafer-scale computing`, `#model deployment`

---

<a id="item-4"></a>
## [苹果将于周三发布首款触屏 MacBook Pro](https://www.bloomberg.com/news/newsletters/2026-10-25/apple-to-unveil-touch-screen-macbook-pro-executive-promotions-in-box-checker) ⭐️ 7.0/10

据报道，苹果将于本周三推出其史上首款触屏 MacBook Pro，这是 Mac 首次支持触摸输入并采用 OLED 屏幕，同时加入灵动岛设计，提供 14 英寸与 16 英寸两个版本。售价预计将高于现款 2499 美元的起售价。 这推翻了苹果长期以来“笔记本不应配备触屏”的立场——高管们多年来以人体工学为由坚持这一观点；同时也意味着其旗舰笔记本产品线将围绕两项此前专属于 iPhone 和 iPad 的特性重新定义。这一转变显示苹果更愿意反思和调整自身做法，而非一味强推行业跟随自己，也将对已经推出 OLED 触屏产品的 Windows 笔记本厂商形成压力。 据报道，触控将作为键盘和触控板的补充而非替代方案，而此次立场转变的动因被描述为更多出于营收与营销考量，而非新的人体工学突破。OLED 面板和灵动岛都是 Mac 上的首次应用，但该消息未披露刷新率、亮度等具体参数，也未说明屏幕是否支持类 Apple Pencil 的手写笔。

telegram · zaihuapd · 10月25日 14:25

**背景**: OLED（有机发光二极管）屏幕的像素自身发光，无需依赖背光，因此单个像素可以完全熄灭，从而呈现真正的黑色和极高的对比度；OLED 早已是 iPhone 和 iPad Pro 的标配，但从未应用于 Mac。灵动岛是近年 iPhone 顶部容纳前置摄像头与传感器的药丸形区域，可通过软件扩展以显示计时器、媒体播放等实时活动。苹果历来反对在 Mac 上加入触控，公司高层长期认为伸手去触摸竖直的笔记本屏幕在人体工学上很别扭。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OLED">OLED - Wikipedia</a></li>
<li><a href="https://www.cnet.com/tech/mobile/iphone-14-pro-max-review-welcome-apples-dynamic-island/">iPhone 14 Pro and 14 Pro Max Review: Welcome to Apple 's Dynamic ...</a></li>

</ul>
</details>

**标签**: `#Apple`, `#MacBook Pro`, `#touchscreen`, `#OLED`, `#consumer tech`

---

<a id="item-5"></a>
## [俄勒冈警方对一名警员记录开价 250 万美元](https://theintercept.com/2026/10/01/oregon-police-misconduct-public-records-cost-fee/) ⭐️ 6.0/10

据 The Intercept 报道，俄勒冈州尤金市警察局告知一家当地新闻机构，处理其针对一名警员的公共记录申请至少需要 44,816 个工时，费用约为 2,484,599.04 美元。约 250 万美元的报价被视为利用费用阻碍警方问责记录公开的极端案例。 高得令人望而却步的费用估算和缓慢、零散的记录发布，可能使公共记录法在实际中无法使用，从而让警察部门逃避新闻监督和公众问责。这一案例也呼应了美国及海外围绕政府机构如何定价、如何控制信息获取节奏的更广泛透明度争议。 44,816 个工时相当于一名全职员工工作约 21.5 年；俄勒冈州公共记录法允许政府机构收回处理申请的“实际成本”，但没有对费用设定明确上限。该州还要求机构在五个工作日内确认收到申请，但允许对大量记录申请进行延期，因此及时确认并不等于会及时提供记录。

hackernews · tdeck · 10月25日 18:04 · [社区讨论](https://news.ycombinator.com/item?id=50234232)

**背景**: 《信息自由法》（FOIA）是美国联邦层面的透明度法律，但它不适用于市警察局；市警察局的记录受州法律管辖，例如俄勒冈州公共记录法（ORS 192.410 至 192.505）。俄勒冈州法律要求机构在五个工作日内确认收到申请，允许对大量记录申请延期，并允许机构收取处理申请的实际成本。由于这些收费没有硬性上限，极高的费用估算实际上可能等同于拒绝申请，除非申请者付费、协商或提出挑战。透明度倡导者长期认为，收费和分批发布常被用来拖延或劝退记录申请。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.smarsh.com/blog/regulations/oregon-public-records-law/">Oregon Public Records Law Requests and Compliance | Smarsh</a></li>
<li><a href="https://www.investigatewest.org/redacted-y2k-bites-oregon-public-records-law/">Redacted: Y2K bites Oregon Public Records Law</a></li>
<li><a href="https://insideinvestigator.org/foia-the-ongoing-fight-for-freedom-of-information/">FOIA : The Ongoing Fight for Freedom of Information</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为这一费用荒谬至极，有人计算 44,816 小时约等于 21 年的工作量，还有人分享了类似经历：机构通过每月发布少量记录来拖延申请。一位德国评论者警告说，包括延斯·施潘在内的政客正推动在德国版 FOIA 中允许这种 prohibitive 收费并缩小获取范围；一位英国评论者则拿英国法定的 30 天答复期限与美国的情况作对比。

**标签**: `#public-records`, `#FOIA`, `#government-transparency`, `#press-freedom`, `#police-accountability`

---

<a id="item-6"></a>
## [FOSDEM 演讲“我拒绝接受被审查的互联网”引发热议](https://talkweb.eu/openweb/4558/) ⭐️ 6.0/10

talkweb.eu 发布了一篇题为“我拒绝接受被审查的互联网，来 FOSDEM 27 与我同行”的演讲预告，号召开源社区参加这场 FOSDEM 演讲，主张不应把“被审查的互联网”当作可接受的默认状态。该帖在 Hacker News 上获得约 300 分和 160 条评论，使一则会议预告演变成关于抗审查网络建设的广泛讨论。 这场讨论表明，尽管主流舆论越来越把平台、企业和国家的网络过滤视为常态，抗审查对开发者和用户而言仍是切身议题。FOSDEM 是欧洲规模庞大且非商业化的开源聚会，这样一场演讲能把该议题直接摆在那些构建相关协议与工具的维护者面前。 该帖本身只是一则演讲预告而非技术论文，因此并未详细说明所提议的机制；讨论更多地聚焦于现实障碍，例如绕过审查的流量仍然要经过审查方和运营商所控制的基础设施。也有参与者指出颇具讽刺意味的实际体验，一位评论者称该页面本身一直卡在“请稍候，正在验证您的请求”的机器人校验上。

hackernews · Tomte · 10月25日 17:30 · [社区讨论](https://news.ycombinator.com/item?id=50233929)

**背景**: FOSDEM（欧洲自由及开源软件开发者会议）是一年一度在布鲁塞尔冬末举办、由志愿者组织、非商业化的软件会议，以技术内容密集、缺少厂商推销环节而著称。抗审查网络指的是 Tor 以及相关覆盖网络、隐蔽信道等系统，它们力求在网络运营方封锁或检测流量时仍保持通信畅通；该领域的研究（如“互联网审查文献目录”这类资源所收录的成果）专门分析审查者如何过滤流量，以及规避工具如何绕开这些过滤。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/FOSDEM">FOSDEM - Wikipedia</a></li>
<li><a href="https://censorbib.nymity.ch/">The Internet censorship bibliography</a></li>
<li><a href="https://link.springer.com/chapter/10.1007/978-3-319-08506-7_1">CloudTransport: Using Cloud Storage for Censorship - Resistant ...</a></li>

</ul>
</details>

**社区讨论**: 整体情绪偏向同情，但对可行性意见分歧：多位评论者认为审查难以避免，甚至认为只要符合自身政治立场，多数用户其实是欢迎审查的，而且仅靠软件无法对抗那些能被收买配合的基础设施所有者。另一些人则称赞 FOSDEM 的技术深度和少有推销色彩，还有一位开发者提到自己发起的 VPN 项目 Mother of all VPNs，作为对伊朗等地互联网断网的实际回应。

**标签**: `#internet-censorship`, `#fosdem`, `#privacy`, `#network-freedom`, `#community-discussion`

---

<a id="item-7"></a>
## [AI 的使用让加州大学伯克利分校数学教授认为批改作业“毫无意义”](https://www.dailycal.org/news/campus/academics/ai-use-leads-uc-berkeley-math-professor-to-see-no-point-in-grading-homework/article_bdf1eae2-c08b-491f-b9f1-81a7cea177de.html) ⭐️ 6.0/10

加州大学伯克利分校数学教授理查德·博切兹（Richard Borcherds）认为，AI 使批改作业变得毫无意义，这引发了 Hacker News 上一场关于 AI 时代作业、评估与学习目的的大讨论。

hackernews · romanhn · 10月25日 16:28 · [社区讨论](https://news.ycombinator.com/item?id=50233304)

**标签**: `#AI in education`, `#LLMs`, `#academic integrity`, `#assessment/grading`, `#community discussion`

---

<a id="item-8"></a>
## [fheroes2：用 C++ 开源重制《魔法门之英雄无敌 II》游戏引擎](https://github.com/ihhub/fheroes2) ⭐️ 6.0/10

开源项目 fheroes2 是一个用 C++ 重新实现《魔法门之英雄无敌 II》游戏引擎的仓库，近日再次登上 Hacker News 首页，获得 195 分和 69 条评论。这轮讨论主要源于项目本身的成熟度与怀旧情绪，而非某个具体的新版本发布，讨论中并没有附带重大版本公告。 像 fheroes2 这样的项目对游戏保存意义重大：它让一款 1996 年的商业游戏能够原生运行在现代 Windows、Linux 和 macOS 上，而不是被困在 DOS 模拟器里慢慢失效。它也展示了社区如何在原发行商缺席的情况下现代化一个闭源引擎——加入更高分辨率、更好的 AI 和多人对战等功能。 fheroes2 是彻底重写的引擎实现，本身不附带任何受版权保护的游戏资源，因此玩家必须自备原版游戏，并让引擎读取其数据文件。除了兼容性之外，它还叠加了原版从未具备的增强功能，例如更高分辨率的渲染、改进的 AI 以及更完善的多人对战支持。

hackernews · tosh · 10月25日 11:09 · [社区讨论](https://news.ycombinator.com/item?id=50230384)

**背景**: 《魔法门之英雄无敌 II》由 New World Computing 于 1996 年开发、3DO 发行，该系列版权如今归育碧所有。由于原始源代码从未公开，粉丝们只能逆向分析游戏的文件格式与行为逻辑，再用 C++ 从头重写引擎，最终产出一个只需原版数据文件即可运行的程序。系列第三作《魔法门之英雄无敌 III》的开源引擎重写项目 VCMI 采用的也是同样的思路。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://quiverlauncher.com/apps/heroesofmightandmagiciii-vcmi">VCMI – Heroes of Might and Magic III PC port | Quiver</a></li>

</ul>
</details>

**社区讨论**: 评论者大多带着怀旧情绪，不少人表示《英雄无敌 III》才是系列中经久不衰的最爱，并向读者推荐了该作对应的开源引擎项目 VCMI，以及一个每周更新一局带解说对战的优质 YouTube 频道。一位评论者称自己搭建了 MCP 服务器让 Claude 玩《英雄无敌 III》，结果发现该智能体玩得很差而且非常慢，即使尝试教它策略也没有明显改善。也有人持怀疑态度，希望推出一款融合《英雄无敌 II》美术风格与《英雄无敌 III》游戏机制的新作，还有人感慨像这样的童年神作成年后重玩往往令人难以忍受。

**标签**: `#game-engine`, `#open-source`, `#reverse-engineering`, `#retro-gaming`, `#c++`

---