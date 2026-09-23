---
layout: default
title: "Horizon Summary: 2026-09-23 (EN)"
date: 2026-09-23
lang: en
---

> From 15 items, 10 important content pieces were selected

---

**Technology News**
1. [Jev: LLM-as-Judge Evaluation in 25 Lines of Python](#item-tech-news-1) ⭐️ 7.0/10
2. [Technical memo explains Mixture of Experts fundamentals and modern load-balancing methods](#item-tech-news-2) ⭐️ 6.0/10
3. [New M6 and M5 Pro Mac mini reportedly solder storage, ending third-party upgrades](#item-tech-news-3) ⭐️ 6.0/10
4. [HBM Memory Die Value Per Area Surpasses Leading-Edge Logic Chips](#item-tech-news-4) ⭐️ 6.0/10
5. [JCOM internet outage hits most of Japan](#item-tech-news-5) ⭐️ 5.0/10
6. [Geta.Team: AI &\#x27;employees&\#x27; with dedicated email, phone numbers, and self-hosting](#item-tech-news-6) ⭐️ 5.0/10
7. [ByteDance&\#x27;s Doubao Reportedly Halves General Conversation Team](#item-tech-news-7) ⭐️ 5.0/10
8. [Musk Praises Chinese AI Models, Predicts Compute Gap Closure in 2-3 Years](#item-tech-news-8) ⭐️ 5.0/10

**Technology Blog**
1. [Four Copyright Risks of Generative AI, Grounded in Primary Sources](#item-tech-blog-1) ⭐️ 8.0/10

**Financial News**
1. [China&\#x27;s Self-Sufficiency Shifts Trade Calculus Ahead of Trump-Xi Summit](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Jev: LLM-as-Judge Evaluation in 25 Lines of Python](https://www.nobodywho.ai/posts/jev-in-25-lines/) ⭐️ 7.0/10

A blog post from nobodywho.ai demonstrates &quot;Jev,&quot; an LLM-as-judge evaluation technique implemented in roughly 25 lines of Python that classifies text by reading token logprobs for candidate answer labels rather than parsing generated output. The approach frames classification as a single forward pass, comparing the probabilities the model assigns to each option token. The post drew substantive technical discussion on Hacker News about the method&\#x27;s limitations and possible refinements, though it is a small practical hack rather than a validated evaluation framework.

hackernews · bashbjorn · Sep 23, 07:26 · [Discussion](https://news.ycombinator.com/item?id=49812769)

**「Background」** LLM-as-a-judge is a common evaluation pattern in which a language model classifies or scores outputs instead of relying on hand-written rules, and one lightweight variant reads the model&\#x27;s token logprobs for answer options \(such as &quot;yes&quot; vs &quot;no&quot;\) rather than parsing generated prose. Jev is a recent decision-only judging approach built on this idea: it classifies intent, scores severity, or ranks candidates while leaving generation and reasoning to a full LLM, and a recent arXiv study found such a judge within three percentage points of generative judges while offering a cheaper first pass that escalates low-confidence cases. The post demonstrates how to reproduce this technique in roughly 25 lines of Python.

**「Community Discussion」** Commenters raised several caveats: sigmoid10 warned that chat models are trained to produce prose, so choice-token probabilities can be diluted unless the prompt is carefully constrained, while armcat argued logprob-based scoring has been unreliable on frontier models since GPT-4o and that simply asking the model for confidence correlates better. Antirez suggested concrete improvements, noting that because of causal attention masking, placing options before the input text lets the model build task-specific state, and that few-shot examples or repeating the question can improve calibration; alun separately criticized the post&\#x27;s &quot;System One&quot; framing as a misnomer for what is deliberate classification work.

<details><summary>References</summary>
<ul>
<li><a href="https://dev.to/miruky/jev-does-not-replace-the-llm-it-changes-who-owns-the-decision-3n6">Jev Does Not Replace the LLM. It Changes Who Owns the ...</a></li>
<li><a href="https://arxiv.org/abs/2609.26550">[2609.26550] JEV-as-a-Judge: Accept When Confident, Escalate ...</a></li>

</ul>
</details>

**Tags**: `#llm-evaluation`, `#logprobs`, `#python`, `#prompt-engineering`, `#machine-learning`

---

<a id="item-tech-news-2"></a>
### [Technical memo explains Mixture of Experts fundamentals and modern load-balancing methods](https://iwashi.co/2026/09/23/mixture-of-experts-moe-memo) ⭐️ 6.0/10

A Japanese technical memo by iwashi.co explains the fundamentals of Mixture of Experts \(MoE\) architecture used in recent open-weight LLMs such as DeepSeek-V4.1-Flash, Kimi K3, and MiMo-V2.6. It corrects the common &\#x27;domain expert&\#x27; intuition, clarifying that MoE is simply a sparsely activated architecture where the dense FFN layer of a Transformer block is replaced by router-selected experts, with different experts activated per token. The memo details routing design choices \(token choice, expert choice, global assignment\), the expert collapse problem documented in OLMoE ablations, and the auxiliary load balancing loss from Switch Transformer with a worked numerical example. It then compares modern aux-loss-free approaches: DeepSeek-V3&\#x27;s dynamic per-expert bias, Kimi K3&\#x27;s Quantile Balancing for its 896-expert top-16 configuration, and MiMo-V2.6&\#x27;s similar bias mechanism, noting that MiMo-V2.6&\#x27;s technical report describes routing collapse during reinforcement learning that was fixed by rolling back router parameters.

rss · はてなブックマーク \(テクノロジー\) · Sep 23, 07:32

**「Background」** Mixture of Experts \(MoE\) is a neural network architecture that replaces the dense feed-forward layers of a Transformer with multiple parallel &\#x27;expert&\#x27; subnetworks, activating only a small subset per token via a learned router. This lets models grow total parameter counts into the trillions while keeping per-token compute roughly constant, which is why most recent top-tier open-weight LLMs have adopted it. The technique builds on earlier work such as Switch Transformer, which introduced the auxiliary load-balancing loss that later designs like DeepSeek-V3&\#x27;s bias-based approach sought to replace.

**「Impact」** For practitioners, the memo highlights two operationally relevant facts: MoE inference still requires GPU memory for the full parameter count \(making quantization essential on consumer hardware despite sparse activation\), and shared experts remain a contested design choice, with DeepSeek reporting clear gains while OLMoE found no significant difference and MiMo-V2.6 omits them entirely.

**Tags**: `#mixture-of-experts`, `#llm-architecture`, `#deep-learning`, `#transformers`, `#technical-explainer`

---

<a id="item-tech-news-3"></a>
### [New M6 and M5 Pro Mac mini reportedly solder storage, ending third-party upgrades](https://9to5mac.com/2026/09/22/m6-mac-mini-upgrade-storage-change/) ⭐️ 6.0/10

Teardowns reported by 9to5Mac indicate that the new M6 and M5 Pro Mac mini have their NAND storage chips soldered to the logic board, removing the replaceable storage module design that the M4 Mac mini offered. Buyers must now choose their capacity at purchase, since third-party SSD modules can no longer be installed afterward. The cost gap is significant: Apple charges $500 to go from 256 GB to 1 TB and $1,000 for 2 TB on the M6 Mac mini, while third-party 1 TB and 2 TB modules for the M4 model cost roughly $300 and $420. These findings come from teardown reporting rather than an Apple statement, so they reflect a single source&\#x27;s examination of the hardware.

telegram · zaihuapd · Sep 23, 08:00

**「Background」** Apple&\#x27;s M4 Mac mini, released in 2024, used a removable proprietary SSD module rather than storage soldered directly to the logic board, which allowed third-party vendors to sell cheaper upgrade modules after purchase. Soldered NAND has historically been Apple&\#x27;s approach on most Macs, forcing buyers to pay Apple&\#x27;s higher storage upgrade prices at the time of purchase.

**「Impact」** Prospective Mac mini buyers who previously relied on cheaper third-party storage upgrades now face paying Apple&\#x27;s configuration prices upfront, which run roughly $200 to $580 higher per tier than the third-party modules the M4 model accepted. Users with uncertain future storage needs should factor the full upgrade cost into the initial purchase decision.

**Tags**: `#apple`, `#mac-mini`, `#hardware`, `#storage`, `#right-to-repair`

---

<a id="item-tech-news-4"></a>
### [HBM Memory Die Value Per Area Surpasses Leading-Edge Logic Chips](https://www.tomshardware.com/pc-components/dram/dram-is-now-more-expensive-than-compute-chips-on-per-area-basis-ai-demand-drives-memory-die-value-past-leading-edge-silicon) ⭐️ 6.0/10

AI infrastructure demand for high-bandwidth memory \(HBM\) has pushed the per-unit-area value of memory dies above that of some leading-edge logic chips, according to a Tom&\#x27;s Hardware report. The shift is attributed to HBM&\#x27;s demanding stacking processes, advanced packaging, and stricter yield control, combined with rapidly growing AI accelerator requirements for memory bandwidth and capacity. This reverses the longstanding position of advanced-process logic chips as the highest-value products in the semiconductor industry, though the report does not provide specific pricing figures or name particular chips compared.

telegram · zaihuapd · Sep 23, 11:39

**「Why HBM costs more per area」** HBM stacks multiple DRAM dies vertically using through-silicon vias and advanced packaging, which consumes more silicon area per gigabyte than standard memory and tightens yield requirements. Micron warned at Hot Chips 2026 that this silicon penalty of HBM relative to DDR5 is widening with every generation, and Tom&\#x27;s Hardware reports that per-area memory manufacturing cost can now exceed the price of silicon made on TSMC&\#x27;s N2 and N3 nodes.

**「Impact」** Memory manufacturers such as HBM suppliers gain increased leverage and strategic importance in the AI chip supply chain, which could affect pricing negotiations and capacity allocation for AI accelerator buyers.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/pc-components/dram/dram-is-now-more-expensive-than-compute-chips-on-per-area-basis-ai-demand-drives-memory-die-value-past-leading-edge-silicon">Memory chips are now more expensive than compute chips on a ...</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/micron-says-the-silicon-gap-between-hbm-and-ddr5-is-widening-with-every-generation">Hot Chips 2026: Micron warns HBM wafer penalty is widening ...</a></li>

</ul>
</details>

**Tags**: `#HBM`, `#semiconductors`, `#AI infrastructure`, `#DRAM`, `#chip industry`

---

<a id="item-tech-news-5"></a>
### [JCOM internet outage hits most of Japan](https://news.web.nhk/newsweb/na/nd-20260923de52004) ⭐️ 5.0/10

Japanese cable operator JCOM reported that its internet connection service went down starting around 9 AM on the 23rd, leaving subscribers unable to connect. According to NHK&\#x27;s brief report, the outage affects most of the country, excluding Hokkaido and the Kyushu/Okinawa regions. The report provides no information on the cause, the number of affected users, or an estimated restoration time.

rss · はてなブックマーク \(テクノロジー\) · Sep 23, 07:20

**「Background」** JCOM is one of Japan&\#x27;s largest cable television operators and provides the J:COM NET internet service to subscribers nationwide. According to other Japanese reports on the same incident, the company had not disclosed the cause of the outage or an estimated recovery time, and its customer support lines were difficult to reach.

**「Impact」** JCOM subscribers in the affected regions cannot use their internet service and should monitor JCOM&\#x27;s official announcements for restoration updates, as the report gives no timeline for recovery.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sankei.com/article/20260923-UMFHABPPAJK3DGTY5BIMUXBCGE/">Jcomネットで全国的に接続障害原因調査、復旧は未定 窓口問い合わせもつながりにくく - 産経ニュース</a></li>
<li><a href="https://reaitimenews.com/entry/jcom-network-outage-2026-09-23">J:COMで9月23日朝から全国ネット障害、原因は非公表</a></li>

</ul>
</details>

**Tags**: `#internet-outage`, `#ISP`, `#JCOM`, `#network-infrastructure`, `#japan`

---

<a id="item-tech-news-6"></a>
### [Geta.Team: AI &\#x27;employees&\#x27; with dedicated email, phone numbers, and self-hosting](https://gigazine.net/news/20260923-geta-team/) ⭐️ 5.0/10

Gigazine published a hands-on review of Geta.Team, a service that lets users create AI agents presented as &\#x27;employees&\#x27; with names, job roles, generated profile images, and—in paid tiers—dedicated email addresses and real phone numbers via Twilio integration. The agents have persistent memory across sessions, support scheduled autonomous tasks, connect to Slack, Teams, WhatsApp, Telegram, Discord, Gmail, and Outlook, and can operate a logged-in browser via a Chrome extension or an entire PC via a Windows desktop app. In the review, an agent successfully gathered AI news and drafted social media posts while respecting an instruction to wait for human approval before posting. A free tier offers one AI employee on shared servers with 100 credits per day and no credit card or API key required, while dedicated email, phone, the desktop app, and multiple employees are paid-only; self-hosting is offered as an enterprise deployment to a customer&\#x27;s cloud or data center rather than a public Docker Compose setup.

rss · はてなブックマーク \(テクノロジー\) · Sep 23, 09:22

**「Background」** Geta.Team is part of a recent wave of services that package large language models as persistent &\#x27;AI employees&\#x27; or agents, combining long-term memory, scheduled autonomous tasks, and integrations with email, chat platforms, and browsers to handle routine work. Similar offerings covered by the same outlet include OpenAI&\#x27;s Frontier platform for building enterprise AI workers and Microsoft&\#x27;s always-on agent Scout, reflecting a broader industry push to frame AI agents as delegated staff rather than one-off chatbots.

**「Impact」** For users evaluating the service, the free tier is enough to test core agent behavior—memory, scheduled tasks, skills, and web browsing—without payment details, but the features that make agents act like standalone staff \(their own email address and phone number, plus full PC control\) require a paid plan, and organizations wanting on-premises deployment must go through the enterprise channel rather than self-installing from a published compose file.

**Tags**: `#AI agents`, `#automation`, `#product review`, `#self-hosting`, `#SaaS`

---

<a id="item-tech-news-7"></a>
### [ByteDance&\#x27;s Doubao Reportedly Halves General Conversation Team](https://mp.weixin.qq.com/s/a50_mhFCB9n8WdmRFVx_lA) ⭐️ 5.0/10

ByteDance&\#x27;s AI app Doubao, which reports over 200 million daily active users, is shrinking its conversational AI teams, according to a LatePost report relayed via Telegram. The general Session team of roughly 50 people is expected to be cut by about half, with some staff transferred to Doubao&\#x27;s commercialization unit or Feishu and the rest laid off; the post-training team for conversation products is also being reduced. The restructuring is tied to commercialization bottlenecks: after paid-tier plans surfaced in April, users complained that Doubao&\#x27;s answers had become &quot;dumb and sycophantic,&quot; prompting the company to accept a short-term retention drop of under 1% to fix the experience. These are reported figures from a single secondhand source and have not been independently confirmed.

telegram · zaihuapd · Sep 23, 06:18

**「Background」** Doubao is ByteDance&\#x27;s flagship consumer AI chatbot app, which the source describes as having surpassed 200 million daily active users, making it one of China&\#x27;s largest AI applications. In April of this year, reports of a paid tier triggered user complaints that Doubao&\#x27;s answers had become &quot;dumb and sycophantic,&quot; prompting the company to accept a short-term retention dip of under 1% to correct the experience. The reported team cuts, originally covered by LatePost, come as conversational AI products face pressure to find viable commercialization paths.

**「Impact」** For affected employees, the report indicates transfers to commercialization or Feishu teams for some and layoffs for the rest, while the post-training cuts suggest ByteDance is deprioritizing general-purpose chat quality work in favor of monetization. If accurate, the episode illustrates a concrete trade-off for large-scale chatbot operators: tuning models for engagement or paid conversion can degrade perceived answer quality enough to force a corrective retreat.

**Tags**: `#AI industry`, `#ByteDance`, `#Doubao`, `#layoffs`, `#chatbot commercialization`

---

<a id="item-tech-news-8"></a>
### [Musk Praises Chinese AI Models, Predicts Compute Gap Closure in 2-3 Years](https://weibo.com/2258727970/RjqEdvjne) ⭐️ 5.0/10

In an interview with CCTV Finance, Tesla CEO Elon Musk said Chinese AI large models are &quot;overall very impressive,&quot; claiming their performance per unit of compute is nearly world-leading. He predicted China would solve its compute constraints faster than most expect, estimating that within roughly two to three years the country could close its compute gap through lithography and chip manufacturing advances. These are Musk&\#x27;s stated opinions in a media interview, not measured benchmarks or announced technical milestones, and the report circulating via Telegram and Weibo provides no additional technical detail.

telegram · zaihuapd · Sep 23, 07:20

**「Background」** Musk&\#x27;s remarks refer to China&\#x27;s well-documented AI compute constraint: US export controls have restricted Chinese firms&\#x27; access to advanced GPUs and the EUV lithography equipment needed to manufacture cutting-edge chips domestically, forcing Chinese AI labs to emphasize compute efficiency. His comments were made in a CCTV Finance interview and relayed by multiple Chinese outlets, which report the same quotes without additional technical detail or independent verification.

**「Impact」** The prediction is a high-profile endorsement of China&\#x27;s AI efficiency narrative, but it carries no actionable detail: no specific models, chips, or fabrication processes were named, so readers should treat the two-to-three-year timeline as one executive&\#x27;s estimate rather than a verified forecast.

<details><summary>References</summary>
<ul>
<li><a href="https://m.21jingji.com/article/20260923/herald/557254d0058ed7533d516224b161aeb7.html">马斯克惊叹中国AI大模型“单位算力产出性能几乎是全球顶尖水平”，预计两到三年内就能靠光刻技术与芯片制造补齐算力缺口 - 21财经</a></li>
<li><a href="https://tech.ifeng.com/c/8wbYxCAilw3">马斯克：中国AI大模型单位算力产出近全球顶尖，2-3年补齐算力缺口_凤凰网</a></li>

</ul>
</details>

**Tags**: `#AI`, `#China tech`, `#semiconductors`, `#compute`, `#industry news`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Four Copyright Risks of Generative AI, Grounded in Primary Sources](https://qiita.com/songchong/items/7306e0b1a9207e08d86e?utm_campaign=popular_items&amp;utm_medium=feed&amp;utm_source=popular_items) ⭐️ 8.0/10

rss · Qiita \(人気記事\) · Sep 23, 07:45

**「Background」** A common sales pitch claims generative AI output is a novel creation of probabilistically arranged words, so it cannot infringe copyright. The author tests this claim against three primary sources: two LLM memorization papers, Japan&\#x27;s Agency for Cultural Affairs 2024 guidance on AI and copyright, and OpenAI&\#x27;s enterprise Services Agreement.

**「Solution」** The author identifies four risks. First, memorization: Carlini et al. \(USENIX Security 2021\) extracted hundreds of verbatim training strings from GPT-2—including code and strings appearing in only one training document—and Nasr et al. \(2023\) showed alignment techniques like RLHF do not eliminate memorization, though both studies used deliberate extraction attacks rather than normal use. Second, user liability: the Cultural Affairs guidance \(non-binding\) separates training from output use; training is generally permitted under Article 30-4 unless the purpose includes reproducing expression \(e.g., RAG built to regurgitate source text\), and if output resembles a work the model trained on, reliance is &\#x27;normally presumed&\#x27; even if the user never knew the work. Third, weak ownership: AI cannot be an author, and OpenAI&\#x27;s contract assigns rights only &\#x27;if any,&\#x27; noting outputs may not be unique. Fourth, indemnification limits: OpenAI&\#x27;s §13.1 lists four exclusions \(combinations, modifications, customer content—which includes inputs and outputs—and customer apps\), while §12.2 disclaims any non-infringement warranty. Countermeasures follow: check outputs against existing works before use, avoid training/RAG designed to reproduce others&\#x27; expression, document human creative contributions, and have legal counsel map contract exclusions to your integration.

**「Takeaway」** The author concludes that &\#x27;probabilistic generation&\#x27; does not guarantee non-infringement: memorized text can surface verbatim, users can bear liability, outputs may be unprotectable, and vendor indemnification is narrower than marketed. Safe adoption requires verifying outputs, preserving human authorship records, and reading contract exclusions against your own architecture.

**Tags**: `#generative-ai`, `#copyright-law`, `#llm-memorization`, `#vendor-contracts`, `#risk-management`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s Self-Sufficiency Shifts Trade Calculus Ahead of Trump-Xi Summit](https://www.cnbc.com/2026/09/23/trump-xi-meeting-why-chinas-self-sufficiency-changes-the-calculus.html) ⭐️ 7.0/10

Ahead of a Trump-Xi summit this week, CNBC reports that China&\#x27;s push for self-sufficiency and the world&\#x27;s continued reliance on Chinese goods have blunted U.S. tariff leverage, with businesses hoping at best for an extension of last fall&\#x27;s trade truce. Despite tariffs, the U.S. trade deficit with China has risen again this year on surging demand for AI-related parts, and China reached 40% of global container exports this summer—a milestone the European Chamber of Commerce in China had not expected until 2030.

rss · CNBC Finance · Sep 23, 09:13

**「Background」** China&\#x27;s property downturn, which began in 2022, weakened domestic demand and pushed its companies to expand exports aggressively, while U.S. tariffs imposed since last year have failed to significantly shrink the bilateral trade deficit.

**「Impact」** China&\#x27;s domestic weakness is spilling abroad: the American Chamber of Commerce in Shanghai says three-quarters of surveyed members now see Chinese rivals as more advanced, and the EU—which runs the largest trade deficit with China—is stepping up scrutiny of Chinese exports, with its trade commissioner expected in Beijing next month.

**Tags**: `#US-China trade`, `#Trump-Xi summit`, `#tariffs`, `#China economy`, `#AI exports`

---