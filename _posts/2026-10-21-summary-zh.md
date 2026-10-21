---
layout: default
title: "Horizon Summary: 2026-10-21 (ZH)"
date: 2026-10-21
lang: zh
---

> 从 42 条内容中筛选出 8 条重要资讯。

---

1. [PHP 禁令泄露后紧急发布 RCE 补丁，并承诺强化安全治理](#item-1) ⭐️ 9.0/10
2. [eMudhra 证书颁发机构签发的 RSA 密钥弱到毫秒级即可被分解](#item-2) ⭐️ 9.0/10
3. [DuckDB 2.0.0 LTS“Cinnamon Teal”发布：新增客户端-服务器模式、触发器与更强扩展性](#item-3) ⭐️ 9.0/10
4. [PHP 8.2.35 发布，修复关键 PHP2Shell 远程代码执行漏洞](#item-4) ⭐️ 9.0/10
5. [eMudhra 八个中间 CA 私钥泄露，触发信任库紧急更新](#item-5) ⭐️ 9.0/10
6. [PHP 核心曝高危 RCE 漏洞，官方将于 10 月 21 日发布紧急补丁](#item-6) ⭐️ 9.0/10
7. [SpaceX 星舰超重型助推器首次被得州发射塔臂成功捕获](#item-7) ⭐️ 9.0/10
8. [PHP 核心曝两处高危 RCE 漏洞，官方定于 10 月 21 日 22:00（UTC+8）发布修复](#item-8) ⭐️ 9.0/10

---

<a id="item-1"></a>
## [PHP 禁令泄露后紧急发布 RCE 补丁，并承诺强化安全治理](https://thephp.foundation/blog/2026/10/21/todays-php-security-release-and-how-were-strengthening-php-security/) ⭐️ 9.0/10

2026 年 10 月 21 日，PHP 发布修复版本，解决了两个严重的远程代码执行漏洞 CVE-2026-109618 与 CVE-2026-109619（被称作「PHP2Shell」），影响范围几乎覆盖 PHP 5.4 以来的所有版本；由于漏洞细节在 10 月 20 日、即原定协调披露日前约一天外泄，官方被迫提前发布补丁。与此同时，PHP 基金会公布了新的安全强化举措，包括 2026 年 5 月成立的生态安全团队（Ecosystem Security Team），以及一位与 PHP 安全团队协作的常驻 AI 安全工程师。 PHP 承载着互联网上极大比例的网站，一个可远程利用且细节已公开的漏洞，迫使数以百万计的站点运营者紧急打补丁，美国与英国的国家安全机构均已发出警告。禁令被提前打破这一事实也说明，信息泄露与 AI 辅助的漏洞利用正把「披露到大面积攻击」之间的窗口从数周压缩到数小时。 根据安全通告与相关讨论，这两个 CVE 源于 PHP 会话上传进度（session.upload_progress）处理中的堆释放后重用（use-after-free）问题，细节比原定协调日期提前约一天流出，打乱了发布节奏。据报道，一家安全公司在约定时间前发布了宣传视频，Chainguard 也单方面推送了构建镜像；而运维人员发现，只需在 nginx 层拦截 multipart 上传，就足以挡住针对该漏洞的利用。

hackernews · ejohnso49 · 10月21日 15:48 · [社区讨论](https://news.ycombinator.com/item?id=50182987)

**背景**: PHP 是一门广泛用于服务端的脚本语言，全球大多数网站都依赖它运行；而「远程代码执行」（RCE）属于最严重的一类漏洞，因为攻击者可以直接在服务器上运行任意代码。协调披露通常依赖「禁令期」（embargo）：报告者与厂商约定统一的公开日期，确保补丁先于技术细节抵达用户；一旦信息外泄，禁令即视为失效，厂商往往被迫立即公开。如今 AI 工具同时加速了漏洞的发现与武器化，使这类禁令窗口变得越来越脆弱。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thephp.foundation/blog/2026/10/21/todays-php-security-release-and-how-were-strengthening-php-security/">Today's PHP Security Release, and How We're Strengthening PHP ...</a></li>
<li><a href="https://sansec.io/research/php2shell">Critical PHP RCE: CVE-2026-109618 and CVE-2026-109619</a></li>
<li><a href="https://www.redhat.com/en/blog/Understanding-security-embargoes-at-Red-Hat">Understanding security embargoes at Red Hat</a></li>

</ul>
</details>

**社区讨论**: 在约 300 条评论的 Hacker News 讨论中，运维人员分享了他们写的三行 nginx 规则（拦截 multipart 上传），它持续保护着一台无法下线的脆弱机器，而攻击流量据称来自各类主流 AI 智能体工具。评论者严厉批评安全公司 Calif 在泄密后抢发营销视频，以及 Chainguard 单方面破坏禁令；也有人借此呼吁彻底更换互联网的安全模型，例如用配送令牌代替提交个人信息、禁止用于广告的用户追踪。

**标签**: `#security`, `#php`, `#vulnerability-disclosure`, `#remote-code-execution`, `#ai-security`

---

<a id="item-2"></a>
## [eMudhra 证书颁发机构签发的 RSA 密钥弱到毫秒级即可被分解](https://scotthelme.co.uk/eight-bits-of-trust-emudhras-ca-keys-cracked-in-milliseconds/) ⭐️ 9.0/10

公开受信任的证书颁发机构 eMudhra 被发现在其签发的证书中使用了熵极低的 RSA 密钥，以致其素因子可在毫秒之内被分解还原。该问题由研究员 Wayne 用谷歌开源工具 paranoid_crypto 对 CCADB 中的 CA 证书语料做了一次“开箱即用”的扫描而发现，随后引发了操作系统、语言运行时和容器基础镜像中 CA 证书包的紧急更新。 由于 eMudhra 位于几乎所有浏览器和设备的默认信任库之中，一个可被轻易分解的密钥会动摇整条信任链：任何能分解该密钥的人都可以伪造出对任意域名看似合法的证书。这起事件也为“同时信任约一百家根证书机构是否是可长期维持的安全模型”这一长期争论提供了一个具体的反面案例。 问题出在密钥生成而非 RSA 算法本身——随机性不足导致生成的素数存在共享或可被猜出，于是分解从天文级难度变成举手之劳。修复方式是更新所有包含 eMudhra 根证书的 CA 证书包（操作系统 ca-certificates、certifi、Node、Homebrew 等）并重建容器镜像；原报告者表示，对所有现有 CCADB 证书的更全面复查未再发现其他命中。

hackernews · hkc · 10月21日 09:08 · [社区讨论](https://news.ycombinator.com/item?id=50177916)

**背景**: 证书颁发机构（CA）是为网站 TLS 证书签名的实体，用来证明网站身份；如果 CA 自身的签名密钥被攻破，攻击者就能为任意域名签发受信任的证书。RSA 的安全性建立在一个假设之上：分解两个大随机素数的乘积在计算上不可行，因此一旦素数由弱随机数生成器产生，整个方案便会崩塌。浏览器和操作系统内置一份受信任根证书列表（CA bundle），当某个 CA 被吊销信任或被发现有弱密钥时，更新的正是这些证书包。CCADB 即 Common CA Database，是由 Mozilla 维护的公共数据库，各 CA 需在其中披露其运营的根证书与中间证书。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.keyfactor.com/wp-content/uploads/Factoring-RSA-Keys-in-the-IoT-Era-JD-Kilgallin-Keyfactor-IEEE-Conference.pdf">Factoring RSA</a></li>
<li><a href="https://pepijnvanderstap.nl/blog/the-pki-trust-paradox/">The PKI Trust Paradox | Pepijn van der Stap</a></li>
<li><a href="https://emudhra.com/en/faq/what-is-certificate-authority">What Is a Certificate Authority (CA)? | eMudhra - Global</a></li>

</ul>
</details>

**社区讨论**: 评论者大多对检测手段之“平淡”感到惊讶——原报告者确认谷歌的 paranoid_crypto 开箱即用就找出了弱密钥——一条高赞评论则调侃说，事后看来同时信任一百家证书机构或许确实过分了。另一些人关注修复的不对称性：对可掌控的系统来说升级并不复杂，真正棘手的是固件被冻结的物联网设备；还有评论者推测，这些被破解的密钥反过来可以被用来伪造证书，从而越狱这些同样封闭的设备。

**标签**: `#security`, `#PKI`, `#cryptography`, `#certificate-authority`, `#RSA`

---

<a id="item-3"></a>
## [DuckDB 2.0.0 LTS“Cinnamon Teal”发布：新增客户端-服务器模式、触发器与更强扩展性](https://duckdb.org/2026/10/21/announcing-duckdb-200) ⭐️ 9.0/10

2026 年 10 月 21 日，开源分析型数据库 DuckDB 发布了代号为“Cinnamon Teal”的 2.0.0 LTS 版本，这是一次重大版本升级。此次发布主要集中在三个方面：在高核心数机器上大幅提升的可扩展性、全新的客户端-服务器架构，以及对触发器的支持。 客户端-服务器能力标志着 DuckDB 从纯嵌入式引擎向“开箱即用的数据仓库”转变——单个中心实例即可服务众多客户端，有望取代由多台服务器组成的数据栈。再加上大型云主机上更强的扩展性，DuckDB 的适用范围从单机分析扩展到了组织级分析负载。 早期用户反馈称，DuckDB 2.0 在 EC2 上可将 CPU 利用率跑满至约 128–192 vCPU，而 2.0 之前的上限约为 64 vCPU，但超过约 192 vCPU 后加速效果仍会趋于平缓。DuckDB 自有的 Quack 协议目前客户端支持有限，因此实际部署往往改用 Postgres 线协议或 Arrow Flight/ADBC。

hackernews · nnx · 10月21日 14:01 · [社区讨论](https://news.ycombinator.com/item?id=50181136)

**背景**: DuckDB 是一个开源、列式存储的关系型数据库管理系统，专为 OLAP（联机分析处理）负载设计，即在大型数据表上执行快速分析查询，通常以嵌入式方式使用，常被形容为“分析领域的 SQLite”。在传统嵌入式模式下，以写入方式打开数据库文件会对其加锁，同一时间只允许一个写入者；而把 DuckDB 作为服务器运行，则可以让众多客户端连接到这个唯一的写入者。新的客户端-服务器路径由 Quack 协议支撑，这是一种面向 DuckDB 的 RPC 风格协议；而“LTS”表示长期支持版本，旨在为生产用户提供稳定的基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://duckdb.org/quack/">The Quack protocol turns DuckDB into a client - server database.</a></li>
<li><a href="https://motherduck.com/blog/duckdb-client-server/">If It Quacks Like a Duck : DuckDB Gets a Client - Server ... | MotherDuck</a></li>
<li><a href="https://en.wikipedia.org/wiki/DuckDB">DuckDB - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者热情很高：有人表示 DuckDB 2.0 在 EC2 上把满载利用率提升到 128–192 vCPU（此前约为 64），使其得以将 Splink 记录链接工具扩展到更大规模；另一位用户称已把 alpha 版本用于生产，借助 Postgres 线协议和 Arrow Flight 扩展，将其作为服务小型组织的集中式分析服务器。还有人认为客户端-服务器架构是“游戏规则改变者”，将取代许多多服务器数据栈，并称赞触发器支持让 DuckDB 真正成为“开箱即用的数据仓库”。

**标签**: `#duckdb`, `#databases`, `#analytics`, `#olap`, `#open-source`

---

<a id="item-4"></a>
## [PHP 8.2.35 发布，修复关键 PHP2Shell 远程代码执行漏洞](https://github.com/php/php-src/releases/tag/php-8.2.35) ⭐️ 9.0/10

PHP 8.2.35 已作为 8.2 分支的安全更新发布，配合“PHP2Shell”漏洞的协同披露；该漏洞是 PHP 核心中的一对关键漏洞，编号为 CVE-2026-109618 和 CVE-2026-109619，于 2026 年 10 月 20 日公开。据报道，这些漏洞是在 Wiz、Calif 和 OpenAI 参与的联合工作中借助人工智能发现的。 这很重要，因为 PHP2Shell 可让未经身份验证的攻击者在核心 PHP 部署上执行任意代码，包括最新的 WordPress、Drupal 和 Joomla 容器镜像，其 CVSS 严重性评分达到 9.2。这也标志着人工智能辅助的漏洞研究触及基础性开源基础设施，迫使管理员尽快打补丁。 PHP2Shell 将两个 CVE 组合成一条利用链，研究人员已演示了在无需身份验证的情况下对 WordPress、Drupal 和 Joomla 容器部署实现远程代码执行。发布过程本身也受到审视：据报道 8.4.27 标签一度出现但没有 amd64 镜像，社区成员还指出可能存在第二个漏洞的线索。

hackernews · tuyuri · 10月21日 13:45 · [社区讨论](https://news.ycombinator.com/item?id=50180873)

**背景**: PHP 是一种广泛使用的服务器端脚本语言，支撑着 WordPress、Drupal 和 Joomla 等内容管理系统。远程代码执行（RCE）漏洞尤其严重，因为攻击者可以在服务器上运行命令，而不仅仅是读取数据。协同披露是一种流程：研究人员私下报告漏洞，厂商准备修复，各方商定公开日期，以便防御者在细节被广泛利用之前完成修补。PHP2Shell 事件还值得注意，因为据报道其发现过程借助了人工智能，这是漏洞研究中日益增长的趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PHP2Shell">PHP 2 Shell - Wikipedia</a></li>
<li><a href="https://www.wiz.io/blog/php2shell-php-rce">PHP 2 Shell : AI uncovers critical RCE vulnerabilities ... | Wiz Blog</a></li>
<li><a href="https://www.php2shell.com/">PHP 2 Shell — AI uncovers critical vulnerabilities in the backbone of...</a></li>

</ul>
</details>

**社区讨论**: 评论者迅速给出了 Wiz、Calif、OpenAI 和 PHP 基金会的公告链接，同时指出可能存在第二个漏洞，并实时跟踪发布产物。一些人对发布处理方式提出批评，因为 8.4.27 标签出现时没有 amd64 镜像，不过一位有 20 年 PHP 托管经验的用户表示，自己此前从未预防性地关停服务器。总体情绪既有对安全问题的严肃担忧，也有对发布协调不力的不满。

**标签**: `#php`, `#security`, `#rce`, `#coordinated-disclosure`, `#ai-security-research`

---

<a id="item-5"></a>
## [eMudhra 八个中间 CA 私钥泄露，触发信任库紧急更新](https://simonwillison.net/2026/Oct/20/emudhra-certificates/) ⭐️ 9.0/10

eMudhra 八个中间 CA 证书的私钥已被泄露，而这些证书均链接到 Mozilla、Microsoft、Apple 和 Chrome 根计划所信任的根证书。该事件已触发各 Linux 发行版的 ca-certificates 包以及 Python 工具链的紧急证书列表更新，uv 0.13.4、pip 26.2.2 和 certifi 2026.10.19 均已发布升级后的证书包。 任何持有这些私钥的人都能签发对任意域名看似合法的证书，从而在信任库被修补之前透明地拦截 TLS 流量。由于受影响的中间 CA 链接到被广泛信任的根证书，其影响范围几乎覆盖每一个自带 CA 包的操作系统、浏览器、容器镜像和语言运行时。 Cloudflare 的分析文章将这八个中间证书的问题归因于密钥强度不足，并表示正在部署缓解措施并发布客户端更新；Mozilla 也已提交一个 P1 级别的 CA 证书合规缺陷（bug 2083449）。实际的修复手段虽然平常但十分紧迫：在 Linux 上更新 ca-certificates 包，并升级 certifi、pip、uv 以及任何内置静态信任库的软件。

rss · Simon Willison · 10月20日 23:50

**背景**: 公钥基础设施依赖一条信任链：操作系统和浏览器中预装了一小部分根证书，这些根证书签发中间 CA 证书，中间 CA 再签发网站使用的终端实体证书。信任库本质上就是某款软件所接受的一组根证书和中间证书列表，这也是 certifi 这类项目会把 Mozilla 精心维护的 CA 包内置进 Python 包的原因。一旦某个中间 CA 的私钥泄露，它签发过的所有证书——以及攻击者用它签发的证书——都将与合法证书无法区分，因此必须将该中间 CA 标记为不受信任并从各处的信任库中移除。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/emudhra-certificate-compromise">8 eMudhra certificates are compromised. Here's what you need ...</a></li>
<li><a href="https://bugzilla.mozilla.org/show_bug.cgi?id=2083449">2083449 - Private key compromise of eMudhra Intermediate ...</a></li>
<li><a href="https://cybersecuritynews.com/emudhra-security-compromise/">eMudhra Certificate Authority Compromise Triggers Emergency ...</a></li>

</ul>
</details>

**标签**: `#security`, `#pki`, `#certificate-authority`, `#tls`, `#supply-chain-security`

---

<a id="item-6"></a>
## [PHP 核心曝高危 RCE 漏洞，官方将于 10 月 21 日发布紧急补丁](https://sansec.io/research/php2shell) ⭐️ 9.0/10

PHP 官方团队披露了 PHP 核心解释器中的两处高危远程代码执行漏洞——CVE-2026-109618 与 CVE-2026-109619，CVSS 评分均为 9.2，并计划于 10 月 21 日 22:00（UTC+8）发布修复补丁。漏洞影响自 PHP 5.4 以来的所有版本，涵盖 5.x、7.x 以及 8.0 至 8.5 各分支，但官方仅为受支持分支 PHP 8.2、8.3、8.4、8.5 提供修复更新。 由于漏洞在解释器核心层就被触发，早于任何业务框架或应用代码执行，因此常见的应用层防护和框架级输入过滤都无法拦截，攻击者可在未打补丁的服务器上实现完整的代码执行。PHP 至今支撑着大量 Web 站点——WordPress、Laravel、Drupal 以及无数遗留系统——而数量庞大的已停更（EOL）部署永远拿不到官方修复，是风险最集中的部分。 两个漏洞的 CVSS 评分均为 9.2（严重级），且利用发生在业务框架代码执行之前，因此框架本身无法起到缓解作用。官方只对 PHP 8.2、8.3、8.4、8.5 提供补丁；PHP 5.x、7.x 以及 8.0/8.1 等已停更分支只能通过收敛公网访问入口或实施网络隔离来防止被利用。

telegram · zaihuapd · 10月21日 03:28

**背景**: PHP 是一种服务端脚本语言，驱动着全球大多数内容管理系统和 Web 框架，因此其核心解释器出现漏洞时影响范围异常广泛。RCE（远程代码执行）意味着攻击者可以在服务器上执行任意命令，这通常是面向 Web 的组件最糟糕的一种漏洞后果。CVSS 是业界通用的严重程度评分体系，9.0 分及以上被归类为“严重”，表示攻击复杂度低且影响巨大。“停更”（EOL，End-of-Life）版本指维护方已不再支持的分支，官方完全不会为其发布安全修复。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.first.org/cvss/calculator/3-1">Common Vulnerability Scoring System Version 3.1 Calculator</a></li>
<li><a href="https://vitejs.cn/news/2026-09-22-nuxt-3-end-of-life">Nuxt 3 正式结束生命周期： 风 险 、漏洞清单与三条出路</a></li>

</ul>
</details>

**标签**: `#PHP`, `#security`, `#RCE`, `#CVE`, `#vulnerability`

---

<a id="item-7"></a>
## [SpaceX 星舰超重型助推器首次被得州发射塔臂成功捕获](https://t.me/zaihuapd/44587) ⭐️ 9.0/10

SpaceX 的超重型助推器在飞行返回后，被得克萨斯州发射塔的机械臂成功捕获，这是该助推器首次实现发射塔臂回收。助推器在发射场被接住的同时，星舰第二级继续飞行，并按计划准备在印度洋进行受控溅落。 用发射塔机械臂直接捕获助推器，而不是让其依靠着陆腿降落，是实现快速复用的关键一步——助推器无需从远处着陆场运回，就能就地检查、加注并再次飞行。如果这一方式能够稳定可靠地运行，将有望大幅降低这枚史上最大火箭的单次发射成本，并巩固 SpaceX 在商业与政府发射市场中的地位。 这次捕获依靠发射塔的大型机械臂在助推器动力下降过程中将其夹住，对末端制导精度要求极高，容错空间很小。与此同时，第二级目前还不会返回陆地，而是在印度洋进行受控的动力溅落，以验证再入与着陆点火的表现。

telegram · zaihuapd · 10月21日 06:00

**背景**: 星舰（Starship）是 SpaceX 正在研制的全复用超重型运载系统，由超重型（Super Heavy）第一级助推器和星舰第二级组成。位于得克萨斯州博卡奇卡星基地（Starbase）的发射塔装有巨大的机械臂，被外界戏称为“Mechazilla”，其设计目的是在空中夹住返回的助推器，而不是让其依靠着陆腿降落。两级火箭都能完整且快速地复用，是 SpaceX 通过规模效应压低发射成本、并支撑登月与火星任务目标的核心思路。目前第二级仍以受控海面溅落的方式回收，作为未来返回发射场降落之前的过渡方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SpaceX_Super_Heavy">SpaceX Super Heavy - Wikipedia</a></li>
<li><a href="https://www.aa.com.tr/en/science-technology/spacex-s-starship-completes-test-with-controlled-splashdowns/3670244">SpaceX’s Starship completes test with controlled splashdowns</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#Starship`, `#Super Heavy`, `#aerospace`, `#rocket landing`

---

<a id="item-8"></a>
## [PHP 核心曝两处高危 RCE 漏洞，官方定于 10 月 21 日 22:00（UTC+8）发布修复](https://t.me/zaihuapd/44597) ⭐️ 9.0/10

PHP 官方团队宣布将于 10 月 21 日 22:00（UTC+8）发布安全更新，修复核心解释器中的两处高危远程代码执行漏洞，编号为 CVE-2026-109618 与 CVE-2026-109619，CVSS 评分为 9.2。此次补丁仅覆盖仍受支持的分支 PHP 8.2、8.3、8.4 和 8.5，而据称漏洞影响自 PHP 5.4 以来的所有版本，包括 5.x、7.x 以及 8.0 至 8.5 各分支。 PHP 支撑着互联网上极大比例的站点与应用，包括 WordPress、Drupal、Laravel、Symfony 以及无数自研系统，因此解释器层面的、类似免认证的 RCE 漏洞影响面极其广泛；又因为攻击在框架代码执行之前即可触发，应用层防护几乎无能为力。仍运行已停止维护分支的管理员则必须规划升级，而不是简单打补丁。 据二手报道，CVE-2026-109618 涉及内存耗尽（OOM）处理过程中的内存破坏，CVE-2026-109619 则是与请求之间保留状态有关的释放后使用（use-after-free）缺陷，两者均可让未认证攻击者以 Web 工作进程的权限远程执行代码。该消息源自聚合类帖子，并未附带上游官方公告链接，因此 CVE 编号与技术细节尚未得到独立核实，除安装官方更新外也未给出其他缓解措施。

telegram · zaihuapd · 10月21日 14:00

**背景**: PHP 是一种服务端脚本语言，由解释器（Zend 引擎）执行，运行在绝大多数 Web 服务器上；由于解释器会在任何框架或业务代码之前处理每一个请求，其内部缺陷位于大多数安全工具所监控的层次之下。CVE 是为已公开漏洞分配的标准编号，CVSS 则是与厂商无关的 0 到 10 分严重性评分体系，9.2 分属于“严重”级别。远程代码执行（RCE）指攻击者可在远程机器上执行任意命令的一类漏洞，通常被视为最严重的类别，因为它可能让攻击者完全控制主机。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.imperva.com/learn/application-security/remote-code-execution/">Remote Code Execution (RCE) | Types, Examples & Mitigation ... CVE-2026-67631: Microsoft SQL Server Remote Code Execution ... CVE-2026-109618 and CVE-2026-109619: Critical ... - Rapid7 What is Remote Code Execution (RCE)? - GeeksforGeeks What Is Remote Code Execution (RCE)? Attacks ... - Fortinet Mitigating CVE-2025-22944 Remote Code Execution Vulnerability ...</a></li>
<li><a href="https://www.techtarget.com/cybersecurity/definition/Common-Vulnerability-Scoring-System-CVSS">What is a Common Vulnerability Scoring System ( CVSS )?</a></li>
<li><a href="https://www.cve.org/">CVE : Common Vulnerabilities and Exposures</a></li>

</ul>
</details>

**标签**: `#php`, `#security`, `#rce-vulnerability`, `#cve`, `#patching`

---