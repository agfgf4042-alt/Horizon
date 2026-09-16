---
layout: default
title: "Horizon Summary: 2026-09-16 (EN)"
date: 2026-09-16
lang: en
---

> From 47 items, 2 important content pieces were selected

---

**AI Agents &amp; Society**
1. [Project Lily: 404 Media Reports Contractors Read Real ChatGPT Chats](#item-ai-agent-impact-1) ⭐️ 7.0/10
2. [Baseten confirms remediation of reported GitHub token exposure](#item-ai-agent-impact-2) ⭐️ 6.0/10

---

## AI Agents &amp; Society

<a id="item-ai-agent-impact-1"></a>
### [Project Lily: 404 Media Reports Contractors Read Real ChatGPT Chats](https://www.404media.co/inside-project-lily-the-humans-reading-your-chatgpt-chats/) ⭐️ 7.0/10

A 404 Media report says OpenAI is hiring hundreds of contractors to read large numbers of real users’ ChatGPT prompts and full conversations, score model replies, and suggest changes; the material may include sensitive personal information. OpenAI said it tries to remove personal information before reviewers see it, but acknowledged that sensitive details may still be visible. Anthropic also confirmed that it uses human review to improve its models. The report, described in the source as “Project Lily,” raises questions about privacy exposure for ChatGPT users whose chats are reviewed and about how such human review is handled.

telegram · zaihuapd · Sep 15, 11:56

**「Background」** Human review of user interactions sits inside the standard pipeline that large language model developers use to evaluate and improve model outputs: contractors read prompts and responses, rate quality, and flag errors or harmful content. This work is typically staffed through third-party vendors rather than by the AI company&\#x27;s own employees, which places the people doing the reading outside the direct employment relationship with the developer. The 404 Media report situates OpenAI&\#x27;s &quot;Project Lily&quot; and Anthropic&\#x27;s confirmation of similar review within that established practice, and the privacy question turns on how effectively personal information can be stripped from conversations before they reach reviewers.

**「Privacy and Labor Consequences」** People who use ChatGPT — or Anthropic&\#x27;s models — cannot assume their conversations remain only between them and the system: according to the 404 Media report, hundreds of contractors read real prompts and complete conversations to score replies and suggest changes, and OpenAI acknowledges that sensitive details may still be seen even after it tries to strip personal information before review. That creates a plausible privacy risk for users who discuss health, finances, relationships, or other personal matters, since such exposure reaches information people intended to keep private rather than public \(tool-2-1, tool-2-3\). The reporting also points to labor implications for the contractors themselves, whose job is reading large volumes of user conversations, but the supplied evidence documents the arrangement and the companies&\#x27; acknowledgements rather than any confirmed misuse, breach, or harm to an identified person.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Privacy">Privacy - Wikipedia</a></li>
<li><a href="https://simple.wikipedia.org/wiki/Privacy">Privacy - Simple English Wikipedia , the free encyclopedia</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#data privacy`, `#human review`, `#AI contractors`, `#ChatGPT`

---

<a id="item-ai-agent-impact-2"></a>
### [Baseten confirms remediation of reported GitHub token exposure](https://www.strix.ai/blog/baseten-harbor-github-pat-takeover) ⭐️ 6.0/10

Strix published a report claiming its AI agent obtained admin access to Baseten&\#x27;s production GitHub after finding a live \`basetenbot\` token tied to a public Harbor project and repository permissions. In Hacker News comments, Baseten&\#x27;s Philip Kiely said the company collaborated with Strix, invalidated the leaked key, removed the public container image, and that logs confirmed the vulnerability was never exploited and no customer data was exposed. Commenter swyx recounted a timeline: the token and public project were reported July 13 at 11:10 PM; Baseten made Harbor private the morning of July 14 but the token still worked; and at 4:34 PM on July 14, Anton from Baseten Security confirmed the issue as critical, said the project was private and the token rotated, and asked for the downloaded images to be securely deleted. The thread debated whether the agent found anything a motivated human could not and whether scanning a prospective vendor&\#x27;s domain was pre-authorized. The strongest verified evidence is Baseten&\#x27;s own confirmation of remediation and no observed exploitation; the AI-agent capability itself is not independently detailed in the provided material.

hackernews · bearsyankees · Sep 15, 18:11 · [Discussion](https://news.ycombinator.com/item?id=49716476)

**「Context」** Baseten is an AI infrastructure company that provides a platform for model inference and training, including hosted models through an OpenAI-compatible API, dedicated deployments, and management of model containers, GPU capacity, scaling, and observability \(tool-1-1, tool-1-2\). The reported incident involves GitHub credentials and a public container image associated with Baseten&\#x27;s production environment, so understanding the disclosure depends on Baseten&\#x27;s role as an AI infrastructure provider serving customers&\#x27; model workloads \(tool-1-3\).

**「Social impact」** Baseten says no customer data was exposed and logs show the token was never exploited, so direct customer harm is not established. The case still shows a plausible risk for AI infrastructure users: a leaked token linked to a public container project could expose proprietary artifacts or internal systems if detection and rotation lag. It also raises an authorization concern for security engineers and vendors who may be scanned by agentic tools, though the thread does not establish whether Strix&\#x27;s testing of a prospective vendor domain was negotiated in advance.

**「Community discussion」** Commenters accepted Baseten&\#x27;s remediation and praised responsible disclosure, but disputed the agent&\#x27;s significance: ivraatiems argued such agents mainly find many things faster than unmotivated humans would bother to look, and asked what Strix&\#x27;s agent did that Claude or Codex could not. SaucyWrong, a security software engineer, asked whether running Strix against a prospective vendor domain had been pre-negotiated with approval and rules of engagement, while swyx supplied the July 13–14 disclosure timeline and Philip Kiely confirmed no exploitation or customer-data exposure.

<details><summary>References</summary>
<ul>
<li><a href="https://www.baseten.co/about-us/">Meet the engineers behind Baseten</a></li>
<li><a href="https://docs.baseten.co/overview">Baseten overview - Baseten</a></li>
<li><a href="https://www.linkedin.com/company/baseten">Baseten - LinkedIn</a></li>

</ul>
</details>

**Tags**: `#AI security agents`, `#vulnerability disclosure`, `#GitHub token leak`, `#AI infrastructure`, `#Baseten`

---