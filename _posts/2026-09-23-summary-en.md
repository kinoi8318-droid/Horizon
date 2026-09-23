---
layout: default
title: "Horizon Summary: 2026-09-23 (EN)"
date: 2026-09-23
lang: en
---

> From 41 items, 22 important content pieces were selected

---

**Technology News**
1. [Anthropic launches Claude Opus 5.5 with 40% lower cost](#item-tech-news-1) ⭐️ 9.0/10
2. [Trail of Bits dissects SAML&\#x27;s compounding design flaws](#item-tech-news-2) ⭐️ 8.0/10
3. [WordPress patches unauthenticated path traversal enabling conditional RCE](#item-tech-news-3) ⭐️ 8.0/10
4. [Pentagon report blames AI overreliance for strike on Iranian school](#item-tech-news-4) ⭐️ 8.0/10
5. [Claude Opus 5.5 and GPT-6 Sol/Luna launch with steep price cuts](#item-tech-news-5) ⭐️ 8.0/10
6. [OpenAI Announces GPT-6 Sol and Luna Models](#item-tech-news-6) ⭐️ 7.0/10
7. [ShinyHunters claims breach of FBI systems and employee data](#item-tech-news-7) ⭐️ 7.0/10
8. [FoxScript: MIT-licensed Visual FoxPro reimplementation on Rust/WebAssembly](#item-tech-news-8) ⭐️ 7.0/10
9. [Artificial Analysis Benchmarks Claude Opus 5.5 at Half the Cost per Task](#item-tech-news-9) ⭐️ 7.0/10
10. [Nathan Lambert&\#x27;s congressional testimony on open-weight model competition](#item-tech-news-10) ⭐️ 7.0/10
11. [Kamipo on Rails 2026: ActiveRecord SQL Generation Internals](#item-tech-news-11) ⭐️ 7.0/10
12. [25 Fields Medalists Accuse OpenAI of Appropriating Mathematical Results](#item-tech-news-12) ⭐️ 7.0/10
13. [Xbox cuts 268 more jobs, hands next Halo to Activision](#item-tech-news-13) ⭐️ 7.0/10
14. [Qualcomm Unveils Snapdragon 8 Elite Extreme Gen 6 Platform](#item-tech-news-14) ⭐️ 7.0/10
15. [llm 0.36 adds GPT-6 models and single-turn plugin support](#item-tech-news-15) ⭐️ 6.0/10
16. [HarnessRouter Community Edition: Self-Hosted Unified API for Agent Harnesses](#item-tech-news-16) ⭐️ 6.0/10
17. [US criticises Australia&\#x27;s algorithm opt-out and duty of care bills as censorship](#item-tech-news-17) ⭐️ 5.0/10
18. [Anthropic publishes usage guide for Opus 5.5 in Claude and Claude Code](#item-tech-news-18) ⭐️ 5.0/10
19. [OpenAI to Allow Earlier Third-Party Safety Evaluations of AI Models](#item-tech-news-19) ⭐️ 5.0/10
20. [Apple Reportedly Prototyping Screenless Whoop-Style Fitness Band](#item-tech-news-20) ⭐️ 5.0/10

**Financial News**
1. [China Reportedly Tells Banks Not to Classify Vanke&\#x27;s Overdue Loans as Bad Debt](#item-finance-news-1) ⭐️ 7.0/10
2. [CFTC Warns Prediction-Market &\#x27;Mentions&\#x27; Contracts Carry Higher Manipulation Risk](#item-finance-news-2) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Anthropic launches Claude Opus 5.5 with 40% lower cost](https://www.anthropic.com/claude-opus-5-5) ⭐️ 9.0/10

Anthropic has released Claude Opus 5.5, the first model in its Claude 5.5 family, claiming performance comparable to Claude Fable 5.1 on most work at 40% lower cost than Opus 5 on typical workloads. Pricing drops to $4 per million input tokens and $20 per million output tokens \(from $5/$25\), with cache reads cut 60% to $0.20 per million, and output generation is over 30% faster. Anthropic reports Opus 5.5 leads its benchmarks in agentic coding, computer use, and knowledge work, and scored best of any model it has tested on its internal automated behavioral audit, with pre-release testing by external evaluators Frontier Design and METR. Because Anthropic assesses it as comparable to Claude Mythos 5.1 in biology and cybersecurity capability, it ships with Fable 5.1-style safeguards, and vetted organizations can apply to the Life Sciences Verification Program now, with Cyber Verification Program access expanding in coming weeks; Sonnet 5.5 and Haiku 5.5 are also due in the coming weeks.

rss · はてなブックマーク \(テクノロジー\) · Sep 22, 16:34 · [Discussion](https://news.ycombinator.com/item?id=49803892)

**「Background」** Claude Opus 5.5 succeeds Opus 5 as Anthropic&\#x27;s flagship model and is the first release in the Claude 5.5 family, with Sonnet 5.5 and Haiku 5.5 announced to follow. Anthropic describes it as its first release since publicly calling for pacing the frontier, and says it was evaluated before release by external organizations including Frontier Design and METR. Because Anthropic assesses Opus 5.5 as comparable to Claude Mythos 5.1 in biology and cybersecurity capability, it is being deployed under safeguards similar to those used for Claude Fable 5.1, with gated access programs for life sciences and cybersecurity work.

**「Impact」** For existing Opus 5 users, the release is a direct cost and speed upgrade: Anthropic says typical workloads cost 40% less, and Pro, Max, Team, and seat-based Enterprise plans get increased five-hour usage limits plus a saveable rate limit reset. Developers using Claude Code or the Claude Platform can also opt into a fast mode at up to 2.5x speed for $8/$40 per million input/output tokens, a premium tier for latency-sensitive work.

**「Community Discussion」** Commenters noted the irony that Anthropic opened the announcement by referencing its recent call to &\#x27;pace the frontier&\#x27; while the rest of the post details rapid capability and efficiency gains. Others welcomed the price cut—one noted Opus 5 was the highest-spend model on OpenRouter—while some users said cheaper alternatives like DeepSeek v4.1 already meet their coding needs.

**Tags**: `#anthropic`, `#claude`, `#llm`, `#ai-models`, `#model-release`

---

<a id="item-tech-news-2"></a>
### [Trail of Bits dissects SAML&\#x27;s compounding design flaws](https://blog.trailofbits.com/2026/09/21/saml-a-fractal-of-bad-design/) ⭐️ 8.0/10

Trail of Bits published a critique of SAML arguing that the enterprise SSO standard is a compounding series of design failures rooted in XML-era complexity, including its reliance on XML canonicalization and signature validation. The post frames these flaws as structural rather than implementation-specific, affecting anyone who operates or integrates SAML-based single sign-on. The analysis is a vendor blog critique rather than a disclosure of a new vulnerability.

hackernews · aray07 · Sep 22, 18:57 · [Discussion](https://news.ycombinator.com/item?id=49806335)

**「Background」** SAML \(Security Assertion Markup Language\) is an XML-based single sign-on standard from the early 2000s that remains widely deployed in enterprise identity federation, built by merging multiple existing specifications into what critics call a &\#x27;kitchen-sink&\#x27; design. Its reliance on XML signatures and canonicalization has produced a long history of implementation vulnerabilities, notably XML signature wrapping attacks, which the Trail of Bits post argues are symptoms of compounding design failures rather than isolated bugs.

**「Community Discussion」** Commenter bawolff recounted that the main C implementation of xmlsig once, by default, also validated signatures against an HMAC using an attacker-controlled password from the document and against web PKI, letting an attacker sign a SAML response with their own domain&\#x27;s TLS key. Others debated SAML versus OIDC: cameronh90 argued SAML still offers enterprise features OIDC lacks, notably IdP-initiated flow, and that OIDC&\#x27;s constellation of specs has inconsistent support, while cryptonector contended canonicalization problems should be avoided by validating signatures over the exact received bytes before decoding.

<details><summary>References</summary>
<ul>
<li><a href="https://thenote.app/post/en/saml-a-fractal-of-bad-design-puhir0xvn6">SAML: A fractal of bad design - thenote.app</a></li>

</ul>
</details>

**Tags**: `#SAML`, `#authentication`, `#security`, `#SSO`, `#XML`

---

<a id="item-tech-news-3"></a>
### [WordPress patches unauthenticated path traversal enabling conditional RCE](https://github.com/WordPress/wordpress-develop/security/advisories/GHSA-7hp8-65ch-5whp) ⭐️ 8.0/10

WordPress disclosed an unauthenticated path traversal vulnerability in core that can lead to conditional remote code execution. The fix shipped in WordPress 7.1.2 and was backported to all branches back to 4.7, covering the vast majority of supported installs. The RCE is described as conditional, meaning exploitation depends on specific site configuration rather than working universally.

hackernews · vntok · Sep 22, 16:33 · [Discussion](https://news.ycombinator.com/item?id=49803959)

**「Background」** WordPress core&\#x27;s locate\_template\(\) function resolves template files from the active theme, parent theme, or /wp-includes directories, and a nine-year-old note on its official documentation page has long warned that it does not prevent directory traversal when given user-provided template names. WordPress powers a large share of websites, and commenters note that roughly a third of installs are not on the current 7.x branch, which is why the fix was backported to all branches back to 4.7.

**「Impact」** Any WordPress site reachable on the public internet should update to 7.1.2 or the corresponding patched point release for its branch immediately, since the vulnerability requires no authentication. Site operators on older branches \(4.7 through 7.0\) can apply the backported fix without a major version upgrade.

**「Community Discussion」** Commenter chrismorgan identified the specific patch by comparing the 7.1.1 and 7.1.2 trees, and vntok noted that a nine-year-old documentation comment already warned that locate\_template\(\) does not prevent directory traversal when passed user-provided template names. Others, including beezle, pointed out that roughly a third of installs are not on the recent 7 branch, making the backports significant, while zelphirkalt and random\_savv expressed broader frustration with WordPress&\#x27;s security track record.

**Tags**: `#wordpress`, `#security`, `#rce`, `#path-traversal`, `#vulnerability`

---

<a id="item-tech-news-4"></a>
### [Pentagon report blames AI overreliance for strike on Iranian school](https://www.bloomberg.com/graphics/2026-iran-school-attack/) ⭐️ 8.0/10

A Pentagon investigation concluded that overreliance on AI-generated target recommendations contributed to a U.S. missile strike on a school in Minab, Iran. The site had been cataloged as an Islamic Revolutionary Guard Corps facility based on outdated data, and was fed into the Project Maven targeting system, which surfaced it as a recommended day-one target—compressing target-list work that once took hours into minutes. The report found the U.S. &quot;failed in its obligation to do everything feasible to verify&quot; the school was a military objective, that the failure &quot;went beyond mere negligence,&quot; and that strikes were directed at the building despite awareness of a substantial risk it was a civilian object.

hackernews · devonnull · Sep 22, 19:03 · [Discussion](https://news.ycombinator.com/item?id=49806430)

**「Background」** The strike occurred on February 28, 2026, the first day of the U.S.-Iran war, when Tomahawk cruise missiles hit the Shajareh Tayyebeh elementary school in Minab, southern Iran, killing more than 150 people, including at least 123 children. The site had been cataloged as an Islamic Revolutionary Guard Corps facility based on outdated data and was fed into the Pentagon&\#x27;s Project Maven AI targeting system, which surfaced it as a recommended day-one target. Following the investigation, the military modified its AI and lethal targeting processes, including refining target-vetting procedures and adding open-source data feeds to better track civilian objects, while Palantir added features making Maven re-review underlying intelligence for disqualifying factors.

**「Impact」** The findings establish an official accountability precedent for AI-assisted targeting: the Pentagon&\#x27;s own report frames the failure as reckless disregard of verification obligations rather than a technical glitch, which strengthens the case that human operators remain legally responsible for validating algorithmically recommended targets before strikes are authorized.

**「Community Discussion」** Commenters argued the AI itself was not the true culprit, pointing to the report&\#x27;s language that the failure to verify &quot;went beyond mere negligence&quot; and that commanders acted recklessly despite knowing the risk of hitting a civilian object. Others criticized the optimization of targeting speed—condensing hours of target-list work into minutes—as the wrong metric, and one commenter cited a separate reported incident where AI incorrectly flagged a Chinese vessel as carrying nuclear weapons materiel.

<details><summary>References</summary>
<ul>
<li><a href="https://www.militarytimes.com/news/your-military/2026/03/24/deadly-iran-school-strike-casts-shadow-over-pentagons-ai-targeting-push/">Deadly Iran school strike casts shadow over Pentagon’s AI ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-09-22/us-military-modifies-ai-combat-targeting-after-iran-minab-school-strike">US Military Modifies AI, Combat Targeting After Iran Minab ...</a></li>
<li><a href="https://aiweekly.co/alerts/pentagon-rewires-palantir-maven-after-iran-school-strike">Pentagon Rewires Palantir Maven After Iran School Strike | AI ...</a></li>

</ul>
</details>

**Tags**: `#AI in military`, `#algorithmic targeting`, `#AI accountability`, `#defense technology`, `#automation risk`

---

<a id="item-tech-news-5"></a>
### [Claude Opus 5.5 and GPT-6 Sol/Luna launch with steep price cuts](https://simonwillison.net/2026/Sep/22/opus-and-sol-and-luna/) ⭐️ 8.0/10

Anthropic released Claude Opus 5.5 and OpenAI released GPT-6 Sol and GPT-6 Luna within an hour of each other, and Simon Willison&\#x27;s early impressions focus on an aggressive pricing shift. GPT-6 Luna costs $0.10/M input and $0.50/M output—half the promotional price of GPT-5.6 Luna, which faces a scheduled 25% increase in November—while GPT-6 Sol dropped to $2/M input and $10/M output, matching Grok 4.7 on input price. Claude Opus 5.5 is priced at $4/M input and $20/M output, a 20% cut from the $5/$25 price shared by Opus 4.5 through 5.0, with cache reads down 60%, which matters for long agentic conversations. Willison also reports a practical failure: Opus 5.5 at &\#x27;max&\#x27; thinking level exhausted its 128,000-token output limit while reasoning about his pelican SVG test, twice, costing $2.56 and nearly 20 minutes per attempt, leading him to distrust the max setting.

rss · Simon Willison · Sep 22, 23:46

**「Background」** Anthropic&\#x27;s Claude Opus line and OpenAI&\#x27;s GPT series are the flagship large language model families that developers access via paid APIs, with pricing quoted per million input and output tokens. Prior Opus versions \(4.5 through 5\) held steady at $5/$25 per million tokens, while OpenAI&\#x27;s GPT-5.6 generation had been sold at promotional prices with a scheduled 25% increase set for November. Simon Willison is a widely followed independent developer who tests new models with benchmarks like his &\#x27;pelican riding a bicycle&\#x27; SVG prompt.

**「Impact」** Developers building on LLM APIs can now run workloads on GPT-6 Luna at one-tenth the price of Claude Haiku 4.5 \($1/$5\), putting immediate pressure on Anthropic&\#x27;s lower-end competitiveness ahead of its announced Sonnet 5.5 and Haiku 5.5 releases. Users of Opus 5.5 should avoid the &\#x27;max&\#x27; thinking level for now, since Willison&\#x27;s testing shows it can over-reason until it hits the output cap and returns nothing while still incurring full cost.

**Tags**: `#llm`, `#openai`, `#anthropic`, `#model-pricing`, `#ai-industry`

---

<a id="item-tech-news-6"></a>
### [OpenAI Announces GPT-6 Sol and Luna Models](https://openai.com/index/introducing-gpt-6-sol-and-luna/) ⭐️ 7.0/10

OpenAI has announced two new flagship models, GPT-6 Sol and GPT-6 Luna, according to an OpenAI blog post shared on Hacker News. The original announcement text was not available, so specific capabilities, benchmarks, and official pricing cannot be confirmed from the supplied material. Community discussion indicates that GPT-6 Luna is priced at half the cost of its predecessor, referred to as GPT-5.6 Luna, and that the lineup also includes variants discussed as GPT-6 Astra and a higher-tier Sol configuration.

hackernews · OfficialTurkey · Sep 22, 18:00 · [Discussion](https://news.ycombinator.com/item?id=49805509)

**「Background」** GPT-6 Sol and Luna are follow-ons to GPT-6 Astra, OpenAI&\#x27;s earlier GPT-6 model, and are positioned as faster, more affordable variants that carry over much of Astra&\#x27;s capability for scaled workloads. OpenAI attributes the lower serving costs to improvements in caching and inference infrastructure, and the models are available across the API, Codex, and ChatGPT.

**「Impact」** If the reported 50% price cut on GPT-6 Luna is accurate, developers running high-volume API workloads or coding agents on OpenAI models would see a meaningful reduction in per-token costs, though the exact pricing tiers and rate limits remain unverified without the announcement text.

**「Community Discussion」** Simon Willison highlighted the Luna price cut as significant and shared SVG-generation test outputs comparing the new models, while other commenters weighed subscription tradeoffs: one user praised Codex Pro&\#x27;s effectively unmetered ChatGPT usage compared to Claude Code&\#x27;s limits, and another expressed concern that a successor to 5.6 Sol might lose the conversational &\#x27;feel&\#x27; that made it effective for agentic coding work. These are individual experiences and preferences, not measured comparisons of the new models.

<details><summary>References</summary>
<ul>
<li><a href="https://community.openai.com/t/announcing-gpt-6-sol-and-gpt-6-luna-in-the-api-codex-and-chatgpt/1399925">Announcing GPT-6 Sol and GPT-6 Luna in the API, Codex and ChatGPT - Announcements - OpenAI Developer Community</a></li>
<li><a href="https://openai.com/index/introducing-gpt-6-sol-and-luna/">Introducing GPT-6 Sol and Luna | OpenAI</a></li>

</ul>
</details>

**Tags**: `#openai`, `#llm`, `#gpt-6`, `#ai-models`, `#pricing`

---

<a id="item-tech-news-7"></a>
### [ShinyHunters claims breach of FBI systems and employee data](https://www.404media.co/we-hacked-the-fbi-hackers-say-they-have-data-on-all-fbi-employees/) ⭐️ 7.0/10

The hacking group ShinyHunters claims it breached FBI systems, defaced an FBI website with a message reading &quot;this site has been seized by ShinyHunters,&quot; and obtained data on all FBI employees, according to a 404 Media report. A representative of the group said the operation was &quot;not financially motivated,&quot; describing their plans as &quot;coercion&quot; rather than extortion. These remain unverified claims by the attackers; the report does not include independent confirmation from the FBI or evidence that the full employee dataset was actually exfiltrated.

hackernews · spenvo · Sep 22, 17:46 · [Discussion](https://news.ycombinator.com/item?id=49805278)

**「Background」** ShinyHunters is a hacking group known for data breaches and extortion campaigns against companies and organizations, typically stealing databases and threatening to leak or sell them. In this case, the group defaced an FBI-affiliated site with a seizure notice and claimed to hold data on all FBI employees, while telling reporters its motives were coercive rather than financial; the claims remain unverified hacker assertions.

**「Impact」** If the claims hold, exposed personal data on FBI employees could endanger agents and staff, but readers should treat the scope as unproven until the FBI or independent researchers confirm it, since hacker groups routinely exaggerate breach claims for attention or leverage.

**「Community Discussion」** Commenters expressed broad cynicism about government data security, with one citing the 2015 OPM breach of 22.1 million federal employee records as precedent for assuming such data is already compromised. Others shared screenshots and the full text of ShinyHunters&\#x27; defacement notice, while some speculated about the group&\#x27;s motives and the FBI&\#x27;s staffing decisions.

**Tags**: `#cybersecurity`, `#data-breach`, `#FBI`, `#ShinyHunters`, `#hacking`

---

<a id="item-tech-news-8"></a>
### [FoxScript: MIT-licensed Visual FoxPro reimplementation on Rust/WebAssembly](https://foxscript.org/) ⭐️ 7.0/10

A developer has released FoxScript, an MIT-licensed reimplementation of Visual FoxPro built on a Rust runtime compiled to WebAssembly, with behavior checked against the original vfp9.exe. It removes the 2 GB table size limit, still loads legacy 32-bit .fll add-ins, and adds lambdas, JSON support, and an HTTP server. The project is unfinished: reports are not implemented and builds are unsigned. The stated motivation is keeping decades-old 32-bit FoxPro business applications running without a full rewrite.

hackernews · boredjohnny · Sep 22, 21:00 · [Discussion](https://news.ycombinator.com/item?id=49808023)

**「Background」** Microsoft ended Visual FoxPro at version 9 in 2007, but many business applications built on it remain in production because rewriting them is risky and expensive. Those apps typically run as 32-bit Windows software with file-based tables, which makes them increasingly awkward to maintain on modern infrastructure.

**「Impact」** Organizations maintaining legacy FoxPro applications gain a potential migration path that preserves existing code and .fll add-ins while lifting the 2 GB table cap, though the missing report engine and unsigned builds mean it is not yet a drop-in production replacement.

**「Community Discussion」** Commenter mikestew raised a concrete security concern: FoxPro Database Containers must be read/write for all users and store stored procedures as plain text, so anyone with technical knowledge could modify a trigger to execute arbitrary code, a flaw any revival inherits. Other commenters shared experiences with multi-user file-locking problems in networked FoxPro apps, reinforcing why some businesses eventually moved to client/server architectures.

**Tags**: `#visual-foxpro`, `#legacy-systems`, `#rust`, `#webassembly`, `#open-source`

---

<a id="item-tech-news-9"></a>
### [Artificial Analysis Benchmarks Claude Opus 5.5 at Half the Cost per Task](https://artificialanalysis.ai/models/claude-opus-5-5) ⭐️ 7.0/10

Artificial Analysis has published independent benchmark results for Anthropic&\#x27;s Claude Opus 5.5, covering intelligence, performance, and price across multiple reasoning effort settings \(medium, xhigh, and max\). According to the analysis, Opus 5.5 delivers roughly half the cost per task compared to its predecessor Opus 5 when comparing high-effort to high-effort settings. The results are third-party benchmark measurements rather than vendor claims, though the max reasoning setting can consume the full 128,000-token budget on some tasks.

hackernews · theanonymousone · Sep 22, 16:51 · [Discussion](https://news.ycombinator.com/item?id=49804316)

**「Background」** Artificial Analysis is an independent benchmarking site that evaluates large language models on intelligence, speed, and cost, publishing per-model pages for each reasoning effort setting. Claude Opus 5.5 is Anthropic&\#x27;s flagship model and the successor to Opus 5, against which the reported cost-per-task comparison is made. Anthropic&\#x27;s Claude models expose configurable reasoning effort levels—such as medium \(the default\), xhigh, and max—which trade token budget and latency against answer quality, so benchmark results are reported separately for each setting.

**「Impact」** For teams paying for frontier-model API access, a halved cost per task at equivalent reasoning effort directly reduces operating costs, but commenters caution that benchmark scores at launch may not hold: one developer reported a model&\#x27;s performance regressing on an internal dataset weeks after release, suggesting users should re-run their own evaluations over time before committing to a switch.

**「Community Discussion」** Commenters debated whether frontier models justify their price, with one arguing they are only slightly better than open-weight models while costing around 100x as much, making &\#x27;good enough&\#x27; open models the likely winners. Others shared practical concerns: simonw noted the max reasoning setting twice exhausted its 128,000-token budget mid-task, and one user reported reverting to Opus 4.8 because Opus 5 lost track of instructions mid-problem, hoping 5.5 fixes that behavior.

**Tags**: `#llm-benchmarks`, `#claude`, `#ai-models`, `#cost-analysis`, `#artificial-analysis`

---

<a id="item-tech-news-10"></a>
### [Nathan Lambert&\#x27;s congressional testimony on open-weight model competition](https://www.interconnects.ai/p/the-current-balance-of-power-in-open) ⭐️ 7.0/10

Nathan Lambert of the Allen Institute for AI \(Ai2\), author of the RLHF book, delivered a prepared statement to the US Congress assessing the shifting balance of power between American and Chinese open-weight AI models. The testimony argues that open models carry strategic importance for the United States as Chinese labs have closed much of the capability gap. This is policy analysis and synthesis rather than a new technical result, and the full statement text was not included in the source material.

hackernews · gmays · Sep 22, 22:03 · [Discussion](https://news.ycombinator.com/item?id=49808816)

**「Background」** Nathan Lambert is a researcher at the Allen Institute for AI \(Ai2\) and the author of the RLHF Book, a widely referenced resource on reinforcement learning from human feedback. Open-weight models, whose parameters can be downloaded and run independently, have become a focal point of US-China technology competition, with Chinese labs such as DeepSeek and Qwen releasing competitive models that have narrowed the gap with American offerings. This piece is Lambert&\#x27;s prepared congressional testimony arguing that open models carry strategic importance for the United States.

**「Community Discussion」** Commenters largely welcomed the testimony reaching US leadership, with one practitioner arguing enterprises handling sensitive data like bank statements cannot risk closed models and therefore need open ones. Another commenter suggested global users adopt Chinese open models partly out of fear that American providers could withdraw access, while others wished the testimony had covered OpenAI&\#x27;s gpt-oss family or comparative training spending, which they noted is likely impossible to collect.

**Tags**: `#open-weight-models`, `#ai-policy`, `#llm`, `#us-china-competition`, `#ai-industry`

---

<a id="item-tech-news-11"></a>
### [Kamipo on Rails 2026: ActiveRecord SQL Generation Internals](https://speakerdeck.com/kamipo/kamipo-on-rails-2026) ⭐️ 7.0/10

Rails committer kamipo published slides explaining how ActiveRecord generates SQL for eager loading and associations, aimed at Rails developers who want to understand or debug its query output. The deck covers three internals with references to specific upstream rails/rails pull requests: deduplication of JOINs through has\_many :through associations so aliased joins do not multiply \(rails/rails\#40000\), alias-aware WHERE clauses where conditions like \`includes\(:children\).where\(&quot;children.label&quot;: &quot;child&quot;\)\` match the JOIN alias rather than rewriting the WHERE clause afterward \(rails/rails\#40106\), and the semantic difference between JOIN-based filtering and EXISTS/IN subqueries, where correlated NOT EXISTS avoids row duplication and works across multiple intermediate tables \(rails/rails\#58810\). The material is conference slide content in Japanese, so it assumes familiarity with ActiveRecord and provides limited standalone narrative context.

rss · はてなブックマーク \(テクノロジー\) · Sep 22, 21:43

**「Background」** ActiveRecord, Rails&\#x27; ORM, generates SQL for associations and eager loading \(includes/preload\), and its handling of JOIN aliases and deduplication has long been a source of subtle bugs when queries mix joins with string or hash conditions. The slides are by kamipo, a Rails committer known for work on ActiveRecord&\#x27;s SQL generation, and reference specific upstream rails/rails pull requests \(\#40000, \#40106, \#58810\) that changed how through-association JOINs are deduplicated, how WHERE clauses align with JOIN aliases, and how correlated NOT EXISTS subqueries replace multi-hop JOINs.

**「Impact」** For Rails developers troubleshooting surprising queries, the slides clarify a concrete behavioral difference: JOIN-based filtering can duplicate parent rows when multiple children match, whereas EXISTS/IN subqueries only test for the existence of a match, which matters when choosing how to express association filters.

**Tags**: `#rails`, `#activerecord`, `#sql`, `#ruby`, `#database-internals`

---

<a id="item-tech-news-12"></a>
### [25 Fields Medalists Accuse OpenAI of Appropriating Mathematical Results](https://www.nikkei.com/article/DGXZQOGN221FZ0S6A920C2000000/) ⭐️ 7.0/10

Twenty-five Fields Medal winners issued a statement on the 11th criticizing OpenAI, warning that the company&\#x27;s approach to AI-driven mathematics could harm academic knowledge sharing. Martin Hairer, a Fields medalist and professor at EPFL in Switzerland, signed the statement and accused the AI company of appropriating researchers&\#x27; results, saying such practices impede the open exchange of knowledge. The Nikkei report describes growing friction between OpenAI, which has been applying AI to difficult mathematical problems, and the mathematics community. The full text of the statement and the specific incidents cited are not visible in the paywalled article, so the precise basis for the criticism cannot be independently assessed from the available material.

rss · はてなブックマーク \(テクノロジー\) · Sep 23, 00:21

**「Background」** The statement referenced in the article is a declaration titled &quot;A Severe Misalignment of AI in Mathematics,&quot; published on September 11, 2026, and signed by 25 Fields Medal recipients, including figures such as Terence Tao and Peter Scholze. The signatories argue that AI systems optimized for mathematical benchmark performance are misaligned with how the mathematical community creates and transmits knowledge, contending that rapid, unreferenced AI-generated proofs erode attribution and auditability. The dispute follows OpenAI&\#x27;s claims that an internal model solved more than 100 open math problems and a contested Navier-Stokes proof, after which OpenAI formed a nine-person Advisory Group on Mathematics and Artificial Intelligence at Princeton&\#x27;s Institute for Advanced Study to referee its AI&\#x27;s math claims.

**「Impact」** The public criticism by a large group of the field&\#x27;s most decorated mathematicians signals that norms around credit and openness for AI-assisted mathematical discovery remain unresolved, which could affect how researchers choose to collaborate with or share results with AI companies.

<details><summary>References</summary>
<ul>
<li><a href="https://startupfortune.com/openai-recruits-nine-mathematicians-to-referee-its-ais-math-claims/">OpenAI Recruits Nine Mathematicians to Referee Its AI&#x27;s Math ...</a></li>
<li><a href="https://aigovernance.com/news/25-fields-medalists-warn-ai-math-benchmarks-erode-attribution-and-auditability">25 Fields Medalists Warn AI Math Benchmarks Erode Attribution ...</a></li>
<li><a href="https://pasqualepillitteri.it/en/news/15971/fields-medalists-alarm-ai-mathematics">25 Fields Medalists Sound the Alarm on AI in Mathematics</a></li>

</ul>
</details>

**Tags**: `#AI`, `#mathematics`, `#OpenAI`, `#research-ethics`, `#academia`

---

<a id="item-tech-news-13"></a>
### [Xbox cuts 268 more jobs, hands next Halo to Activision](https://www.itmedia.co.jp/news/article/2609/23/2000001675/) ⭐️ 7.0/10

Microsoft&\#x27;s Xbox division announced on September 22 that it is cutting 268 jobs across first-party studios including Halo Studios and Xbox Game Studios management and central functions, according to an employee memo from EVP and Chief Content Officer Matt Booty. The cuts are part of a previously announced restructuring of roughly 3,200 roles through fiscal 2027, which began with about 1,600 layoffs in July; Booty said roughly three-quarters of the announced reorganization is now complete. The next Halo game will be developed by a new dedicated team at Activision, separate from Call of Duty development, while Halo Studios shrinks to a small team supporting released titles and the community. The restructuring also consolidates studios: Activision absorbs World&\#x27;s Edge and Rare, Bethesda takes Obsidian under its wing, King integrates Microsoft Casual Games, and Playground Games and Turn 10 merge into one studio focused on Forza and Fable.

rss · ITmedia NEWS · Sep 23, 00:55

**「Background」** This cut is part of a restructuring Xbox announced in July, under which it plans to eliminate roughly 3,200 positions across the division through fiscal year 2027, starting with about 1,600. Asha Sharma, who became CEO in February succeeding Phil Spencer, described the effort at the time as the largest organizational restructuring in Xbox&\#x27;s history, saying the business was &quot;not healthy.&quot; Microsoft acquired Activision Blizzard in 2023, which is why Activision, Bethesda, and King now sit inside the same gaming division being reorganized.

**「Impact」** Ninja Theory faces a proposed closure after two agreed ownership transfers fell through, with Xbox beginning employee consultations while saying it will keep exploring alternatives; talks with Arkane are expected to continue through year-end. Meanwhile, Compulsion Games, Double Fine Productions, and Undead Labs have completed their previously announced spin-outs as independent studios, with Undead Labs&\#x27; State of Decay 3 still slated for day-one Game Pass release under a new publisher.

**Tags**: `#Microsoft`, `#Xbox`, `#layoffs`, `#game industry`, `#restructuring`

---

<a id="item-tech-news-14"></a>
### [Qualcomm Unveils Snapdragon 8 Elite Extreme Gen 6 Platform](https://www.qualcomm.com/smartphones/products/8-series/snapdragon-8-elite-extreme-gen-6-mobile-platform) ⭐️ 7.0/10

Qualcomm has announced the Snapdragon 8 Elite Extreme Gen 6 flagship mobile platform, positioned for on-device agentic AI. Its Oryon CPU is billed as the first 5 GHz smartphone CPU with a 13% performance gain, while the Adreno GPU claims 44% higher performance and 40% better efficiency, and the Hexagon NPU is 35% faster. The platform supports 8K60 and 4K240 video, a claimed world-first triple 64 MP camera configuration, and an X105 5G modem with 14.8 Gbps peak downlink. These are vendor figures; independent testing by Geekerwan on an engineering unit found efficiency gains over the previous generation to be modest, well below what it measured on the retail A20 Pro.

telegram · zaihuapd · Sep 23, 00:52

**「Background」** Qualcomm announced the Snapdragon 8 Elite Extreme Gen 6 alongside a standard Snapdragon 8 Elite Gen 6 at Snapdragon Summit 2026 in Maui, continuing the dual-flagship strategy it introduced with the previous generation. Both chips are Qualcomm&\#x27;s first built on a 2nm process, joining Apple&\#x27;s A20 Pro and MediaTek&\#x27;s latest silicon at that node, and are slated for phones from Vivo, Xiaomi, Oppo, Honor, OnePlus, Redmi, and other Android makers.

**「Impact」** Buyers and reviewers should treat Qualcomm&\#x27;s efficiency claims cautiously: Geekerwan&\#x27;s engineering-unit testing suggests real-world power efficiency improvements are more restrained than the advertised 40% GPU efficiency gain, so retail-device benchmarks will be the deciding evidence.

<details><summary>References</summary>
<ul>
<li><a href="https://9to5google.com/2026/09/22/snapdragon-8-elite-gen-6/">Qualcomm announces the Snapdragon 8 Elite Gen 6 and 8 Elite Extreme Gen 6</a></li>
<li><a href="https://www.cnet.com/tech/computing/qualcomm-snapdragon-8-elite-extreme-gen-6-chips-ai-8k-video-android-phones/">Qualcomm’s New Chips Power AI and 8K Video for Top Android Phones — and They’re Coming Soon - CNET</a></li>
<li><a href="https://www.theverge.com/gadgets/998842/qualcomm-snapdragon-8-elite-extreme-gen-6">Qualcomm’s Snapdragon 8 Elite Gen 6 comes in an Extreme version too | The Verge</a></li>

</ul>
</details>

**Tags**: `#移动芯片`, `#高通骁龙`, `#手机CPU`, `#端侧AI`, `#5G`

---

<a id="item-tech-news-15"></a>
### [llm 0.36 adds GPT-6 models and single-turn plugin support](https://simonwillison.net/2026/Sep/22/llm/) ⭐️ 6.0/10

Simon Willison released llm 0.36, adding support for two new OpenAI models, gpt-6-sol and gpt-6-luna. Model plugins can now declare supports\_conversation = False for models that only accept single-turn prompts; llm raises llm.ConversationNotSupported when such models receive assistant or tool history, and llm chat rejects them before starting a session. The first plugin to use this capability is llm-typesafe. The release also wraps reasoning traces in llm logs Markdown output in &lt;details&gt;&lt;summary&gt; tags and includes bug fixes from five new contributors.

rss · Simon Willison · Sep 22, 18:48

**「Background」** llm is Simon Willison&\#x27;s open-source command-line tool and Python library for interacting with large language models, which supports additional models through a plugin system. Prior to this release, plugins had no standard way to declare that a model only accepts single-turn prompts, so conversation history could be passed to models unable to handle it.

**「Impact」** Plugin authors building on models without conversational context can now declare that limitation explicitly instead of failing unpredictably, and users get a clear error or an upfront rejection in llm chat rather than a broken session.

**Tags**: `#llm-cli`, `#openai-models`, `#plugin-api`, `#release-notes`, `#developer-tools`

---

<a id="item-tech-news-16"></a>
### [HarnessRouter Community Edition: Self-Hosted Unified API for Agent Harnesses](https://github.com/HarnessRouter/harnessrouter) ⭐️ 6.0/10

HarnessRouter Community Edition is a newly published, Apache-2.0-licensed, self-hosted API layer that runs multiple coding-agent harnesses—including Codex, Claude Code, Hermes, PI, and DSH—behind a single OpenAI Responses-compatible interface implementing the project&\#x27;s Unified Harness Protocol \(UHP\). It handles persistent sessions, streaming progress, file and artifact management, cancellation, and structured failures, and deploys with one Docker command requiring about 4 GB of disk and a user-supplied provider API key. Products integrate by calling the instance&\#x27;s /v1/responses endpoint and selecting a harness via metadata.harness\_id, with secrets injectable through environment references that are redacted from logs and traces. The README includes benchmark comparisons across eight harness–model configurations, but these are vendor-produced figures with no independent validation or demonstrated adoption.

rss · はてなブックマーク \(テクノロジー\) · Sep 22, 16:32

**「Background」** Coding agents such as OpenAI&\#x27;s Codex and Anthropic&\#x27;s Claude Code each expose their own CLIs and APIs, so products that want to support multiple agents must integrate and maintain each harness separately. HarnessRouter positions itself as an abstraction layer over these harnesses, implementing what it calls the Unified Harness Protocol with an OpenAI Responses-compatible API, and is offered both as this self-hosted Apache-2.0 Community Edition and as a managed Cloud service.

**「Impact」** Developers building agent-powered products can swap between harnesses like Codex and Claude Code without rewriting integration code, but self-hosters must change the default harnessrouter/harnessrouter Console credentials before exposing the instance, and the container requires root for per-session user management, which is a security consideration for production deployments.

**Tags**: `#ai-agents`, `#open-source`, `#developer-tools`, `#llm-infrastructure`, `#api`

---

<a id="item-tech-news-17"></a>
### [US criticises Australia&\#x27;s algorithm opt-out and duty of care bills as censorship](https://www.bbc.com/news/articles/cqj3dgy8x3vro) ⭐️ 5.0/10

The US government has formally criticised Australia&\#x27;s proposed Digital Duty of Care legislation and a related &\#x27;algorithmic opt-out&\#x27; provision, arguing in a submission that the laws&\#x27; definitions of &\#x27;harm&\#x27; and &\#x27;risks&\#x27; could enable censorship. The US asked Australia to clarify how those terms would be determined so they do not encroach on protected speech. The proposals remain draft legislation, and the criticism reflects a diplomatic position rather than any enacted change.

hackernews · 1659447091 · Sep 23, 02:13 · [Discussion](https://news.ycombinator.com/item?id=49810829)

**「Australia&\#x27;s proposed Digital Duty of Care bill」** Australia&\#x27;s federal government unveiled the Digital Duty of Care legislation on September 8, 2026, proposing that platforms be required to let users opt out of algorithmically recommended social media feeds. The bill also includes provisions obliging platforms to proactively address &\#x27;harmful&\#x27; content, and it is these harm definitions that the Trump administration targeted in a public submission reported on September 22, 2026, asking Australia to clarify how &\#x27;harm&\#x27; and &\#x27;risks&\#x27; would be determined so they do not encroach on protected speech.

**「Community Discussion」** Commenters disputed both the framing and the substance: one argued the article conflates the US response to the opt-out provision with its criticism of a separate Digital Duty of Care requirement that platforms proactively remove harmful content, while an Australian commenter claimed the opt-out label is euphemistic and the bill would let officials designate content as &\#x27;harmful&\#x27; and remove it. Others questioned how &\#x27;algorithm&\#x27; would be legally defined, noting that even chronological feeds are algorithms, and some dismissed the US submission as irrelevant to Australian policymaking.

<details><summary>References</summary>
<ul>
<li><a href="https://www.abc.net.au/news/2026-09-08/labour-s-social-media-algorithm-choice-duty-of-care-bill/107130100">Labor proposes social media algorithm choice under new ...</a></li>
<li><a href="https://ia.acs.org.au/article/2026/-digital-duty-of-care--to-let-aussies-opt-out-of-social-media-al.html">&#x27;Digital duty of care&#x27; to let Aussies opt out of social media ...</a></li>
<li><a href="https://www.abc.net.au/news/2026-09-22/trump-administration-slams-digital-duty-of-care-bill/107182970">Trump administration attacks Australia&#x27;s &#x27;opt-out&#x27; algorithm ...</a></li>

</ul>
</details>

**Tags**: `#tech-regulation`, `#australia`, `#content-moderation`, `#free-speech`, `#platform-policy`

---

<a id="item-tech-news-18"></a>
### [Anthropic publishes usage guide for Opus 5.5 in Claude and Claude Code](https://claude.dev/blog/getting-the-most-out-of-opus-5-5/) ⭐️ 5.0/10

Anthropic published a vendor-authored guide on getting the most out of Opus 5.5 in Claude apps and Claude Code, covering prompting, steering long runs, and verifying results. Key advice includes giving the whole task in one message with an explicit finish line, removing &quot;think step by step&quot; lines since Opus 5.5 always thinks before replying, sending follow-up messages mid-run instead of restarting, and adding CLAUDE.md rules that define when the model should stop and ask versus keep going. The guide also recommends file-based task checklists to survive context summarization, parallel subagents for large audits, and attaching images directly since Opus 5.5 reads charts and screenshots more accurately than Opus 5. Anthropic&\#x27;s claims—such as early testers running multi-hour coding tasks with little oversight and Opus 5.5 at lowest effort catching more bugs than Opus 5 at high effort—come from the vendor and its early testers, not independent measurement.

rss · はてなブックマーク \(テクノロジー\) · Sep 22, 20:45

**「Background」** Opus 5.5 is Anthropic&\#x27;s successor to Opus 5, available in the Claude apps and the Claude Code command-line tool, and Anthropic says its largest gains over prior Opus models are on long, multi-step work such as carrying a change through a large repository until tests pass. Unlike earlier versions, it always thinks before replying and decides how much thinking to do itself, which changes how users should prompt it. This guide is Anthropic&\#x27;s own usage documentation for the model rather than an independent evaluation, so its claims about improved chart reading, code review, and document quality reflect the vendor&\#x27;s testing and early tester reports.

**「Impact」** Claude Code users running long autonomous tasks can reduce interruptions and restarts by adopting the guide&\#x27;s concrete patterns: a CLAUDE.md stop-and-ask rule, a TASKS.md checklist, and mid-run follow-up messages. Users should note the guide&\#x27;s own caveat that fewer stops mean keeping permission prompts on for destructive commands like deleting data or force-pushing.

**Tags**: `#claude`, `#llm-prompting`, `#ai-coding-tools`, `#anthropic`, `#developer-guide`

---

<a id="item-tech-news-19"></a>
### [OpenAI to Allow Earlier Third-Party Safety Evaluations of AI Models](https://www.bloomberg.com/news/articles/2026-09-22/openai-to-let-outside-groups-evaluate-ai-models-at-earlier-phase) ⭐️ 5.0/10

OpenAI plans to let external organizations conduct technical safety evaluations earlier in the AI model training, evaluation, and release process, rather than only shortly before release, according to a Bloomberg report relayed via Telegram. The company is reportedly in talks with evaluators including METR and Redwood Research, and may allow outside evaluators to work on-site with access to sensitive material. OpenAI says it requires evaluators to demonstrate independence, scientific rigor, and clear accountability. The plan was to be announced in a blog post on Tuesday; the report is a plan announcement, not a shipped program, and specific evaluation scope and timelines remain unconfirmed.

telegram · zaihuapd · Sep 22, 17:39

**「Background」** Third-party safety evaluations of frontier AI models have typically occurred only shortly before public release, limiting what external auditors can observe about a model&\#x27;s development. OpenAI&\#x27;s stated rationale for moving evaluations earlier is that models are becoming better at recognizing when they are being evaluated, which can distort pre-release test results. METR and Redwood Research are independent organizations that specialize in evaluating AI systems for dangerous capabilities, and OpenAI has said such reviews should meet standards of independence, scientific rigor, security practices, and clear responsibilities.

**「Impact」** If implemented, earlier third-party access would give independent evaluators visibility into model behavior during training rather than only on near-final checkpoints, potentially catching dangerous capabilities before release decisions are locked in. However, since the arrangement is still under negotiation, organizations relying on external audits for compliance or risk assessment should treat this as a pending commitment rather than an available mechanism.

<details><summary>References</summary>
<ul>
<li><a href="https://aiweekly.co/alerts/openai-opens-model-training-to-outside-safety-evaluators">OpenAI Opens Model Training to Outside Safety Evaluators</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#OpenAI`, `#model evaluation`, `#AI governance`, `#third-party auditing`

---

<a id="item-tech-news-20"></a>
### [Apple Reportedly Prototyping Screenless Whoop-Style Fitness Band](https://www.bloomberg.com/news/articles/2026-09-22/apple-is-developing-new-fitness-tracker-aimed-at-rivaling-whoop) ⭐️ 5.0/10

Apple is developing a screenless health and fitness tracker resembling Whoop&\#x27;s wristband, according to a Bloomberg report citing people familiar with the matter. The device takes the form of a thin fabric band with embedded sensors, and the company has reportedly explored the concept for several months and begun building prototypes. The project remains in early technical research with no decision made on whether to release it; if it proceeds, the earliest possible launch would be 2028, and the effort has backing from executives including Tim Cook.

telegram · zaihuapd · Sep 23, 00:01

**「Background」** Whoop is a subscription-based fitness wearable known for its screenless fabric band that continuously tracks metrics like recovery, strain, and sleep, syncing data to a companion app rather than displaying it on-device. Apple already sells the Apple Watch, a screen-based smartwatch with health sensors, so a screenless band would represent a different form factor targeting continuous, low-distraction health monitoring.

**「Impact」** Because this is an unconfirmed early-stage research project with no committed release, there is nothing for users or developers to act on now; its main significance is that Apple is exploring a subscription-style, screen-free wearable category currently dominated by Whoop, which would compete with rather than replace the Apple Watch.

**Tags**: `#apple`, `#wearables`, `#fitness-tracker`, `#industry-news`, `#rumor`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China Reportedly Tells Banks Not to Classify Vanke&\#x27;s Overdue Loans as Bad Debt](https://www.reuters.com/world/asia-pacific/china-asks-banks-keep-vanke-loans-off-bad-debt-books-sources-say-2026-09-22/) ⭐️ 7.0/10

Chinese financial regulators have told some major banks not to classify China Vanke&\#x27;s overdue loans as non-performing, to extend repayment terms, and to defer interest collection, according to people familiar with the matter cited by Reuters. The reported directive — one of Beijing&\#x27;s strongest interventions to prevent the developer&\#x27;s default — follows Vanke&\#x27;s record 88.6 billion yuan loss in 2025 and a widened net loss of 14.95 billion yuan in the first half of 2026.

telegram · zaihuapd · Sep 23, 03:12

**「Background」** Vanke is one of China&\#x27;s largest state-backed property developers and has been under severe financial strain during the country&\#x27;s prolonged property downturn, posting a record 88.6 billion yuan loss in 2025 and a widened 14.95 billion yuan net loss in the first half of 2026. Classifying a loan as non-performing forces banks to set aside reserves against it, so keeping Vanke&\#x27;s overdue loans off bad-debt books would shield both the developer and lenders&\#x27; reported asset quality.

**「Impact」** If confirmed, the move would ease immediate default pressure on Vanke but keep troubled property loans on banks&\#x27; books as performing assets, masking the true level of bad debt in China&\#x27;s banking system.

<details><summary>References</summary>
<ul>
<li><a href="https://www.reuters.com/world/asia-pacific/china-asks-banks-keep-vanke-loans-off-bad-debt-books-sources-say-2026-09-22/">EXCLUSIVE: China asks banks to keep Vanke loans off bad-debt books ...</a></li>
<li><a href="https://www.iux24.com/zh-CN/news/china-asks-banks-to-keep-vanke-loans-off-bad-debt-books-to-prevent-default-20260922">中国要求银行保护万科贷款 | IUX24</a></li>

</ul>
</details>

**Tags**: `#中国房地产市场`, `#万科`, `#银行监管`, `#不良贷款`, `#债务风险`

---

<a id="item-finance-news-2"></a>
### [CFTC Warns Prediction-Market &\#x27;Mentions&\#x27; Contracts Carry Higher Manipulation Risk](https://www.cnbc.com/2026/09/22/cftc-prediction-markets-mentions-contracts-have-manipulation-risk.html) ⭐️ 6.0/10

The CFTC told regulated exchanges on Tuesday that prediction-market &\#x27;mentions&\#x27; contracts — bets on specific words used in a speech, earnings call, or broadcast — face heightened manipulation risk because settlement depends on one person&\#x27;s conduct that may not be independently verifiable. The guidance is advisory rather than a new binding rule, and it lists four factors exchanges should weigh before listing such contracts.

rss · CNBC Finance · Sep 23, 00:58

**「Background」** The warning follows an internal CFTC review that prompted Kalshi, one of the few U.S.-regulated platforms offering these markets, to pull its sports-related mention contracts, and an August settlement in which a teleprompter operator for President Trump paid a $172,539 fine for insider trading on Kalshi mention markets.

**「Impact」** The guidance directly affects regulated platforms like Kalshi, which must now show their mention contracts meet the agency&\#x27;s listing criteria, while rival Polymarket&\#x27;s mention markets sit on its international exchange outside CFTC oversight.

**Tags**: `#CFTC`, `#prediction markets`, `#market regulation`, `#manipulation risk`, `#Kalshi`

---