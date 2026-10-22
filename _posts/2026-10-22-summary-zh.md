---
layout: default
title: "Horizon Summary: 2026-10-22 (ZH)"
date: 2026-10-22
lang: zh
---

> 从 41 条内容中筛选出 8 条重要资讯。

---

1. [任天堂 Switch 2 据报被纯软件漏洞破解，LLM 智能体参与其中](#item-1) ⭐️ 9.0/10
2. [Quad9 因藐视法庭裁决将撤出法国 DNS 解析服务](#item-2) ⭐️ 8.0/10
3. [Show HN：HackiOS 借助 QEMU 与 XNU 在安卓手机上启动完整 iOS 16.5 固件](#item-3) ⭐️ 8.0/10
4. [eMudhra 在密钥遭破解后退出全球 SSL/TLS 证书业务](#item-4) ⭐️ 8.0/10
5. [Earstrip 用 489 毫秒三角化 370 万个地图多边形，速度超越 Earcut](#item-5) ⭐️ 8.0/10
6. [澳大利亚联邦法院认定苹果和谷歌滥用市场支配地位](#item-6) ⭐️ 8.0/10
7. [333 个遭 Ebury 后门感染的 Tor 出口节点被下线](#item-7) ⭐️ 8.0/10
8. [NVIDIA OpenShell：面向自主 AI 智能体集群的沙箱化运行时](#item-8) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [任天堂 Switch 2 据报被纯软件漏洞破解，LLM 智能体参与其中](https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) ⭐️ 9.0/10

一位开发者在 pepsipu.com 上发布文章，记录了看似是任天堂 Switch 2 的首次越狱（jailbreak），据称使用的是可在当前固件上运行的纯软件漏洞，而非硬件改装芯片。该文章及其在 Hacker News 上的讨论帖（669 分、236 条评论）描述了这样一套方案：给 Codex 编程智能体配上“眼睛和手”——通过 JetKVM 远程 KVM 设备经 USB 发送手柄输入、经 HDMI 读取画面输出——以协助搜索并驱动该漏洞。 如果得到证实，这将是任天堂迄今防护最严密的游戏主机之一首次被公开攻破，可能在硬件生命周期远早于厂商预期的阶段就打开自制软件（homebrew）、游戏 Mod 和加密文件系统访问的大门。同样重要的是，将 LLM 智能体与廉价的远程 KVM 硬件搭配使用的工作流，可能成为一种可复用的自动化硬件安全研究范式，其影响远不止于游戏主机。 相关报道强调，该漏洞是纯软件的且并非永久性，重启后需要重新触发，无法形成持久化安装。文章还披露了这套自动化方案的“土法上马”之处：由于每次崩溃后主机都需要手动按一下电源键才能恢复，作者用一个 SwitchBot Bot 智能开关机械臂去物理按压电源键。

hackernews · ledoge · 10月22日 08:01 · [社区讨论](https://news.ycombinator.com/item?id=50192536)

**背景**: Switch 2 是任天堂接替 Switch 的新一代主机，与多数现代游戏机一样，它会对所有运行的代码进行加密签名校验，因此要运行非官方软件就必须找到一个绕过这些校验的漏洞，这一过程被称为越狱。主机厂商通常会以固件补丁和法务手段回应，这也是可用漏洞稀缺且价值极高的原因。JetKVM 是一款体积小、成本低的 IP-KVM 设备，可通过网络暴露目标机器的 HDMI 输出与 USB 输入，让软件（或 AI 智能体）操作它原本无法触及的硬件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.notebookcheck.net/The-Nintendo-Switch-2-has-reportedly-been-jailbroken-through-a-software-only-exploit.1431060.0.html">The Nintendo Switch 2 has reportedly been jailbroken through ...</a></li>
<li><a href="https://kotaku.com/nintendo-switch-2-jailbreak-hack-exploit-piracy-homebrew-emulation-modding-2000748784">The Switch 2 Has Been Jailbroken For The First Time - Kotaku</a></li>
<li><a href="https://www.vice.com/en/article/nintendo-switch-2-jailbreak-mario-kart-world-mods/">Nintendo Switch 2 Jailbreak Reportedly Allows Mario Kart ...</a></li>

</ul>
</details>

**社区讨论**: 评论者大多表示惊叹，最高赞的评论指出，若能真正读写解密后的文件系统，很可能数小时内就会出现 Switch 2 游戏转储，而考虑到当下的重编译（recomp）生态（评论提到《塞尔达传说：王国之泪》已能在 iPhone 上原生跑 60fps），这意味着主机独占游戏可以在任意硬件上运行。也有人为这套自动化装置——被戏称为“Switch SwitchBot Bot”——的荒诞感叫好；还有评论者困惑于作者究竟如何让 Codex 配合工作，称该模型曾拒绝其类似的老款 Android CVE 研究请求。另一个反复出现的话题是社交媒体上对该事件的批评：有人声称这种 AI 辅助的破解“没有灵魂”，宁愿等待“更合乎道德”的、由人类开发的漏洞。

**标签**: `#hardware hacking`, `#console jailbreak`, `#Nintendo Switch 2`, `#security research`, `#LLM agents`

---

<a id="item-2"></a>
## [Quad9 因藐视法庭裁决将撤出法国 DNS 解析服务](https://quad9.net/news/blog/au-revoir-france/) ⭐️ 8.0/10

瑞士非营利公共 DNS 解析器 Quad9 宣布将撤出法国市场，原因是法国法院认定其未全面屏蔽盗版相关域名而构成藐视法庭。Quad9 首席技术官 John Todd 表示，11 月 24 日之后，该服务很可能通过 geoIP 过滤彻底屏蔽法国用户。 这一退出表明，法国激进的网站屏蔽禁令正在把独立 DNS 解析器逐出该国，使域名解析进一步集中到谷歌、Cloudflare 等选择服从命令的少数大型厂商手中。它还确立了一个先例：基于地理位置的“部分合规”可能无法令版权方满意，这对整个欧洲的 DNS 层面审查具有广泛影响。 原告索尼音乐娱乐（Sony Music Entertainment GmbH）从德国通过 VPN 访问了 Quad9 针对法国 IP 地址所屏蔽的内容，法院将这种绕过行为认定为 Quad9 未合规，而非屏蔽本身生效的证据。Quad9 则认为，geoIP 过滤从根本上无法按用户位置精准选择性拒绝解析，称这场争议是法律预期与技术现实之间的错位。

hackernews · farrokhi · 10月22日 14:32 · [社区讨论](https://news.ycombinator.com/item?id=50195959)

**背景**: Quad9 是由瑞士一家非营利基金会运营的免费公共递归 DNS 解析器，会拦截与恶意软件和钓鱼相关的域名查询。DNS 解析器相当于互联网的“电话簿”，负责把域名翻译成 IP 地址，因此成为版权方封杀盗版网站时青睐的卡点。地理封锁（geo-blocking）依据用户表面上的 IP 归属地限制访问，而众所周知可通过 VPN 绕过。自 2024 年以来，法国法院多次应 Canal+、beIN Sports 等广播商的请求，命令公共 DNS 解析器屏蔽盗版体育直播站点；思科旗下的 OpenDNS 约两年前退出该市场，而谷歌和 Cloudflare 则选择服从。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Quad9">Quad9 - Wikipedia</a></li>
<li><a href="https://torrentfreak.com/dns-resolver-quad9-rejects-french-piracy-blocks-weighs-exit-as-bein-seeks-up-to-e580k-a-day/">DNS Resolver Quad9 Rejects French Piracy Blocks, Weighs Exit ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Geo-blocking">Geo-blocking</a></li>

</ul>
</details>

**社区讨论**: 评论者几乎一边倒地同情 Quad9 并批评该裁决，有人将其比作因电话簿收录了罪犯号码而惩罚电话簿出版商。Quad9 首席技术官澄清了法律与技术上的权衡，也承认用 geoIP 封锁排除法国用户看似自相矛盾；其他人则指出思科/OpenDNS 曾有过类似退出，谷歌和 Cloudflare 则是被迫服从，还有人建议解析器反过来停止解析起诉方的域名作为回应。

**标签**: `#DNS`, `#internet-censorship`, `#internet-governance`, `#privacy`, `#legal`

---

<a id="item-3"></a>
## [Show HN：HackiOS 借助 QEMU 与 XNU 在安卓手机上启动完整 iOS 16.5 固件](https://github.com/oosexgang/hackios-xnu-kernel) ⭐️ 8.0/10

一个名为 HackiOS 的 Show HN 项目（仓库 oosexgang/hackios-xnu-kernel）在安卓手机硬件上启动了苹果开源的 XNU 内核（xnu-8796.121.2，即 iOS 16.5 所用的内核），并在其上运行未经修改的 iOS 16.5 用户空间，从 launchd 到 backboardd、SpringBoard 再到应用程序逐级跑通。该项目已在 QEMU 以及 POCO X5 Pro 5G 和部分小米设备上演示成功，依赖自制的 EFI 引导器和伪造的 iPhone X 设备驱动。 这是一个令人印象深刻的移动安全与虚拟化概念验证：在非苹果硬件上运行未经修改的 iOS 用户空间，为不接触真机 iPhone 的安全研究、模糊测试和应用测试提供了新思路。讨论也折射出关于移动操作系统开放性的更大争论，因为不少评论者更希望看到相反的方向——在苹果硬件上运行自由的安卓发行版。 作者强调这是一个研究台（research bench）而非 ROM：每次会话仅持续固定的秒数，随后内核返回加载器并交出日志，重启后直接回到安卓系统，全程不需要刷机。据称该发布不包含任何苹果文件，并且可以在 QEMU 中复现。

hackernews · aghuang · 10月22日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=50196718)

**背景**: XNU 是苹果的混合内核，结合了 Mach 微内核与 BSD 组件，是 macOS、iOS、iPadOS、tvOS 和 watchOS 的基础。QEMU 是一款开源的机器模拟与虚拟化工具，常用于在通用硬件上运行安卓或其他操作系统。启动真实的设备内核通常需要匹配的硬件驱动，因此该项目伪造了 iPhone X 的驱动，并使用自制的 EFI 引导器和兼容层。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://book.st-hakky.com/en/news/run-ios-16-5-firmware-on-android">HackiOS: Running unmodified iOS 16.5 on Android hardware</a></li>
<li><a href="https://github.com/oosexgang/hackios-xnu-kernel">Show HN: Run full iOS 16.5 firmware on Android Devices</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mach_(kernel)">Mach ( kernel ) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者对其能在 QEMU、POCO X5 Pro 5G 和部分小米设备上运行表示惊叹，但也有多人质疑其意义——有人认为更值得追求的目标是在苹果硬件上运行 GrapheneOS 之类的自由安卓发行版，或解放被锁引导程序的手机。还有人调侃项目缺少由 AI 自动修复崩溃的循环，以及按压重启和音量键的电动机械装置；也有人提醒，现在购买二手 iPhone 时需要仔细甄别那些运行着仿 iOS 安卓系统的山寨机。

**标签**: `#iOS`, `#Android`, `#virtualization`, `#mobile-security`, `#QEMU`

---

<a id="item-4"></a>
## [eMudhra 在密钥遭破解后退出全球 SSL/TLS 证书业务](https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business) ⭐️ 8.0/10

印度证书颁发机构 eMudhra 宣布退出全球 SSL/TLS 证书业务，并强调其全球 SSL/TLS 基础设施与其他业务分开运行。此举发生在该机构 8 个中间 CA 私钥被破解的事件之后，且此前已遭到浏览器厂商和安全社区的强烈审视。 一家受公开信任的 CA 退出 Web PKI 十分罕见，凸显了浏览器根证书计划如今对整个证书生态的强大掌控力。这将影响所有使用 eMudhra 签发 TLS 证书的客户与依赖方，也表明密钥生成环节的缺陷足以终结一条完整业务线。 据 Palo Alto Unit 42 分析，这 8 个中间 CA 私钥在生成时随机性不足，属于证书生成流程中的关键密码学缺陷，因而可被破解。eMudhra 还声称受影响的 CA 未签发任何终端实体证书，但评论者对此表示怀疑，因为任何人都可以向这些 CA 申请证书。

hackernews · bo0tzz · 10月22日 13:33 · [社区讨论](https://news.ycombinator.com/item?id=50195110)

**背景**: 证书颁发机构（CA）是受信任的实体，负责签发将域名与公钥绑定的 X.509 证书；浏览器和操作系统只接受能链接到其信任存储（即 Chrome、Mozilla、苹果、微软等运营的根证书计划）中根证书的证书。一旦中间 CA 的私钥泄露，攻击者就能为任意域名伪造看似合法的证书，因此根证书计划要求严格的密钥管理，并会迅速取消对失职 CA 的信任。证书透明度（Certificate Transparency）日志使这类错误签发可被公众发现，本次事件中大量审视正源于此。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://unit42.paloaltonetworks.com/emudhra-certificate-compromise/">EMudhra Intermediate CA Certificates Compromised</a></li>
<li><a href="https://www.coindesk.com/tech/2026/10/21/a-company-that-vouches-for-websites-had-secret-keys-so-weak-that-8-of-them-were-cracked">Internet panics after 8 eMudhra private keys get cracked</a></li>
<li><a href="https://certificate.transparency.dev/">Certificate Transparency : Certificate Transparency</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论以批评为主，嘲讽该公司所谓“审视与事件不成比例”的说法，并指出它从未解释密钥生成缺陷是如何发生的，也没有真正道歉。还有人提到 Chrome 团队公开向 eMudhra 提交的一连串严厉质询，并有评论者贴出一段仅四个字符的“RSA 私钥”来调侃此事。

**标签**: `#PKI`, `#SSL/TLS`, `#certificate authorities`, `#security incident`, `#browser trust`

---

<a id="item-5"></a>
## [Earstrip 用 489 毫秒三角化 370 万个地图多边形，速度超越 Earcut](https://globus.software/blog/2026/10/16/cutting-map-polygons/) ⭐️ 8.0/10

Globus Software 发布了一篇技术文章，介绍了一种多边形三角化方法（其实现库在讨论中被称为 "Earstrip"，并有 WebAssembly 构建），可在 489 毫秒内完成 370 万个地图多边形的三角化。文章称其速度超过了 Mapbox 的 Earcut——浏览器三角化领域长期以来的 JavaScript 基准实现，同时公开了基准数据集，方便他人复现与对比。 三角化正处于矢量地图和三维地球可视化的渲染关键路径上，因此在大规模多边形数据集上取得接近一个数量级的加速，意味着更流畅的交互，以及可以把更大的数据集体直接下发到浏览器端而无需在服务器上预处理。这也重新打开了一个在地图生态中被视为已有定论的问题：Earcut 的耳切法是否仍是合适的默认方案。 Earcut 作者指出，他有意放弃了一些可行的优化以保持库体积小巧（最小化并 gzip 后约 4.1 kB），因此这一对比在一定程度上是用打包体积换取原始速度，他还询问 Earstrip 的 WASM 构建有多大。Delaunay32 作者则表示，他的约束 Delaunay 三角化器采用分治而非增量插入，尚未在该数据集上跑过基准，而且现有 API 要求简单环且洞之间不能接触。

hackernews · molind · 10月22日 09:31 · [社区讨论](https://news.ycombinator.com/item?id=50193170)

**背景**: 多边形三角化是计算几何中的一个经典问题：把一个多边形区域切分成一组互不重叠的三角形，这正是 GPU 为地图图形填充颜色所需要的。耳切法（Ear clipping，即 Mapbox 的 Earcut 所采用的方法）不断找出并剪掉“耳朵”（凸顶点三元组），直到只剩下三角形；它流行的原因不是渐进复杂度最优，而是简单、健壮且体积小。Earcut 经 gzip 压缩后约 4 kB，一直是 Mapbox GL JS 等浏览器地图渲染器做实时三角化的事实标准。WebAssembly 让用 C++ 或 Rust 编写的库能在浏览器中以接近原生的速度运行，这也正是本文性能差距得以出现的前提。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/mapbox/earcut">GitHub - mapbox/earcut: The fastest and smallest JavaScript ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Polygon_triangulation">Polygon triangulation - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 讨论吸引了 Earcut 作者（mourner）和 Delaunay32 作者（morishuz）参与，两人都称赞了结果，但分别提出了打包体积和 API 兼容性方面的保留意见。有评论者指出 CMU 的 Shewchuk Triangle 是三角化领域的经典参考实现；也有人质疑为什么“耳切法加优化”能胜过 Seidel 梯形法等渐进复杂度更优的算法，并猜测差异是否源于三角形质量和狭长三角形的处理。

**标签**: `#triangulation`, `#computational-geometry`, `#performance`, `#WebAssembly`, `#maps`

---

<a id="item-6"></a>
## [澳大利亚联邦法院认定苹果和谷歌滥用市场支配地位](https://t.me/zaihuapd/44612) ⭐️ 8.0/10

2025 年 8 月 12 日，澳大利亚联邦法院作出当庭口头裁决，认定苹果和谷歌在应用商店与支付系统领域滥用市场支配地位，实质性削弱了竞争，违反了澳大利亚竞争法。 这是一项重要的反垄断裁决，可能迫使苹果在澳大利亚向第三方应用商店和支付渠道开放 App Store，也加入了全球范围内影响开发者的平台监管浪潮。 法院认定，苹果强制开发者仅使用其自有应用内支付系统，以及谷歌在安卓应用商店和支付服务市场的行为，均构成滥用市场力量；判决全文目前因保密争议被封存，苹果和谷歌已表示对部分裁决内容持异议。

telegram · zaihuapd · 10月22日 06:54

**背景**: 此案源于 Epic Games 在全球范围内针对所谓“苹果税”的长期诉讼——即苹果对应用内购买抽取的佣金，以及禁止开发者使用其他支付渠道的规定。澳大利亚竞争法禁止拥有显著市场力量的企业从事实质性削弱竞争的行为，当地法院正在审查移动应用分发与支付是否属于被苹果和谷歌不当捆绑在一起的两个独立市场。

**标签**: `#antitrust`, `#Apple`, `#Google`, `#App Store regulation`, `#mobile payments`

---

<a id="item-7"></a>
## [333 个遭 Ebury 后门感染的 Tor 出口节点被下线](https://kaba.cx/posts/20261020_Tor/) ⭐️ 8.0/10

一名 Tor 运营者用脚本扫描了约 3000 个出口中继，发现其中 333 个（约占全部出口的 10%）被植入了 Ebury 后门；该后门会把 22 端口的 SSH 连接劫持到 12 台拦截服务器上以窃取凭据。这些节点于 10 月 4 日被标记为 BadExit，次日已全部下线。 Tor 出口中继是流量离开匿名网络的最后一跳，约 10% 的出口被协同攻陷，直接威胁到在暴露期间通过 Tor 登录 SSH 或收发未加密邮件的用户。这也说明长期活跃、以往主要针对托管服务商的 Ebury 行动，如今已被用来攻击匿名网络基础设施本身。 攻击者据信在 8 月就已入侵这些服务器，并特意屏蔽部分端口，以便专门收集未加密的邮件流量，而最初的入侵途径目前尚无定论。Ebury 是一种 OpenSSH 后门兼凭据窃取工具，通常通过篡改合法 sshd 程序所加载的共享库（.so 文件）来传播。

telegram · zaihuapd · 10月22日 14:52

**背景**: Tor 通过入口、中间和出口三跳中继转发流量，只有出口中继能看到最终目的地，因此恶意出口可以窥探或篡改任何未受端到端加密保护的内容。Tor 的目录权威可以给中继打上 BadExit 标记，指示客户端不再把它当作出口使用，实际上等同于让它变成非出口节点。Ebury 由 ESET 记录、并被 MITRE 编号为 S0377，是一种与 Windigo 组织关联的 Linux/OpenSSH 后门，十余年间已攻陷数十万台服务器，主要用于挖矿、发送垃圾邮件和窃取凭据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://attack.mitre.org/software/S0377/">Ebury, Software S0377 | MITRE ATT&CK®</a></li>
<li><a href="https://archive.torproject.org/websites/support.torproject.org/relay-operators/what-is-the-bad-exit-flag/">What is the BadExit flag ? | Tor Project | Support</a></li>
<li><a href="https://www.eset.com/us/about/newsroom/press-releases/eset-research-ebury-botnet-alive-growing/">ESET Research: Ebury botnet alive & growing; 400k Linux ...</a></li>

</ul>
</details>

**标签**: `#Tor`, `#security`, `#backdoor`, `#Ebury`, `#malware`

---

<a id="item-8"></a>
## [NVIDIA OpenShell：面向自主 AI 智能体集群的沙箱化运行时](https://github.com/NVIDIA/OpenShell) ⭐️ 7.0/10

NVIDIA 在 GTC 圣何塞 2026 大会上发布了 OpenShell，这是一个采用 Apache-2.0 许可证的开源运行时，可在由声明式 YAML 策略管控的内核级沙箱中运行成批的自主 AI 智能体。它允许智能体读取文件、安装软件包、调用 API 并使用凭证，同时对每一次文件访问、系统调用和网络连接强制执行策略。 智能体基础设施一直缺少一个可信且有厂商背书的方案来限制凭证使用与出站网络流量，而这恰恰是数据外泄与影响范围失控风险最集中的地方。一个由 NVIDIA 维护、能够管控智能体执行乃至推理请求走向的运行时，有可能成为团队从单智能体演示迈向生产级智能体集群时的默认安全层。 OpenShell 需要受支持的主机环境（Linux、Apple Silicon 上的 macOS，或实验性支持、需配合 WSL 2 的 Windows），并需要启用 Docker、Podman 或主机虚拟化来提供基于 MicroVM 的沙箱。策略执行发生在基础设施层而非智能体自身代码中，覆盖文件访问、系统调用和网络出站流量，但它只是限制访问权限，并不能消除能力与安全之间固有的取舍。

hackernews · niemandhier · 10月22日 17:44 · [社区讨论](https://news.ycombinator.com/item?id=50198675)

**背景**: 自主编程与任务型智能体只有在能操作真实系统时才最有价值——读取代码仓库、安装依赖、调用外部 API——但这也意味着一个被攻陷或产生幻觉的智能体可能泄露源码或密钥。沙箱化通过把每个智能体放进隔离环境（通常是轻量级 MicroVM 或容器）并要求每个动作都通过显式策略来解决这一问题。相关技术还包括凭证隔离（智能体使用中间代理签发的令牌而非原始密钥）以及只允许连接白名单域名的出站过滤。OpenShell 把这些思路打包成一个声明式运行时，目标是同时运行大量智能体，而不仅是单个智能体。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/ai/openshell/">NVIDIA OpenShell | Open, Secure Runtime for AI Agents</a></li>
<li><a href="https://perspectives.nvidia.com/nvidia-openshell/">OpenShell</a></li>
<li><a href="https://www.everydev.ai/tools/nvidia-openshell">NVIDIA OpenShell - Sandboxed Runtime for AI Agents | EveryDev. ai</a></li>

</ul>
</details>

**社区讨论**: 从业者对工具本身总体持肯定态度，但对宣传措辞持怀疑态度：多人表示自己早已把智能体跑在容器里，并推荐 iron proxy 之类的辅助工具来实现按域名限制网络访问和凭证替换。反复出现的质疑是，最困难的问题依然是通过可信通道进行的数据外泄（有评论提到 Hugging Face 事件），并且有人反驳 OpenShell 能同时实现最大能力与最大安全的说法。也有人追问大家究竟用智能体集群做什么，还有一位用户称 Claude 的安全分类器阻止其开发进程执行审计功能。

**标签**: `#AI agents`, `#sandboxing`, `#security`, `#NVIDIA`, `#agent infrastructure`

---