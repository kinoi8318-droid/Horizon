---
layout: default
title: "Horizon Summary: 2026-09-24 (EN)"
date: 2026-09-24
lang: en
---

> From 16 items, 11 important content pieces were selected

---

**Technology News**
1. [Qualcomm Announces Upstream Linux Support for Snapdragon X2 Series](#item-tech-news-1) ⭐️ 7.0/10
2. [Cloudflare adds Vary header support to its cache](#item-tech-news-2) ⭐️ 7.0/10
3. [Google launches Gemini 3.8 Flash and Flash-Lite TTS models](#item-tech-news-3) ⭐️ 7.0/10
4. [Meta&\#x27;s Muse AI agent triggers selloff in travel and finance stocks](#item-tech-news-4) ⭐️ 7.0/10
5. [Fly.io Examines VSCode Remote-SSH Agent&\#x27;s Security Implications](#item-tech-news-5) ⭐️ 6.0/10
6. [YouTube Unveils Gemini Editing, Video A/B Testing, and Live Tools](#item-tech-news-6) ⭐️ 6.0/10
7. [Meta Announces New VR Glasses at $1,300](#item-tech-news-7) ⭐️ 5.0/10
8. [YouTube Announces Custom Feeds, Ask Music, and AI Shopping Features](#item-tech-news-8) ⭐️ 5.0/10

**Technology Blog**
1. [Deleting AI Chat History Doesn&\#x27;t Delete the Logs: A 37-Tool Survey](#item-tech-blog-1) ⭐️ 7.0/10

**Financial News**
1. [U.S.-China trade truce extended to January 10, Bessent says](#item-finance-news-1) ⭐️ 8.0/10
2. [China&\#x27;s Self-Sufficiency Shifts Stakes Ahead of Trump-Xi Summit](#item-finance-news-2) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Qualcomm Announces Upstream Linux Support for Snapdragon X2 Series](https://www.qualcomm.com/news/onq/2026/09/snapdragon-summit-agentic-ai-pcs-linux) ⭐️ 7.0/10

Qualcomm announced it is upstreaming core Linux drivers for its Snapdragon X2 Series laptop chips, explicitly including the Hexagon NPU and Adreno GPU, to enable developers and partners to build on the platform. This is an announced commitment rather than a completed capability, and community evidence suggests early progress: an OpenBSD developer has already committed initial arm64 support for X2 Elite laptops, and ARM EL2 has been confirmed working, which would enable KVM virtualization unlike previous Snapdragon laptop generations.

hackernews · aaronday · Sep 23, 22:38 · [Discussion](https://news.ycombinator.com/item?id=49823582)

**「Background」** The Snapdragon X2 Series is Qualcomm&\#x27;s second generation of ARM-based laptop chips, following the original Snapdragon X Elite, which was also promised good Linux support that commenters note never fully materialized. Upstreaming drivers means submitting them to the mainline Linux kernel rather than shipping semi-proprietary vendor trees, which determines whether distributions can support the hardware out of the box. Qualcomm&\#x27;s announcement specifically covers core drivers including the Hexagon NPU and Adreno GPU.

**「Impact」** If the upstreaming effort is completed, developers could run mainline Linux with NPU and GPU acceleration on Snapdragon X2 laptops rather than relying on vendor-specific or semi-proprietary stacks. However, commenters note that the original Snapdragon X Elite was also promised good Linux support that never fully materialized, so the practical value depends on Qualcomm&\#x27;s follow-through.

**「Community Discussion」** Commenter brynet reported that OpenBSD developer Tobias Heider has committed initial OpenBSD/arm64 support getting USB, keyboard, and touchpad working in ACPI mode on the HP Elitebook X G2q, and confirmed ARM EL2 works, implying KVM support absent in prior generations. Other commenters expressed enthusiasm about performance rivaling Apple&\#x27;s M series, but sharktheone cautioned that the original X Elite&\#x27;s promised Linux support never arrived, tempering expectations for the X2.

**Tags**: `#linux`, `#qualcomm-snapdragon`, `#arm64`, `#open-source-drivers`, `#hardware`

---

<a id="item-tech-news-2"></a>
### [Cloudflare adds Vary header support to its cache](https://blog.cloudflare.com/vary-support/) ⭐️ 7.0/10

Cloudflare announced that its cache now supports the HTTP Vary header, allowing content-negotiated responses to be cached as separate variants instead of one response being served to all clients. Previously, Cloudflare ignored Vary on anything other than images, which made patterns like serving HTML to browsers and JSON to API clients based on the Accept header unsafe to deploy behind its cache. The company notes that if an origin response omits a Vary header, the response is cached normally, which can leave it unisolated from Vary-segmented variants.

hackernews · thisisfatih · Sep 23, 22:03 · [Discussion](https://news.ycombinator.com/item?id=49823195)

**「Background」** The HTTP Vary header tells caches which request headers \(such as Accept or Accept-Encoding\) determine which version of a response should be stored and served, enabling content negotiation. Historically, Cloudflare&\#x27;s cache ignored Vary except for images, so sites serving different formats from the same URL risked having one variant cached and incorrectly served to all clients.

**「Impact」** Developers running content negotiation behind Cloudflare can now rely on correct variant caching, but they should ensure every response carries a Vary header, since a non-Vary response may be cached without the variance needed to keep it isolated from segmented variants.

**「Community Discussion」** Commenters including simonw and bhouston said they had wanted this for years and reported real production bugs from assuming Cloudflare already honored Vary, with one noting CloudFront supported it long ago. Others pointed out mitigating context: Cloudflare does not cache HTML by default, and rob-olmos raised the open question of whether a non-Vary cached object could front-run Vary-segmented ones.

**Tags**: `#http`, `#caching`, `#cloudflare`, `#cdn`, `#web-infrastructure`

---

<a id="item-tech-news-3"></a>
### [Google launches Gemini 3.8 Flash and Flash-Lite TTS models](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-8-text-to-speech/) ⭐️ 7.0/10

Google announced two new text-to-speech models, Gemini 3.8 Flash TTS and Gemini 3.8 Flash-Lite TTS, available starting today in the Gemini API and Google AI Studio, with Gemini Enterprise API access coming soon. Flash TTS targets creative work, offering generative voice design from natural-language prompts across 100+ languages, a library of 2,000+ preset voices, and voice replication from a 30-second sample gated by verbal consent verification, SynthID watermarking, and C2PA credentials. Flash-Lite TTS is optimized for high-volume, cost-efficient uses such as dubbing and voice agents, and both models support line-by-line delivery direction, long-form generation, two-speaker scenes, and scripted non-verbal cues. Google claims the models took the top spots on Hume AI&\#x27;s Voice Design Benchmark and Overall Quality Index and led blind human preference tests on Voice Arena in several languages, though these are vendor-reported results without independent verification.

rss · はてなブックマーク \(テクノロジー\) · Sep 23, 19:27

**「Background」** These models extend Google&\#x27;s Gemini Audio family, which the company says already includes 3.5 Live Translate, 3.5 Transcribe, 3.8 Live, and 3.8 Live Extended Thinking. They succeed Gemini 3.1 Flash TTS, against which Google claims improvements in long-form content and dual-speaker screenplay control, and they continue Google&\#x27;s practice of embedding SynthID watermarks in AI-generated audio.

**「Impact」** Developers can try both models now through Google AI Studio&\#x27;s new audio playground and the Gemini API, and platforms including Agora, LiveKit, Pipecat, and Vercel already support deployment, while consumer access arrives via Gemini Notebook and Google Vids. Teams considering voice replication should note the consent-recording requirement and that voice remixing of library voices is listed as coming soon rather than available at launch.

**Tags**: `#text-to-speech`, `#gemini`, `#google-ai`, `#voice-generation`, `#generative-ai`

---

<a id="item-tech-news-4"></a>
### [Meta&\#x27;s Muse AI agent triggers selloff in travel and finance stocks](https://www.nikkei.com/article/DGXZQOFD2339C0T20C26A9000000/) ⭐️ 7.0/10

Meta has unveiled Muse, an AI agent that handles shopping and travel bookings on users&\#x27; behalf, prompting a selloff in online travel and financial services stocks over fears the agent could displace those services and drive away their customers. TripAdvisor shares closed on the 23rd down about 14% from their close on the 4th, before Muse was announced, while retail brokerage Charles Schwab fell 9%. The Nikkei report is paywalled and truncated, so details on Muse&\#x27;s capabilities, availability, and technical underpinnings are not confirmed beyond the announcement itself.

rss · はてなブックマーク \(テクノロジー\) · Sep 23, 22:02

**「What Muse is and when it launched」** Meta launched its personal AI agent Muse in the US earlier this month, on September 8, with capabilities including flight booking across more than 500 airlines via Duffel, browser-based hotel shopping, and checkout through Meta&\#x27;s Link payment system. The launch drew attention because Meta had widely been viewed as lagging rivals in AI, and the agent&\#x27;s ability to complete transactions on users&\#x27; behalf has already provoked pushback from companies such as Amazon, which argued the bot crossed a line.

**「Impact」** The double-digit single-session declines in TripAdvisor and Charles Schwab show investors are already pricing agentic AI as a direct threat to intermediary consumer services, meaning companies whose business depends on customer-facing booking or brokerage flows face immediate pressure to articulate how they will integrate with or compete against agents like Muse.

<details><summary>References</summary>
<ul>
<li><a href="https://www.latimes.com/business/story/2026-09-23/meta-muse-can-now-book-travel-shop-for-you-amazon-says-it-crossed-line">Meta’s viral AI agent can now book travel and shop for you. Amazon says it crossed a line</a></li>
<li><a href="https://deeparrival.com/news/meta-muse-agent-books-travel-september-2026/">Meta Muse Opens US Travel Booking on 500 Duffel Airlines</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#Meta`, `#agentic AI`, `#market impact`, `#travel tech`

---

<a id="item-tech-news-5"></a>
### [Fly.io Examines VSCode Remote-SSH Agent&\#x27;s Security Implications](https://fly.io/blog/vscode-ssh-wtf/) ⭐️ 6.0/10

A Fly.io blog post analyzes the behavior of VSCode&\#x27;s Remote-SSH agent, which ships a server binary to the remote host over SSH/SFTP, installs and runs extensions there, and sets up port tunneling between the local and remote machines. The post frames these capabilities as surprising and potentially risky, particularly the reverse direction in which a compromised remote machine could act against the developer&\#x27;s local machine. The analysis is a vendor blog&\#x27;s examination rather than a report of a newly discovered vulnerability, and much of the described behavior is the documented design of the Remote-SSH extension.

hackernews · Rapzid · Sep 23, 21:01 · [Discussion](https://news.ycombinator.com/item?id=49822555)

**「How VSCode Remote-SSH works」** VSCode&\#x27;s Remote-SSH extension connects to a remote host over SSH and installs a server-side agent \(VS Code Server\) there, which then communicates back with the local editor over the SSH connection, including via WebSockets, so extensions and terminals run on the remote machine. Per Microsoft&\#x27;s documentation, the extension by default tries to download the server on the remote host and falls back to downloading it locally and transferring it over the connection, a behavior configurable via the remote.SSH.localServerDownload setting. This architecture means the agent can spawn shell processes and persist itself on the remote host, which is the behavior the Fly.io post scrutinizes from a security perspective.

**「Impact」** For developers using Remote-SSH, the concrete takeaway is that connecting to a remote host grants that host substantial trust: a malicious or compromised remote could potentially affect the local machine through the reverse direction of the connection. Teams should treat Remote-SSH targets as trusted environments and avoid pointing the extension at production servers or untrusted hosts, applying SSH-level access restrictions where guardrails are needed.

**「Community Discussion」** Commenters largely pushed back on the alarm, arguing that editing files, running commands, and tunneling on a remote machine is exactly what Remote-SSH is designed to do, and that shipping the agent binary over SSH is the natural bootstrap method when remotes lack internet access. However, some agreed with the post&\#x27;s strongest point: MajesticHobo2 called the reverse direction, where a compromised remote can affect the local machine, unacceptable, and kayson questioned whether the same risk applies to VSCodium&\#x27;s extensions.

<details><summary>References</summary>
<ul>
<li><a href="https://fly.io/blog/vscode-ssh-wtf/">VSCode ’s SSH Agent Is Bananas · The Fly Blog</a></li>
<li><a href="https://code.visualstudio.com/docs/remote/ssh">Remote Development using SSH</a></li>

</ul>
</details>

**Tags**: `#vscode`, `#ssh`, `#security`, `#remote-development`, `#developer-tools`

---

<a id="item-tech-news-6"></a>
### [YouTube Unveils Gemini Editing, Video A/B Testing, and Live Tools](https://www.itmedia.co.jp/news/article/2609/24/2000001682/) ⭐️ 6.0/10

At its Made on YouTube 2026 event on September 23, YouTube announced a broad set of creator tools, including a Gemini-powered conversational editing assistant for Shorts and the YouTube Create app, new Insights and Research analytics pages in YouTube Studio, and A/B testing of up to three video edits to compare intros. It also previewed opt-in AI comment moderation, voice detection added to its likeness detection deepfake tool, livestreamer matching for Go Live Together, real-time live auto dubbing, and an expansion of the Shopping affiliate program beyond the US by year-end. Most features have no announced release date or region: Shorts series organization began rolling out the same day, Watch With expansion starts this year, while Go Live Together matching, Live showdown, and auto dubbing are slated for 2027.

rss · ITmedia NEWS · Sep 23, 22:14

**「Background」** Made on YouTube is the platform&\#x27;s annual event where it unveils creator-facing features, and the 2026 edition was held on September 23. Several of the announced tools build on existing capabilities: title and thumbnail A/B testing officially launched in 2024, and the Gemini Omni assistant was added to Shorts and the YouTube Create app earlier this year. YouTube has also been expanding AI features under its Gemini integration and its likeness detection tool, which was originally designed to flag deepfakes using facial matching.

**「Impact」** Creators gain AI-assisted editing and analytics without leaving YouTube&\#x27;s own apps, but because availability dates and regions are unspecified for most features—and Japanese feature names are not yet decided—creators outside the US cannot yet plan around them; the affiliate tagging expansion explicitly leaves Japan&\#x27;s inclusion unconfirmed.

**Tags**: `#YouTube`, `#Gemini`, `#AI video editing`, `#creator tools`, `#Google`

---

<a id="item-tech-news-7"></a>
### [Meta Announces New VR Glasses at $1,300](https://www.meta.com/vr-glasses/) ⭐️ 5.0/10

Meta has announced a new pair of VR glasses, with community reports putting the price at $1,300 and a field of view of 70 x 66 degrees, notably narrower than the Quest 3&\#x27;s 103 x 96. Despite the &quot;VR&quot; branding, most of the promotional imagery depicts augmented-reality use cases, suggesting the device sits closer to Meta&\#x27;s transparent-display AR line \(Ray-Ban Display, Orion\) than to its Quest headsets. The announcement page offers limited technical detail, so specifications beyond those cited by early viewers remain unconfirmed.

hackernews · polymorph1sm · Sep 23, 23:47 · [Discussion](https://news.ycombinator.com/item?id=49824268)

**「Background」** Meta has sold VR headsets since the Oculus Quest line, which it later rebranded under its own name, and has more recently pushed toward lightweight AR-style eyewear such as the Ray-Ban Display glasses and its Orion prototype. The VR Glasses were unveiled at Meta&\#x27;s Connect event in Menlo Park, priced at $1,300, with a roughly 70-degree horizontal field of view—narrower than the Quest 3&\#x27;s 103 x 96 degrees but wider than most display glasses, a trade-off Meta says yields a higher pixel density of 37 PPD.

**「Impact」** For existing Quest 3 owners, the reduced 70 x 66 field of view is the main compatibility-and-experience concern raised, and it is unclear whether announced titles such as a new Beat Saber game and an Ace Attorney VR project will also ship on Quest 3 or PCVR.

**「Community Discussion」** Commenters split between hardware skepticism and distrust of Meta itself: one former Oculus Quest owner said they abandoned the platform after Meta began requiring a government ID upload, calling the practice user-hostile. Others questioned the product&\#x27;s purpose, comparing it to a reinvented HoloLens with no clear problem to solve, while some noted Meta&\#x27;s apparent strategic shift away from passthrough-headset AR toward transparent glasses.

<details><summary>References</summary>
<ul>
<li><a href="https://roadtovr.com/meta-vr-glasses-unveiled-price-release-date/">Meta Announces &#x27;VR Glasses&#x27; Next-Gen XR Headset, Priced at $1,300 | Road to VR</a></li>
<li><a href="https://www.wired.com/story/metas-answer-to-the-meta-creep-camera-free-smart-glasses/">Meta VR Glasses, Ray-Ban Meta Audio, Ray-Ban Meta Gen 3: Specs, Features, Prices | WIRED</a></li>
<li><a href="https://www.engadget.com/2267218/meta-vr-glasses-price-specs-apple-vision-pro-comparison/">Meta&#x27;s $1,300 VR Glasses look like the Vision Pro sequel Apple should be making - Engadget</a></li>

</ul>
</details>

**Tags**: `#virtual-reality`, `#meta`, `#hardware`, `#privacy`, `#ar-vr`

---

<a id="item-tech-news-8"></a>
### [YouTube Announces Custom Feeds, Ask Music, and AI Shopping Features](https://www.itmedia.co.jp/news/article/2609/24/2000001684/) ⭐️ 5.0/10

At its Made on YouTube 2026 event on September 23, YouTube announced a set of viewer-facing features, most of which are announced plans rather than shipped capabilities. Custom Feeds lets users create prompt-defined home-screen tabs \(for example, podcasts for a 30-minute commute\) that auto-update with new recommendations, rolling out soon in the US on web, mobile, and TV. The Ask YouTube AI assistant gains conversational shopping support with comparison tables and voice control on TV, while YouTube Music gets Ask Music, a conversational tool for building play queues across a catalog of over 300 million tracks, and Your Podcast Lineup, a weekly voice-narrated recommendation guide—both coming soon worldwide for YouTube Music and Premium subscribers. Other announcements include localized product links on foreign creators&\#x27; videos, Shorts series with seasons and episodes \(available from the announcement date\), voice comments on TV, Watch With expansion to long-form videos later this year, Live Showdown creator competitions in 2027, and real-time auto-dubbing for livestreams starting trials in early 2027.

rss · ITmedia NEWS · Sep 23, 23:10

**「Background」** Made on YouTube is the platform&\#x27;s annual event where it unveils product updates, with creator-focused features covered separately from these viewer-facing ones. Ask YouTube is YouTube&\#x27;s existing conversational AI feature, which this update extends into shopping assistance. Japanese names for the new features have not yet been announced, and availability timing or regions are unspecified for some items.

**「Impact」** Viewers outside the US should note that Custom Feeds is US-only at launch, while Ask Music and Your Podcast Lineup require a paid YouTube Music or Premium subscription; several features, including Live Showdown and livestream auto-dubbing, will not arrive until 2027.

**Tags**: `#YouTube`, `#AI features`, `#recommendation systems`, `#conversational AI`, `#product announcement`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Deleting AI Chat History Doesn&\#x27;t Delete the Logs: A 37-Tool Survey](https://qiita.com/songchong/items/5aa4bc07279ea271909a?utm_campaign=popular_items&amp;utm_medium=feed&amp;utm_source=popular_items) ⭐️ 7.0/10

rss · Qiita \(人気記事\) · Sep 23, 19:18

**「Background」** When companies write internal rules for generative AI use, one question always comes up: can managers or the AI provider read what employees type, and does deleting chat history actually erase the record? The author argues that answering &quot;just delete the history&quot; is only half right, because on-screen history and provider-side logs are separate things.

**「Solution」** The author reviewed the terms of service, privacy notices, and admin documentation for 37 AI tools, counting only the 22 products where the provider&\#x27;s own wording on record retention could be verified against original documents \(the other 15 are &quot;not found,&quot; not &quot;no retention&quot;\). The findings sort into five retention patterns: logs kept locally on the user&\#x27;s machine \(Ollama, OpenClaw\); provider-held audit logs readable by corporate admins under enterprise contracts \(ChatGPT via its Compliance API, Claude and GitHub Copilot with 180-day logs, Microsoft 365 Copilot\); auto-expiring logs \(Grok, Codex, Dify at 30 days; SmartRead at one year\); explicit no-retention claims \(Perplexity, Felo\); and—the most overlooked—records that survive user deletion, such as Gemini&\#x27;s human-reviewed conversations kept up to three years even after the user deletes them. The author also notes that providers retain content for two reasons, model training and abuse investigation, and that personal and enterprise tiers of the same product can have opposite policies. Practical guidance: classify each tool by type, verify admin audit access and retention windows, and ask vendors directly what persists after deletion.

**「Takeaway」** The author&\#x27;s core point is that &quot;deletable history&quot; and &quot;deleted records&quot; are different claims, and internal AI policies must specify which product and which log they govern. Because every claim rests on vendor documentation rather than independent verification, the survey is a map of what providers promise—not proof of what they do.

**Tags**: `#AI tools`, `#data retention`, `#audit logs`, `#enterprise security`, `#privacy policy`

---

## Financial News

<a id="item-finance-news-1"></a>
### [U.S.-China trade truce extended to January 10, Bessent says](https://www.cnbc.com/2026/09/24/us-china-trade-truce-bessent-trump-xi.html) ⭐️ 8.0/10

U.S. Treasury Secretary Scott Bessent said the U.S.-China trade truce, which keeps tariffs lower and rare earth exports flowing, will be extended from its November expiry to January 10—a shorter extension than the six months or more many had expected—announced as Xi Jinping began a state visit to Washington.

rss · CNBC Finance · Sep 23, 23:59

**「Background」** Trump and Xi agreed to the original one-year truce at an October meeting in South Korea, and Bessent said Beijing still needs to fulfill more deliverables, while Chinese state media did not immediately confirm the extension.

**Tags**: `#US-China trade`, `#tariffs`, `#trade policy`, `#rare earths`, `#diplomacy`

---

<a id="item-finance-news-2"></a>
### [China&\#x27;s Self-Sufficiency Shifts Stakes Ahead of Trump-Xi Summit](https://www.cnbc.com/2026/09/23/trump-xi-meeting-why-chinas-self-sufficiency-changes-the-calculus.html) ⭐️ 6.0/10

Ahead of an expected Trump-Xi summit this week, CNBC reports that China&\#x27;s push for self-sufficiency and the world&\#x27;s continued reliance on Chinese goods have shifted the trade calculus, with businesses hoping at best for an extension of last fall&\#x27;s trade truce. Despite tariffs, the U.S. trade deficit with China has risen again this year on surging demand for AI-related parts, and China reached 40% of global container exports this summer — a milestone the European Chamber of Commerce in China had not expected until 2030.

rss · CNBC Finance · Sep 23, 21:26

**「Background」** China&\#x27;s property downturn, which began in 2022 with house prices down about 30% over six years, pushed its companies to expand exports aggressively, while U.S. tech firms&\#x27; AI data-center buildout has supported demand for Chinese goods even as AI-related exports fell significantly in August, according to think tank CF40.

**「Impact」** Foreign competitors face intensifying pressure: three-quarters of American Chamber of Commerce members in Shanghai now see Chinese rivals as more advanced, and the EU — which has the largest trade deficit with China — is stepping up scrutiny of China-origin exports, with its trade commissioner expected in Beijing next month.

**Tags**: `#US-China trade`, `#Trump-Xi summit`, `#China economy`, `#tariffs`, `#AI exports`

---