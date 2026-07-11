---
layout: default
title: "Horizon Summary: 2026-07-11 (ZH)"
date: 2026-07-11
lang: zh
---

> 从 29 条内容中筛选出 8 条重要资讯。

---

1. [vLLM v0.25.0：MRv2 成默认，PagedAttention 移除，速度持平](#item-1) ⭐️ 9.0/10
2. [全球首例远程操控人形机器人活猪手术](#item-2) ⭐️ 9.0/10
3. [U-Boot 引导程序曝 6 个漏洞，可在启动时执行恶意代码](#item-3) ⭐️ 9.0/10
4. [爱因斯坦相对论支配重元素化学键](#item-4) ⭐️ 8.0/10
5. [苹果起诉 OpenAI 窃取商业机密](#item-5) ⭐️ 8.0/10
6. [上海目标：2027 年前实现高质量脑控，推动脑机接口临床](#item-6) ⭐️ 8.0/10
7. [SGLang v0.5.15 提升 LLM 服务性能](#item-7) ⭐️ 7.0/10
8. [VultronRetriever 模型登顶 MTEB，可在 iPhone 离线运行](#item-8) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0：MRv2 成默认，PagedAttention 移除，速度持平](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 9.0/10

vLLM v0.25.0 将 Model Runner V2 设为所有稠密模型的默认执行路径，移除了旧版 PagedAttention 实现，并使 Transformers 后端速度与原生 vLLM 持平。 此版本标志着 vLLM 架构的范式转变，简化了代码库并提升了大多数模型的性能。与 Transformers 后端的速度持平扩大了兼容性且不牺牲效率，惠及 LLM 推理社区。 Model Runner V2 现在支持基于驱逐的调度（EVS）、实时嵌入、Mamba 混合模型的 prefix caching，以及带有完整 CUDA graphs 的动态推测解码。移除 PagedAttention 消除了遗留的注意力代码路径。

github · khluu · 7月11日 20:06

**背景**: PagedAttention 是一种注意力算法，通过将 KV 缓存划分为固定大小的块来优化内存管理，类似于虚拟内存分页。它于 2023 年随 vLLM 一起提出。Model Runner V2 (MRv2) 是重新设计的执行后端，取代了原始的模型运行器和注意力实现。此版本将 MRv2 设为稠密模型的默认后端，完成了从基于 PagedAttention 的旧方法的迁移。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PagedAttention">PagedAttention</a></li>
<li><a href="https://github.com/vllm-project/vllm/releases">Releases · vllm -project/ vllm</a></li>

</ul>
</details>

**标签**: `#LLM Inference`, `#vLLM`, `#Model Optimization`, `#Open Source`, `#Performance`

---

<a id="item-2"></a>
## [全球首例远程操控人形机器人活猪手术](https://arstechnica.com/ai/2026/07/humanoid-robots-controlled-by-surgeons-did-world-first-operation-on-live-pigs/) ⭐️ 9.0/10

外科医生成功利用远程操控的宇树 G1 人形机器人，在活猪身上完成了全球首例微创胆囊切除手术。该概念验证实验已发表在《自然》期刊，标志着通用人形机器人首次用于活体手术。 这一突破展示了低成本人形机器人执行远程手术的潜力，有望将手术能力带到农村、战场或太空等传统机器人系统过于昂贵或不实用的地方。 宇树 G1 机器人基础款售价 13,500 美元，配备灵巧手后约 67,000 美元，远低于达芬奇等专用手术机器人（高达数百万美元）。该机器人高 1.5 米，重 27 公斤，由加州大学圣地亚哥分校的外科医生远程操控。

telegram · zaihuapd · 7月11日 02:29

**背景**: 微创手术（如腹腔镜胆囊切除术）是胆囊切除的标准方法，但需要昂贵的机器人系统。达芬奇手术机器人售价 50 万至数百万美元，限制了可及性。像 G1 这样的人形机器人提供了更便宜的替代方案，可轻松部署在资源有限的环境中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://today.ucsd.edu/story/surgeons-use-teleoperated-humanoid-robots-to-perform-live-surgery-a-world-first">Surgeons Use Teleoperated Humanoid Robots to Perform Live Surgery – a World First</a></li>
<li><a href="https://www.nature.com/articles/s41586-026-10796-x">In vivo feasibility study of humanoid robots in surgery | Nature</a></li>
<li><a href="https://www.popsci.com/technology/humanoid-robots-perform-surgery/">In groundbreaking first, humanoid robots performed surgery | Popular Science</a></li>

</ul>
</details>

**标签**: `#humanoid robotics`, `#surgical robotics`, `#medical innovation`, `#telemedicine`

---

<a id="item-3"></a>
## [U-Boot 引导程序曝 6 个漏洞，可在启动时执行恶意代码](https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/) ⭐️ 9.0/10

固件安全公司 Binarly 披露了 U-Boot 引导程序 FIT 签名验证代码中的 6 个漏洞，其中 2 个可导致任意代码执行，4 个可造成设备崩溃。这些漏洞影响超过 50 个稳定版本，最早可追溯到 U-Boot 2013.07 版本，并波及大量下游厂商分支。 由于漏洞位于固件验证阶段，攻击者可在操作系统和安全软件启动之前执行恶意代码，从而禁用固件安全功能或植入持久性恶意软件。对于支持远程固件更新的 BMC 等系统，攻击者无需物理接触即可利用这些漏洞。 Binarly 已向 U-Boot 维护者提交补丁并获得接受，但每个硬件厂商需要将这些补丁集成到固件更新中并分发。已停止支持的老旧设备可能永远无法获得修复。6 个漏洞中有 2 个可导致任意代码执行，4 个可导致设备崩溃。

telegram · zaihuapd · 7月11日 08:32

**背景**: U-Boot 是一个开源引导程序，广泛用于嵌入式设备，负责硬件初始化和启动操作系统内核。FIT（扁平化设备树镜像）格式是一种灵活的镜像打包格式，支持加密签名，而漏洞就存在于其签名验证代码中。BMC（基板管理控制器）是服务器主板上的专用微控制器，支持远程管理和固件更新。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Das_U-Boot">Das U-Boot - Wikipedia</a></li>
<li><a href="https://u-boot.org/">Das U-Boot: The Universal Boot Loader</a></li>
<li><a href="https://www.supermicro.com/en/glossary/baseboard-management-controller">What is a Baseboard Management Controller? (BMC)</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerabilities`, `#U-Boot`, `#firmware`, `#embedded systems`

---

<a id="item-4"></a>
## [爱因斯坦相对论支配重元素化学键](https://www.brown.edu/news/2026-07-09/chemical-bonds-relativity) ⭐️ 8.0/10

发表在《科学》杂志上的新研究表明，爱因斯坦的相对论通过自旋-轨道耦合控制重元素的化学键合，为汞的液态和金子的颜色等现象提供了统一解释。 这项研究加深了对量子化学的基本理解，并可能为涉及重元素的新材料和催化剂的设计提供指导。 该研究强调了自旋-轨道耦合，即电子在相对论速度下其自旋和轨道运动变得相互依赖，从而改变了键合特性。

hackernews · hhs · 7月10日 22:30 · [社区讨论](https://news.ycombinator.com/item?id=48866134)

**背景**: 相对论量子化学将爱因斯坦的相对论与量子力学结合，用于计算重元素的性质。对于重核，内部电子速度接近光速的显著比例，导致相对论效应影响化学行为。例如，汞的液态和金子的黄色是已知的相对论效应。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Spin–orbit_interaction">Spin–orbit interaction - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Relativistic_quantum_chemistry">Relativistic quantum chemistry - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，相对论对电子轨道的影响早已为人所知，但这项研究为自旋-轨道耦合提供了新见解。一位评论者幽默地强调自己不是物理学家。另一位则指出这是对爱因斯坦工作的美好验证。

**标签**: `#relativity`, `#chemical bonds`, `#heavy elements`, `#quantum chemistry`, `#spin-orbit coupling`

---

<a id="item-5"></a>
## [苹果起诉 OpenAI 窃取商业机密](https://9to5mac.com/2026/07/10/apple-sues-openai-trade-secret-theft/) ⭐️ 8.0/10

苹果对 OpenAI 提起诉讼，指控该公司指使前苹果员工窃取机密商业机密，并指导新员工如何在离职时规避审查。 此诉讼可能为 AI 行业的知识产权保护树立重要先例，且鉴于苹果的雄厚资源，这对 OpenAI 的运营和硬件野心构成重大法律威胁。 苹果声称 OpenAI 利用窃取的硬件信息接触苹果供应商，并指出员工在离职前通过邮件发送机密数据的模式。此诉讼可能导致 OpenAI 的硬件计划终结，类似 Waymo 诉 Uber 案。

hackernews · stock_toaster · 7月10日 20:47 · [社区讨论](https://news.ycombinator.com/item?id=48865019)

**背景**: 商业机密诉讼涉及盗用保密商业信息的指控。在科技行业，员工在竞争公司间跳槽时常发生此类案件。苹果和 OpenAI 都是 AI 和硬件领域的主要参与者，使这场法律战尤为重要。

**社区讨论**: 评论者大多支持苹果的行动，许多人批评 OpenAI 的企业道德及其所谓的“版权侵犯”。一些人警告称，证据开示过程可能严重损害 OpenAI 的投资者信心和员工留存。

**标签**: `#Apple`, `#OpenAI`, `#trade secrets`, `#lawsuit`, `#AI`

---

<a id="item-6"></a>
## [上海目标：2027 年前实现高质量脑控，推动脑机接口临床](https://t.me/zaihuapd/42501) ⭐️ 8.0/10

上海市科学技术委员会印发《上海市脑机接口未来产业培育行动方案（2025-2030 年）》，目标是 2027 年前实现高质量脑控，半侵入式脑机接口产品在国内率先实现临床应用，侵入式脑机接口研发取得突破。 该政策表明政府对脑机接口技术的大力支持，有望加速该技术从实验室走向临床应用，特别是帮助瘫痪或失语患者恢复语言和运动功能。 方案要求推动 5 款以上侵入式、半侵入式脑机接口产品完成医疗器械型式检验和临床试验，面向失语、瘫痪等患者实现部分语言和运动功能恢复。

telegram · zaihuapd · 7月11日 15:49

**背景**: 脑机接口（BCI）分为侵入式、半侵入式和非侵入式三类。侵入式 BCI 需通过手术将电极植入脑组织，信号质量高但风险也高；半侵入式 BCI 将电极置于大脑表面（如皮质脑电图），在信号质量和安全性之间取得平衡；非侵入式 BCI 使用头皮电极（脑电图），安全性高但分辨率较低。上海的计划重点推动半侵入式和侵入式 BCI 走向临床应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Brain–computer_interface">Brain–computer interface - Wikipedia</a></li>
<li><a href="https://www.linkedin.com/pulse/minds-interface-bridging-thought-technology-bci-neuranet-ai-otbae">The Mind's Interface : Bridging Thought and Technology with BCI</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12671281/">Invasive Brain-Computer Interfaces: A Critical Assessment of Current Developments and Future Prospects - PMC</a></li>

</ul>
</details>

**标签**: `#brain-computer interface`, `#policy`, `#medical technology`, `#Shanghai`, `#neural engineering`

---

<a id="item-7"></a>
## [SGLang v0.5.15 提升 LLM 服务性能](https://github.com/sgl-project/sglang/releases/tag/v0.5.15) ⭐️ 7.0/10

SGLang v0.5.15 提供了显著的 LLM 服务性能优化，包括具有零开销调度的 Speculative Decoding V2 以及可将草稿步骤成本降低最多 1.9 倍的 IndexShare MTP。它还引入了在 Blackwell GPU 上优化的 GLM-5.2 NVFP4 服务，在 8x B300 上实现 500+ tok/s/user。 此版本实现了更高吞吐量和更低延迟的生产级 LLM 服务，尤其有利于 GLM-5.2 和 DeepSeek-V4 等模型。推测解码和多 token 预测技术的进步对于聊天机器人和编码助手等实时应用至关重要。 Speculative Decoding V2 默认启用，采用 CUDA 图可处理的 DSA draft-extend，端到端 TPS 提升 11%。IndexShare MTP 在草稿步骤间重用索引器 top-k，长上下文下成本降低最多 1.9 倍。新增模型支持包括 Hunyuan 3、NVIDIA LocateAnything-3B 等。

github · Fridge003 · 7月10日 22:58

**背景**: SGLang 是一个高效的 LLM 服务开源框架，专注于低延迟和高吞吐量。NVFP4 是 NVIDIA 为 Blackwell GPU 推出的 4 位浮点格式，可在保持准确性的同时提高推理效率。推测解码使用草稿模型每步预测多个 token，从而减少延迟。IndexShare MTP 是一种多 token 预测技术，通过跨草稿步骤共享计算来进一步降低开销。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision Inference | NVIDIA Technical Blog</a></li>
<li><a href="https://www.spheron.network/blog/b300-vs-b200-inference-cost-per-token/">NVIDIA B 300 vs B200 for AI Inference: Is Blackwell ... | Spheron Blog</a></li>
<li><a href="https://huggingface.co/blog/zai-org/glm-52-blog">GLM-5.2: Built for Long-Horizon Tasks</a></li>

</ul>
</details>

**标签**: `#sglang`, `#LLM serving`, `#performance optimization`, `#speculative decoding`, `#GLM`

---

<a id="item-8"></a>
## [VultronRetriever 模型登顶 MTEB，可在 iPhone 离线运行](https://www.reddit.com/r/MachineLearning/comments/1utmxq8/vultronretriever_family_of_models_released_on/) ⭐️ 7.0/10

Vultr 在 HuggingFace 上发布了 VultronRetriever 系列嵌入模型，其中 Prime-8B 模型声称在 MTEB 排行榜上位列全球第一。所有模型都针对离线部署进行了优化，可在 iPhone 等边缘设备上完全运行。 此次发布通过提供最先进的准确性并大幅减少存储占用、提高吞吐量，挑战了现有的嵌入模型领导者，使得在消费级设备上实现强大的检索增强生成（RAG）应用成为可能。这可能会加速在无网络环境下进行搜索、问答和文档理解的设备端 AI 的普及。 该系列包含三个规模：Prime-8B 声称相比之前的 9B 类领先模型，索引存储占用减少 16 倍，吞吐量提高 12 倍；Core-4.5B 的性能超越两倍于其大小的模型；Flash-0.8B 离线状态下每分钟可索引多达 60 张图片。所有模型均采用 Hydra 架构，支持后期交互检索，内存消耗仅为同类模型的一半。

reddit · r/MachineLearning · /u/madkimchi · 7月11日 15:22

**背景**: 嵌入模型将文本或图像转换为捕获语义含义的数值向量，从而实现相似性搜索和检索。大规模文本嵌入基准（MTEB）是一个标准的公共排行榜，用于评估模型在检索、分类和聚类等任务上的表现。Hydra 架构在单个视觉语言模型中统一了文档检索和生成，使用双向注意力进行检索，使用因果注意力进行生成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/spaces/mteb/leaderboard">MTEB Leaderboard - a Hugging Face Space by mteb</a></li>
<li><a href="https://docs.vultr.com/models">Model Library | Vultr Docs</a></li>
<li><a href="https://arxiv.org/html/2603.28554">Hydra: Unifying Document Retrieval and Generation in a Single Vision-Language Model</a></li>

</ul>
</details>

**标签**: `#embedding models`, `#MTEB`, `#retrieval`, `#efficient ML`, `#offline AI`

---