---
layout: default
title: "Horizon Summary: 2026-09-16 (ZH)"
date: 2026-09-16
lang: zh
---

> 从 47 条内容中筛选出 2 条重要资讯。

---

**AI Agent 与社会影响**
1. [“Project Lily”内幕：人工阅读 ChatGPT 聊天记录](#item-ai-agent-impact-1) ⭐️ 7.0/10
2. [Strix 报告 Baseten GitHub 令牌接管漏洞，Baseten 确认未遭利用](#item-ai-agent-impact-2) ⭐️ 6.0/10

---

## AI Agent 与社会影响

<a id="item-ai-agent-impact-1"></a>
### [“Project Lily”内幕：人工阅读 ChatGPT 聊天记录](https://www.404media.co/inside-project-lily-the-humans-reading-your-chatgpt-chats/) ⭐️ 7.0/10

404 Media 报道称，OpenAI 正雇用数百名合同工参与代号“Project Lily”的项目，人工阅读大量真实用户的 ChatGPT 提示词和完整对话，并为模型回复评分、提出修改意见。报道指出，这些聊天记录中可能包含敏感个人信息；OpenAI 表示会在交给审核员前尽量删除个人信息，但承认敏感细节仍可能被看到。Anthropic 也确认会使用人工审核来改进模型。受影响者包括聊天记录被审阅的 ChatGPT 用户，以及从事审核工作的合同工。支持这一报道的最强证据是 404 Media 的独立报道，以及 OpenAI 和 Anthropic 对人工审核做法的确认；目前公开信息未说明具体审核规模、涉及地区或数据保留期限。

telegram · zaihuapd · 9月15日 11:56

**「背景」** 在大语言模型的开发流程中，人工审核被用于评估模型回复质量并提出改进意见，这类工作通常由外包合同工承担，是模型训练与调优的常见环节。当用户与聊天机器人的对话被纳入此类审核时，聊天内容会离开用户与模型之间的会话环境，进入公司内部工具和审核流程，因此个人信息能否得到保护取决于事前过滤和访问控制措施。OpenAI 与 Anthropic 均确认使用人工审核来改进模型，表明这并非单一公司的做法，而是当前行业的一种普遍机制。

**「社会影响」** 对使用者而言，最直接的后果是私密性受损：据 404 Media 报道，大量真实提示词与完整对话被数百名合同工阅读，OpenAI 虽称会尽量在审核前删除个人信息，却承认敏感细节仍可能被看到，这意味着用户自认为私密的倾诉或身份、健康类信息存在被第三方看到的实际风险——隐私通常被理解为“属于个人、不对外公开”的事物\[tool-2-1\]\[tool-2-3\]。对合同工群体，长期阅读他人敏感对话可能带来心理负担与保密压力，但这一点在现有材料中没有直接证据，属于合理推测而非已观察到的结果。由于报道未给出被泄露信息的数量、具体案例，也未说明用户是否被告知或被征得同意，实际损害的范围与程度仍不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Privacy">Privacy - Wikipedia</a></li>
<li><a href="https://simple.wikipedia.org/wiki/Privacy">Privacy - Simple English Wikipedia , the free encyclopedia</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#data privacy`, `#human review`, `#AI contractors`, `#ChatGPT`

---

<a id="item-ai-agent-impact-2"></a>
### [Strix 报告 Baseten GitHub 令牌接管漏洞，Baseten 确认未遭利用](https://www.strix.ai/blog/baseten-harbor-github-pat-takeover) ⭐️ 6.0/10

Strix 报告了 Baseten 的一个 GitHub 令牌接管漏洞，涉及泄露的 basetenbot 令牌、公开的 Harbor 项目及仓库权限。Baseten 安全团队的 Philip 在 Hacker News 确认与 Strix 协作修复，立即作废泄露密钥并移除公开容器镜像，日志显示漏洞从未被利用且没有客户数据暴露。根据 swyx 的时间线，7 月 13 日晚 11:10 报告了该活跃令牌、公开 Harbor 项目与仓库权限；7 月 14 日上午 Baseten 将 Harbor 项目设为私有，但令牌仍有效；同日下午 4:34，Baseten 安全团队的 Anton 确认问题为严重，并称已设为私有并轮换令牌，还要求安全删除已拉取的镜像。该事件被描述为 AI 智能体辅助发现，但评论对其能力独特性、是否事前授权测试等仍有争议。

hackernews · bearsyankees · 9月15日 18:11 · [社区讨论](https://news.ycombinator.com/item?id=49716476)

**「背景」** Baseten 是一家 AI 基础设施公司，提供模型推理与训练平台：客户可通过 OpenAI 兼容的 API 调用托管模型、在专属基础设施上部署自有模型或训练模型，平台负责管理模型容器、跨云与跨区域的 GPU 容量、扩缩容和可观测性（tool-1-2、tool-1-3）。本次事件所涉的 GitHub token 是一种授予代码仓库读写或管理权限的凭据，当它随公开的容器项目或镜像一起暴露时，任何获取到该字符串的人都可能使用这些权限。据社区讨论，泄露的 token 与一个公开的 Harbor 容器项目相关联，Baseten 方面随后确认已作废该密钥、移除公开镜像并完成修复。

**「社会影响」** 已观察到的后果有限：Baseten 表示日志确认漏洞未被利用，没有客户数据暴露，泄露密钥已作废、公开镜像已移除。若该令牌被利用，理论上可能危及 Baseten 的生产 GitHub 仓库与容器镜像，进而影响其 AI 基础设施及依赖它的客户，但现有证据不支持实际影响。事件也把“安全智能体能否未经事先授权对潜在供应商域名进行测试”的合规与信任问题推到讨论前台。

**「社区讨论」** Baseten 的 Philip 确认修复并感谢负责任披露，swyx 给出了详细时间线；ivraatiems 认为智能体更多是比人更快地发现人类会找到但懒得找的问题，并质疑 Strix 相较其他智能体的独特优势。SaucyWrong 以安全工程师经验追问是否事前授权对潜在供应商域名进行红队测试，wxw 仅提及 pen-testing agent。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.baseten.co/overview">Baseten overview - Baseten</a></li>
<li><a href="https://www.linkedin.com/company/baseten">Baseten - LinkedIn</a></li>

</ul>
</details>

**标签**: `#AI security agents`, `#vulnerability disclosure`, `#GitHub token leak`, `#AI infrastructure`, `#Baseten`

---