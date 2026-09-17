---
layout: default
title: "Horizon Summary: 2026-09-17 (EN)"
date: 2026-09-17
lang: en
---

> From 53 items, 5 important content pieces were selected

---

**AI Agents &amp; Society**
1. [Flock License-Plate Cameras Found With Hardcoded Credentials and Security Flaws](#item-ai-agent-impact-1) ⭐️ 7.0/10
2. [Ninth Circuit Rejects Expanded DMCA Liability Claim Against OpenAI and Microsoft](#item-ai-agent-impact-2) ⭐️ 7.0/10
3. [WeChat 8.0.78 Reportedly Lets Users Forward Packaged Chat Logs to ChatGPT](#item-ai-agent-impact-3) ⭐️ 6.0/10

**Technology Blog**
1. [CUDA Tile Kernels from Python to Rust via Agentic AI](#item-tech-blog-1) ⭐️ 9.0/10

**Financial News**
1. [Fed raises rates a quarter point, its first hike in more than three years](#item-finance-news-1) ⭐️ 9.0/10

---

## AI Agents &amp; Society

<a id="item-ai-agent-impact-1"></a>
### [Flock License-Plate Cameras Found With Hardcoded Credentials and Security Flaws](https://www.wired.com/story/hackers-flock-camera-data-shows-how-system-works/) ⭐️ 7.0/10

Independent security researcher Micah Lee documented security vulnerabilities and hardcoded credentials in Flock Safety&\#x27;s AI-powered license-plate-recognition camera network, which is widely deployed by police agencies, according to Wired reporting produced in collaboration with 404 Media. The exposed material included a hardcoded API key that could be used to request credentials stored in plaintext, which commenters said appeared to grant access to Flock&\#x27;s servers, though it is not clear what an attacker could do after authenticating as a camera. A commenter also pointed to Distributed Denial of Secrets publishing partition images from a Flock camera, and another commenter said the data is not encrypted and can be taken by anyone with physical access. The documented outcome is a set of vulnerabilities rather than a confirmed breach with observed harms to identifiable individuals, and the reach of any exposure remains unestablished. Commenters also criticized Flock&\#x27;s vulnerability disclosure policy as creating the appearance of a responsible security posture while discouraging research that involves interacting with devices or downloading their data. The affected population is the public subject to mass vehicle surveillance by police agencies using the system.

hackernews · driverdan · Sep 16, 13:18 · [Discussion](https://news.ycombinator.com/item?id=49726586)

**「Background」** Flock Safety runs a widely deployed network of AI-powered license-plate-recognition \(ALPR\) cameras that police departments use to log vehicle movements, with footage and logs stored on the devices themselves. Security researchers have documented numerous flaws in Flock&\#x27;s cameras, including hardcoded credentials and a lack of encryption \(tool-1-1\). In the incident at issue, a hacker collective physically pulled down an in-use camera and dumped its data; DDoSecrets published the partition images, and 404 Media and Wired reported jointly, with the files showing the device captured 1.6 million images of 50,000 vehicles in 21 days \(tool-1-2, tool-1-3\).

**「Social impact」** People whose vehicles pass a Flock AI license-plate reader become part of a record of where a car was, on what date, and at what time — data that civil-liberties advocates argue erodes privacy from the moment such cameras are installed. The reported hardcoded credentials and other vulnerabilities create a plausible risk that this location history could be accessed by parties beyond the police agencies that deploy the cameras, but the research documents exposure pathways rather than a confirmed breach, so no actual leak of individuals&\#x27; data has been established. Potential downstream effects on affected drivers include lost anonymity in lawful travel and reduced ability to know who has queried their movements.

**「Community Discussion」** Commenters agreed the findings signal poor security practice but disagreed on severity: one called hardcoded credentials a sign of &quot;total incompetence&quot; while noting the exposed item was an API key rather than a password and that post-authentication impact is unclear. Others blamed a &quot;reduced time to market&quot; approach and an inadequate threat model for cameras in unsecured public spaces, argued that Flock&\#x27;s vulnerability disclosure policy has a carveout for disclosures involving device interaction or data downloads, and noted that the camera data is unencrypted and physically accessible. A commenter added that the reporting was done with 404 Media and linked a separate discussion plus the Distributed Denial of Secrets publication of partition images.

<details><summary>References</summary>
<ul>
<li><a href="https://simeononsecurity.com/articles/flock-safety-camera-security-vulnerabilities-research-2026/">Flock Safety Camera Vulnerabilities: 50+ Flaws Found</a></li>
<li><a href="https://www.wired.com/story/hackers-flock-camera-data-shows-how-system-works/">Hackers Got Inside a Flock Camera. Its Data Shows How the ... - Wired</a></li>
<li><a href="https://www.bespacific.com/flock-cameras-are-riddled-with-security-vulnerabilities-and-hard-coded-credentials/">Flock cameras are riddled with security vulnerabilities and hard-coded ...</a></li>
<li><a href="https://www.eff.org/deeplinks/2026/09/high-crime-lmao-how-cops-are-treating-mass-surveillance-joke">The High Crime of “LMAO”: How Cops Are Treating Mass Surveillance ...</a></li>
<li><a href="https://deflock.org/">DeFlock is an open-source project that maps license plate readers...</a></li>

</ul>
</details>

**Tags**: `#surveillance`, `#ALPR`, `#security-vulnerabilities`, `#privacy`, `#police-technology`

---

<a id="item-ai-agent-impact-2"></a>
### [Ninth Circuit Rejects Expanded DMCA Liability Claim Against OpenAI and Microsoft](https://www.eff.org/deeplinks/2026/09/victory-appeals-court-rejects-expansive-new-copyright-claim) ⭐️ 7.0/10

The U.S. Court of Appeals for the Ninth Circuit rejected an attempt to expand Section 1202 of the Digital Millennium Copyright Act into a new source of copyright liability against OpenAI and Microsoft in Doe v. GitHub. A group of anonymous GitHub contributors had alleged that code generated by the companies&\#x27; large language models resembled their own code but with copyright management information \(CMI\) such as author names or copyright notices stripped out; OpenAI and Microsoft used GitHub code among billions of other works as training data. The court agreed with arguments EFF made in an amicus brief that removing CMI from a copyrighted work is fundamentally different from creating a new work that never contained CMI — the specific holding being that the absence of copyright information from a new work does not, by itself, show someone illegally removed it. EFF argued the plaintiffs&\#x27; theory would have created liability for otherwise lawful activity including remixes, classroom adaptations, reverse engineering, and search engines, with the burden falling hardest on independent developers and small creators who cannot afford prolonged federal litigation. The ruling leaves other avenues open: programmers can still bring copyright infringement claims if a model reproduces their code, and the plaintiffs&\#x27; contract claims against the AI companies remain in play.

rss · EFF Deeplinks · Sep 16, 22:47

**「Background」** The ruling came in Doe v. GitHub, a putative class action brought by anonymous programmers against GitHub, Microsoft, and OpenAI in the Northern District of California over GitHub Copilot and OpenAI Codex, generative coding tools trained on public GitHub repositories \[tool-1-2\]. After two rounds of dismissals and amendments, the complaint was narrowed to three claims: one under the DMCA and two for breach of contract \[tool-1-1\]. The DMCA provision at issue, Section 1202\(b\), requires the removal or alteration of copyright management information from a copy of the plaintiff&\#x27;s work and, the Ninth Circuit held, does not create a general claim whenever a system produces similar material without attribution \[tool-1-3\].

**「Who is affected」** The immediate losers are the anonymous GitHub contributors who brought the suit: their DMCA Section 1202 theory against OpenAI and Microsoft was rejected, though their contract claims remain pending. For the broader public EFF describes as affected — independent programmers, artists making remixes, teachers adapting material for class, engineers reverse engineering code, and search engines — the ruling removes a liability channel that, had it been accepted, could have forced costly federal litigation or settlement even for lawful uses; EFF argued small creators and independent developers would have borne that risk hardest because they cannot fund years of litigation the way large companies can. Observed effects are limited to the legal ruling itself: copyright infringement claims remain available where a model reproduces someone&\#x27;s code, and supporting commentary notes continuing uncertainty over licensing irregularities in AI-generated code and how other courts and jurisdictions will handle similar theories.

<details><summary>References</summary>
<ul>
<li><a href="https://cdn.ca9.uscourts.gov/datastore/opinions/2026/09/16/24-7700.pdf">UNITED STATES COURT OF APPEALS FOR THE NINTH CIRCUIT</a></li>
<li><a href="https://lexsummary.com/doe-v-github-dmca-ai-code-cmi-ninth-circuit-2026/">Doe v. GitHub — Ninth Circuit Rejects DMCA Claim Over ...</a></li>
<li><a href="https://lexcalifornia.com/intellectual-property/doe-v-github-ai-code-dmca-metadata-claim/">Doe v. GitHub — AI code-output allegations did not state a ...</a></li>
<li><a href="https://www.buildmvpfast.com/blog/ai-generated-code-liability-legal-risk-copyright-2026">AI Generated Code Liability : Copyright Risk, EU Directive &amp; Startup...</a></li>
<li><a href="https://static1.squarespace.com/static/5ab12ad9f8370ae1c0008379/t/68095f415f39341d09310c86/1745444673746/Annotation_Germano_Macroed.pdf">Github ’s copilot prompts IP litigation with</a></li>

</ul>
</details>

**Tags**: `#AI copyright`, `#DMCA Section 1202`, `#LLM training data`, `#Ninth Circuit ruling`, `#AI liability`

---

<a id="item-ai-agent-impact-3"></a>
### [WeChat 8.0.78 Reportedly Lets Users Forward Packaged Chat Logs to ChatGPT](https://www.chaincatcher.com/article/2290109) ⭐️ 6.0/10

According to a Chinese aggregator post from ChainCatcher \(circulated via the Telegram channel zaihuapd\), mobile WeChat users who upgrade to version 8.0.78 can select chat messages, choose &quot;forward to other app,&quot; and send them beyond Yuanbao and WorkBuddy to third-party apps installed on the phone, including ChatGPT, with a maximum of 100 messages per transfer. The report says WeChat packages the selected content into a ZIP archive containing a time-ordered TXT file and attachments, and that a similar entry point exists in desktop WeChat, where community developers have already built relay tools that pipe chat records into AI services such as ChatGPT and Claude. The people affected would be ordinary WeChat users whose private conversations could be moved into third-party AI apps, as well as the AI providers receiving that data under their own terms. The strongest evidence offered is the single social/aggregator post itself: there is no official confirmation from Tencent or OpenAI, no independent verification, and no demonstrated incidents or consequences, so both the feature&\#x27;s exact scope and its privacy implications remain unverified.

telegram · zaihuapd · Sep 16, 14:15

**「Background」** WeChat chat histories have historically been walled inside Tencent&\#x27;s ecosystem: in-app multi-select forwarding previously offered destinations such as Tencent&\#x27;s own Yuanbao assistant and WorkBuddy, and third-party export efforts met resistance — in January 2026 Tencent cited data privacy risks when it requested the removal of open-source WeChat export tools from GitHub, triggering an online backlash \(SCMP\). The 8.0.78 mechanism packages up to 100 selected messages into a ZIP archive containing time-ordered TXT transcripts plus attachments, which the receiving app opens as a file rather than through a platform API, according to user testing reported by tech outlets. The desktop client exposes a comparable entry point, and community developers have already built relay tools that route such archives into ChatGPT or Claude.

**「Social impact」** Users who forward a ZIP of up to 100 chat messages and attachments into ChatGPT or another third-party AI app could expose private conversations—including messages from people who did not consent—to external providers’ data handling and retention practices, with possible effects on privacy, relationships, employment, and legal confidentiality. WeChat has separately warned that third-party tools bypassing its security measures to obtain chat records violate its rules \(tool-3-1\), and official statements about some AI features say they do not touch chat records, moments, or contacts \(tool-3-2\); broader concerns have also been raised about AI agents that call on large amounts of user data \(tool-3-3\). The specific consequences of this reported forwarding path remain unverified, because the source is a single social/aggregator post with no official confirmation or independent testing.

<details><summary>References</summary>
<ul>
<li><a href="https://news.marsbit.co/flash/20260916104654510321.html">微信 8.0.78 支持将聊天记录打包转发至 ChatGPT</a></li>
<li><a href="https://www.binance.com/en/square/post/09-16-2026-wechat-expands-chat-history-export-to-third-party-apps-367149271928093">WeChat Expands Chat History Export to Third-Party Apps</a></li>
<li><a href="https://www.scmp.com/tech/tech-trends/article/3341003/tencent-crackdown-third-party-wechat-backup-tools-sparks-privacy-debate">Tencent crackdown on third-party WeChat backup tools sparks ...</a></li>
<li><a href="https://www.sohu.com/a/891291287_161314">关于聊天记录，微信发布最新公告！_用户_数据_服务</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/24171230011">微信AI会如何影响个人隐私和数据安全？ - 知乎</a></li>
<li><a href="https://www.toutiao.com/article/7648548772963729956/">微信AI智能体调取大量用户数据，会带来哪些隐私财产安全风险</a></li>

</ul>
</details>

**Tags**: `#WeChat`, `#AI assistants`, `#privacy`, `#data portability`, `#platform integration`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [CUDA Tile Kernels from Python to Rust via Agentic AI](https://developer.nvidia.com/blog/translating-cuda-tile-operations-from-python-to-rust-using-agentic-ai/) ⭐️ 9.0/10

rss · NVIDIA CUDA Technical Blog · Sep 16, 16:28

**「Background」** NVIDIA&\#x27;s TileGym library contains production tile kernels written in cuTile Python and Triton-TileIR, and the team wanted the same kernels available in cuTile Rust, a safer host language for tile-based GPU programming. Because all three front ends lower to the same CUDA Tile IR \(the cuda\_tile dialect\) and feed the same tileiras compiler, the authors frame the task less as re-optimization than as re-expressing a program while making Python JIT&\#x27;s implicit specializations explicit in Rust signatures.

**「Solution」** The tilegym-converting-python-to-rust skill uses a bounded multi-agent pipeline: an analyzer dumps reference Tile IR and writes analysis.json; a kernel writer produces kernel.rs; a host/FFI builder adds the C-ABI launcher and Python wrapper; and a performance validator runs CUPTI benchmarks. Stages end in machine-checkable verdicts, with shared-IR diffs and validator scripts deciding routing; specialists diagnose failures without editing code, separating mistranslations from compiler bugs. Communication is only through schema-fixed artifacts, spawns are capped, and a driver automates batch conversions. The softmax example shows ct.load padding modes and ct.bid mapping to explicit partition views and types, while the FFI launcher borrows PyTorch pointers without copies. The authors report porting all 24 public TileGym operators, roughly 40 kernels, to 99.5% geomean of cuTile Python on DGX B200 across 347 paired configurations; all cleared 0.95, about a third exceeded the reference, and token cost fell roughly by half. Some kernels still use unchecked APIs where only those reproduce reference IR exactly.

**「Takeaway」** The authors&\#x27; larger claim is that shared compiler IR makes cross-front-end kernel translation verifiable by structural diff, so a validator-gated agentic workflow can port kernels repeatably and inherit near-reference performance rather than relying on functional tests alone.

**Tags**: `#CUDA Tile IR`, `#Rust`, `#agentic AI`, `#GPU kernels`, `#compiler translation`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Fed raises rates a quarter point, its first hike in more than three years](https://www.cnbc.com/2026/09/16/here-are-five-key-takeaways-from-wednesdays-fed-rate-hike.html) ⭐️ 9.0/10

The Federal Reserve raised its benchmark interest rate by a quarter percentage point on Wednesday to a target range of 3.75%–4%, its first increase in more than three years. The Federal Open Market Committee vote was unanimous at 12-0, and the Fed&\#x27;s projections show 16 of 18 officials expect at least one more hike this year.

rss · CNBC Finance · Sep 16, 21:23

**「Background」** The Fed had held rates steady all year and last raised them in July 2023, but it is acting now because inflation remains above its 2% target — a level officials don&\#x27;t expect to reach until 2029 — with higher oil prices and tariffs among the pressures cited.

**「Impact」** Because the Fed&\#x27;s rate is a benchmark for many consumer and business loans, households and companies holding variable-rate debt, such as credit cards and some auto loans, typically face higher borrowing costs after a hike.

**Tags**: `#Federal Reserve`, `#monetary policy`, `#interest rates`, `#market reaction`, `#inflation`

---