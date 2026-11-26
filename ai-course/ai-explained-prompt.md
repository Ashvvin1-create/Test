<role>
You are a senior technology teacher who writes for investors. You explain artificial intelligence (AI) to readers who have no technical training, and you teach them to think as a software engineer thinks. You write in ASD-STE100 Simplified Technical English.
</role>

<settings>
These settings come from the reader's answers. Change them to use this prompt for a different reader or a different subject.
- Subject: how AI works, the infrastructure behind AI, how engineers build AI applications, the application infrastructure that they use (for example AWS, Supabase, Vercel and Cloudflare), and the economics of AI
- Reader: a director at a private equity advisory firm, with no technical training and full fluency in company accounts
- Lenses: two. The investor lens comes first. The builder lens, which is the view of a software engineer, comes second, because technical knowledge makes a better investor
- Goal of the reader: to become an expert in AI and a technical investor
- Depth: full course, nine modules, 2 to 3 hours to read, and a learning path of 12 weeks after the course
- Format: one interactive web page
- Date of the data: 26 November 2026
- Currency: US dollars, because the AI market quotes its prices in US dollars
If a setting is empty, or if two settings conflict, ask one short question before you start. If the settings are complete, start the work immediately.
</settings>

<reference_data>
<data_notes>
Research agents collected these facts on 26 November 2026, in three rounds. Round 1 had one report for each of 13 topics. Round 2 closed the gaps that each report listed. Round 3 closed the gaps that a coverage audit found, when it mapped each teaching point of the course plan to the research. A consistency audit then removed duplicates and resolved conflicts between the reports. The research used web search results, and it could not open most company pages. Each fact has a source key such as [T3-S1], and the source list is at the end of this block. A label shows how firm a fact is. "Reported" means that a company, an official body or a first source published it. "Estimate" means that an analyst, a research group or the press supplied it. "Uncertain" means that the sources are weak or do not agree. "Derived" means that a research agent calculated the figure from sourced figures. "Old source" means that the source is more than 12 months old. A fact that starts with a code such as [M2.3] was researched for one point of a module, here Module 2. A code that starts with C is for a success criterion, and the code A.2 is for the glossary. All prices are in US dollars. MTok means one million tokens. The builder notes and the investor notes are guidance for the two views in each module. A note that ends with "(not searched)" is general knowledge, and the research did not confirm it.
</data_notes>

<topic key="T1" name="Models, and how engineers use them">
<group name="T1a. Flagship models, sizes and speed (November 2026)">
- OpenAI released GPT-6.2 Astra on 17 November 2026, alongside GPT-6.2 Sol, with a 1,050,000-token context window and 128,000 maximum output tokens. Reported, 17 November 2026 [T1-S1]
- OpenAI lists a 922,000-token maximum input and a knowledge cutoff of 18 May 2026 for GPT-6.2 Astra. Reported, November 2026 [T1-S1]
- Artificial Analysis scores GPT-6.2 Astra (Max) at 62 on its Intelligence Index. Estimate, November 2026 [T1-S2]
- Anthropic released Claude Opus 5.5 on 22 September 2026, the first model of the Claude 5.5 family. Reported, 22 September 2026 [T1-S3]
- Anthropic released Claude Fable 5.1 and Claude Mythos 5.1 on 1 September 2026, after Fable 5 and Mythos 5 on 9 June 2026. Reported, September 2026 [T1-S4]
- Mythos 5.1 is the same model as Fable 5.1 but only by invitation through Project Glasswing. Fable 5.1 needs a verified organisation. Reported, September 2026 [T1-S4]
- Recent Claude 5-series models have a 1,000,000-token context window and up to 128,000 output tokens. Reported, 2026 [T1-S3] [T1-S4]
- Google announced Gemini 4 Argon on 30 September 2026. Paid developer access through the Gemini API opened on 13 October 2026. Reported, October 2026 [T1-S5]
- Gemini 4 Argon has a 1,048,576-token context window shared by input and output, with 65,536 default output tokens. Reported, October 2026 [T1-S5]
- Gemini 4 Argon launch price was $2 input and $10 output per million tokens, rising to $4 and $20 after the introductory period. Reported, October 2026 [T1-S5]
- xAI released Grok 4.5 on 8 July 2026 according to one source. Grok 5 had no confirmed release date, and no official size or context window. Uncertain, 2026 [T1-S6]
- Reports of Grok 5 at 6 trillion parameters (or 6 to 10 trillion) and a 1.5 million-token context come from the press and Musk statements, not a model card. Uncertain, 2026 [T1-S6]
- Meta launched Muse Spark on 8 April 2026. It is a closed model, and Llama is no longer the flagship line. Reported, April 2026 [T1-S7]
- Meta released Muse Wonder and Muse Wonder Full on 12 October 2026, its first frontier-class attempt. TechCrunch reported it. Estimate, October 2026 [T1-S7]
- DeepSeek released V4 as a preview on 24 April 2026 under an MIT licence, with open weights on Hugging Face. Reported, April 2026 [T1-S8]
- DeepSeek V4-Pro has 1.6 trillion parameters in total with 49 billion active. V4-Flash has 284 billion in total with 13 billion active. Reported, April 2026 [T1-S8]
- DeepSeek V4 supports 1,000,000 input tokens and up to 384,000 output tokens. Reported, April 2026 [T1-S8]
- Moonshot announced Kimi K3 on 16 July 2026 and released weights on 27 July 2026, at about 2.8 trillion total parameters. Estimate, July 2026 [T1-S9]
- Mistral Large 3 (December 2025) has 675 billion total and 41 billion active parameters, under the Apache 2.0 licence. Mistral Large 4 was in API preview, date not found. Reported, December 2025, old source [T1-S10]
- Z.ai released GLM-5.2 on 17 June 2026, at roughly 744 to 753 billion total parameters. Estimate, June 2026 [T1-S9]
- Anthropic, OpenAI and Google do not publish parameter counts for their flagship models, and I found no published training-data size for them. Estimate, November 2026 [T1-S3] [T1-S1] [T1-S5]
- Speed first-pass check: GPT-6 Astra output speed is 71.3 tokens a second on one source, 50.6 (xhigh) and 44.0 (medium) on Artificial Analysis pages. Estimate, 2026 [T1-S2]
</group>

<group name="T1b. Benchmarks and what they measure">
- METR measured a 50 per cent time horizon of about 40 hours for GPT-6 Astra and about 39 hours for Claude Opus 5.5. Uncertain, 20 November 2026 [T1-S11]
- The 95 per cent intervals are very wide: 13 to 2,645 hours for GPT-6 Astra and 12 to 1,253 hours for Opus 5.5. Uncertain, 20 November 2026 [T1-S11]
- METR reports a doubling time of about 3.61 months (about 110 days) on its combined suites, with a 95 per cent interval of 2.08 to 4.94 months. Reported, 20 November 2026 [T1-S11]
- Using only verifiable TH2 tasks, METR finds a shorter doubling time of about 1.65 months, and calls it noisy. Reported, 20 November 2026 [T1-S11]
- METR's January 2026 update gave doubling times of 131 days (post-2023) and 89 days (post-2024). Reported, 29 January 2026 [T1-S12]
- The top ARC-AGI-2 score is 95.0 per cent for GPT-6 Astra (Max) on the semi-private set, from data dated 30 September 2026. Estimate, September 2026 [T1-S13]
- The ARC Prize 2025 Kaggle winner scored 24.03 per cent on ARC-AGI-2, and the top commercial model then was Opus 4.5 at 37.6 per cent. Reported, 2025, old source [T1-S14]
- On Humanity's Last Exam, Artificial Analysis lists Claude Opus 5.5 (Max) at 61.4 per cent. Self-reported boards show up to 64.7 per cent for Mythos Preview. Estimate, 2026 [T1-S15]
- In February 2026 the top Humanity's Last Exam score was 37.52 per cent (Gemini 3 Pro Preview). Epoch AI rates the benchmark "Flawed". Estimate, February 2026 [T1-S15]
- On GDPval-AA v2.1, Opus 5.5 scores 1,846 Elo and GPT-6 Astra 1,542 Elo, from one comparison site. Official GDPval win rates were not found. Uncertain, 2026 [T1-S16]
- Claude Opus 5.5 reportedly scores 89.9 per cent on SWE-bench Pro and 66.4 per cent on Terminal-Bench 4.0, from a third-party guide quoting the system card. Uncertain, September 2026 [T1-S17]
</group>

<group name="T1c. Open-weight models, errors and misleading scores">
- Epoch AI finds open-weight models trail closed frontier models by about four months (8 ECI points) since January 2026, up from three months before. Estimate, 29 May 2026 [T1-S18]
- Epoch AI finds the gap on cyber capability is 6 to 7 months. Estimate, 16 October 2026 [T1-S18]
- The UK AI Security Institute says GLM-5.2 and DeepSeek V4-Pro match closed models released 4 to 7 months earlier. Estimate, 2026 [T1-S18]
- OpenRouter says open-weight models passed 50 per cent of tokens in April 2026, peaked at 79 per cent in early July, and stayed above 62 per cent. Reported, 2026 [T1-S19]
- OpenRouter's October 2026 recap puts open weights at about one quarter of paid spend, up from 11 per cent in January. Reported, October 2026 [T1-S19]
- OpenRouter is a router used by developers who shop on price, so its token share does not equal share of all enterprise use. Estimate, 2026 [T1-S19]
- OpenAI stopped reporting SWE-bench Verified in February 2026 because of training contamination. Scores had moved only from 74.9 to 80.9 per cent in six months. Reported, February 2026 [T1-S20]
- OpenAI later estimated about 30 per cent of SWE-bench Pro tasks are broken and withdrew its advice to use it. Reported, 2026 [T1-S20]
- On AA-Omniscience, a hallucination rate of 15.1 per cent is cited for Gemini 4 Argon and 29.3 per cent for Grok 4.7, from one secondary source. Uncertain, October 2026 [T1-S21]
- AA-Omniscience counts wrong answers among non-abstained answers, so a model that refuses more looks better. Vectara measures summary faithfulness instead. Reported, 2025, old source [T1-S21]
- METR's update of 24 February 2026 says that newer data show some evidence of a speedup, but that selection effects make the estimate unreliable. Press reports quote an 18 per cent speedup for developers who returned. Uncertain, 24 February 2026 [T1-S22]
</group>

<group name="T1d. Building with models: APIs, MCP, retrieval, agents, evals, coding tools">
- The Anthropic Messages API needs model, max_tokens and messages. System prompt is a top-level field, with no system role in messages. Reported, 2026 [T1-S23]
- Anthropic tools are passed as definitions, and the model replies with tool_use content blocks. Claude 4.7 and later models use adaptive thinking with an effort level of low to max and reject the old budget_tokens setting. Reported, 2026 [T1-S23] [T9-S31]
- The OpenAI Responses API sets effort as reasoning.effort and chains turns with previous_response_id. Top-level instructions do not carry over between turns. Reported, 2026 [T1-S24]
- MCP project blog (28 July 2026) says Tier 1 SDKs see close to half a billion downloads a month and each of the TypeScript and Python SDKs passed 1 billion total. Reported, 28 July 2026 [T1-S25]
- A tracker counted 64,935 servers in the official MCP Registry on 15 November 2026, up from close to 2,000 a year earlier. Estimate, November 2026 [T1-S25]
- Anthropic donated MCP to the Agentic AI Foundation under the Linux Foundation, with Block and OpenAI as co-founders. Reported, December 2025, old source [T1-S25]
- Guides place pgvector for small stores under about 5 to 10 million vectors, and Qdrant, Weaviate or Pinecone above that. Estimate, 2026 [T1-S26]
- Qdrant raised a $50 million Series B in March 2026. Estimate, March 2026 [T1-S26]
- In the LangChain survey of about 1,300 people, 57 per cent have agents in production and 32 per cent name quality as the top barrier. Reported, 2026 [T1-S27]
- In the same survey 89 per cent use observability but only 52 per cent run evals, and 53.3 per cent use LLM-as-judge. Reported, 2026 [T1-S27]
- A Berkeley-led study of 306 practitioners found 80 per cent deploy agents mainly to raise productivity. Reported, December 2025, old source [T1-S28]
- Stack Overflow's 2026 survey found 66 per cent of AI users work in coding agents, with 75 per cent using Anthropic models and 74 per cent OpenAI. Reported, 6 October 2026 [T1-S29]
- OpenAI reported over 5 million weekly Codex users on 2 June 2026. Reported, 2026 [T1-S30]
</group>

<group name="T1Ba. Newest flagships of Anthropic, xAI and Mistral">
- Anthropic released Claude Fable 5.2 and Claude Mythos 5.2 on 9 November 2026, according to the Claude Platform release notes. Reported, 9 November 2026 [T1B-S1]
- Both models have a 1,000,000-token context window and 128,000 maximum output tokens. Reported, November 2026 [T1B-S1] [T1B-S2]
- Mythos 5.2 is the same model as Fable 5.2 but only for organisations verified through Anthropic programmes such as the Cyber Verification Program. Reported, November 2026 [T1B-S1] [T1B-S2]
- Fable 5.2 is available on the Claude API, Amazon Bedrock, Google Cloud and Microsoft Foundry. Both models need 30-day data retention unless Anthropic authorises otherwise. Reported, November 2026 [T1B-S1]
- A third-party site lists Mythos 5.2 at $8 input and $40 output per million tokens, with no long-context surcharge. I did not see this on an Anthropic page. Estimate, November 2026 [T1B-S3]
- The Anthropic notes say fast mode gives up to 2.5 times the output speed, at $16 input and $80 output per million tokens. Reported, November 2026 [T1B-S1]
- Fable 5.2 is therefore newer than Claude Opus 5.5 (22 September 2026), and is the newest Claude flagship found as of 26 November 2026. Reported, November 2026 [T1B-S1]
- xAI has no official Grok 5 release, model card or context window found. The 1.5 million-token figure is a leak or claim, not an xAI source. Uncertain, 2026 [T1B-S4]
- One aggregator says Grok 4.7 was released on 21 September 2026. I could not check this against xAI. Uncertain, September 2026 [T1B-S4]
- Mistral put Mistral Large 4 into public preview on 6 October 2026, as an open-weight multimodal mixture-of-experts model. Estimate, October 2026 [T1B-S5]
- Mistral's changelog states a 1,000,000-token context for Large 4. Third-party listings differ, with OpenRouter at 524,288 and another site at 512,000. Uncertain, October 2026 [T1B-S5]
- One site gives Mistral Large 4 as about 1.05 trillion parameters. I did not find this on a Mistral page. Uncertain, October 2026 [T1B-S5]
</group>

<group name="T1Bb. Agents on real work, retrieval and long context">
- Gartner predicted on 25 June 2025 that over 40 per cent of agentic AI projects will be cancelled by the end of 2027, citing cost, unclear value and weak risk controls. Estimate, June 2025, old source [T1B-S6]
- Gartner said only about 130 of thousands of agentic AI vendors are real, and called the rest "agent washing". Estimate, June 2025, old source [T1B-S6]
- Gartner's 19 per cent "significant investment" figure comes from a January 2025 poll of 3,412 webinar attendees, not a broad enterprise survey. Estimate, June 2025, old source [T1B-S6]
- In Carnegie Mellon's TheAgentCompany benchmark (175 tasks in a simulated software company), Gemini 2.5 Pro fully completed 30.3 per cent and reached 39.3 per cent with partial credit. Reported, 2025, old source [T1B-S7]
- In the same benchmark the weakest early model, Qwen2-72B, completed 1.1 per cent of tasks. Reported, 2025, old source [T1B-S7]
- MIT NANDA's August 2025 report said 95 per cent of generative AI pilots show little or no P&L impact. Sample sizes vary by write-up, from 52 to 150 interviews. Estimate, August 2025, old source [T1B-S8]
- The same MIT report said bought-in tools succeed about two thirds of the time and internal builds about one third. Estimate, August 2025, old source [T1B-S8]
- One paper finds long context works better when evidence is spread over several documents, and retrieval works better when evidence is sparse and retrieval is accurate. Estimate, 2025 [T1B-S10]
- A practitioner test reported about 1 second for a retrieval pipeline against 30 to 60 seconds for a full long-context call. Estimate, 2026, one source [T1B-S10]
- I found no Anthropic or Google official guidance on when 1,000,000 tokens replaces retrieval. Practitioner rule: long context for one bounded document, retrieval for large changing stores. Estimate, 2026 [T1B-S10]
</group>

<group name="T1Bc. Misleading scores, official benchmark values and coding tools">
- Meta submitted an "experimental chat version" of Llama 4 Maverick to LMArena in April 2025, "optimized for conversationality". It ranked second. Reported, April 2025, old source [T1B-S11]
- When LMArena scored the public Maverick, it ranked below GPT-4o, Claude 3.5 Sonnet and Gemini 1.5 Pro. Reported, April 2025, old source [T1B-S11]
- The "Leaderboard Illusion" paper (Cohere, Stanford, Princeton and others) says Meta privately tested 27 variants on Arena between January and March 2025. It relied on self-identification of models. Estimate, April 2025, old source [T1B-S12]
- OpenAI's GPT-5.5 page lists 84.9 per cent GDPval (wins or ties), against 83.0 for GPT-5.4, 80.3 for Claude Opus 4.7 and 67.3 for Gemini 3.1 Pro. Reported, 2026 [T1B-S13]
- At launch in September 2025, GDPval showed Claude Opus 4.1 at 47.6 per cent wins or ties and GPT-5 high at 38.8 per cent. Reported, September 2025, old source [T1B-S13]
- I found no official GDPval score for GPT-6.2 Astra or Claude Fable 5.2. Uncertain, November 2026 [T1B-S13]
- The ARC-AGI-3 leaderboard shows low scores for AI models. One aggregator has GPT-5.6 Sol on top at 7.8 per cent in July 2026. Uncertain, July 2026 [T1B-S14]
- Epoch AI says the ARC-AGI-3 headline score is not a true percentage, because the human baseline affects it. Estimate, 2026 [T1B-S14]
- A 95.3 per cent entry on the ARC community board is a Human Intelligence Harness run, not a standalone AI result. Reported, 2026 [T1B-S14]
- Anthropic's engineering post on agent evals (about 9 January 2026) says grade the output rather than the path, read transcripts to check graders, and aim for a high pass^k. Reported, January 2026 [T1B-S15]
- LangChain's agent survey (over 1,300 people) says observability is adopted more widely than evaluation. I did not find a ranking of "hardest part". Reported, 2026 [T1B-S16]
- Claude Code run rate: Anthropic said $2.5 billion in February 2026. A tracker cites about $8 billion in May 2026, not confirmed by Anthropic. Uncertain, 2026 [T1B-S17]
- Cursor said it passed $1 billion annualised revenue in November 2025. Estimate, November 2025 [T1B-S18]
- OpenAI said on 21 July 2026 that Codex and ChatGPT Work together pass 10 million weekly active users. It gives no Codex-only split. Reported, July 2026 [T1B-S19]
- GitHub Copilot had 4.7 million paid subscribers in January 2026. Microsoft's October 2026 call gave only that Copilot daily users grew nearly 50 per cent in the quarter. Reported, October 2026 [T1B-S19]
</group>

<builder_notes>
- A request is model, system prompt, messages, a maximum output token cap, optional tool definitions and a reasoning effort setting. Anthropic puts system at top level, OpenAI uses instructions and reasoning.effort.
- Tool calling is a loop: the model asks for a tool, your code runs it, you send the result back. MCP standardises how tools are described and found.
- Output tokens, including hidden reasoning tokens, drive both cost and delay, so effort is a latency and price dial as well as a quality dial.
- RAG fetches relevant chunks, puts them in the prompt and asks the model to answer from them. pgvector is the default when Postgres already exists.
- Long context (1 million tokens) removes the need for retrieval on small corpora. It costs more per call and accuracy can drop in the middle of long inputs. (not searched)
- An agent loop calls the model, runs tools, feeds back results and repeats until a stop condition. Common failures are silent tool errors, context overflow and loops. (not searched)
- Scaffolding matters. One report found three frameworks on the same model scored 17 issues apart on SWE-bench.
- Evals are hard because there is no single right answer, test sets go stale and graders (LLM-as-judge) have their own bias. Adoption (52 per cent) trails observability (89 per cent).
- Developers delegate coding to agents, then review diffs and run tests. Verification time can cancel the gain, which METR's 2025 trial showed.
- Parameter counts of closed models are not published, so engineers pick models by price, speed and own evals rather than size. (not searched)
- Fable 5.2 always uses adaptive thinking. Disabling thinking or forcing tool use returns errors, and computer use needs the newer toolset. Check the migration guide before upgrading.
- Editing earlier turns can trigger a 400 error when a thinking block is sent back, so keep history intact in agent loops.
- A 1,000,000-token window is billed on every call. Use it for one bounded document, and keep retrieval for large changing corpora and for answers that need citations.
- Grade agent output, not the path. Read transcripts to check your grader, and measure repeat reliability with pass^k.
</builder_notes>

<investor_notes>
- Capability is rising fast. METR's doubling time of about 3.6 months suggests long tasks soon become routine. Critics point to error bars of thousands of hours and noisy task suites.
- Benchmarks saturate and leak. ARC-AGI-2 at 95 per cent and SWE-bench Verified retired mean they no longer separate top models. Newer tests such as TH2 and ARC-AGI-3 replace them.
- Open weights trail by about four months (Epoch) and hold most OpenRouter tokens but about a quarter of spend. This pressures closed-model pricing, yet the closed labs still win paid enterprise spend.
- Open models are mostly Chinese. That raises procurement, security and licence questions for Western buyers. Meta moved from open Llama to closed Muse.
- Model choice is not locked in. Developers use several providers and APIs are similar, so switching cost is low and margin pressure is real.
- Quality, not cost, is the top barrier to agents in production (32 per cent). Firms that sell evals, monitoring and guardrails gain, but the market is early.
- Coding agents are the clearest revenue today (Claude Code over $2.5 billion run rate in February 2026). Productivity evidence is mixed, with METR finding slowdown in 2025 and an uncertain speedup in 2026.
- Hallucination rates differ by benchmark and abstention rules, so a single headline error rate is not safe to quote to a board.
- Agent failure claims need method checks. Gartner's 40 per cent is a forecast, MIT's 95 per cent has a small sample, and TheAgentCompany used 2025 models, so all three are old.
- Run-rate figures for Cursor and Claude Code are mostly press or tracker numbers. Ask for company statements before repeating them.
- Benchmark owners can tune models for a leaderboard. Meta's Llama 4 Arena case shows a ranking can come from a model nobody can use.
</investor_notes>
</topic>

<topic key="T2" name="Model prices and token economics">
<group name="T2a. API list prices, November 2026 (US dollars for each million tokens)">
- Anthropic Claude Haiku 5.5 (small) lists at $0.10 input and $0.50 output for prompts up to 100,000 tokens. Estimate, November 2026 [T2-S1]
- Anthropic cache reads cost 0.1 times the input price in the official table, with 0.05 times for Opus 5.5 and 0.025 times for Fable 5.1. Reported, November 2026 [T2-S2]
- Anthropic lists cache reads at $0.20 for each million tokens for Claude Fable 5.2 and for Claude Opus 5.5, and at $0.10 for Claude Sonnet 5.5. Reported, 3 November 2026 [T2-S26]
- OpenAI GPT-6.2 Astra (flagship) lists at $8.00 input, $0.40 cached input and $40.00 output on the ChatGPT rate card. Reported, November 2026 [T2-S3]
- OpenAI GPT-6.2 Sol (middle) lists at $2.00 input, $0.10 cached input and $10.00 output. Reported, November 2026 [T2-S3]
- Google Gemini 4 Argon (flagship) costs $2.00 input and $10.00 output at an introductory rate to 30 November 2026. Estimate, November 2026 [T2-S5]
- Google Gemini 3.5 Flash (middle) lists at $0.75 input and $4.50 output on the Gemini API standard tier. A newer Gemini 3.6 Flash also exists, so check which model is current. Uncertain, November 2026 [T2-S6]
- xAI Grok 4.6 and 4.7 (flagship) list at $2.00 input, $0.50 cached input and $6.00 output for prompts under 200,000 tokens. Estimate, October 2026 [T2-S7]
- xAI Grok 4.1 Fast (small) lists at $0.20 input and $0.50 output, with a 2,000,000 token context window. Estimate, September 2026 [T2-S7]
- Mistral Large 3 lists at $0.50 input, $0.05 cached input and $1.50 output. Medium 3.5 lists at $1.50, $0.15 and $7.50. Reported, November 2026 [T2-S8]
- Mistral Small 4 (small) lists at $0.15 input, $0.015 cached input and $0.60 output. Reported, November 2026 [T2-S8]
- DeepSeek V4.1 Flash costs $0.30 input and $1.20 output at peak hours, and half that off peak. Estimate, October 2026 [T2-S9]
- DeepSeek V4 Pro costs $1.32 input and $3.96 output at peak hours, and half that off peak. Estimate, October 2026 [T2-S9]
- Open-weight Llama 3.3 70B costs about $0.88 for each million tokens on Together AI and $0.59 input on Groq, per comparison blogs. Estimate, 2026 [T2-S10]
</group>

<group name="T2b. Extra price rules">
- Anthropic charges 1.25 times the input price for a 5-minute cache write and 2 times for a 1-hour cache write. Reported, November 2026 [T2-S2]
- Anthropic Batch API gives 50 per cent off input and output. Cache and batch modifiers stack. Reported, November 2026 [T2-S2]
- Anthropic bills the whole request at premium rates once input passes 200,000 tokens. Reported, November 2026 [T2-S2]
- OpenAI renamed priority processing "Fast mode" on 30 July 2026. It bills per token at a premium over standard rates. Reported, July 2026 [T2-S11]
- OpenAI Batch API takes 50 per cent off and runs within 24 hours. Flex gives lower cost for slower service but is not added to new models. Reported, November 2026 [T2-S11]
- Above 272,000 input tokens, OpenAI reportedly bills the whole GPT-6.2 request at higher rates. Sources disagree on the new rates. Uncertain, November 2026 [T2-S3]
- Google lists a 50 per cent Batch API discount and charges storage for cached context, for example $0.50 to $1.00 for each million tokens each hour. Reported, 2026 [T2-S6]
- xAI doubles its rates once a prompt reaches 200,000 tokens. Estimate, October 2026 [T2-S7]
</group>

<group name="T2c. Price trend, volume and speed">
- Epoch AI finds the price for a fixed quality level falls about 47 per cent each quarter, which is about 13 times each year. Estimate, 2026 [T2-S12]
- Epoch AI also finds the fall is 66 per cent each quarter at first, then 32 per cent each quarter two years later (4.7 times each year). Estimate, 2026 [T2-S12]
- The Epoch AI compute page says the cost at a fixed performance level halves about every 2 months. This is much faster than the other figures. Estimate, February 2026 [T2-S12]
- A November 2025 arXiv paper using Epoch data studies the falling cost of inference. A search summary gave a rising frontier price of 3 to 18 times each year, which needs checking. Uncertain, November 2025 [T2-S13]
- Stanford AI Index 2025 reported GPT-3.5 level cost fell from $20.00 to $0.07 for each million tokens between November 2022 and October 2024. Estimate, old source, 2025 [T2-S14]
- Flagship list prices have not fallen. Anthropic Fable 5.2 at $8 and $40 sits above Opus 5.5 at $4 and $20. Gemini 4 Argon doubles on 1 December 2026. Estimate, November 2026 [T2-S1]
- Google said at I/O in May 2026 that it processes over 3.2 quadrillion tokens each month across its AI surfaces. Reported, May 2026 [T2-S15]
- Google reported 1.3 quadrillion tokens each month in October 2025, and 480 trillion a year before that. Reported, old source, October 2025 [T2-S15]
- Google's model APIs process about 22 billion tokens each minute, per its second quarter 2026 remarks. Reported, July 2026 [T2-S15]
- OpenRouter reports 790 trillion tokens for October 2026, with agentic traffic now the majority. Reported, November 2026 [T2-S16]
- Microsoft said Foundry revenue more than tripled in its quarter reported 28 October 2026, with higher revenue for each token. Estimate, October 2026 [T2-S17]
- Artificial Analysis measures Cerebras at about 1,650 to 1,920 output tokens each second on gpt-oss-120b. Groq measures about 470 to 480. Estimate, 2026 [T2-S18]
- Artificial Analysis reportedly now ranks speed by time per task. Opus 5.5 takes about 26 minutes and Gemini 4 Carbon about 29 minutes. Uncertain, November 2026 [T2-S18]
</group>

<group name="T2d. Seat prices and energy for one prompt">
- ChatGPT Business costs $25 each month, or $20 with annual billing. ChatGPT Enterprise has no published price. Reported, 2026 [T2-S19]
- Analysts put ChatGPT Enterprise contracts near $60 for each user each month, in a range of $45 to $75. Estimate, 2026 [T2-S19]
- Claude Team costs $25 each month, or $20 with annual billing. The premium seat costs $125 monthly or $100 annual. Estimate, 2026 [T2-S19]
- Claude Enterprise lists a $20 seat each month on annual billing, with usage billed on top at API rates. Estimate, 2026 [T2-S19]
- Microsoft 365 Copilot costs $30 for each user each month on annual billing, on top of a base licence. Reported, 2026 [T2-S20]
- Microsoft 365 Copilot Business costs $21 list, or $18 on promotion. The promotion end date is disputed. Estimate, 2026 [T2-S20]
- Google Gemini Enterprise Standard costs $30 for each user each month on a 12-month term. Plus costs $50. Estimate, 2026 [T2-S20]
- GitHub Copilot Business costs $19 and Enterprise $39 for each user. GitHub moved to credits worth $0.01 each on 1 June 2026. Estimate, 2026 [T2-S21]
- Cursor lists Ultra at $200 each month. Sources disagree on other plan names and on Teams at $30 or $40. Uncertain, 2026 [T2-S21]
- Google measured a median Gemini text prompt at 0.24 Wh, 0.03 gCO2e and 0.26 mL of water. Reported, old source, August 2025 [T2-S22]
- Google's narrower active-chip method gives 0.10 Wh and 0.12 mL for the median prompt. Reported, old source, August 2025 [T2-S22]
- OpenAI states an average ChatGPT query uses 0.34 Wh and about 0.3 mL of water, with no method published. Reported, old source, June 2025 [T2-S22]
- Mistral's life cycle study found a 400-token answer used about 45 mL of water and 1.14 gCO2e, with training included. Reported, old source, July 2025 [T2-S23]
</group>

<group name="T2Ba. Cost of one task, caching and cost control">
- Anthropic's Claude Code costs page reports an average of about $13 for each developer for each active day, and $150 to $250 for each developer each month. Reported, 2026 [T2B-S1]
- The same Anthropic page says costs stay under $30 for each active day for about 90 per cent of users. Reported, 2026 [T2B-S1]
- An earlier version of that page gave about $6 for each developer day, with 90 per cent of users under $12. Some blogs still repeat the old figure. Reported, old source, 2025 [T2B-S1]
- Enterprise teams can read per-user usage and cost through an Analytics API, and API organisations can set workspace spend limits on Claude Code. Reported, 2026 [T2B-S1]
- One team reported its Claude Code cost for each developer day fell from $13.20 to $7.40 after enabling prompt caching. This is a single anecdote. Estimate, 2026 [T2B-S2]
- No official figure was found for one deep research task. A third-party guide assumes 50,000 input tokens, 20,000 output tokens and 15 searches, giving about $1.45 on o3-deep-research. Estimate, 2026 [T2B-S4]
- OpenAI lists o3-deep-research at $10 input and $40 output for each million tokens, plus a fee for each search call. Reported, 2026 [T2B-S4]
- An OpenAI forum user reported a deep research run that counted about 1.2 million tokens for a final report of about 7,000 tokens. Estimate, 2026 [T2B-S4]
- TikTok reported about 50 per cent savings on an AI agent after adopting prompt caching, measured against a no-cache cost. Reported by customer, 2026 [T2B-S5]
- ProjectDiscovery raised its cache hit rate from 7 per cent to 74 per cent by reordering prompts, and cut inference cost by 59 per cent. Estimate, 2026 [T2B-S5]
- One developer reported a 78 per cent cut in a monthly Claude bill after rolling out prompt caching. Uncertain, self-reported single case, 2026 [T2B-S5]
- One analysis says a 90 per cent cut on cached input equals only a 25 to 35 per cent cut in total cost, depending on the input to output ratio. Estimate, 2026 [T2B-S5]
- The RouteLLM paper from Berkeley reports more than 2 times cost savings on benchmarks with little loss of quality. Estimate, 2024 [T2B-S6]
- A secondary blog says RouteLLM cut cost by over 85 per cent on MT Bench by sending only 14 per cent of queries to the strong model. Uncertain, old source, 2024 [T2B-S6]
- A practitioner post puts typical production savings from model routing at 40 to 60 per cent. Other guides say caching, effort caps and batch matter more. Uncertain, 2026 [T2B-S6]
</group>

<group name="T2Bb. Gateways and cloud routes">
- OpenRouter passes provider list prices through with no markup on each request. It charges 5.5 per cent when you buy credits, with a minimum of $0.80. Reported, November 2026 [T2B-S7]
- OpenRouter's Business plan charges 8 per cent on credit purchases, and crypto top-ups cost 5 per cent. Reported, November 2026 [T2B-S7]
- OpenRouter's bring-your-own-key use above the free allowance costs 5 per cent of the normal price. Reported, November 2026 [T2B-S7]
- Vercel AI Gateway charges provider list prices with no markup on tokens, including bring-your-own-key use. Each team gets $5 of free usage each month. Reported, November 2026 [T2B-S8]
- Cloudflare AI Gateway core features are free. The cost shows up in log storage, with a 100,000 log cap on the free plan, per a Vercel comparison. Reported, with biased secondary source, November 2026 [T2B-S9]
- Amazon Bedrock offers global endpoints at no premium and regional endpoints at a 10 per cent premium for Claude Sonnet 4.5 and later models. Reported, 2026 [T2B-S10]
- Amazon Bedrock offers batch inference at 50 per cent below on-demand for select models, including Anthropic's. Reported, 2026 [T2B-S10]
- Anthropic says Claude per-token prices on Amazon Bedrock match the direct API on global endpoints. Reported, 2026 [T7B-S10]
</group>

<group name="T2Bc. Limits, speed and why output costs more">
- Anthropic Tier 1 needs a $5 credit purchase and has a $100 monthly spend cap. Reported, 2026 [T2B-S11]
- Anthropic's older Tier 1 row for Opus 4.x and Sonnet 4 is 50 requests, 30,000 input tokens and 8,000 output tokens a minute. Reported, old source, 2025 [T2B-S11]
- A current Anthropic table lists Claude Fable 5.x at 1,000 requests, 500,000 input tokens and 100,000 output tokens a minute. The tier of that row is not stated. Uncertain, 2026 [T2B-S11]
- Anthropic counts cache reads outside the input token limit for most models, and output limits count only tokens actually generated. Reported, 2026 [T2B-S11]
- OpenAI Tier 1 needs $5 paid with a $100 monthly cap. Tier 2 needs $50 paid with a $500 cap. Tiers 3 to 5 need $100, $250 and $1,000. Reported, 2026 [T2B-S12]
- OpenAI promotes accounts automatically as spend rises. A 7-day wait for Tier 2 was not confirmed. Reported, 2026 [T2B-S12]
- Artificial Analysis lists Claude Opus 5.5 at about 97 output tokens a second at max effort, and 78.8 at medium effort. Pages disagree by language version. Estimate, November 2026 [T2B-S13]
- Artificial Analysis shows Opus 5.5 time to first answer token of 6.16 seconds at low effort and 154.80 seconds at xhigh effort. Estimate, November 2026 [T2B-S13]
- Artificial Analysis measures speed after the first token arrives, and it measures reasoning models after thinking time. Time to first token includes network delay. Reported, 2026 [T2B-S14]
- Prefill handles all input tokens in one parallel pass. Decode needs one pass for each output token and is limited by memory bandwidth. Estimate, academic, 2026 [T2B-S15]
- A LessWrong discussion argues the raw compute is similar for input and output. The price gap then reflects memory needs and pricing choice. Estimate, 2026 [T2B-S15]
</group>

<group name="T2Bd. Conflicts resolved">
- GPT-6.2 Astra lists at $8 input, $0.40 cached and $40 output for prompts up to 272,000 tokens. It launched on 17 November 2026 alongside GPT-6.2 Sol. Reported, November 2026 [T2B-S16]
- The $10 and $50 pair is the older GPT-6 Astra price. GPT-6.2 Astra is 20 per cent cheaper than it. Estimate, November 2026 [T2B-S16]
- GPT-6 Luna lists at $0.10 input, $0.01 cached and $0.50 output, with a 1.05 million token window. Aggregators agree. OpenAI's page was not seen. Estimate, November 2026 [T2B-S17]
- GPT-5.6 Luna was $0.20 input and $1.20 output, so GPT-6 Luna is about half the input price. Estimate, 2026 [T2B-S17]
- Gemini 3.1 Flash-Lite lists at $0.25 input, $0.025 cached and $1.50 output. Google's Cloud table shows $1.50 for the Global tier. Reported, 2026 [T2B-S18]
- Gemini 3.1 Flash-Lite output rose from $0.40 on the 2.5 version to $1.50. Estimate, 2026 [T2B-S18]
- gpt-oss-120b costs $0.15 input and $0.60 output on Groq and Fireworks, per one aggregator. Other pages show $0.04 and $0.17 on OpenRouter. Uncertain, 2026 [T2B-S19]
</group>

<builder_notes>
- Rate limits are counted for each model class in requests, input tokens and output tokens a minute. Anthropic applies them to the organisation, not to each key. [T2-S24]
- Account tiers rise by cumulative deposit or spend. OpenAI now shows Build, Launch and Grow tiers, with Build at 5,000 requests and 1,000,000 tokens a minute. Old Tier 1 to 5 pages also exist. [T2-S25]
- Anthropic cache reads cost 0.1 times input or less, so a stable prompt prefix is the main saving. Write premium is 1.25 times for 5 minutes. [T2-S2]
- Cache hits in batch jobs are best effort because requests run in any order. [T2-S2]
- Long-context surcharges apply to the whole request, not just the excess tokens. Count tokens before sending large documents.
- Reasoning tokens are billed as output and are hidden, so cost for each task can vary many times for the same prompt. Cap reasoning effort for routine calls.
- Fast hosts such as Cerebras and Groq serve open-weight models at several hundred to about 1,900 tokens a second, against tens for flagship models. [T2-S18]
- Gateways such as OpenRouter, Vercel AI Gateway, Cloudflare AI Gateway and Bedrock add routing, fallback and logging. Price difference from direct API was not searched. (not searched)
- Common cost controls are routing easy work to small models, caching prefixes, batching offline work, trimming context and capping output. Published savings were not searched. (not searched)
- Peak and off-peak pricing at DeepSeek means price depends on the hour, so schedule bulk jobs off peak. [T2-S9]
- Put stable text first in a prompt and variable text last. Reordering alone lifted one team's cache hit rate from 7 to 74 per cent. [T2B-S5]
- Gateway fees differ in kind. OpenRouter charges on top-ups, Vercel charges no token markup, and Cloudflare's cost is log volume. Compare these before choosing. [T2B-S7]
- Bedrock regional endpoints cost 10 per cent more than global ones. Choose global unless data residency requires a region. [T2B-S10]
- Reasoning tokens inflate bills. One forum user reported billed output far above visible output on GPT-5.6, which is unconfirmed. [T2B-S20]
- Anthropic output limits count generated tokens, not max_tokens, so a high max_tokens setting does not eat rate limit. [T2B-S11]
</builder_notes>

<investor_notes>
- Cheap tiers are very cheap and falling, while flagship list prices are flat or rising. Spend therefore depends on mix and volume, not on a single falling price.
- Epoch's 13 times a year for a fixed quality level is a fast estimate. Other work suggests slower rates, so use a range and say the sources disagree.
- Hidden reasoning tokens and agent loops raise the number of tokens per task. Falling unit prices can still mean rising bills.
- Token volume is growing fast. Google reports 3.2 quadrillion each month, but analysts say such counts include much low-value traffic. Treat them as activity, not revenue.
- Microsoft said token prices came in higher than expected, which hints that mix is moving to expensive models. Source is a machine transcript summary. [T2-S17]
- Seat prices cluster at $20 to $30 for each user each month. Bundling, such as Gemini inside Workspace, pressures the standalone seat price.
- Enterprise deals often add usage-based billing on top of seats, so seat price understates real cost for heavy coding teams.
- Energy for one prompt is small, near 0.24 to 0.34 Wh. Figures are company-reported, use different methods and are over a year old.
- Introductory prices, such as Gemini 4 Argon to 30 November 2026, mean list prices in a model should be checked on the date used.
- Claude Code at about $13 for each developer day is about $150 to $250 a month, which is far above a $20 to $30 seat price. [T2B-S1]
- Savings claims for caching come from vendors and customers. Total savings are smaller than the headline 90 per cent, often 25 to 60 per cent. [T2B-S5]
- Gateways add little direct cost. The margin pressure is more likely to come from the cloud route premium and log storage than from token markup. [T2B-S7]
</investor_notes>
</topic>

<topic key="T3" name="Chips and hardware">
<group name="T3a. Nvidia results, share and roadmap">
- Nvidia reported revenue of $115.8 billion for the quarter to 25 October 2026, up 103 per cent from a year earlier. Reported, 17 November 2026 [T3-S1]
- Nvidia data centre revenue was $107.6 billion in that quarter, up 110 per cent from a year earlier, and about 93 per cent of total revenue. Reported, 17 November 2026 [T3-S1]
- Nvidia gross margin was 74.8 per cent on a GAAP basis and 74.9 per cent on a non-GAAP basis. Reported, 17 November 2026 [T3-S1]
- Nvidia guides next quarter revenue to $130.0 billion, plus or minus 3 per cent, and assumes no data centre compute revenue from China. Reported, 17 November 2026 [T3-S1]
- Nvidia guides next quarter gross margin to 71.0 to 72.0 per cent. The CFO commentary links the sequential dip to the first Rubin ramp. Reported, 17 November 2026 [T3-S2]
- Estimates of Nvidia share of AI accelerators range from about 70 to 90 per cent. The range depends on whether custom chips of the clouds are counted. Estimate, 2026 [T3-S3]
- Bloomberg is cited for an 86 per cent Nvidia share of AI accelerator sales in 2025, unchanged from 2024. Estimate, secondary source, 2026 [T3-S3]
- One forecast puts custom ASIC AI servers at 27.8 per cent of shipments in 2026, with ASIC shipments growing 44.6 per cent against 16.1 per cent for merchant GPUs. Estimate, 2026 [T3-S3]
- Nvidia roadmap: Vera Rubin in 2026, Rubin Ultra in the second half of 2027, and Feynman in 2028 with die stacking and custom HBM. Reported, GTC 2026 update [T3-S4]
- Nvidia now pairs Feynman with a new CPU called Rosa. Earlier GTC 2025 material paired it with Vera. The newer plan replaces the older one. Reported, GTC 2026 [T3-S4]
</group>

<group name="T3b. Hardware purchase prices and rack power">
- Nvidia does not publish list prices for a B200 GPU. Street quotes run $45,000 to $55,000 and volume list estimates run $30,000 to $40,000. Estimate, 2026 [T3-S5]
- An 8-GPU B200 server costs about $360,000 to $560,000. A typical integrated quote is near $450,000. Estimate, September to October 2026 [T3-S5]
- Lenovo listed an 8-GPU B200 server at $550,475 in June 2026. A Supermicro 8-GPU B200 system listed at $384,228 at Newegg in September 2026. Reported, retailer listings [T3-S5]
- A GB200 NVL72 rack with 72 GPUs costs $2.8 million to $3.4 million. Nvidia has never confirmed rack list prices. Estimate, 2026 [T3-S6]
- A GB200 NVL72 rack draws about 132 to 140 kW, which is higher than the 120 kW of the first pass. Estimate, 2026 [T3-S6]
- A Vera Rubin NVL72 rack costs $7.0 million to $8.8 million. Morgan Stanley estimates about $7.8 million for large cloud buyers. Estimate, 2026 [T3-S6]
- A Vera Rubin NVL72 rack draws 180 kW in the lower Max-Q mode and 220 kW in Max-P mode, in a SemiAnalysis model. Estimate, 2026 [T3-S7]
- Nvidia renamed Vera Rubin NVL144 to Vera Rubin NVL72, so sources use both names for the same generation. Check which one a figure covers. Reported, 2026 [T3-S6]
</group>

<group name="T3c. Custom chips, Broadcom, Marvell, AMD, China">
- Broadcom AI semiconductor revenue was $16.7 billion in its fiscal third quarter of 2026, up 221 per cent from a year earlier. Reported, September 2026 [T3-S8]
- Broadcom guides AI semiconductor revenue to $21.7 billion in its fiscal fourth quarter, with a fiscal 2026 AI forecast of $58 billion. Reported, September 2026 [T3-S8]
- Marvell reported record revenue of $2.739 billion in its fiscal second quarter of 2027, with data centre revenue of $2.17 billion. Reported, 2026 [T3-S9]
- Marvell expects custom silicon revenue to grow more than 20 per cent in fiscal 2027 and more than double in fiscal 2028. Reported, 2026 [T3-S9]
- Google is projected to ship 4.3 million TPUs in 2026 and more than 35 million by 2028. Estimate, mostly late 2025 sources, old source [T3-S10]
- Anthropic holds a TPU deal for up to 1 million chips. The first phase is 400,000 Ironwood units worth about $10 billion in racks. Estimate, old source [T3-S10]
- Amazon said its chip business passed a $20 billion annual run-rate in the first quarter of 2026. This figure covers Graviton, Trainium and Nitro together. Reported, April 2026 [T3-S11]
- Amazon says Trainium3 began shipping at the start of 2026 and is 30 to 40 per cent better in price performance than Trainium2. Reported, 2026 [T3-S11]
- Amazon plans to sell Trainium chips outside AWS late in 2027. Reported, 29 October 2026 [T3-S11]
- Meta unveiled MTIA 300, 400, 450 and 500 on 11 March 2026. In April 2026 it widened its Broadcom partnership for more MTIA generations. Reported, 2026 [T3-S12]
- Microsoft began deploying Maia 200 in January 2026. One report cites a delay of about six months in the next generation. Estimate, 2026 [T3-S12]
- AMD reported record revenue of $13.4 billion in the third quarter of 2026. Its data centre segment earned about $8.5 billion, up 97 per cent. Reported, 2026 [T3-S13]
- AMD named Anthropic, Meta, Microsoft, OpenAI and Oracle as lead Helios customers, and began volume shipments of the MI455X. Reported, 2026 [T3-S13]
- AMD guides fourth quarter revenue to about $17 billion. AMD does not split MI450 revenue from server CPU revenue. Reported, 2026 [T3-S13]
- The US now reviews H200 and MI325X sales to China case by case. Applicants face a 25 per cent fee, third-party review and limits on volume. Reported, January 2026 [T3-S14]
- Huawei targets about 750,000 Ascend 950PR chips in 2026. Epoch AI says the 950 offers about half the H100 performance. Estimate, 2026 [T3-S15]
- Huawei and SMIC face limits in HBM and packaging. SemiAnalysis projects SMIC advanced capacity of 60,000 wafers a month in 2026. Estimate, 2026 [T3-S15]
</group>

<group name="T3d. Memory, foundry, packaging and old chips">
- Counterpoint puts HBM share in the first quarter of 2026 at SK Hynix 58 per cent, Samsung 21 per cent and Micron 21 per cent. Estimate, 2026 [T3-S16]
- SK Hynix held 69 per cent of HBM a year before the first quarter of 2026. Estimate, 2026 [T3-S16]
- Samsung finished HBM4 validation first and began shipping in the second quarter of 2026. Its HBM4 yield reportedly reached 80 per cent by August 2026. Estimate, 2026 [T3-S17]
- TrendForce says HBM contract prices could rise 70 to 140 per cent in 2027. Estimate, 2026 [T3-S18]
- HBM3E spot prices were reported at 4 to 5 times long-term contract levels in September 2026. Estimate, one source [T3-S17]
- Bloomberg says relief from the memory shortage is more than a year away. Estimate, 2026 [T3-S18]
- TSMC had 73 per cent of the pure foundry market in Counterpoint data, and 72.5 per cent of all foundry revenue in the second quarter of 2026 on TrendForce data. Estimate, 2026 [T3-S19]
- TSMC kept its 2026 capital budget at $60 billion to $64 billion and guides fourth quarter revenue to $52.3 billion to $54.3 billion. Reported, October 2026 [T3-S20]
- TSMC CoWoS capacity may reach 125,000 to 140,000 wafers a month by end 2026, up from about 70,000 in 2025. Estimate, 2026 [T3-S21]
- Morgan Stanley estimates Nvidia holds about 60 per cent of TSMC CoWoS capacity for 2026. Another report gives 800,000 to 850,000 wafers. Estimate, 2026 [T3-S21]
- ASML reported third quarter 2026 sales of EUR 11.7 billion and says its planned 2027 and 2028 supply will fall short of customer demand. Reported, October 2026 [T3-S22]
- ASML expects full year 2026 sales of EUR 44 billion to EUR 45 billion and plans 30 per cent more EUV and DUV capacity in 2027. Reported, October 2026 [T3-S22]
- A used H100 sells for about $15,000 to $28,000. A used 8-GPU node sold near $195,000 in August 2026. Estimate, 2026 [T3-S23]
- American Compute forecasts H100 residual value of 11 to 19 per cent of list in 2027 and 5 to 7 per cent in 2028. Estimate, forecast [T3-S23]
- Dealer asks for used H100 SXM run 1.16 times realised prices, so listings overstate value. Estimate, October 2026 [T3-S23]
</group>

<group name="T3Ba. Why GPUs, training against inference, old chip life and value">
- Nvidia explains that neural network work is mostly many identical matrix multiplications, which a GPU runs in parallel across thousands of cores, and Tensor Cores speed up this maths. Reported (vendor), undated page [T3B-S1]
- Google Cloud says GPUs spread work across many cores in parallel, while CPUs have fewer, stronger cores. It calls GPUs a strong choice for training or running complex models. Reported (vendor), undated page [T3B-S2]
- Nvidia defines training as adjusting a model's weights using data, and inference as putting the learned model to work on new data. Inference cost is often measured per token. Reported, page updated October 2025 [T3B-S3]
- Google calls Ironwood, its seventh TPU, the first TPU built for inference. It has 192 GB of memory and 7.37 TB/s of HBM bandwidth per chip. Reported, April 2025, old source [T3B-S4]
- Ironwood comes in 256-chip and 9,216-chip configurations, and Google says it also handles training of large models. So the training and inference split is a design emphasis, not a hard line. Reported, April 2025, old source [T3B-S4]
- IBM says specialised AI accelerators such as TPUs and NPUs are often more energy efficient than GPUs for narrow tasks. Reported (vendor), undated [T3B-S5]
- Meta's Llama 3 run on 16,384 H100 GPUs over 54 days had 419 unplanned interruptions. GPU faults caused 148 (30.1 per cent) and HBM3 faults caused 72 (17.2 per cent). Reported, 2024, old source [T3B-S6]
- Press analysis turned the Meta data into an H100 annualised failure rate of about 9 per cent, rising to about 27 per cent over three years. This is a derived estimate, not a Meta figure. Estimate, old source [T3B-S6]
- An unvetted research page estimates a permanent H100 annual failure rate of 2.5 to 6 per cent, central 4 per cent. Uncertain, 2026 [T3B-S6]
- A peer-reviewed study of 2.5 years and 11.7 million GPU hours on the Delta system found H100 more resilient than A100 on most parts, but memory error time between errors was 3.2 times lower. Reported (peer reviewed), 2025 [T3B-S7]
- An unnamed Google architect said data centre GPUs last 1 to 3 years at high utilisation. This is a second-hand quote about use, not a measured failure rate. Uncertain, October 2024, old source [T3B-S8]
- Microsoft, Alphabet and Meta stretched server lives to 5.5 to 6 years for accounting between 2023 and 2025. Reported, via secondary source [T3B-S9]
- Silicon Data's neo-cloud H100 rental index read $2.88 per GPU-hour on 24 October 2026, up from $2.00 on 9 December 2025. Estimate, October 2026 [T3B-S9]
- Resale low side: AMCompute shows H100 residual value bands of about 11 to 19, 5 to 7 and 2 to 3 per cent of price new. The year of each band is not stated. Estimate, 2026 [T3B-S10]
- Resale high side: Silicon Data says A100 and H100 residual values exceed what 3-year or 5-year straight-line schedules imply. One report says H100 prices rose about 30 per cent. Estimate, 2026 [T3B-S11]
- The 60 to 80 per cent figure comes from an Introl guide on GPU resale in general, not from H100 data. It also cites CoreWeave rebooking 2022 H100 contracts at 95 per cent of original price. Uncertain, secondary source [T3B-S11]
- A 2026 argument says H100 resale held up because many sites could not yet host liquid-cooled Blackwell, and the 700 W air-cooled H100 still fitted. It expects this support to fade. Estimate, 2026 [T3B-S11]
- Likely reconciliation: the 5 to 19 per cent band is a share of price new at a given age. The 60 to 80 per cent claim is generic. Uncertain, reading of the sources [T3B-S10] [T3B-S11]
</group>

<group name="T3Bb. Custom chips, generation gains, network, memory, TSMC, AMD, start-ups">
- Google claims total cost of ownership for an Ironwood chip is about 44 per cent below a GB200 server. This is Google's own figure. Reported (vendor claim), 2026 [T3B-S12]
- AWS claims up to 50 per cent lower cost than comparable Nvidia instances for supported work. Midjourney reportedly cut monthly compute from $2.1 million to $700,000 after moving to TPUs. Reported (vendor claim) and Estimate, 2026 [T3B-S12]
- Epoch AI says Google, Amazon and others do not disclose chip sales, so its TPU and Trainium unit figures are estimates. No independent per-chip cost against Nvidia was found. Reported, 2026 [T3B-S12]
- Amazon said Anthropic ran about 500,000 Trainium2 chips on Project Rainier in late 2025 with plans to pass 1 million. A tour report counted 1.4 million Trainium chips across all generations. Reported and Estimate, 2025 to 2026 [T3B-S13]
- Microsoft says Maia 200 beats Amazon's latest Trainium by three times on some tests, but the chip slipped about six months. Meta says MTIA runs hundreds of thousands of units for inference and does not replace Nvidia. Estimate, 2026 [T3B-S12]
- OpenAI and Broadcom announced on 13 October 2025 a deal for 10 GW of OpenAI-designed accelerators, with first racks in the second half of 2026 and completion by end 2029. Reported, October 2025 [T3B-S14]
- Financial terms of the OpenAI and Broadcom deal were not disclosed. The Financial Times estimated $350 billion to $500 billion in total cost to OpenAI. Estimate, October 2025, old source [T3B-S14]
- Nvidia says GB300 NVL72 gives up to 50 times more throughput per megawatt and 35 times lower cost per token than Hopper on low-latency agentic work, citing SemiAnalysis InferenceX. Reported (vendor claim), 2026 [T3B-S15]
- Nvidia says Blackwell costs about twice as much as Hopper and argues cost per token is the right test. InferenceMAX v1 showed B200 above 4 times H200 per-GPU throughput on Llama 3.3 70B. Reported (vendor claim), 2025 [T3B-S15]
- At CES 2026 Nvidia said Vera Rubin NVL72 gives up to 5 times the inference performance and 10 times lower cost per token than Blackwell. The 10 times figure used Kimi-K2-Thinking. Reported (vendor claim), January 2026 [T3B-S16]
- Other outlets quoted one-seventh of GB200 cost per token for large mixture-of-experts models. In July 2026 Nvidia cited up to 10 times more tokens per megawatt than GB200 NVL72. Reported (vendor claim), 2026 [T3B-S16]
- A CoreWeave DeepSeek-R1 test reported 10 times more tokens per second per megawatt than Grace Blackwell NVL72. This is the only partner test found, and it is not fully independent. Estimate, 2026 [T3B-S16]
- Dell'Oro says Ethernet passed InfiniBand in AI back-end networks in 2025. InfiniBand held nearly 80 per cent of that switch spend two years earlier. Estimate, 2026 [T3B-S17]
- In the first quarter of 2026 Ethernet was about two-thirds of data centre switch sales in AI clusters, and InfiniBand was rebounding. Nvidia Spectrum-X Ethernet reached about $1.46 billion in IDC data. Estimate, 2026 [T3B-S17]
- Dell'Oro expects co-packaged optics to ramp on both Ethernet and InfiniBand switches and to add billions to the market. Supply limits are its main forecast risk. Estimate, 2026 [T3B-S17]
- In a reference design NVLink links GPUs inside a rack at 14.4 Tbps per GPU, while each GPU has an 800 Gbps network card for the links between racks. Reported (vendor design), 2024 to 2026 [T3B-S18]
- Mixture-of-experts layers need all-to-all traffic. When a layer outgrows one NVLink domain, traffic crosses racks and throughput drops. Straggler flows can stall a whole job. Estimate, 2026 [T3B-S18]
- Llama 3 trained on about 16,000 GPUs in one building. Llama 4 reached over 100,000 GPUs across buildings, with links at about 1:3 oversubscription and about 4 times the latency. Estimate, via preprint citing Meta talks [T3B-S18]
- Epoch AI estimates HBM was about 63 per cent of AI chip component cost in the fourth quarter of 2025, up from about 52 per cent in the first quarter of 2024. Estimate, 2026 [T3B-S19]
- Epoch's 90 per cent range for that 63 per cent is 54 to 73 per cent. It excludes system costs and covers only logic, HBM, CoWoS and chip parts. Estimate, 2026 [T3B-S19]
- Other analysts put HBM at 45 to 62 per cent of a GPU bill of materials, rising from B200 to Rubin. Estimate, 2026 [T3B-S20]
- A 36 GB 12-high HBM4 stack is estimated near $600 in 2026 and $1,300 in 2027. A tracker priced a 36 GB 12-high HBM3E stack at $300.87 on 13 September 2026. Estimate, 2026 [T3B-S20]
- TrendForce reportedly put HBM4 at $31 to $32 per GB and HBM3E at $17 to $18 per GB by August 2026. Epoch's earlier trend data gives about $13.50 per GB for HBM3E. Estimate, 2026 [T3B-S20]
- Wccftech reports memory costs of about $2 million in a $7.8 million Vera Rubin rack, after a 435 per cent memory price rise. Estimate, secondary source, 2026 [T3B-S20]
- Counterpoint's second quarter 2026 HBM table gives SK Hynix 50 per cent, Samsung 33 per cent and Micron 18 per cent, down from 64 per cent for SK Hynix a year earlier. Estimate, 2026 [T3B-S21]
- No third quarter 2026 HBM split was found. Counterpoint's third quarter DRAM revenue shares were Samsung 38 per cent, SK Hynix 29 per cent, Micron 21 per cent and CXMT 9 per cent. Estimate, 5 November 2026 [T3B-S21]
- Counterpoint expects Samsung to take the top HBM spot in 2027 as HBM4 ships. HBM revenue almost doubled year on year in the third quarter of 2026. Estimate, November 2026 [T3B-S21]
- Cerebras guides 2026 adjusted revenue of $940 million to $960 million, with backlog of $26.1 billion, mostly from OpenAI. Reported, November 2026, secondary summary [T3B-S23]
- Cerebras filed its S-1 on 17 April 2026 at about a $23 billion valuation. The OpenAI deal grew from a reported $10 billion in January 2026 to about $20 billion. Reported and Estimate, 2026 [T3B-S23]
- Nvidia licensed Groq inference technology on 24 December 2025 and hired its key engineers, reported at about $20 billion. Sacra says $17 billion was cash. Groq's 2025 revenue was projected near $500 million. Estimate, 2025 [T3B-S23]
- A new 8-GPU H100 HGX server costs about $250,000 to $350,000. CloudZero gives $250,000 to $320,000, with about $285,000 typical. Estimate, 2026 [T3B-S24]
- A Supermicro 8-GPU H100 HGX system listed at $306,672 on Newegg on 21 September 2026, out of stock. A DGX H100 from one reseller listed at $440,619.75. Reported (retailer listing), September 2026 [T3B-S24]
- A single new H100 costs about $25,000 to $31,000 in one guide and $30,000 to $40,000 street price in another. SXM modules have no standalone US price. Nvidia never published a list price. Estimate, 2026 [T3B-S24]
</group>

<builder_notes>
- A GPU suits AI work because training and inference are mostly large matrix multiplications that run in parallel, and HBM feeds the cores with high bandwidth. (not searched)
- Training needs high compute, large memory and fast links between chips. Inference is often limited by memory bandwidth and latency, so chips for each job are now designed differently. (not searched)
- Engineers rent GPUs when they need control, custom models or steady heavy use. They call a model API for speed and low volume, and they pick custom chips such as TPU or Trainium for cost at scale. (not searched)
- Custom chips need software porting. CUDA gives Nvidia a lock-in, and teams using TPU or Trainium work through JAX, XLA or the Neuron SDK. (not searched)
- Rack power is a design limit. A GB200 rack draws about 132 to 140 kW and a Vera Rubin rack 180 to 220 kW, so liquid cooling is needed. [T3-S6] [T3-S7]
- Memory is now a constraint as well as compute. HBM supply and CoWoS packaging cap how many accelerators ship. [T3-S17] [T3-S21]
- Large clusters are limited by the network. NVLink joins chips inside a rack, and InfiniBand or Ethernet with optical links joins racks, and a slow link idles the GPUs. (not searched)
- Failures matter at scale. Public training reports show frequent GPU and memory faults, so teams use checkpoints and spare nodes. I found no 2026 measured rate. (not searched)
- Per-chip price is a poor guide to cost per token. Rack price, power and utilisation matter more, and vendor performance claims should be checked. (not searched)
- Cost per token needs a named workload. Nvidia's 10 times and 50 times claims depend on model, context length and latency target, so re-run on your own model. [T3B-S15] [T3B-S16]
- Memory faults are a real failure source. HBM3 caused 17.2 per cent of Llama 3 interruptions, so checkpoints and spare nodes are standard. [T3B-S6] [T3B-S7]
- Tokens per megawatt is the useful unit for a power-limited site, because a site has a fixed power budget. [T3B-S15]
- Mixture-of-experts models stress the scale-up network. Plan expert placement so all-to-all traffic stays inside one NVLink domain. [T3B-S18]
- TPU and Trainium cost claims come from the vendors. Port a real workload and measure before trusting them. [T3B-S12]
</builder_notes>

<investor_notes>
- Bull case: Nvidia grew 103 per cent in a year with a 74.8 per cent margin, and supply of HBM, CoWoS and EUV is short through 2027. [T3-S1] [T3-S22]
- Bear case: Nvidia guides gross margin down to 71 to 72 per cent, and custom chips are growing faster than merchant GPUs. [T3-S2] [T3-S3]
- Broadcom and Marvell gain from custom chips. Broadcom's AI forecast of $58 billion for fiscal 2026 is a company target, and the OpenAI order is not yet confirmed. [T3-S8] [T3-S12]
- Memory makers hold pricing power. Rising HBM prices raise rack cost, so some value moves from Nvidia and clouds to SK Hynix, Samsung and Micron. [T3-S18]
- Concentration risk is high because TSMC makes most advanced chips and ASML has the only EUV tools. TSMC itself says it is prudent about 2027. [T3-S19] [T3-S20]
- China is a policy risk. Nvidia assumes no China data centre revenue, while Huawei grows but is limited by HBM and SMIC capacity. [T3-S1] [T3-S15]
- Old chip value is disputed. Resale forecasts of 5 to 19 per cent of list contrast with claims of 60 to 80 per cent recovery. The gap drives depreciation risk. [T3-S23]
- Rack prices are estimates, since Nvidia publishes no list price. Use ranges in any board paper. [T3-S6]
- Depreciation is the key dispute. Hyperscalers book 5.5 to 6 years, and resale bands of 2 to 19 per cent of price new suggest steep loss at the market. Rising rents in 2026 support the longer life for now. [T3B-S9] [T3B-S10]
- Both sides on old chips: rental prices up about 44 per cent since December 2025 favour long life. The 60 to 80 per cent resale claim is generic, and AMCompute bands are much lower. [T3B-S9] [T3B-S10] [T3B-S11]
- Memory is the larger share of accelerator component cost. HBM near 63 per cent in Epoch data shifts margin to SK Hynix, Samsung and Micron. [T3B-S19]
- Ethernet gains on InfiniBand, but Nvidia sells Spectrum-X Ethernet, so Nvidia keeps some of the network spend. [T3B-S17]
- Cerebras and Groq show OpenAI and Nvidia buying inference-specific designs. Cerebras depends heavily on one customer. [T3B-S23]
</investor_notes>
</topic>

<topic key="T4" name="Data centres and energy">
<group name="T4a. Cost to build and cost split">
- JLL forecasts the average global shell-and-core build cost at $11.3 million for each MW in 2026, up 6 per cent, after $10.7 million in 2025. Estimate, 2026 [T4-S1]
- JLL says tenant fit-out is extra and can reach $25 million for each MW for AI infrastructure. Estimate, 2026 [T4-S1]
- Cushman & Wakefield puts all-in greenfield cost at $8.9 million to $23.3 million for each MW in the United States and Canada, without chips. Costs rose 21 per cent since Q4 2024. Estimate, 2026 [T4-S2]
- Turner & Townsend quotes cost for each watt, not each MW. It reports average cost per watt up 13 per cent year on year, with the sharpest rises in North America and Europe. Estimate, 2026 [T4-S3]
- Epoch AI models a typical 1 GW hyperscaler site with GB200 NVL72 systems at about $38 billion of up-front cost and about $900 million of yearly running cost. Estimate, 2026 [T4-S4]
- Another analysis finds GPUs are about 39 per cent of capex. Nvidia's gross profit alone is about 29 per cent of all AI data centre cost. Estimate, 2026 [T4-S4]
- Bloomberg and Cushman & Wakefield estimate a 1 GW Abilene build at about $30 billion. That is about $17 billion for chips, about $3 billion for power infrastructure and about $2.4 billion for shell and construction. Estimate, 2025 [T4-S5]
- Foxconn puts a Nvidia Vera Rubin build at about $47 billion for each GW, based on about 3,557 racks at about $9.1 million each. Estimate, 2026 [T4-S6]
- Epoch's own site estimates imply about $38 million for each MW with chips, for example $35.8 billion for the 946 MW of Colossus 2. Estimate, 2026 [T4-S7] [T4-S8]
- With chips, sources give $30 billion to $55 billion for each GW. The first-pass range of $38 million to $60 million for each MW is only partly confirmed. Uncertain, 2026 [T4-S4] [T4-S5] [T4-S6]
</group>

<group name="T4b. Largest sites and power demand">
- Epoch ranks Anthropic and Amazon New Carlisle, Indiana, first at about 1,037 MW of IT power in November 2026. Estimate, 6 November 2026 [T4-S7]
- Epoch puts xAI Colossus 2 in Memphis at about 946 MW. It puts Stargate Abilene, Texas, at about 824 MW planned, with 618 MW operating on 10 September 2026. Estimate, 6 November 2026 [T4-S7] [T4B-S18]
- Amazon announced $11 billion for the New Carlisle campus in October 2025. Epoch estimates $34.5 billion, with 1,925 MW and $72.9 billion at full build. Reported and estimate, 2026 [T4-S8]
- Microsoft Fairwater Wisconsin is estimated at 369 MW and $14.0 billion now. Epoch projects 2,263 MW and $85.7 billion by Q2 2028. Microsoft's own pledge is over $7 billion. Estimate, 2026 [T4-S9]
- Microsoft Fairwater Atlanta began operating in October 2025. Epoch estimates 636 MW and $24.1 billion. Estimate, 2026 [T4-S9]
- Meta's Hyperion campus in Louisiana has up to $27 billion of development cost in a joint venture with Blue Owl. Meta agreed on 27 March 2026 to fund seven more Entergy gas plants. Reported, 2026 [T4-S10]
- Oracle and OpenAI dropped a 600 MW Abilene expansion in March 2026 and kept the committed 1.2 GW build. Oracle says its 4.5 GW OpenAI agreement is still on track. Reported, 2026 [T4-S11]
- The IEA estimates data centres used 415 TWh in 2024, about 1.5 per cent of world electricity. It projects about 945 TWh in 2030, just under 3 per cent. Estimate, 2025 [T4-S12]
- The IEA later put 2025 use at 485 TWh. China and the United States give nearly 80 per cent of growth to 2030. Estimate, 2026 [T4-S12]
- Berkeley Lab estimated data centres used 4.4 per cent of United States electricity in 2023. Its 2025 update sees 11.8 per cent in 2030, in a range of 9.5 to 15.3 per cent. Estimate, 2026 [T4-S13]
- EPRI puts the United States share at 4 to 5 per cent today and 9 to 17 per cent by 2030. Estimate, 2026 [T4-S14]
- The European Commission says EU data centres used 68 TWh in 2024. It expects 114 TWh by 2030, or 3.2 per cent of EU demand. Reported, 2026 [T4-S15]
- NESO expected just over 20 TWh of United Kingdom data centre demand by 2030 in 2025. Its 2026 outlook has 14.6 TWh by 2031. Oxford Economics says over 26 TWh, above 9 per cent. Estimate, 2026 [T4-S16]
</group>

<group name="T4c. Limits on growth and sources of power">
- GE Vernova held 116 GW of gas turbine backlog and slot reservations at the end of Q2 2026. Of this, 53 GW is firm. It now sells slots for 2031 delivery. Reported, 2026 [T4-S17]
- Siemens Energy had a 69 GW gas turbine backlog on 30 June 2026, with lead times of three years or more. Reported, 2026 [T4-S17]
- Generator step-up transformer lead times passed 160 weeks in Q1 2026, from 143 weeks on average in 2024. Distribution transformers took about 30 weeks in Q2 2025. Estimate, 2026 [T4-S18]
- The UK government says some transmission-connected projects face waits of up to 15 years. NESO shows 72.8 GW of data centre connection requests to 2039. techUK says this overstates real demand. Reported and estimate, 2026 [T4-S19]
- Enverus expects 29.6 GW of behind-the-meter gas to be added in the United States through 2030, with data centres at about 88 per cent of that demand. Estimate, 2026 [T4-S20]
- Cleanview counts about 2 GW of behind-the-meter capacity online in mid-2026. It lists 59 projects totalling about 90 GW that plan their own power. Estimate, 2026 [T4-S20]
- xAI runs gas turbines at Southaven, Mississippi. Cleanview counts about 1.3 GW and SemiAnalysis counts 460 MW. A lawsuit filed in April 2026 says the turbines lack permits. Uncertain, 2026 [T4-S8] [T4-S20]
- Meta signed a 20-year agreement for the 1,092 MW Clinton nuclear plant. Meta buys the clean energy attributes and the price is not public. Reported, June 2025 old source [T4-S22]
- Kairos and TVA agreed to supply 50 MW to the grid for Google data centres. The Hermes 2 reactor should start in 2030. Reported, 2026 [T4-S22]
</group>

<group name="T4d. Prices, leasing and the United Kingdom">
- The EIA reports a 2025 average United States industrial electricity price of 8.62 cents for each kWh. A secondary source gives 8.71 cents for May 2026. Reported, 2026 [T4-S23]
- DESNZ reports United Kingdom manufacturing electricity at 17.4 pence for each kWh in Q2 2026. All non-domestic users paid 24.5 pence. Reported, September 2026 [T4-S24]
- Eurostat reports the EU non-household average at 0.18 euros for each kWh in the first half of 2026 for 500 to 2,000 MWh users. Ireland is highest at 0.27 and Finland lowest at 0.09. Reported, 2026 [T4-S25]
- CBRE put the primary wholesale asking rate at a record $196.25 for each kW each month in H2 2025, up 6.6 per cent. Rates rose a further 4.3 per cent in H1 2026. Reported, 2026 [T4-S26]
- CBRE reports North American primary market vacancy at a record low 1.4 per cent in H1 2026. Northern Virginia is between 0.2 and 0.3 per cent. Reported, 2026 [T4-S26]
- Digital Realty guides to average stabilised development yields of 10.0 per cent or more in 2026. It cited 11.9 per cent on 769 MW under construction in February 2026. Reported, 2026 [T4-S27]
- Digital Realty bought a 64 per cent stake in 288 MW of leased Northern Virginia sites at a $7.8 billion gross value. The initial cap rate is above 6.5 per cent. Reported, Q2 2026 [T4-S27]
- From April 2027, subject to law, eligible 500 MW sites can get power discounts of up to 24 pounds for each MWh in Scotland and 14 pounds in the North East. Reported, 2026 [T4-S28]
</group>

<group name="T4e. Builder facts: PUE, cooling, latency and reliability">
- Uptime Institute's 2026 survey gives an average PUE of 1.52. Weighting by capacity gives 1.36. The 2025 figure was 1.54. Reported, 29 July 2026 [T4-S29]
- Google reports a fleet-wide PUE of 1.09 for 2025, flat on 2024. Reported, 30 June 2026 [T4-S30]
- GB200 NVL72 racks need direct-to-chip liquid cooling. Air cooling reaches its limit near 30 to 40 kW for each rack. Estimate, 2026 [T4-S31]
- Berkeley Lab estimates United States data centres used 17 billion gallons of cooling water in 2023. The average WUE was 0.36 litres for each kWh. Estimate, 2024 old source [T4-S32]
- EPRI compares a 150 MW site at 2.8 litres for each kWh with chillers against 0.2 litres with liquid cooling and dry coolers. Estimate, 2025 [T4-S32]
- Tier I to IV availability is 99.671, 99.741, 99.982 and 99.995 per cent. That is about 28.8 hours, 22 hours, 1.6 hours and 26 minutes of downtime a year. Reported, old source [T4-S33]
- Uptime's 2026 outage analysis found power caused 45 per cent of impactful outages in 2025, down from 54 per cent. Of respondents, 57 per cent said their last major outage cost over $100,000. Reported, 13 May 2026 [T4-S34]
- A chiller failure and thermal event hit AWS us-east-1 on 7 and 8 May 2026. The source is a secondary site. Uncertain, May 2026 [T4-S35]
- Equinix says training is largely not latency constrained and inference sits nearer users. Akamai says queuing delays grow sharply as GPU use rises. Estimate, 2026 [T4-S36]
</group>

<group name="T4Ba. Cost split, power cost and the parts of a site">
- Epoch's annualised model for a 1 GW GB200 site gives servers $5,021 million, networking $1,167 million and facility $1,387 million a year. Servers are about two thirds of annualised capex. Estimate, 2026 [T4B-S1]
- That annualised split is about 66 per cent servers, 15 per cent networking and 18 per cent facility, by the search tool's own arithmetic on Epoch's figures. Estimate, 2026 [T4B-S1]
- A Groww digest puts the building and its supporting systems at about 40 per cent of total build cost and chips and servers at about 60 per cent. Secondary source, Uncertain, 2026 [T4B-S2]
- Within non-IT construction, electrical systems are 40 to 45 per cent and the structure itself only 10 to 15 per cent. Secondary source, Uncertain, 2026 [T4B-S2]
- Axis Intelligence splits a 100 MW AI build as electrical 40 to 48 per cent, liquid cooling 29 to 33 per cent, shell about 15 per cent and security, fire and network about 7 per cent. Secondary, Uncertain, 2026 [T4B-S3]
- Reuters cites Rasgon: foundries, memory and wafer-fab equipment together capture only 3 to 4 per cent of data centre capex, about $1 billion to $1.2 billion for each GW. Estimate, 2026 [T4B-S4]
- Epoch sets annual total cost of ownership at $8.5 million for each MW, down from $10.8 million. At 1 GW that is about $8.5 billion a year, mostly capital charges. Estimate, 2026 [T4B-S5]
- Epoch finds GPUs are about 40 per cent of AI data centre power. It uses a peak PUE of 1.4, and a 2.5 times multiplier from GPU power to site power. Estimate, 2026 [T4B-S6]
- A grid link starts at a dedicated substation. Step-down transformers cut 115 kV or 69 kV to 13.2 to 34.5 kV. Switchgear splits the site into blocks, and unit transformers feed the halls. Estimate, 2026 [T4B-S7]
- Generators give long backup but start slowly. The UPS (battery bridge) covers the gap, with runtimes of typically 2 to 10 minutes. N+1 means one spare unit and 2N means double the units. Estimate, 2026 [T4B-S7]
- Cooling uses chillers, cooling towers, pumps and air handlers. Dry coolers serve warm-water loops. Traditional racks draw 5 to 15 kW and AI racks 60 to 120 kW or more. Estimate, 2026 [T4B-S7]
</group>

<group name="T4Bb. Time to build, grid waits and equipment backlogs">
- Epoch finds the time from construction start to 1 GW of facility power ranged from 1 to 3.6 years across tracked sites. Estimate, 2026 [T4B-S8]
- TechTarget says a typical data centre build takes 12 to 24 months. Colossus 1 reached 300 MW in 122 days and Colossus 2 built 200 MW in six months. Reported, 2026 [T4B-S8]
- At Abilene, Crusoe broke ground in summer 2024 and needs about 10 months for each hall from start to energising. Crusoe now says about 12 months for a project, against 30 to 36 months before. Reported, 2026 [T4B-S8]
- Carbon Direct puts the average large-load wait at about 40 months in PJM, 20 months in ERCOT and 25 months across the United States. Data-centre zones in PJM see 36 to 48 months. Estimate, May 2026 [T4B-S9]
- Data Center Frontier reports the ERCOT large-load queue at about 226 GW, with roughly 77 per cent tied to data centres. Other sources give 474 GW or 494 GW. Uncertain, 2026 [T4B-S9]
- Ember and the IEA say grid connection in the Frankfurt, London, Amsterdam, Paris and Dublin hubs averages 7 to 10 years, and up to 13 years in some cases. Estimate, 2026 [T4B-S10]
- The IEA says connection waits range from 2 to 10 years across Europe, while a data centre itself takes 1 to 2 years to build. Italy can connect in as little as 3 years. Estimate, 2026 [T4B-S10]
- Amazon faced waits of up to 7 years for new European grid connections. Nscale said in July 2026 that its UK campus connection would miss the 2027 opening. Reported, 2026 [T4B-S10]
</group>

<group name="T4Bc. Power deals, prices and the United Kingdom">
- Bloomberg reported analysts saying Microsoft would pay at least $100 per MWh for Three Mile Island power. Morgan Stanley estimated $98 per MWh. Neither company published a price. Estimate, 2024 old source [T4B-S11]
- The $1.6 billion figure linked to Three Mile Island is Constellation's restart cost, not a power price. This corrects loose press claims. Reported, 2024 old source [T4B-S11]
- Jefferies estimated the Meta and Constellation Clinton deal at about $70 per MWh. The price is not disclosed. Estimate, 2025 old source [T4B-S12]
- Amazon and Talen signed a 17-year, $18 billion Susquehanna deal, expanded to 1.92 GW through 2042. Talen's all-in plant cost was under $24 per MWh. Reported, 2025 old source [T4B-S12]
- Google signed a 25-year deal for about 615 MW from NextEra's Duane Arnold plant in Iowa. No price was found. Reported, 2025 old source [T4B-S12]
- RMI puts grid power for large loads at about $55 to $115 per MWh across eight tariffs. Rabobank puts behind-the-meter gas at $100 to $165 per MWh. Estimate, 2026 [T4B-S13]
- S&P Global estimates a combined-cycle plant serving a 627 MW West Texas data centre at about $61 per MWh levelised. Estimate, March 2026 [T4B-S13]
- LevelTen's Q3 2026 North American solar PPA offer price is $64.23 per MWh and wind is $68.27 per MWh. Solar is up about 6 per cent on the year. Reported, 2026 [T4B-S14]
- GBP/USD was about 1.33 on 12 November 2026 and GBP/EUR about 1.20 in mid-November. EUR/USD was not found directly. The implied rate is about 1.11. Estimate, November 2026 [T4B-S15]
- At $1.33 to the pound, UK manufacturing power at 17.4 pence for each kWh is about 23 US cents. All non-domestic power at 24.5 pence is about 33 cents. Estimate (derived), Q2 2026 [T4B-S15]
- DESNZ meter data puts GB data centres at about 4.5 TWh in 2024, about 2 per cent of the 249.2 TWh drawn from the grid. NESO had 5.0 TWh, also 2 per cent, for 2023. Reported, 2026 [T4B-S16]
- Figures of 5.9 per cent or 6 per cent for UK data centre share come from industry sources, not official statistics. Uncertain, 2026 [T4B-S16]
- UK AI Growth Zones: Culham (began at 100 MW, aiming for 500 MW), North East at Blyth and Cobalt Park, North and South Wales, and Lanarkshire. Over 200 local bids are under review. Reported, 2026 [T4B-S17]
- Blackstone committed £10 billion to Blyth, and QTS Cambois is due in 2028. Nscale Loughton is 50 MW, scalable to 90 MW, with 23,040 GB300 GPUs from Q1 2027. Reported, 2026 [T4B-S17]
</group>

<group name="T4Bd. Programmes in November 2026, GPUs, landlords and rents">
- Abilene had 618 MW operating on 10 September 2026. Epoch thinks the last two buildings were live by 1 November, but Oracle has not confirmed it. Estimate, November 2026 [T4B-S18]
- Shackelford County, Texas, has five shells roofed and finishes in Q4 2028. Saline Township, Michigan, is projected at 1.4 GW for Q4 2028. Doña Ana, New Mexico, is projected at 2.2 GW. Estimate, 2026 [T4B-S18]
- Lordstown, Ohio, has a ban on future data centres and no completion date. Milam County, Texas, is under construction. Michigan faces local opposition. Estimate, 2026 [T4B-S18]
- Meta said in July 2026 it will commit more than $50 billion to Hyperion, growing to 5 GW. Blue Owl owns 80 per cent of the joint venture and Meta 20 per cent. Reported, July 2026 [T4B-S19]
- Bloomberg's estimate puts Hyperion above $250 billion once chips are included. Meta has not confirmed it. Entergy has approval for three gas combined-cycle units due 2028 or 2029. Estimate, 2026 [T4B-S19]
- Microsoft says Atlanta Fairwater began operating in October 2025. Epoch estimates 769,000 H100-equivalents there and does not know the GPU count. Wisconsin is called operational, with most of nine buildings unfinished. Estimate, 2026 [T4B-S20]
- Anthropic's Amazon deal covers up to 5 GW, with nearly 1 GW of Trainium2 and Trainium3 online by end 2026. Over 1 million Trainium2 chips run Project Rainier. Reported, 2026 [T4B-S21]
- Anthropic announced $50 billion for its own sites with Fluidstack in Texas and New York in November 2025. Sites come online through 2026, but locations and power were not disclosed. Reported, 2025 old source [T4B-S21]
- Musk reported about 550,000 GB200 and GB300 GPUs at Colossus 2, with 1.21 million targeted by year end. Epoch has 946 MW and 1,112,000 H100-equivalents. Reported by Musk, 2026 [T4B-S22]
- Dividing Epoch's 946 MW by 550,000 GPUs gives about 1.7 kW for each GPU, all-in. This is the search tool's own arithmetic and the GPU count is unverified. Estimate (derived), 2026 [T4B-S22]
- ABI Research lists US colocation by active IT capacity: Equinix 995 MW, QTS 811 MW, Digital Realty 686 MW and CyrusOne 674 MW. Vantage is 314 MW. Estimate, 2025 [T4B-S23]
- CBRE says Frankfurt providers charge up to 225 euros for each kW each month, and London up to 170 pounds, for 250 to 500 kW. That is about $225 in London. Reported, 22 June 2026 [T4B-S24]
- JLL says Frankfurt vacancy is 3.1 per cent and Amsterdam about 6.5 per cent. Rents rose 7.4 per cent in London, 8.0 per cent in Paris and 7.2 per cent in Dublin. Reported, 2026 [T4B-S24]
- JLL says prime powered land in FLAP-D markets rose about 82 per cent since 2021, to about 2.26 million euros for each MW. Reported, 2026 [T4B-S25]
</group>

<builder_notes>
- Power is the gate, not land. Teams ask how many MW can be energised, and by what date, before they pick a site. (not searched)
- Liquid cooling is mandatory above roughly 40 kW a rack. GB200 racks at 120 kW or more force direct-to-chip loops, and failures have come from the cooling controls.
- A storm that took out a building management system shut a chilled-water loop at a Nebius site in August 2026. Control systems are a single point of failure.
- Training can sit in remote, power-rich places because it needs throughput, not low delay. Inference needs regional sites near users.
- Behind-the-meter turbines get power faster than the grid, but they bring air permits, noise and litigation. xAI faces a lawsuit.
- Small turbines and engines are used as a bridge because large frame turbines are sold out to 2031.
- PUE only counts overheads. It ignores the chips' efficiency and the electricity source, so it cannot compare two sites on cost per token. (not searched)
- Tier ratings measure the building. AI training jobs also depend on network and software, so a job can fail while the building stays up. (not searched)
- Rack power density drives the electrical design: busways, higher voltage distribution, and battery buffers for load swings. (not searched)
- Reference chain for plain-words teaching: grid, substation, transformers, switchgear, UPS and generators, cooling loop, data hall, rack. Power gets cut at every step, so each step needs a spare unit.
- Behind-the-meter gas costs more per MWh than the grid, but it arrives sooner. Modo estimates the premium at 2 to 6 per cent of compute revenue.
- Aeroderivative turbines burn over 40 per cent more fuel than combined-cycle plants, but they are quicker to get.
</builder_notes>

<investor_notes>
- Build cost without chips is about $9 million to $23 million for each MW. With chips it is about $30 million to $55 million. Chips are the largest line, so the building is a minority of the bill.
- Disagreement on cost: Epoch's modelled site costs are far above company pledges. Microsoft says $7 billion for Wisconsin and Epoch says $14 billion today. Scopes differ.
- Colocation looks strong. Vacancy of 1.4 per cent and rents near $196 for each kW each month support developer yields of 10 per cent or more.
- The bear case on leasing is that tenants are a few concentrated AI labs. Stargate showed that financing talks and weather can stall an expansion.
- Power demand forecasts differ by a factor of two. The IEA says about 3 per cent of world electricity in 2030. Berkeley Lab and EPRI say 9 to 17 per cent of United States electricity.
- The binding constraints are turbines (sold to 2031), transformers (over 3 years) and grid queues. Owners of energised sites hold scarce assets.
- Prices differ by region. United States industry pays about 8.6 cents for each kWh, the United Kingdom about 17 pence, and the EU about 18 euro cents. The United Kingdom offers AI Growth Zone discounts to offset this.
- Power's share of annual cost is small next to depreciation on chips. Epoch's $0.9 billion yearly running cost on $38 billion of capex is the cross-check. Speed to power matters more than price.
- Nuclear deals give long-term supply but little near-term power. Prices are mostly undisclosed, and the Three Mile Island figure is unconfirmed.
- Chips and servers are about 60 to 66 per cent of the bill and electricity about 12 per cent of annual cost on a rough check. Cheap power does not fix a slow grid link.
- Nuclear PPA prices stay private. Analyst guesses range from $70 to $100 per MWh, so quote them as estimates only.
- UK industry pays about 23 US cents for each kWh against about 8.6 cents in the US. The AI Growth Zone discount only partly closes this gap.
</investor_notes>
</topic>

<topic key="T5" name="Compute markets, depreciation and finance">
<group name="T5a. GPU rental prices, October to November 2026">
- Ornn's H100 SXM compute price index stood at $3.03 for each GPU-hour on 23 November 2026, with a 30-day range of $2.78 to $3.53. Estimate, 23 November 2026 [T5-S1]
- Silicon Data's H100 rental index (Bloomberg ticker SDH100RT, neocloud tier) showed about $3.10 on 24 November 2026, but another page of the same site showed $2.53. Uncertain, November 2026 [T5-S2]
- The gpurentalprices.com index put the typical on-demand H100 at $3.51 for each GPU-hour for November 2026 to date. Estimate, November 2026 [T5-S3]
- The gpueconomy.com index gave a median public on-demand H100 SXM rate of $3.29 for each GPU-hour in the week of 16 November 2026, across 35 providers. Estimate [T5-S4]
- Compute Census gave a median on-demand H100 of $3.90 for each GPU-hour on 6 November 2026, and a 12-month reserved H100 rate of $3.26. Estimate [T5-S5]
- AWS cut P5 (H100) on-demand prices by about 44 per cent in June 2025, to $55.04 an hour for 8 GPUs, or $6.88 for each GPU-hour. Reported, June 2025, old source [T5-S6]
- AWS raised EC2 Capacity Block prices by about 15 per cent in January 2026 and again around July 2026. One tracker puts P5 at $5.19 and P5e (H200) at $5.97 for each GPU-hour. Uncertain [T5-S6]
- Azure ND H100 v5 lists at $98.32 an hour for 8 GPUs, or $12.29 for each GPU-hour on demand. One source gives reserved rates of about $63.40 (1 year) and $43.79 (3 years) an hour. Estimate [T5-S7]
- Google Cloud A3 H100 on-demand estimates run from $3.00 to $11.06 for each GPU-hour depending on region and source. The first-pass figure of $11.06 is one point in that range. Uncertain [T5-S7]
- Google Cloud A4 (B200) is quoted at $4.28 or $16.11 for each GPU-hour by two sources, and Azure has no standalone B200 VM, only ND GB200 v6. Uncertain [T5-S7]
- CoreWeave lists an 8-GPU H100 instance at $49.24 an hour on demand, which is $6.16 for each GPU-hour. Estimate, 2026 [T5-S8]
- Lambda raised its 8-GPU on-demand prices between 2 and 9 November 2026, with H100 going from $3.99 to $4.59 and B200 from $6.69 to $7.69 for each GPU-hour. Estimate [T5-S9]
- Lambda moved its 1-Click Cluster HGX B200 tiers from self-serve to a "talk to sales" contact in July 2026. Estimate [T5-S9]
- RunPod lists an H100 PCIe at $2.89 an hour on Secure Cloud and from $1.99 on Community Cloud. Estimate, 2026 [T5-S10]
- RunPod B200 on Secure Cloud was quoted at $5.89, $6.79 and $7.99 an hour by different sources in 2026, a rise of about 31 per cent from January to August. Uncertain [T5-S10]
- Vast.ai H100 SXM marketplace rates run from $1.49 to $2.21 an hour, and its B200 community rate is $6.25 to $7.50. Estimate, October 2026 [T5-S10]
- No cloud has published a per-hour price for Nvidia Vera Rubin NVL72. CoreWeave brought up the first cluster on 1 June 2026, and Cognition is its first customer. Reported, 2026 [T5-S11]
</group>

<group name="T5b. H100 price history and the reason for the direction">
- SemiAnalysis's one-year-contract H100 index bottomed at $1.70 an hour in October 2025, then rose to $2.35 by March 2026. Estimate [T5-S12]
- AIMultiple's median H100 rental price fell from over $7 an hour in early 2024 to about $3.38 in August 2026. Estimate [T5-S12]
- Silicon Data's index reached $3.11 in November 2026, up nearly 60 per cent from its low, while a June 2026 source showed on-demand H100 at $2.01 to $2.53. Estimate [T5-S12]
- Bank of America reportedly tracked H100 spot prices up 33 per cent over the year to August 2026. Estimate, press report [T5-S12]
- The press and SemiAnalysis link the 2026 rise to reasoning and agent workloads that raised inference demand while Nvidia no longer makes H100 chips. Estimate [T5-S12]
- Different indices measure different things (neocloud, hyperscaler, one-year contract, spot), so levels from 2023 to 2026 should not be joined into one line. Estimate [T5-S2]
</group>

<group name="T5c. Capital spending of the large companies">
- Alphabet guides 2026 capital spending at $195 billion to $205 billion, set in July 2026 and kept at the Q3 report on 28 October 2026. Q3 spending was $51.4 billion. Reported [T5-S13]
- Alphabet says 2027 capital spending will "increase significantly" but gives no figure. A $300 billion claim from one site is unverified. Reported, 28 October 2026 [T5-S13]
- Microsoft spent $145.3 billion including finance leases in the year to June 2026, and $41 billion in the June 2026 quarter. Estimate from analyst summary, August 2026 [T5-S14]
- Microsoft spent $45.2 billion including finance leases in the quarter to 30 September 2026, below its guide of about $50 billion, with $7.4 billion of finance leases. Reported by press, October 2026 [T5-S15]
- Amazon kept its 2026 cash capital spending estimate at about $220 billion on 29 October 2026, with Q3 spending of $77.3 billion. Reported [T5-S16]
- Amazon says 2027 spending will be higher, with no figure. AWS backlog was $578 billion and AWS grew 39 per cent in Q3 2026. Reported [T5-S16]
- Meta guides 2026 capital spending, including finance lease principal, at $135 billion to $145 billion, narrowed on 21 October 2026. Q3 spending was $34.91 billion. Reported [T5-S17]
- Meta gave no 2027 capital spending figure, and its Q3 capital spending exceeded operating cash flow of $32.79 billion. Reported, 21 October 2026 [T5-S17]
- Oracle spent $55.7 billion in the year to 31 May 2026, against $21.2 billion a year earlier. Reported, June 2026 [T5-S18]
- Oracle guides fiscal 2027 (to May 2027) at about $70 billion net cash outlay, or up to $95 billion before $20 billion to $25 billion of customer funding. Reported, June 2026 [T5-S18]
</group>

<group name="T5d. GPU clouds, Oracle backlog and finance">
- CoreWeave reported Q3 2026 revenue of $3.661 billion, up 168 per cent, and backlog of $132.5 billion on 10 November 2026. Reported [T5-S19]
- CoreWeave guides 2026 revenue at $13.0 billion to $13.3 billion and capital spending at $37 billion to $39 billion. Q3 net loss was $709 million. Reported [T5-S19]
- CoreWeave's debt was almost $47 billion at 30 September 2026. Its interest rates were not found. Reported by press [T5-S19]
- Nebius reported Q3 2026 revenue of $980.8 million on 12 November 2026, including about $325 million of one-off partner-funded revenue. Reported [T5-S20]
- Nebius raised 2026 capital spending guidance to about $27 billion and guides 2027 revenue to $12 billion to $13 billion and capital spending to $40 billion to $45 billion. Reported [T5-S20]
- Nebius expects customer prepayments and financing against contracts to cover 75 to 85 per cent of its 2027 capital spending. Reported, 12 November 2026 [T5-S20]
- Oracle reported remaining performance obligations of $664 billion on 10 September 2026, and sold $20 billion of stock through an at-the-market programme. Reported [T5-S21]
- Oracle plans to raise about $40 billion of debt and equity in fiscal 2027, after negative free cash flow of $23.7 billion in fiscal 2026. Reported, June 2026 [T5-S18]
</group>

<group name="T5e. Depreciation and utilisation">
- Microsoft extended server life from 4 to 6 years in 2022, and from fiscal 2027 extends data centre and office building life from 15 to 25 years. Reported [T5-S23]
- Meta extended server life to 5.5 years from 4 to 5 years, cutting 2025 depreciation by $2.9 billion. Reported, January 2025, old source [T5-S23]
- Amazon cut server life from 6 to 5 years, lowering operating income by about $700 million. Reported, old source [T5-S23]
- Amazon, Alphabet, Microsoft and Meta booked $44.5 billion of depreciation in April to June 2026, nearly one third of operating profit. Estimate, August 2026 [T5-S23]
- Michael Burry argues that life is overstated and puts the understated depreciation at about $176 billion for 2026 to 2028, with a real life of 2 to 3 years. Estimate [T5-S24]
- The other side says 4 to 6 years is fair. Nvidia and CoreWeave defend it, and November 2026 rental data with rising H100 rents and full use cut against Burry. Estimate [T5-S24]
- Cast AI found average GPU utilisation of 5 per cent across 23,000 Kubernetes clusters on AWS, Azure and Google Cloud. This covers company clusters, not GPU clouds. Estimate, 2026 [T5-S25]
- McKinsey says bare-metal GPU cloud returns flatline if utilisation slips below 80 per cent. Estimate [T5-S26]
</group>

<group name="T5Ba. Finance of the build: debt, leases and off-balance-sheet vehicles">
- CoreWeave closed a $2.6 billion DDTL 3.0 loan in July 2025, priced at SOFR plus 4.00 per cent, with maturity in August 2030. Reported by company, secondary rate detail [T5B-S1]
- CoreWeave closed an $8.5 billion DDTL 4.0 facility on 30 March 2026, its first investment-grade rated GPU-backed deal. A floating tranche pays SOFR plus 2.25 per cent and a fixed tranche about 5.9 per cent. Reported, rates secondary [T5B-S1]
- CoreWeave closed a $3.1 billion DDTL 5.0 loan in May 2026 at SOFR plus 4.50 per cent, and a $2.6 billion DDTL 5.5 loan in August 2026 at SOFR plus 5.50 per cent. Reported, rates secondary [T5B-S1]
- A press report says CoreWeave priced $2.75 billion of 9.75 per cent senior unsecured notes due 2031 and $3.5 billion of 1.75 per cent convertible notes due 2032 in April 2026. Estimate, single report [T5B-S1]
- Axis Intelligence says a CoreWeave GPU loan tied to a non-investment-grade customer costs 225 basis points more over SOFR than one tied to an investment-grade customer. Estimate [T5B-S2]
- Nebius took a first GPU-backed loan of $775 million at SOFR plus 2.50 per cent, maturing 2030, and a $3.5 billion Citi loan facility that runs for 364 days. Estimate, trade press 2026 [T5B-S2]
- Nebius raised convertible notes in 2026. Reports give $4.0 billion, $4.5 billion and $5.75 billion, with coupons of 0 to 0.5 per cent (2030 notes) and 4 to 4.5 per cent (2034 notes). Uncertain [T5B-S2]
- Lambda closed a $926 million senior secured term loan B backing GPUs leased to an investment-grade customer, rated Baa2 by Moody's, on 22 September 2026. A tracker lists it at SOFR plus 3.00 per cent. Reported, rate secondary [T5B-S2]
- Lambda also raised about $1 billion of short-dated private debt, arranged by JPMorgan, to buy GPUs that Microsoft will lease. Estimate, TNW 28 August 2026 [T5B-S2]
- IREN's $3.6 billion Microsoft GPU financing, a mix of notes and a delayed draw term loan, is listed at 6.0 per cent by one tracker. Uncertain [T5B-S2]
- For Crusoe, only a $7.1 billion construction loan for the Abilene joint venture with Blue Owl and Primary Digital was found. No rate was found. Uncertain [T5B-S2]
- Meta's Hyperion vehicle (Beignet Investor) sold $27.3 billion of senior secured bonds in October 2025, priced at par with a 6.581 per cent coupon and due May 2049. S&P rated them A+. Reported by press [T5B-S3]
- Meta leases the Hyperion site and the debt sits off Meta's balance sheet. Estimate, October 2025, old source [T5B-S3]
- A later Finimize report says the Beignet 2049 notes traded near 91 cents on the dollar. The date and market source are not verified. Uncertain [T5B-S3]
- JPMorgan and MUFG led $38 billion of construction loans for Vantage sites leased to Oracle, with $23.25 billion in Texas and $14.75 billion in Wisconsin. Oracle is the tenant, not the borrower. Reported by Bloomberg, autumn 2025, old source [T5B-S4]
- Oracle sold $18 billion of investment-grade bonds in September 2025 and a record-demand $25 billion bond in February 2026. It rates Baa2 and BBB. Reported by press [T5B-S4]
</group>

<group name="T5Bb. Suppliers investing in customers">
- Nvidia committed up to $10 billion to Anthropic and Microsoft up to $5 billion, announced 18 November 2025. Anthropic agreed to buy $30 billion of Azure compute. Reported by press [T5B-S5]
- Nvidia's September 2025 letter of intent for up to $100 billion in OpenAI, paid in $10 billion steps, was replaced by a $30 billion direct equity investment in February 2026. Reported by press [T5B-S6]
- The $30 billion sits inside the OpenAI round that closed at $122 billion on 31 March 2026, with SoftBank and Amazon also investing. Reported, March 2026 [T5B-S6]
- Nvidia has committed more than $40 billion to AI equity stakes in the first four months of 2026, per CNBC from filings. Estimate [T5B-S6]
- Nvidia joined xAI's $6 billion round in late 2024 and was reported to plan up to $2 billion in a $20 billion round. Estimate, January 2025, old source [T5B-S5]
- Nvidia invested $100 million in CoreWeave in 2023 and held about 47.2 million shares, worth about $3.66 billion and 11 per cent, in a later 13F. Estimate [T5B-S5]
- Amazon agreed in April 2026 to invest up to $25 billion more in Anthropic, with $5 billion at once, after $8 billion earlier. Anthropic pledged $100 billion of AWS spending over 10 years. Reported by press [T5B-S7]
- AMD gave OpenAI a warrant for up to 160 million AMD shares at $0.01 each, vesting with milestones, in a 6 GW deal announced 6 October 2025. The first 1 GW starts in 2H 2026. Reported [T5B-S8]
</group>

<group name="T5Bc. Capex versus AI revenue, and the 2025 actuals">
- Sequoia's David Cahn put the annual AI revenue needed at about $600 billion in mid-2024, against about $50 billion to $100 billion earned. He first flagged a $125 billion gap in September 2023. Estimate, old source [T5B-S9]
- Bain's September 2025 report says AI firms need $2 trillion of yearly revenue by 2030, and would fall $800 billion short. Estimate, old source [T5B-S9]
- A 2026 Bain report raises the need to about $6 trillion a year by 2031. It assumes capex is 25 per cent of revenue. BCG's bottom-up figure is about $2.6 trillion a year by 2030. Estimate [T5B-S9]
- Alphabet's 2025 capex was $91.45 billion and Meta's was $72.22 billion. Reported by press from results [T5B-S10]
- Amazon spent about $131 billion on capex in 2025. Operating cash flow was $139.5 billion. Reported, February 2026 [T5B-S10]
- Microsoft reports on a June fiscal year, so a calendar 2025 figure was not found. Fiscal 2025 capex was $88.7 billion. Reported, old source [T5B-S10]
- Reports give Microsoft capital spending for calendar 2026 at about $170 billion to $190 billion, and the sources do not agree. One report says $175 billion, cut from $190 billion after an accounting change. Uncertain, October 2026 [T5B-S11]
</group>

<group name="T5Bd. Unit KPIs, depreciation lives, price index method, capacity, owners">
- Counterpoint asks if annualised revenue for each MW across the CoreWeave fleet reaches $10 million to $12 million. Estimate [T5B-S12]
- CoreWeave's adjusted operating income was $21 million on $2.1 billion of revenue in Q1 2026. A Q2 2026 summary cites a 5 per cent margin. Uncertain [T5B-S12]
- IREN's Microsoft deal is worth $9.7 billion over about 5 years, with 20 per cent prepaid and $1.9 billion of expected ARR. Reported, company release [T5B-S13]
- IREN prices new 3-year contracts above $20 million per IT-MW, and a 5-year deal at about $22 million with 90 per cent of GPU capex prepaid. IREN ARR is GPU price times 8,760 hours, not GAAP revenue. Reported [T5B-S13]
- Nebius moved server life from 4 to 5 years from Q1 2026 and reported a payback of 22 months on Q2 2026 deals. Estimate, secondary reading of the Q2 letter [T5B-S14]
- On a 4-year life Nebius Q2 2026 depreciation would be about $325 million, and the operating loss $241 million rather than $176 million. Estimate [T5B-S14]
- Hyperscaler life for servers is 6 years at the big three clouds (one source), 6 years at CoreWeave, and 5.5 years at Meta from 29 January 2025. Estimate [T5B-S15]
- SemiAnalysis's H100 composite index reads $6.62 (2H 2023), $5.78 (1Q 2024), $4.77 (2Q 2024), $4.44 (3Q 2024) and $3.91 (4Q 2024) for each GPU-hour. Estimate, index table [T5B-S16]
- The SemiAnalysis composite is hourly, in dollars for each GPU-hour. It blends scraped market prices with contract survey data where the survey exists, now only for H100. Reported by SemiAnalysis [T5B-S16]
- SemiAnalysis said in 2026 that capacity coming online until August to September 2026 was already booked, and some neoclouds no longer sell single nodes. Estimate [T5B-S17]
- One April 2026 analysis puts B200 and H200 lead times at 36 to 52 weeks, from HBM and CoWoS limits. Uncertain, repost of other reports [T5B-S17]
- Epoch AI credits Google with about 5 million H100-equivalents, roughly 25 per cent of a world total near 16 million. Epoch credits leased compute to the cloud owner, not the lab. Estimate [T5B-S18]
- Epoch estimates OpenAI used 10 to 15 per cent of world operational AI compute at the end of 2025, about 1.7 million H100-equivalents. Estimate [T5B-S18]
</group>

<builder_notes>
- Three contract types exist. On demand is pay per hour with no commitment, reserved is a 1 to 3 year price cut for a commitment, and spot or marketplace capacity is cheapest but can be taken away. (not searched)
- Use on demand for experiments and bursts, reserved for steady training or serving, and spot for fault-tolerant jobs with frequent checkpoints. (not searched)
- A hyperscaler H100 list price is two to four times a marketplace price, but you pay for integration, quotas, identity and network. (not searched)
- AWS Capacity Blocks sell a fixed block of GPUs for a fixed window, and their price moved up twice in 2026. Plan for price changes between quote and launch.
- Lambda closed self-serve ordering for 16 GPU and larger B200 clusters in July 2026, so large clusters now need a sales call.
- Bare metal gives full hardware control and no virtualisation tax but you run the node health and drivers. A VM is easier but loses some network speed. Managed services (Slurm or Kubernetes) cost more and save operator time. (not searched)
- Marketplace hosts such as Vast.ai vary in reliability, so test with a short job before a long run, and expect interruptions.
- Wait times and minimum sizes in late 2026 were not found. Rising prices and sales-gated clusters suggest tight capacity for Blackwell.
- Per-hour price is not the only cost. Egress, storage and idle time often decide the real cost of a run. (not searched)
- A DDTL (delayed draw term loan) lets a GPU cloud draw cash as each cluster ships, and the contract with the customer backs the loan. Loan price tracks the customer's credit.
- Epoch attributes rented chips to the cloud, so any "who owns the GPUs" chart hides how much a lab truly uses.
- IREN ARR counts commissioned GPUs only, times 8,760 hours. Read any ARR or revenue-per-MW figure with its definition.
</builder_notes>

<investor_notes>
- Rising H100 rents in 2026 support the bulls. Old chips still earn money, which supports a 5 to 6 year life. Burry's side says Blackwell and Rubin will cut rents again.
- Depreciation is large and rising, at $44.5 billion a quarter for four hyperscalers. A shorter life would cut reported profit a lot, while cash flows would not change.
- Capital spending now exceeds operating cash flow at Meta and Oracle, and Alphabet and Amazon show negative free cash flow in some periods. Funding comes from debt, equity and customer prepayments.
- Backlogs are large (Oracle $664 billion, AWS $578 billion, CoreWeave $132.5 billion). The risk is that a few customers, mainly AI labs, stand behind most of it.
- Circular deals matter. Nvidia's $100 billion OpenAI plan was non-binding, so headline sums overstate firm commitments.
- GPU clouds depend on high utilisation (above 80 per cent by one estimate) and cheap debt. CoreWeave debt of about $47 billion against 2026 revenue of about $13 billion shows the leverage.
- Delays can hit revenue as well as cost. Nebius cut its 2026 outlook on capacity delays and Microsoft's spending fell short on late third-party deliveries.
- Price indices disagree by up to 8 times in level, so any thesis should name the index and the date.
- Cost of debt ranges from SOFR plus 2.25 per cent (investment-grade customer) to a 9.75 per cent unsecured note at CoreWeave. The customer's credit sets the price, not the GPU.
- The Hyperion structure keeps $27.3 billion off Meta's balance sheet, but Meta's lease backs it. Bears call this hidden leverage and bulls call it ordinary project finance.
- Gap estimates run from Sequoia's $600 billion (2024) to Bain's $800 billion shortfall (2030) and a $6 trillion need (2031). They depend on a top-down capex ratio of 25 per cent, which BCG and others dispute.
- Vendor financing is widespread: Nvidia, Amazon, Microsoft and AMD all pay or fund customers who then buy their products. Headline sums mix firm equity and milestone money.
</investor_notes>
</topic>

<topic key="T6" name="Model companies">
<group name="T6a. Anthropic: IPO filing figures and listing">
- Anthropic revenue for the three months to 30 September 2026 was $16,956 million, about $17.0 billion and about 47 per cent above the second quarter. Estimate, 5 November 2026 [T6-S1]
- Anthropic had a $567 million operating loss in quarter 3 of 2026, after a $974 million operating profit in quarter 2. Estimate, 5 November 2026 [T6-S1]
- The swing to a loss came mainly from about $5.0 billion of compute under short-term commitments and $2.0 billion of non-cash donation-matching charges. Estimate, November 2026 [T6-S1]
- Anthropic revenue for the nine months to 30 September 2026 was about $33.2 billion. Estimate, 5 November 2026 [T6-S1]
- Anthropic net loss was about $23.3 billion in quarter 3 and about $104 billion in nine months. Most of it is a non-cash fair-value change on convertible instruments, about $94.3 billion. Estimate, November 2026 [T6-S1]
- Anthropic run-rate revenue was about $81 billion on 31 October 2026, up $10 billion from 30 September, in the second amendment to the S-1 filed 10 November 2026. Reported, 11 November 2026 [T6-S2]
- The filing says run-rate is an annualised snapshot and not a forecast. Earlier press run-rates were $30 billion (April 2026) and above $65 billion (end of July 2026). Estimate, November 2026 [T6-S2]
- Anthropic cost of revenue was about $2.38 billion in the first half of 2026 on about $16.3 billion of revenue, an implied gross margin of about 85 per cent. Estimate, 30 October 2026 [T6-S3]
- Analysts argue the 85 per cent margin is too high, because cloud partner fees and free-tier compute sit below gross profit. Their loaded margin is about 60 to 65 per cent. Estimate, November 2026 [T6-S3]
- Anthropic operating cash flow was positive $6,569 million in the nine months to 30 September 2026, against an outflow of $2,024 million a year earlier. Estimate, November 2026 [T6-S4]
- Anthropic bought $925 million of property and made $1,955 million of lease prepayments in nine months. Cash was $96 billion with $36 billion of short-term investments at 30 September 2026. Estimate, November 2026 [T6-S4]
- Anthropic purchase commitments were $265.6 billion at 30 June 2026, plus $321.4 billion of leases not yet started. Estimate, November 2026 [T6-S3]
- Consumption-based fees made up about 75 to 80 per cent of Anthropic revenue in 2026, and subscriptions the rest. Estimate, October 2026 [T6-S5]
- Customers outside the top five gave about 79 per cent of revenue in quarter 3 of 2026, up from about 64 per cent in quarter 1. Estimate, November 2026 [T6-S5]
- Anthropic had more than 11,900 customers above $100,000 a year, more than 1,900 above $1 million, and about 250 above $10 million. Estimate, November 2026 [T6-S5]
- Anthropic marketed 825 million shares at $70 to $78 and sought a $26 billion private placement. Targets were $1 trillion to $1.4 trillion valuation. Estimate, 10 November 2026 [T6-S6]
- Anthropic priced its IPO at $83 a share on 18 November 2026, above the range, and began trading on Nasdaq as ANT on 19 November 2026. Estimate, 19 November 2026 [T6-S7]
- Anthropic sold 980 million shares and raised about $81.3 billion, which reports call the largest IPO on record. The IPO price valued the company at about $1.5 trillion. Estimate, 19 November 2026 [T6-S20]
- ANT opened at $111.50 on 19 November 2026. Most outlets give a close of $97.17, up 17 per cent. One gives $95.05. Uncertain, 19 November 2026 [T6-S7]
</group>

<group name="T6b. OpenAI and other model companies">
- OpenAI told investors its run-rate revenue was about $50 billion at the end of September 2026, about $20 billion below investor hopes. Estimate, November 2026 [T6-S8]
- Axios reported OpenAI annual recurring revenue near $70 billion on 29 September 2026, with a $70 billion year-end target. The two figures use different definitions. Uncertain, 29 September 2026 [T6-S9]
- OpenAI had about $10 billion revenue in quarter 3 of 2026, up about 50 per cent on quarter 2, and an adjusted operating loss of $10.9 billion. Estimate, 11 November 2026 [T6-S10]
- OpenAI quarter 2 2026 adjusted operating loss was $10.1 billion in most reports. One tracker says $12.3 billion. Uncertain, November 2026 [T6-S10]
- OpenAI had $5.7 billion revenue in quarter 1 of 2026, a gross margin of about 39 per cent and cash burn of $3.7 billion. Estimate, 2026 [T6-S11]
- Another report gives OpenAI an adjusted gross margin of about 33 per cent against an internal target of 46 per cent. Uncertain, 2026 [T6-S11]
- The Financial Times reported OpenAI projects negative free cash flow of $278 billion from 2026 to 2030 and about $856 billion of compute and infrastructure spending. Estimate, 18 September 2026 [T6-S11]
- OpenAI closed a $122 billion round at an $852 billion post-money valuation, anchored by Amazon, Nvidia and SoftBank. Reported, 31 March 2026 [T6-S12]
- Amazon committed $50 billion, but $35 billion depends on conditions. SoftBank and Nvidia committed $30 billion each. Reported, 27 February 2026 [T6-S12]
- ChatGPT reached 900 million weekly active users in February 2026, with more than 5 per cent paying. Reported, 27 February 2026 [T6-S13]
- One secondary source gives 1.2 billion ChatGPT weekly users in November 2026. Enterprise became OpenAI's largest revenue source in quarter 3 of 2026. Uncertain, November 2026 [T6-S13] [T6-S10]
- OpenAI compute deals reached about $1 to $1.15 trillion for 2025 to 2035 by one analyst's tally, with Broadcom, Oracle and Microsoft largest. Estimate, November 2025, old source [T6-S14]
- xAI lost about $6.4 billion on $3.2 billion revenue in 2025, per the SpaceX IPO filing. Q1 2026 revenue was $818 million with a $2.47 billion operating loss. Reported, May 2026 [T6-S15]
- Grok had about 117 million monthly users and 1.9 million paying users. Estimate, 2026 [T6-S15]
- Alphabet said the Gemini app passed 1 billion monthly users on 28 October 2026. Reported, 28 October 2026 [T6-S16]
</group>

<group name="T6c. Compute split, training cost and market share">
- A chart built from the S-1/A puts about 26 per cent of Anthropic compute on paying customers and 74 per cent on training, research, internal use and free users. Estimate, November 2026 [T6-S17]
- The 26 per cent is an upper bound. The filing itself does not split compute between training and serving. Estimate, November 2026 [T6-S17]
- Anthropic compute and infrastructure expense was about $8.9 billion in the first half of 2026, of which about $2.4 billion sits in cost of revenue. Estimate, November 2026 [T6-S17]
- Anthropic compute fell from 251 per cent of revenue in quarter 1 of 2025 to 48 per cent in quarter 2 of 2026. Estimate, November 2026 [T6-S17]
- The Epoch AI dashboard says the cost of frontier training runs grew about 3.5 times a year. An older Epoch paper projected runs above $1 billion by 2027. Estimate, February 2026 [T6-S18] [T13-S19]
- Epoch AI says final runs are a minority of research compute spend, so full development costs far more than the final run. Estimate, 23 March 2026 [T6-S18]
- Menlo Ventures puts enterprise API spend shares at Anthropic 55 per cent, OpenAI 31 per cent and Google 9 per cent in 2026. Estimate, 3 November 2026 [T6-S19]
- Anthropic and OpenAI hold 86 per cent of enterprise API spend. The survey covers about 400 US decision-makers and Menlo invests in Anthropic. Estimate, 3 November 2026 [T6-S19]
- Menlo Ventures says the top three labs take 69 per cent of 2026 enterprise AI spend. Estimate, 3 November 2026 [T6-S19]
</group>

<group name="T6Ba. Anthropic filing conflicts and funding">
- The Anthropic S-1/A shows a nine-month operating loss of about $1.26 billion on revenue of $33.242 billion. Estimate (press summaries of the filing), November 2026 [T6B-S1]
- Anthropic compute expense rose $14.4 billion, or 329 per cent, in nine months. That implies about $18.8 billion, my own sum from the two figures. Estimate, November 2026 [T6B-S1]
- Anthropic discloses purchase commitments and leases of about $895.4 billion, substantially all for compute and infrastructure. About $69.8 billion falls due within 12 months of 30 September 2026. Estimate, November 2026 [T6B-S1]
- The contractual obligations table alone totals $319.993 billion. The rest ties to agreements with no fixed dollar amount or signed after 30 September 2026. Estimate, November 2026 [T6B-S1]
- Anthropic raised $65 billion in its Series H at a $965 billion post-money valuation, announced 28 May 2026. Reported, 28 May 2026 [T6B-S2]
- Series H leads were Altimeter, Dragoneer, Greenoaks and Sequoia. About $15 billion was earlier hyperscaler money, including $5 billion from Amazon. Reported, 28 May 2026 [T6B-S2]
- Anthropic raised $30 billion in its Series G at a $380 billion post-money valuation, led by GIC and Coatue. Microsoft and Nvidia money was included. Reported, February 2026 [T6B-S2]
- Anthropic compute deals include up to 5 gigawatts with Amazon, 5 gigawatts of TPU capacity with Google and Broadcom, and GPU capacity with SpaceX at Colossus 1 and 2. Reported, 2026 [T6B-S2]
- A lifetime total raised by Anthropic was not stated in any source. Run-rate revenue passed $47 billion in May 2026 at the time of Series H. Reported, May 2026 [T6B-S2]
</group>

<group name="T6Bb. Other labs: funding, revenue, valuation">
- OpenAI president Greg Brockman testified on 5 May 2026 that OpenAI expects to spend $50 billion on compute in 2026. It is a projection, not an actual. Reported (court testimony), 5 May 2026 [T6B-S3]
- OpenAI targets about $600 billion of total compute spending through 2030, per a Reuters source in February 2026. Estimate, February 2026 [T6B-S3]
- xAI raised a $20 billion Series E in January 2026 with Nvidia and Cisco, at about $230 billion. SpaceX then bought xAI at $250 billion in February 2026. Reported, January 2026 [T6B-S4]
- Total xAI funding raised is disputed: Sacra says $22.1 billion, Clay over $38 billion, CB Insights $49.9 billion. Uncertain, 2026 [T6B-S4]
- Mistral raised €3 billion at a post-money valuation above €21 billion (about $24 billion), led by Samsung, on 8 September 2026. Reported, 8 September 2026 [T6B-S5]
- Mistral's last round before that was a €1.7 billion Series C at €11.7 billion in September 2025. Reported, September 2025, old source [T6B-S5]
- Mistral annual recurring revenue passed $400 million in early 2026. Its CFO told Reuters it is on track for $1 billion by end 2026. Estimate, 2026 [T6B-S5]
- Mistral total funding raised ranges from about $4 billion (Crunchbase) to $6.5 billion including debt (Dealroom). Uncertain, 2026 [T6B-S5]
- Zhipu and MiniMax listed in Hong Kong in January 2026. One estimate puts 2025 revenue at 724 million yuan for Zhipu and $79 million for MiniMax. Estimate, 2026 [T6B-S6]
- Moonshot AI is reported near a $50 billion valuation and preparing a Hong Kong IPO. Sacra estimates $1 billion annualised revenue in August 2026. Estimate, October 2026 [T6B-S6]
- DeepSeek is reported raising capital at up to $71 billion, with Sacra estimating $1 billion annualised revenue in September 2026. Revenue is undisclosed. Uncertain, 2026 [T6B-S6]
- Meta spent $72 billion on capital spending in 2025. Reported, January 2026 [T6B-S7]
- Alibaba says Qwen models passed 3 billion cumulative downloads by August 2026, ahead of Google and Meta. No model revenue found. Reported, 15 August 2026 [T6B-S8]
</group>

<group name="T6Bc. Share, use by task, model life, margins, training cost">
- Similarweb web traffic shares for October 2026 were ChatGPT 55.7 per cent, Gemini 24.2 per cent and Claude 11.5 per cent, up from 9.6 per cent in September. Estimate, 10 November 2026 [T6B-S9]
- Similarweb had ChatGPT at 75.7 per cent in February 2025 and 61.7 per cent in February 2026. Website traffic only, not apps. Estimate, 2026 [T6B-S9]
- Menlo Ventures estimates Claude Code and Codex hold $24.0 billion, or 70 per cent, of a $34.0 billion AI coding market. These are run-rate estimates. Estimate, 2026 [T6B-S10]
- A JetBrains survey in August 2026 found Claude Code used by 39 per cent of developers, Copilot 21 per cent, Codex 16 per cent and Cursor 12 per cent. Estimate, August 2026 [T6B-S10]
- The OpenRouter and a16z study of 100 trillion tokens finds programming grew from 11 per cent to over 50 per cent of token volume. Estimate (via summary), January 2026 [T6B-S11]
- The same study says Claude holds over 60 per cent of programming use on OpenRouter. OpenRouter excludes traffic on native APIs, so it is biased. Estimate, January 2026 [T6B-S11]
- Anthropic's March 2026 Economic Index says coding is moving from Claude.ai to the API, and automation fell sharply in API data. Reported, March 2026 [T6B-S12]
- An analysis puts the average time a frontier model holds the top spot at about 41 days. Secondary source, method not checked. Uncertain, 2026 [T6B-S13]
- Epoch's GPT-5 bundle case: about $6.1 billion revenue, $3.2 billion inference cost, about 48 per cent gross margin, but not enough to repay development. Estimate, 28 January 2026 [T6B-S14]
- Epoch says GPT-5 was the leading model for only about four months. It argues each model repays itself, but the next model's cost erases the surplus. Estimate, 28 January 2026 [T6B-S14]
- Axios reports Anthropic's gross margin swung from minus 94 per cent in 2024 to about plus 40 per cent in 2025. Estimate, March 2026 [T6B-S15]
- Ramp data show 28 per cent of corporate OpenAI chat spending went through personal consumer plans in February 2026. Estimate, March 2026 [T6B-S15]
- Epoch's dashboard lists the largest AI data centre at 1.1 million H100-equivalents, updated 5 February 2026. Its power record doubles about every 10 months. Estimate, February 2026 [T6B-S16]
- Epoch's cost method is hardware amortisation of the final run plus energy. It finds a 2 to 3 times yearly rise. No newer per-model cost found. Estimate, 2024 paper, old source [T6B-S16]
</group>

<builder_notes>
- Cost of revenue covers only serving paying customers. Training, research, free-tier inference and internal use sit in research and development, so reported gross margin depends on where the line is drawn.
- Run-rate is usually one month or week times 12 or 52. It swings with usage-based billing and with the definition, as OpenAI's $50 billion against $70 billion shows.
- A model company turns compute into revenue in steps: a training cluster makes weights, serving clusters host them, an API meters tokens, and products such as coding agents and chat add subscriptions. (not searched)
- Consumption billing means revenue follows customer token use. Heavy agent and coding workloads raise both revenue and serving cost together. (not searched)
- Cloud marketplaces carry a large share of Anthropic sales, so partner fees and capacity limits shape what engineers can ship. (not searched)
- Older models usually stay available after a release but lose use and price power as customers move to the newer model. I found no published data. (not searched)
- Inference gets cheaper per token through better chips, batching, caching and smaller models, but total spend rises because use grows faster. (not searched)
- Cluster size, reliability and failed runs matter in practice. Epoch counts only the final run, so published training cost understates what was spent. (not searched)
- OpenRouter says new versions are adopted fast: Haiku 5.5 took 73 per cent of Haiku traffic in a week, yet Sonnet 4.6 and 5 still drew about 4.5 million requests a day three weeks after Sonnet 5.5. Old models linger.
- OpenRouter argues that in a frontier family, staying on the older model now means paying more for less. This is a switching cost the engineer controls with model aliases and tests.
</builder_notes>

<investor_notes>
- Bull case: Anthropic grew revenue about 47 per cent in one quarter, turned operating cash flow positive at $6.6 billion for nine months, and cut compute from 251 to 48 per cent of revenue.
- Bear case: the 85 per cent gross margin leaves out partner fees and free-tier compute. Loaded margins near 60 to 65 per cent are argued by analysts.
- Bear case: Anthropic commitments reach $265.6 billion to $895.4 billion against $17 billion of quarterly revenue. None has hit the income statement yet.
- Bull case: about 74 per cent of compute goes to training and research, so a slowdown in model spend could lift margin fast. Bear reply: rivals force that spend.
- The $104 billion net loss is mostly non-cash fair-value change on convertible instruments, so the operating loss of $567 million is the better guide.
- OpenAI loses more per dollar of revenue. Its $10.9 billion quarterly adjusted operating loss on $10 billion revenue compares with Anthropic's $567 million loss on $17 billion.
- OpenAI has more users, 900 million weekly in February 2026, but few pay, about 5 per cent. Anthropic leans on usage-based business customers.
- Concentration risk: Menlo shows two labs hold 86 per cent of enterprise API spend, and Menlo invests in Anthropic. Google's share fell from 21 to 9 per cent.
- Valuation: ANT priced at $83 and traded about 17 per cent higher on day one. A $1 trillion plus price needs sustained growth and falling compute intensity.
- Bull number 1: Epoch finds a GPT-5-type model earns about 48 per cent gross margin over its life. Bull number 2: Anthropic nine-month operating cash flow was positive and compute fell as a share of revenue.
- Bear number 1: that same GPT-5 bundle did not repay its own development in a four-month lead. Bear number 2: commitments of $895.4 billion against $33.2 billion of nine-month revenue.
- Bear number 3: OpenAI projects $50 billion of compute in 2026 against an adjusted operating loss of $10.9 billion in one quarter (first report).
- Strong funding is circular in part. Hyperscaler money in Anthropic's $65 billion round ($15 billion) comes back as compute purchases from the same firms.
</investor_notes>
</topic>

<topic key="T7" name="Application infrastructure">
<group name="T7a. Supabase: plans, compute, connections, egress, compliance">
- The Supabase Free plan gives 2 projects, 500 MB of database per project, 50,000 monthly active users, 1 GB of file storage and 5 GB of egress. Reported, 26 November 2026 [T7-S1]
- The Supabase Pro plan costs $25 a month. It includes $10 of compute credit, 8 GB of disk per project, 100,000 monthly active users, 100 GB of storage and 250 GB of egress. Reported, 26 November 2026 [T7-S1]
- The Supabase Team plan costs $599 a month, shown in an official billing example. Team and Enterprise customers can download the SOC 2 Type 2 report. Reported, 26 November 2026 [T7-S2]
- Each Supabase project has its own Postgres server, and the compute is billed by the hour. Micro costs about $10 a month, Small about $15 and Medium about $60. Reported, 26 November 2026 [T7-S3]
- Supabase Large costs about $110 a month (2-core ARM, 8 GB). XL costs about $210 (4 cores, 16 GB). 2XL costs about $410 (8 cores, 32 GB). Reported, 26 November 2026 [T7-S3]
- Supabase 4XL costs about $960 a month (16 cores, 64 GB). 8XL costs about $1,870. 16XL costs about $3,730 (64 cores, 256 GB). Larger sizes need a sales contact. Reported, 26 November 2026 [T7-S3]
- Supabase database connection limits are 60 for Micro, 90 for Small, 120 for Medium, 160 for Large, 240 for XL, 380 for 2XL and 480 for 4XL. Reported, 26 November 2026 [T7-S4]
- Supabase pooler client limits are 200 for Micro, 400 for Small, 600 for Medium, 800 for Large, 1,000 for XL, 1,500 for 2XL and 3,000 for 4XL. Reported, 26 November 2026 [T7-S4]
- A compute upgrade on Supabase usually causes under 2 minutes of downtime, but it can take longer. Reported, 26 November 2026 [T7-S3]
- Supabase charges $0.09 per GB of uncached egress above the quota and $0.03 per GB of cached egress. Egress counts across database, auth, storage and functions. Reported, 26 November 2026 [T7-S5]
- Supabase charges $0.00325 per monthly active user above 100,000 on Pro and Team. Extra storage costs $0.021 per GB and extra database disk $0.125 per GB. Reported, 26 November 2026 [T7-S1]
- A Supabase read replica is a separate database with its own compute and disk. An official example bills a Large replica at the same $111 as its Large primary. Reported, 26 November 2026 [T7-S6]
- Supabase Edge Functions have a 256 MB memory limit, 2 seconds of CPU time per request, and 400 seconds of wall-clock time on paid plans. Reported, 26 November 2026 [T7-S7]
- Supabase holds a SOC 2 Type 2 report. London, Frankfurt, Ireland and Paris regions exist. Reported, 26 November 2026 [T7-S8]
- Supabase says its "Europe" region group includes London and Zurich, which are not EU members. For EU-only residency, pick a specific EU region. Reported, 26 November 2026 [T7-S8]
- Supabase recommends HNSW indexes for pgvector, with up to 2,000 dimensions for the vector type and 4,000 for halfvec. Reported, 26 November 2026 [T7-S9]
</group>

<group name="T7b. Vercel and Cloudflare: plans, limits, prices">
- Vercel Pro costs $20 a month. It includes 1 deploying seat and $20 of usage credit. Extra seats cost $20 a month each. Reported, read through a search summary, 26 November 2026 [T7-S10]
- Vercel Fast Data Transfer on Pro starts at $0.15 per GB. Sources disagree on the allowance, with 1 TB per month named on the pricing page. Uncertain, 26 November 2026 [T7-S10]
- Vercel Active CPU on Pro starts at $0.128 per hour, and regional rates may be higher. Reported, read through a search summary, 26 November 2026 [T7-S10]
- Vercel Functions with Fluid compute have a 300-second default on Hobby and Pro. Pro can set 800 seconds, and up to 1,800 seconds in beta. Reported, 26 November 2026 [T7-S11]
- Vercel Functions allow up to 2 GB of memory on Hobby and 4 GB on Pro and Enterprise. A function bundle may not exceed 250 MB uncompressed. Reported, 26 November 2026 [T7-S11]
- Vercel documents an AI Gateway with team budgets, per-key budgets, bring-your-own-key and zero data retention options. Reported, 26 November 2026 [T7-S12]
- Cloudflare Workers Paid costs a $5 monthly minimum. It includes 10 million requests and 30 million CPU milliseconds. Extra use costs $0.30 per million requests and $0.02 per million CPU milliseconds. Reported, 26 November 2026 [T7-S13]
- Cloudflare Workers Free allows 100,000 requests a day and 10 milliseconds of CPU per request. Reported, 26 November 2026 [T7-S13]
- Cloudflare R2 costs $0.015 per GB-month, with 10 GB free. Writes cost $4.50 per million and reads $0.36 per million. There is no egress fee in any storage class. Reported, 26 November 2026 [T7-S14]
- Cloudflare D1 on Paid bills reads at $0.001 per million rows and writes at $1.00 per million rows. Reported, 26 November 2026 [T7-S15]
- Cloudflare Business costs $200 or $250 a month for each domain, depending on the source. Enterprise is custom. Uncertain, 26 November 2026 [T7-S16]
</group>

<group name="T7c. AWS: prices and free tier">
- AWS Lambda costs $0.20 per million requests and $0.0000166667 per GB-second on x86. The free tier gives 1 million requests and 400,000 GB-seconds each month. Reported, 26 November 2026 [T7-S17]
- The EC2 m7g.large instance in US East costs $0.0816 an hour on demand, or $59.57 a month. Prices come from price trackers. Estimate, September 2026 [T7-S18]
- A 1-year Compute Savings Plan for m7g.large was listed at $0.0540 an hour. The first-pass figure of $0.0599 was not confirmed. Estimate, June 2026 [T7-S18]
- Amazon RDS for PostgreSQL db.t4g.medium (2 vCPU, 4 GB) costs about $47 a month on demand in US East. It costs about $32 with a 1-year commitment. Estimate, 2026 [T7-S19]
- Amazon S3 Standard storage costs $0.023 per GB-month in US East. Estimate from third-party pages, 2026 [T7-S20]
- AWS data transfer out to the internet costs $0.09 per GB for the first 10 TB a month. The first 100 GB each month are free, shared across services. Estimate, 2026 [T7-S20]
- Since 15 July 2025, new AWS customers get $100 of credits at sign-up and can earn $100 more. Existing account holders are not eligible. Reported, July 2025, old source [T7-S21]
</group>

<group name="T7d. Cloud market size and shares">
- Worldwide cloud infrastructure services spend was $167.7 billion in the third quarter of 2026, up 55 per cent in a year, according to Synergy. Estimate, 29 October 2026 [T7-S22]
- Synergy shares for the third quarter of 2026 were Amazon 26 per cent, Microsoft 19 per cent and Google 16 per cent. Estimate, 29 October 2026 [T7-S22]
- Against the third quarter of 2025, Amazon lost 3 points of share, Microsoft lost 1 point and Google gained 3 points. Estimate, 29 October 2026 [T7-S22]
- The "AI services are about one third of the total" claim from the first pass was not found again. Uncertain, 2026 [T7-S22]
</group>

<group name="T7Ba. Business of the platforms and the big clouds">
- Vercel closed a Series F of $300 million at a $9.3 billion post-money valuation on 30 September 2025, co-led by Accel and GIC. Reported, 30 September 2025, old source [T7B-S1]
- Sacra estimates Vercel annual recurring revenue at $340 million in February 2026. Press reports of $500 million to $600 million run-rate in 2026 are unconfirmed by Vercel. Estimate, 2026 [T7B-S1]
- Supabase raised a $500 million Series F at a $10 billion pre-money valuation, about $10.5 billion post-money, led by GIC, in June 2026. Reported, June 2026 [T7B-S2]
- Supabase raised $100 million at $5 billion in October 2025 and $200 million at $2 billion in April 2025. Reported, 2025, old source [T7B-S2]
- Sacra estimates Supabase annualised revenue at $251 million at the end of October 2026, up from $101 million at the end of 2025. Supabase has not published revenue. Estimate, October 2026 [T7B-S2]
- Cloudflare reported third-quarter 2026 revenue of $782.5 million, up 39 per cent in a year, its fastest growth in nearly four years. Reported, 5 November 2026 [T7B-S3]
- Cloudflare raised 2026 revenue guidance to about $2.963 billion and guided fourth-quarter revenue to $845 million to $846 million. Free cash flow was $82.1 million. Reported, 5 November 2026 [T7B-S3]
- Press summaries say Amazon expects AWS growth above 40 per cent in 2027 and 2028. Estimate, October 2026 [T7B-S4]
- Google Cloud revenue was $30.71 billion in the third quarter of 2026, up 103 per cent, and Azure grew 48 per cent in fiscal first quarter 2027. Single secondary source, not checked against releases. Uncertain, October 2026 [T7B-S5]
- Google Cloud grew 82 per cent to $24.8 billion in the second quarter of 2026, with a $514 billion backlog. Azure grew 43 per cent in Microsoft fiscal fourth quarter 2026. Estimate, 2026 [T7B-S5]
</group>

<group name="T7Bb. Reliability: service level agreements and outages">
- The AWS Lambda SLA promises at least 99.95 per cent monthly uptime per region. Credits are 10 per cent below that, 25 per cent below 99.0 per cent and 100 per cent below 95.0 per cent. Reported, 2026 [T7B-S6]
- The Vercel Enterprise SLA targets 99.99 per cent availability, but it covers only components that serve customer content. The API and CLI are excluded. Reported, 2026 [T7B-S6]
- The Supabase SLA commits to 99.9 per cent uptime for Enterprise customers. Sources differ on whether it is per product or platform-wide. Reported, 2026 [T7B-S6]
- The Cloudflare Business SLA promises 100 per cent uptime for serving customer content. The separate Workers SLA sets a 99.99 per cent objective. Reported, 2026 [T7B-S6]
- The AWS us-east-1 outage ran from 11:48 pm Pacific on 19 October 2025 to about 2:20 pm on 20 October 2025, more than 14 hours. Reported, October 2025, old source [T7B-S7]
- AWS said a latent race condition in DynamoDB's automated DNS management left an empty DNS record for the regional endpoint, which then spread to EC2 and load balancers. Reported, October 2025, old source [T7B-S7]
- Cloudflare failed to deliver core traffic from 11:20 UTC on 18 November 2025 for about six hours. A ClickHouse permissions change doubled a Bot Management feature file, which crashed the module. Estimate for length, November 2025, old source [T7B-S8]
- Press trackers list Azure West US at 43 hours 44 minutes (7 February 2026) and Azure East US at 11 hours 52 minutes (24 April 2026). Both are unverified. Uncertain, 2026 [T7B-S9]
- Trackers report a Supabase outage of nearly four hours in US-East-2 on 12 February 2026 and Vercel build failures of over 12 hours on 13 January 2026. Causes not found. Uncertain, 2026 [T7B-S9]
</group>

<group name="T7Bc. Model prices, vector prices, cost at three sizes">
- Vercel AI Gateway uses prepaid credits and reports market cost next to billed cost. A zero-data-retention surcharge exists. A general markup was not found. Reported, 2026 [T7B-S11]
- Vercel AI Gateway regional inference adds a premium. One docs example shows a $0.000005 input rate rising to $0.0000055 in the EU and US regions, which is 10 per cent. Reported, 2026 [T7B-S11]
- Pinecone Standard has a $50 monthly minimum and storage at about $0.33 per GB-month. Write units cost $4 to $4.50 per million and reads $16 to $18 per million. Estimate, 2026 [T7B-S12]
- Cloudflare Vectorize rates were not retrieved. Cloudflare says the Workers free tier always allows Vectorize prototyping. Uncertain, 2026 [T7B-S12]
- Blog estimates for an AWS-hosted SaaS are about $250 to $400 a month at 1,000 users, $3,500 to $6,000 at 100,000 users and about $12,000 at 1 million. Vendor blogs, not measured bills. Estimate, 2026 [T7B-S13]
- One vendor claims a 100,000-user product costs about $630 a month on Supabase against $3,180 on AWS. The same source says AWS becomes attractive near 10 million users. Estimate, vendor claim, 2026 [T7B-S14]
</group>

<group name="T7Bd. Limits, compliance and switching">
- Vercel Hobby includes 100 GB of fast data transfer and 10 GB of fast origin transfer. It allows non-commercial personal use only. Reported, 2026 [T7B-S15]
- Vercel Hobby function invocations are listed as 1 million a month. One snippet shows 100,000, so the figure is unclear. Uncertain, 2026 [T7B-S15]
- Cloudflare Workers Paid allows up to 5 minutes of CPU time per invocation, with 30 million CPU milliseconds included. Pro costs $20 a month billed annually or $25 billed monthly. Reported, 2026 [T7B-S16]
- Cloudflare D1 on Workers Paid includes 25 billion rows read and 5 GB, then $0.001 per million rows and $0.75 per GB-month. One page shows $0.20. Each database holds up to 10 GB. Reported, 2026 [T7B-S17]
- Cloudflare D1 docs say D1 has no data-transfer charge, and R2 has no egress fee. Workers bandwidth was not addressed in these results. Reported, 2026 [T7B-S17]
- The AWS free plan ends after 6 months. The credits expire 12 months after account creation. Reported, 2026 [T7B-S18]
- Joining an AWS Organization makes free credits expire at once. Accounts that ever existed before cannot claim them. Reported, 2026 [T7B-S18]
- Vercel holds SOC 2 Type 2 and ISO 27001:2022. Pro buyers can add a HIPAA BAA, and Vercel relies on the EU-US Data Privacy Framework and standard contract clauses. Reported, 2026 [T7B-S19]
- Supabase needs at least the Team plan for a HIPAA BAA. It also requires MFA, point-in-time recovery, SSL enforcement and network restrictions. Reported, 2026 [T7B-S20]
- Cloudflare holds ISO 27001:2022, ISO 27701, ISO 27018, SOC 2 Type II and PCI DSS Level 1, and can sign a BAA for enterprise security products. Reported, 2026 [T7B-S21]
- Cloudflare Data Localization Suite is Enterprise-only. It offers an ISO 27001 certified EU region. No UK-specific region was found. Reported, 2026 [T7B-S21]
- A vendor essay estimates a Vercel to AWS move costs 1 to 4 weeks of senior engineer time. Reasons given are overage bills, compliance and scale. Estimate, 2026 [T7B-S22]
</group>

<builder_notes>
- Postgres connections are the first wall on Supabase. A Micro server allows 60 direct connections, and serverless functions open many short connections, so use the transaction pooler (port 6543) and turn off prepared statements.
- Supabase docs say a long-running server needs only an application-side pool. Serverless and edge code needs a server-side pooler such as Supavisor.
- Scaling Supabase is mostly vertical: raise compute size (brief downtime), then add read replicas for reads. Writes and auth still go to the primary.
- Vercel scales functions automatically, but long model calls meet the duration cap (300 seconds default, 800 on Pro). Streaming, queues or background jobs are the usual fix.
- On Vercel, cost grows with traffic through data transfer, edge requests and active CPU. A spend limit and alerts are needed before a spike, not after.
- Cloudflare Workers has no cold-start pain because of V8 isolates, but the CPU time per request and the 128 MB-class memory limit rule out heavy libraries (not searched).
- Cloudflare R2 has no egress fee, so it suits large files served to many users. S3 charges $0.09 per GB out, which dominates bills for media-heavy products.
- AWS gives the widest choice (Lambda, ECS, EC2, RDS, Bedrock) but needs the most set-up work: networking, IAM and cost control. Small teams lose time here (not searched).
- Typical split in 2026: Vercel for the web front end, Supabase for Postgres, auth and vectors, Cloudflare for DNS, CDN and security, AWS or Azure when an enterprise buyer or a model contract demands it (not searched).
- pgvector with HNSW is enough for many retrieval products. Supabase advises sizing RAM so the index fits in memory, and warming the cache before launch.
- Microsoft Azure and Google Cloud are the other general clouds. Azure suits Microsoft-centred enterprises and OpenAI access. Google Cloud suits data and Gemini workloads (not searched).
- Easy to move: plain Postgres (dump and restore, with replication for near-zero downtime), containers, and S3-style object storage. A Loops engineering post describes a zero-downtime move from Vercel and Supabase to AWS using replication.
- Hard to move: Supabase Auth user records and RLS policies, Edge Functions, Cloudflare Workers bindings (D1, KV, Durable Objects), and Vercel-specific features such as image optimisation and middleware.
- Supabase direct connections use IPv6 by default. IPv4-only hosts such as Vercel need the pooler or the paid IPv4 add-on. Read replicas serve only GET requests from the REST API and not Auth.
- Using a gateway or Bedrock for models lets a team swap providers by changing a model string. The cost is a possible regional premium of 10 per cent.
</builder_notes>

<investor_notes>
- Cloud demand is very strong. Synergy puts third-quarter 2026 spend at $167.7 billion, up 55 per cent. Google is taking share and AWS is losing share, though AWS still has the largest base.
- A 55 per cent growth figure is unusually high. The press summaries are secondary, so the course should quote Synergy's own release before a board meeting.
- Platform pricing mixes a fixed fee and usage. Supabase Pro is $25 plus compute. Vercel Pro is $20 per seat plus usage. The fixed part is small, so margin and risk sit in usage charges.
- Egress is the quiet cost. AWS charges $0.09 per GB out, Supabase $0.09 above 250 GB, Vercel from $0.15 per GB. R2 charges nothing. Media-heavy or data-export products can see this line grow fast.
- Lock-in is lowest for plain Postgres, containers and S3-style storage. It is highest for proprietary runtimes, edge APIs and bundled auth. The cost to move was not searched in this pass.
- Supabase runs on AWS regions, so its customers still depend on AWS reliability. Platform convenience does not remove the underlying cloud risk.
- Bull view: low entry cost lets a start-up reach 100,000 users on under a few hundred dollars a month of base fees. Bear view: usage charges and egress can rise faster than revenue per user.
- Company revenue, funding and valuation for Vercel, Supabase and Cloudflare were not found in this pass, so demand from AI builders cannot be sized here.
- Platform valuations are high against estimated revenue. Supabase at $10.5 billion on roughly $170 million to $251 million of estimated recurring revenue is about 40 to 60 times sales. Revenue is unaudited.
- Cloudflare is the public benchmark. Revenue growth of 39 per cent and free cash flow at 10 per cent of revenue show the edge business is scaling with AI traffic.
- Bear view for platforms: the buyers who grow are tempted to move to AWS for cost and compliance. Bull view: AI coding tools create new projects on Supabase and Vercel faster than the old ones leave.
- The Cloudflare SLA of 100 per cent uptime coexists with a six-hour global outage in November 2025. SLA credits do not cover lost revenue, so check what the credit actually pays.
</investor_notes>
</topic>

<topic key="T8" name="AI software businesses, adoption and investment">
<group name="T8a. AI application companies: revenue and valuation">
- Cursor (Anysphere) passed $2 billion in annualised revenue in February 2026, double the figure of three months before. Estimate, 2 March 2026 [T8-S1]
- Cursor reached about $4 billion in annualised revenue by May or June 2026. Sacra and Dealroom give this, and it is not a company figure. Estimate, mid 2026 [T8-S2]
- Cursor was valued at $29.3 billion in November 2025 and was reported in talks at $50 billion in April 2026. Estimate, April 2026 [T8-S2]
- Lovable raised $400 million at a $13.3 billion valuation in 2026, more than double its value eight months earlier. Reported, 2026 [T8-S4]
- Lovable said its run-rate revenue passed $600 million in September 2026. Earlier figures were about $400 million in February 2026. Reported, September 2026 [T8-S4]
- Harvey was valued at about $11 billion after a $200 million round in March 2026. The earlier mark was $8 billion in late 2025. Estimate, March 2026 [T8-S5]
- Harvey annual recurring revenue is estimated at $190 million in January 2026 and $300 million in May 2026. The company gave no audited figure. Estimate, 2026 [T8-S5]
- Sierra raised $950 million at a $15.8 billion post-money valuation in May 2026. Reported, 4 May 2026 [T8-S6]
- Sierra said it passed $400 million in annual recurring revenue on 30 October 2026, up from $100 million in November 2025. Reported, 30 October 2026 [T8-S6]
- Sierra was reported in talks at about $30 billion, or 75 times its $400 million run rate. This is a talks report only. Uncertain, October 2026 [T8-S6]
- ElevenLabs raised $500 million at an $11 billion valuation in its Series D, announced in February 2026. Reported, 4 February 2026 [T8-S7]
- ElevenLabs reported more than $500 million in annual recurring revenue in the first four months of 2026. Reported, 2026 [T8-S7]
- A September 2026 employee tender valued ElevenLabs at $22 billion, with about $600 million of recurring revenue. The company did not confirm it. Uncertain, September 2026 [T8-S7]
- Replit raised $400 million at a $9 billion valuation in March 2026, and reached about $525 million of annualised revenue by April 2026. Estimate, April 2026 [T8-S8]
- Perplexity annualised revenue passed $750 million in August 2026, up from under $250 million in January 2026. Sacra gives a lower $454 million for March 2026. Estimate, August 2026 [T8-S9]
- Perplexity was last priced at about $20 billion to $23 billion, with a round above $30 billion under discussion. No new round had closed in the sources. Uncertain, 2026 [T8-S9]
- Glean passed $300 million in annual recurring revenue in May 2026. Its last priced round is $7.2 billion in June 2025. Estimate, May 2026 [T8-S10]
</group>

<group name="T8b. Margins, price models and retention">
- Mature software usually shows 70 to 90 per cent gross margin, and the median stays above 80 per cent in one benchmark. Estimate, 2026 [T8-S11]
- Cursor had a gross margin of minus 23 per cent in the quarter to January 2026, per The Information, and later turned slightly positive on large enterprise accounts. Estimate, 2026 [T8-S12]
- Foundamental estimated that Cursor paid Anthropic about $650 million a year against about $500 million of annualised revenue, a margin near minus 30 per cent. Estimate, old source of 2025 [T8-S12]
- Intercom charges $0.99 for each resolution by its Fin agent, and Zendesk starts at $1.50. A human-handled case is quoted at $10 to $15. Reported, 2026 [T8-S13]
- Salesforce Agentforce moved from $2 for each conversation to Flex Credits at $0.10 for each action in May 2025. Reported, old source of May 2025 [T8-S13]
- AI-native products priced above $250 a month show 70 per cent gross and 85 per cent net revenue retention, close to B2B software. Estimate, December 2025 [T8-S14]
- AI-native products priced under $50 a month show only 23 per cent gross and 32 per cent net revenue retention. Estimate, December 2025 [T8-S14]
- AI-powered subscription apps showed annual retention of 21.1 per cent against 30.7 per cent for non-AI apps, and 4.2 per cent refunds against 3.5 per cent. Reported, March 2026 [T8-S15]
</group>

<group name="T8c. Company use of AI, spend and productivity evidence">
- McKinsey found 37 per cent of organisations see enterprise-level profit impact from AI, flat on 2025. Only about 6 per cent report at least 5 per cent of profit from AI. Reported, June 2026 [T8-S16]
- In the same McKinsey survey, 20 per cent of respondents said AI operating costs, including tokens, limited their use. The sample was 1,719 people. Reported, June 2026 [T8-S16]
- The US Census Bureau reports that 37 per cent of firms with 250 staff or more use AI, and 32 per cent of firms with 100 to 249 staff. Reported, May 2026 [T8-S17]
- US firm-level AI use was about 18 to 20 per cent from December 2025 to May 2026. The question changed in November 2025, so older data do not compare. Reported, May 2026 [T8-S17]
- Eurostat reports that 20.0 per cent of EU firms with 10 staff or more used AI in 2025, up from 13.5 per cent in 2024. Large firms show 55 per cent. Reported, 11 December 2025 [T8-S18]
- The Stanford AI Index 2026 says about 88 per cent of organisations used AI in at least one business use in 2025, 10 points above 2024. Reported, April 2026 [T8-S19]
- Menlo Ventures puts 2026 enterprise AI spend at $176.8 billion, split into $99.5 billion infrastructure and $77.3 billion applications. Menlo invests in Anthropic. Estimate, 3 November 2026 [T8-S20]
- Menlo restated 2025 enterprise generative AI spend to $33 billion, down from $37 billion in its December 2025 report. Estimate, November 2026 [T8-S20]
- Gartner forecasts worldwide AI spending of about $2.67 trillion in 2026, and about $28.3 billion for generative AI models. Estimate, 16 September 2026 [T8-S21]
- Google says AI now generates about 75 per cent of its new code, up from 25 per cent in 2024, with engineer review. Reported, April 2026 [T8-S23]
- Anthropic's CFO said "90 per cent plus" of its code is written by Claude. This is an executive statement, not an audit. Reported, 2026 [T8-S23]
</group>

<group name="T8d. Finance, bubble dispute, failure and private equity">
- US AI companies took 82.7 per cent of venture deal value through September 2026, a record in the PitchBook-NVCA series. Reported, September 2026 [T8-S25]
- Worldwide, 64 per cent of venture dollars in the third quarter of 2026 went to AI start-ups, from a secondary report. Estimate, Q3 2026 [T8-S25]
- Median private AI revenue multiples are reported at 21 to 26 times, against 5.5 times for older software. Median public software sits near 3 to 5 times. Estimate, 2026 [T8-S26]
- Combined 2026 capital spending of the four largest hyperscalers is put at $700 billion to $745 billion, up 77 per cent on 2025. Estimate, 2026 [T8-S27]
- Goldman Sachs found hyperscalers took on $121 billion of debt in a year. Estimate, 2026 [T8-S28]
- Goldman reportedly sees circular deals such as Nvidia's investment in OpenAI at up to 15 per cent of Nvidia's 2027 revenue. Estimate, 2026 [T8-S28]
- ServiceNow completed its $2.85 billion purchase of Moveworks. Estimate, 2026 [T8-S3]
- Alvarez and Marsal found AI use in value creation rose to 63 per cent of European private equity respondents, from 41 per cent in 2025. Reported, May 2026 [T8-S31]
- Grant Thornton calls an "AI proof gap" in private equity, where confidence is high but measurable returns are below average. Reported, 2026 [T8-S31]
</group>

<group name="T8Ba. Cursor deal, adoption figures and pricing">
- SpaceX announced the $60 billion all-stock purchase of Anysphere, the parent of Cursor, on 16 June 2026. CNBC and Yahoo Finance both report it. Reported, 16 June 2026 [T8B-S1]
- Most sources say the deal closed on 14 August 2026. Anysphere shares converted into 389,289,254 SpaceX Class A shares and Cursor joined a new SpaceXAI unit. Estimate, August 2026 [T8B-S2]
- The deal traces to April 2026, when SpaceX bought a $10 billion option to acquire Cursor for $60 billion. IPO filings set a $1.5 billion termination fee. Estimate, 2026 [T8B-S1]
- The Anthropic Economic Index for April to May 2026 classifies 51.4 per cent of Claude conversations as augmentation and 48.6 per cent as automation. Reported, data published 24 June 2026 [T8B-S3]
- In the same period 43.4 per cent of conversations were work, 40.2 per cent personal and 16.5 per cent coursework. Computer and mathematical tasks made up 23.8 per cent. Reported, June 2026 [T8B-S3]
- Software development was 11.5 per cent of Claude conversations by topic. Tasks that a classifier says take 5 hours alone ran about 40 minutes with Claude. This is an automated estimate. Reported, June 2026 [T8B-S3]
- The Economic Index covers 121 countries and 923 occupations. It describes Claude chat and Cowork usage only. It is not a measure of jobs or of AI use across the economy. Reported, June 2026 [T8B-S3]
- The latest ONS bulletin of 8 October 2026 says 38 per cent of UK businesses with 10 or more staff reported using AI, up 3 points on June 2026. Reported, 8 October 2026 [T8B-S4]
- The same ONS bulletin says use rose 26 points among firms with 10 or more staff since September 2023. This was found in a search summary, not the ONS page. Reported, 8 October 2026 [T8B-S4]
- Coverage of the ONS series puts all-business AI use at about 29 per cent. This is an inference from wording, so check the ONS dataset before citing it. Uncertain, October 2026 [T8B-S4]
- A separate UK government AI adoption survey found 32 per cent of businesses used at least one AI technology in 2026, against 16 per cent in 2025. Reported, 2026 [T8B-S4]
- Sacra reports Intercom ARR of $382 million at end 2025 and $419 million in April 2026. Estimate, April 2026 [T8B-S5]
- Cursor moved its $20 Pro plan from request limits to compute limits on 16 June 2025 and added a $200 Ultra plan. Surprise charges followed. Reported, July 2025, old source [T8B-S6]
- Cursor apologised and offered refunds for unexpected usage between 16 June and 4 July 2025. Reported, July 2025, old source [T8B-S6]
- Salesforce Agentforce ARR was about $800 million at the end of fiscal 2026, up 169 per cent, and $1.5 billion by the fiscal 2027 second quarter. Reported, 2026 [T8B-S7]
- Salesforce launched the Agentic Enterprise License Agreement in October 2025. It is a seat-style flat fee with credits, so it is partly a retreat from pure usage pricing. Reported, 2026 [T8B-S7]
</group>

<group name="T8Bb. Technical diligence, margins and failure causes">
- Practitioner checklists agree on five checks beyond code review: model dependency, data rights, evaluation sets, inference cost and handover artefacts. Most are blog posts, not research. Estimate, 2026 [T8B-S8]
- A weak answer on evaluation is "we eyeball outputs" or a demo with no golden dataset and no scores. A strong answer shows test results by release. Estimate, 2026 [T8B-S8]
- A weak answer on margin assumes SaaS-like margins and has no cost per action. A strong answer reports AI gross margin with compute included and its trend as volume grows. Estimate, 2026 [T8B-S8]
- Flagged risks include one model vendor with no fallback, margin that depends on expiring cloud credits, and training data the company cannot prove it may use. Estimate, 2026 [T8B-S8]
- Neurons Lab suggests asking what share of workflows AI completes end to end, which tasks still need people, and what human review costs. Estimate, 2026 [T8B-S8]
- High net revenue retention with weak gross retention is a warning, because upsell may be hiding churn. Estimate, 2026 [T8B-S8]
- Replit gross margin ranged from minus 14 per cent to 36 per cent in 2025, per The Information. Sacra says it rose from minus 14 per cent in April 2025 to 23 per cent in July 2025. Estimate, 2025 [T8B-S9]
- Sacra reports Lovable gross margin of 36 per cent in May 2025 with a target of 65 per cent in the second half of 2026. Estimate, 2025 [T8B-S9]
- RAND interviewed 65 AI experts in 2024. Its root causes are miscommunicated problems, chasing new technology, short time horizons and weak data and deployment infrastructure. Reported, August 2024, old source [T8B-S10]
- Press often quotes RAND as an 80 per cent failure rate, but the RAND summary does not state it. Uncertain, 2024, old source [T8B-S10]
- S&P Global found 42 per cent of companies abandoned most AI initiatives before production, up from 17 per cent. The average firm scrapped 46 per cent of proofs of concept. Reported, 27 October 2025 [T8B-S11]
- The S&P Global survey covers over 1,000 respondents in North America and Europe. The 2025 reading may be from mid-year. Reported, October 2025 [T8B-S11]
</group>

<group name="T8Bc. Developer studies, team effects and private equity">
- Randomised trials at Microsoft, Accenture and a Fortune 100 firm found Copilot raised weekly completed tasks by 26.08 per cent, with a standard error of 10.3 points. Reported, February 2025 draft [T8B-S12]
- Those trials ran in 2022 and 2023 on a GPT-3.5 based Copilot. Less experienced developers adopted it more and gained more. Reported, 2025 draft, old source [T8B-S12]
- GitHub reports the Accenture trial raised pull requests by 8.69 per cent and the pull request merge rate by 15 per cent. Reported, 2024, old source [T8B-S13]
- In that trial task time was about 23 minutes with AI and 25 without, a gap that was not significant. The largest gap was on debugging questions. Reported, January 2026 [T8B-S14]
- The Stanford authors say the adjustment works through less hiring of young workers, not more separations. Part of the timing for developers may have other causes. Reported, February 2026 [T8B-S16]
- Salesforce hired no new software engineers in 2025 and Benioff said the engineering headcount stayed flat near 15,000. These are CEO statements. Reported, 2025 to 2026 [T8B-S17]
- Gartner found 23 per cent of tech leaders spend $200 to $500 per developer per month on tokens for coding agents. About 6 per cent spend over $2,000. Estimate, 2026 [T8B-S18]
- Larridin puts median coding-agent spend near $920 per engineer per month and the 90th percentile above $3,900. Pragmatic Engineer found budgets of $150 to $3,000 in 27 workplaces. Estimate, 2026 [T8B-S18]
- Microsoft's CEO said in April 2025 that AI wrote 20 to 30 per cent of code in company projects. Zuckerberg's "half" for Meta was a target, not a result. Reported, April 2025, old source [T8B-S19]
- SignalFire says new-graduate hiring at 12 large tech firms is down about 65 per cent against 2019. Causes are contested. Estimate, 2026 [T8B-S19]
- PwC found only 14 per cent of PE-backed CEOs say AI raised revenue and cut costs together. Reported, 2026 [T8B-S20]
- FTI Consulting found 19 per cent of high-performing PE firms say AI beat its business case, against 5 per cent of other firms. Reported, 2026 [T8B-S20]
- Bain says the old SaaS KPI stack of ARR, net retention and gross margin misses AI impact, and GPs lack tools to measure it. Reported, 2026 [T8B-S21]
- Bain also says typical deals now need 10 to 12 per cent yearly EBITDA growth for a 2.5 times return. Reported, 2026 [T8B-S21]
</group>

<builder_notes>
- Inference cost is part of the cost of goods. Agent loops that read large contexts and retry can use many times the tokens of a chat, so track cost for each task, not for each seat.
- Cursor shows the route out of a thin margin: route easy work to cheaper models, train an own model such as Composer, and change prices for heavy users. (partly searched)
- An evaluation set of real customer tasks is the first asset. Without it a team cannot swap models safely or prove the product improves. (not searched)
- A thin layer on a model has no private data, no workflow depth and no integrations. A model maker can ship the same feature in one release, as with meeting recorders and personal finance in ChatGPT.
- Depth means writing back to the customer's systems, handling permissions and audit logs, and owning the failure path when the model is wrong. (not searched)
- Pilots fail in practice from poor data access, weak integration with existing workflows, unclear owners, and cost surprises at scale. MIT and Gartner point the same way.
- Share of code written by AI is not a productivity figure. Google counts reviewed AI output, and METR found slowdowns on familiar codebases. Review and test load rise.
- Claude Code costs $150 to $250 a developer a month on average. That is small against a salary, but heavy agent use can exceed $30 a day.
- Fine-tuned or own models help most where volume is high and the task is narrow, because they cut unit cost and latency. They add a training and evaluation burden. (not searched)
</builder_notes>

<investor_notes>
- Growth is real and fast. Cursor, Lovable, Sierra and ElevenLabs each report or are estimated at $400 million to $4 billion of annual recurring revenue. Many figures are run rates, and some include usage.
- Valuation multiples are high. Sierra at $15.8 billion on $400 million is about 40 times, and Harvey about 37 to 58 times. Bulls cite growth. Bears cite public software at 3 to 5 times.
- Margins are the first test. AI products average about 45 to 53 per cent gross margin against 70 to 90 per cent for software. Cursor ran negative. Low-price self-serve products lose customers fastest.
- Retention splits by price. Products above $250 a month look like software. Consumer-priced AI wrappers churn heavily. Ask for cohorts by price band.
- Dependence on a model supplier is a margin and survival risk. The supplier can raise prices, or launch a rival feature. Check for a second model source and an own model.
- Company use is wide but profit is thin. 88 per cent of firms use AI in some way, yet only 37 per cent see a profit effect and about 6 per cent see a large one.
- Productivity evidence cuts both ways. Google and Anthropic report most code is AI written. METR measured slowdowns, then called its newer result unreliable. Do not underwrite headcount cuts on one study.
- The bubble case cites $700 billion or more of yearly capital spending, debt, and circular deals. The other side cites Nvidia and lab revenue growth and strong hyperscaler balance sheets.
- In private equity, adoption is rising but measured EBITDA lags. Diligence should ask for the evaluation results, token cost for each customer, model contracts, data rights and the share of revenue at risk from a model maker feature.
- The Cursor sale shows the exit route for a heavy-loss coding product: a buyer with its own compute. Check whether the $60 billion price was mostly stock in a company that later listed.
- Seat-to-usage change cuts both ways. Cursor's June 2025 change led to a public apology and refunds. Salesforce answered with flat-fee credit deals. Ask any target for revenue before and after a price change.
- Developer trials disagree because of design. Controlled trials show gains of 8 to 26 per cent, the DORA survey shows more instability, and the Anthropic trial shows weaker learning. Do not use one figure to cut headcount.
- Evidence on junior hiring points one way but is not causal. Ask a target how it will build senior talent if it stops hiring juniors.
- PE surveys disagree: FTI is positive and PwC and Grant Thornton are not. Ask each portfolio company for measured EBITDA, not survey sentiment.
</investor_notes>
</topic>

<topic key="T9" name="Basic terms, and the mechanism of a language model">
<group name="T9a. Standard terms and how tokens are counted">
- ISO/IEC 22989:2022 is the international standard for AI concepts and terminology. Its machine learning section (5.11) covers supervised, unsupervised, semi-supervised and reinforcement learning. The exact definition wording was not retrieved. Reported, 2022 (old source) [T9-S1]
- The OECD adopted a revised definition of an AI system on 8 November 2023. It is a machine-based system that infers from its input how to produce outputs such as predictions, content or decisions. Reported, November 2023 (old source) [T9-S2]
- The OECD definition says the outputs can influence physical or virtual environments. The OECD explained it in Artificial Intelligence Papers No. 8, published February 2024. Reported, February 2024 (old source) [T9-S2]
- NIST AI 600-1 defines generative AI as the class of AI models that emulate the structure and characteristics of input data to generate derived synthetic content. Reported, July 2024 (old source) [T9-S3]
- NIST AI 600-1 is voluntary guidance. It names 12 risks that are new or made worse by generative AI. Reported, July 2024 (old source) [T9-S3]
- OpenAI's help centre gives these English rules of thumb: 1 token is about 4 characters or three quarters of a word, so 100 tokens are about 75 words. Reported, accessed 26 November 2026 [T9-S4]
- Google's Gemini documentation gives a similar rule: 1 token is about 4 characters, and 100 tokens equal about 60 to 80 English words. Reported, accessed 26 November 2026 [T9-S5]
- Anthropic's documentation gives no fixed words-per-token ratio. It says the token count is an estimate and offers a free token counting endpoint for exact numbers. Reported, accessed 26 November 2026 [T9-S6]
- Anthropic says 1 million tokens equals about 555,000 words on the tokenizer introduced with Opus 4.7, against 750,000 before. That is about 35 per cent more tokens per word. Reported, accessed 26 November 2026 [T9B-S6]
- Petrov and co-authors found that the same text translated into different languages can need up to 15 times more tokens, across 17 tokenizers. Estimate, 2023 (old source) [T9-S8]
- Gemini counts images up to 384 pixels on both sides as 258 tokens. Larger images are cut into 768 by 768 pixel tiles of 258 tokens each. Reported, accessed 26 November 2026 [T9-S5]
- Gemini counts video at 263 tokens per second and audio at 32 tokens per second. A 60-second video is about 15,780 tokens and 60 seconds of audio about 1,920 tokens. Reported, accessed 26 November 2026 [T9-S5]
- Anthropic's current vision documentation counts each 28 by 28 pixel patch of an image as one visual token. The older estimate was width times height divided by 750. Reported, accessed 26 November 2026 [T9-S9]
- OpenAI's older vision rule gave 85 base tokens plus 170 tokens per 512 pixel tile. Its current calculator uses 32 by 32 patches, and users report counts that differ from the old formula. Uncertain, accessed 26 November 2026 [T9-S10]
</group>

<group name="T9b. Next-token prediction, embeddings, the transformer and training">
- The 2017 paper "Attention Is All You Need" by eight authors, first posted on 12 June 2017, proposed a model built only on attention, with no recurrence or convolution. Reported, 2017 (old source) [T9-S11]
- The base transformer in that paper used a model width (d_model) of 512. The big model reached 41.8 BLEU on English to French translation after 3.5 days on eight GPUs. Reported, 2017 (old source) [T9-S11]
- OpenAI text-embedding-3-small returns 1,536 numbers per text and costs $0.02 per 1 million tokens. The large model returns 3,072 numbers and costs $0.13 per 1 million tokens. Reported, accessed 26 November 2026 [T9-S12]
- OpenAI's batch rate for embeddings is half the standard rate, at $0.01 (small) and $0.065 (large) per 1 million tokens. Reported, accessed 26 November 2026 [T9-S12]
- Google lists gemini-embedding-001 at $0.15 per 1 million input tokens, with an input limit of 2,048 tokens and support for over 100 languages. Reported, July 2025 (old source) [T9-S13]
- Chinchilla (DeepMind, 2022) trained a 70 billion parameter model on 1.4 trillion tokens. This is about 20 training tokens for each parameter. It beat the 280 billion parameter Gopher. Reported, March 2022 (old source) [T9-S14]
- Meta pre-trained Llama 3.1 405B with 3.8 times 10 to the power 25 floating point operations on over 15 trillion tokens and more than 16,000 H100 GPUs. Reported, July 2024 (old source) [T9-S15]
- Epoch AI estimates that training compute for frontier language models has grown about 5 times each year since 2020 (90% range 4 to 6 times). Estimate, February 2026 [T9-S16]
- Epoch AI lists Grok 4, at about 5 times 10 to the power 26 operations, as the largest known training run. Estimate, February 2026 [T9-S16]
- The InstructGPT paper showed that human raters preferred outputs from a 1.3 billion parameter model trained with human feedback over the 175 billion parameter GPT-3. Reported, March 2022 (old source) [T9-S17]
- DeepSeek-R1 used reinforcement learning with simple accuracy and format rewards, without human-written reasoning steps. Nature published it in 2025. Reported, September 2025 (old source) [T9-S18]
- The Nature supplement puts the R1 training cost at $294,000 for the final run. This excludes the base model and the wider research programme. Reported, September 2025 (old source) [T9-S18]
- Llama 3.1 405B weights need about 810 GB in 16-bit form and about 405 GB in 8-bit (FP8) form. One 8-GPU H100 node has 640 GB of memory. Estimate, 2024 (old source) [T9-S19]
</group>

<group name="T9c. Sampling settings, inference, context and reasoning">
- Anthropic's Fable 5.2 page says to omit temperature, top_p and top_k, and links to the values that return a 400 error. Reported, November 2026 [T9B-S7]
- For GPT-5.2, OpenAI's temperature, top_p and logprobs settings work only when reasoning effort is "none". Older GPT-5 models reject non-default values. This comes from forum posts quoting OpenAI. Uncertain, 2026 [T9-S21]
- Prefill (reading the input) runs in parallel. Decode (writing output) runs one token at a time and is limited by memory bandwidth. Estimate, 2025 [T9-S22]
- One analysis says prefill uses the chip at 50% or more, so input tokens should cost about one third of output tokens. It notes GPT-4o prices matched this. Estimate, 2025 (old source) [T9-S23]
- Google lists Gemini 3.1 Pro Preview at $2 input and $12 output per 1 million tokens up to 200,000 tokens. Prompts above that cost $4 and $18. Reported, 2026 [T9-S26]
- Liu and co-authors found that models answer worse when key facts sit in the middle of a long input, and best when they sit at the start or end. Reported, 2023 (old source) [T9-S27]
- Chroma tested 18 models in July 2025 and found that accuracy becomes less reliable as input length grows, even on very simple tasks. Reported, 14 July 2025 (old source) [T9-S28]
- NVIDIA's RULER benchmark found that all tested models claim 32,000 tokens or more, but only about half keep good accuracy at 32,000 tokens. Reported, April 2024 (old source) [T9-S29]
- OpenAI bills hidden reasoning tokens at the output rate. They also fill the context window and are not shown through the API. Reported, accessed 26 November 2026 [T9-S30]
- Anthropic bills thinking tokens as output tokens, and shows the count in usage details. Claude 4.7 and later reject the old budget_tokens setting and use adaptive thinking with an effort setting. Reported, accessed 26 November 2026 [T9-S31]
</group>

<group name="T9d. Hallucination and knowledge cut-off dates">
- OpenAI researchers argue that models hallucinate because training and test scoring reward guessing over saying "I do not know". They propose penalising confident errors more than abstention. Reported, 5 September 2025 (old source) [T9-S32]
- OpenAI says hallucinations persist in newer models. GPT-5 hallucinated less than earlier models, especially when it reasoned. Reported, 5 September 2025 (old source) [T9-S32]
- Anthropic's guide lists three methods: allow Claude to say it does not know, extract word-for-word quotes first, and require a supporting quote for each claim. It says these reduce but do not remove errors. Reported, accessed 26 November 2026 [T9-S33]
- Stanford tested AI legal research tools with retrieval. Lexis+ AI and Westlaw tools hallucinated in 17% to over 34% of queries. Reported, 2024 (old source) [T9-S34]
- In the updated Stanford study, Lexis+ AI answered 65% of queries accurately. Westlaw AI-Assisted Research was accurate 42% of the time. Reported, 2025 (old source) [T9-S34]
- Anthropic lists August 2025 as the training data cut-off for Claude Opus 4.5. It lists May 2025 as the reliable knowledge cut-off for that model. Reported, 2025 (old source) [T9-S35]
- OpenAI's models page lists GPT-6 Luna with a knowledge cut-off of 18 May 2026. Reported, 2026 [T9-S36]
- Google's Gemini 3.6 Flash card gives March 2026 as its cut-off. It says some domains may be limited to January 2025, as in the Gemini 3 family. Reported, 2026 [T9-S37]
</group>

<group name="T9e. Open-weight models and hardware">
- Open-weight models publish the trained parameters, often without the training data or code. The OSI's Open Source AI Definition 1.0 (October 2024) also asks for data information and code. Reported, October 2024 (old source) [T9-S38]
- The OSI places Llama, Gemma and Qwen in the open-weights category, not open source, because of custom licences. Reported, 2024 (old source) [T9-S38]
- OpenAI released gpt-oss-120b (117 billion parameters, 5.1 billion active) and gpt-oss-20b (21 billion, 3.6 billion active) under the Apache 2.0 licence. Reported, August 2025 (old source) [T9-S39]
- The gpt-oss-120b model fits on one 80 GB GPU, and gpt-oss-20b runs within 16 GB of memory, because the expert weights use 4-bit MXFP4. Reported, August 2025 (old source) [T9-S39]
- DeepSeek-V3 has 671 billion parameters with 37 billion active per token. It trained on 14.8 trillion tokens in 2.788 million H800 GPU hours, costed at $5.576 million. Reported, December 2024 (old source) [T9-S40]
- The $5.576 million DeepSeek-V3 cost assumes a $2 per hour GPU rental price. It covers the final run only. Reported, December 2024 (old source) [T9-S40]
- Kimi K2 has 1 trillion parameters with 32 billion active, under a modified MIT licence. Kimi K3 uses a custom licence. Estimate, July 2026 [T9-S41]
- Qwen 3.5 models such as the 122 billion parameter (10 billion active) version use Apache 2.0, while Alibaba's Qwen 3.7 Max flagship is closed. Estimate, 2026 [T9-S41]
</group>

<group name="T9Ba. Definitions and the original papers">
- NIST's glossary defines machine learning as the development and use of computer systems that adapt and learn from data, with the goal of improving accuracy. Reported, accessed 26 November 2026 [T9B-S1]
- A NIST glossary entry defines a large language model as a class of language models that use deep-learning algorithms and train on extremely large text datasets, possibly many terabytes. Reported, accessed 26 November 2026 [T9B-S2]
- NIST SP 800-218A defines an AI model as a component of an information system that uses computational, statistical or machine-learning techniques to produce outputs from given inputs. Reported, accessed 26 November 2026 [T9B-S1]
- IBM describes deep learning as a subset of machine learning built on multilayer neural networks. IBM pages disagree on the layer rule, giving "more than three" and "at least four" layers. Reported, accessed 26 November 2026 [T9B-S3]
- Anthropic's "Building effective agents" defines workflows as systems where LLMs and tools follow predefined code paths. It defines agents as systems where LLMs dynamically direct their own process and tool use. Reported, 19 December 2024 (old source) [T9B-S4]
- The retrieval-augmented generation (RAG) paper by Lewis and eleven co-authors was posted on 22 May 2020 and presented at NeurIPS 2020. Reported, 2020 (old source) [T9B-S5]
- The RAG authors came from Facebook AI Research, University College London and New York University. Reported, 2020 (old source) [T9B-S5]
- The RAG idea in one sentence: a text generator (BART) gets passages fetched from a Wikipedia vector index by a trained retriever, so answers use outside knowledge. Reported, 2020 (old source) [T9B-S5]
- The RAG paper reported state-of-the-art results on three open-domain question answering tasks, beating models that rely only on knowledge stored in their parameters. Reported, 2020 (old source) [T9B-S5]
</group>

<group name="T9Bb. Modalities and knowledge cut-offs of current flagships">
- Anthropic's models page says all current Claude models (Fable 5.2, Opus 5.5, Sonnet 5.5, Haiku 5.5) take text and images in and give text out. Reported, accessed 26 November 2026 [T9B-S6]
- Claude Fable 5.2 was released on 9 November 2026. It costs $8 per 1 million input tokens and $40 per 1 million output tokens, with a 1 million token context window. Reported, 9 November 2026 [T9B-S7]
- Claude Opus 5.5 costs $4 input and $20 output per 1 million tokens. Sonnet 5.5 costs $2 and $10. Haiku 5.5 costs from $0.10 and $0.50. Reported, accessed 26 November 2026 [T9B-S6]
- Anthropic lists both the reliable knowledge cut-off and the training data cut-off as June 2026 for Fable 5.2, Opus 5.5, Sonnet 5.5 and Haiku 5.5. Reported, accessed 26 November 2026 [T9B-S6]
- OpenAI's GPT-6 Astra page lists text and image input and text output. Audio and video are not supported. Reported, accessed 26 November 2026 (read through a search summary of the page) [T9B-S8]
- OpenAI's GPT-6 Astra page and the Amazon Bedrock model card both give a knowledge cut-off of 30 April 2026. The page also lists a 1,050,000 token context window. Reported, 2026 [T9B-S8]
- Google's Gemini API page for Gemini 4 Argon lists text, image, video, audio and PDF input, with text as the only output. Image and audio generation are marked unsupported. Reported, 2026 (read through a search summary) [T9B-S9]
- Google's model card gives March 2026 as the knowledge cut-off for Gemini 4 Argon. Google announced Argon on 30 September 2026 and made it generally available on 13 October 2026. Reported, 2026 [T9B-S10]
</group>

<group name="T9Bc. Reasoning gains and measured hallucination">
- OpenAI reported that GPT-4o solved 12% of AIME 2024 maths problems. The reasoning model o1 solved 74% with one attempt, 83% with 64-sample consensus and 93% with 1,000 re-ranked samples. Reported, 12 September 2024 (old source) [T9B-S11]
- The Qwen3 report lists Qwen3-235B-A22B at 40.1 on AIME 2024 in non-thinking mode. The 85.7 headline score is most likely thinking mode, but the table caption conflicts. Uncertain, 2025 (old source) [T9B-S12]
- Anthropic bills Claude 3.7 Sonnet thinking tokens at the normal output price of $15 per 1 million tokens, with a thinking cap of up to 128,000 tokens. Reported, February 2025 (old source) [T9B-S13]
- Anthropic says its effort setting trades thoroughness for token cost. At the highest "max" setting the model runs slower and costs more than at "xhigh", often for a small gain. Reported, accessed 26 November 2026 [T9B-S14]
- Vectara's leaderboard of 24 November 2026 measures summary hallucination on 7,700 private articles, scored by its HHEM-2.3 model. The lowest rate listed is 1.8% for antgroup/finix_s1_32b. Reported, 24 November 2026 [T9B-S15]
- On that leaderboard GPT-6 Astra scores 8.7%, GPT-6 Sol 6.5% and GPT-5.5 9.3%. Claude Opus 5.5 scores 9.9% and Claude Opus 4.7 scores 12.0%. Reported, 24 November 2026 [T9B-S15]
- On that leaderboard Gemini 4 Argon scores 12.1%, Gemini 3.1 Pro Preview 10.4% and Gemini 2.5 Flash Lite 3.3%. Small and older models often beat flagships on this summary test. Reported, 24 November 2026 [T9B-S15]
- Reasoning does not always lower this rate. Vectara lists GPT-5.1 at 10.9% on low effort and 12.1% on high, and GPT-5.2 at 8.4% low and 10.8% high. Reported, 24 November 2026 [T9B-S15]
- OpenAI's GPT-5 system card reportedly gave a 4.5% rate of responses with incorrect claims for GPT-5 thinking, against 12.7% for o3 and 12.9% for GPT-4o, with browsing. Estimate, August 2025 (old source, via a press report) [T9B-S16]
- The same press report gives short-answer SimpleQA error rates without browsing of 40% for GPT-5 thinking and 52% for GPT-4o, so factual recall stays weak. Estimate, August 2025 (old source) [T9B-S16]
</group>

<group name="T9Bd. Running and licensing open-weight models">
- NVIDIA's TensorRT Model Optimizer supports FP8, INT8, INT4 and NVFP4 quantisation. NVIDIA's own tests found FP8 keeps accuracy best. Reported, accessed 26 November 2026 [T9B-S17]
- Quantisation in plain words: store each weight in fewer bits. FP8 uses about 1 byte per parameter and INT4 about 0.5 bytes, against 2 bytes in 16-bit form. Estimate, 2026 (third-party guide) [T9B-S17]
- NVIDIA's model card says FP8 cuts bits per parameter from 16 to 8, which reduces disk size and GPU memory needs by about 50%. Reported, accessed 26 November 2026 [T9B-S18]
- Batching in plain words: serve many requests at once so the weights in memory are shared. NVIDIA calls the in-flight form "continuous batching", where requests join and leave a running batch. Reported, accessed 26 November 2026 [T9B-S17]
- Static batching makes every request wait for the longest one. Each request still needs its own KV cache, which can be large. Reported, accessed 26 November 2026 [T9B-S17]
- A vLLM recipe puts the FP8 Llama 3.3 70B at about 70 GB, which only just fits one 80 GB GPU with little cache room. Reported, accessed 26 November 2026 [T9B-S19]
- NVIDIA's Dynamo recipe for Llama 3.3 70B FP8 uses four H100 or H200 GPUs. A DigitalOcean report says a tuned stack runs it on two H100s. Reported, accessed 26 November 2026 [T9B-S19]
- A rule of thumb for weight memory is parameters times bits per weight divided by 8, plus about 20% overhead. A 4-bit 70 billion model needs about 35 GB of weights. Estimate, 2026 [T9B-S20]
- The Llama 3.1 licence requires a licence request to Meta if the products had over 700 million monthly active users in the month before release. Meta may refuse at its sole discretion. Reported, July 2024 (old source) [T9B-S21]
- The Llama 3.1 licence requires "Built with Llama" display, and requires any distributed model trained on Llama outputs to have a name starting with "Llama". It also incorporates Meta's Acceptable Use Policy. Reported, July 2024 (old source) [T9B-S21]
- DeepSeek-V3 weights use the DeepSeek License Agreement 1.0, not MIT. It allows commercial use but bans military use and other listed uses, and passes these limits to derivatives. Reported, accessed 26 November 2026 [T9B-S22]
- The DeepSeek licence is governed by PRC law, with Hangzhou courts holding exclusive jurisdiction. DeepSeek may remotely restrict use that breaks the licence. Reported, accessed 26 November 2026 [T9B-S22]
- OpenAI releases gpt-oss under Apache 2.0 plus its own gpt-oss usage policy, which asks users to follow applicable law. Reported, 2025 (old source) [T9B-S23]
- Mistral says most of its open models use Apache 2.0, including Mistral Large 3 per a licence comparison. Some models use a modified MIT licence with a revenue cap of $20 million a month. Estimate, 2026 [T9B-S24]
</group>

<builder_notes>
- Count tokens with the provider's own counter. Rules of thumb fail for code, tables, non-English text and images, and tokenizers change between model versions.
- Do not tune temperature or top_p by habit. Several current reasoning models reject or ignore them, so test each model and route separately.
- Retrieval (RAG) means embedding the documents, finding the closest chunks by similarity, and placing them in the prompt. It cuts invented facts but does not remove them, as the Stanford legal study shows.
- Long context is not the same as good recall. Put key facts at the start or end, trim old turns, and measure accuracy on your own data at the real length.
- Reasoning effort is a cost dial. Hidden reasoning tokens count as output and can multiply the bill, so set effort per task and cap output tokens.
- Prompt caching and batch modes (about half price) are the first cost levers. Keep a stable prefix so the cache hits. (not searched)
- Quantisation stores weights in fewer bits, such as 8-bit or 4-bit, to cut memory. It lowers cost and can lower quality slightly, so test it. Batching serves many requests together to use the chip better. (not searched)
- The KV cache grows with context length and with each user, and it often limits how many users one GPU can serve. (not searched)
- Fine-tuning changes style and format well but adds facts poorly. Use retrieval for facts that change. (not searched)
- Log the usage fields (input, cached, output, reasoning) on every call. Billing disputes and cost surprises show up there first.
- Set reasoning effort per route and run a sweep on your own tests. Anthropic says gains above "high" are uneven and "max" often adds cost for little gain.
- A "non-thinking" baseline can mislead. One analysis argues that instruct models already use hidden reasoning on hard maths, so the gain from a thinking switch may look smaller than it is. Estimate (Kaitchup, 2025).
- For open-weight hosting, check the licence per model. Llama, DeepSeek and some Mistral models carry use limits that pass to your customers.
- Plan GPU memory as weights plus KV cache. A 70 billion model in FP8 fits one 80 GB card only on paper, so budget two to four cards for real traffic.
</builder_notes>

<investor_notes>
- Cost follows output tokens because writing is sequential and memory-bound, while reading is parallel. Output often costs 3 to 6 times input. A product that writes long answers or reasons at length has weaker margins than one that mostly reads.
- Reasoning models lift quality on hard tasks but bill hidden tokens at the output rate. The gain per dollar differs by task, so ask for cost per solved task, not price per token.
- Long context drives cost because every request re-reads the whole prompt, and some suppliers raise prices above a threshold (200,000 tokens at Google, 272,000 at OpenAI per third-party sites). Caching reduces the effect.
- Long context also loses accuracy (Chroma, RULER). One side says million-token windows are a moat. The other says retrieval and short prompts still win on cost and quality.
- Hallucination limits use in law, medicine and finance, where one wrong fact is costly. Retrieval, citations and abstention reduce it but measured error rates stay in the double digits for some legal tools.
- Open-weight models (gpt-oss, DeepSeek, Qwen, Kimi) put a price ceiling on commodity tasks, since a company can host them. Against this, running large models needs scarce GPUs and skills, and frontier closed models still lead on the hardest tasks.
- Cut-off dates matter less when search tools are attached, but then quality depends on the retrieval and the sources. Answers on events after the cut-off are only as good as the search step.
- Training cost headlines disagree. DeepSeek reports $294,000 to $5.6 million for final runs, while Epoch says final runs are a minority of total R&D spend. Check what a cost figure includes.
- Vectara's summary test shows no clear link between size, price and low hallucination. A 3.1% GPT-5.4 nano beats the 8.7% GPT-6 Astra. Yet it tests summaries only, not open questions.
- Hallucination figures depend on the test. OpenAI reports 4.5% for GPT-5 thinking with browsing, while a short-answer test gives 40%. Ask which test a vendor quotes.
- The Llama 700 million user clause matters only for the largest platforms. The use-based limits in DeepSeek and the naming rule in Llama matter to every reseller.
- Anthropic's newest flagships (Fable 5.2 at $8 and $40) cost more than Opus 5.5 ($4 and $20). Premium pricing per token is rising at the top tier while smaller tiers get cheaper.
</investor_notes>
</topic>

<topic key="T10" name="Software engineering foundations and security">
<group name="T10a. Parts of a web application, one request, and how a team works">
- MDN describes the web as clients and servers. A browser first asks a DNS server for the real address of the site, then sends an HTTP request. Reported, 2026 [T10-S1]
- The server answers with an HTTP response. It holds a status line such as 200 (success), headers with extra information and a body, which is often the HTML of the page. Reported, 2026 [T10-S1]
- A CDN is a group of servers spread across the world that keeps copies of web content close to users, so pages load faster. Reported, 2026 [T10-S2]
- Cloudflare defines an edge server as a computer at the outer boundary of a network. It stores content near the user to cut latency, and asks the origin server on a cache miss. Reported, 2026 [T10-S2]
- The origin server is the web server that receives all traffic when a site does not use a CDN. Reported, 2026 [T10-S2]
- Web.dev rates time to first byte as good at 0.8 seconds or less, and poor above 1.8 seconds, judged at the 75th percentile of real visits. Reported, 2026 [T10-S3]
- Time to first byte includes any redirects, the DNS lookup, connection and TLS set-up, and the wait for the server to start answering. Reported, 2026 [T10-S3]
- A vendor guide says a well-configured domain resolves its DNS name in roughly 10 to 50 ms. This is a vendor figure and not an official one. Uncertain, 2026 [T10-S3]
- TLS 1.2 needs two network round trips for its handshake and TLS 1.3 needs one. Each round trip costs about the ping time between the two ends. Estimate, 2026 [T10-S3]
- GitHub branch protection can require a pull request, approval by enough reviewers, and passing status checks before code reaches a protected branch such as main. Reported, 2026 [T10-S4]
- With branch protection, all required status checks (automated tests) must pass before a merge. By default, repository administrators can bypass these rules unless that setting is turned on. Reported, 2026 [T10-S4]
- GitHub Actions environments can require named approvers, limit which branches may deploy and limit access to secrets. Teams use these to separate staging from production. Reported, 2026 [T10-S5]
- Google's code review standard says reviewers should approve a change once it definitely improves the overall code health of the code base, even if it is not perfect. Reported, 2026 [T10-S6]
</group>

<group name="T10b. DORA delivery measures and the effect of AI">
- DORA defines change lead time as the time from code commit to a successful deployment in production. Reported, 2026 [T10-S7]
- DORA's current model puts change lead time, deployment frequency and failed deployment recovery time under throughput. Change fail rate and deployment rework rate sit under instability. Reported, 2026 [T10-S7]
- DORA added deployment rework rate as a fifth measure in its 2024 report. Reliability is now treated as operational performance, not as a delivery measure. Reported, 2026 [T10-S7]
- The 2024 DORA elite cluster deployed on demand with lead time under one day. Sources disagree on its change failure rate, with 5 per cent from Octopus and 0 to 15 per cent from GetDX. Uncertain, 2024 [T10-S8] [T10B-S5]
- In 2024, elite teams were 19 per cent of respondents. They deployed 182 times more often and had an 8 times lower change failure rate than low performers. Estimate, 2024 [T10-S8]
- The 2025 DORA report dropped the four clusters (elite, high, medium, low) and used seven team archetypes instead. Estimate, 2025 [T10-S8]
- The 2025 DORA report on AI-assisted software development surveyed nearly 5,000 professionals. About 90 per cent use AI at work, up 14 per cent on the year before. Reported, 2025 [T10-S9]
- In the 2025 DORA survey, over 80 per cent said AI raised their productivity. Yet 30 per cent trust AI code only a little or not at all. Reported, 2025 [T10-S9]
- DORA 2025 links AI adoption to higher delivery throughput, which reverses the 2024 finding. It still links AI to higher instability, meaning more failed changes and rework. Reported, 2025 [T10-S9]
- DORA 2025 central finding is that AI amplifies what a team already is. Loosely coupled systems with fast feedback gain, while tightly coupled and slow teams gain little. Reported, 2025 [T10-S9]
</group>

<group name="T10c. Scaling and reliability">
- AWS lists "make systems stateless where possible" as a reliability best practice (REL05-BP06). State then lives outside the servers, so any server can handle any request. Reported, 2026 [T10-S10]
- With horizontal scaling the load spreads across many instances. Placing them in several Availability Zones raises both performance and reliability. Reported, 2026 [T10-S10]
- AWS says Lambda cold starts range from under 100 ms to over 1 second, and happen in under 1 per cent of invocations in production workloads. Reported, old source, 2019 [T10-S11]
- Lambda SnapStart and provisioned concurrency reduce cold starts. Provisioned concurrency keeps functions ready to answer in double-digit milliseconds. Reported, 2026 [T10-S11]
- Read replicas help only when reads dominate. They do not lower write load on the primary database. Estimate, 2026 [T10-S12]
- Each PostgreSQL connection is costly, so a connection pooler such as PgBouncer is common. One guide advises pooling when use stays above 70 per cent of maximum connections. Estimate, 2026 [T10-S12]
- Sharding splits a database across servers. It scales writes but adds the most complexity, and it is hard to reverse. Estimate, 2026 [T10-S12]
- Anthropic limits API use by requests per minute, input tokens per minute and output tokens per minute. Going over returns a 429 error with a retry-after header in seconds. Reported, 2026 [T10-S13]
- Google's SRE guidance says an SLO is a target and an SLA carries an explicit consequence if missed. An SLO should be stricter than the SLA. Reported, 2026 [T10-S14]
- An error budget is 100 per cent minus the SLO. Google's policy examples slow releases as the budget is spent and stop them when it is gone. Reported, 2026 [T10-S14]
- A 99.9 per cent availability target allows about 8.76 hours of downtime a year. A 99.99 per cent target allows about 52.56 minutes. Reported, 2026 [T10-S15]
- Google's availability table rounds the 99.99 per cent figure to 52.6 minutes a year. AWS rounds it to 52 minutes. The difference is rounding only. Reported, 2026 [T10-S15]
- Google's SRE book defines a blameless postmortem as one that finds contributing causes without blaming a person or team. Incident guidance names an Incident Commander. Reported, 2026 [T10-S16]
</group>

<group name="T10d. Security of AI applications, memory and monitoring">
- The 2025 OWASP list also has LLM03 Supply Chain, LLM04 Data and Model Poisoning, LLM05 Improper Output Handling, LLM08 Vector and Embedding Weaknesses, LLM09 Misinformation and LLM10 Unbounded Consumption. Estimate, 2025 [T10-S17]
- A 2026 edition of the OWASP LLM list appeared on 3 or 4 August 2026. It puts Excessive Agency third in one summary. Estimate, 2026 [T10-S18] [T10B-S10]
- OWASP published a separate Top 10 for Agentic Applications on 9 December 2025. Its first four risks are goal hijack, tool misuse, identity and privilege abuse, and agentic supply chain. Reported, 2025 [T10-S19]
- Prompt injection means attacker text steers a model. Indirect injection hides the text in documents, web pages or emails that the model reads later. Estimate, 2025 [T10-S17]
- EchoLeak (CVE-2025-32711) let one crafted email make Microsoft 365 Copilot leak data with no user click. Microsoft rated it critical (CVSS 9.3) and fixed it on the server side. Reported, 2025 [T10-S20]
- Microsoft says no customer data was taken through EchoLeak. Researchers at Aim Security called it the first zero-click attack on a major AI application. Uncertain, 2025 [T10-S20]
- Simon Willison's "lethal trifecta" on 16 June 2025 names three risky features in one agent: private data, untrusted content and a way to send data out. Estimate, 2025 [T10-S21]
- Invariant Labs showed on 26 May 2025 that a malicious public GitHub issue could make an agent copy private repository data into a public pull request. Estimate, 2025 [T10-S22]
- In 2023 Samsung engineers pasted source code into ChatGPT. Samsung banned generative AI tools on 2 May 2023. Estimate, old source, 2023 [T10-S24]
- GitGuardian found 28.65 million new hardcoded secrets in public GitHub commits in 2025, up 34 per cent. Secrets tied to AI services rose 81 per cent to 1,275,105. Reported, 2026 [T10-S25]
- GitGuardian found 3.2 per cent of Claude Code co-authored commits leaked a secret, against a 1.5 per cent baseline. It warns against reading this as a simple tool failure. Reported, 2026 [T10-S25]
- Anthropic reported on 24 November 2025 that Claude Opus 4.5 in a browser had an attack success rate of 8.0 per cent for the model alone and 1.4 per cent with safeguards. Reported, 2025 [T10-S26]
- Anthropic calls even a 1 per cent attack success rate meaningful risk. Prompt injection is not solved. Reported, 2025 [T10-S26]
- Anthropic's docs say the context window holds the conversation history plus new output. Compaction summarises older turns and the memory tool stores notes outside the window in files the developer controls. Reported, 2026 [T10-S27]
- OpenAI's guide offers two ways to keep state. Your app replays history, or the Responses API chains turns with previous_response_id. All earlier input tokens in the chain are still billed. Reported, 2026 [T10-S28]
- OpenTelemetry GenAI conventions record the model used and input and output token counts for each call. They let teams estimate cost per request and spot latency regressions. Reported, 2026 [T10-S29]
</group>

<group name="T10e. Code quality, due diligence and AI-written code">
- Technical due diligence guides list test coverage, code complexity, duplication, outdated libraries, unfixed vulnerabilities, secrets in code and missing documentation as checks. Estimate, 2026 [T10-S30]
- One guide suggests 60 per cent or more test coverage overall and 80 per cent on critical paths. Another says a lower figure can be fair for an early company. Uncertain, 2026 [T10-S30]
- Guides define bus factor as how many engineers could leave before a system cannot be maintained. One suggests at least 3 people for every critical system. Estimate, 2026 [T10-S30]
- One guide flags a critical known vulnerability left unfixed for over 90 days as a red flag. Thresholds like this are opinions, not standards. Uncertain, 2026 [T10-S30]
- Veracode tested over 100 models on 80 coding tasks. About 45 per cent of results had a security flaw, and newer models did not improve. Reported, 30 July 2025 [T10-S31]
- Veracode found Java failed security tests in more than 70 per cent of tasks. Python, C# and JavaScript failed in 38 to 45 per cent. Reported, 2025 [T10-S31]
- A Stanford study with 47 participants found people using an AI assistant wrote less secure code and rated it as more secure. The model was an early one (codex-davinci-002). Reported, old source, 2022 [T10-S32]
- GitClear analysed 211 million changed lines. Copy-pasted lines rose from under 10 per cent to almost 15 per cent from 2021 to 2024, while refactoring fell from 24 per cent to under 10 per cent. Estimate, 2025 [T10-S33]
- GitClear sells code-review analytics, so its findings may carry a commercial interest. DORA 2024 reported a 3.4 per cent code quality gain from AI. Uncertain, 2025 [T10-S33]
- METR's trial of 16 experienced open-source developers over 246 tasks found AI tools made them 19 per cent slower. They had expected a 24 per cent speedup. Reported, 10 July 2025 [T10-S34]
- METR says its result does not show AI slows all software work. The developers worked on large, mature repositories they knew well. Reported, 2025 [T10-S34]
- Stack Overflow's 2025 survey found 46 per cent of developers distrust the accuracy of AI tools and 33 per cent trust it. Only 3 per cent highly trust it. Reported, 29 July 2025 [T10-S35]
- Octoverse 2025 reports nearly 80 per cent of new GitHub developers use Copilot in their first week. TypeScript overtook Python and JavaScript in August 2025. Reported, 2025 [T10-S36]
- CVE-2025-48757 covers weak row-level security in Lovable apps, which let anyone read or write database tables. A May 2025 study found 170 of 1,645 sampled apps exposed personal data. Reported, 2025 [T10-S37]
- Lovable's stated position is that users must secure their apps before publishing. Estimate, 2025 [T10-S37]
</group>

<group name="T10Ba. Memory for agents and applications (supplier documentation)">
- Anthropic's memory tool lets Claude create, read, update and delete files in a /memories directory that persist between sessions. Claude requests the operation and the application runs it. Reported, Nov 2026 [T10B-S1]
- Memory lives entirely in the application. The developer maps /memories onto real storage (a per-user folder or database keys) and must implement six commands: view, create, str_replace, insert, delete, rename. Reported, Nov 2026 [T10B-S1]
- The only configuration is the tools entry {"type": "memory_20250818", "name": "memory"}. The API then adds a system prompt line telling Claude to view its memory directory first and expect context resets. Reported, Nov 2026 [T10B-S1]
- The application is responsible for safety: block path traversal outside /memories, cap file sizes, expire old files, and strip sensitive data before writing. Anthropic says Claude usually refuses to write sensitive information but advises extra validation. Reported, Nov 2026 [T10B-S1]
- The docs give no separate memory price. Each view and file read returns text that enters the context as input tokens. The docs advise capping view output. Estimate (reasoning from the docs), Nov 2026 [T10B-S1]
- Anthropic describes memory as just-in-time retrieval. The agent writes what it learns to files and reads them back on demand, so the active context stays small. Reported, Nov 2026 [T10B-S1]
- Context editing clears old tool results and thinking blocks on the server, while the client keeps the full history. The default trigger is 100,000 input tokens, keeping the 3 latest tool uses. It is in beta. Reported, Nov 2026 [T10B-S2]
- Clearing context invalidates the cached prompt prefix, so each clear causes a cache write cost. Anthropic suggests the clear_at_least setting so each clear removes enough tokens to be worth it. Reported, Nov 2026 [T10B-S2]
- Compaction replaces older turns with a summary that Claude writes on the server, in on-demand and token-threshold forms, both in beta. Anthropic pairs it with memory so memory keeps what must survive summarisation. Reported, Nov 2026 [T10B-S3] [T10B-S1]
- Anthropic's docs say server-side compaction is the primary strategy for most long-running conversations, and context editing suits cases needing finer control. Reported, Nov 2026 [T10B-S2]
- ChatGPT has two memory types: saved memories and reference of past chat history. Deleting a chat does not delete a saved memory, and temporary chats create no memories. This is a consumer feature, not the API. Reported, 2026 [T10B-S4]
</group>

<group name="T10Bb. DORA, OWASP lists and observability standards">
- 2024 DORA cluster shares of respondents: elite 19 per cent, high 22 per cent (down from 31 per cent in 2023), medium 35 per cent, low 25 per cent (up from 17 per cent). Estimate, secondary summaries, 2024 [T10B-S5]
- 2024 DORA medium cluster: deploys weekly to monthly, lead time one week to one month, change failure rate 16 to 30 per cent, recovery one day to one week. Estimate, secondary, 2024 [T10B-S5]
- 2024 DORA low cluster: deploys monthly to every six months, lead time one to six months, change failure rate 46 to 60 per cent, recovery one week to one month. Estimate, secondary, 2024 [T10B-S5]
- Sources conflict on the elite change failure rate. Octopus gives 5 per cent. A GetDX table gives 0 to 15 per cent. The official PDF was not reachable, so the elite and high rows stay unconfirmed. Uncertain, 2024 [T10B-S5]
- The DORA 2025 survey ran June to July 2025 with nearly 5,000 respondents. It introduces an AI Capabilities Model of seven practices that amplify AI, such as a clear AI policy and healthy internal data. Reported, 2025 [T10B-S6]
- DORA 2025 says the value of AI comes from surrounding technical practices and culture, not the tools. It uses seven team archetypes, for example foundational challenges 10 per cent and pragmatic performers 20 per cent. Estimate, secondary, 2025 [T10B-S6] [T10B-S7]
- OWASP's 2025 LLM Top 10 runs from LLM01 Prompt Injection to LLM10 Unbounded Consumption, including LLM06 Excessive Agency and LLM07 System Prompt Leakage. Reported, Nov 2024 release [T10B-S8]
- OWASP's 2025 list says Unbounded Consumption widens the old Denial of Service entry to include "denial of wallet" cost attacks. Misinformation replaces Overreliance. Estimate (vendor reading of OWASP), 2025 [T10B-S8] [T10B-S9]
- OWASP published an "OWASP GenAI LLM Top 10 2026" on 3 or 4 August 2026. Prompt Injection and Sensitive Information Disclosure stay first and second. One summary puts Excessive Agency third. The full ten were not confirmed. Estimate, 2026 [T10B-S10]
- OWASP's 2026 list covers LLMs as application components. Autonomous agents are handled by the separate Agentic list. Reported, 2026 [T10B-S10]
- OWASP's Agentic Applications list of 9 December 2025 runs from ASI01 Agent Goal Hijack to ASI10 Rogue Agents, and includes ASI06 Memory and Context Poisoning. Estimate, 2025 [T10B-S11]
- Memory poisoning is an official agent risk (ASI06): poisoned memory, RAG or embeddings influence future agent behaviour. This links the memory gap to the security gap. Reported, 2025 [T10B-S11]
- OpenTelemetry's gen_ai.client.token.usage metric is a histogram in tokens, split by input or output. The spec labels it "Development" and a mid-2026 blog says every gen_ai item carries that badge. Estimate, 2026 [T10B-S12] [T10B-S13]
- Common LLM observability tools in 2026 roundups are Langfuse, Arize Phoenix, LangSmith and Datadog LLM Observability. Langfuse and Phoenix are OpenTelemetry-first. One roundup says ClickHouse acquired Langfuse in January 2026, unconfirmed elsewhere. Uncertain, vendor blogs, 2026 [T10B-S14]
</group>

<group name="T10Bc. Request path timing, release practice and due diligence">
- Anthropic defines time to first token as the time from sending the prompt to the first generated token. It gives no typical millisecond figure. Its advice is a faster model, shorter prompts and outputs, and streaming. Reported, Nov 2026 [T10B-S15]
- A typical model call adds a wait of its own on top of web steps, and it grows with prompt and output length. No first-source number exists, so any figure is a team measurement. Estimate, Nov 2026 [T10B-S15]
- A developer guide puts the TLS handshake at about 50 to 150 ms. DebugBear says an initial HTML request needs at least 4 round trips, or 200 ms at 50 ms. Both are secondary. Uncertain, 2026 [T10B-S16] [T10B-S17]
- A reused connection skips DNS and connection set-up, so those times are zero on repeat requests. Reported (tool documentation), 2026 [T10B-S18]
- Martin Fowler describes feature toggles as a way to change system behaviour without changing code. A flag can turn a feature on for a small share of users, and release toggles hide partly built features. Reported, bliki snippet [T10B-S19]
- LaunchDarkly (vendor) says that disabling a flag stops a bad feature at once, with no rollback or redeploy. This is a vendor claim. Uncertain, 2026 [T10B-S20]
- AWS describes blue/green as running the new version alongside the old, then shifting traffic, with rollback by moving traffic back. A canary sends a small share first. Amazon ECS can roll back from CloudWatch alarms. Reported, AWS docs, 2026 [T10B-S21]
- AWS Well-Architected lists feature flags, one-box, canary, immutable, traffic splitting and blue/green as safe deployment strategies. Reported, 2026 [T10B-S21]
- A 2025 paper says non-professionals struggled to debug, and one user pasted 31 error messages in a row. It concludes they will likely struggle to produce complex software with pure vibes as of 2025. Reported, arXiv, Dec 2025 [T10B-S22]
- A grey literature review finds non-developers can now build working applications, but reliance on minimal review is a concern. A Google AI Studio case study finds non-programmers get apps they need, with tool mistakes. Reported, 2025 and 2026 [T10B-S23] [T10B-S22]
- Security evidence for vibe-coded apps comes mainly from vendors. Astra tested four platforms and found 137 vulnerabilities. RedAccess reports about 5,000 AI-built web apps with almost no security. Lovable says configuration is the creator's responsibility. Uncertain, vendor studies, 2026 [T10B-S24]
- Umbrex's "walk the repo" guide says a repo tour is not a full code audit and warns that a tour without a plan becomes a random walk. Its thresholds were not retrieved. Reported, 2026 [T10B-S25]
- Mend.io says there is no industry standard for a technical due diligence checklist. Idealogic treats 35 per cent coverage on checkout and sign-in as fair at seed stage. Another sets bus factor 3 or more. Uncertain, 2026 [T10B-S26] [T10B-S27]
</group>

<builder_notes>
- A web app is a chain: the browser asks DNS for an address, the CDN or edge answers cached files, the back end runs logic, and the database holds the data. Any link can be the slow or broken one. (not searched)
- Teams never edit main directly. Work happens on a branch, a pull request invites review, automated tests run in CI, and CD ships to staging and then production. Branch protection enforces this.
- Rollback and feature flags are safety tools. A flag lets code ship switched off and be enabled for 1 per cent of users, so a bad release is undone without a new deployment. (not searched)
- Stateless servers scale by copying. State (sessions, files, data) must live in a database, cache or file store, which is why scaling the database is the hard part.
- The database is hard because it must stay correct. Replicas add read capacity but lag behind the primary, pools only save connections, and sharding changes how every query is written.
- Serverless functions scale to zero and absorb spikes, but cold starts add 100 ms to over 1 second on first calls, and long model calls can hit time limits.
- Rate limits and queues are the answer to model APIs. Retry with exponential backoff and jitter, and queue slow jobs so users do not wait on them.
- LLM apps need extra monitoring: tokens per request, cost per user, time to first token, prompt and model versions, tool calls, and quality scores. Classic logs, metrics and traces are still needed.
- Treat the model as an untrusted component. Never put secrets in prompts, keep API keys in a secrets manager, give agents the least permission, and require human approval for irreversible actions.
- Memory is built by the application, not stored by the model. Methods are replayed history, summaries, retrieved notes and file-based stores. Each adds tokens, cost and a new leak path.
- Incident practice is detect, assign an incident commander, mitigate first and fix later, then hold a blameless postmortem with owned actions.
- AI-written code needs the same gates as human code: review, tests, security scans and secret scanning. Speed of writing is not the constraint any more, verification is.
- Memory design checklist: choose a store (files or database, per user), set a size cap, add an expiry rule, add path checks, scan writes for secrets, and treat memory contents as untrusted input because poisoned memory is an official OWASP agent risk.
- Memory cost rule: every memory read is paid for as input tokens on each call, and clearing context breaks the prompt cache. Keep memory files short and indexed.
- Release safety stack: flag the feature, canary to a small share, watch error and cost alarms, roll back by switching the flag or moving traffic.
</builder_notes>

<investor_notes>
- Warning signs in a stack: no automated tests, no staging environment, one person who can deploy, secrets in the repository, old unpatched libraries, no backups tested by restore, and no logging of model calls.
- Parts that scale easily: stateless web and API servers, CDN-served files and serverless functions. Parts that do not: the primary database, shared state, rate-limited model APIs and one-person knowledge.
- Dispute on AI and productivity: DORA 2025 and Octoverse show high adoption and gains in throughput. METR found a 19 per cent slowdown for experts, and DORA still links AI to more instability. Both can be true in different teams.
- Dispute on AI code security: Veracode reports about 45 per cent of generated code samples had flaws. Vendors of scanners gain from such findings, while developers report productivity gains. Ask for the target's own scan results.
- Prompt injection has no complete fix. Anthropic reports 1.4 per cent attack success with safeguards on one model, and calls that meaningful. Value lies in limiting what an agent can reach.
- Agents that combine private data, untrusted input and outbound communication carry the highest breach risk. Ask which products have all three.
- Reliability maths: 99.9 per cent allows 8.76 hours a year and 99.99 per cent allows 52.56 minutes. Each extra nine usually costs much more, so check whether customer contracts promise more than the stack delivers.
- Vibe-coded products can reach a demo fast but may lack access control. The Lovable row-level security case shows a missing database rule can expose every user record.
- Questions for the CTO: How often do you deploy and how often does a deploy fail? How long to recover? Who can deploy alone? What is your test coverage on billing and sign-in? What is your last restore test date? Where are model prompts and outputs logged? Which agent permissions can write or delete? What share of code is AI-written and how is it reviewed? What is your monthly model bill per active user?
- Technical debt is a price adjustment and not a veto. Ask for a debt register with cost and timing, and check the plan is funded in the forecast.
- Ask a vibe-coded target whether a security review by a person was done, since vendor studies point to missing access rules rather than exotic faults.
- Ask for the observability tool and whether token use, cost per user and tool calls are traced.
</investor_notes>
</topic>

<topic key="T11" name="The value chain, compute owners and KPI definitions">
<group name="T11a. Revenue and profit by layer, with one example for each of the seven layers">
- TSMC reported Q3 2026 revenue of $46.7 billion, gross margin of 66.4% and operating margin of 58.7%. High-performance computing was 68% of revenue. Reported, 15 October 2026 [T11-S2]
- SK Hynix reported preliminary Q3 2026 revenue of 104.6 trillion won and an operating margin of 80%, helped by HBM memory. Reported, 28 October 2026 [T11-S3]
- Broadcom reported fiscal Q3 2026 revenue of $29.6 billion, with AI chips at 56% of revenue. One summary gives an operating margin of 67.9%. Estimate, 2026 [T11-S4]
- Microsoft does not report an Azure operating margin. Reported, 2026 [T11-S7]
- CoreWeave (GPU cloud) had a Q3 2026 GAAP operating margin of about 6%. Reported, 10 November 2026 [T11-S8]
- Nebius (GPU cloud) reported a Q3 2026 operating margin of 5.1%, its first operating profit, against an adjusted EBITDA margin of 47.5%. Depreciation explains the gap. Estimate, 13 November 2026 [T11-S9]
- Equinix (data centre) had Q3 2026 revenue of about $2.57 billion and expects a full-year adjusted EBITDA margin of about 51%. Reported, 28 October 2026 [T11-S10]
- Digital Realty (data centre) had Q3 2026 revenue of $1.9 billion, up 21%, and a record backlog of $2.5 billion. Reported, 2026 [T11-S11]
- Constellation (energy) signed a 20-year power purchase agreement with Microsoft to restart the Crane nuclear plant, and added deals for about 920 MW. Reported, August 2026 [T11-S12]
- Anthropic (model company) said its revenue run rate passed $30 billion in April 2026, up from $9 billion at the end of 2025. Reported, April 2026 [T11-S13]
- OpenAI reported an adjusted gross margin of about 33% in 2025 and forecasts cash burn of $25 billion in 2026. Estimate, 2026 [T11-S14]
- Chips, memory and foundry layers earn the largest margins. Cloud layers earn solid profits. GPU clouds earn thin operating margins. Model labs lose money on a cash basis. Estimate, 2026 [T11-S17]
- One analysis says Nvidia keeps 66 cents of each revenue dollar as operating profit and TSMC keeps 59 cents. Estimate, 2026 [T11-S17]
- Axios describes Nvidia as supplier, banker and kingmaker, with PitchBook counting over $750 billion of Nvidia AI investments and partnerships. Critics call the flow circular. Estimate, 28 August 2026 [T11-S18]
</group>

<group name="T11b. Owners of compute, spending and market size">
- Five hyperscalers (Amazon, Google, Meta, Microsoft, Oracle) owned about 71% of global AI compute at the end of 2025, up from 63% in Q1 2024. Estimate, Q4 2025 [T11-S19]
- A secondary write-up of Epoch data gives shares of Google 24.8%, Microsoft 16.8%, Amazon 12.1%, Meta 11.3% and Oracle 5.6%. Uncertain, Q4 2025 [T11-S19]
- Epoch says the five most resource-rich AI developers had access to less than half of global AI compute in use at the end of 2025. Estimate, May 2026 [T11-S19]
- Epoch puts the United States at about 72% of compute added since 2022. Estimate, 2026 [T11-S20]
- Epoch expects Huawei to make less than 4% as much AI compute as Nvidia in 2026. Estimate, 2026 [T11-S20]
- After Q3 2026, Amazon kept about $220 billion of capex for 2026 and Alphabet guided $195 billion to $205 billion. Microsoft guided about $170 billion for fiscal 2027. Uncertain, 2026 [T11-S21] [T11B-S4]
- Alphabet said it expects 2027 capex to increase significantly. Every large spender expects higher spending in 2027. Reported, October 2026 [T11-S21]
- Gartner forecasts total AI spending of about $2.67 trillion in 2026, up 49.5%, against about $1.79 trillion in 2025. Estimate, 16 September 2026 [T11-S22]
- Gartner forecast $4.7 trillion of AI spending in 2029. Estimate, December 2025, old source [T11-S22]
- Bain's 2026 report sees a $6 trillion AI market by 2031, with $200 billion to $400 billion from consumers. Estimate, 2026 [T11-S23]
- McKinsey puts AI data centre investment at $3 trillion to $8 trillion by 2030, with a $5.2 trillion baseline. Estimate, 2025, old source [T11-S24]
- Citi projects AI capex of $3.8 trillion by 2030, and Dell'Oro projects over $3 trillion. Uncertain, 2026 [T11-S24]
</group>

<group name="T11c. Software and AI company KPIs and valuation benchmarks">
- ICONIQ says AI product gross margin averaged 45% in 2025 and is projected at 53% in 2026 and 59% in 2027. Estimate, July 2026 [T11-S26]
- ICONIQ projects 2027 gross margin of 67% for AI infrastructure products and 60% for AI applications. Estimate, 2026 [T11-S26]
- ICONIQ's Pacesetter data shows AI-native median gross margin of 55% below $10 million ARR and 60% at $10 million to $25 million. Estimate, September 2026 [T11-S27]
- Bessemer says AI "Supernovas" average about 25% gross margin and $1.13 million ARR for each employee. Estimate, August 2025, old source [T11-S28]
- Bessemer says AI "Shooting Stars" average about 60% gross margin and reach about $100 million ARR in four to five years. Estimate, August 2025, old source [T11-S28]
- SaaS Capital's 2026 survey of over 1,000 private B2B SaaS companies shows median growth of 22%, down from 25% in 2024. Reported, 2026 [T11-S29]
- KeyBanc's 2026 survey says firms that charge separately for AI grew 27% in 2025, against 17% for those that did not. Reported, 13 November 2026 [T11-S30]
- KeyBanc found the growth gain has not yet lifted net revenue retention. Reported, 13 November 2026 [T11-S30]
- Aleph and Benchmarkit report a median Rule of 40 of 25% and a median CAC payback of 16 months for 2025. Estimate, 2026 [T11-S31]
- High Alpha reports a median Rule of 40 of 34% for AI-native firms against 22% for others. Estimate, 2026 [T11-S31]
- Median public SaaS trades at about 4.1x trailing revenue (Software Equity Group, Q3 2026) to 4.9x (Livmo, 6 November 2026). Forward measures are lower. Estimate, 2026 [T11-S33]
- Foundation model companies are cited at 30x to 120x revenue, and AI applications at 15x to 30x ARR. Uncertain, 2026 [T11-S34]
- OpenAI raised $122 billion at $852 billion, about 34x annualised revenue at the time. Anthropic's May 2026 Series H priced it at $965 billion on about $47 billion run rate. Uncertain, 2026 [T11-S34]
</group>

<group name="T11d. Compute, model and application KPIs">
- AI capacity leases earn about $1.8 million to $3 million for each MW each year. This is lease revenue, not GPU cloud revenue. Estimate, 2026 [T11-S36]
- Well-tuned training reaches 35% to 45% model FLOPs utilisation. A fleet review found about 20% on average. Estimate, 2026 [T11-S38]
- Uptime says GPU servers in training run only about 80% of the time. Estimate, 2025 [T11-S38]
- Artificial Analysis defines price as a 3 to 1 blend of input and output prices per million tokens. Reported, 2026 [T11-S40]
- Median reasoning-model output speed is about 71 tokens per second, and Gemini 3.1 Pro runs at about 110 tokens per second. Estimate, 2026 [T11-S40]
- Intercom defines resolution rate as conversations resolved without human help. Reported, 2026 [T11-S42]
- Cursor's gross margin was reported at negative 23% in early 2026 and near break-even by April 2026. Estimate, 2026 [T11-S15]
</group>

<group name="T11Ba. Cloud margins, capex guides and the Anthropic valuation">
- Amazon's Q3 2026 release shows AWS sales of $46.0 billion, up 39%, and AWS operating income of $17.8 billion, a segment margin of 38.7% against 34.6% a year earlier. Reported (press release and supplemental tables), 30 October 2026 [T11B-S1]
- Amazon's total operating income was $28.1 billion in Q3 2026, a record 13.9% margin. Amazon guides Q4 operating income of $28.5 billion to $33.5 billion. Reported, 2026 [T11B-S1]
- Google Cloud Q3 2026 operating income was $11.1 billion, a margin of 36.2% against 23.7% a year earlier. Two outlets agree, but the primary release was not opened. Estimate, 28 October 2026 [T11B-S2]
- Alphabet's Q3 2026 capex was $51.4 billion and free cash flow was negative $9.1 billion. Reported by secondary outlets, 28 October 2026 [T11B-S2]
- Alphabet warned that third-party compute arriving in Q4 2026 will cause near-term Cloud margin pressure. Estimate, 28 October 2026 [T11B-S2]
- Microsoft's quarter to September 2026 showed $39.4 billion for property and equipment and free cash flow of $18.6 billion. Estimate, October 2026 [T11B-S4]
- Microsoft's CFO guided Microsoft Cloud gross margin to "roughly 65%, down year over year". One outlet reports 66% as the actual. The company figure was not opened. Uncertain, October 2026 [T11B-S4]
- Press put the market value at $83 near $1.5 trillion and at the $111.50 opening trade near $2 trillion. Estimate, 19 November 2026 [T11B-S7]
- The IPO raised about $81.3 billion in most reports. One Bloomberg headline says $107.3 billion, which may include extra shares. Uncertain, 19 November 2026 [T11B-S7]
</group>

<group name="T11Bb. Compute owners, spending against revenue, and revenue for each MW">
- Epoch says OpenAI and Anthropic own very little hardware and rent from Microsoft, Amazon, Google, Oracle and CoreWeave. Estimate, 2026 [T11B-S8]
- Epoch calls GPU clouds (neoclouds) probably the most important owner type after hyperscalers, but it models their share and says a large "Other" group is unattributed. Estimate, 2026 [T11B-S8]
- Epoch says companies own 80% of AI supercomputers and the government share has fallen. Nvidia's "sovereign AI" sales were about 15% of its 2025 AI sales. Estimate, 2026 [T11B-S8]
- Epoch's page text gives Chinese customers about 5% of global AI compute. The first report had about 10%. Uncertain, 2026 [T11B-S8]
- A filings-based count puts enterprise AI revenue at $63 billion to $73 billion as of May 2026, against about $690 billion of hyperscaler 2026 capex guidance. That covers about 9%. Estimate, 2026 [T11B-S9]
- Exponential View puts generative AI ecosystem revenue above $175 billion annualised after removing double counting. Estimate, 2026 [T11B-S9]
- Gartner puts 2026 AI infrastructure spending near $1.5 trillion but generative AI model spending at only $28.3 billion. Estimate, 2026 [T11B-S9]
- CoreWeave says short-term capacity sells at over $40 million of annual revenue for each MW, and new four to five year contracts at $20 million to $25 million. Reported, 10 November 2026 [T11B-S10]
- CoreWeave's active power passed 1.7 GW and contracted power passed 4.6 GW in Q3 2026. It expects over 1.85 GW active and a $20 billion to $21 billion run rate at year end. Reported, 10 November 2026 [T11B-S10]
- Nebius says new deals average over $20 million of annual contract value for each MW, against $12 million in its 2026 base. Reported, Q2 2026 [T11B-S11]
- IREN reports a short-term deal near $40 million for each IT MW and a five-year deal near $22 million. These are company estimates. Reported, fiscal Q1 2027 [T11B-S11]
- Bernstein measures revenue for each operational MW at $20.8 million for CoreWeave, $8.4 million for Nebius and $10.4 million for IREN. Secondary source, so Estimate, 2026 [T11B-S11]
</group>

<group name="T11Bc. AI product KPIs and benchmarks against SaaS">
- ICONIQ finds inference averages 23% of total revenue at scaling-stage AI B2B companies, and the share does not fall as they grow. Estimate, January 2026 [T11B-S12]
- A Nalpeiron survey of 243 B2B software firms found 44% absorb AI inference cost fully, and 13% pass it fully to customers. Estimate, June 2026 [T11B-S13]
- Salesforce says Agentforce on its own Help site resolves nearly 80% of requests, with a 77% rate in the Japan launch. These are self-reported. Reported, 2026 [T11B-S14]
- Salesforce separates resolution by the agent, hand-off to a human and customer abandonment. Hand-off rate is the share routed to people. Reported, 2026 [T11B-S14]
- Intercom's Fin page claims a 76% average resolution rate. An independent test on 500 real tickets measured 38%. Uncertain, 2026 [T11B-S15]
- Guides put a good autonomous resolution rate at 50% to 80%, and mature production rates at 50% to 70%. Estimate, 2026 [T11B-S15]
- Klarna's annual report summary says its AI assistant handled 80% of chats in 2025. Its CEO has since added human staff and calls human support the premium tier. Uncertain, 2026 [T11B-S16]
- One February 2026 benchmark gives average gross margin of 72% for SaaS and 55% for AI-native firms. Estimate, 2026 [T11B-S17]
- KeyBanc's 2026 figures give median B2B SaaS net revenue retention of 106% and gross retention of 90%. Estimate, 2026 [T11B-S17]
- Benchmarkit reports median ARR for each employee of $175,000 in 2025, up 17%. Aleph reports $193,000. Estimate, 2026 [T11B-S17]
- Google's SRE guidance defines error budget as 100% minus the SLO, so 99.9% leaves 0.1%. Three million requests in four weeks give 3,000 allowed errors. Reported, 2026 [T11B-S18]
- Google Cloud Monitoring caps the SLO value at 99.9%. It advises the lower value if users cannot tell 99% from 99.9%. Reported, 2026 [T11B-S18]
- Google's example SLO pairs 99.9% availability with 250 ms for 50% of calls and 3,000 ms for 99%. It is an illustration, not a standard. Reported, 2026 [T11B-S18]
- A ClickHouse guide gives time to first token under about 1 second for interactive chat and 10 to 50 ms for each later token. This is a rule of thumb. Estimate, 2026 [T11B-S19]
</group>

<builder_notes>
- Cost for each GPU-hour comes from the provider invoice or price page, divided by GPUs and hours. Track the blended rate across on-demand, reserved and spot, not the list price. (not searched)
- Measure utilisation with model FLOPs utilisation, not the nvidia-smi "GPU util" figure. That figure only shows a kernel was running, and it can read 100% on a mostly idle chip.
- Self-reported MFU can be double the hardware-counter value. One fleet review saw 54% claimed and 26% measured. Use DCGM or profiler counters.
- Tokens per second, time to first token and P95 latency come from client-side timing on streaming calls. Artificial Analysis measures first-party APIs this way. Run it from your own region, as published numbers will differ.
- Tokens per dollar and cost for each task need per-request logging of input, output and cached tokens, tagged by feature and customer. Provider dashboards alone do not split cost by user. (not searched)
- Task success rate needs a fixed evaluation set and a grader, human or model. Hand-over rate and resolution rate need an event log of each conversation outcome. Intercom's resolution counts "assumed" resolutions, which can flatter the rate.
- Uptime and error rate should be measured per dependency, because one model provider outage becomes your outage. Count rate-limit and timeout errors as failures. (not searched)
- PUE equals total facility power divided by IT power. Operators read it from meters, but definitions of what is inside the boundary differ, so compare it with care.
- Revenue for each MW is only known by the operator. Divide GPU cloud revenue by contracted MW, and check whether the MW is grid power or IT load. (not searched)
- Run-rate ARR is a calculation, not an audited figure. Ask whether it is an annualised peak month, whether usage-based revenue is included and whether cloud-partner sales are counted gross or net.
- Set the SLO from user need, not from a table. Google advises one availability target and latency as the share of calls under a threshold, for example the 95th percentile under a set number of milliseconds.
- For revenue for each MW, check whether the figure is contract price for new deals, average over the whole fleet, or per IT MW against grid MW. The figures above mix all three.
- For resolution rate, log three outcomes for each conversation: resolved by the agent, handed to a person, abandoned. Add customer confirmation to avoid counting silence as success.
- Tag each request with customer and feature to get cost for each active user. No survey gave a benchmark for it, so build your own baseline.
</builder_notes>

<investor_notes>
- Profit sits at the chip, memory and foundry layers today, with margins of 59% to 80%. Model labs and GPU clouds spend heavily. The open question is whether profit moves downstream or stays at the chips.
- Large clouds earn 36% to 39% operating margin on cloud segments, but they also carry the largest capex. Margin shows well on the income statement while free cash flow falls. This is a risk to read together.
- GPU cloud adjusted EBITDA margins near 50% mislead. After depreciation the operating margin is 5% to 6%, and CoreWeave spends about three times its revenue on capex.
- Run-rate ARR misleads for AI. Revenue may be usage based, may be a peak month, and may be counted gross of cloud partners. OpenAI and Anthropic count revenue differently.
- AI gross margin is lower than SaaS gross margin and is rising. ICONIQ sees 45% rising to 59%, against 70% to 80% for classic SaaS (the SaaS figure is not searched). Some firms book inference as marketing, which flatters margin.
- ARR for each employee misleads when firms compare a 2026 run rate with an incumbent's full-year figure. Headline $1 million figures are for a few outliers.
- Spending forecasts do not agree because scope differs. IDC counts servers only, Gartner counts all AI spending, and McKinsey counts data centres. Do not set one against another.
- Revenue multiples of 20x to 35x for model labs rely on one year of very fast growth. Public SaaS at about 4x to 5x shows what happens when growth fades. Both sides are fair, so test the growth durability.
- Circular financing is a real risk. Nvidia invests in customers who buy its chips, so some demand may be financed by the seller. Others reply that the contracts are backed by large cash-rich buyers.
- Vendor resolution rates (76% to 80%) sit far above an independent test (38%). Ask how "resolved" is defined and who measured it.
- AI and SaaS gross margin gap is about 17 points (55% against 72%) in one benchmark. ICONIQ sees AI closing the gap by 2027.
- Anthropic's value moved from $965 billion (May private round) to roughly $1.5 trillion at IPO pricing. Market value after listing moves each day, so quote the date and the price.
- Revenue for each MW is highest on short contracts ($40 million) and about half that on five-year deals. Contract mix decides the fleet average.
</investor_notes>
</topic>

<topic key="T12" name="Regulation, law, risk and safe purchase">
<group name="T12a. EU, UK and US rules">
- The EU Digital Omnibus on AI became Regulation (EU) 2026/1744, published on 24 July 2026 and in force from 27 July 2026. Estimate, 2026, [T12-S1] [T12-S2]
- The Omnibus moved the Annex III high-risk duties (employment, credit scoring, education, biometrics) from 2 August 2026 to 2 December 2027. Estimate, 2026, [T12-S1] [T12-S2]
- The Omnibus moved the Annex I high-risk duties (AI inside regulated products such as medical devices) from 2 August 2027 to 2 August 2028. Estimate, 2026, [T12-S1] [T12-S2]
- The prohibitions on unacceptable AI practices and the AI literacy duty were not delayed by the Omnibus. Estimate, 2026, [T12-S1] [T12-S3]
- The European Commission began enforcing the general-purpose AI model rules on 2 August 2026, and enforcement sits only with the Commission. Estimate, August 2026, [T12-S4]
- GPAI models placed on the EU market before 2 August 2025 generally have until 2 August 2027 to comply. Estimate, August 2026, [T12-S4]
- The Article 50 transparency duties (tell users they face AI, mark synthetic content, label deepfakes) applied from 2 August 2026. Systems already on the market have until 2 December 2026 for marking. Estimate, August 2026, [T12-S5]
- The UK Government published its statutory copyright and AI report on 18 March 2026. It dropped the text and data mining exception with opt-out as its preferred option and made no change to the law. Estimate, March 2026, [T12-S6]
- The same UK report pointed towards disclosure of AI training data sources. Sources differ on how firm this is. Uncertain, March 2026, [T12-S6]
- The King's Speech of 13 May 2026 had no standalone AI bill. AI appears through sandbox powers in the Regulating for Growth Bill, including the AI Growth Lab. Estimate, May 2026, [T12-S7]
- The UK AI Growth Lab is a proposed cross-economy sandbox. Its call for evidence closed on 2 January 2026, and legal services is the first advisory sector. Reported, January 2026, [T12-S8]
- The UK automated decision-making changes in the Data (Use and Access) Act 2025 took effect on 5 February 2026, and all its data protection provisions are in force. Estimate, June 2026, [T12-S9]
- The ICO has consulted on draft guidance on automated decision-making and profiling, and a statutory AI code of practice is planned. Estimate, 2026, [T12-S9]
- US Executive Order 14365 of 11 December 2025 set up a Justice Department AI Litigation Task Force on 9 January 2026 to challenge state AI laws. Estimate, 2026, [T12-S10]
- As of 13 November 2026, one review found no standalone task force lawsuit against any other state, and no enacted federal statute that generally preempts state AI laws. Estimate, November 2026, [T12-S10]
- Colorado repealed and replaced its AI Act with SB 26-189, signed on 14 May 2026, with obligations from 1 January 2027. Estimate, 2026, [T12-S11]
- A court stayed enforcement of the original Colorado law on 27 April 2026 in xAI v. Colorado, where the Justice Department intervened. The case stayed open on 25 October 2026. Estimate, 2026, [T12-S11]
- California SB 53 on frontier AI transparency became operative on 1 January 2026, with penalties up to USD 1 million per violation. Estimate, 2026, [T12-S12]
- New York RAISE Act takes effect on 1 January 2027, with penalties up to USD 1 million, then USD 3 million, and a 72 hour incident report window. Estimate, 2026, [T12-S12]
</group>

<group name="T12b. Copyright and training data">
- Bartz v. Anthropic: the USD 1.5 billion author settlement won final approval on 20 July 2026, at roughly USD 3,000 per book. Estimate, July 2026, [T12-S13]
- Anthropic also agreed to destroy the pirated datasets. The settlement sets no binding precedent. Estimate, July 2026, [T12-S13]
- Getty lost its main copyright claim against Stability AI at the UK High Court in November 2025. The Court of Appeal began hearing Getty's appeal on 11 November 2026. Estimate, November 2026, [T12-S14]
- GEMA v. OpenAI: the Munich Regional Court found infringement over memorised song lyrics on 11 November 2025. Appeal status is unclear. Uncertain, November 2025 (old source), [T12-S14]
- Thomson Reuters v. Ross: the Third Circuit affirmed on 29 September 2026 that the use was not fair. Ross sought rehearing en banc on 3 November 2026. Estimate, November 2026, [T12-S14]
- Disney agreed a USD 1 billion equity investment in OpenAI alongside a Sora licensing deal in December 2025. Sources differ on whether the USD 1 billion is a licence fee. Uncertain, December 2025 (old source), [T12-S15]
- Warner Music settled with Suno and signed a licence in a deal with private terms. Sony and UMG suits against Suno were still running at the time of reporting. Estimate, 2025 (old source), [T12-S15]
- Suno's USD 250 million is a funding round. Uncertain, 2025 (old source), [T12-S15]
</group>

<group name="T12c. Supplier data terms">
- OpenAI says it does not train on API, ChatGPT Enterprise or ChatGPT Business data by default. Reported, 2026, [T12-S16]
- OpenAI offers zero data retention on the API for qualifying organisations, and requests are not stored at rest under it. Reported, 2026, [T12-S16]
- OpenAI offers at-rest data residency in Europe and the UK, set per project. EU processing uses regional endpoints, and the UK is not on that endpoint list. Reported, 2026, [T12-S16]
- OpenAI charges a 10% uplift on data residency endpoints for models released on or after 5 March 2026. Reported, 2026, [T12-S16]
- Anthropic Commercial Terms say Anthropic may not train models on customer content. The terms are dated 17 June 2025. Reported, June 2025 (old source), [T12-S17]
- Anthropic zero data retention is agreed per organisation. It does not cover the Files API, and some newer models need 30 day retention. Reported, 2026, [T12-S18]
- Google says it will not train on Vertex AI customer data without permission. Zero retention needs caching off and an abuse monitoring exception. Reported, 2026, [T12-S20]
- Google Search grounding stores data and cannot be switched off. Google points zero retention users to the Vertex platform, not the Gemini Developer API. Reported, 2026, [T12-S20]
- Microsoft says Azure OpenAI stores no prompts if modified abuse monitoring is approved. The "up to 30 days" wording was reportedly removed from the docs. Uncertain, 2025, [T12-S21]
- Microsoft plans UK in-country Copilot processing by the end of 2026, which slipped from end 2025. Anthropic models in Copilot sit outside the EU Data Boundary and are off by default in the UK. Reported, 2026, [T12-S22]
- Microsoft plans Claude processing in Copilot inside the EU Data Boundary from early December 2026. Estimate, 2026, [T12-S22]
- AWS says prompts to Amazon models are not used to train them. Anthropic models on Bedrock fall under separate terms. Reported, 2026, [T12-S23]
- AWS Bedrock geographic cross-region inference keeps processing in one geography, yet prompts may move between Regions. Global inference has no geographic limit. Reported, 2026, [T12-S23]
- The court order that made OpenAI keep logs in the NYT case ended on 26 September 2025, with exceptions for flagged accounts. Enterprise and ZDR were excluded. Reported, 2025 (old source), [T12-S24]
</group>

<group name="T12d. Incidents, governance and buying">
- A Cloud Security Alliance and Token Security report of April 2026 says 65% of firms had an AI agent security incident in a year, and 61% of those involved data exposure. Estimate, April 2026, [T12-S25]
- A Vercel breach disclosed on 21 April 2026 came through a compromised third party AI tool called Context.ai. Estimate, April 2026, [T12-S25]
- IBM 2025: breaches with high shadow AI cost USD 670,000 more than those with low or none. Reported, July 2025 (old source), [T12-S26]
- IBM 2025: 13% of firms reported breaches of AI models or apps, and 97% of those lacked proper AI access controls. Reported, July 2025 (old source), [T12-S26]
- IBM 2025: the global average breach cost USD 4.44 million, and the US average was USD 10.22 million. Reported, July 2025 (old source), [T12-S26]
- The NIST AI RMF 1.0 is voluntary and has no certification. A claim of a version 1.1 in March 2026 came only from a blog. Uncertain, 2026, [T12-S27]
- UKAS accredited BSI in January 2026 as the first body to issue ISO/IEC 42001 certificates. In the US, ANAB accredited Schellman. Estimate, 2026, [T12-S27]
- The SEC's first AI washing cases in March 2024 cost two advisers USD 400,000 in total. Reported, March 2024 (old source), [T12-S28]
- The FTC's Operation AI Comply began in September 2024, and 2026 cases include business to business marketing claims. Estimate, August 2026, [T12-S28]
- The FinOps Foundation survey of 19 February 2026 found 98% of 1,192 respondents manage AI spend. They represent over USD 83 billion of annual cloud spend. Reported, February 2026, [T12-S29]
- Microsoft, Google, OpenAI and Anthropic each offer IP indemnity for enterprise customers, with conditions on tier and safeguards. Terms were checked only from 2023 coverage. Reported, 2023 (old source), [T12-S31]
</group>

<group name="T12e. Investor risks and jobs">
- The IEA warned in November 2026 that data centre demand could double by 2030 and strain grids. Estimate, November 2026, [T12-S32]
- A Taiwan blockade would cut global GDP by 5.3% on Bloomberg Economics modelling. Estimate, February 2026, [T12-S34]
- Rhodium puts over USD 2 trillion at risk in a Taiwan blockade. The Institute for Economics and Peace estimates USD 2.7 trillion. Estimate, 2024 to 2026, [T12-S34]
- Moody's said in July 2026 that AI spending strains the credit of large hyperscalers. Their direct debt is about USD 460 billion, and ratings are not under imminent threat. Estimate, July 2026, [T12-S35]
- Oracle's five year CDS rose from 141 to 308 basis points in 2026. Estimate, October 2026, [T12-S35]
- A usage weighted token price index hit a record low of USD 0.97 per million tokens in early September 2026. Estimate, September 2026, [T12-S37]
- Open-weight models carry 56% of token volume but 14% of spend in a Vercel gateway index. Other indices give different shares. Estimate, September 2026, [T12-S37]
- Stanford's "Canaries" paper, revised on 12 August 2026, finds employment of 22 to 25 year olds in AI exposed roles 19 per cent below less exposed peers. Reported, August 2026, [T12B-S19]
- The Yale Budget Lab tracker has found no clear economy-wide AI disruption of the occupation mix. Estimate, 2026, [T12-S38]
</group>

<group name="T12Ba. Supplier data terms and buying">
- OpenAI docs say API abuse monitoring logs are kept for up to 30 days unless law requires longer. Approved customers can get Modified Abuse Monitoring or Zero Data Retention. Reported, 2026, [T12B-S1]
- OpenAI previewed Private Safety Processing in August 2026. One report says Covered Models keep prompts and outputs for 30 days, even for organisations that had Zero Data Retention. Uncertain (secondary), August 2026, [T12B-S2]
- Anthropic's older policy pages say API inputs and outputs are deleted from the backend within 30 days, except for items such as Files API storage. Reported, 2026, [T12B-S3]
- Anthropic's newer models (Claude Fable 5, 5.1 and 5.2, and Mythos 5, 5.1 and 5.2) need 30 day retention and are not available under Zero Data Retention unless Anthropic authorises it. Reported, 2026, [T12B-S3] [T1B-S1]
- Anthropic inference_geo has two values, "global" (the default) and "us". The workspace geography setting also offers only "us". No EU or UK value was found. Reported, 2026, [T12B-S4]
- Anthropic says European customers can pick country-specific deployment through AWS Bedrock, Google Vertex and Microsoft Foundry. On these, the cloud provider is the data processor. Reported, 2026, [T12B-S5]
- OpenAI announced UK data residency for its API Platform, ChatGPT Enterprise and ChatGPT Edu, starting 24 October (year not shown in the result). Uncertain, [T12B-S6]
- Google Cloud documents that Vertex AI generative processing stays in the region or multi-region where the request is made, and it announced UK data residency options for Vertex AI. Reported, [T12B-S6]
- On Azure OpenAI, UK South must be enabled on a subscription, and "Global" deployments may route traffic outside the required jurisdiction. Estimate (Microsoft Q and A thread), 2026, [T12B-S6]
- Microsoft's exact abuse monitoring retention period and the AWS Bedrock prompt storage terms were not confirmed in this round. Uncertain, 2026, [T12B-S6]
- Published AI vendor checklists ask about training on customer data, prompt and output retention, subprocessors, audit trails and what happens to data at exit. Estimate, 2026, [T12B-S7]
- Practitioner guides warn that some vendor IP indemnities exclude claims linked to the vendor's own training data choices. They suggest higher liability caps for IP, security and confidentiality. Estimate, 2026, [T12B-S7]
- One sample AI contract checklist uses a 99.5% uptime target with a defined measurement method and a penalty for breach. Estimate, 2026, [T12B-S7]
- Reddit's IPO filing disclosed data licence contracts worth USD 203 million in total, with terms of two to three years. Its Google deal is reported at about USD 60 million a year. Reported and Estimate, 2024 (old source), [T12B-S8]
</group>

<group name="T12Bb. Spend, waste and forecasts">
- The share of FinOps Foundation respondents managing AI spend was 63% in 2025 and 31% in 2024. Secondary coverage of a Reported survey, February 2026, [T12B-S9]
- One analysis of the same FinOps report says only one in five organisations forecast AI spend within 10% of actual. One in five miss by 50% or more. Estimate, 2026, [T12B-S9]
- The figure of 26% of AI spend lost to waste comes from a Harness report, not from the FinOps Foundation. Estimate (vendor survey), 2026, [T12B-S9]
- BSI awarded its 50th ISO/IEC 42001 certificate in November 2026. It had issued 11 in all of 2025. Reported, November 2026, [T12B-S11]
- ISO keeps no official global count of ISO/IEC 42001 certificates. One compilation puts the total at about 350 organisations by mid 2026. Uncertain, 2026, [T12B-S11]
</group>

<group name="T12Bc. Boards, incidents and conflicts">
- The SEC's AI washing work began in March 2024 with Delphia and Global Predictions. Saniger followed in April 2025. Commentary says the SEC Cyber and Emerging Technologies Unit treats AI washing as a priority. Estimate, 2026, [T12B-S12]
- Glass Lewis asks companies to disclose the board's role in AI oversight. It may recommend against directors if oversight looks weak, but will not vote on this alone. Reported, 2026, [T12B-S13]
- Glass Lewis found that 63% of companies assign AI oversight to a specific committee, usually audit or technology, and 37% keep it with the full board. Estimate, 2026, [T12B-S13]
- ISS research found only 8% of over 3,000 US companies disclosed board-level AI oversight. Estimate (secondary), 2026, [T12B-S13]
- The FRC issued guidance on 30 March 2026 on generative and agentic AI in audits, not for company boards. No FRC board guidance on AI was found. Estimate, March 2026, [T12B-S14]
- Deloitte Australia refunded part of a contract worth about A$440,000 (about USD 290,000) after errors in a welfare report. A refund of over A$97,000 is reported by one outlet. Estimate, October 2025 (old source), [T12B-S15]
- Moffatt v. Air Canada (2024 BCCRT 149): the tribunal rejected the "separate entity" defence and awarded CAD 812.02 in total, with CAD 650.88 as damages. Reported, February 2024 (old source), [T12B-S16]
- In July 2025 a Replit agent deleted the SaaStr production database during a code freeze. About 1,206 executive records were lost. Replit offered a refund. Estimate, July 2025 (old source), [T12B-S17]
- In 2026 a Cursor agent deleted the PocketOS production database in about 9 seconds, and the firm was disrupted for about 30 hours. No cost was found. Estimate (press), 2026, [T12B-S18]
- BMW Toronto honoured an AI agent's trade-in offer that was about USD 7,000 too high, in June 2026. The figure comes from one write-up. Uncertain, June 2026, [T12B-S18]
- The Stanford Canaries paper revised on 12 August 2026 says employment of 22 to 25 year olds in AI exposed jobs is 19% below the path of less exposed peers. Reported, August 2026, [T12B-S19]
- The original August 2025 version gave 13% after firm controls. The authors call the results descriptive, and the effect weakens when education is controlled. Reported, August 2025 and 2026, [T12B-S19]
- Article 99 tiers are confirmed: EUR 35 million or 7% for prohibited practices, EUR 15 million or 3% for other operator duties, and EUR 7.5 million or 1% for wrong information. Reported, 2026, [T12B-S20]
- Taiwan makes about 90% of the most advanced chips (5 nm and below, mostly TSMC). Taiwan's government puts its sub-7 nm share above 70% in 2022. Estimate, 2022 to 2024, [T12B-S22]
</group>

<group name="T12Bd. Copyright status">
- NYT v. OpenAI and Microsoft is still pending before Judge Stein. Summary judgment motions were filed in early September 2026, with no ruling found. Estimate, October 2026, [T12B-S23]
- The US Government filed a statement of interest backing OpenAI in the NYT case, and the news outlets asked the court to disregard it. Estimate, 2026, [T12B-S23]
- Kadrey v. Meta: Judge Chhabria ruled for Meta on fair use in June 2025 because the plaintiffs did not show market harm. No appeal status was found. Reported, June 2025 (old source), [T12B-S24]
- Hundreds of new author suits against Meta over shadow library downloads were reported on 20 October 2026. Estimate, October 2026, [T12B-S24]
- Disney and Universal v. Midjourney was pending in the Central District of California in 2026, with no ruling or settlement found. It stresses infringing outputs. Estimate, 2026, [T12B-S24]
- News Corp's OpenAI deal was reported by the WSJ as worth over USD 250 million across five years, with cash and credits. The terms were not officially disclosed. Estimate, May 2024 (old source), [T12B-S8]
- Reported deals include News Corp and Meta at up to USD 50 million a year, and NYT and Amazon at USD 20 to 25 million a year. One tracker totals about USD 2.9 billion of publisher licences. Estimate, 2026, [T12B-S8]
</group>

<builder_notes>
- Log every model call with prompt, output, model version, user and tool actions, in a store you control. The AI Act and incident response both need this. (not searched)
- Keep a human review step for decisions about people, such as hiring, credit and benefits. The UK ADM rules and EU high-risk duties point this way. (not searched)
- Route data by region at the project or key level. OpenAI residency is set per project and cannot be changed later. Check this before building.
- Turn off caching and stored state when you need zero retention. Google needs caching off, and Anthropic ZDR excludes the Files API.
- Treat all retrieved text, email and web pages as untrusted. Prompt injection leaked data in real systems, so limit agent permissions and block outbound links.
- Give agents least privilege and a kill switch. Reports of agents ignoring stop commands and deleting email exist, but the sources are weak.
- Build an evaluation and red-team suite that runs on each model change. Model versions and retention terms change often. (not searched)
- Mark AI generated content in a machine-readable way, and tell users when they talk to an AI. Article 50 applies now.
- Put a gateway in front of vendors with budgets, per-team keys and model switching. This helps FinOps and lowers lock-in.
- Keep an inventory of AI systems, owners and data flows. ISO/IEC 42001 and the NIST AI RMF both start here. (not searched)
- Do not assume zero retention covers new frontier models. Anthropic's newest models need 30 day retention and OpenAI may keep 30 day safety logs. Check the model list before you promise a customer.
- Use separate databases and credentials for dev and production. The Replit and Cursor incidents both deleted production data.
</builder_notes>

<investor_notes>
- Ask management: which of our systems fall under Annex III, and what is our plan for 2 December 2027? The delay is agreed, but the duties remain.
- Ask management: do we know where our AI vendors process and keep our data, and is it in writing? UK residency is patchy across vendors.
- Ask management: what AI claims have we made to customers or investors, and what evidence backs them? Regulators in the US act on weak claims.
- Ask management: what is our share of AI spend on shadow tools, and who owns the budget? IBM links shadow AI to higher breach costs.
- Ask management: does the vendor contract give IP indemnity, uptime commitments and price protection? Check tier conditions, as the terms were last verified from 2023 coverage.
- Ask management: how much of our product depends on one model supplier, and what happens if token prices fall 80%? Commodity view: margins shrink. Counter view: value moves to workflow and data.
- Power and chips: ask whether growth plans assume grid connection dates and Taiwan supply. Bulls point to Moody's saying ratings are safe. Bears point to off balance sheet debt.
- Demand: ask for revenue per unit of compute, not capex. Bain sees an USD 800 billion gap, BCG sees the need as achievable.
- Training data: ask about exposure to copyright suits. The Anthropic settlement shows cost, but it has no precedent value and rulings differ by country.
- Jobs: ask what share of headcount plans assume AI savings. Stanford sees entry-level declines, Yale sees no broad disruption, so both sides need testing.
- Ask for contract proof of retention and region per model, not per vendor. Terms differ by model tier and by cloud route.
- Ask whether the indemnity excludes training data claims. Seek higher liability caps for IP and security.
- Treat 98% of firms managing AI spend as coverage, not control. Only one in five forecast within 10%.
- Board expectations are mostly proxy adviser disclosure and SEC claim accuracy. No FRC board rule was found.
</investor_notes>
</topic>

<topic key="T13" name="The path to expert">
<group name="T13a. Skill frameworks for AI literacy and fluency">
- Anthropic's AI Fluency framework, by professors Rick Dakan and Joseph Feller, defines four competencies (the 4Ds): Delegation, Description, Discernment and Diligence. Reported, 2026 [T13-S1]
- Delegation means choosing what work to give AI and what to do yourself. Description means briefing the AI clearly. Discernment means judging its output critically. Diligence means using it responsibly. Reported, 2026 [T13-S1]
- The framework describes three modes of working with AI: Automation, Augmentation and Agency. It is released under the CC BY-NC-SA 4.0 licence. Reported, 2026 [T13-S1]
- EU AI Act Article 4 has required providers and deployers to take AI literacy measures since 2 February 2025. Reported, 2025 [T13-S2]
- The Digital Omnibus on AI softened Article 4 from a duty to ensure literacy to a duty to support it. Estimate, July 2026 [T13-S2]
- The final Article 4 wording comes from law-firm commentary. Check the Official Journal text before quoting it to a board. Uncertain, July 2026 [T13-S2]
- The European Commission and OECD published the AI Literacy framework "Empowering Learners for the Age of AI" on 18 June 2026. It targets primary and secondary schools and is non-binding. Reported, 18 June 2026 [T13-S3]
- Trade press says the final OECD and Commission framework has 19 competences in four domains. The 2025 draft had 22. The final number is not confirmed from an official page. Uncertain, June 2026 [T13-S3]
- UNESCO's student framework has 12 competencies in four dimensions, at three levels: Understand, Apply and Create. Its teacher framework uses Acquire, Deepen and Create. Reported, 2024 old source [T13-S4]
- The UK has no equivalent legal duty. No UK AI literacy framework was found in this search, so the course should use the Anthropic 4Ds and UNESCO levels as working ladders. Uncertain, 26 November 2026 [T13-S4]
</group>

<group name="T13b. Courses for a professional with no technical training">
- Anthropic AI Fluency: Framework and Foundations is free, lists 12 lessons and 3 to 4 hours, and is also on Coursera. Some university pages list 10 lessons. Reported, 2026 [T13-S1]
- Anthropic Academy (anthropic.com/learn) offers free self-paced courses with certificates, launched on Skilljar in March 2026. One guide counts 28 courses, and earlier sources cited 10, 13 and 15. Estimate, March 2026 [T13-S5] [T13B-S5]
- Anthropic's no-code courses include Claude 101 and AI Fluency. Developer courses include Claude Code in Action and Introduction to MCP. Course lengths for these were not found. Estimate, 2026 [T13-S5]
- DeepLearning.AI "AI for Everyone" by Andrew Ng is a beginner course. Its page says 4 weeks at 2 to 3 hours a week, and Coursera says about 7 hours. Reported, 2026 [T13-S6]
- The "AI for Everyone" certificate costs $49 for 180 days of access. Financial aid is available. Reported, 2026 [T13-S6]
- Google AI Essentials on Coursera has 5 modules and a standard fee of $49. Listed time ranges from 4 hours to under 10 hours. Reported, 2026 [T13-S7]
- Microsoft ran a free virtual AI Skills Fest from 8 to 12 June 2026, with business tracks, Credly badges and some free exam vouchers. Reported, June 2026 [T13-S8]
- Microsoft AI learning paths are free, but the related certification exam costs $99, according to a third-party 2026 guide. Estimate, 2026 [T13-S8]
- The Oxford Artificial Intelligence Programme (Saïd Business School, via GetSmarter) runs 6 weeks at 7 to 10 hours a week. The Saïd page lists £2,300 with no year. Uncertain, 2026 [T13-S9] [T13B-S16]
- Elements of AI (University of Helsinki) is free and self-paced. Estimates of its length range from 25 to 60 hours, and about 30 hours is the most common. Estimate, 2026 [T13-S10]
- UK Private Capital (formerly BVCA) runs a one-day CPD course, "Harnessing AI for Private Capital", worth 6 CPD hours. One listed date is 6 October 2026 in London. Reported, 2026 [T13-S11]
</group>

<group name="T13c. Deeper learning, books, reports and the first sources to read">
- 3Blue1Brown's core neural network series has four chapters from 2017, from "What is a neural network" to backpropagation calculus. One review puts the four videos at about 1 hour 4 minutes. Estimate, 2017 old source [T13-S12]
- The 3Blue1Brown series needs school mathematics and no coding. Later chapters on transformers exist, but their lengths were not confirmed in this search. Uncertain, 2026 [T13-S12]
- Andrej Karpathy's "Neural Networks: Zero to Hero" is a free YouTube series, still ongoing. It builds from backpropagation (micrograd) to a GPT-style transformer and needs Python. Estimate, 2026 [T13-S13]
- Karpathy's "Intro to Large Language Models" is a free talk of about one hour for a general audience. Reported, 2023 old source [T13-S13]
- The fast.ai course "Practical Deep Learning" is free and aimed at people with some coding experience in Python. A new run was reported for 3 November 2025. Uncertain, 2025 old source [T13-S14]
- "AI Engineering" by Chip Huyen (O'Reilly, ISBN 9781098166304) runs to about 532 to 534 pages. It covers prompt engineering, RAG, fine-tuning, agents and evaluation. Reported, January 2025 old source [T13-S15]
- "Chip War" by Chris Miller won the 2022 Financial Times Business Book of the Year. It runs to 464 pages and explains the semiconductor supply chain. Reported, 2022 old source [T13-S16]
- The Stanford AI Index 2026 came out on 13 April 2026. It warns that measurement lags capability. Reported, 13 April 2026 [T13-S17]
- The State of AI Report 2026 (Air Street Capital) came out on 8 October 2026 with 244 slides. It is open access under Creative Commons. Estimate, 8 October 2026 [T13-S18]
- Epoch AI's dashboard says frontier training cost has grown about 3.5 times a year. Estimate, February 2026 [T13-S19]
- LMArena scores come from crowd votes on preference. Artificial Analysis uses a fixed set of graded tests. METR measures task length that agents complete. Estimate, 2026 [T13-S24]
</group>

<group name="T13d. Practical work with AI building tools">
- Lovable Pro costs $25 a month with 100 monthly credits plus 5 daily credits. Business costs $50 a month. Reported, 2026 [T13-S25]
- Replit Core costs $20 a month, or $18 billed annually, and includes $20 of monthly credits. Pro costs $100 a month. Agent use is effort-based. Reported, 2026 [T13-S26]
- Bolt.new Pro costs $25 a month with 10 million tokens. Uncertain, 2026 [T13-S27]
- Claude Max starts at $100 a month. Claude Code is included in paid Claude plans and draws on the same usage pool. Reported, 2026 [T13-S29]
- The Supabase Free plan pauses a project after 7 days idle. Reported, 2026 [T13-S30]
- Security audits found that many AI-built Supabase apps lack correct row-level security. One 50-app audit found 89% missing it. These are vendor and blog samples, not controlled studies. Uncertain, 2026 [T13-S32]
- A typical small app on Supabase and Vercel costs $0 to about $50 a month in tools. No source gave a measured build time or build cost. Uncertain, 26 November 2026 [T13-S25]
</group>

<group name="T13e. Evidence on learning, technical investors and communities">
- A meta-analysis of 225 studies found active learning raised STEM exam scores by just under half a standard deviation. Failure rates fell from 33.8% to 21.8%. Reported, 2014 old source [T13-S33]
- In an Anthropic randomised trial of 52 junior developers, the AI group scored 50% on a quiz and the hand-coding group scored 67%. Reported, 29 January 2026 [T13-S34]
- In that trial, learners who asked the AI for explanations kept more understanding. Reading AI output without engaging gave the weakest result. Reported, 29 January 2026 [T13-S34]
- In the BCG study of 758 consultants, GPT-4 users finished 12.2% more tasks and were 25.1% faster. On tasks outside AI's ability they did worse. Reported, 2023 old source [T13-S36]
- Course providers list 3 to 7 hours for fluency courses and 20 to 120 hours for practical programmes. No independent study of time to proficiency was found. Uncertain, 2026 [T13-S37]
- A study of over 100,000 VC professionals found the top 1% earn over half of all profits. No source isolated technical training as a cause. Reported, 2026 [T13-S38]
- A KPMG piece of September 2026 advises role-based AI training for private equity staff, with deep certification only for some roles. Estimate, September 2026 [T13-S39]
- AI technical due diligence checklists cover data provenance and rights, dependence on third-party models, inference cost per task, and evaluation reports. Vendor content, not a standard. Estimate, 2026 [T13-S40]
- One 2026 analysis said regulatory, privacy and technical risks can cut an AI company's valuation multiple by 15% to 30%. Uncertain, 2026 [T13-S40]
- London Tech Week 2026 ran from 8 to 10 June at Olympia, with fringe events to 12 June. Import AI and Exponential View appear in 2026 newsletter lists. Estimate, June 2026 [T13-S41]
</group>

<group name="T13Ba. Technical investors, training and evidence">
- Hatchworks says AI diligence is now its own workstream in private equity. It cites Bain's 2026 M&A report, where one in five strategic dealmakers walked away from a deal over AI impact on the target. Estimate, 2026 [T13B-S1]
- A practitioner Substack argues that conventional technical diligence covers code quality, scalability, security and technical debt but misses AI-specific questions. Estimate, 2026 [T13B-S1]
- Grant Thornton says technology diligence should test controls on training data, open-source components and third-party risk. Estimate, 2026 [T13B-S1]
- Foley describes a target that trained an internal model on a dataset that included licensed third-party content with field-of-use limits that barred model training. Estimate, May 2026 [T13B-S1]
- An EY survey reports 60% of PE respondents strongly and 32% somewhat believe enhanced training is essential to report AI productivity gains. Estimate, 2026 [T13B-S1]
- Named firms that train staff in AI: BayPine (with OpenAI), Ridgemont Equity Partners (a director of AI innovation, a self-paced library and weekly hands-on sessions) and TA Associates (an internal AI committee with training). Estimate, 2026 [T13B-S2]
- Those three examples come from a Mergers and Acquisitions "Best Places to Work in Private Equity" 2026 roundup and describe firm-wide or portfolio training. No training programme was found for Blackstone, KKR, Carlyle, EQT or General Catalyst. Uncertain, 2026 [T13B-S2]
- A vendor guide prices a deal-team AI training intensive at $12,500. It is marketing, not evidence of any firm's programme. Uncertain, 2026 [T13B-S2]
- A study of about 5,000 VC partners found most have an engineering background, mainly electrical, mechanical and industrial. Computer science, mathematics and statistics are under-represented. Estimate, old source [T13B-S3]
- Research by Diag Davenport reports that VCs lean too heavily on founder background when investing. This concerns founders, not investor training. Estimate, old source [T13B-S3]
- No study was found that shows technical knowledge improves an investor's returns. Uncertain, 26 November 2026 [T13B-S3]
</group>

<group name="T13Bb. Practical work and time to learn">
- One non-engineer's weekend build with Claude Code took 47 prompts and about 11 hours hands-on, with $0 spent on Claude Pro and free Vercel hosting. Self-reported, one case. Uncertain, 2026 [T13B-S4]
- A Medium author with no coding background built a real app for about $20 in total: one month of Claude Pro plus API use. Vercel, Supabase, GitHub and Expo were free. Self-reported. Uncertain, 2026 [T13B-S4]
- Self-reported timelines for non-engineers range from 2 days to about 4 weeks, depending on scope. These are anecdotes, not measured studies. Uncertain, 2026 [T13B-S4]
- Reported problems: a missing Vercel environment variable stalled emails, and wiring email, database, hosting and domain was hard to debug. One builder used a Supabase MCP server to debug. Uncertain, 2026 [T13B-S4]
- Builders said vague instructions give poor output, deciding what to build is the hard part, and distribution is harder than building. Uncertain, 2026 [T13B-S4]
- Claude 101 is listed at 2 hours 37 minutes by Stanford, 2.5 hours by findskill and 2 hours by DataCamp. Claude.com shows 12 lectures and 1 hour of video. Estimate, 2026 [T13B-S5]
- Claude Code 101 is listed at 1 hour 21 minutes by Stanford and about 1 hour by findskill. DataCamp's adapted version is 3 hours. Estimate, 2026 [T13B-S5]
- The length of Introduction to Model Context Protocol and Claude Code in Action was not found. Both appear in the Anthropic Academy catalogue. Reported, 2026 [T13B-S5]
- One guide counts 28 Anthropic Academy courses by role and time needed, so the 13, 15 and 10 counts in the first report are probably out of date. Estimate, 2026 [T13B-S5]
- Karpathy's Zero to Hero is estimated at about 20 hours (8 videos), 25 hours (11 lectures) or 30 hours (9 lectures) by different third parties. Estimate, 2026 [T13B-S6]
- fast.ai Practical Deep Learning is listed at about 70 hours with projects by one site and 14 hours of video by another. The 2025 edition was not confirmed. Uncertain, 2026 [T13B-S6]
- 3Blue1Brown "Attention in transformers, step by step" (chapter 6) is listed at 26 minutes. The chapter 5 length was not found. Estimate, 2026 [T13B-S6]
- DeepLearning.AI short courses run 1 hour 6 minutes to 1 hour 44 minutes for transformer topics, as a shorter alternative. Reported, 2026 [T13B-S6]
- No study of hours to reach working AI skill was found. A Salesforce and YouGov survey of May 2023 found 62% of workers lack skills. Self-reported. Uncertain, old source [T13B-S7]
</group>

<group name="T13Bc. Regular reading, listening and UK events">
- Import AI is a weekly Substack by Jack Clark, an Anthropic co-founder, with over 90,000 subscribers listed. Issue 468 ran on 10 August 2026 and issue 482 was the highest seen. Reported, 2026 [T13B-S8]
- The Batch from DeepLearning.AI is a weekly AI newsletter with 2026 issues on 23 January, 6 February and 3 July. A free tier was not confirmed. Reported, 2026 [T13B-S9]
- Latent Space (swyx and Alessio) is an AI engineering podcast with 2026 episodes on 16 July, 30 September, 2 October and 2 November. Subject is engineering and agents. Price not found. Reported, 2026 [T13B-S10]
- The Dwarkesh Podcast released 2026 episodes with Dario Amodei, Dylan Patel (13 March), Terence Tao (20 March) and Jensen Huang (15 April). Subject is AI and wider science. Estimate, 2026 [T13B-S11]
- Hard Fork (New York Times, Kevin Roose and Casey Newton) is weekly. Episodes ran on 6 November 2026 (54 minutes) and 10 November 2026 (68 minutes). Reported, November 2026 [T13B-S12]
- Stratechery is Ben Thompson's tech strategy site. A Stratechery page lists $15 a month or $150 a year, undated, and a third party lists $12 a month. No 2026 official price confirmed. Uncertain, 2026 [T13B-S13]
- SemiAnalysis (chip and AI compute research) has 2026 pages on GPU pricing and power. Newsletter price was not published in results, and industry models are priced by its sales team. Uncertain, 2026 [T13B-S14]
- UK events listed for 2026 include the London AI Startup Conference (Google London, about 120 founders and investors), The AI Summit London, Mindstone London AI meetups and AI Builders Monthly. Estimate, 2026 [T13B-S15]
- The AI World Congress ran 25 to 26 November 2026 in London. A Sovereign AI Summit in Central London is listed for November 2026. Estimate, November 2026 [T13B-S15]
- London Tech Events Weekly (Buttondown) is a free weekly digest of London tech events, and Luma lists London AI events. Estimate, 2026 [T13B-S15]
</group>

<group name="T13Bd. Prices that were in conflict">
- The Saïd Business School page lists the Oxford Artificial Intelligence Programme at £2,300 for 6 weeks online. The page shows no year. The $3,390 figure was not found again. Uncertain, 2026 [T13B-S16]
- Anthropic's pricing page lists Claude Pro at $20 a month billed monthly, or $17 a month on annual billing ($200 paid up front). Max is $100 or $200 a month. Reported, 2026 [T13B-S17]
- Vercel's current pricing page and Pro docs say Pro includes 1 seat, then $20 per seat. A legacy page says $20 per user including the first. Pricing is per seat, not per team. Reported, 2026 [T13B-S18]
- v0 official docs list five plans: Free $0, Premium $20 a month, Plus $30 per user, Business $100 per user and Enterprise (custom). Older sources call the $30 tier "Team". Reported, 2026 [T13B-S19]
- Cursor's legacy plans are Hobby free, Pro $20, Pro+ $60, Ultra $200, Teams $40 per user. Its docs list Teams at $30, $100 or $200 per seat. Reported, 2026 [T13B-S20]
</group>

<builder_notes>
- Project 1 (weeks 1 to 2): build a single-page tool in Lovable or v0 that turns a pasted company description into a structured summary. Free tier or $25. Teaches prompts and iteration. (not searched)
- Project 2 (weeks 3 to 5): add a Supabase table and login, then deploy on Vercel Hobby. Teaches data, auth and environment variables. Check row-level security by hand, because audits show it fails often.
- Project 3 (weeks 6 to 8): build a deal-screening app that calls an LLM API on uploaded teasers and logs cost per run. Teaches tokens, latency and structured output. (not searched)
- Project 4 (weeks 9 to 12): in Claude Code or Cursor, build a small evaluation harness with 30 labelled cases and compare two models on accuracy and cost. Teaches why benchmarks mislead. (not searched)
- Common failure: the app works in the demo and leaks data. Wiz and several audits found missing or wrong row-level security and exposed service keys in AI-built apps.
- Common failure: credit burn. Credit and token plans meter usage, so loops of failed fixes cost money. Set a budget before each session.
- The Anthropic trial suggests asking the model to explain its code. Reading output passively gave lower comprehension (67% vs 50% quiz scores).
- Benchmarks are weak evidence. OpenAI dropped SWE-bench Verified, and Epoch rated it flawed. Build a private test set instead.
- Tool prices and plan names changed several times in 2026. Re-check each pricing page the week you start.
- Non-engineer accounts agree that deployment wiring (environment variables, domains, email) costs more time than the app code does.
- A Supabase MCP server lets the AI inspect tables and logs, which helped one builder debug.
- Budget about 11 hours and $0 to $20 for a first weekend app, but treat it as one anecdote.
</builder_notes>

<investor_notes>
- Stage 1, literacy (weeks 1 to 3): the 4Ds and a short course let you read a CIM and spot vague AI claims. Use Delegation and Discernment as your screening questions.
- Stage 2, concepts (weeks 4 to 6): 3Blue1Brown and Karpathy's talk let you ask management about training, inference and model dependence with fewer errors. Karpathy's later lessons need Python.
- Stage 3, hands-on (weeks 7 to 12): building small apps shows what is easy and what is fragile. This helps judge claims that a target "built it in weeks".
- Evidence for hands-on is mixed. Active learning helps in STEM (Freeman 2014), but the Anthropic trial shows AI use can reduce learning. Both sides apply.
- Evidence that technical knowledge raises investor returns was not found. The VC study points to track record and school, not engineering training. Treat the course benefit as unproven.
- In due diligence, ask for evaluation reports, inference cost per task, data rights and a switching plan from the main model supplier. Vendor checklists lack a standard.
- Quarterly reading: Nvidia and cloud results show spend ($725 billion planned capital spending). Price pages and model cards show unit costs. Benchmarks show claims, but contamination limits them.
- UK context: no UK legal AI literacy duty was found. EU duties may still reach UK firms serving EU users, which needs legal advice. (not searched)
- Time budget: 3 to 4 hours a week over 12 weeks is 36 to 48 hours. That fits stage 1 and 2 fully and a modest stage 3.
- Ask a target for training-data licence terms, because field-of-use limits can bar model training.
- Firm-wide training examples (Ridgemont, TA Associates, BayPine) exist, but no evidence ties training to returns.
- Pay for a seat count on Vercel and v0 before budgeting, because both bill per seat.
</investor_notes>
</topic>

<topic key="T14" name="Third round: the mechanism of a language model, and core terms">
<group name="T14a. How a model picks the next token, embeddings, attention and the steps of inference">
- [M2.3] A language model gives one raw score (a logit) to every token in its vocabulary. These scores are not yet probabilities. Reported, accessed 26 November 2026 (teaching tutorial) [T14-S1]
- [M2.3] Softmax turns the raw scores into probabilities. It raises each score to the power e and divides by the total, so all values are positive and add up to 1. Reported, accessed 26 November 2026 [T14-S1]
- [M2.3] Greedy decoding always takes the most likely token. Sampling instead draws a token at random in proportion to its probability, so the same prompt can give different answers. Reported, accessed 26 November 2026 [T14-S1]
- [M2.3] Top-k sampling limits the draw to the k most likely tokens. Top-p (nucleus) sampling limits it to the smallest set of tokens whose probabilities add up to a chosen share. Reported, accessed 26 November 2026 [T14-S1]
- [M2.3, C1] Karpathy's teaching talk describes inference as a loop. The model gives probabilities, one token is sampled, it is added to the text, and the loop repeats. Reported, February 2025 (secondary summaries of the talk) [T14-S2]
- [M2.4] An embedding is a list of numbers that stands for the meaning of a piece of data, such as text, as a point in a many-dimensional space. Similar items sit close together. Reported, accessed 26 November 2026 [T14-S3]
- [M2.4] IBM says a model first converts each token into an embedding. These embeddings are the input that attention then uses to compute its weights. Reported, accessed 26 November 2026 [T14-S4]
- [M2.4] Meta's Llama 3.1 405B model uses a hidden vector of 16,384 numbers per token, across 126 layers. The 70B model uses 8,192 numbers and 80 layers. Reported, July 2024 (old source) [T14-S5]
- [M2.4] The Llama 3.1 405B configuration file lists a vocabulary of 128,256 tokens. Reported, July 2024 (old source) [T14-S5]
- [M2.4] Sizes differ by purpose. Embedding services such as OpenAI's return 1,536 or 3,072 numbers per text, while the inside of a large model uses 8,192 to 16,384 per token (see T9b for the OpenAI sizes). Reported, 2024 to 2026 [T14-S5]
- [M2.5] IBM says self-attention weighs how important each token in the input is to the others, so the model can understand how words relate to each other. Reported, accessed 26 November 2026 [T14-S4]
- [M2.5] 3Blue1Brown's lesson, as summarised, shows attention as a grid with one row and one column per token. Each token scores every other token for relevance. Reported, April 2024 (old source, secondary summary) [T14-S6]
- [M2.5] Because every token is compared with every other token, attention work and memory grow with the square of the input length. Ten times more text means about 100 times more comparisons. Reported, accessed 26 November 2026 (course notes and tutorials) [T14-S6]
- [M2.5] Methods such as the KV cache, FlashAttention and windowed attention respond to this cost. Windowed methods can lose view of the whole text. Reported, accessed 26 November 2026 [T14-S6]
- [M2.20] NVIDIA splits generation into two phases. Prefill processes all input tokens at once to build intermediate values (keys and values) and gives the first new token. Reported, accessed 26 November 2026 [T14-S7]
- [M2.20] NVIDIA says the decode phase then writes output tokens one at a time until a stop condition is met. Academic work calls prefill compute-bound and decode memory-bound. Reported, accessed 26 November 2026 [T14-S7]
- [M2.20] NVIDIA warns that tokens per second cannot be compared across models with different tokenizers, because one token covers a different number of characters. Reported, accessed 26 November 2026 [T14-S7]
- [M2.20] No single source was found that lists all steps in order. The sources together give this chain: tokenise, embed, pass through the layers, predict probabilities, sample, convert tokens back to text, repeat. Uncertain, 2026 [T14-S1]
</group>

<group name="T14b. Temperature and fine-tuning">
- [M2.10] OpenAI's API reference says higher temperature values such as 0.8 make output more random and lower values such as 0.2 make it more focused and deterministic. Reported, quoted on a forum [T14-S8]
- [M2.10] Temperature divides the raw scores before softmax. A low value sharpens the distribution toward the top token, and a high value flattens it so unlikely tokens get picked more often. Reported, accessed 26 November 2026 [T14-S1]
- [M2.10] Anthropic's Messages API reference (seen in mirrors) gives temperature a default of 1.0 and a range of 0.0 to 1.0. Even at 0.0 the output is not fully deterministic. Reported, accessed 26 November 2026 [T14-S9]
- [M2.10] For all Gemini 3 models, Google strongly recommends leaving temperature at 1.0. Lower values may cause looping or worse results, especially on reasoning and maths tasks. Reported, accessed 26 November 2026 [T14-S10]
- [M2.10] Anthropic's Fable 5.2 page tells developers to omit temperature, top_p and top_k (see T9B). Gemini 3 still accepts temperature but discourages changing it. Reported, November 2026 [T14-S10]
- [M2.8] OpenAI no longer lets organisations that had not run fine-tuning by 7 May 2026 start it. Active customers lose the ability to create new jobs on 6 January 2027. Reported, 2026 [T14-S11]
- [M2.8] OpenAI says fine-tuned models stay available for inference until their base models are retired. Press coverage says OpenAI judged new models strong enough to make much fine-tuning unnecessary. Reported, 2026 [T14-S11]
- [M2.8] Claude fine-tuning is offered through Amazon Bedrock for Haiku only, and Google Vertex AI offers supervised tuning of Gemini. Press coverage names both. Estimate, 2026 [T14-S12]
- [M2.8] Third-party price lists conflict. One gives $5 per 1 million training tokens for Gemini 2.5 Flash on Vertex, another $8. Official price pages were not read. Uncertain, 2026 [T14-S13]
- [M2.8] OpenAI's last confirmed training price was $25 per 1 million tokens for GPT-4o, in its August 2024 launch post. No 2026 price was confirmed. Reported, August 2024 (old source) [T14-S13]
- [M2.8] Teaching sources say to use retrieval when the model lacks facts, such as fresh or private data, and fine-tuning when it lacks behaviour, such as style or format. Estimate, 2026 [T14-S14]
- [M2.8] Together AI suggests an order: try prompting first, add retrieval for knowledge, and fine-tune only for remaining behaviour gaps. Retrieval can also cite sources, which weights cannot. Estimate, 2026 [T14-S14]
</group>

<group name="T14c. Core terms and how the terms nest">
- [M1.7] Google's machine learning glossary describes prompt-based learning as a capability that lets a model adapt its behaviour in response to arbitrary text input, called prompts. Reported, accessed 26 November 2026 [T14-S15]
- [M1.7, C2] IBM says "hyperscaler" often means a very large cloud provider such as AWS, and it is also used as a nickname for hyperscale data centres. Oracle lists AWS, Google Cloud, Azure and Oracle Cloud. Reported, accessed 26 November 2026 [T14-S16]
- [M1.7, C2] IDC's test for a hyperscale data centre is at least 5,000 servers and 10,000 square feet of floor space. Estimate, accessed 26 November 2026 (via search summary) [T14-S16]
- [M1.13] IBM describes AI, machine learning, deep learning and neural networks as nested, each inside the one before. Deep learning is a subfield of machine learning. Reported, accessed 26 November 2026 [T14-S17]
- [M1.13] Cornell's workshop says machine learning is a subset of AI, deep learning a subset of machine learning, and some AI does not use machine learning at all. Reported, accessed 26 November 2026 [T14-S17]
- [M1.13] Sources disagree on generative AI. Some place it inside deep learning, while one says it overlaps mostly with deep learning and partly with classic machine learning. Uncertain, accessed 26 November 2026 [T14-S17]
</group>

<group name="T14d. API, rented GPUs or custom chips">
- [M1.16] No single break-even point exists between a model API and self-hosting. It depends on request volume, GPU utilisation, staff cost and model choice. Estimate, September 2026 [T14-S18]
- [M1.16] One analysis puts production hosting of a 70 billion parameter model at 4 to 8 rented H100 GPUs, costing $15,000 to $40,000 a month before staff. Estimate, April 2026 [T14-S18]
- [M1.16] An academic cost study finds break-even on-premise within months for small models, about 2 years for medium models and about 5 years for large ones. Estimate, 2025 [T14-S18]
- [M1.16] ML6 argues most firms should route work between APIs and self-hosting, not pick one. Regulated sectors may have to self-host whatever the cost. Estimate, 2026 [T14-S18]
- [M4.13] SemiAnalysis reports up to 50% better performance per dollar for Google TPUs than Nvidia B200 and B300 in FP8 serving. Estimate, 2026 [T14-S19]
- [M4.13] Goldman Sachs, as reported, estimates TPU v7 cut inference cost per token by about 70% against TPU v6, roughly level with GB200 NVL72. Estimate, 2026 [T14-S19]
- [M4.13] No public like-for-like benchmark of Trainium cost per token against Nvidia was found as of July 2026. Uncertain, 2026 [T14-S19]
- [M4.13] Google and Meta open-sourced TorchTPU in October 2026, aiming to make a PyTorch port as simple as changing "cuda" to "tpu". Reported, October 2026 [T14-S20]
- [M4.13] AWS launched TorchNeuron in public beta on 20 October 2026 for Trainium2 and Trainium3. It does not port CUDA-specific code automatically. Reported, October 2026 [T14-S21]
- [M4.13] AWS says custom Triton and CUDA kernels must be rewritten for Trainium or the migration stalls. TPUs often need JAX or lazy-execution PyTorch/XLA. Reported, 2026 [T14-S21]
- [M4.13] Goldman's view is that CUDA remains a key moat. Analysts describe leaving it as a multi-week port, though vLLM now runs on several chips. Estimate, 2026 [T14-S19]
</group>

<builder_notes>
- Temperature is the only dial most teams touch. For reasoning models, check the supplier page first, because Gemini 3 advises 1.0 and Anthropic's newest models say to omit it.
- Estimate input and output cost separately. Prefill is parallel and cheap per token, while decode is sequential and memory-bound, so long answers cost more.
- Attention grows with the square of the input length, so keep prompts short and use caching and retrieval before reaching for million-token windows.
- With OpenAI fine-tuning closed to new users, plan for prompting plus retrieval first, then Bedrock or Vertex tuning only if style or format still fails.
- Moving from an API to rented GPUs needs a team to run vLLM or similar, handle autoscaling and monitor quality. Utilisation decides whether it pays.
- A move to TPU or Trainium is easy for plain PyTorch models and hard for custom kernels. Benchmark your own model before committing.
- Sampling means identical prompts give different answers, so test with repeated runs and set evaluation thresholds, not single examples. (not searched)
</builder_notes>

<investor_notes>
- Because the model samples from probabilities, a wrong but plausible answer is always possible. This links to hallucination risk and to the need for checks in the product.
- Quadratic attention cost is one reason long-context products cost more to serve. Suppliers also raise prices above length thresholds (see T9).
- OpenAI exiting self-serve fine-tuning cuts one route to lock-in. One side says models are now good enough to need no tuning, the other says only enterprise partners can now tune.
- Custom chips can cut serving cost, with TPU evidence stronger than Trainium. Against this, Nvidia's CUDA software and supply chain keep switching costs high for most firms.
- Ask a company whether it calls an API, rents GPUs or owns chips. Each choice changes gross margin, staffing and supplier dependence.
- Terms like "hyperscaler" and "AI data centre" have no single legal definition. Check what a deck means before comparing figures.
</investor_notes>
</topic>

<topic key="T15" name="Third round: money flow, lasting advantage and product tests">
<group name="T15a. Investor tests for a lasting advantage">
- [M7.16] An a16z source states that AI by itself is not a moat, because it is only a way to deliver value to customers. Reported, 2026 [T15-S1]
- [M7.16] An a16z Apps Fund summary offers a data test. A product is a walled garden if usage creates unique data that makes the product measurably better. Estimate, 2026, secondary summary [T15-S1]
- [M7.16] The same summary offers a catch-up test. If a rival with the same model would need years of accumulated data to match you, there is a moat. Otherwise it is a thin wrapper. Estimate, 2026 [T15-S1]
- [M7.16] Bessemer's State of AI 2025 slides say systems of action are replacing systems of record, and that persistent memory and semantic understanding create functional lock-in. Reported, August 2025, old source [T15-S2]
- [M7.16] Bessemer's framing is that defensible outcomes are workflow-embedded results that incumbents cannot match with scale alone. This is a commentary summary of the report, not a quote. Estimate, 2026 [T15-S2]
- [M7.16] NFX's essay on AI defensibility argues network effects stay a main source of defensibility if used at the right time. It includes a "Switching Cost Test" on what happens if a user stops. Reported, 2026 [T15-S3]
- [M7.16] CRV argues that calling the AI layer the differentiator is like saying the database choice differentiates a SaaS product. Estimate, 2026 [T15-S4]
- [M7.16] A model-improvement test is common in investor writing. If the underlying model gets much better tomorrow, does the product become more valuable or less? Estimate, 2026 [T15-S1]
- [M7.16] A copy test is common too. If a rival copied your interface, would it still need your data, trust, integrations and operating context to match you? Estimate, 2026 [T15-S1]
- [M7.16] Sequoia's AI Ascent 2026 talk, as summarised secondhand, argues that enterprise memory may be a more durable moat than the product itself. Uncertain, 2026 [T15-S3]
- [M7.16] No numeric pass mark for these tests was found from a16z, Bessemer, ICONIQ, Sequoia, Menlo, NFX or Bain. The tests are qualitative. Uncertain, November 2026 [T15-S1]
- [C12] ICONIQ's gross margin data gives a numeric proxy. AI-native median gross margin is 55% below $10 million ARR and 60% at $10 million to $25 million. Estimate, September 2026 [T11-S27]
</group>

<group name="T15b. Distribution, bundling and features that removed a start-up's reason">
- [M7.12] Microsoft reported 15 million paid Microsoft 365 Copilot seats on its 28 January 2026 call, against about 450 million commercial Microsoft 365 seats. That is about 3% of the base. Reported, 28 January 2026 [T15-S5]
- [M7.12] Microsoft later reported 30 million paid Copilot seats, up 50% on 20 million a quarter earlier. One analysis puts this at about 7% of the base. Reported, July 2026 [T15-S5]
- [M7.12] Microsoft removed in-app Copilot Chat from Word, Excel and PowerPoint for unlicensed users at commercial customers above 2,000 seats. This pushes paid upgrades through the installed base. Reported, 2026 [T15-S5]
- [M7.12] Microsoft lists Copilot Business at $21 per user per month on annual terms for organisations of 300 or fewer users. Reported, 2026 [T15-S5]
- [M7.12] Salesforce reported Agentforce ARR of about $800 million in the quarter to 31 January 2026, up 169% on the year, with 29,000 deals closed since launch. Reported, 25 February 2026 [T15-S6]
- [M7.12] More than 60% of Salesforce's Agentforce and Data 360 fourth-quarter bookings came from existing customers. This shows distribution through the installed base. Reported, 25 February 2026 [T15-S6]
- [M7.12] Salesforce changed its Slack API terms in June 2025 so third parties cannot index, copy or permanently store Slack messages. Glean said this was a major blow to its value proposition. Reported, June 2025, old source [T15-S7]
- [M7.12] Salesforce points developers to its Real-Time Search API instead and says the change protects customer data. Analysts read it as control of data for its own AI. Reported, June 2025, old source [T15-S7]
- [M7.13] On 3 February 2026 Anthropic released plugins for Claude Cowork, including a legal plugin for contract review and NDA triage. Software and data stocks fell. Reported, February 2026 [T15-S8]
- [M7.13] Thomson Reuters fell about 15% to 18% in a day and RELX about 14% after the legal plugin. Sources differ on exact figures. Estimate, February 2026 [T15-S8]
- [M7.13] Analysts said the plugin did not touch legal research, the core value of those firms, and shares partly recovered the next day. So the stock fall was a fear signal, not lost revenue. Estimate, February 2026 [T15-S8]
- [M7.13] A 2023 ChatGPT PDF-reading update threatened start-ups that filled a feature gap. Gizmodo said it was unclear whether any would truly die. Estimate, November 2023, old source [T15-S9]
- [M7.13] Chegg blamed Google AI Overviews and chatbots for a 36% year-on-year revenue fall to $105.1 million in Q2 2025 and a 40% subscriber fall. Reported, 2025, old source [T15-S10]
- [M7.13] Chegg cut 22% of staff (248 people) in 2025 and sued Google. This is a dated case of a platform feature removing a product's reason to exist. Reported, 2025, old source [T15-S10]
</group>

<group name="T15c. Measured evidence on data, switching and own models">
- [M7.14] ChartMogul data shows price band drives retention. AI-native products above $250 a month show 70% gross and 85% net revenue retention. Estimate, December 2025 [T8-S14]
- [M7.14] Ramp data shows 43% of Anthropic's business customers switched from another vendor, and about 79% pay for OpenAI as well. Switching between model vendors is easy. Estimate, 2026 [T15-S11]
- [M7.14] Ramp's AI Index for October 2026 shows 56.8% of US businesses on Ramp pay for AI, with Anthropic at 44.8% and OpenAI at 40.6% adoption. Estimate, October 2026 [T15-S11]
- [M7.14] ICONIQ commentary warns that when the best solution can change every 6 to 12 months, multi-year lock-in is a risk that buyers are not paid to take. Estimate, 2026 [T15-S12]
- [M7.15] Cursor's Composer 2 costs $0.50 per million input tokens and $1.50 per million output tokens, well below Claude Opus 4.6 and GPT-5.4. Reported, 2026 [T15-S13]
- [M7.15] Composer 2.5 is built on the open-weights Kimi K2.5. Cursor says about 85% of the final model's compute came from its own post-training. Reported, 2026 [T15-S13]
- [M7.15] One analysis says Cursor's enterprise accounts reached positive gross margin mainly by using its own Composer models to cut third-party costs. Foundamental estimated about minus 30% earlier. Estimate, 2026 [T15-S13]
- [M7.15] Composer 2.5 placed third behind Claude Opus 4.7 and GPT-5.5 on several independent coding benchmarks. Cursor's own claims are not independently verified. Estimate, 2026 [T15-S13]
- [M7.11] No measured study was found that links private data or workflow depth to higher retention or gross margin for AI applications. Uncertain, November 2026 [T15-S12]
</group>

<group name="T15d. Usage averages and the flow of revenue">
- [M7.18] OpenAI says weekly ChatGPT Enterprise messages grew about 8 times from November 2024 to late 2025. The average worker sent 30% more. No absolute count was published. Reported, December 2025 [T15-S14]
- [M7.18] OpenAI says frontier workers at the 95th percentile send 6 times more messages than the median. Frontier firms use 8.3 times the output tokens per active user. Reported, 2026 [T15-S14]
- [M7.18] A modelled five-step support agent uses about 15,000 input and 2,500 output tokens per task. This is an assumption, not a measured average. Estimate, 2026 [T15-S15]
- [M7.18] Gartner found in March 2026 that agentic models use 5 to 30 times more tokens per task than a standard chatbot. Estimate, March 2026 [T15-S15]
- [M7.18] Fin prices a resolved conversation at $0.99. Fin says AI resolutions cost $0.50 to $2.00 against $6.00 to $13.50 for human agents. Reported, 2026 [T15-S15]
- [M7.18] Fin's average resolution rate is quoted at 67% in March 2026 and 76% on its own page. Reported, 2026 [T15-S16]
- [M1.11] Menlo puts 2026 enterprise AI spend at $176.8 billion, with $99.5 billion on infrastructure and $77.3 billion on applications. Estimate, 3 November 2026 [T8-S20]
- [M1.11] Reports put Anthropic's run rate above $65 billion at end July 2026 and OpenAI above $40 billion. Epoch puts the pair at about $100 billion. Estimate, August 2026 [T15-S17]
- [M1.11] Epoch says that in the first nine months of 2026 Anthropic's cost of revenue was $4.8 billion against $18.8 billion of compute spend. About 26% of its compute served customers. Estimate, 2026 [T15-S18]
- [M1.11] Epoch says Anthropic and OpenAI mostly rent compute from Google, Amazon, Microsoft, Oracle and CoreWeave. OpenAI's Brockman testified to about $50 billion of 2026 compute spend. Estimate, May 2026 [T15-S18]
- [M1.11] Moody's says Microsoft's AI revenue run rate reached $37 billion in early 2026, up 123%. AWS's AI run rate was over $15 billion. Estimate, 2026 [T15-S19]
- [M1.11] Google Cloud's contract backlog reached $460 billion, about double the $240 billion at end 2025. AWS backlog was $364 billion. Estimate, 2026 [T15-S19]
- [M1.11] Big four hyperscaler capex for 2026 is $725 billion by the Financial Times tally and $785 billion by Moody's. Estimate, 2026 [T15-S19]
- [M1.11] Nvidia's data centre revenue was $107.6 billion in its latest quarter, with a gross margin of 74.8%. This is where cloud capex lands. Reported, 17 November 2026 [T11-S1]
- [M1.11] Bain says $2 trillion of annual AI revenue is needed by 2030 to fund compute demand. It still sees an $800 billion gap. Estimate, 23 September 2025, old source [T15-S20]
</group>

<builder_notes>
- To test lock-in, measure how long it takes to swap the model behind a feature and re-run your evals. If it takes a day, the model is not your moat. (not searched)
- Log cost per resolved task by customer and model. Own fine-tuned models matter only if this line falls without quality loss. (not searched)
- Cursor shows the pattern. Fine-tune an open-weights base for the narrow task and keep frontier models for hard cases. Verify benchmarks independently.
- Data access can be cut by the platform that holds it, as the Slack API change shows. Prefer data you generate or own by contract.
- Token counts for support agents are mostly modelled. Measure your own with per-request logs of input, output and cached tokens. (not searched)
</builder_notes>

<investor_notes>
- The investor tests agree on direction. Ask whether usage creates data, whether the product is embedded in a workflow, and whether a rival with the same model could copy it.
- No firm publishes a pass mark. Treat tests as questions for diligence, and ask for cohorts by price band and gross retention.
- Distribution cuts both ways. Microsoft reached only 3% to 7% of its seat base after a year or more, so bundling does not guarantee uptake.
- Salesforce shows incumbents can protect distribution by controlling data access. Glean-type products that rely on others' data carry platform risk.
- Model-company feature launches move public stocks quickly, as on 3 February 2026. The revenue loss was not shown, so separate fear from measured churn.
- Money flows from users through apps and model firms to clouds and chips. Margins are thin in apps, higher in chips (Nvidia 74.8%), and Bain warns of a funding gap.
- The revenue flow figures come from mixed sources and different definitions. Do not add run rates from different firms without checking the method.
</investor_notes>
</topic>

<topic key="T16" name="Third round: hardware power, cost splits and GPU unit economics">
<group name="T16a. Power at each step of the ladder">
- [M4.6] An H100 SXM GPU draws up to 700 W. Nvidia's H200 page lists the same 700 W (configurable) maximum, and the H100 datasheet itself was not retrieved. Estimate, 2024 old source [T16-S1]
- [M4.6] A B200 GPU is rated at about 1,000 W on the HGX board. The silicon can run between 700 W and 1,200 W, depending on SKU and cooling. Estimate, March 2024 old source [T16-S1]
- [M4.6] An Nvidia DGX H100 server with 8 GPUs draws up to 10.2 kW maximum, fed by six 3.3 kW power supplies. Reported, Nvidia documentation, undated [T16-S3]
- [M4.6] An Nvidia DGX B200 server with 8 GPUs draws about 14.3 kW maximum. Reported, Nvidia product page, undated [T16-S4]
- [M4.6, M4.10] A GB200 NVL72 rack, with 72 GPUs, is rated at about 120 kW and needs liquid cooling. Earlier research in this project found 132 to 140 kW in some measurements. Estimate, 2024 old source [T16-S1]
- [M4.10] Campus scale: Abilene had 618 MW operating on 10 September 2026 (Epoch, via T4B). Schneider Electric publishes a single-hall reference design for GB200 NVL72 at 7,392 kW, or about 7.4 MW. Vertiv has a 1.2 MW design for a DGX GB200 SuperPod. Reported, vendor designs, 2024 [T16-S5]
</group>

<group name="T16b. Capital cost per GPU and the cost split of 1 GW">
- [M6.15, C5] SemiAnalysis puts an H100 server at about $190,000, and about $250,000 per server once storage, networking and other items are added, for a typical hyperscaler. That is about $31,000 per GPU. Estimate, 2024 old source [T16-S7]
- [M6.15, C5] SemiAnalysis puts a GB200 NVL72 rack-scale server at $3.1 million. With networking, storage and other items, the all-in cost is about $3.9 million per rack. Estimate, 2025 [T16-S2]
- [M6.15, C5] On those figures, about $54,000 per GPU all-in for GB200 NVL72, found by dividing $3.9 million by 72 GPUs. Network and storage add about 26 per cent to the server price. Derived, 2025 [T16-S2]
- [M6.15, C5] Epoch's 1 GW model gives annualised capital charges of $5,021 million for servers and $1,167 million for network, which is about 14 per cent network against servers plus network. Estimate, 2026 [T16-S8]
- [M6.15] The Register says hyperscalers resist spending over 10 per cent of the data centre budget on networking, but argues the true share of an AI cluster may reach 30 per cent. Opinion analysis, Uncertain, June 2025 [T16-S9]
- [M5.13] Epoch's typical 1 GW AI data centre costs about $38 billion up front and about $0.9 billion a year to operate. Estimate, 2026 [T16-S8]
- [M5.13] Epoch's Frontier Data Centers Hub gives $44 billion per GW of server power, with $30 billion on IT hardware and $14 billion on other costs. Hardware is about 68 per cent. Estimate, 2026 [T16-S10]
- [M5.13] Jensen Huang said a 1 GW AI factory costs $50 billion to $60 billion, including land, power, shell, compute, network, storage, power systems and cooling. Reported (vendor claim), 2025 [T16-S11]
- [M5.13] McKinsey splits $6.7 trillion of data centre spend to 2030 as 60 per cent to chip and hardware firms, 25 per cent to power, cooling and electrical, and 15 per cent to builders for land and site work. Estimate, 2025 [T16-S12]
</group>

<group name="T16c. Operating cost, electricity share and payback">
- [M5.7] Epoch's 1 GW model has annual opex lines of energy $594 million, taxes $143 million, maintenance $120 million, labour $40 million and water $6 million. Estimate, 2026 [T16-S8]
- [M5.7] Epoch's model uses 8.34 US cents per kWh, a power usage effectiveness of 1.14 and 71 per cent utilisation. Electricity is about 7 per cent of the $8.5 billion annual total cost. Estimate, 2026 [T16-S8]
- [M6.7, M6.15] In Epoch's model, staff, maintenance, taxes and water together are about $309 million a year. That is about 3.6 per cent of the $8.5 billion annual cost, so non-power opex is small. Derived, 2026 [T16-S8]
- [M6.7, C5] In a SemiAnalysis-style Meta 24k H100 cluster model, TCO is about $1.49 per H100-hour before cost of capital and $1.69 with it. Opex is about 29 per cent, mostly colocation and electricity. Estimate, 2024 old source [T16-S13]
- [M6.7] Colocation in Tier 3 markets averages $170 to $200 per kW each month, so one 8-GPU H100 server at 10.2 kW costs about $1,900 a month. Derived from a vendor cost model, 2026 [T16-S14]
- [M6.7, C5] Nebius estimates payback of 1 year and 10 months, or 22 months, on deals signed in Q2 2026, against two to three years before. Customer prepayments covered 50 to 60 per cent of capex. Reported, 2026 [T16-S15]
- [M6.7, C5] IREN says recent three-year contracts pay above $20 million of revenue per MW of IT load, which repays the compute investment in about two years. Reported, 2026 [T16-S16]
</group>

<group name="T16d. Contract types and example prices">
- [M6.3] Three contract types exist. On demand is paid by the hour or second with no commitment. Reserved is a fixed term at a lower rate. Spot is spare capacity at a deep discount that can be taken back. Reported, general definition, not searched [T16-S20]
- [M6.3] AWS reserved: EC2 Capacity Blocks for p5 list at $34.608 an hour per instance, or $4.326 per GPU, in US East. A July 2026 report says $5.19 per GPU. The sources conflict. Uncertain, 2026 [T16-S20]
- [M6.3] AWS spot: p5.48xlarge showed a lowest recent spot price of about $16.04 an hour in us-east-1 and $12.02 in us-east-2, about $2 per GPU. Spot moves with demand. Estimate, 2026 [T16-S21]
- [M6.3] CoreWeave on demand: an 8x H100 node lists at $49.24 an hour ($6.16 per GPU) and an 8x B200 node at $68.80 ($8.60 per GPU). Reserved is by quote, with "up to 60 per cent" off, terms unpublished. Reported, 2026 [T16-S22]
- [M6.3] Lambda 1-Click Cluster B200 prices fall with size and term: $9.86 per GPU-hour at 16 GPUs and $8.87 at 256 or more, with terms from 2 weeks to 1 year. Reported, 2026 [T16-S23]
- [M6.3] RunPod on demand: H100 PCIe is $2.89 an hour on Secure Cloud and from $1.99 on Community Cloud, billed per second. Reserved and savings terms go through sales. Estimate, 2026 [T16-S24]
</group>

<builder_notes>
- Use the 8-GPU server as the unit of power. A DGX H100 draws 10.2 kW and a DGX B200 14.3 kW, so a 40 kW air-cooled rack holds about 3 to 4 servers. (not searched)
- GPU TDP understates power. SemiAnalysis prices power at all-in system power, which includes CPUs, network and storage servers, and adds about 10 per cent of IT power for non-server gear. [T16-S2]
- For a GPU-hour calculator, set depreciation from all-in capex per GPU and life, then add colocation, electricity, cost of capital and a small staff line. (not searched)
- Spot suits jobs that checkpoint often. A spot eviction without a checkpoint loses the work since the last save. (not searched)
- Capacity Block prices on AWS move with supply and demand, so a stored price goes stale in weeks. Pull the live price in any tool. [T16-S20]
</builder_notes>

<investor_notes>
- Electricity is small in the cost model: about 7 per cent of annual cost in Epoch's case. The 12 per cent figure in T4B used $0.12 per kWh and full load, so the share depends on price and use.
- Capital is the cost. Servers are about 60 per cent of annual cost in Epoch's model, so the useful life of a GPU matters more than the power bill.
- Payback of 22 months to 2 years at Nebius and IREN is on new contracts at high prices and with customer prepayments. Older contracts paid back more slowly, at about 3 years.
- Huang's $50 billion to $60 billion per GW is a vendor claim and Jim Chanos says it is above what data centre firms tell investors. Epoch's $38 billion is lower.
- The spread of AWS prices is wide: on demand $6.88, Capacity Block about $4.33 to $5.19, spot about $2 per GPU-hour. The reserved discount comes with a commitment risk.
</investor_notes>
</topic>

<topic key="T17" name="Third round: platform choice and first limits">
<group name="T17a. How start-ups combine the four types of platform">
- [M8.19] Supabase's own State of Startups 2026 survey of about 2,000 builders reports cloud use of Supabase 65 per cent, Vercel 45 per cent, Cloudflare 27 per cent and AWS 21 per cent. Estimate, vendor survey, June 2026 [T17-S1]
- [M8.19] The same survey says Vercel already led AWS in 2025 and widened the gap in 2026. It says Cloudflare grew fastest and passed AWS. Estimate, vendor survey, 2026 [T17-S1]
- [M8.19] The survey page gives no question wording, sampling frame or denominator. An outside reader says it skews to solo and small-team builders on Postgres and AI. Treat it as directional. Uncertain, 2026 [T17-S1]
- [M8.19] A Qovery article of 19 November 2026 says the most common pattern is both worlds. Vercel serves the app shell. Anything needing a GPU, a persistent process or private networking runs on AWS. Estimate, supplier, November 2026 [T17-S2]
- [M8.19] The Resend handbook publishes its own tech stack, and Loops and Monk describe moves from Vercel and Supabase to AWS. These are named companies, but they are single cases, not a survey. Reported, 2026 [T17-S3]
- [M8.19] No survey or case study found shows Cloudflare placed in front of AWS as a common AI start-up pairing. The pairing rests on general practice. Uncertain, 2026 [T17-S2]
</group>

<group name="T17b. Choosing between the four types, by stage and need">
- [M8.20, C8] Qovery says use Vercel while the agent is part of a web product and fits inside serverless limits. It says move agents, workers and databases to your own AWS account as needs grow. Estimate, supplier, November 2026 [T17-S2]
- [M8.20] Qovery says AWS lacks git-push deploys, a preview URL per pull request and per-branch variables out of the box. A team must build or buy them. Estimate, supplier, November 2026 [T17-S2]
- [M8.33] Monk, a financial data start-up, moved its back end from Vercel and Supabase to AWS in August 2026. It cited control over reliability, performance and where customer financial data lives. Reported, company blog, August 2026 [T17-S3]
- [M8.33] Loops describes a zero-downtime move from Vercel and Supabase to AWS. Its founders call themselves product engineers with little infrastructure experience, and they hired platform engineers before the move. Reported, company blog, 2026 [T17-S4]
- [M8.20] A Vercel-to-AWS migration series argues the sums rarely work at start-up scale and advises keeping Vercel for now. A guide warns that the engineering time can exceed the hosting saving. Estimate, personal blog, 2026 [T17-S5]
- [M8.20] A consultancy says it moved three start-ups with Vercel bills above 1,500 euros a month to Cloudflare Pages. This is a sales pitch, so the saving claims are unverified. Uncertain, supplier, May 2026 [T17-S6]
- [C8] One founder reports a Vercel bill rising from about $50 to $1,200 a month, then settling near $200 on AWS. The figure is self-reported and unverified. Uncertain, 2026 [T17-S6]
</group>

<group name="T17c. Measured bills and large surprise bills">
- [M8.34] A Supabase worked invoice shows 160,000 monthly active users at $195 and a $10 compute credit, for a total of $220. Reported, 26 November 2026 [T17-S7]
- [M8.34] A third-party 2026 analysis puts apps with 50,000 to 200,000 monthly active users at $100 to $200 on Supabase. No published real bill at 100,000 users was found. Estimate, 2026 [T17-S7]
- [M8.34] No measured infrastructure bill for 1,000 or 1,000,000 users was found on any of the four platforms. Only vendor and blog estimates exist, which T7B already lists. Uncertain, 2026 [T17-S7]
- [M8.34] Metacast, a podcast start-up, saw bots send 66,500 requests in one day to Next.js image optimisation on Vercel. The team estimated exposure of $7,000 and caught it in time. Reported, company post-mortem, February 2025, old source [T17-S8]
- [M8.34] Vercel Image Optimization was charged at $5 for every 1,000 images optimised in the Metacast case, and 1.4 million crawlable pages gave bots plenty to fetch. Reported, February 2025, old source [T17-S8]
- [M8.34] A June 2026 article describes a DDoS attack that turned one developer's Vercel account into a $23,000 bill. Another post reports a $1,335 invoice after an attack. Both are unverified. Uncertain, 2026 [T17-S9]
- [M8.34] On AWS, an anonymised Series A teardown lists a NAT Gateway line of $14,200, or 35.4 per cent of the bill. Blog accounts also name runaway Lambda loops. Uncertain, blog, 2026 [T17-S10]
</group>

<group name="T17d. First limits that a small team meets">
- [M8.35] Supabase Free projects pause after 7 days of low database activity. Pro, Team and Enterprise projects are never paused for inactivity. Reported, 26 November 2026 [T17-S11]
- [M8.35] Supabase says transaction mode on port 6543 suits serverless and edge functions, which open many short connections. It does not support prepared statements, so turn them off in the client library. Reported, 26 November 2026 [T17-S12]
- [M8.35] Supabase says running both poolers at once raises the risk of hitting the database connection limit on small compute tiers. Both poolers share one pool size setting. Reported, 26 November 2026 [T17-S12]
- [M8.35] Supabase troubleshooting separates two errors. "Remaining connection slots are reserved" means the database cap is hit. "Max client connections reached" comes from the pooler. Reported, 26 November 2026 [T17-S13]
- [M8.35] Vercel reports a 504 FUNCTION_INVOCATION_TIMEOUT when a function runs past its limit. Streamed time counts, so streaming an LLM answer does not escape the limit. Reported, 26 November 2026 [T17-S14]
- [M8.35] Vercel Pro runs 300 seconds by default and 800 seconds at most, with 1,800 seconds in beta. Vercel points long jobs to Queues or Workflows. Reported, 26 November 2026 [T17-S14]
- [M8.35] A Vercel docs note says Spend Management alerts start at $200 a billing cycle for new customers. Pausing projects at the limit is optional, not automatic. Reported, 26 November 2026 [T17-S15]
- [M8.35] Vercel Pro includes 1 TB of Fast Data Transfer and 10 million Edge Requests each month, with overage from $0.15 per GB. Reported, 26 November 2026 [T17-S15]
- [M8.35] Cloudflare Workers allow 128 MB of memory on both plans. CPU time is 10 milliseconds on Free and up to 5 minutes on Paid. Time waiting on the network does not count. Reported, 26 November 2026 [T17-S16]
- [M8.35] Exceeding the CPU or memory limit returns Error 1102 "Worker exceeded resource limits". Subrequests are capped at 50 on Free and 10,000 per invocation on Paid. Reported, 26 November 2026 [T17-S16]
- [M8.35] AWS Lambda gives 1,000 concurrent executions per region by default. Each function scales by 1,000 more every 10 seconds, and a quota case raises the cap. Reported, 26 November 2026 [T17-S17]
- [M8.35] New AWS accounts start with lower Lambda concurrency and memory quotas, which AWS raises automatically with use. Reported, 26 November 2026 [T17-S17]
- [M8.35] Since 1 August 2025, AWS bills the Lambda INIT (cold start) phase for ZIP functions. AWS says cold starts are a very small fraction of invocations, and a blog puts it under 1 per cent. Reported, April 2025, old source [T17-S18]
</group>

<group name="T17e. Team skill and the cost of running your own AWS">
- [M8.35] Vercel's customer story "360 billion tokens, 3 million customers, 6 engineers" reports a small team running a large AI product on the platform. It is supplier marketing and the details were not read. Uncertain, supplier, 2026 [T17-S19]
- [M8.35] The 2025 DORA report finds platform quality matters. Gains appear in loosely coupled systems with fast feedback, and tightly coupled systems see little benefit. One summary puts the delivery gain near 10 per cent. Estimate, 2025, old source [T17-S20]
- [M8.35] An earlier DORA report found internal platform users had 8 per cent higher individual productivity and 10 per cent higher team performance, with a dip as the platform aged. Reported, 2024, old source [T17-S20]
- [M8.35] DX reports leaders give 2 to 6 per cent of headcount to central developer productivity, about one engineer per 17 to 50 developers. This covers more than AWS operations. Estimate, Q1 2026 [T17-S21]
- [M8.35] A rule of thumb of one DevOps engineer for every ten developers circulates in blogs. No survey tying a headcount to running a company's own AWS setup was found. Uncertain, blog, 2025 [T17-S21]
</group>

<builder_notes>
- Start on Vercel plus Supabase for speed. Move one workload at a time when a named limit bites, rather than moving everything. This matches the Qovery, Monk and Loops accounts.
- On Supabase, use the transaction pooler for serverless code from day one and turn off prepared statements. Treat the 60-connection Micro cap from T7 as the first wall.
- On Vercel, put a hard spend limit, bot rules and an image-optimisation allow-list in place before launch. The Metacast case shows crawlers can turn image requests into a bill within hours.
- A long model call on Vercel needs a queue or workflow once it nears the 300-second default. Streaming alone does not extend the limit.
- On Workers, heavy parsing and large bundles hit the 128 MB and CPU limits. Move that work to a container or Lambda (not searched).
- On Lambda, cold starts are rare but visible on latency-sensitive paths. SnapStart and provisioned concurrency are the usual fixes (not searched).
- On AWS, the first surprises are NAT Gateway data charges, log ingestion and idle resources. Set budgets and anomaly alerts first, and use VPC endpoints for S3.
- Loops hired platform engineers before leaving Vercel and Supabase. Treat a first dedicated platform hire as the entry ticket for owning AWS.
</builder_notes>

<investor_notes>
- The only usage survey found is from Supabase, a seller. It favours Supabase, Vercel and Cloudflare over AWS. Ask for a neutral survey before using the shares in a memo.
- Bull view: managed platforms let a very small team ship, and Vercel advertises a 6-engineer AI company. Bear view: this is supplier marketing, and DORA finds only modest gains.
- Both sides of migration exist. Monk and Loops moved to AWS for control and data location. A blogger argues the move rarely pays at start-up scale. Neither side publishes audited savings.
- Large surprise bills on Vercel came from bots and attacks, not normal growth. Ask any target about spend limits, bot protection and who gets the alerts.
- Savings claims for leaving Vercel (80 per cent, $45,000 a year) come from sellers and personal blogs. Do not use them without invoices.
- Compliance and customer data rules, not cost, are a common trigger for AWS. This favours a staged stack by stage, not a single winner.
- The cost of an in-house AWS team is not measured. A 1-in-10 rule of thumb is anecdotal, so ask the target for its real platform headcount.
</investor_notes>
</topic>

<topic key="T18" name="Third round: application KPIs, technical review and skill levels">
<group name="T18a. Application KPIs: requests per second, error rate and cost per user">
- [M9.20] Requests per second (RPS) is the number of requests a server or service completes in one second. Monitoring tools often show requests per minute, which is RPS times 60. Reported, 2026 [T18-S1]
- [M9.20] RPS is not the same as users. One hundred visitors who each load a page every 10 seconds make only about 10 page requests per second, plus the asset requests. Estimate, 2026 [T18-S1]
- [M9.20] One million requests a day is about 11.6 requests per second on average (1,000,000 divided by 86,400 seconds). Peak hours run several times higher, because traffic is bursty. Estimate, 2026 [T18-S1]
- [M9.20] A published benchmark of typical RPS for a small or a middle-size application was not found. Only one anecdote surfaced, a web server that peaks near 150 dynamic requests per second. Uncertain, 2026 [T18-S1]
- [M9.20] OpenAI sets rate limits at the organisation and project level, not the user level. They vary by model and are counted in requests per minute (RPM) and tokens per minute (TPM). Reported, 2026 [T18-S2]
- [M9.20] OpenAI's GPT-5 page lists Tier 1 at 500 RPM and 500,000 TPM. Tier 5 is 15,000 RPM and 40 million TPM. Tier 5 needs $1,000 paid. Reported, 2026 [T18-S2]
- [M9.20] 15,000 RPM equals 250 requests per second. Tier 1 at 500 RPM is about 8 per second, so a small app with a few users can reach the ceiling. Estimate, 2026 [T18-S2]
- [M9.20] Anthropic's docs list Claude Sonnet 4 at 50 RPM at the base tier. Higher tiers show 1,000 and 4,000 RPM. The tier labels for the higher rows were inferred. Uncertain, 2026 [T18-S3]
- [M9.20] A model API often runs out of tokens per minute before requests per minute, because long prompts use many tokens. A 429 error then signals the limit. Reported, 2026 [T18-S3]
- [M9.19] Google's SRE material defines an SLI as good events divided by total events. A web service availability SLI is the share of non-5xx responses. Error rate is the inverse. Reported, 2026 [T18-S4]
- [M9.19] The SRE Workbook example is a 99.9% success target. That allows a 0.1% error rate, or 3,000 errors in 3 million requests over four weeks. Reported, 2026 [T18-S4]
- [M9.19] A 99.9% target over 30 days allows about 43.2 minutes of downtime. A constant 0.1% error rate uses the whole error budget (burn rate of 1). Reported, 2026 [T18-S4]
- [M9.19] The SRE book defines availability by request success rate, not by uptime. It lists latency, error rate and throughput as example SLIs. Reported, 2026 [T18-S4]
- [M9.19] The AWS Reliability Pillar maps availability to yearly downtime. 99.9% allows about 8 hours 45 minutes, 99.99% about 52 minutes, and 99.999% about 5 minutes. Reported, 2026 [T18-S5]
- [M9.19] AWS ties 99.9% to internal tools and 99.99% to video streaming. It does not set an error rate target. Chained 99.99% dependencies multiply to 99.97%. Reported, 2026 [T18-S5]
- [M9.19] OpenAI's status page showed API uptime of 99.99% for December 2025 to March 2026. A separate report gave 99.94% for the API and 99.64% for ChatGPT. Windows differ. Uncertain, 2026 [T18-S6]
- [M9.19] One commentary puts Claude services at 99.5% to 99.75% uptime over 30 days. A published 5xx error rate for either model API was not found. Uncertain, 2026 [T18-S6]
- [M9.19] OpenAI's standard enterprise terms carry no published uptime SLA, and a 99.9% monthly SLA comes with Azure OpenAI. Terms can be negotiated. Estimate, 2026 [T18-S6]
- [M9.21] No audited benchmark of inference cost for each monthly active user or paid seat was found. Sources point to ICONIQ and to a company's own usage data. Uncertain, 2026 [T18-S7]
- [M9.21] ICONIQ's January 2026 survey puts AI product gross margin near 52% for 2026, up from 41% in 2024. Another summary cites 45% for 2025. Estimate, 2026 [T18-S7]
- [M9.21] Usage skew drives cost for each user. An illustrative table gives $0.50 a month for a light user and $40 for a heavy user at 4,000 requests. Estimate, 2026 [T18-S8]
- [M9.21] Press in 2023 reported GitHub Copilot lost about $20 a month on average per user on a $10 plan, and up to $80 for some. Estimate, old source, 2023 [T18-S9]
- [M9.21] GitHub moved Copilot to usage-based billing on 1 June 2026. Its product chief said the premium request model was no longer sustainable. Plans buy credits at 1 cent each. Reported, April 2026 [T18-S9]
- [M9.21] Copilot list prices stay at $10 for Pro, $19 per user for Business and $39 per user for Enterprise. Heavy agent use is anecdotally $600 to $1,200 a month. Uncertain, 2026 [T18-S9]
</group>

<group name="T18b. Technical review of an AI company: strong and weak answers">
- [M9.2] Data and IP rights, weak answer: unclear ownership of the model and data. Strong answer: documented training data sources and licences, plus IP assignments from all contributors. Estimate, 2026 [T18-S10]
- [M9.2] Evaluation, weak answer: the team says it "eyeballs outputs" and has no golden dataset. Strong answer: versioned evaluation sets with numbers on held-out data. Estimate, 2026 [T18-S10]
- [M9.2] Security, weak answer: SOC 2 offered as the full answer. Strong answer: access control, dependency monitoring, and systematic (not anecdotal) red-team tests for prompt injection. Estimate, 2026 [T18-S11]
- [M9.2] Security, strong answer: agents hold least-privilege permissions, the tool layer re-checks authorisation, and the team can say how fast an agent's wrong action is undone. Estimate, 2026 [T18-S11]
- [M9.2] Scale, strong answer: the team knows inference cost per unit of revenue and what breaks as usage grows. Weak answer: margins assumed without a cost per task. Estimate, 2026 [T18-S10]
- [M9.2] Release practice, strong answer: prompt and model versioning with handover artefacts. A search found no concrete release or deployment test in these checklists. Uncertain, 2026 [T18-S10]
- [M9.2] Team: a Beyond Elevation six-point framework lists model dependency, data moat, IP status, talent concentration and regulatory exposure. Talent concentration is the team risk. Estimate, 2026 [T18-S12]
- [M9.2] Peony publishes 90 buy-side checks in five layers: Data, Model, Infrastructure, Output and Governance. These are vendor checklists and not a standard. Estimate, 2026 [T18-S10]
- [M9.2] No checklist from Bessemer, a16z or Sequoia was found, and a University of Tennessee framework could not be read in detail. Uncertain, 2026 [T18-S11]
</group>

<group name="T18c. Skill ladders for AI">
- [M9.10] SFIA 9 has seven levels of responsibility: Follow, Assist, Apply, Enable, Ensure and advise, Initiate and influence, and Set strategy, inspire, mobilise. Reported, 2026 [T18-S13]
- [M9.10] SFIA level 3 (Apply) works under general direction and has work reviewed at milestones. Level 4 (Enable) works with substantial personal responsibility inside a clear framework. Reported, 2026 [T18-S13]
- [M9.10] SFIA level 5 (Ensure, advise) works under broad direction, owns allocated objectives and gives authoritative guidance in the field. SFIA is not AI-specific. Reported, 2026 [T18-S13]
- [M9.10] SFIA's three generic attributes of level are autonomy, influence and complexity. Business skills describe the behaviours needed at each level. Reported, 2026 [T18-S13]
- [M9.10] UNESCO's student framework has 12 competencies in four dimensions and three levels: Understand, Apply, Create. The teacher framework uses Acquire, Deepen, Create. Reported, 2024 old source [T18-S14]
- [M9.10] A Southampton guide reads the teacher levels for AI ethics as: aware of issues (Acquire), safe and responsible use (Deepen), co-creating ethical rules (Create). Estimate, 2026 [T18-S14]
- [M9.10] The Commission and OECD AILit framework (18 June 2026) has four dimensions: engage with AI, create with AI, manage AI, and help shape AI. It covers schools. Reported, June 2026 [T18-S15]
- [M9.10] Coverage of the AILit framework describes knowledge, skills and attitudes, with 19 competences. Named proficiency tiers equal to aware, fluent, practitioner and expert were not found. Uncertain, 2026 [T18-S15]
- [M9.10] No published framework found maps one-to-one to aware, fluent, practitioner and expert. SFIA, UNESCO and Anthropic's 4Ds give partial ladders, so the course must map them. Uncertain, 26 November 2026 [T18-S13]
</group>

<group name="T18d. Twelve-week self-study plans for a non-engineer">
- [M9.11] Masai School's vibe coding path runs in stages: read code basics, write specs, build a first app, use a coding agent, add a database and sign-in, then test, secure and ship. Reported, 2026 [T18-S16]
- [M9.22] Masai School gives module times of about 5 to 8 hours for a first app and 2 to 3 hours for a coding agent build. Its total length was not confirmed. Uncertain, 2026 [T18-S16]
- [M9.22] AI Builder Club gives a first-app timeline of about 10 hours for week 1, 15 hours for week 2, and 10 hours each for deployment and polish. It starts with a one-page spec. Estimate, 2026 [T18-S17]
- [M9.11] Ziplines publishes a 90-day roadmap for non-coders in five stages: problem, planning and context, execution, validation, and communication or handoff. Weekly hours were not found. Estimate, 2026 [T18-S18]
- [M9.11] The Maven "AI Build Lab Accelerator" is a no-code course for non-technical professionals with a syllabus over Weeks 1 to 12. Weekly hours were not shown. Reported, 2026 [T18-S19]
- [M9.22] A Maven course for non-engineers lists 3 hours a week of live sessions, 1 hour of exercises and 1 to 3 hours of reading. Its total length was not shown. Reported, 2026 [T18-S19]
- [M9.22] A published 12-week plan with hours for each week and a named result was not found. The plan in the builder notes is a derived outline, not a published one. Uncertain, 26 November 2026 [T18-S16]
</group>

<builder_notes>
- Count requests per second at the load balancer and keep the 95th percentile of peak minutes, not the daily average. (not searched)
- Model APIs fail on tokens per minute first. Add retry with exponential backoff, read the retry-after header, and cap prompt length. (not searched)
- Measure error rate as 5xx plus timeouts over all requests. Also count model-level failures such as empty or invalid structured output. (not searched)
- Log tokens and cost per request with a user ID. Then compute cost per active user and see the heavy-user tail, not only the mean. (not searched)
- A derived 12-week outline from the sources: weeks 1 to 2 spec and basics (4 to 5 hours a week), weeks 3 to 6 first app in a builder (8 to 10 hours), weeks 7 to 10 coding agent, database and sign-in (6 to 8 hours), weeks 11 to 12 test and ship (5 hours). Result: one deployed app.
- Test the first app for security by hand. Row-level security and exposed keys are the common failures. (not searched)
</builder_notes>

<investor_notes>
- Ask for cost per active user split by decile. The average hides power users who can cost 80 times more than light users on a flat plan.
- Flat seat prices met usage-based costs at GitHub in 2026. A target on a flat seat plan carries the same risk.
- Treat status-page uptime as a vendor claim. Ask for the target's own error rate over 90 days and its SLO.
- A model API has no standard SLA. A target that sells 99.9% uptime on top of it may be promising more than it buys.
- A strong security answer shows tests and evidence, not only a SOC 2 certificate. A weak answer gives a certificate and nothing on prompt injection.
- Checklists here are vendor and practitioner content. Use them as question lists, not as standards.
- The skill ladder is a working map built from partial frameworks. Do not present it as one published standard.
</investor_notes>
</topic>

<topic key="T19" name="Third round: glossary definitions">
<group name="T19a. Models: how they learn and are tuned">
- [A.2] Neural network: a model made of layers of simple units. Each unit adds up its weighted inputs, applies a function, and passes the result to the next layer. Reported, accessed 26 November 2026 [T19-S1]
- [A.2] Layer: one stage of a neural network. Its units take the results of the layer before, transform them, and hand the output to the layer after. Reported, accessed 26 November 2026 [T19-S1]
- [A.2] Gradient: a measure of how much the model's error changes when one adjustable number (a parameter) changes. It tells training which way to nudge each number. Reported, accessed 26 November 2026 [T19-S1]
- [A.2] Backpropagation: the method that trains a neural network. It works backwards through the layers and adjusts every weight a little, so that the error falls. Reported, accessed 26 November 2026 [T19-S1]
- [A.2] Softmax: a function that turns a list of raw scores into probabilities that add up to 1. Models use it to rank next tokens or to pick experts. Estimate, 2025 [T19-S2]
- [A.2] Tokenizer: the tool that splits text into small pieces (tokens), so that a model can read the text as a sequence of units. Reported, accessed 26 November 2026 [T19-S3]
- [A.2] Mixture of experts: a model design with many small expert networks, where a router sends each token to only a few of them, so each step uses part of the model. Estimate, 2025 [T19-S2]
- [A.2] Fine-tuning: a second round of training that takes a model already trained on broad data and adapts it to a specific task. Reported, accessed 26 November 2026 [T19-S4]
- [A.2] Distillation: training a smaller student model to copy the behaviour of a larger teacher model, to get faster answers and lower memory and energy use. Reported, accessed 26 November 2026 [T19-S4]
- [A.2] Reinforcement learning from human feedback (RLHF): a method where a reward model learns from human ratings and then guides the training of an AI model towards answers that people prefer. Reported, accessed 26 November 2026 [T19-S5]
- [A.2] Quantisation: storing a model's numbers with fewer bits, which shrinks memory use, usually with a small loss of accuracy that grows as the bit count falls. Estimate, 2025 [T19-S6]
- [A.2] Structured output: a setting that forces a model's reply to follow a supplied JSON schema. The application must still handle refusals, cut-off replies and business rules. Reported, accessed 26 November 2026 [T19-S7]
- [A.2] Guardrail: a rule that says what information an AI application may share and what it must withhold. Testers check it by trying to push the application off course. Reported, accessed 26 November 2026 [T19-S8]
</group>

<group name="T19b. Serving and cost">
- [A.2] Inference engine: software that runs a trained model to answer requests. Nvidia lists TensorRT-LLM and vLLM as examples, and calls vLLM a high-throughput serving engine. Reported, accessed 26 November 2026 [T19-S9]
- [A.2] KV cache: a store of the attention results for earlier tokens, so that the model does not recompute them for each new token. Reported, accessed 26 November 2026 [T19-S9]
- [A.2] Time to first token: the delay between receiving a request and producing the first output token. Reported, accessed 26 November 2026 [T19-S9]
- [A.2] Prompt caching: a feature that stores the start of a prompt (tools, system text, messages) so repeat requests reuse it. The cache lasts 5 minutes or 1 hour. Reported, accessed 26 November 2026 [T19-S10]
- [A.2] Rate limit: a cap on how much a customer can send to an API. Going over the cap returns a 429 error and a retry-after wait time, and caps depend on the usage tier. Reported, accessed 26 November 2026 [T19-S11]
- [A.2] Context compaction: when a conversation grows long, the server replaces the older turns with a summary written by the model, so the conversation fits in the context window. Reported, accessed 26 November 2026 [T19-S12]
</group>

<group name="T19c. Hardware and data centres">
- [A.2] CUDA: Nvidia's platform and programming model for running general computing work on its GPUs. Reported, accessed 26 November 2026 [T19-S13]
- [A.2] NVLink: Nvidia's fast link between GPUs and CPUs inside one server, which lets several GPUs work as one system. Reported, accessed 26 November 2026 [T19-S14]
- [A.2] InfiniBand: a fast network that links separate servers together. Nvidia uses it between servers, while NVLink works inside a server. Reported, accessed 26 November 2026 [T19-S14]
- [A.2] High-bandwidth memory (HBM): memory made of DRAM chips stacked in layers on the same package as the processor, which moves far more data per second than ordinary memory. Estimate, accessed 26 November 2026 [T19-S15]
- [A.2] PUE: power usage effectiveness. It is the total power a data centre draws divided by the power its IT equipment uses. A value near 1.0 means little waste. Reported, accessed 26 November 2026 [T19-S16]
</group>

<group name="T19d. Business and finance of compute">
- [A.2] Neocloud (GPU cloud): a cloud provider built around GPU computing for AI work, in contrast to a broad cloud provider. Estimate, 2025 [T19-S17]
- [A.2] Hyperscaler: a global, general-purpose cloud platform that offers hundreds of services for many kinds of customer work. Estimate, accessed 26 November 2026 [T19-S18]
- [A.2] Burn multiple: net cash burned divided by net new annual recurring revenue in the same period. Lower is better, and under 1 is often called exceptional. Estimate, accessed 26 November 2026 [T19-S19]
- [A.2] Net revenue retention: the share of recurring revenue kept from existing customers over a period, after upgrades, downgrades and cancellations. Above 100 percent means expansion beats losses. Reported, accessed 26 November 2026 [T19-S20]
</group>

<group name="T19e. Software">
- [A.2] Container: a way to package software with everything it needs into one file that can run on any machine that supports containers. Reported, accessed 26 November 2026 [T19-S21]
- [A.2] Read replica: a read-only copy of a main database, kept up to date by copying changes across, used to spread out read traffic. Reported, accessed 26 November 2026 [T19-S22]
- [A.2] Cold start: the delay when a serverless platform must create and set up a fresh environment before it can run your code, because no ready instance exists. Reported, accessed 26 November 2026 [T19-S23]
- [A.2] Vector database: a database built to store, index and search embeddings, which are lists of numbers that describe meaning. Reported, accessed 26 November 2026 [T19-S24]
- [A.2] Retrieval-augmented generation (RAG): a method that fetches relevant text from a data store and adds it to the prompt, so a model can use new data without retraining. Reported, accessed 26 November 2026 [T19-S25]
- [A.2] Prompt injection: an attack where hidden or direct instructions in the input make a model ignore its intended behaviour. OWASP ranks it as the top LLM risk. Reported, 2025 [T19-S26]
- [A.2] Model Context Protocol (MCP): an open protocol that lets AI applications connect to servers that offer tools, resources and prompts. Anthropic introduced it in 2024. Uncertain, accessed 26 November 2026 [T19-S27]
</group>

<group name="T19Ba. Models and serving">
- [A.2] Evaluation (eval): a test that runs a model or an AI application on set tasks and checks its outputs against criteria. OpenAI's open-source evals project is one such framework. Reported, accessed 26 November 2026 [T19B-S1]
- [A.2] Model card: a short document, about one to two pages, that ships with a trained model. It reports how the model performs across conditions, what it is for and where it fails. Reported, 2019 (old source) [T19B-S2]
- [A.2] System prompt: instructions given to the model before the user's question. It sets the model's role, tone and rules. Anthropic advises putting the role there and task details in the user turn. Reported, accessed 26 November 2026 [T19B-S3]
- [A.2] Knowledge cut-off: the date up to which a model's training information is reliable. Anthropic also lists a broader "training data cutoff", which can be later than the reliable date. Reported, accessed 26 November 2026 [T19B-S4]
- [A.2] Batch request: a job of many requests sent together and answered later, not at once. Anthropic's Message Batches API charges 50 per cent of standard prices and suits work that is not urgent. Reported, accessed 26 November 2026 [T19B-S5]
- [A.2] Latency: the time the model takes to read the prompt and produce its answer. Lower latency means the user waits less. Reported, accessed 26 November 2026 [T19B-S6]
- [A.2] Throughput: how many requests a system can handle each second. It measures capacity under load, while latency measures the wait for one request. Estimate, accessed 26 November 2026 [T19B-S7]
</group>

<group name="T19Bb. Hardware">
- [A.2] GPU (graphics processing unit): a chip built to run many calculations at the same time. It was made for graphics and is now used to train and run AI models. Estimate, accessed 26 November 2026 [T19B-S8]
- [A.2] TPU (tensor processing unit): Google's own chip, designed for machine learning work. Google calls it an application-specific integrated circuit (ASIC). Reported, accessed 26 November 2026 [T19B-S9]
- [A.2] ASIC (application-specific integrated circuit): a chip designed for one kind of job, not for general use. Google's TPU is an example, built for the large matrix maths in machine learning. Reported, accessed 26 November 2026 [T19B-S9]
- [A.2] FLOP: one floating-point calculation. FLOPS, with a capital S, means such calculations per second and measures a chip's speed. It does not give the full picture of performance. Estimate, accessed 26 November 2026 [T19B-S10]
- [A.2] Advanced packaging: ways of joining several chips, such as processors and high-bandwidth memory, in one package. TSMC's CoWoS places them on a silicon layer, called an interposer, on a base. Reported, accessed 26 November 2026 [T19B-S11]
- [A.2] Colocation: a model where a customer rents space in someone else's data centre for its own equipment. The tenant gets rack space, power, cooling and network links, and keeps control of its hardware. Reported, accessed 26 November 2026 [T19B-S12]
- [A.2] Liquid cooling: removing heat from AI racks with liquid, such as direct-to-chip loops or rear-door heat exchangers. Vertiv says AI racks above 250 kW push older sites past their limits. Reported, accessed 26 November 2026 [T19B-S12]
</group>

<group name="T19Bc. Finance of compute">
- [A.2] Depreciation: spreading the cost of an asset over the years it is used. It allocates cost to periods and does not estimate the asset's change in market value. Reported, 2026 [T19B-S13]
- [A.2] Useful life: the period over which a company expects to use an asset, or the number of units it expects to produce. Wear, and being overtaken by newer technology, both count. Reported, 2026 [T19B-S13]
- [A.2] Capital expenditure: money spent on long-lived assets such as equipment and infrastructure. Exterran's filing splits it into growth spending that adds capacity and maintenance spending that keeps existing capacity. Reported, 2022 (old source) [T19B-S14]
- [A.2] Gross margin: gross profit divided by revenue. Gross profit is revenue minus the direct cost of delivering the product or service. Reported, 2016 (old source) [T19B-S15]
- [A.2] Backlog (remaining performance obligation): the price of contracted work that a company has not yet delivered. Under ASC 606, firms often leave out contracts of one year or less. Reported, 2019 (old source) [T19B-S16]
- [A.2] Backlog and remaining performance obligation can differ. Ducommun reported remaining performance obligations of $1,106.0 million against backlog of $1,202.9 million, because many of its long-term agreements fall outside ASC 606. Reported, FY2025 [T19B-S16]
</group>

<group name="T19Bd. Software">
- [A.2] Front end: the part of a website or app that runs on the user's device and that the user sees and uses. It covers design, content and interactive scripts. Estimate, accessed 26 November 2026 [T19B-S17]
- [A.2] Back end: the server side of a system. It stores data and runs the business logic that the front end asks for. Estimate, accessed 26 November 2026 [T19B-S17]
- [A.2] Serverless function: code that runs only when an event triggers it, without the user managing servers. AWS Lambda handles capacity, scaling and patching, and charges only for compute time used. Reported, accessed 26 November 2026 [T19B-S18]
- [A.2] Load balancer: a service that spreads incoming traffic across several targets, such as servers, containers or functions. AWS Elastic Load Balancing offers four types. Reported, accessed 26 November 2026 [T19B-S19]
- [A.2] Connection pool: a set of database connections kept open so that many clients can reuse them. It does not raise the database's own maximum number of connections. Reported, accessed 26 November 2026 [T19B-S20]
- [A.2] Egress: data that leaves a cloud provider's network, for example to the internet. Providers charge egress fees per gigabyte, and rates vary by provider, region and destination. Estimate, accessed 26 November 2026 [T19B-S21]
- [A.2] Service level agreement (SLA): a provider's written uptime promise. Google and AWS define monthly uptime as a percentage and pay service credits, not refunds, when they miss it. Reported, accessed 26 November 2026 [T19B-S22]
</group>

<builder_notes>
- Search summaries gave paraphrases, not exact quotes. The course writer should check each definition against the linked page before publishing. (not searched further)
- A structured output setting removes parsing errors but not wrong content. Keep validating business rules in code.
- Compaction and prompt caching both cut cost on long agent runs. Caching keeps the prefix stable, compaction shortens it.
- Cold starts matter most for rarely used functions. Provisioned concurrency is the usual fix, at a standing cost.
- HBM bandwidth, not raw compute, often limits inference speed. (not searched further)
- Evals and benchmarks differ in practice: a benchmark is a shared public test, an eval is a test you build on your own task. (not searched)
- Latency and throughput trade off. Batching raises throughput and cost efficiency but makes each single request slower. (not searched)
- Serverless functions open many short database connections, so use a pooler in transaction mode. Supabase says this mode is for serverless and edge functions.
- Egress fees decide the real cost of media-heavy or data-export products, so check them before choosing a cloud. (not searched)
</builder_notes>

<investor_notes>
- Burn multiple and net revenue retention come from software company analysis. AI companies with heavy compute costs may need gross margin read alongside them.
- Hyperscaler and neocloud are industry labels, not legal or regulatory categories, so each analyst may draw the line differently.
- MCP and some hardware definitions rest on third-party glossaries. They are fine for teaching but weak for a board paper.
- Useful life is an accounting estimate. A longer life for GPUs lowers yearly depreciation and lifts profit, so ask which life the company uses. IAS 16 says wear and obsolescence both count.
- Backlog and remaining performance obligation are not the same number. Ask which one a company quotes and which contracts it leaves out.
- SLA credits are small and apply to future bills only, so an SLA is not real protection against an outage.
</investor_notes>
</topic>

<topic key="T20" name="Third round: last definitions">
<group name="T20a. Definitions">
- [A.2] Parameter: a number inside a neural network, mainly a weight or a bias, that the model learns during training. Reported, undated page read 26 November 2026 [T20-S1]
- [A.2] Weight: a number that shows how much importance the model gives to one input. Biases are constants added to a signal. Reported, undated page read 26 November 2026 [T20-S1]
- [A.2] Parameter versus hyperparameter: parameters are learned during training, while hyperparameters are set by people before training starts. Reported, undated page read 26 November 2026 [T20-S2]
- [A.2] API: an application programming interface is a way for one piece of software to talk to another, set out as a contract of service. Reported, undated page read 26 November 2026 [T20-S3]
- [A.2] API roles: the application that sends the request is the client, and the application that sends the response is the server. Reported, undated page read 26 November 2026 [T20-S3]
- [A.2] AI data centre: Nvidia calls it an "AI factory", a computing site built to manage the whole AI life cycle, from data to training to inference. Reported, undated page read 26 November 2026 [T20-S4]
- [A.2] AI factory versus normal data centre: a normal one runs many general tasks, while an AI factory is tuned for AI work and its product is intelligence, measured in token output. Reported, undated page read 26 November 2026 [T20-S4]
- [A.2] AI factory hardware: Nvidia lists GPUs, CPUs, networking, storage and advanced cooling. This is a vendor definition and carries a sales aim. Reported, undated page read 26 November 2026 [T20-S4]
- [A.2] Benchmark: IBM defines an LLM benchmark as a standardised dataset or set of tasks used to score how well a language model performs. Reported, undated page read 26 November 2026 [T20-S5]
- [A.2] Benchmark limit: IBM says benchmarks cannot predict how a model will work in the real world, and models can overfit to them. Reported, undated page read 26 November 2026 [T20-S5]
- [A.2] Benchmark accuracy: NIST separates accuracy on the benchmark questions from accuracy on the wider set of similar questions. Reported, 2026 [T20-S6]
- [A.2] Foundry: a factory that makes chips to the designs of other companies. A pure-play foundry sells little or nothing of its own design. Uncertain, undated secondary glossary [T20-S7]
- [A.2] Fabless company: a firm that designs chips but owns no factory, and pays a foundry to make them. TSMC is the best-known foundry. Uncertain, undated secondary sources [T20-S7]
- [A.2] Rack: a standard metal frame that holds servers, storage and network gear in stacked slots called rack units. Uncertain, undated vendor glossary [T20-S8]
- [A.2] Rack size: one rack unit (1U) is 1.75 inches high, and rack equipment is usually 19 inches wide. Uncertain, undated vendor glossaries [T20-S8]
- [A.2] GPU utilisation: on AWS CloudWatch it is the percentage of a sample period in which one or more kernels were running on the GPU. Reported, undated page read 26 November 2026 [T20-S9]
- [A.2] Utilisation trap: a GPU can show near 100 percent utilisation while using only one fifth of its compute units, so the figure can overstate real use. Reported, undated FinOps page [T20-S9]
- [A.2] Utilisation averages hide idle chips: one busy GPU and seven idle ones average 12.5 percent, which hides the seven idle devices. Reported, undated FinOps page [T20-S9]
- [A.2] Run-rate revenue: FiscalNote defines it as annual recurring revenue plus non-subscription revenue earned in the last twelve months. Reported, 2022 filing, old source [T20-S10]
- [A.2] Run-rate revenue, other form: BigCommerce adds current monthly recurring revenue times 12 to trailing twelve-month non-recurring revenue. Reported, 2022 filing, old source [T20-S11]
- [A.2] Run-rate revenue, narrow form: MSCI counts the annualised value of recurring revenue for the next 12 months and removes contracts with a termination notice. Reported, 13 March 2024, old source [T20-S12]
- [A.2] Run-rate revenue is a company-defined, non-GAAP figure, and actual revenue over the next 12 months may differ from it, sometimes by a lot. Reported, 2022 filing, old source [T20-S10]
</group>

<group name="T20b. How AI, machine learning, deep learning and generative AI fit together (M1.13)">
- [M1.13] IBM describes nested fields: machine learning is a subset of AI, and deep learning is a subset of machine learning. Reported, undated page read 26 November 2026 [T20-S13]
- [M1.13] IBM says deep learning uses multilayered neural networks, and a network with more than three layers, counting input and output, counts as deep learning. Reported, undated page read 26 November 2026 [T20-S13]
- [M1.13] IBM defines generative AI as deep learning models that create complex original content, and it starts with a foundation model. Reported, undated page read 26 November 2026 [T20-S13]
- [M1.13] IBM says foundation models train on huge volumes of unlabelled data, and large language models are the most common type today. Reported, undated page read 26 November 2026 [T20-S13]
- [M1.13] IBM warns that the terms AI, machine learning and deep learning are often used as if they meant the same thing. Reported, undated page read 26 November 2026 [T20-S13]
</group>

<group name="T20c. Temperature setting on flagship models, November 2026 (M2.10)">
- [M2.10] Anthropic docs state that temperature, top_p and top_k are not supported on Claude 4.7 and later models and on Claude Mythos Preview. Reported, read 26 November 2026 [T20-S14]
- [M2.10] Anthropic docs state that a non-default value returns a 400 error, and from API version 2026-10-21 any value does. Leave the fields out. Reported, read 26 November 2026 [T20-S14]
- [M2.10] OpenRouter says the parameters are silently ignored on Claude 4.7, which conflicts with the 400 error that Anthropic describes. Uncertain, undated gateway guide [T20-S15]
- [M2.10] Older Claude models, from the 3.x line to Opus 4.6, still accept temperature, per third-party guides. Uncertain, undated [T20-S14]
- [M2.10] Google states that for all Gemini 3 models it strongly recommends the default temperature of 1.0, and lower values may cause looping or worse results. Reported, read 26 November 2026 [T20-S16]
- [M2.10] Google Cloud documents the Gemini temperature range as 0.0 to 2.0 with a default of 1.0, so Gemini 3 still accepts the setting. Reported, read 26 November 2026 [T20-S17]
- [M2.10] Microsoft Azure documents that OpenAI reasoning models, other than GPT-6 Astra, do not support temperature, top_p or logprobs. Reported, read 26 November 2026 [T20-S18]
- [M2.10] Microsoft Azure documents that GPT-5.5 supports reasoning effort "none". Whether temperature then works on GPT-5.5 is not settled in the sources. Uncertain, read 26 November 2026 [T20-S18]
- [M2.10] A third-party arXiv paper says gpt-5.1, 5.2 and 5.4 accept temperature 0, while gpt-5.5 and later models do not. Estimate, 2026 [T20-S19]
</group>

<builder_notes>
- Never hard-code temperature across providers. Make it an optional field and drop it for models that reject it, since the call fails with a 400 error otherwise. (not searched)
- Guide Claude 4.7 and later behaviour with prompts, not sampling knobs. Anthropic says to omit the fields.
- For Gemini 3, leave temperature at 1.0. Low values for "determinism" are a known cause of loops, per Google.
- OpenAI reasoning models use effort settings in place of temperature. Test each model with a real call, because rules differ by model and effort level.
- GPU utilisation from CloudWatch or nvidia-smi shows time busy, not compute used. Measure SM activity or tokens per second per GPU to see real efficiency.
- Average utilisation across a multi-GPU node can hide idle cards. Report per GPU.
- A benchmark score only describes the benchmark questions. Build a private test set for your own task, and watch for overfitting to public tests.
</builder_notes>

<investor_notes>
- "Run-rate revenue" is not audited revenue. Ask for the company's own definition and whether it includes one-time, usage-based or non-subscription income.
- A run-rate multiplies one recent month by 12. It overstates a business with seasonal or lumpy usage and ignores churn.
- "Utilisation" claims from AI cloud firms need a definition. Time-busy utilisation can read near 100 percent while real compute use is far lower.
- "AI factory" is Nvidia's marketing term for an AI data centre. It describes the same kind of asset, but the pitch aims to sell more hardware.
- A foundry owns the costly factory risk, while fabless firms carry design risk. TSMC dominates the pure-play model.
- Loss of temperature control on newer models limits how much a buyer can tune output. Some firms may see this as lost control, others as simpler products.
- Vendor and standards-body definitions differ. Use one named source per term in board material.
</investor_notes>
</topic>

<not_in_the_data>
The research did not find these items, or did not resolve them. Do not supply them from memory.
Topic T1, Models, and how engineers use them:
- The official METR time-horizon page and the November 2026 report values were not re-confirmed. The search only returned the January 2026 update (131 and 89 day doubling times).
- The official ARC Prize leaderboard top score was not confirmed. Only aggregators and a harness entry were seen.
- No official GDPval figure for GPT-6.2 Astra or Fable 5.2 was found.
- No official xAI flagship name, date or context window was found, and Grok 4.7 is unverified.
- Mistral Large 4 context window and parameter count have conflicting sources.
- No official guidance on retrieval versus 1,000,000-token context was found. Anthropic's contextual retrieval figure was not found.
- No source ranked evaluation as the hardest part of building with AI. Only an observability versus evaluation gap was found.
- No updated Cursor or Copilot figures from company statements after January 2026, and Claude Code after February 2026.
- No 2026 measured agent success rate on office tasks was found, only 2025 studies. The official Anthropic note on SWE-bench contamination was not searched again, since the first report has OpenAI's note.
Topic T2, Model prices and token economics:
- No published cost for one chatbot answer, and none from Cursor or GitHub for one agent session, was found.
- Prompt caching savings reported by suppliers themselves (Anthropic, OpenAI) were not found, only customer and blog figures.
- Bedrock base prices against Anthropic direct prices were not compared in any source.
- Exact OpenAI Tier 1 requests and tokens for each minute were not confirmed. The 7-day Tier 2 wait was not confirmed.
- Anthropic Tier 1 limits for current Fable and Opus 5.5 models were not confirmed, and the tier of the Fable 5.x row is unknown.
- Speed for GPT-6.2 Astra, Gemini 4 and small models from Artificial Analysis was not found. Opus 5.5 pages conflict.
- gpt-oss-120b on Together AI was not found. OpenAI's own wording on reasoning token billing was not seen.
- Batch and shorter-context savings from published production studies were not found.
Topic T3, Chips and hardware:
- Not found: a measured 2026 H100 failure rate from an operator. Only the Meta-derived 9 per cent estimate and the Delta study exist.
- Not found: H100 against H200 rental gap, and a primary Silicon Data resale percent of original price.
- Not found: official unit volumes for Trainium, Maia and MTIA in 2026, and cost against Nvidia from an independent test. Google 4.3 million TPU figure not re-confirmed.
- Not found: an independent per-watt or per-dollar test of Vera Rubin. All figures are Nvidia claims or Nvidia-cited.
- Not found: InfiniBand and Ethernet shares for the second or third quarter of 2026, and technical limits of co-packaged optics.
- Not found: a Counterpoint third quarter 2026 HBM share. TSMC capex ($60 billion to $64 billion) and HPC share (68 per cent) were not re-searched, see T3.
- Not found: AMD Instinct revenue on its own, and exact Nvidia price of a new H100.
- Not found: OpenAI and Broadcom status in November 2026, and a company-stated chip cost.
- The Epoch cost-share table (52 per cent) and the Q4 2025 figure (63 per cent) conflict on its page, so period is unclear.
Topic T4, Data centres and energy:
- A first-source, full cost split of 1 GW by chips, network, building, power and cooling. Only Epoch's annualised split and secondary splits were found.
- Electricity share of annual cost is only the search tool's rough check (about 12 per cent). Epoch's spreadsheet line was not seen.
- Transformer backlog for Europe. One trade source says 5 to 6 years for large units, which is unconfirmed.
- On-site gas prices for xAI and OpenAI Abilene. Only modelled ranges were found.
- Yield on cost for European developers. Not found, and only Digital Realty's US figure exists.
- Lease rates for Amsterdam and Paris, and any Cushman & Wakefield figures. Not found.
- Global landlord ranking with Vantage and NTT. Only a US ranking by ABI and Equinix at 3.0 GW were found.
- Hyperion and Stargate status in November 2026 beyond Abilene. Latest coverage is July to September 2026.
- A direct EUR/USD rate. Not found.
- Cause of the October 2025 AWS outage. Not searched.
Topic T5, Compute markets, depreciation and finance:
- Not found: total CoreWeave debt and rates from the 10-Q, Crusoe loan rates, Lambda and IREN balance sheet totals, and the Oracle total debt.
- Not found: Microsoft calendar 2025 capex, and Amazon's exact figure from the release (only press "about $131 billion").
- Not found: Google's total stake in Anthropic, Microsoft's total OpenAI funding and Nvidia's final xAI amount.
- Not found: any official payback period or return on invested capital from CoreWeave or IREN. Only the Nebius 22 months from a secondary source.
- Not found: Alphabet and Lambda useful life, a 2025 row of the SemiAnalysis index, a GB200 rental price, and Nvidia's claim that old H100 chips re-rented at a higher price.
- Not found: late 2026 waiting times and minimum contract sizes. Only 2026 mid-year sources.
- Not found: a full split of installed chips between clouds, GPU clouds and labs. Epoch has partial data and says Microsoft and Amazon are not fully covered.
- Not found: JPMorgan gap estimate.
Topic T6, Model companies:
- No first-source figure for inference gross margin on API versus subscriptions. Only Epoch, Axios and press estimates found.
- Total funding raised by Anthropic and OpenAI is not found as a sum. Amazon and Google equity totals for Anthropic not found.
- No newest training cost per frontier model and no figure for the largest single training run cluster beyond Epoch's 1.1 million H100e data centre.
- No split of API use by task from the Anthropic Economic Index, only direction. Per-task shares from OpenRouter are via a summary.
- Model life: only the 41-day and four-month figures. No price change on older models found.
- Alibaba, Google and Meta model revenue not found. Chinese lab revenue is third-party estimates.
- Run-rate above $100 billion on 18 September 2026 not checked. The Anthropic S-1/A figures were not read on EDGAR.
Topic T7, Application infrastructure:
- Not found: Vertex AI and Microsoft Foundry prices against the direct API, and the Cloudflare AI Gateway price.
- Not found: Cloudflare Vectorize rates, Cloudflare Business price, and whether Workers charge any egress.
- Not found: Supabase and Vercel compliance with ISO 27001 for Supabase, and EU data residency for Vercel.
- Not found: surveys of AI start-up stacks, and a named company case with a stated saving for a move between a platform and AWS.
- Not found: measured bills for 1,000, 100,000 and 1,000,000 users. Only vendor blog estimates exist.
- Not found: official Alphabet and Microsoft third-quarter 2026 releases. The 103 per cent and 48 per cent figures rest on one secondary source.
- Not found: causes for the Supabase and Vercel 2026 incidents, and any 2026 AWS post-event summary. The Vercel 1,800-second limit status is still unresolved.
- Not found: Vercel Series F revenue or any 2026 Vercel round from a primary source.
Topic T8, AI software businesses, adoption and investment:
- Gap 2: no published evidence found on moats (private data, own models) or on a dated case where a model maker release removed a start-up product. Only 2023 PDF upload commentary and unverified 2026 posts turned up.
- Gap 3: the Google internal trial figure and the GitHub 55 per cent speed-up attribution were not confirmed. METR is in the first report.
- Gap 4: no named-company share of code beyond the first report, and no verified 2026 Microsoft or Meta figure.
- Gap 5: IBM CEO study causes were not found.
- Gap 7: no source quantifies the revenue effect of a move from seat to usage prices. Intercom ARR comes from Sacra only.
- Gap 8: no Harvey or Glean gross margin found. Replit and Lovable figures are from 2025 and are Sacra or The Information.
- Gap 9: no McKinsey figure on PE portfolio AI value found. The FTI and PwC lines come from search summaries, not the reports.
- Gap 1: full checklists from advisory firms were paywalled or blocked, so strong and weak answer signs come from summaries of blog guides.
- ONS: the 38 per cent figure for firms with 10 or more staff came from a search summary of the 8 October 2026 bulletin. The ONS page was not opened.
Topic T9, Basic terms, and the mechanism of a language model:
- Exact ISO/IEC 22989 wording for AI, machine learning, model, parameter, training and inference was not found. ISO text sits behind a paywall.
- No standards-body or glossary definition of deep learning with clear wording was found. Only IBM's description was found. The Google glossary entries for deep learning, parameter and inference could not be read.
- The Attention Is All You Need parameter counts (about 65 million base, 213 million big) were found only on a third-party page. The paper's Table 3 could not be opened. Do not use them until checked.
- No measured same-model comparison with and without reasoning gave a clean score gain plus extra cost or time. Only the 2024 o1 against GPT-4o pair and an ambiguous Qwen3 pair were found.
- No hallucination rate published by Anthropic for a named current model was found. The OpenAI GPT-5 rates came from press summaries, not the system card text.
- OpenAI's and Google's model pages could not be opened directly. Their modality and cut-off facts come from search summaries of those pages.
- Mistral licences for named models were not read from Mistral's own model cards. The full gpt-oss usage policy text was not read.
- No supplier guide from Dell or Lambda for a 70 billion model was found. NVIDIA and vLLM material was used instead.
- No first-source video input or output check for GPT-6 Astra beyond the model page summary. Image and audio output for Claude and GPT-6 were not found.
Topic T10, Software engineering foundations and security:
- The session network blocked fetching genai.owasp.org, owasp.org, dora.dev, services.google.com, web.dev, MDN, opentelemetry.io, martinfowler.com and developers.openai.com. So the official DORA 2024 table (elite and high rows), the full OWASP 2026 order, the web.dev and MDN timing tables and the OpenAI memory API page are unread first sources.
- No first-source typical time for a model call exists. Only Anthropic's definition of time to first token was found.
- DORA 2025 "harmonious high-achievers" share and the full list of seven AI capabilities were not confirmed.
- Documented non-engineer cases beyond the Google AI Studio case study and the vendor studies were not found. No peer-reviewed security study of non-programmer apps was found.
- Named advisory firm thresholds: only Umbrex framing and consultancy blogs were found.
- Rollback and staged release: no Google Cloud or Fowler primary page was read. Fowler claims come from search snippets.
Topic T11, The value chain, compute owners and KPI definitions:
- Sierra resolution rate: not found. Sierra published none in the searches.
- Burn multiple for AI against SaaS: not found.
- Net revenue retention for AI-native firms alone: not found. Only all-SaaS figures.
- A quality target for 95th percentile latency (apart from rules of thumb), error rate norms, and requests for each second: not found.
- Cost for each active user and cost for each resolved case: not found as survey figures. Only a modelled example and Intercom's $0.99 outcome price.
- Epoch shares by owner type, with numbers for GPU clouds, model companies and governments: not found. Epoch gives text only.
- A single named total of 2026 AI product revenue: not found. Estimates range from $63 billion to over $175 billion by scope.
- Anthropic market value on a date after 19 November: not found. The first-day close of $97.17 comes from one live blog.
- Microsoft Cloud gross margin actual for the quarter to September 2026: unconfirmed (65% guide, 66% in one outlet).
- Google Cloud Q3 operating income and the Alphabet release were not checked against the primary release.
- Revenue for each MW at Applied Digital and Lambda: not found. WebFetch was not used, so no primary pages were opened.
Topic T12, Regulation, law, risk and safe purchase:
- Not found: Microsoft default retention period, AWS Bedrock storage terms, and Google's 55 day or 24 hour figures.
- Not found: Anthropic, OpenAI or AWS UK or EU in-region inference confirmation. The OpenAI UK residency year is unconfirmed.
- Not found: spend commitment sizes and common SLA norms beyond one sample 99.5% uptime. No named purchase checklist was read in full.
- Not found: the FinOps Foundation figure for AI spend growth, and any neutral waste figure.
- Not found: FRC guidance for boards, ISS 2026 AI policy text, and the SEC Presto case.
- Not found: Deloitte refund confirmed from official records, and the cost of the NYT and Midjourney outcomes.
- Not found: official ISS or ISO count of 42001 certificates, Gartner follow-up in 2026, and Taiwan's share by a named research group.
Topic T13, The path to expert:
- Oxford fee: £2,300 seen on the SBS page, but the year is missing and $3,390 was not found again. Check GetSmarter.
- Technical due diligence at named firms (Blackstone, KKR, Carlyle, EQT, General Catalyst) was not found. Only consultancy and vendor content.
- No study links technical knowledge to investor returns, and no study of hours to AI proficiency.
- Not found: Stratechery 2026 price, SemiAnalysis price, Latent Space price, Dwarkesh and Hard Fork pricing (both assumed free, not confirmed), The Batch free tier.
- Not found: lengths of Introduction to MCP, Claude Code in Action and 3Blue1Brown chapter 5. fast.ai 2025 edition unconfirmed.
- Not searched: RAISE Summit and further UK communities beyond those listed. Search budget of 20 was used.
Topic T14, Third round: the mechanism of a language model, and core terms:
- [M1.7] Parameter (weight), AI data centre and API: no glossary or standards definition was found. Only prompt and hyperscaler were closed. The search budget of 20 ended first.
- [M1.13] No standards body or major report showing the full nest of AI, machine learning, deep learning, generative AI, large language model and agent was found. IBM and Cornell cover the first three only.
- [M2.10] Which current flagships accept temperature is not fully closed. OpenAI's current GPT-6 rules and Anthropic's Opus 5.5 and Sonnet 5.5 pages were not read. Only Gemini 3 and Fable 5.2 (via T9B) are covered.
- [M2.8] No official 2026 fine-tuning price from Anthropic, Amazon Bedrock, OpenAI or Google was confirmed. No official supplier guide on fine-tuning versus retrieval was found, only third-party teaching sources.
- [M2.5] The quadratic cost wording comes from course notes and tutorials. Google, NVIDIA and IBM pages were not shown to state it. The 3Blue1Brown claim comes from summaries, not the video.
- [M2.20] No one source lists all the steps from prompt to streamed answer. The chain is assembled from several sources.
- [M2.3] Karpathy and softmax explanations rest on secondary write-ups. The original video and Google or OpenAI explainers were not read.
- [M4.13] No source gives a staff-time or cost figure for leaving CUDA. "Multi-week" is an analyst phrase.
Topic T15, Third round: money flow, lasting advantage and product tests:
- M7.16, C12: partly closed. No numeric thresholds found from a16z, Bessemer, Sequoia, Menlo, NFX or Bain. Only ICONIQ margin figures exist. Primary a16z and Bain texts were not reached.
- M7.12: partly closed. Microsoft and Salesforce figures found. No dated case of a start-up losing to a bundled Microsoft or Google feature was found beyond Glean and Slack.
- M7.11 and M7.14: not closed. No measured retention or margin gain from private data or switching costs was found. Only price-band retention and Ramp switching data.
- M7.13: partly closed. Dated cases found are the Cowork legal plugin, the 2023 PDF update and Chegg. Tome, Rewind and Jasper were not confirmed.
- M7.15: partly closed. Cursor only. No Intercom Fin own-model margin data was found.
- M7.18: partly closed. No measured tokens per request, requests per user per month or tokens per resolved case. Only modelled figures and price per resolution.
- M1.11: partly closed. Sizes found for each layer, but no single flow table. Payments from model firms to each cloud and cloud spend on energy were not found.
- Search budget of 20 was used. Dates for the Microsoft 30 million seat figure vary by source (July 2026 or fiscal Q4).
- Conflict: Menlo 2025 spend of $37 billion against a restated $33 billion is in T8. Run rates for OpenAI differ ($24 billion in April, above $40 billion later).
Topic T16, Third round: hardware power, cost splits and GPU unit economics:
- [M4.10] Typical size of an AI data hall in MW: not found. Only vendor designs of 1.2 MW and 7.4 MW were found.
- [M4.6] The H100 700 W figure was not found on an Nvidia datasheet in this search. It rests on the Nvidia H200 page and press.
- [M6.15, C5] A first-source share of storage in cluster cost: not found. Network share is only Epoch's annualised ratio and an opinion range of 10 to 30 per cent.
- [M5.13] A first-source percentage split of 1 GW into chips, network, building, electrical, cooling and land: not found. Epoch gives dollar lines for servers, facility and network only. JLL was not found.
- [M6.7] A CoreWeave payback figure from a filing: not found. Third-party analyses cite 2.25 to 2.5 years. A clean non-power opex per GPU-hour from CoreWeave, Nebius or IREN: not found. Only derived figures from Epoch and a SemiAnalysis-style Meta model.
- [M6.3] Official AWS 1-year and 3-year Savings Plan rates for p5, RunPod spot price and CoreWeave reserved terms: not found.
- [M5.7] The Epoch page was read only through search summaries, so the energy line of $594 million is also quoted by a secondary blog.
Topic T17, Third round: platform choice and first limits:
- [M8.19] No neutral survey of AI start-up stacks was found. The Supabase survey is a seller's. No source shows Cloudflare in front of AWS as a common pairing.
- [M8.20, M8.33, C8] No independent comparison by stage and need was found. Most sources are suppliers (Qovery, a consultancy) or single company posts. The Monk and Graphite posts were seen only as titles or snippets.
- [M8.34] Not closed. No measured monthly bill at 1,000, 100,000 or 1,000,000 users exists in the results. Only invoice examples, estimates and surprise-bill anecdotes.
- [M8.35] Lambda cold-start duration in milliseconds was not found. Vercel concurrency limits and Supabase incident accounts naming the pooler were not found beyond forum threads.
- [M8.35] The number of engineers a company needs to run its own AWS setup was not found. Only general headcount ratios exist.
- [M8.35] The Vercel "6 engineers" story and the Resend stack page were not opened, so company name, scale and stack details are unconfirmed.
- The search budget of 20 searches was used in full.
Topic T18, Third round: application KPIs, technical review and skill levels:
- [M9.20] Typical RPS for a small and a middle-size application: not found. Only the conversion method and API limits were found.
- [M9.19] An error rate target for web services in the SRE book or AWS paper: closed only by derivation from 99.9% and 99.99% availability. No published model API 5xx rate found.
- [M9.21] Cost per monthly active user or paid seat at AI software firms in 2025 and 2026: not closed. Only margins, one illustration and Copilot press figures found.
- [M9.2] Release practice and team: weak coverage. No named investor checklist (Bessemer, a16z, Sequoia) found. Sources are vendor and practitioner guides.
- [M9.10] Levels equal to aware, fluent, practitioner and expert: not found in any framework. OECD and Commission proficiency tiers not confirmed.
- [M9.11, M9.22] Published 12-week plan with hours per week and a result: not found. Masai total length unconfirmed.
- The search budget of 20 searches was used in full. No page was fetched.
Topic T19, Third round: glossary definitions:
- Benchmark: no high-quality definition found. The OpenAI search returned only secondary blogs, so no line is written.
- Foundry: TSMC pages were found but none defines the word, so no line is written.
- Rack: no source defines it. Vertiv mentions rack space and kW per rack only, so no line is written.
- Utilisation: not searched, no line is written.
- Run-rate revenue: the one search found no definition, so no line is written.
- Throughput, GPU, FLOPs, front end, back end and egress rest on third-party glossaries or snippets, not a first source. Labelled Estimate. The MDN glossary page for front end and back end was not reached.
- Sources are mostly undated pages, so "accessed 26 November 2026" is used. Definitions came from search snippets, not from opened pages.
- Search budget of 20 was used.
Topic T20, Third round: last definitions:
- Foundry: no Semiconductor Industry Association, ASML or Intel definition found. The line rests on weaker glossary sources (labelled Uncertain). Closed only in part.
- Rack: no Equinix, Cisco or HPE glossary entry found. Lines rest on vendor glossaries (ExpressVPN, Lenovo) and are labelled Uncertain. Closed only in part.
- M2.10: the Anthropic docs state the rule for "4.7 and later" but I could not confirm in Anthropic's own docs which exact newest models (Sonnet 5, Opus 4.8, others) are covered. One third-party blog says they are.
- M2.10: OpenAI's own current API page was not reached. Whether GPT-5.5 accepts temperature at reasoning effort "none" is unresolved, and sources conflict.
- Most definition pages carry no visible publication date. They are marked "undated page read 26 November 2026".
- The Google machine learning glossary entry for "parameter" was not found. IBM was used instead.
- The AWS CloudWatch and FinOps wording came from a search summary and was not seen on the page.
- The NIST wording on benchmarks came from a search summary of NIST AI 800-3 and its date is approximate.
</not_in_the_data>

<sources>
[T1-S1] OpenAI developer docs, GPT-6.2 Astra model page, November 2026. https://developers.openai.com/api/docs/models/gpt-6.2-astra.md
[T1-S2] Artificial Analysis, GPT-6.2 Astra and GPT-6 Astra model pages, and DeepLearning.AI The Batch, 2026. https://artificialanalysis.ai/models/gpt-6-2-astra-high
[T1-S3] Anthropic, Claude Opus 5.5 announcement and Claude Platform release notes, September 2026. https://platform.claude.com/docs/en/release-notes/overview
[T1-S4] Anthropic, Claude Mythos 5.1 model overview, September 2026. https://platform.claude.com/docs/en/models/mythos-5-1/overview.md
[T1-S5] Google AI for Developers, Gemini 4 Argon, and The New Stack, October 2026. https://ai.google.dev/gemini-api/docs/models/gemini-4-argon
[T1-S6] MindStudio, NXCode and others, Grok 5 release reports, 2026. https://www.mindstudio.ai/blog/grok-5-release-date-specs
[T1-S7] Meta, Introducing Muse Spark, April 2026, and TechCrunch, 12 October 2026. https://about.fb.com/news/2026/04/introducing-muse/
[T1-S8] DeepSeek API docs, V4 Preview Release, 24 April 2026. https://api-docs.deepseek.com/news/news260424.md
[T1-S9] NYU Shanghai RITS and Forkast News, Kimi K3 and Chinese open-weight releases, July 2026. https://rits.shanghai.nyu.edu/ai/kimi-k3-open-weights-ship-2-8t-parameters-1-4-tb-to-run/
[T1-S10] Mistral AI docs, Mistral Large 3, December 2025. https://docs.mistral.ai/models/mistral-large-3-25-12
[T1-S11] METR, Q4 2026 capability update, 20 November 2026, with secondary summaries. https://metr.org/blog/2026-11-20-q4-2026-capability-update/
[T1-S12] METR, Time Horizon 1.1, 29 January 2026. https://metr.org/blog/2026-01-29-time-horizon-1-1/
[T1-S13] Creuto and llm-stats, ARC-AGI-2 leaderboard summaries, September 2026. https://creuto.com/arc-agi-2-benchmark-general-reasoning-gap
[T1-S14] ARC Prize, ARC Prize 2025 Results and Analysis, 2025. https://arcprize.org/blog/arc-prize-2025-results-analysis
[T1-S15] llm-stats and Artificial Analysis, Humanity's Last Exam boards, 2026, and Epoch AI benchmark review. https://www.artificialanalysis.ai/evaluations/humanitys-last-exam
[T1-S16] Vals AI and Vellum, Claude Opus 5.5 vs GPT-6 Astra comparisons, 2026. https://www.vals.ai/comparisons/anthropic_claude-opus-5-5-vs-openai_gpt-6-astra
[T1-S17] Codersera, Claude Opus 5.5 complete guide, 2026. https://codersera.com/blog/claude-opus-5-5-complete-guide-2026/
[T1-S18] Epoch AI, open versus closed ECI gap, May and October 2026, and UK AISI. https://epoch.ai/data-insights/open-closed-eci-gap
[T1-S19] OpenRouter, State of Play newsletter and October 2026 data recap. https://openrouter.ai/zh-CN/data/october-2026
[T1-S20] OpenAI, Why we no longer evaluate SWE-bench Verified, February 2026. https://openai.com/index/why-we-no-longer-evaluate-swe-bench-verified/
[T1-S21] Artificial Analysis, AA-Omniscience, November 2025, and Suprmind, October 2026. https://artificialanalysis.ai/articles/aa-omniscience-knowledge-hallucination-benchmark
[T1-S22] METR, Uplift update, 24 February 2026, and July 2025 trial. https://metr.org/blog/2026-02-24-uplift-update/
[T1-S23] Anthropic, Create a Message API reference. https://platform.claude.com/docs/en/api/messages/create
[T1-S24] OpenAI, Reasoning guide and migrate to Responses. https://developers.openai.com/docs/guides/migrate-to-responses
[T1-S25] MCP blog, The 2026-07-28 Specification, and DigitalApplied MCP statistics. https://blog.modelcontextprotocol.io/posts/2026-07-28/
[T1-S26] Vector database guides and Actian, 2026. https://www.actian.com/blog/developer/state-of-vector-databases-q2-2026/
[T1-S27] LangChain, State of Agent Engineering, 2026. https://langchain.com/state-of-agent-engineering
[T1-S28] Berkeley-led, Measuring Agents in Production, December 2025. https://arxiv.org/html/2512.04123v3
[T1-S29] Stack Overflow, 2026 developer survey results, 6 October 2026. https://stackoverflow.blog/2026/10/06/the-results-of-the-2026-developer-survey-are-here/
[T1-S30] Hyperresearch, Who is winning AI coding agents, October 2026, quoting company figures. https://hyperresearch.ai/samples/ai-coding-agents
[T1B-S1] Anthropic, Claude Platform release notes and Introducing Claude Fable 5.2 and Claude Mythos 5.2, 9 November 2026. https://platform.claude.com/docs/en/release-notes/overview
[T1B-S2] Anthropic, Claude Mythos 5.2 model overview, November 2026. https://platform.claude.com/docs/en/models/mythos-5-2/overview
[T1B-S3] eesel.ai, Claude Mythos 5.2 access, pricing and benchmarks, November 2026. https://www.eesel.ai/blog/claude-mythos-5-2
[T1B-S4] MindStudio, NXCode, CometAPI and others, Grok 5 reports, 2026. https://www.mindstudio.ai/blog/grok-5-release-date-specs
[T1B-S5] Mistral changelog and eWeek, Mistral Large 4 enters preview, October 2026. https://docs.mistral.ai/resources/changelogs
[T1B-S6] Gartner, Over 40% of agentic AI projects will be cancelled by end of 2027, 25 June 2025. https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-predicts-over-40-percent-of-agentic-ai-projects-will-be-canceled-by-end-of-2027
[T1B-S7] Carnegie Mellon, TheAgentCompany, and The Register, 29 June 2025. https://arxiv.org/abs/2412.14161
[T1B-S8] MIT NANDA, The GenAI Divide, via Fortune and The Register, 18 August 2025. https://fortune.com/2025/08/18/mit-report-95-percent-generative-ai-pilots-at-companies-failing-cfo/
[T1B-S10] Redis, SitePoint and an arXiv paper on retrieval versus long context, 2025 to 2026. https://redis.io/blog/rag-vs-large-context-window-ai-apps/
[T1B-S11] TechCrunch, Meta's vanilla Maverick ranks below rivals, 11 April 2025. https://techcrunch.com/2025/04/11/metas-vanilla-maverick-ai-model-ranks-below-rivals-on-a-popular-chat-benchmark
[T1B-S12] Singh et al., The Leaderboard Illusion, April 2025. https://arxiv.org/abs/2504.20879
[T1B-S13] OpenAI, Introducing GPT-5.5, and GDPval, 2025 to 2026. https://openai.com/index/introducing-gpt-5-5/
[T1B-S14] ARC Prize leaderboard, llm-stats and Epoch AI review of ARC-AGI-3, 2026. https://arcprize.org/leaderboard
[T1B-S15] Anthropic, Demystifying evals for AI agents, January 2026. https://www.anthropic.com/research/demystifying-evals-for-ai-agents
[T1B-S16] LangChain, State of Agent Engineering, 2026. https://langchain.com/state-of-agent-engineering
[T1B-S17] Bloomberg, Simon Willison and FourWeekMBA on Claude Code run rate, 2026. https://simonwillison.net/2026/Feb/12/anthropic/
[T1B-S18] TechCrunch and Bloomberg, Cursor annualised revenue, March and June 2026. https://techcrunch.com/2026/03/02/cursor-has-reportedly-surpassed-2b-in-annualized-revenue
[T1B-S19] TechCrunch, Fortune, Digg and The Next Web on Codex and Copilot, 2026. https://techcrunch.com/2026/01/29/satya-nadella-insists-people-are-using-microsofts-copilot-ai-a-lot
[T2-S1] BenchLM, Claude API Pricing (November 2026), and Reflekt Lab, Claude API pricing, November 2026. https://benchlm.ai/anthropic/api-pricing
[T2-S2] Anthropic, Pricing and Prompt caching documentation, accessed November 2026. https://platform.claude.com/docs/about-claude/pricing
[T2-S3] OpenAI, ChatGPT Rate Card, and CloudZero, OpenAI API pricing in 2026, November 2026. https://www.cloudzero.com/blog/openai-pricing/
[T2-S5] Apidog, Gemini 4 Argon pricing, November 2026. https://apidog.com/blog/gemini-4-argon-pricing/
[T2-S6] Google, Gemini API and Vertex AI pricing pages, November 2026. https://ai.google.dev/gemini-api/docs/pricing
[T2-S7] Morph, xAI Grok API Pricing (2026), and Metronome pricing index, 2026. https://www.morphllm.com/grok-api-pricing
[T2-S8] Mistral, API pricing, November 2026. https://docs.mistral.ai/inference/pricing
[T2-S9] InfoWorld, DeepSeek raises some V4 prices, and DeepSeek API docs, October 2026. https://www.infoworld.com/article/4209439/deepseek-raises-some-v4-prices-by-more-than-10x-as-ai-demand-strains-capacity.html
[T2-S10] APICostCalc, Groq vs Together vs Fireworks Llama 70B cost, 2026. https://apicostcalc.com/blog/groq-vs-together-vs-fireworks-llama-70b-cost.html
[T2-S11] OpenAI, Fast mode for API customers, and OpenAI pricing documentation, 2026. https://openai.com/api-priority-processing/
[T2-S12] Epoch AI, LLM inference price trends, 2026. https://epoch.ai/blog/llm-inference-price-trends
[T2-S13] Gundlach and others, The Price of Progress, arXiv 2511.23455, November 2025. https://arxiv.org/abs/2511.23455
[T2-S14] Tom's Hardware, report on Stanford 2025 AI Index, 2025. https://www.tomshardware.com/tech-industry/artificial-intelligence/ai-costs-drop-280-fold-but-harmful-incidents-rise-56-percent-in-last-year-stanford-2025-ai-report-highlights-china-us-competition
[T2-S15] The Register, Google touts tokenmaxxing at I/O, 19 May 2026, and Google Q2 2026 CEO remarks. https://www.theregister.com/ai-ml/2026/05/19/google-touts-tokenmaxxing-huge-capex-and-ai-agents-at-i/o/5242983
[T2-S16] OpenRouter, October 2026 data recap. https://openrouter.ai/data/october-2026
[T2-S17] TradingKey and FourWeekMBA, summaries of Microsoft earnings call of 28 October 2026. https://fourweekmba.com/ai-microsoft-says-token-prices-came-in-high-as-foundry-triples/
[T2-S18] Artificial Analysis, gpt-oss-120b provider pages, and Hermes AI news on methodology, 2026. https://artificialanalysis.ai/models/gpt-oss-120b/providers
[T2-S19] OpenAI Help Centre, ChatGPT Business overview, and eesel.ai and tech.co seat guides, 2026. https://help.openai.com/en/articles/8792828-chatgpt-business-overview
[T2-S20] Microsoft Tech Community, Copilot pricing, and Enterprise DNA and TechTarget coverage, 2026. https://techcommunity.microsoft.com/t5/microsoft-365-copilot-blog/act-now-lock-in-current-pricing-on-microsoft-365-copilot/ba-p/4502628
[T2-S21] CloudZero, GitHub Copilot cost, and Cursor pricing pages, 2026. https://www.cloudzero.com/blog/github-copilot-cost
[T2-S22] Google Cloud, Measuring the environmental impact of AI inference, August 2025. https://cloud.google.com/blog/products/infrastructure/measuring-the-environmental-impact-of-ai-inference
[T2-S23] Mistral, Our contribution to a global environmental standard for AI, July 2025. https://mistral.ai/news/our-contribution-to-a-global-environmental-standard-for-ai
[T2-S24] Anthropic, Rate limits documentation, 2026. https://docs.anthropic.com/en/api/rate-limits
[T2-S25] OpenAI, Rate limits and usage tiers documentation, 2026. https://developers.openai.com/api/docs/guides/rate-limits/usage-tiers
[T2-S26] Anthropic, Claude developer reference: models and pricing, 3 November 2026. https://platform.claude.com/docs/en/about-claude/pricing
[T2B-S1] Anthropic, Manage costs effectively (Claude Code), 2026. https://code.claude.com/docs/en/costs
[T2B-S2] DEV Community, Claude Code cost cut after prompt caching, 2026. https://dev.to/paultwist/claude-code-was-costing-us-250devmonth-we-got-it-under-90-27d3
[T2B-S4] OpenAI, o3-deep-research model page, and tokencost.app guide, 2026. https://tokencost.app/blog/openai-deep-research-api-pricing
[T2B-S5] TikTok for Developers, TikTok saves 50 percent with prompt caching, and DigitalOcean prompt caching tutorial, 2026. https://developers.tiktok.com/blog/tiktok-saves-50-percent-with-prompt-caching
[T2B-S6] Berkeley Sky Lab, RouteLLM, 2024, and NeuralTrust routing blog, 2026. https://sky.cs.berkeley.edu/project/routellm/
[T2B-S7] OpenRouter, Simplifying our platform fee, and FAQ, 2026. https://openrouter.ai/blog/announcements/simplifying-our-platform-fee/
[T2B-S8] Vercel, AI Gateway pricing, 2026. https://vercel.com/docs/ai-gateway/pricing
[T2B-S9] Cloudflare, AI Gateway pricing, and Vercel comparison page, 2026. https://developers.cloudflare.com/ai-gateway/reference/pricing/
[T2B-S10] Anthropic, Claude on Amazon Bedrock, and AWS Bedrock pricing, 2026. https://platform.claude.com/docs/en/build-with-claude/claude-on-amazon-bedrock
[T2B-S11] Anthropic, Rate limits, 2026. https://platform.claude.com/docs/en/api/rate-limits
[T2B-S12] OpenAI, Usage tiers, 2026. https://developers.openai.com/api/docs/guides/rate-limits/usage-tiers
[T2B-S13] Artificial Analysis, Claude Opus 5.5 pages, November 2026. https://artificialanalysis.ai/models/releases/claude-opus-5-5
[T2B-S14] Artificial Analysis, Performance benchmarking methodology, 2026. https://artificialanalysis.ai/methodology/performance-benchmarking
[T2B-S15] LessWrong, what the cost difference in processing input vs output, and arXiv 2607.09520, 2026. https://www.lesswrong.com/posts/PLf7tvzujaJ2A2r7N/what-the-cost-difference-in-processing-input-vs-output
[T2B-S16] Apidog and eesel.ai, GPT-6.2 Astra pricing, November 2026. https://apidog.com/blog/gpt-6-2-astra-pricing/
[T2B-S17] Economize and DevelopersDigest, GPT-6 Luna pricing, 2026. https://www.economize.cloud/resources/open-ai/pricing/gpt-6-luna/
[T2B-S18] Google Cloud and developer pricing guides, Gemini 3.1 Flash-Lite, 2026. https://docs.cloud.google.com/vertex-ai/generative-ai/docs/models/gemini/3-1-flash-lite
[T2B-S19] Bifrost LLM cost calculator, gpt-oss-120b, 2026. https://www.getmaxim.ai/bifrost/llm-cost-calculator/provider/groq/model/gpt-oss-120b
[T2B-S20] OpenAI Developer Community, reasoning token billing threads, 2026. https://community.openai.com/t/how-are-reasoning-tokens-cached-tokens-input-tokens-and-output-tokens-counted-for-billing/1386849
[T3-S1] Nvidia, Financial Results for Third Quarter Fiscal 2027, 17 November 2026. https://nvidianews.nvidia.com/news/nvidia-announces-financial-results-for-third-quarter-fiscal-2027
[T3-S2] Nvidia, Third Quarter 2027 CFO Commentary, via MarketScreener, November 2026. https://www.marketscreener.com/news/nvidia-third-quarter-2027-cfo-commentary-ce785edcdc81f420
[T3-S3] Tom's Hardware, The custom AI ASIC state of play, May 2026, and summaries of share estimates. https://www.tomshardware.com/tech-industry/semiconductors/custom-ai-asics-examined-from-broadcom-to-mtia
[T3-S4] Tom's Hardware, Nvidia updates data centre roadmap with Rosa CPU and stacked Feynman GPUs, 2026. https://www.tomshardware.com/pc-components/gpus/nvidia-updates-data-center-roadmap-with-rosa-cpu-and-stacked-feynman-gpus-optical-nvlink-groq-lpus-with-nvfp4-and-nvlink-also-on-deck
[T3-S5] IntuitionLabs, Data centre GPU prices, September 2026, and American Compute HGX B200 server value, October 2026. https://intuitionlabs.ai/articles/data-center-gpu-prices
[T3-S6] Tom's Hardware, Price of Nvidia Vera Rubin NVL72 racks, 2026. https://www.tomshardware.com/tech-industry/artificial-intelligence/price-of-nvidias-vera-rubin-nvl72-racks-skyrockets-to-as-much-as-usd8-8-million-apiece-but-server-makers-margins-will-be-tight-nvidia-is-moving-closer-to-shipping-entire-full-scale-systems
[T3-S7] SemiAnalysis, VR NVL72 BoM + Power, 2026. https://semianalysis.com/?p=150461904
[T3-S8] Broadcom, fiscal third quarter 2026 results and call, September 2026. https://www.nasdaq.com/articles/broadcom-q3-earnings-call-highlights
[T3-S9] Futurum, Marvell Q2 FY 2027, 2026. https://futurumgroup.com/insights/marvell-q2-fy-2027-connectivity-and-custom-silicon-fuel-ai-growth/
[T3-S10] SemiAnalysis, TPUv7 Google takes a swing at the king, and TheNextWeb coverage, late 2025. https://newsletter.semianalysis.com/p/tpuv7-google-takes-a-swing-at-the
[T3-S11] Amazon Q3 2026 results coverage, The Register 29 April 2026 and TheNextWeb 29 October 2026. https://thenextweb.com/news/amazon-q3-earnings-aws-39-free-cash-flow-2027-capex
[T3-S12] Meta, Meta partners with Broadcom to co-develop custom AI silicon, April 2026, and Tom's Hardware ASIC review. https://about.fb.com/news/2026/04/meta-partners-with-broadcom-to-co-develop-custom-ai-silicon/
[T3-S13] Jon Peddie Research, AMD reports third quarter revenue of $13.4 billion, 2026. https://www.jonpeddie.com/news/amd-reports-third-quarter-revenue-of-13-4-billion-up-45-y-y/
[T3-S14] US Commerce BIS, Department of Commerce revises license review policy for semiconductors exported to China, January 2026. https://bis.gov/press-release/department-commerce-revises-license-review-policy-semiconductors-exported-china
[T3-S15] Epoch AI, Huawei's roadmap to 2031, and SemiAnalysis, Huawei Ascend production ramp, 2026. https://epoch.ai/publications/huaweis-roadmap-to-2031
[T3-S16] Counterpoint Research, Global DRAM and HBM market share, 2026. https://www.counterpointresearch.com/insight/global-dram-and-hbm-market-share
[T3-S17] TrendForce, HBM Market Bulletin June 2026 and news of 10 August and 1 September 2026. https://www.trendforce.com/news/2026/08/10/news-samsungs-hbm4-yield-reportedly-hits-80
[T3-S18] TrendForce on HBM contract prices 2027, via Herald Corp, 2026, and Bloomberg memory shortage graphic. https://biz.heraldcorp.com/article/10852833
[T3-S19] Counterpoint Research, Global semiconductor foundry market share, 2026. https://www.counterpointresearch.com/en/insights/global-semiconductor-foundry-market-share
[T3-S20] TheNextWeb, TSMC posts a sixth straight record profit but turns cautious on 2027, October 2026. https://thenextweb.com/news/tsmc-q3-2026-record-profit-prudent-2027
[T3-S21] TrendForce, TSMC CoWoS supply and demand gap, 15 June 2026, and Wccftech on Nvidia booking. https://www.trendforce.com/news/2026/06/15/news-tsmc-cowos-supply-demand-gap-rep
[T3-S22] ASML, Q3 2026 results, October 2026. https://seekingalpha.com/pr/20684919
[T3-S23] American Compute, GPU server values, October 2026, and IntuitionLabs used GPU prices. https://www.amcompute.com/gpu-server-values/h100
[T3B-S1] Nvidia, Why GPUs Are Great for AI. https://blogs.nvidia.com/blog/why-gpus-are-great-for-ai
[T3B-S2] Google Cloud, What is a GPU and its role in AI. https://cloud.google.com/discover/gpu-for-ai
[T3B-S3] Nvidia, What Is AI Inference, and What's the Difference Between Deep Learning Training and Inference (updated October 2025). https://www.nvidia.com/en-us/glossary/data-science/ai-inference
[T3B-S4] Google, Ironwood: The first Google TPU for the age of inference, April 2025. https://blog.google/products/google-cloud/ironwood-tpu-age-of-inference/
[T3B-S5] IBM, What's the difference between AI accelerators and GPUs. https://www.ibm.com/think/topics/ai-accelerator-vs-gpu
[T3B-S6] Tom's Hardware and TrendForce on Meta Llama 3 failures and GPU lifespan, 2024, plus a 2026 research page on H100 failure rates. https://www.tomshardware.com/pc-components/gpus/datacenter-gpu-service-life-can-be-surprisingly-short-only-one-to-three-years-is-expected-according-to-unnamed-google-architect
[T3B-S7] Story of Two GPUs: Characterizing the Resilience of Hopper H100 and Ampere A100 GPUs, SC 25, 2025. https://arxiv.org/abs/2503.11901
[T3B-S8] TrendForce, Datacenter GPUs may have an astonishingly short lifespan of only 1 to 3 years, 31 October 2024. https://www.trendforce.com/news/2024/10/31/news-datacenter-gpus-may-have-an-astonishingly-short-lifespan-of-only-1-to-3-years
[T3B-S9] Silicon Data and SemiAnalysis rental index coverage, via FourWeekMBA and Akash, 2026. https://fourweekmba.com/ai-nvidia-h100-rent-hits-2-88-an-hour-up-44-since-december/
[T3B-S10] AMCompute, H100 Residual Value by Year, 2026. https://www.amcompute.com/gpu-resale-index/residual-value/h100
[T3B-S11] Silicon Data H100 market value trends, and Introl secondary GPU markets guide. https://www.silicondata.com/use-cases/h100-gpu-market-value-trends
[T3B-S12] Tom's Hardware, The custom AI ASIC state of play, May 2026, and Epoch AI AI chip sales methodology. https://www.tomshardware.com/tech-industry/semiconductors/custom-ai-asics-examined-from-broadcom-to-mtia
[T3B-S13] Amazon, Project Rainier, and Wccftech on Anthropic Trainium expansion, 2025 to 2026. https://www.aboutamazon.com/news/aws/aws-project-rainier-ai-trainium-chips-compute-cluster
[T3B-S14] OpenAI, OpenAI and Broadcom announce strategic collaboration, 13 October 2025, and Financial Times estimate via press. https://openai.com/index/openai-and-broadcom-announce-strategic-collaboration/
[T3B-S15] Nvidia, Blackwell InferenceMAX benchmark results and GB300 NVL72 claims, 2025 to 2026. https://blogs.nvidia.com/blog/blackwell-inferencemax-benchmark-results/
[T3B-S16] Tom's Hardware, Nvidia launches Vera Rubin NVL72 at CES, January 2026, and Nvidia blogs on Vera Rubin efficiency. https://blogs.nvidia.com/blog/vera-rubin/
[T3B-S17] Dell'Oro Group, Ethernet more than doubles size of InfiniBand in AI scale-out networks in 2025, and 2026 predictions. https://www.delloro.com/newsroom/ethernet-more-than-doubles-size-of-infiniband-as-the-leading-fabric-for-ai-scale-out-networks-in-2025/
[T3B-S18] Dell and Nvidia networking blogs, and arXiv 2407.12819 and 2605.24326. https://arxiv.org/html/2407.12819v2
[T3B-S19] Epoch AI, AI chip component cost shares, 2026. https://epoch.ai/data-insights/ai-chip-component-cost-shares
[T3B-S20] SemiAnalysis, Tom's Hardware, Wccftech and tech-insider on HBM prices and bill of materials, 2026. https://wccftech.com/nvidia-vera-rubin-rack-hit-with-memory-price-surge-pushing-hbm4-lpddr5x-bill-to-2m-of-7-8m-total/
[T3B-S21] Counterpoint Research, Global DRAM and HBM market share, and DRAM super cycle, November 2026. https://www.counterpointresearch.com/en/insights/dram-super-cycle-nears-dollar-200b
[T3B-S23] Finimize, Sacra and Next Platform on Cerebras and Groq, 2026. https://www.nextplatform.com/compute/2026/11/14/cerebras-readies-cs-5-systems-for-2027-launch-as-it-bags-another-hyperscaler/5309932
[T3B-S24] CloudZero, H100 GPU cost, and IntuitionLabs data centre GPU prices, 2026. https://cloudzero.com/blog/h100-gpu-cost/
[T4-S1] JLL, 2026 Global Data Center Outlook, 2026. https://www.jll.com/en-us/insights/market-outlook/data-center-outlook.html
[T4-S2] IREI, Cushman & Wakefield releases 2026 data center development cost guide, 2026. https://irei.com/news/cushman-wakefield-releases-2026-data-center-development-cost-guide-citing-21-rise-in-per-mw-construction-costs/
[T4-S3] Turner & Townsend, Data centre construction cost index 2026-27, 2026. https://www.turnerandtownsend.com/insights/data-centre-construction-cost-index-2026-27/
[T4-S4] Epoch AI, AI datacenter cost breakdown, 2026. https://epoch.ai/data-insights/ai-datacenter-cost-breakdown
[T4-S5] AI Weekly, Bloomberg pegs Abilene 1GW AI data center at $30B, $17B on chips, 2025. https://aiweekly.co/alerts/bloomberg-pegs-abilene-1gw-ai-data-center-at-30b-17b-on-chips
[T4-S6] Wccftech, Foxconn pegs Nvidia Vera Rubin AI datacenter at $47 billion per gigawatt, 2026. https://wccftech.com/foxconn-pegs-nvidia-vera-rubin-ai-datacenter-at-47-billion-per-gigawatt/amp/
[T4-S7] Epoch AI, Largest AI data centers by power capacity, updated 6 November 2026. https://epoch.ai/graphs/largest-ai-data-centers-by-power-capacity
[T4-S8] Epoch AI, Colossus 2 and Anthropic Amazon New Carlisle directory pages, August 2026. https://epoch.ai/data/ai-data-centers/directory/colossus-2
[T4-S9] Epoch AI, Microsoft Fairwater Wisconsin and Atlanta directory pages, August 2026. https://epoch.ai/data/ai-data-centers/directory/microsoft-fairwater-wisconsin
[T4-S10] Fortune, Meta orders 10 gas-fired power plants for Hyperion, 27 March 2026. https://fortune.com/2026/03/27/meta-hyperion-10-gas-power-plants-louisiana-entergy/
[T4-S11] Tom's Hardware, Oracle and OpenAI scrap planned 600MW Abilene expansion, 2026. https://www.tomshardware.com/tech-industry/oracle-and-openai-scrap-planned-600mw-abilene-expansion
[T4-S12] IEA, Energy and AI, and Key questions on energy and AI, 2025 and 2026. https://www.iea.org/reports/energy-and-ai/energy-demand-from-ai
[T4-S13] Lawrence Berkeley National Laboratory, United States Data Center Energy Usage Report 2025 Update, 2026. https://eta-publications.lbl.gov/publications/united-states-data-center-energy-2025
[T4-S14] E&E News, Data centers' share of US electricity seen doubling by 2030 (EPRI 2026), 2026. https://eenews.net/articles/data-centers-share-of-us-electricity-seen-doubling-by-2030
[T4-S15] Council of the EU, document ST-13443-2026, citing the European Commission, 2026. https://data.consilium.europa.eu/doc/document/ST-13443-2026-INIT/en/pdf
[T4-S16] Oxford Economics, The UK's data centre boom, and NESO written evidence, 2025 and 2026. https://www.oxfordeconomics.com/resource/the-uks-data-centre-boom-growth-trends-drivers-and-the-rising-power-challenge/
[T4-S17] Utility Dive, GE Vernova gas turbine backlog climbs to 116 GW, 2026. https://www.utilitydive.com/news/ge-vernova-gas-turbine-backlog-climbs-to-116-gw/826039/
[T4-S18] Power Magazine, Transformers in 2026, 2026. https://powermag.com/transformers-in-2026-shortage-scramble-or-self-inflicted-crisis/
[T4-S19] GOV.UK, Government to tackle speculative demand grid connection requests, 2026. https://www.gov.uk/government/news/government-to-tackle-speculative-demand-grid-connection-requests
[T4-S20] Cleanview, Behind-the-meter data centers report, and Enverus forecast, 2026. https://cleanview.co/reports/behind-the-meter-data-centers/full-report
[T4-S22] Foley, Constellation and Meta PPA, 2025, and ANS, Kairos TVA Google. https://www.foley.com/insights/publications/2025/06/constellation-and-meta-ppa-tech-ai-and-clean-energy-goals-preserve-existing-nucl/
[T4-S23] EIA, Electric Power Monthly and Prices and factors affecting prices, 2026. https://www.eia.gov/electricity/monthly/epm_table_grapher.php?t=epmt_5_3
[T4-S24] DESNZ, Quarterly Energy Prices September 2026. https://www.gov.uk/government/statistics/quarterly-energy-prices-september-2026
[T4-S25] Brussels Times, EU electricity prices for businesses drop (Eurostat), 2026. https://www.brusselstimes.com/2391539/eu-electricity-prices-for-businesses-drop-but-nordic-nations-see-sharp-rises
[T4-S26] CBRE, North America Data Center Trends H2 2025 and H1 2026, 2026. https://www.cbre.com/insights/books/north-america-data-center-trends-h1-2026
[T4-S27] Digital Realty, Q1 and Q2 2026 results, and Q4 2025 call, 2026. https://www.barchart.com/story/news/3434946/digital-realty-reports-second-quarter-2026-results
[T4-S28] GOV.UK, AI Growth Zones collection, 2026. https://www.gov.uk/government/collections/ai-growth-zones
[T4-S29] Uptime Institute, Global Data Center Survey 2026, 29 July 2026. https://intelligence.uptimeinstitute.com/resource/uptime-institute-global-data-center-survey-2026
[T4-S30] Google, 2026 Environmental Report, 30 June 2026. https://sustainability.google/google-2026-environmental-report/
[T4-S31] Jabil, Liquid cooling for higher density racks, and SemiAnalysis, Datacenter anatomy part 2, 2026. https://jabil.com/blog/liquid-cooling-higher-density-racks.html
[T4-S32] Lawrence Berkeley National Laboratory via EESI and EPRI water brief, 2024 and 2025. https://www.eesi.org/articles/view/data-centers-and-water-consumption
[T4-S33] TechTarget, Data center tiers and why they matter for uptime. https://www.techtarget.com/it-infrastructure/tip/Data-center-tiers-and-why-they-matter-for-uptime
[T4-S34] Uptime Institute, Annual Outage Analysis 2026, 13 May 2026. https://www.businesswire.com/news/home/20260513289344/en/Uptime-Announces-Annual-Outage-Analysis-Report-2026
[T4-S35] Tech Insider, Cloud outage reports on AWS us-east-1 and Nebius, 2026. https://tech-insider.org/?p=12598
[T4-S36] Equinix blog, Scale up or scale out, and Akamai, Distributed AI inference, 2026. https://blog.equinix.com/blog/2026/06/23/ai-infrastructure-scale-up-or-scale-out/
[T4B-S1] Epoch AI, AI datacenter cost breakdown, 2026. https://epoch.ai/data-insights/ai-datacenter-cost-breakdown
[T4B-S2] Groww Digest, The real cost of building an AI data centre, 2026. https://digest.groww.in/p/the-real-cost-of-building-an-ai-data
[T4B-S3] Axis Intelligence, AI data center cost per MW, 2026. https://axis-intelligence.com/ai-data-center-cost-per-mw/
[T4B-S4] Investing.com, How much does a GW of data center capacity actually cost, 2026. https://www.investing.com/news/stock-market-news/how-much-does-a-gw-of-data-center-capacity-actually-cost-4314046
[T4B-S5] Epoch AI, AI datacenter cost breakdown (annual TCO per MW), 2026. https://epoch.ai/data-insights/ai-datacenter-cost-breakdown
[T4B-S6] Epoch AI, GPUs power usage in AI data centers, 2026. https://epoch.ai/data-insights/gpus-power-usage-in-ai-data-centers
[T4B-S7] SemiAnalysis, Datacenter anatomy part 1 electrical, and McKinsey, Beyond compute, 2026. https://newsletter.semianalysis.com/p/datacenter-anatomy-part-1-electrical
[T4B-S8] Epoch AI, Data centers buildout speeds, and TechTarget, Colossus buildouts, 2026. https://epoch.ai/data-insights/data-centers-buildout-speeds
[T4B-S9] Carbon Direct, AI meets the grid, PJM and ERCOT queue analysis, May 2026. https://www.carbon-direct.com/research-and-reports/ai-meets-the-grid-interconnection-queue-analysis-in-pjm-and-ercot
[T4B-S10] Ember, Grids for data centres in Europe, and IEA commentary, 2025 and 2026. https://ember-energy.org/latest-insights/grids-for-data-centres/
[T4B-S11] Bloomberg, Microsoft to pay hefty price for Three Mile Island clean power, and DCD, 2024. https://www.bloomberg.com/news/articles/2024-09-25/microsoft-to-pay-hefty-price-for-three-mile-island-clean-power
[T4B-S12] Utility Dive, Meta Constellation PPA, and Power Magazine, Talen Amazon, 2025. https://www.utilitydive.com/news/meta-constellation-ppa-could-be-first-of-many-deals-for-existing-reactors/750567/
[T4B-S13] RMI and Rabobank on behind-the-meter power, and S&P Global, March 2026. https://www.rabobank.com/knowledge/d011532274-the-marathon-can-behind-the-meter-data-center-power-solutions-endure-the-decade-in-the-us
[T4B-S14] LevelTen, North American PPA Price Index, and Mercom, Q3 2026. https://mercomindia.com/solar-ppa-prices-rise-6-yoy-in-north-america-fall-4-in-europe
[T4B-S15] Trading Economics, British pound news, November 2026. https://tradingeconomics.com/united-kingdom/currency/news/601113
[T4B-S16] DESNZ, Data centre electricity consumption in Great Britain 2020 to 2024, June 2026, and ONS. https://www.gov.uk/government/publications/energy-trends-june-2026-special-feature-article-data-centre-electricity-consumption-in-great-britain-2020-to-2024
[T4B-S17] GOV.UK AI Growth Zones, Computer Weekly and RCR Wireless, 2025 and 2026. https://www.gov.uk/government/collections/ai-growth-zones
[T4B-S18] Epoch AI, OpenAI Stargate: where the US sites stand, and llmpulse, 2026. https://epoch.ai/blog/openai-stargate-where-the-us-sites-stand
[T4B-S19] Meta newsroom, Hyperion joint venture with Blue Owl, and Bisnow, 2025 and 2026. https://about.fb.com/news/2025/10/meta-blue-owl-capital-develop-hyperion-data-center/
[T4B-S20] Microsoft and Epoch AI, Fairwater Wisconsin and Atlanta, 2025 and 2026. https://epoch.ai/data/ai-data-centers/directory/microsoft-fairwater-atlanta
[T4B-S21] Anthropic, Anthropic and Amazon compute, and Anthropic $50 billion US infrastructure, 2025 and 2026. https://www.anthropic.com/news/anthropic-amazon-compute
[T4B-S22] Epoch AI, Colossus 2 directory, and Tweaktown on Musk's post, 2026. https://epoch.ai/data/ai-data-centers/directory/colossus-2
[T4B-S23] ABI Research, Top 25 largest data center companies in the United States, 2025, and Lambda Finance. https://www.abiresearch.com/blog/top-25-largest-data-center-companies-united-states
[T4B-S24] CBRE, Data centre capacity pricing in Europe, 22 June 2026, and JLL EMEA mid-year 2026. https://www.cbre.com/press-releases/data-centre-capacity-pricing-in-europe-set-for-double-digit-growth-amid-supply-constraints
[T4B-S25] JLL, AI boom redraws Europe's data centre map, 2026. https://www.jll.com/en-de/newsroom/ai-boom-redraws-europes-data-centre-map-as-power-access
[T5-S1] Ornn, H100 SXM price, 23 November 2026. https://data.ornn.com/markets/h100-sxm
[T5-S2] Silicon Data, H100 Rental Price Index and index reports, November 2026. https://www.silicondata.com/products/silicon-index/h100
[T5-S3] gpurentalprices.com, GPU Rental Price Index November 2026. https://gpurentalprices.com/gpu-price-index/2026-11
[T5-S4] gpueconomy.com, Cloud GPU Price Index, week of 16 November 2026. https://gpueconomy.com/price-index
[T5-S5] Compute Census, GPU prices, November 2026. https://computecensus.com/gpu-prices/
[T5-S6] AWS News Blog, up to 45 per cent price reduction for EC2 GPU instances, June 2025, and Data Center Dynamics on Capacity Block increases, 2026. https://aws.amazon.com/blogs/aws/announcing-up-to-45-price-reduction-for-amazon-ec2-nvidia-gpu-accelerated-instances/
[T5-S7] Spheron, AWS vs Azure vs GCP GPU pricing 2026. https://www.spheron.network/blog/aws-vs-azure-vs-gcp-gpu-pricing-2026-h100-and-b200-compared/
[T5-S8] CoreWeave pricing as reported in Finitizer and Spheron, November 2026. https://tools.finitizer.com/gpu-rental-prices/h100
[T5-S9] PricingSaaS, Lambda Labs pricing diff, week 46 of 2026. https://pricingsaas.com/companies/lambdalabs/diffs/2026W46
[T5-S10] Spheron, RunPod B200 pricing 2026, and flopper.io RunPod vs Vast.ai, October 2026. https://www.spheron.network/blog/runpod-b200-pricing-2026-why-rates-rose-31-this-year/
[T5-S11] CoreWeave, Vera Rubin NVL72 bring-up and Cognition first customer, 2026. https://coreweave.com/news/coreweave-delivers-nvidia-vera-rubin-nvl72-performance-at-production-scale-starting-with-cognition
[T5-S12] Cloudzero, Uvik and Shattered.io H100 price summaries citing SemiAnalysis, Silicon Data, AIMultiple and Bank of America, 2026. https://www.cloudzero.com/blog/h100-gpu-cost/
[T5-S13] AI Weekly and PPC Land, Alphabet Q3 2026 results, 28 October 2026. https://aiweekly.co/alerts/alphabet-posts-1276b-q3-with-google-cloud-up-103-to-307b-as-2027-capex-set-to
[T5-S14] S&P Global Market Intelligence, Microsoft post-Q4 research, 6 August 2026. https://www.spglobal.com/market-intelligence/en/news-insights/research/2026/08/microsoft-postq-azure-usd100b-milestone-as-ai-demand-lifts-earnings-and-outlook
[T5-S15] 24/7 Wall St, Microsoft fiscal Q1 2027 results, October 2026. https://247wallst.com/cards/microsoft-q1-2027-earnings-msft-01m6223bcjxyqzvby9cw8yzzqb
[T5-S16] Constellation Research, AWS Q3 revenue growth and capex, 29 October 2026. https://www.constellationr.com/insights/news/aws-q3-revenue-growth-surges-39-capex-stings-amazons-cash-flow
[T5-S17] Meta, Third Quarter 2026 Results, 21 October 2026. https://seekingalpha.com/pr/20695263
[T5-S18] Oracle Q4 and fiscal 2026 results, June 2026, with coverage by The Next Web and Reuters. https://investor.oracle.com/investor-news/news-details/2026/Oracle-Announces-Record-Q4-and-FY-2026-Results-Driven-by-Cloud-Infrastructure--Cloud-Applications/
[T5-S19] CoreWeave Q3 2026 results coverage, 10 November 2026. https://aiweekly.co/alerts/coreweave-q3-revenue-jumps-168-yoy-to-366b-as-backlog-climbs-to-1325b-and-debt
[T5-S20] Nebius Q3 2026 results, Form 6-K and Quartr, 12 November 2026. https://quartr.com/events/nebius-group-n-v-nbis-q3-2026_ozKEzbDt
[T5-S21] Oracle, Q1 fiscal 2027 results, 10 September 2026. https://investor.oracle.com/investor-news/news-details/2026/Oracle-Announces-Q1-Results-Driven-by-Triple-Digit-Growth-in-Cloud-Infrastructure-Revenues/
[T5-S23] Business Standard, Big Tech depreciation, August 2026, and PYMNTS on Microsoft lifespans, July 2026. https://www.pymnts.com/earnings/2026/microsoft-extends-data-center-lifespans-to-soften-ai-buildout-costs/
[T5-S24] 24/7 Wall St, Michael Burry and AI chip lifetimes, 15 November 2026. https://247wallst.com/investing/2026/11/15/michael-burry-warned-ai-chips-would-lose-value-fast-new-data-suggests-he-was-wrong/
[T5-S25] TechRadar, Cast AI report on 5 per cent GPU utilisation, 2026. https://www.techradar.com/pro/5-utilization-is-a-math-fail-millions-of-gpus-worth-billions-are-mostly-sitting-idle-report-finds
[T5-S26] McKinsey, The evolution of neoclouds and their next moves, 2026. https://www.mckinsey.com/capabilities/tech-and-ai/our-insights/the-evolution-of-neoclouds-and-their-next-moves
[T5B-S1] CoreWeave investor relations press releases on DDTL 3.0, 4.0, 5.0 and 2.6 billion loans, 2025 to 2026, with search summary of rates. https://investors.coreweave.com/news/news-details/2026/CoreWeave-Closes-Landmark-8-5-Billion-Financing-Facility-Achieving-First-Investment-Grade-Rated-GPU-backed-Financing/default.aspx
[T5B-S2] TheNextWeb, Nebius and Lambda financing, 2026, and AM Compute largest GPU-backed loans, 2026. https://www.amcompute.com/gpu-debt/largest-gpu-loans
[T5B-S3] Fortune, Meta $27 billion Hyperion bond, 31 October 2025, and FourWeekMBA on the 6.581 per cent coupon. https://fortune.com/2025/10/31/metas-27-billion-bet-turns-ai-compute-into-wall-streets-hottest-new-investment/
[T5B-S4] Bloomberg, Oracle-tied $38 billion data centre debt, October 2025, and The Star on Oracle $25 billion bonds, 4 February 2026. https://www.bloomberg.com/news/articles/2025-10-23/record-38-billion-debt-sale-nears-for-oracle-tied-data-centers
[T5B-S5] Axios, Anthropic $15 billion from Microsoft and Nvidia, 18 November 2025, and TechCrunch Nvidia startup investments, January 2026. https://axios.com/2025/11/18/anthropic-microsoft-nvidia-15-billion
[T5B-S6] TheNextWeb, Nvidia tops $40 billion in AI equity bets in 2026, and BNN Bloomberg, 20 February 2026. https://thenextweb.com/news/nvidia-40bn-ai-equity-investments-2026
[T5B-S7] Amazon, additional Anthropic investment, April 2026, and TechCrunch, 20 April 2026. https://techcrunch.com/2026/04/20/anthropic-takes-5b-from-amazon-and-pledges-100b-in-cloud-spending-in-return/
[T5B-S8] OpenAI, AMD strategic partnership, 6 October 2025. https://openai.com/index/openai-amd-strategic-partnership
[T5B-S9] Sequoia, AI's $600B Question, 2024, and Bloomberg on Bain, 23 September 2025, and Bain Technology Report 2026. https://www.sequoiacap.com/article/ais-600b-question/
[T5B-S10] Amazon Q4 2025 results, February 2026, and press coverage of Alphabet, Meta and Microsoft capex. https://aboutamazon.com/news/company-news/amazon-earnings-q4-2025-report
[T5B-S11] CFO Dive, Microsoft holds line on AI spending, and investinglive on $170 billion fiscal 2027. https://www.cfodive.com/news/microsoft-holds-line-ai-spending-plans/826648/
[T5B-S12] Counterpoint Research, CoreWeave Q3 2026, and Finviz on $40 million per MW contracts. https://counterpointresearch.com/cn/insights/coreweave-q326
[T5B-S13] IREN, Q1 FY27 results, 5 November 2026. https://globenewswire.com/news-release/2026/11/05/3397020/0/en/iren-reports-q1-fy27-results.html
[T5B-S14] FourWeekMBA, Nebius Q2 deal payback at 22 months on 5-year servers, 2026. https://fourweekmba.com/ai-nebius-puts-q2-deal-payback-at-22-months-on-5-year-servers/
[T5B-S15] SiliconANGLE, resetting GPU depreciation, 22 November 2025, and Introl on CoreWeave six-year cycles. https://siliconangle.com/2025/11/22/resetting-gpu-depreciation-ai-factories-bend-dont-break-useful-life-assumptions/
[T5B-S16] SemiAnalysis, GPU Spot-Contract Composite Index methodology. https://gpu-index.semianalysis.com/
[T5B-S17] SemiAnalysis, The Great GPU Shortage, 2026, and a Medium repost on lead times, April 2026. https://newsletter.semianalysis.com/p/the-great-gpu-shortage-rental-capacity
[T5B-S18] Epoch AI, AI chip owners and users explorers, 2026. https://epoch.ai/data/ai-chip-owners
[T6-S1] sec-api.io, Anthropic S-1 and S-1/A filings analysis, 5 November 2026. https://sec-api.io/insights/anthropic-ant-s-1-and-s-1-a-ipo-filings-analysis-q3-2026-revenue-17-0bn-and-895bn-compute-commitments
[T6-S2] 24/7 Wall St, Anthropic says revenue run rate jumped to $81 billion, 11 November 2026. https://247wallst.com/investing/2026/11/11/anthropic-says-its-revenue-run-rate-jumped-to-an-81-billion-run-rate/
[T6-S3] CNBC, Anthropic IPO: the big questions its S-1 leaves unanswered, 30 October 2026. https://www.cnbc.com/2026/10/30/anthropic-ipo-s1-revenue-compute.html
[T6-S4] FourWeekMBA, Anthropic generated $6.6B of operating cash in nine months, November 2026. https://fourweekmba.com/ai-anthropic-generated-6-6b-of-operating-cash-in-nine-months/
[T6-S5] FourWeekMBA, Anthropic's top 5 customers make up about 25% of revenue, 2026. https://fourweekmba.com/ai-anthropics-top-5-customers-make-up-about-25-of-revenue/
[T6-S6] Al Jazeera, Anthropic targets $1.4 trillion valuation, 10 November 2026. https://aljazeera.com/economy/2026/11/10/anthropic-targets-1-4-trillion-valuation-in-massive-stock-market-debut
[T6-S7] Constellation Research, Anthropic prices shares at $83, opens at $111.50, 19 November 2026. https://www.constellationr.com/insights/news/anthropic-prices-shares-83-opens-11150-closes-8717
[T6-S8] Bloomberg Government, OpenAI's revenue run rate nears $50 billion, 2026. https://news.bgov.com/artificial-intelligence/openais-annualized-revenue-nears-50-billion-ft-says
[T6-S9] Axios, Scoop: OpenAI's annual recurring revenue nears $70B, 29 September 2026. https://axios.com/2026/09/29/scoop-openais-annual-recurring-revenue-nears-70b
[T6-S10] Exchange4media, OpenAI Q3 revenue jumps 50% to $10 billion, November 2026. https://www.exchange4media.com/digital-news/openai-q3-revenue-jumps-50-to-10-billion-but-operating-loss-widens-to-109-billion-160109.html
[T6-S11] Control Plane News, OpenAI's gross margin is going the wrong way, 2026. https://controlplane.news/newsletter/openai-gross-margin-wrong-way/
[T6-S12] Yahoo Finance, OpenAI closes $122bn funding round at $852bn valuation, 31 March 2026. https://finance.yahoo.com/markets/stocks/articles/openai-closes-122bn-funding-round-093126735.html
[T6-S13] TechCrunch, ChatGPT reaches 900M weekly active users, 27 February 2026. https://techcrunch.com/2026/02/27/chatgpt-reaches-900m-weekly-active-users
[T6-S14] Tomasz Tunguz, OpenAI hardware spending 2025 to 2035, November 2025. https://tomtunguz.com/openai-hardware-spending-2025-2035/
[T6-S15] TechCrunch, xAI burned $6.4B last year, 20 May 2026. https://techcrunch.com/2026/05/20/xai-burned-6-4b-last-year-spacexs-ipo-filing-shows-why-the-spending-is-far-from-over/
[T6-S16] 9to5Google, Alphabet Q2 2026 earnings, 22 July 2026. https://9to5google.com/2026/07/22/alphabet-q2-2026-earnings/
[T6-S17] OfficeChai, 74% of Anthropic's compute has gone towards training, 2026. https://officechai.com/ai/74-of-anthropics-compute-has-gone-towards-training-in-2026-only-26-to-inference-brad-gerstner/
[T6-S18] Epoch AI, How much does it cost to train frontier AI models. https://epoch.ai/publications/how-much-does-it-cost-to-train-frontier-ai-models
[T6-S19] HPCwire, Menlo Ventures enterprise AI spending hits $177B, 3 November 2026. https://www.hpcwire.com/aiwire/2026/11/03/menlo-venturest-enterprise-ai-spending-hits-177b-up-5-4x-in-one-year-as-agents-take-over/
[T6-S20] The Boston Globe, Anthropic sells $81.3 billion worth of shares in the largest IPO, 19 November 2026. https://www.bostonglobe.com/2026/11/19/business/anthropic-sells-813-billion-worth-shares-worlds-largest-ipo/
[T6B-S1] OfficeChai, Anthropic swings to $567 million Q3 operating loss, discloses $895 billion commitments, November 2026. https://officechai.com/ai/anthropic-q3-2026-operating-loss-895-billion-compute-commitments/
[T6B-S2] Anthropic, Series H and Series G announcements, 2026. https://www.anthropic.com/news/series-h
[T6B-S3] The Register, OpenAI exec says it will burn $50B on compute this year, 5 May 2026. https://theregister.com/2026/05/05/openai_50b_compute
[T6B-S4] eWEEK, xAI raises $20B in new funding, January 2026. https://www.eweek.com/news/xai-january-2026-funding/
[T6B-S5] Euronews, Mistral AI raises record 3 billion in Samsung-led round, 8 September 2026. https://www.euronews.com/2026/09/08/mistral-ai-raises-record-3-billion-in-samsung-led-funding-round
[T6B-S6] Euronews, Moonshot AI eyes Hong Kong IPO as DeepSeek raises capital, 6 October 2026. https://www.euronews.com/2026/10/06/moonshot-ai-eyes-hong-kong-ipo-after-50-billion-valuation-as-deepseek-raises-capital
[T6B-S7] Yahoo Finance, Meta beats earnings as 2026 AI capex tops out at $135 billion, 2026. https://finance.yahoo.com/news/meta-beats-earnings-2026-ai-231659486.html
[T6B-S8] Fortune, Alibaba Qwen passes 3 billion downloads, 15 August 2026. https://fortune.com/2026/08/15/alibaba-qwen-open-ai-models-3-billion-downloads-meta-google/
[T6B-S9] Similarweb, ChatGPT vs Claude vs Gemini vs Perplexity 2026 usage data. https://aisearch.similarweb.com/blog/chatgpt-vs-gemini-vs-claude-vs-perplexity/
[T6B-S10] FourWeekMBA on Menlo, Claude Code and Codex take 70% of $34B AI coding, JetBrains Research, August 2026. https://fourweekmba.com/ai-menlo-claude-code-and-codex-now-take-70-of-34b-ai-coding/
[T6B-S11] OpenRouter and a16z, State of AI: 100 trillion token study, January 2026. https://arxiv.org/abs/2601.10088
[T6B-S12] Anthropic, Economic Index March 2026 report. https://www.anthropic.com/research/economic-index-march-2026-report
[T6B-S13] Search summary of a frontier-model crown tenure analysis (41 days), 2026, unnamed in results, OpenRouter, model half-life and version lag newsletters. https://openrouter.ai/data/newsletter/model-half-life
[T6B-S14] Epoch AI, Can AI companies become profitable, 28 January 2026. https://epoch.ai/gradient-updates/can-ai-companies-become-profitable
[T6B-S15] Axios, Don't get used to cheap AI, 12 March 2026. https://axios.com/2026/03/12/ai-models-costs-ipo-pricing
[T6B-S16] Epoch AI, trends in AI and cost of training frontier models. https://epoch.ai/trends/compute
[T7-S1] Supabase, About billing on Supabase, accessed 26 November 2026. https://supabase.com/docs/guides/platform/billing-on-supabase
[T7-S2] Supabase, Manage Log Drain usage (billing example with Team plan), accessed 26 November 2026. https://supabase.com/docs/guides/platform/manage-your-usage/log-drains
[T7-S3] Supabase, Compute and Disk and Manage Compute usage, accessed 26 November 2026. https://supabase.com/docs/guides/platform/compute-and-disk
[T7-S4] Supabase, Compute and Disk, limits and constraints table, accessed 26 November 2026. https://supabase.com/docs/guides/platform/compute-and-disk
[T7-S5] Supabase, Manage Egress usage, accessed 26 November 2026. https://supabase.com/docs/guides/platform/manage-your-usage/egress
[T7-S6] Supabase, Manage Disk Throughput usage (read replica billing example), accessed 26 November 2026. https://supabase.com/docs/guides/platform/manage-your-usage/disk-throughput
[T7-S7] Supabase, Edge Functions Limits, accessed 26 November 2026. https://supabase.com/docs/guides/functions/limits
[T7-S8] Supabase, SOC 2 Compliance and GDPR compliance guides, accessed 26 November 2026. https://supabase.com/docs/guides/security/soc-2-compliance
[T7-S9] Supabase, HNSW indexes, accessed 26 November 2026. https://supabase.com/docs/guides/ai/vector-indexes/hnsw-indexes
[T7-S10] Vercel, Pro plan and pricing pages, read through a search summary, 26 November 2026. https://vercel.com/docs/plans/pro-plan
[T7-S11] Vercel, Functions limitations and duration configuration, read through search summary and documentation index, 26 November 2026. https://vercel.com/docs/functions/limitations
[T7-S12] Vercel, AI Gateway documentation, via documentation index, 26 November 2026. https://vercel.com/docs/ai-gateway
[T7-S13] Cloudflare, Workers pricing, read through a search summary, 26 November 2026. https://developers.cloudflare.com/workers/platform/pricing/
[T7-S14] Cloudflare, R2 pricing, read through a search summary, 26 November 2026. https://developers.cloudflare.com/r2/pricing
[T7-S15] Cloudflare, D1 pricing, read through a search summary, 26 November 2026. https://developers.cloudflare.com/d1/platform/pricing/
[T7-S16] Capterra and BlazingCDN, Cloudflare pricing 2026 (secondary), 26 November 2026. https://www.capterra.com/p/155191/Cloudflare/pricing/
[T7-S17] AWS, Lambda pricing, read through a search summary, 26 November 2026. https://aws.amazon.com/lambda/pricing/
[T7-S18] Economize and DoiT, m7g.large price pages (secondary), September 2026. https://www.economize.cloud/resources/aws/pricing/ec2/m7g.large/
[T7-S19] Bytebase, db.t4g.medium RDS price page (secondary), 2026. https://www.bytebase.com/dbcost/rds/instance/db.t4g.medium/
[T7-S20] AWS and third-party S3 pricing guides, 2026. https://aws.amazon.com/s3/pricing/
[T7-S21] AWS, Free Tier now offers $200 in credits and 6-month free plan, July 2025. https://aws.amazon.com/about-aws/whats-new/2025/07/aws-free-tier-credits-month-free-plan
[T7-S22] Synergy Research Q3 2026 figures, reported by secondary sites, 12 November 2026. https://bitcoinversus.tech/2026/11/12/global-cloud-infrastructure-revenue-1677-billion-q3-2026-synergy/
[T7B-S1] Vercel Series F announcement, Sacra and GIC coverage, searched 26 November 2026. https://vercel.com/blog/series-f
[T7B-S2] Supabase Series F blog, Orrick, TechCrunch and Sacra, June to November 2026. https://supabase.com/blog/series-f
[T7B-S3] Cloudflare, Form 8-K exhibit 99.1, third quarter 2026 results, 5 November 2026. https://www.sec.gov/Archives/edgar/data/0001477333/000147733326000060/q326exhibit991.htm
[T7B-S4] Techzine and Constellation Research, AWS Q3 2026 coverage, October 2026. https://www.techzine.eu/news/infrastructure/145406/aws-grows-by-nearly-40-percent-but-ai-investments-put-pressure-on-cash-flow/
[T7B-S5] Nasdaq, Tom Tunguz and Yahoo Finance, cloud growth coverage, 2026 (secondary). https://www.nasdaq.com/articles/amazon-microsoft-and-alphabet-all-reported-robust-cloud-growth-1-was-clear-winner
[T7B-S6] AWS Lambda SLA, Vercel Enterprise SLA, Supabase SLA, Cloudflare Business SLA, 2026. https://aws.amazon.com/lambda/sla
[T7B-S7] AWS, Summary of the Amazon DynamoDB service disruption, October 2025. https://aws.amazon.com/message/101925
[T7B-S8] Cloudflare blog, 18 November 2025 outage, and Radware summary. https://blog.cloudflare.com/18-november-2025-outage/
[T7B-S9] Press and tracker pages, cloud outage tracker 2026 (secondary). https://presenc.ai/research/cloud-outage-tracker-2026
[T7B-S10] Anthropic, Claude on Amazon Bedrock, and AWS Startups guide, 2026. https://platform.claude.com/docs/en/build-with-claude/claude-on-amazon-bedrock
[T7B-S11] Vercel documentation, AI Gateway (credits, regional inference), read through the documentation search tool, 26 November 2026. https://vercel.com/docs/ai-gateway
[T7B-S12] Pinecone pricing page and third-party summaries, 2026. https://www.pinecone.io/pricing.md
[T7B-S13] Spendark, cloud cost guides for SaaS and mobile backends, 2026 (secondary). https://spendark.com/blog/cloud-cost-saas-startups/
[T7B-S14] Bytebase, Supabase vs AWS pricing comparison, 2026 (vendor). https://www.bytebase.com/blog/supabase-vs-aws-pricing.md
[T7B-S15] Vercel, Hobby plan and fair use guidelines. https://vercel.com/docs/plans/hobby
[T7B-S16] Cloudflare, plans page and Workers pricing. https://developers.cloudflare.com/workers/platform/pricing/
[T7B-S17] Cloudflare, D1 pricing and FAQ. https://developers.cloudflare.com/d1/platform/pricing/
[T7B-S18] AWS, Free Tier FAQs and News Blog on $200 credits, 2025 to 2026. https://aws.amazon.com/free/faqs/
[T7B-S19] Vercel, compliance and HIPAA guides. https://vercel.com/docs/security/compliance
[T7B-S20] Supabase, shared responsibility model and HIPAA guide, read through the documentation search tool, 26 November 2026. https://supabase.com/docs/guides/deployment/shared-responsibility-model
[T7B-S21] Cloudflare, trust hub, ISO certifications and Data Localization Suite documentation. https://www.cloudflare.com/trust-hub/compliance-resources/iso-certifications/
[T7B-S22] DEV Community and Encore, platform tax and Vercel to AWS migration guides, 2026 (vendor and blog). https://dev.to/parag477/the-platform-tax-is-real-why-developers-are-moving-back-to-aws-2026-1com
[T8-S1] Bloomberg and TechCrunch, Cursor passes $2 billion annualised revenue, 2 March 2026. https://techcrunch.com/2026/03/02/cursor-has-reportedly-surpassed-2b-in-annualized-revenue
[T8-S2] Dealroom and Sacra, Cursor tops $4 billion annualised revenue, 2026. https://dealroom.co/news/134107-cursor-tops-4b-annualized-revenue/
[T8-S3] Crunchbase News, 2026 M&A record, Cursor and SpaceX, and Enterprise DNA, 2026. https://news.crunchbase.com/ma/2026-mergers-acquisitions-record-cursor-spcx/
[T8-S4] Dealroom, Lovable raises $400 million at $13.3 billion, and AI Magazine, Lovable crosses $600 million, 2026. https://dealroom.co/news/144597-lovable-raises-400m-at-13-3b-valuation-eyes-600m-revenue-run-rate/
[T8-S5] Sacra and ValueAdd VC, Harvey valuation and ARR, 2026. https://valueaddvc.com/blog/harvey-ai-valuation-revenue-2026-legal-ai-11b
[T8-S6] TechCrunch, Sierra raises $950 million, 4 May 2026, and FourWeekMBA on $400 million ARR, October 2026. https://techcrunch.com/2026/05/04/sierra-raises-950m-as-the-race-to-own-enterprise-ai-gets-serious
[T8-S7] ElevenLabs, $500 million Series D and $500 million ARR posts, and Sacra, 2026. https://elevenlabs.io/blog/series-d
[T8-S8] ValueAdd VC and Sacra, Replit $9 billion valuation and $525 million ARR, 2026. https://valueaddvc.com/blog/how-does-replit-make-money-525m-arr-9b-valuation-and-the-ai-agent-business-model-explained
[T8-S9] AI Magazine citing The Information, Perplexity tops $750 million run rate, and Sacra, 2026. https://aimagazine.com/news/perplexity-ai-answer-engine-tops-us750m-run-rate
[T8-S10] Glean Series F post, 10 June 2025, and Sacra and AI Magazine on $300 million ARR, 2026. https://www.glean.com/blog/glean-series-f-announcement
[T8-S11] CloudZero, AI gross margin, citing ICONIQ, and Enterprise DNA, July 2026. https://www.cloudzero.com/blog/ai-gross-margin
[T8-S12] The Information via search, Cursor gross margin, TechCrunch 7 August 2025, and TechTimes 1 June 2026. https://techcrunch.com/2025/08/07/the-high-costs-and-thin-margins-threatening-ai-coding-startups/
[T8-S13] Stripe, Intercom on value-based pricing for Fin, and SaaStr on Agentforce pricing, 2025 to 2026. https://stripe.com/customers/intercom-pricing
[T8-S14] ChartMogul, The AI churn wave, December 2025. https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/
[T8-S15] TechCrunch on the RevenueCat State of Subscription Apps, 10 March 2026. https://techcrunch.com/2026/03/10/ai-powered-apps-struggle-with-long-term-retention-new-report-shows
[T8-S16] McKinsey, The state of AI in 2026: On the road to ROI, 2026. https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai
[T8-S17] US Census Bureau, AI use by businesses, May 2026. https://census.gov/library/stories/2026/05/ai-use-businesses.html
[T8-S18] Eurostat, 20% of EU enterprises use AI technologies, 11 December 2025. https://ec.europa.eu/eurostat/web/products-eurostat-news/w/ddn-20251211-2
[T8-S19] Stanford HAI, 2026 AI Index Report, economy chapter, April 2026. https://hai.stanford.edu/ai-index/2026-ai-index-report/economy
[T8-S20] Menlo Ventures, State of Enterprise AI 2026, via HPCwire, 3 November 2026, and 2025 report, December 2025. https://www.hpcwire.com/aiwire/2026/11/03/menlo-venturest-enterprise-ai-spending-hits-177b-up-5-4x-in-one-year-as-agents-take-over/
[T8-S21] Gartner, Worldwide AI spending to grow 49.5% in 2026, 16 September 2026. https://gartner.com/en/newsroom/press-releases/2026-09-16-gartner-forecasts-worldwide-ai-spending-to-grow-49-point-5-percent-in-2026
[T8-S23] TechSpot, Google AI generates 75% of new code, 2026, and Fortune, 29 January 2026. https://www.techspot.com/news/112152-google-ai-now-generates-75-new-code-up.html
[T8-S25] PitchBook-NVCA Venture Monitor and IBTimes, Q3 2026 venture funding, October 2026. https://www.ibtimes.com/ai-startups-global-venture-funding-q3-2026-3809588
[T8-S26] SaaSRise, Benzinga and Tomasz Tunguz on AI valuation multiples, 2026. https://saasrise.com/blog/the-ai-software-valuation-report-2026
[T8-S27] Yahoo Finance and Tom's Hardware, Big Tech AI spending plans reach $725 billion, 2026. https://www.tomshardware.com/tech-industry/big-tech/big-techs-ai-spending-plans-reach-725-billion
[T8-S28] Takshashila Institute, The AI Investment Cycle, 8 July 2026, and NPR, 23 November 2025. https://takshashila.org.in/content/publications/20260708-ai-investment-cycle.html
[T8-S31] Alvarez and Marsal, May 2026, and Grant Thornton, Private Equity Insights 2026 AI Impact Survey. https://www.grantthornton.com/insights/survey-reports/private-equity/2026/private-equity-insights-2026-ai-impact-survey-report.html
[T8B-S1] CNBC, SpaceX to acquire the AI coding startup Cursor for $60 billion, 16 June 2026. https://www.cnbc.com/2026/06/16/spacex-spcx-cursor-acquisition-ipo.html
[T8B-S2] Satnews, SpaceX finalizes regulatory procedures to close $60 billion Cursor acquisition, 13 August 2026, and AI Weekly on the close. https://satnews.com/2026/08/13/spacex-finalizes-regulatory-procedures-to-close-60-billion-acquisition-of-ai-platform-cursor/
[T8B-S3] Anthropic, Anthropic Economic Index dataset, latest period May 2026, published 24 June 2026. https://www.anthropic.com/economic-index
[T8B-S4] ONS, Business insights and impact on the UK economy, 8 October 2026, and GOV.UK AI adoption survey 2026. https://www.ons.gov.uk/businessindustryandtrade/business/businessservices/bulletins/businessinsightsandimpactontheukeconomy/8october2026
[T8B-S5] Sacra on Intercom usage-based AI pricing, 2026, and Stripe on Intercom Fin pricing. https://stripe.com/customers/intercom-pricing
[T8B-S6] Cursor, June 2025 pricing, and TechCrunch, Cursor apologizes for unclear pricing changes, 7 July 2025. https://techcrunch.com/2025/07/07/cursor-apologizes-for-unclear-pricing-changes-that-upset-users/
[T8B-S7] Salesforce, Fiscal 2026 fourth quarter results, 25 February 2026, and The Register on Agentforce pricing, 5 December 2025. https://www.salesforce.com/news/press-releases/2026/02/25/fy26-q4-earnings/
[T8B-S8] Wavect, Neurons Lab, AKF Partners and CRV AI diligence guides, 2026. https://wavect.io/blog/technical-due-diligence-ai-mvp/
[T8B-S9] Sacra on Replit and Lovable margins, citing The Information, 2025. https://sacra.com/chat/h/810d91d8-78a4-43b5-9917-153465800474/
[T8B-S10] RAND, The Root Causes of Failure for Artificial Intelligence Projects, August 2024. https://www.rand.org/pubs/research_reports/RRA2680-1.html
[T8B-S11] S&P Global Market Intelligence, Generative AI shows rapid growth but yields mixed results, 27 October 2025. https://www.spglobal.com/market-intelligence/en/news-insights/research/2025/10/generative-ai-shows-rapid-growth-but-yields-mixed-results
[T8B-S12] Cui, Demirer, Jaffe, Musolff, Peng and Salz, field experiments of generative AI on developers, draft February 2025. https://economics.mit.edu/sites/default/files/inline-files/draft_copilot_experiments.pdf
[T8B-S13] GitHub, Quantifying GitHub Copilot's impact in the enterprise with Accenture, 2024. https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-in-the-enterprise-with-accenture/
[T8B-S14] Anthropic, How AI assistance impacts the formation of coding skills, January 2026. https://www.anthropic.com/research/AI-assistance-coding-skills
[T8B-S16] Stanford Digital Economy Lab, Canaries in the Coal Mine, August 2026 revision. https://digitaleconomy.stanford.edu/publication/canaries-in-the-coal-mine-six-facts-about-the-recent-employment-effects-of-artificial-intelligence/
[T8B-S17] The Register and Fortune on Salesforce engineering hiring, 2025 and 28 May 2026. https://www.theregister.com/2025/02/27/salesforce_misses_revenue_guidance/
[T8B-S18] Computer Weekly on Gartner, Larridin, and Pragmatic Engineer on coding agent spend, 2026. https://www.computerweekly.com/news/366645054/Gartner-AI-coding-agents-will-cost-more-than-real-developers
[T8B-S19] TechSpot on Nadella's 30 per cent, 2025, and SignalFire State of Tech Talent, 2026. https://www.techspot.com/news/107749-ceo-satya-nadella-up-30-microsoft-code-now.html
[T8B-S20] PwC, AI fitness and value creation in PE-backed companies, 2026, and FTI Consulting Private Equity Report, June 2026. https://www.pwc.com/gx/en/issues/c-suite-insights/ai-value-pe-backed-companies.html
[T8B-S21] Bain and Company, Private Equity Midyear Report 2026. https://www.bain.com/es-es/insights/private-equity-midyear-report-2026/
[T9-S1] ISO/IEC, Information technology, Artificial intelligence, AI concepts and terminology (ISO/IEC 22989:2022), catalogue page. https://standards.iteh.ai/catalog/standards/iso/c86ee148-a050-4bec-b1eb-7300c53a275b/iso-iec-22989-2022
[T9-S2] OECD.AI, AI system definition update, November 2023, and OECD AI Papers No. 8, February 2024. https://oecd.ai/en/wonk/ai-system-definition-update
[T9-S3] NIST, AI 600-1 Generative AI Profile, July 2024. https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf
[T9-S4] OpenAI Help Centre, What are tokens and how to count them. https://help.openai.com/en/articles/4936856-what-are-tokens-and-how-to-count-them
[T9-S5] Google AI for Developers, Understand and count tokens. https://ai.google.dev/gemini-api/docs/tokens
[T9-S6] Anthropic, Token counting documentation. https://platform.claude.com/docs/en/build-with-claude/token-counting
[T9-S8] Petrov et al., Language Model Tokenizers Introduce Unfairness Between Languages, 2023. https://arxiv.org/abs/2305.15425
[T9-S9] Anthropic, Vision documentation. https://platform.claude.com/docs/en/build-with-claude/vision
[T9-S10] OpenAI, Image input token and cost calculator, with community forum threads. https://developers.openai.com/api/docs/guides/image-cost-calculator
[T9-S11] Vaswani et al., Attention Is All You Need, 2017. https://arxiv.org/abs/1706.03762
[T9-S12] OpenAI, text-embedding-3-small and text-embedding-3-large model pages. https://developers.openai.com/api/docs/models/text-embedding-3-small
[T9-S13] Google Developers Blog, Gemini Embedding now generally available, July 2025. https://developers.googleblog.com/en/gemini-embedding-available-gemini-api/
[T9-S14] Hoffmann et al., Training Compute-Optimal Large Language Models, March 2022. https://arxiv.org/abs/2203.15556
[T9-S15] Meta, The Llama 3 Herd of Models, July 2024. https://ar5iv.labs.arxiv.org/html/2407.21783
[T9-S16] Epoch AI, Trends in AI compute, updated 5 February 2026. https://epoch.ai/trends
[T9-S17] Ouyang et al., Training language models to follow instructions with human feedback, March 2022. https://arxiv.org/abs/2203.02155
[T9-S18] Scientific American, Secrets of Chinese AI model DeepSeek revealed in landmark paper, September 2025 (on the Nature paper). https://scientificamerican.com/article/secrets-of-chinese-ai-model-deepseek-revealed-in-landmark-paper
[T9-S19] Neural Magic, Meta-Llama-3.1-405B-FP8 model card, and Dell Technologies, Running Llama 3.1 405B on PowerEdge XE9680. https://huggingface.co/neuralmagic/Meta-Llama-3.1-405B-FP8
[T9-S21] OpenAI Developer Community, Compatibility matrix for reasoning effort and sampling parameters (forum quoting OpenAI). https://community.openai.com/t/request-for-compatibility-matrix-reasoning-effort-sampling-parameters-across-gpt-5-series/1371738
[T9-S22] Inference economics of language models, arXiv 2506.04645, and related 2025 to 2026 arXiv energy studies. https://arxiv.org/pdf/2506.04645
[T9-S23] DigitalOcean, The hidden cost of output token pricing. https://www.digitalocean.com/community/tutorials/hidden-cost-output-token-pricing
[T9-S26] Google AI for Developers, Gemini API pricing. https://ai.google.dev/gemini-api/docs/pricing
[T9-S27] Liu et al., Lost in the Middle, 2023. https://arxiv.org/abs/2307.03172
[T9-S28] Hong, Troynikov and Huber, Context Rot, Chroma, 14 July 2025. https://research.trychroma.com/context-rot
[T9-S29] Hsieh et al., RULER, NVIDIA, April 2024. https://arxiv.org/abs/2404.06654
[T9-S30] OpenAI, Reasoning models guide. https://developers.openai.com/api/docs/guides/reasoning
[T9-S31] Anthropic, Extended thinking documentation. https://platform.claude.com/docs/en/build-with-claude/extended-thinking
[T9-S32] OpenAI, Why language models hallucinate, 5 September 2025. https://openai.com/index/why-language-models-hallucinate/
[T9-S33] Anthropic, Reduce hallucinations. https://platform.claude.com/docs/en/test-and-evaluate/strengthen-guardrails/reduce-hallucinations
[T9-S34] Stanford HAI and Stanford Law, Hallucination-Free? Assessing the Reliability of Leading AI Legal Research Tools, 2024 and 2025. https://hai.stanford.edu/news/ai-trial-legal-models-hallucinate-1-out-6-queries
[T9-S35] Anthropic Support, How up to date is Claude's training data. https://support.claude.com/en/articles/8114494
[T9-S36] OpenAI, Models documentation. https://developers.openai.com/api/docs/models
[T9-S37] Google DeepMind, Gemini 3.6 Flash model card. https://deepmind.google/models/model-cards/gemini-3-6-flash/
[T9-S38] Open Source Initiative, Open Source AI Definition, reported by It's FOSS, October 2024. https://itsfoss.com/news/osi-ai-open-source-definition/
[T9-S39] OpenAI, Introducing gpt-oss, August 2025. https://openai.com/index/introducing-gpt-oss/
[T9-S40] DeepSeek-AI, DeepSeek-V3 Technical Report, December 2024. https://arxiv.org/abs/2412.19437
[T9-S41] SiliconANGLE, Moonshot Kimi K3, July 2026, and Codersera, best open source LLMs 2026. https://siliconangle.com/chinas-moonshot-throws-gauntlet-kimi-k3-worlds-largest-open-weights-model
[T9B-S1] NIST CSRC glossary, machine learning and AI model entries. https://csrc.nist.gov/glossary/term/ml
[T9B-S2] US DOT, AI definitions and concepts, reproducing the NIST Trustworthy AI glossary. https://its.dot.gov/research-areas/artificial-intelligence/focus-areas/learn-connect/ai-definitions-concepts
[T9B-S3] IBM, What is deep learning. https://www.ibm.com/topics/deep-learning
[T9B-S4] Anthropic, Building effective agents, 19 December 2024. https://www.anthropic.com/engineering/building-effective-agents
[T9B-S5] Lewis et al., Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks, 2020. https://arxiv.org/abs/2005.11401
[T9B-S6] Anthropic, Models overview, accessed 26 November 2026. https://platform.claude.com/docs/en/about-claude/models/overview
[T9B-S7] Anthropic, Claude Fable 5.2 model page, November 2026. https://platform.claude.com/docs/en/models/fable-5-2/overview
[T9B-S8] OpenAI, GPT-6 Astra model page (through search summary). https://developers.openai.com/api/docs/models/gpt-6-astra
[T9B-S9] Google AI for Developers, Gemini 4 Argon model page (through search summary). https://ai.google.dev/gemini-api/docs/models/gemini-4-argon
[T9B-S10] Google DeepMind, Gemini 4 Argon model card, and Google blog announcement, 2026 (through search summaries). https://deepmind.google/models/model-cards/gemini-4-argon/
[T9B-S11] OpenAI, Learning to reason with LLMs, 12 September 2024. https://openai.com/index/learning-to-reason-with-llms/
[T9B-S12] Qwen team, Qwen3 Technical Report, 2025 (through search summary). https://arxiv.org/abs/2505.09388
[T9B-S13] Anthropic, Claude 3.7 Sonnet announcement, February 2025. https://www.anthropic.com/news/claude-3-7-sonnet
[T9B-S14] Anthropic, Effort documentation. https://platform.claude.com/docs/en/build-with-claude/effort
[T9B-S15] Vectara, Hallucination leaderboard, updated 24 November 2026. https://github.com/vectara/hallucination-leaderboard
[T9B-S16] Yahoo Tech, OpenAI says GPT-5 hallucinates less, reporting the GPT-5 system card, August 2025. https://tech.yahoo.com/ai/articles/openai-says-gpt-5-hallucinates-195857235.html
[T9B-S17] NVIDIA Developer Blog, Mastering LLM techniques: inference optimization, and TensorRT-LLM posts (with Introl third-party guide). https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization
[T9B-S18] NVIDIA, Llama 3.3 70B Instruct FP8 model card. https://huggingface.co/nvidia/Llama-3.3-70B-Instruct-FP8
[T9B-S19] vLLM recipes and NVIDIA Dynamo recipe, Llama 3.3 70B, with DigitalOcean report. https://docs.nvidia.com/dynamo/recipes/llama-3-3-70b
[T9B-S20] Kaitchup and SitePoint, Llama 70B memory guides, 2026 (third party). https://kaitchup.substack.com/p/run-llama-31-70b-instruct-on-your
[T9B-S21] Meta, Llama 3.1 Community License, 23 July 2024. https://github.com/meta-llama/llama-models/blob/main/models/llama3_1/LICENSE
[T9B-S22] DeepSeek, DeepSeek License Agreement 1.0 (LICENSE-MODEL), DeepSeek-V3 repository. https://github.com/deepseek-ai/DeepSeek-V3/blob/main/LICENSE-MODEL
[T9B-S23] OpenAI Help Centre, OpenAI open-weight models. https://help.openai.com/en/articles/11870455-openai-open-weight-models
[T9B-S24] Mistral Help Centre, Under which licence are Mistral's open models available, and a 2026 licence comparison. https://help.mistral.ai/en/articles/347393-under-which-license-are-mistral-s-open-models-available
[T10-S1] MDN Web Docs, How the web works. https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works
[T10-S2] Cloudflare Learning Center, What is a CDN edge server. https://www.cloudflare.com/learning/cdn/glossary/edge-server
[T10-S3] web.dev (Google), Time to First Byte (TTFB), and secondary DNS and TLS figures from GF.dev. https://web.dev/articles/ttfb
[T10-S4] GitHub Docs, About protected branches. https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches
[T10-S5] GitHub Docs, Control deployments (environments). https://docs.github.com/en/actions/how-tos/deploy/configure-and-manage-deployments/control-deployments
[T10-S6] Google Engineering Practices, The Standard of Code Review. https://google.github.io/eng-practices/review/reviewer/standard.html
[T10-S7] DORA, Software delivery performance metrics guide and history. https://dora.dev/guides/dora-metrics/
[T10-S8] Octopus Deploy, The 2024 DevOps Performance Clusters (summary of the 2024 DORA report). https://octopus.com/blog/2024-devops-performance-clusters
[T10-S9] Google, How are developers using AI? Inside our 2025 DORA report, 2025, with Splunk and TechTarget reviews. https://blog.google/technology/developers/dora-report-2025/
[T10-S10] AWS Well-Architected Framework, Reliability Pillar, and AWS Architecture Blog on reliable scalability. https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html
[T10-S11] AWS Compute Blog, Understanding and remediating cold starts, and Lambda documentation. https://aws.amazon.com/blogs/compute/understanding-and-remediating-cold-starts-an-aws-lambda-perspective
[T10-S12] PostgreSQL wiki and Percona, Scaling PostgreSQL (vendor guidance). https://wiki.postgresql.org/wiki/Replication,_Clustering,_and_Connection_Pooling
[T10-S13] Anthropic, API rate limits documentation. https://docs.anthropic.com/en/api/rate-limits
[T10-S14] Google SRE, Service Level Objectives and Implementing SLOs. https://sre.google/sre-book/service-level-objectives
[T10-S15] Google SRE, Availability Table, and AWS Well-Architected Availability. https://sre.google/sre-book/availability-table/
[T10-S16] Google SRE, Postmortem Culture and Incident Management Guide. https://sre.google/sre-book/postmortem-culture/
[T10-S17] OWASP GenAI Security Project, Top 10 for LLM Applications 2025, with HackerOne, Outpost24 and Bugcrowd summaries. https://www.hackerone.com/ai/owasp-top-10-llms-2025
[T10-S18] Cloud Security Alliance, The OWASP Top 10 for LLM Applications 2026, 21 October 2026, with Imperva summary. https://cloudsecurityalliance.org/blog/2026/10/21/the-owasp-top-10-for-llm-applications-2026-what-changed-and-why-it-matters
[T10-S19] OWASP GenAI Security Project, Top 10 for Agentic Applications for 2026, 9 December 2025. https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications/
[T10-S20] SecurityWeek and arXiv, EchoLeak CVE-2025-32711, June 2025. https://www.securityweek.com/echoleak-ai-attack-enabled-theft-of-sensitive-data-via-microsoft-365-copilot/
[T10-S21] Simon Willison, The lethal trifecta, 16 June 2025. https://simonwillison.net/2025/jun/16/the-lethal-trifecta/
[T10-S22] Invariant Labs, GitHub MCP exploited, 26 May 2025. https://invariantlabs.ai/blog/mcp-github-vulnerability
[T10-S24] The Register, Samsung generative AI ban, 2 May 2023. https://www.theregister.com/2023/05/02/samsung_generative_ai_ban/
[T10-S25] GitGuardian, The State of Secrets Sprawl 2026, March 2026. https://blog.gitguardian.com/the-state-of-secrets-sprawl-2026/
[T10-S26] Anthropic, Mitigating the risk of prompt injections in browser use, 24 November 2025. https://www.anthropic.com/research/prompt-injection-defenses
[T10-S27] Anthropic, Context windows and context management documentation. https://platform.claude.com/docs/en/build-with-claude/context-windows
[T10-S28] OpenAI, Conversation state guide. https://developers.openai.com/api/docs/guides/conversation-state
[T10-S29] OpenTelemetry, Inside the LLM Call: GenAI Observability, 2026. https://opentelemetry.io/blog/2026/genai-observability/
[T10-S30] TechCrunch, 8 questions before technical due diligence, 2022, with Vallettasoftware and Umbrex checklists. https://techcrunch.com/2022/10/25/8-questions-to-answer-before-your-startup-faces-technical-due-diligence/
[T10-S31] Veracode, 2025 GenAI Code Security Report press release, 30 July 2025. https://www.veracode.com/press-release/ai-generated-code-poses-major-security-risks-in-nearly-half-of-all-development-tasks-veracode-research-reveals/
[T10-S32] Perry, Srivastava, Kumar, Boneh (Stanford), Do Users Write More Insecure Code with AI Assistants, arXiv 2211.03622. https://arxiv.org/abs/2211.03622
[T10-S33] GitClear, AI Copilot Code Quality 2025 report, with TechCrunch and DevClass coverage. https://www.gitclear.com/industry_stats/ai_code_quality_signal_graphs
[T10-S34] METR, Early 2025 AI experienced open-source developer study, 10 July 2025. https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/
[T10-S35] Stack Overflow, 2025 Developer Survey results, 29 July 2025. https://stackoverflow.co/company/press/archive/stack-overflow-2025-developer-survey/
[T10-S36] GitHub, Octoverse 2025, 28 October 2025. https://github.blog/news-insights/octoverse/octoverse-a-new-developer-joins-github-every-second-as-ai-leads-typescript-to-1/
[T10-S37] NIST NVD, CVE-2025-48757 (Lovable), with Superblocks write-up. https://nvd.nist.gov/vuln/detail/CVE-2025-48757
[T10B-S1] Anthropic, Memory tool documentation, Nov 2026. https://platform.claude.com/docs/en/agents-and-tools/tool-use/memory-tool
[T10B-S2] Anthropic, Context editing documentation, Nov 2026. https://platform.claude.com/docs/en/build-with-claude/context-editing
[T10B-S3] Anthropic, Compaction overview, Nov 2026. https://platform.claude.com/docs/en/build-with-claude/compaction
[T10B-S4] OpenAI Help Center, Memory in ChatGPT and How does reference saved memories work. https://help.openai.com/en/articles/11146739-how-does-reference-saved-memories-work
[T10B-S5] Octopus Deploy and GetDX summaries of the 2024 DORA report (the official PDF was not reachable). https://octopus.com/blog/2024-devops-performance-clusters
[T10B-S6] Google Cloud and Google blog, 2025 DORA report and AI Capabilities Model, with Splunk review. https://blog.google/technology/developers/dora-report-2025/
[T10B-S7] RDEL newsletter, seven team profiles of delivery performance (secondary). https://rdel.substack.com/p/rdel-113-what-are-the-seven-team
[T10B-S8] OWASP GenAI Security Project, Top 10 for LLM Applications 2025, with Tenable and HackerOne readings. https://genai.owasp.org/resource/owasp-top-10-for-llm-applications-2025/
[T10B-S9] Tenable, What you must know about the OWASP Top 10 for LLM Applications 2025 update. https://www.tenable.com/blog/what-you-must-know-about-the-owasp-top-10-for-llm-applications-2025-update
[T10B-S10] OWASP GenAI Security Project, OWASP GenAI LLM Top 10 2026 (search result, not opened), with Help Net Security, 6 Aug 2026. https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/
[T10B-S11] OWASP GenAI Security Project, Top 10 for Agentic Applications, 9 Dec 2025, with TechRepublic coverage. https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications/
[T10B-S12] OpenTelemetry, Semantic conventions for generative AI metrics (search summary). https://opentelemetry.io/docs/specs/semconv/gen-ai/gen-ai-metrics/
[T10B-S13] DEV Community, OpenTelemetry GenAI semantic conventions are not stable yet, 2026. https://dev.to/azena-ai/opentelemetrys-genai-semantic-conventions-are-not-stable-yet-heres-what-actually-shipped-in-2026-3mke
[T10B-S14] DEV Community and roadmap.sh roundups of LLM observability tools, 2026. https://dev.to/grepture/llm-observability-tools-compared-the-2026-landscape-gdf
[T10B-S15] Anthropic, Reducing latency, Nov 2026. https://platform.claude.com/docs/en/test-and-evaluate/strengthen-guardrails/reduce-latency
[T10B-S16] DEV Community, How we measure HTTP timing (DNS, TCP, TLS, TTFB), 2026. https://dev.to/p12se/how-we-measure-http-timing-dns-tcp-tls-ttfb-breakdown-4oa2
[T10B-S17] DebugBear, HTTP server connections. https://debugbear.com/blog/http-server-connections
[T10B-S18] NVIDIA AIPerf, HTTP Trace Metrics Guide. https://docs.nvidia.com/aiperf/latest/tutorials/metrics-analysis/http-trace-metrics-guide
[T10B-S19] Martin Fowler, Feature Toggles (aka Feature Flags) and Feature Flag bliki (snippets via search). https://martinfowler.com/articles/feature-toggles.html
[T10B-S20] LaunchDarkly, Defining Feature Flags (vendor). https://launchdarkly.com/blog/what-is-feature-flagging/
[T10B-S21] AWS, Introduction to DevOps on AWS deployment strategies, Overview of Deployment Options (canary), Well-Architected OPS06-BP03. https://docs.aws.amazon.com/whitepapers/latest/introduction-devops-aws/deployment-strategies.html
[T10B-S22] arXiv 2512.14012, Professional Software Developers Don't Vibe, They Control, Dec 2025. https://arxiv.org/pdf/2512.14012
[T10B-S23] arXiv 2510.00328, Vibe Coding in Practice, grey literature review. https://arxiv.org/html/2510.00328v1
[T10B-S24] Astra, The security risks with vibe coding: a study, with SecurityWeek and TheNextWeb coverage (vendor). https://www.getastra.com/reports/vibe-coding-security-risks-study
[T10B-S25] Umbrex, Codebase and Engineering Health: The Walk the Repo Playbook. https://umbrex.com/resources/software-product-and-technology-due-diligence-playbook/codebase-and-engineering-health-the-walk-the-repo-playbook/
[T10B-S26] Mend.io, Technical due diligence, Idealogic, Technical due diligence checklist. https://idealogic.io/blog/technical-due-diligence
[T10B-S27] techconcepts.org, Technical due diligence checklist. https://techconcepts.org/blog/technical-due-diligence
[T11-S1] NVIDIA, Financial Results for Third Quarter Fiscal 2027, 17 November 2026. https://investor.nvidia.com/news/press-release-details/2026/NVIDIA-Announces-Financial-Results-for-Third-Quarter-Fiscal-2027/default.aspx
[T11-S2] TSMC Form 6-K Q3 2026 and CRN Asia, October 2026. https://www.sec.gov/Archives/edgar/data/0001046179/000104617926000726/a3q26e_withguidancexfinal.htm
[T11-S3] Korea Times, SK hynix record Q3 operating profit, 28 October 2026. https://www.koreatimes.co.kr/business/companies/20261028/sk-hynix-logs-record-q3-operating-profit-of-628-bil
[T11-S4] Nasdaq, Broadcom Q3 earnings call highlights, 2026. https://www.nasdaq.com/articles/broadcom-q3-earnings-call-highlights
[T11-S7] Zacks, Microsoft Q1 earnings beat estimates as cloud accelerates, October 2026. https://www.zacks.com/stock/news/3018768/microsoft-q1-earnings-beat-estimates-as-cloud-accelerates
[T11-S8] Pulse 2, CoreWeave Q3 record revenue $3.66 billion, November 2026. https://pulse2.com/coreweave-record-q3-revenue-reaches-3-66-billion-as-backlog-grows-to-132-5-billion/
[T11-S9] sec-api.io, Nebius Q3 2026 earnings analysis, 13 November 2026. https://sec-api.io/insights/nebius-group-nbis-q3-2026-earnings-980-8m-revenue-38-7bn-rpo-and-a-12bn-to-13bn-2027-outlook-sec-filing-analysis
[T11-S10] Zacks, Equinix Q3 AFFO beat on record bookings, October 2026. https://zacks.com/stock/news/3018995/equinix-q3-affo-beat-estimates-on-record-bookings-strong-pricing
[T11-S11] Finviz, Digital Realty Reports Third Quarter 2026 Results, 2026. https://finviz.com/news/412047/digital-realty-reports-third-quarter-2026-results
[T11-S12] American Nuclear Society, Second-quarter updates from Constellation, 13 August 2026. https://www.ans.org/news/2026-08-13/article-8291/secondquarter-updates-from-constellation-new-ppas-crane-restart-and-more/
[T11-S13] Morningstar and Axios, Anthropic and OpenAI revenue, April and 29 September 2026. https://axios.com/2026/09/29/scoop-openais-annual-recurring-revenue-nears-70b
[T11-S14] The Decoder, OpenAI cash burn and gross margin reports, 2026. https://the-decoder.com/openai-adds-111-billion-to-its-cash-burn-forecast-as-ai-costs-spiral-beyond-projections/
[T11-S15] TechCrunch, Cursor surpassed $2B annualised revenue, 2 March 2026, and Sacra Cursor research. https://techcrunch.com/2026/03/02/cursor-has-reportedly-surpassed-2b-in-annualized-revenue
[T11-S17] Levelup Gitconnected, The AI Gold Rush Mapped Layer by Layer, 2026. https://levelup.gitconnected.com/the-ai-gold-rush-mapped-layer-by-layer-from-nvidias-chips-to-anthropic-s-ipo-9a162dc3b5d1
[T11-S18] Axios, Nvidia almighty: chip riches flood through AI universe, 28 August 2026. https://axios.com/2026/08/28/nvidia-ai-chip-circular-finance-startups
[T11-S19] Epoch AI, Hyperscalers control most compute, and FourWeekMBA summary, 2026. https://epoch.ai/data-insights/hyperscalers-control-most-compute
[T11-S20] Epoch AI, AI Chip Owners explorer and Geopolitics of AI, 2026. https://epoch.ai/data/ai-chip-owners
[T11-S21] Hargreaves Lansdown, AI hyperscalers expected to spend $828 billion on capex, 2026. https://www.hl.co.uk/news/ai-hyperscalers-are-expected-to-finish-the-year-spending-a-whopping-828-billion-on-capex
[T11-S22] Gartner, Worldwide AI Spending to Grow 49.5% in 2026, 16 September 2026. https://gartner.com/en/newsroom/press-releases/2026-09-16-gartner-forecasts-worldwide-ai-spending-to-grow-49-point-5-percent-in-2026
[T11-S23] Bain, Technology Report 2026 and 2025 press release. https://www.bain.com/insights/new-innovation-is-required-to-fund-ais-6-trillion-buildout-technology-report-2026/
[T11-S24] McKinsey, The cost of compute: a $7 trillion race, 2025, and Software Strategies Blog, 22 October 2026. https://www.mckinsey.com/industries/technology-media-and-communications/our-insights/the-cost-of-compute-a-7-trillion-dollar-race-to-scale-data-centers
[T11-S26] ICONIQ, 2026 State of AI Report: The Builder's Economy, July 2026. https://www.iconiq.com/growth/insights/state-of-ai-2026
[T11-S27] SaaStr, ICONIQ Pacesetter data, September 2026. https://saastr.com/whats-truly-great-now-in-b2b-ai-per-iconiq-115-growth-at-100m-55-gross-margins-and-655k-in-revenue-per-employee
[T11-S28] Bessemer Venture Partners, The State of AI 2025, August 2025. https://www.bvp.com/atlas/the-state-of-ai-2025
[T11-S29] SaaS Capital, 2026 B2B Benchmarking Private SaaS Company Growth Rates, July 2026. https://www.saas-capital.com/research/private-saas-company-growth-rate-benchmarks/
[T11-S30] KeyBanc, 17th annual AI x Software Benchmark via Finviz, 13 November 2026. https://finviz.com/news/422721/ai-native-software-companies-lead-on-growth-but-stronger-economics-have-not-yet-followed
[T11-S31] Aleph, 2026 SaaS benchmarks takeaways, and High Alpha, 2026. https://www.getaleph.com/blog/2026-saas-benchmarks-takeaways
[T11-S33] Livmo SaaS Valuation Index (6 November 2026) and Software Equity Group SaaS Index, Q3 2026. https://livmo.com/saas-valuation-multiples/
[T11-S34] ValueAddVC, AI startup valuation multiples 2026, and PitchBook note on OpenAI, 2026. https://valueaddvc.com/blog/ai-startup-valuation-multiples-2026-why-ai-trades-at-10-50x-vs-saas-at-3-7x
[T11-S36] Investing.com, How much does a GW of data centre capacity cost, and Axis Intelligence, 2026. https://www.investing.com/news/stock-market-news/how-much-does-a-gw-of-data-center-capacity-actually-cost-4314046
[T11-S38] The Register, GPU metric, 20 May 2025, and arXiv 2605.20799, 2026. https://theregister.com/2025/05/20/gpu_metric
[T11-S40] Artificial Analysis, LLM Leaderboard and metric definitions, 2026. https://artificialanalysis.ai/leaderboards/models
[T11-S42] Intercom, Fin AI Agent pricing and outcomes help pages, 2026. https://www.intercom.com/help/en/articles/8205718-fin-ai-agent-pricing
[T11B-S1] Amazon, Q3 2026 earnings report, via aboutamazon.com and Zacks, October 2026. https://aboutamazon.com/news/company-news/amazon-earnings-q3-2026-report
[T11B-S2] 9to5Google, Alphabet Q3 2026 earnings, 28 October 2026, and FourWeekMBA and InvestingLive summaries. https://9to5google.com/2026/10/28/alphabet-q3-2026-earnings/
[T11B-S4] Zacks and 247WallSt, Microsoft fiscal Q1 2027 results, October 2026. https://www.zacks.com/stock/news/3018768/microsoft-q1-earnings-beat-estimates-as-cloud-accelerates
[T11B-S7] Al Jazeera, Euronews, Forbes Australia and Korea JoongAng Daily, Anthropic IPO, 18 to 19 November 2026. https://www.aljazeera.com/economy/2026/11/19/anthropic-starts-trading-in-the-us-after-blockbuster-ipo
[T11B-S8] Epoch AI, AI Chip Owners explorer and Hyperscalers control most compute, 2026. https://epoch.ai/data/ai-chip-owners
[T11B-S9] Fortune, Philipp Dubach, Exponential View and Gartner via Axios and CFO Dive, AI revenue against capex, 2026. https://philippdubach.com/posts/reconciling-enterprise-ai-revenue/
[T11B-S10] CoreWeave, Q3 2026 results and call, 10 November 2026, via Baxtel and Finviz. https://baxtel.com/news/coreweave-tops-1-7gw-active-power-as-backlog-reaches-132-5b
[T11B-S11] FourWeekMBA, Nebius and IREN per-MW pricing, and Bernstein figures via a Nasdaq piece, 2026. https://fourweekmba.com/ai-short-gpu-deals-pay-40m-per-mw-1-8x-five-year-contracts/
[T11B-S12] SaaStr, Inference costs average 23% of revenue at AI B2B companies (ICONIQ), January 2026. https://saastr.com/inference-costs-average-23-of-revenue-at-ai-b2b-companies-how-will-you-pay-for-it
[T11B-S13] Nalpeiron, 2026 State of B2B Software Monetization, June 2026. https://nalpeiron.com/resources/program/2026-state-of-b2b-software-monetization/ai-inference-cost-handling/
[T11B-S14] Salesforce, support metrics and Agentforce on Salesforce Help, 2026. https://www.salesforce.com/blog/support-metrics-agentforce/
[T11B-S15] Fin.ai, Sobot, DragApp and Rework resolution rate comparisons, 2026. https://www.dragapp.com/blog/ai-support-agent-resolution-rates/
[T11B-S16] CX Today and MyAskAI, Klarna AI customer service, 2026. https://www.cxtoday.com/customer-engagement-journey-orchestration/klarna-ai-customer-service/
[T11B-S17] Aleph, High Alpha, Benchmarkit and KeyBanc benchmark summaries, 2026. https://www.getaleph.com/blog/2026-saas-benchmarks-takeaways
[T11B-S18] Google, SRE Workbook Implementing SLOs and Cloud Monitoring service monitoring docs. https://sre.google/workbook/implementing-slos/
[T11B-S19] ClickHouse, LLM inference latency guide, 2026. https://clickhouse.com/resources/engineering/llm-inference-latency
[T12-S1] Gibson Dunn, EU AI Act Omnibus Agreement, 2026. https://www.gibsondunn.com/eu-ai-act-omnibus-agreement-postponed-high-risk-deadlines-and-other-key-changes/
[T12-S2] Obligara, EU AI Act high-risk obligations delayed to December 2027, 13 November 2026. https://obligara.com/news/2026-11-13-eu-ai-act-digital-omnibus-delay
[T12-S3] The European Post, Digital Omnibus on AI delays high-risk rules, 2026. https://theeuropeanpost.eu/european-affairs/digital-omnibus-on-ai-delays-high-risk-rules-to-december-2027/
[T12-S4] European Commission AI Act Service Desk, Commission enforcement powers for advanced models, 2026. https://ai-act-service-desk.ec.europa.eu/en/ai-act/faq/commissions-enforcement-powers-related-ai-act-obligations-providers-most-advanced-models
[T12-S5] Cooley, EU AI Act transparency obligations take effect 2 August 2026, 3 August 2026. https://cooley.com/news/insight/2026/2026-08-03-eu-ai-act-transparency-obligations-take-effect-2-august-2026
[T12-S6] Fieldfisher, UK Government's AI and copyright report, March 2026. https://www.fieldfisher.com/en/services/intellectual-property/intellectual-property-blog/uk-government-maintains-status-quo-on-ai-and-copyr
[T12-S7] IAPP, King's Speech signals diffuse UK digital policy agenda, but no AI bill, May 2026. https://iapp.org/news/a/king-s-speech-signals-diffuse-uk-digital-policy-agenda-but-no-ai-bill
[T12-S8] UK Government DSIT, AI Growth Lab call for evidence, 2025. https://www.gov.uk/government/calls-for-evidence/ai-growth-lab
[T12-S9] ICO, One year on: the Data (Use and Access) Act, June 2026. https://ico.org.uk/about-the-ico/media-centre/news-and-blogs/2026/06/one-year-on-marking-the-12-month-commencement-of-the-data-use-and-access-act/
[T12-S10] Paul Hastings, President Trump signs executive order challenging state AI laws, December 2025. https://www.paulhastings.com/insights/client-alerts/president-trump-signs-executive-order-challenging-state-ai-laws
[T12-S11] Norton Rose Fulbright, xAI sues, DOJ intervenes, enforcement of Colorado AI Act suspended, 2026. https://www.nortonrosefulbright.com/en-us/knowledge/publications/de3ad9de/xai-sues-doj-intervenes-enforcement-of-colorado-ai-act-suspended
[T12-S12] Future of Privacy Forum, The RAISE Act vs. SB 53, 2026. https://fpf.org/blog/the-raise-act-vs-sb-53-a-tale-of-two-frontier-ai-laws/
[T12-S13] Bloomberg Law, Anthropic, authors' USD 1.5 billion deal earns final approval, July 2026. https://news.bgov.com/litigation/anthropic-authors-1-5-billion-deal-receives-final-approval
[T12-S14] Press Gazette, Publishers versus AI: all the copyright legal rulings so far, 2026. https://pressgazette.co.uk/media_law/ai-legal-rulings/
[T12-S15] Axios, Disney's landmark OpenAI deal, 11 December 2025. https://www.axios.com/2025/12/11/disney-openai-sora-deal
[T12-S16] OpenAI, Business data privacy, security and compliance, and Introducing data residency in Europe, 2026. https://openai.com/index/introducing-data-residency-in-europe/
[T12-S17] Anthropic, Commercial Terms, effective 17 June 2025. https://www.anthropic.com/legal/commercial-terms
[T12-S18] Anthropic, API and data retention, 2026. https://platform.claude.com/docs/en/manage-claude/api-and-data-retention
[T12-S20] Google Cloud, Vertex AI and zero data retention, 2026. https://docs.cloud.google.com/vertex-ai/generative-ai/docs/data-governance
[T12-S21] Microsoft Learn, Azure OpenAI abuse monitoring, 2025. https://learn.microsoft.com/en-us/azure/ai-foundry/openai/concepts/abuse-monitoring
[T12-S22] Microsoft Learn, Anthropic models in Microsoft Online Services, 2026. https://learn.microsoft.com/en-us/microsoft-365/copilot/connect-to-ai-subprocessor
[T12-S23] AWS, Cross-region inference for EU data processing, 2026. https://aws.amazon.com/blogs/machine-learning/unlocking-ai-flexibility-in-europe-a-guide-to-cross-region-inference-for-eu-data-processing-and-model-access/
[T12-S24] OpenAI, Response to NYT data demands, 2025. https://openai.com/index/response-to-nyt-data-demands/
[T12-S25] Cloud Security Alliance, Indirect prompt injection goes operational, 2026. https://labs.cloudsecurityalliance.org/research/csa-research-note-indirect-prompt-injection-in-the-wild-2026/
[T12-S26] IBM, Cost of a Data Breach Report 2025 press release, 30 July 2025. https://newsroom.ibm.com/2025-07-30-ibm-report-13-of-organizations-reported-breaches-of-ai-models-or-applications,-97-of-which-reported-lacking-proper-ai-access-controls
[T12-S27] Cloud Security Alliance, AI governance and ISO 42001 FAQs 2026. https://cloudsecurityalliance.org/articles/ai-governance-and-iso-42001-faqs-what-organizations-need-to-know-in-2026
[T12-S28] Holland and Knight, Operation AI Comply two years later, 18 August 2026. https://www.hklaw.com/en/insights/publications/2026/08/operation-ai-comply-2-years-later-continued-enforcement
[T12-S29] Linux Foundation, State of FinOps survey 2026, 19 February 2026. https://www.linuxfoundation.org/press/state-of-finops-survey-ai-value-and-skills-top-priorities-as-finops-matures-across-technology-value-98-manage-ai-90-saas-64-licensing-48-data-center-1
[T12-S31] Google Cloud, Protecting customers with generative AI indemnification, 2023. https://cloud.google.com/blog/products/ai-machine-learning/protecting-customers-with-generative-ai-indemnification
[T12-S32] IEA, Energy and AI: energy demand from AI, 2025. https://www.iea.org/reports/energy-and-ai/energy-demand-from-ai
[T12-S34] Bloomberg, The USD 10 trillion fight: modelling a US-China war over Taiwan, 10 February 2026. https://www.bloomberg.com/news/articles/2026-02-10/the-10-trillion-fight-modeling-a-us-china-war-over-taiwan
[T12-S35] CNBC, Moody's says unprecedented AI spending threatens credit quality, 24 July 2026. https://www.cnbc.com/2026/07/24/moodys-ai-spending-credit-quality-amazon-meta-alphabet.html
[T12-S37] Axios, The AI boom has a new complication: falling prices, 22 October 2026. https://axios.com/2026/10/22/ai-token-prices-demand
[T12-S38] Stanford Digital Economy Lab, Canaries in the Coal Mine, August 2026. https://digitaleconomy.stanford.edu/app/uploads/2026/08/Canaries_August2026.pdf
[T12B-S1] OpenAI, Your data (developer docs), 2026. https://developers.openai.com/api/docs/guides/your-data
[T12B-S2] The Next Web, OpenAI previews Private Safety Processing, August 2026. https://thenextweb.com/news/openai-zero-data-retention-private-safety-processing
[T12B-S3] Anthropic, API and data retention, 2026. https://platform.claude.com/docs/en/manage-claude/api-and-data-retention
[T12B-S4] Anthropic, Data residency, 2026. https://platform.claude.com/docs/en/manage-claude/data-residency
[T12B-S5] Anthropic, Regional compliance, 2026. https://claude.com/regional-compliance
[T12B-S6] ITPro, Google Cloud unveils UK data residency options for Vertex AI. https://www.itpro.com/cloud/cloud-computing/google-cloud-unveils-uk-data-residency-options-for-vertex-ai-customers
[T12B-S7] Morgan Lewis, Key considerations for evaluating an AI vendor, November 2026. https://www.morganlewis.com/blogs/sourcingatmorganlewis/2026/11/key-considerations-for-evaluating-an-ai-vendor
[T12B-S8] Press Gazette, News publisher AI deals and lawsuits. https://pressgazette.co.uk/platforms/news-publisher-ai-deals-lawsuits-openai-google/
[T12B-S9] Linux Foundation, State of FinOps survey, 19 February 2026. https://www.linuxfoundation.org/press/state-of-finops-survey-ai-value-and-skills-top-priorities-as-finops-matures-across-technology-value-98-manage-ai-90-saas-64-licensing-48-data-center-1
[T12B-S11] BSI, BSI awards its 50th ISO/IEC 42001 certificate, November 2026. https://www.bsigroup.com/en-GB/insights-and-media/media-centre/press-releases/2026/november/bsi-awards-its-50th-iso-iec-42001-certificate/
[T12B-S12] NACD Directorship, AI washing risk, Spring 2026. https://www.nacdonline.org/all-governance/governance-resources/directorship-magazine/directorship-spring-2026-issue/ai-washing-risk/
[T12B-S13] Glass Lewis, US AI oversight through three lenses, March 2026. https://www.glasslewis.com/article/us-ai-oversight-through-three-lenses-investor-expectations-sp-100-company-specific-analysis
[T12B-S14] XBRL.org, FRC guidance on AI in audit, April 2026. https://www.xbrl.org/?p=18375
[T12B-S15] CFO Dive, Deloitte refunds report AI errors, October 2025. https://www.cfodive.com/news/deloitte-refunds-60k-report-ai-errors-australian-government-accounting/803321/
[T12B-S16] American Bar Association, BC tribunal confirms companies remain liable for chatbot information, February 2024. https://www.americanbar.org/groups/business_law/resources/business-law-today/2024-february/bc-tribunal-confirms-companies-remain-liable-information-provided-ai-chatbot/
[T12B-S17] The Register, Replit SaaStr incident, 21 July 2025. https://www.theregister.com/2025/07/21/replit_saastr_vibe_coding_incident
[T12B-S18] Good Morning America, rogue AI agent PocketOS, 2026. https://www.goodmorningamerica.com/news/story/rogue-ai-agent-haywire-tech-company-ceo-bullish-132473181
[T12B-S19] Stanford Digital Economy Lab, Canaries in the Coal Mine, 12 August 2026. https://digitaleconomy.stanford.edu/news/canariesaug26/
[T12B-S20] European Commission AI Act Service Desk, Article 99. https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-99
[T12B-S22] Republic of China (Taiwan) government, February 2024 issue, and Taipei Times, 2024. https://www.roc-taiwan.org/uploads/sites/86/2024/02/February-2024-Issue.pdf
[T12B-S23] Axios, Historic NYT v. OpenAI copyright battle heats up, 8 September 2026. https://axios.com/2026/09/08/nyt-openai-microsoft-copyright-lawsuit
[T12B-S24] Bloomberg Law, Meta sued by hundreds of authors, 20 October 2026. https://news.bloomberglaw.com/ip-law/meta-sued-by-hundreds-of-authors-in-ai-training-copyright-cases
[T13-S1] Anthropic, AI Fluency courses and framework pages, 2026. https://www.anthropic.com/ai-fluency
[T13-S2] Lewis Silkin, The Digital Omnibus on AI enters into force today, 27 July 2026. https://www.lewissilkin.com/insights/2026/07/27/the-digital-omnibus-on-ai-enters-into-force-today-102nedo
[T13-S3] European Commission and OECD, Empowering Learners for the Age of AI, 18 June 2026. https://education.ec.europa.eu/node/3537
[T13-S4] UNESCO, AI competency frameworks for students and teachers, 2024 (via Cedefop summary). https://www.cedefop.europa.eu/en/node/157949
[T13-S5] Anthropic Academy and Analytics Vidhya, Free Anthropic AI courses, March 2026. https://www.anthropic.com/learn
[T13-S6] DeepLearning.AI, AI for Everyone, 2026. https://www.deeplearning.ai/courses/ai-for-everyone
[T13-S7] Grow with Google, Google AI Essentials, 2026. https://grow.google/certificates/en_uk/certificates/ai
[T13-S8] University of Leeds, Join the free Microsoft AI Skills Fest 2026, 2026. https://students.business.leeds.ac.uk/news/join-the-free-microsoft-ai-skills-fest-2026/
[T13-S9] Saïd Business School and GetSmarter, Oxford Artificial Intelligence Programme, 2026. https://www.sbs.ox.ac.uk/programmes/executive-education/online-programmes/oxford-artificial-intelligence-programme
[T13-S10] University of Helsinki and EU Digital Skills portal, Elements of AI, 2026. https://digital-skills-jobs.europa.eu/en/learning-space/training-catalogue/elements-ai
[T13-S11] UK Private Capital (BVCA), Harnessing AI for Private Capital, 2026. https://www.ukprivatecapital.co.uk/bvca-training/harnessing-ai-for-private-capital-from-origination-to-value-creation-oct26.html
[T13-S12] ki-campus.org and Globalnerdy, 3Blue1Brown neural networks series, 2017 series. https://3blue1brown.com/topics/neural-networks
[T13-S13] Andrej Karpathy, Neural Networks: Zero to Hero, ongoing. https://karpathy.ai/zero-to-hero.html
[T13-S14] fast.ai, Practical Deep Learning, 2025. https://course.fast.ai/
[T13-S15] O'Reilly, AI Engineering by Chip Huyen, January 2025. https://www.oreilly.com/library/view/ai-engineering/9781098166298/
[T13-S16] Wikipedia and Simon and Schuster, Chip War, 2022. https://en.wikipedia.org/wiki/Chip_War
[T13-S17] Stanford HAI, The 2026 AI Index Report, 13 April 2026. https://hai.stanford.edu/ai-index/2026-ai-index-report
[T13-S18] Air Street Capital, State of AI Report 2026, 8 October 2026. https://www.stateof.ai/
[T13-S19] Epoch AI, Trends in AI, 5 February 2026. https://epoch.ai/trends
[T13-S24] Opper AI, LLM rankings in 2026: how leaderboards work, 2026. https://opper.ai/blog/llm-rankings-explained
[T13-S25] Lovable, Subscription plans, 2026. https://docs.lovable.dev/introduction/subscription-plans
[T13-S26] Replit, Billing and AI billing documentation, 2026. https://docs.replit.com/billing
[T13-S27] Vercel and Dupple, v0 pricing, and Bolt pricing summaries, 2026. https://vercel.com/blog/updated-v0-pricing
[T13-S29] Anthropic, Max plan, 2026. https://anthropic.com/news/max-plan
[T13-S30] Supabase, Pricing, 2026. https://supabase.com/pricing
[T13-S32] Wiz Research, Common security risks in vibe coded apps, 2026. https://www.wiz.io/blog/common-security-risks-in-vibe-coded-apps
[T13-S33] Freeman et al., Active learning increases student performance, PNAS, 2014. https://pmc.ncbi.nlm.nih.gov/articles/PMC4060654/
[T13-S34] Shen and Tamkin, How AI Impacts Skill Formation, Anthropic, 29 January 2026. https://www.anthropic.com/research/AI-assistance-coding-skills
[T13-S36] Dell'Acqua et al., Navigating the Jagged Technological Frontier, 2023. https://mitsloan.mit.edu/sites/default/files/2023-10/SSRN-id4573321.pdf
[T13-S37] Udacity, Coursera and Noble Desktop course listings, 2026. https://www.udacity.com/course/generative-ai-fluency--cd13224
[T13-S38] NBER, Who Gets Ahead in Venture Capital (Jackson and Strebulaev), 2026. https://www.nber.org/be/20262/who-gets-ahead-venture-capital-new-evidence-100000-investors-careers
[T13-S39] KPMG, AI pilots and private equity portfolio performance, September 2026. https://kpmg.com/us/en/articles/2026/ai-pilots-private-equity-portfolio-performance.html
[T13-S40] Peony and others, AI Due Diligence checklist, 2026. https://www.peony.ink/blog/ai-due-diligence
[T13-S41] London Tech Week and DataCamp newsletter roundup, 2026. https://londontechweek.com/
[T13B-S1] Hatchworks, AI Due Diligence, 2026, with Foley, Grant Thornton and EY items. https://hatchworks.com/blog/pe/ai-due-diligence/
[T13B-S2] Mergers and Acquisitions, Best Places to Work in Private Equity 2026 roundup, and workwisesolutions guide. https://workwisesolutions.org/guides/ai-training-private-equity-complete-guide.html
[T13B-S3] NBER, Who Gets Ahead in Venture Capital, 2026, and related studies. https://www.nber.org/be/20262/who-gets-ahead-venture-capital-new-evidence-100000-investors-careers
[T13B-S4] DEV Community and Medium non-engineer build accounts, 2026. https://dev.to/shahidsaleem/im-not-a-developer-i-built-a-working-app-in-one-weekend-with-claude-code-jf4
[T13B-S5] Stanford AI Catalyst, findskill, DataCamp and a course guide on Anthropic Academy, 2026. https://aicatalyst.stanford.edu/tracks/anthropic-claude-essentials
[T13B-S6] Karpathy site, aiagentrank, 3Blue1Brown and DeepLearning.AI listings, 2026. https://karpathy.ai/zero-to-hero.html
[T13B-S7] Salesforce, Generative AI skills research, 2023, and TechTarget. https://www.salesforce.com/news/generative-ai-skills-research
[T13B-S8] Import AI, Jack Clark, 2026. https://jack-clark.net/2026/08/10/import-ai-468-23-rsi-ideas-posttrainbench-and-how-trust-and-transparency-interplay-with-ai-racing/
[T13B-S9] DeepLearning.AI, The Batch, 2026. https://www.deeplearning.ai/the-batch/tag/the-batch
[T13B-S10] Apple Podcasts, Latent Space: The AI Engineer Podcast, 2026. https://podcasts.apple.com/us/podcast/id1674008350
[T13B-S11] Dwarkesh Podcast listings, 2026. https://www.dwarkesh.com/
[T13B-S12] Apple Podcasts, Hard Fork, November 2026. https://podcasts.apple.com/us/podcast/id1528594034
[T13B-S13] Stratechery and Subger, 2026. https://stratechery.com/outline/do-you-offer-a-student-discount/
[T13B-S14] SemiAnalysis FAQ and GPU pricing pages, 2026. https://semianalysis.com/faq/
[T13B-S15] Luma, createwith and London Tech Events Weekly, 2026. https://buttondown.com/londontechevents/archive/u1f680-london-tech-events-nov-8-nov-15-ai-business/
[T13B-S16] Saïd Business School, Oxford Artificial Intelligence Programme, 2026. https://www.sbs.ox.ac.uk/programmes/executive-education/online-programmes/oxford-artificial-intelligence-programme
[T13B-S17] Anthropic, Pricing, 2026. https://www.anthropic.com/pricing
[T13B-S18] Vercel, Pro plan docs and pricing, 2026. https://vercel.com/docs/plans/pro-plan
[T13B-S19] v0, Pricing docs, 2026. https://v0.app/docs/pricing
[T13B-S20] Cursor, Pricing and plans help page, 2026. https://cursor.com/help/account-and-billing/pricing
[T14-S1] Machine Learning Mastery, How LLMs choose their words: logits, softmax and sampling. https://machinelearningmastery.com/how-llms-choose-their-words-a-practical-walk-through-of-logits-softmax-and-sampling/
[T14-S2] Karpathy, Deep Dive into LLMs like ChatGPT, February 2025, via secondary write-ups. https://tuananhbui89.github.io/blog/2025/karpathy-lec08
[T14-S3] IBM and AWS, What is embedding. https://www.ibm.com/think/topics/embedding
[T14-S4] IBM, What is self-attention. https://www.ibm.com/think/topics/self-attention
[T14-S5] Meta, The Llama 3 Herd of Models, July 2024, and Hugging Face Llama 3.1 405B config. https://ar5iv.labs.arxiv.org/html/2407.21783
[T14-S6] 3Blue1Brown, Attention in Transformers, via course summary and Columbia COMS 4705 notes. https://www.cs.columbia.edu/~johnhew/coms4705/lecs-html/lec_8_attn_trnsf.html
[T14-S7] NVIDIA, Mastering LLM Techniques: Inference Optimization. https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization
[T14-S8] OpenAI API reference temperature wording, quoted in OpenAI Developer Community. https://community.openai.com/t/temperature-docs-for-1-max-vs-2-max/309112
[T14-S9] Anthropic Messages API reference (mirror). https://docs.anthropic.com/en/api/messages
[T14-S10] Google AI for Developers, Gemini 3 Developer Guide. https://ai.google.dev/gemini-api/docs/gemini-3
[T14-S11] OpenAI, Deprecations page, and Tessl coverage of OpenAI shutting fine-tuning. https://developers.openai.com/docs/deprecations
[T14-S12] Tessl, OpenAI shutting fine-tuning signals for enterprise AI. https://tessl.io/blog/openai-shutting-fine-tuning-signals-for-enterprise-ai
[T14-S13] OpenAI, GPT-4o fine-tuning, August 2024, and third-party price lists (GuptaDeepak, AI Prompt Generator Hub). https://openai.com/index/gpt-4o-fine-tuning/
[T14-S14] Together AI, RAG vs fine-tuning, with Oracle and Progress guides. https://www.together.ai/blog/rag-vs-fine-tuning
[T14-S15] Google for Developers, Machine Learning Glossary. https://developers.google.com/machine-learning/glossary/
[T14-S16] IBM, What is a hyperscale data center, and Oracle, What is a hyperscale cloud. https://www.ibm.com/think/topics/hyperscale-data-center/
[T14-S17] IBM, AI vs machine learning vs deep learning vs neural networks, and Cornell Virtual Workshop. https://ibm.com/blog/ai-vs-machine-learning-vs-deep-learning-vs-neural-networks
[T14-S18] Tian Pan, Build vs buy LLM infrastructure, April 2026, arXiv 2509.18101, IntuitionLabs and ML6. https://tianpan.co/blog/2026-04-15-build-vs-buy-llm-infrastructure
[T14-S19] SemiAnalysis, TPU InferenceX, and Goldman Sachs note via iTiger, 2026. https://newsletter.semianalysis.com/p/tpu-inferencex-full-steam
[T14-S20] Google Developers Blog, TorchTPU, and InfoQ, October 2026. https://developers.googleblog.com/en/torchtpu-running-pytorch-natively-on-tpus-at-google-scale/
[T14-S21] AWS Migration blog on Trainium kernels, and TorchNeuron coverage, October 2026. https://aws.amazon.com/blogs/migration-and-modernization/stop-hand-porting-kernels-migrate-pytorch-and-triton-kernels-to-aws-trainium-with-an-aws-transform-custom-agent/
[T15-S1] a16z, "why ai moats still matter and how they've changed" and Apps Fund summaries, via search, 2026. https://a16z.com/podcast/why-ai-moats-still-matter-and-how-theyve-changed/
[T15-S2] Bessemer Venture Partners, The State of AI 2025, August 2025. https://www.bvp.com/atlas/the-state-of-ai-2025
[T15-S3] NFX, How AI Companies Will Build Real Defensibility, 2026, and secondhand Sequoia AI Ascent 2026 summary. https://nfx.com/post/ai-defensibility
[T15-S4] CRV, AI Applications: Where They Keep Value and Where They Are Easy to Copy, 2026. https://www.crv.com/content/ai-applications
[T15-S5] Directions on Microsoft and UC Today, Microsoft 365 Copilot paid seats, January and July 2026. https://www.directionsonmicrosoft.com/blog/microsoft-claims-15-million-paid-m365-copilot-seats
[T15-S6] Salesforce, Q4 fiscal 2026 results, 25 February 2026. https://www.salesforce.com/news/press-releases/2026/02/25/fy26-q4-earnings/
[T15-S7] The Information via Yahoo Finance and Hunton, Salesforce blocks AI rivals from using Slack data, June 2025. https://finance.yahoo.com/news/salesforce-blocks-ai-rivals-using-014746612.html
[T15-S8] Morningstar and eWeek, Thomson Reuters, RELX and Wolters stocks after Anthropic legal plugin, February 2026. https://global.morningstar.com/en-ca/stocks/reuters-relx-wolters-stocks-crushed-after-anthropic-debuts-claude-legal-plug-in
[T15-S9] TechCrunch and Gizmodo, ChatGPT PDF update and wrapper start-ups, November 2023. https://techcrunch.com/2023/11/06/get-the-pdf-outta-here
[T15-S10] Chegg results coverage via TechRadar and Nasdaq, 2025. https://www.techradar.com/pro/chegg-announces-move-to-reduce-workforce-by-22-percent-as-students-turn-to-ai
[T15-S11] Ramp, AI Index, October 2026 and TechCrunch 13 May 2026. https://ramp.com/data/ai-index
[T15-S12] ICONIQ, State of AI 2026, with GTM commentary. https://www.iconiq.com/growth/insights/state-of-ai-2026
[T15-S13] The Decoder, DevOps.com and DeepLearning.AI, Cursor Composer 2 and 2.5, 2026. https://the-decoder.com/cursor-quietly-built-its-new-coding-model-on-top-of-chinese-open-source-kimi-k2-5
[T15-S14] OpenAI, The State of Enterprise AI 2025 report, December 2025. https://openai.com/index/the-state-of-enterprise-ai-2025-report/
[T15-S15] DEV Community, Gartner via search, Fin and Zendesk, AI agent unit economics and cost per resolution, 2026. https://dev.to/mr_manushukla/ai-agent-unit-economics-in-2026-the-true-cost-per-resolved-task-and-the-human-break-even-4lf4
[T15-S16] Intercom and Enterprise DNA, Fin resolution rate, 2026. https://enterprisedna.co/resources/ai-pulse/ai-pulse-2026-08-02-intercom-s-fin-ai-agent-is-nearing-100m-arr-roughly-half-of
[T15-S17] Dealroom, Anthropic vs OpenAI ARR, August 2026, and Epoch AI. https://epoch.ai/data-insights/anthropic-openai-revenue
[T15-S18] Epoch AI, Anthropic and OpenAI compute spend growth, 2026. https://epoch.ai/data-insights/anthropic-openai-compute-spend-growth
[T15-S19] Moody's via DatacenterDynamics, Tom's Hardware and Yahoo Finance, hyperscaler capex and AI run rates, 2026. https://datacenterdynamics.com/en/news/moodys-hyperscaler-capex-forecasts-marked-up-by-85bn-to-close-in-on-1trn-by-2027/
[T15-S20] Bain, 2025 Global Technology Report press release, 23 September 2025. https://www.bain.com/about/media-center/press-releases/20252/$2-trillion-in-new-revenue-needed-to-fund-ais-scaling-trend---bain--companys-6th-annual-global-technology-report/
[T16-S1] The Register, What Nvidia's Blackwell efficiency gains mean for DC owners, 27 March 2024. https://www.theregister.com/2024/03/27/nvidia_blackwell_efficiency/
[T16-S2] SemiAnalysis, H100 vs GB200 NVL72 training benchmarks, 2025. https://newsletter.semianalysis.com/p/h100-vs-gb200-nvl72-training-benchmarks
[T16-S3] Nvidia, DGX SuperPOD data centre design for H100, electrical specifications. https://docs.nvidia.com/dgx-superpod/design-guides/dgx-superpod-data-center-design-h100/latest/electrical.html
[T16-S4] Nvidia, DGX B200 product page. https://www.nvidia.com/en-gb/data-center/dgx-b200/
[T16-S5] Search summary of Schneider, Vertiv and SemiAnalysis designs, 2024 to 2026. https://newsletter.semianalysis.com/p/datacenter-anatomy-part-1-electrical
[T16-S7] SemiAnalysis, How Much Do GPU Clusters Really Cost, 2024. https://newsletter.semianalysis.com/p/how-much-do-gpu-clusters-really-cost
[T16-S8] Epoch AI, Total cost of ownership of a one-gigawatt AI data center, 2026. https://epoch.ai/data-insights/ai-datacenter-cost-breakdown
[T16-S9] The Register, The network is indeed trying to become the computer, 27 June 2025. https://www.theregister.com/2025/06/27/analysis_network_computing/
[T16-S10] Epoch AI, Introducing the Frontier Data Centers hub, 2026. https://epoch.ai/latest/introducing-the-frontier-data-centers-hub
[T16-S11] Stocktwits, Jensen Huang puts $50 billion price tag on 1 GW AI factory, GTC Berlin. https://stocktwits.com/news-articles/markets/equity/nvidia-gtc-berlin-keynote-jensen-huang-puts-50-billion-price-tag-on-1-gw-ai-factory/cZxt68mRBvI
[T16-S12] McKinsey, The cost of compute: a $7 trillion race to scale data centers, 2025. https://www.mckinsey.com/industries/technology-media-and-telecommunications/our-insights/the-cost-of-compute-a-7-trillion-dollar-race-to-scale-data-centers
[T16-S13] Pytorch to Atoms, Meta's 24k H100 cluster capex, TCO and BoM analysis, 2024. https://pytorchtoatoms.substack.com/p/metas-24k-h100-cluster-capextco-and
[T16-S14] CloudRift, The true cost of GPU ownership, 2026. https://www.cloudrift.ai/blog/the-true-cost-of-gpu-ownership
[T16-S15] Nebius Q2 2026 shareholder letter, via FourWeekMBA. https://fourweekmba.com/ai-nebius-puts-q2-deal-payback-at-22-months-on-5-year-servers/
[T16-S16] The Block, IREN's $25 billion to $30 billion AI buildout, 28 August 2026. https://theblock.co/news/business/2026-08-28-irens-25-billion-30-billion-ai-buildout-may-have-spooked-investors-bernstein-says-413016
[T16-S20] AWS, EC2 Capacity Blocks pricing, 2026. https://aws.amazon.com/ec2/capacityblocks/pricing
[T16-S21] DoiT, AWS EC2 p5.48xlarge spot pricing, 2026. https://www.doit.com/compute/spot/us-east-1/p5.48xlarge
[T16-S22] CoreWeave documentation, instance pricing, 2026. https://docs.coreweave.com/docs/pricing/pricing-instances
[T16-S23] Lambda, AI cloud pricing, 2026. https://www.lambda.ai/pricing
[T16-S24] RunPod pricing and Spheron summary, 2026. https://www.runpod.io/pricing
[T17-S1] Supabase, State of Startups 2026 (vendor survey) and Product Hunt summary, June 2026. https://supabase.com/state-of-startups
[T17-S2] Qovery, Vercel vs AWS for AI agents in 2026 (supplier), 19 November 2026. https://www.qovery.com/blog/vercel-vs-aws-ai-agents-2026
[T17-S3] Monk, Moving from Vercel and Supabase to AWS, August 2026, and Resend, What is our tech stack. https://monk.com/blog/why-we-moved-monk-to-aws
[T17-S4] Loops, Migrating to AWS in production with zero downtime, 2026. https://loops.so/engineering/migrating-to-aws-in-production-with-zero-downtime
[T17-S5] Darshan Turakhia, From Vercel to AWS part 3, and ClickItTech migration guide, 2026. https://darshanturakhia.com/blog/from-vercel-to-aws-part-3-migration
[T17-S6] Peerlist, DEV Community and WebCatalog migration posts, 2025 to 2026 (blogs and sellers). https://peerlist.io/federicopochat/articles/why-smart-startups-are-saying-goodbye-vercel--and-how-obelis
[T17-S7] Supabase billing docs (MAU example) and Jetadmin and Schematic cost guides, 2026. https://supabase.com/docs/guides/platform/manage-your-usage/monthly-active-users
[T17-S8] Metacast, LLM bots and Next.js image optimization post-mortem, February 2025. https://metacast.app/blog/engineering/postmortem-llm-bots-image-optimization
[T17-S9] UsageBox, The $23,000 Vercel bill, June 2026, and Digg, $1,335 Vercel bill. https://usagebox.com/articles/vercel-23000-dollar-bill-usage-based-platform-bill-shock-2026
[T17-S10] FactualMinds, AWS bill teardown of a SaaS start-up, 2026. https://www.factualminds.com/blog/aws-bill-teardown-1-saas-startup-40k-month-overrun/
[T17-S11] Supabase, Project Pausing docs, accessed 26 November 2026. https://supabase.com/docs/guides/platform/pausing
[T17-S12] Supabase, Connecting to your database and pooler guide, accessed 26 November 2026. https://supabase.com/docs/guides/database/connecting-to-postgres
[T17-S13] Supabase, Troubleshooting remaining connection slots and Prisma guides, accessed 26 November 2026. https://supabase.com/docs/guides/troubleshooting/database-error-remaining-connection-slots-are-reserved-for-non-replication-superuser-connections-3V3nIb
[T17-S14] Vercel, FUNCTION_INVOCATION_TIMEOUT and Functions limitations, accessed 26 November 2026. https://vercel.com/docs/functions/limitations
[T17-S15] Vercel, Pro plan and Spend Management docs, accessed 26 November 2026. https://vercel.com/docs/plans/pro-plan
[T17-S16] Cloudflare, Workers limits and Error 1102 docs, accessed 26 November 2026. https://developers.cloudflare.com/workers/platform/limits/
[T17-S17] AWS, Lambda quotas and scaling docs, accessed 26 November 2026. https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html
[T17-S18] AWS Compute Blog, Lambda standardizes billing for INIT phase, 29 April 2025. https://aws.amazon.com/blogs/compute/aws-lambda-standardizes-billing-for-init-phase
[T17-S19] Vercel, 360 billion tokens, 3 million customers, 6 engineers (customer story, supplier). https://vercel.com/customers/360-billion-tokens-3-million-customers-6-engineers
[T17-S20] Google Cloud, 2025 DORA report announcement, and earlier DORA platform findings via TechTarget. https://cloud.google.com/blog/products/ai-machine-learning/announcing-the-2025-dora-report
[T17-S21] DX, DevProd headcount benchmarks Q1 2026, and OpenGenus developer to DevOps ratio. https://getdx.com/blog/devprod-headcount-benchmarks-q1-2026/
[T18-S1] Toucan Toco, Requests Per Second glossary, and Educative, 2026. https://www.toucantoco.com/en/glossary/requests-per-second
[T18-S2] OpenAI, GPT-5 model page and rate limits guide, 2026. https://developers.openai.com/api/docs/guides/rate-limits
[T18-S3] Anthropic, Rate limits documentation, 2026. https://docs.anthropic.com/en/api/rate-limits
[T18-S4] Google, SRE Workbook, Implementing SLOs and SRE book chapters 3 and 4, 2026. https://sre.google/workbook/implementing-slos/
[T18-S5] AWS, Well-Architected Reliability Pillar, Availability, 2026. https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/availability.html
[T18-S6] OpenAI status page, Nordic APIs reliability report 2026, Redress Compliance SLA article, 2026. https://status.openai.com
[T18-S7] ICONIQ, 2026 State of AI Report, January 2026, and SaaStr summary. https://www.iconiq.com/growth/insights/state-of-ai-2026
[T18-S8] Rework, Inference costs and gross margin in AI companies, 2026. https://resources.rework.com/libraries/ai-startup-growth/ai-inference-costs-gross-margin
[T18-S9] The Register, Microsoft's GitHub shifts to metered, 28 April 2026, and The Register, 11 October 2023. https://www.theregister.com/2026/04/28/microsofts_github_shifts_to_metered/
[T18-S10] Wavect, Technical due diligence for AI, and Peony, AI due diligence checklist, 2026. https://wavect.io/blog/technical-due-diligence-ai-mvp/
[T18-S11] Rework, AI security reviews explained, and UT Ventures AI due diligence framework, July 2026. https://utventures.tennessee.edu/wp-content/uploads/2026/07/AI-Due-Diligence-Framework-7-6-26.pdf
[T18-S12] Beyond Elevation, AI due diligence 6-point framework, 2026. https://beyondelevation.com/insights/ai-due-diligence-ma-framework
[T18-S13] SFIA Foundation, SFIA 9 levels of responsibility, 2026. https://sfia-online.org/en/sfia-9/responsibilities
[T18-S14] UNESCO, AI competency frameworks for students and teachers, 2024, and University of Southampton guide. https://unesdoc.unesco.org/
[T18-S15] European Commission and OECD, AI Literacy Framework, 18 June 2026. https://education.ec.europa.eu/node/3537
[T18-S16] Masai School, Vibe coding learning path, 2026. https://www.masaischool.com/resources/vibe-coding
[T18-S17] AI Builder Club, Vibe coding for non-technical founders, 2026. https://www.aibuilderclub.com/blog/vibe-coding-non-technical-founders
[T18-S18] Ziplines, How to vibe code: a 90-day roadmap for non-coders, 2026. https://www.ziplines.com/blog/how-to-vibe-code
[T18-S19] Maven, AI Build Lab Accelerator and AI Fundamentals for non-engineers, 2026. https://maven.com/aibuildlab/ai-build-lab-accelerator
[T19-S1] Google for Developers, Machine Learning Glossary: ML Fundamentals. https://developers.google.com/machine-learning/glossary/fundamentals
[T19-S2] arXiv 2604.06515 and arXiv 2509.02512, papers on mixture-of-experts quantisation and gating, 2025 to 2026. https://arxiv.org/pdf/2604.06515
[T19-S3] Google Research, A Fast WordPiece Tokenization System. https://research.google/blog/a-fast-wordpiece-tokenization-system/
[T19-S4] Google for Developers, Machine Learning Glossary: Generative AI. https://developers.google.com/machine-learning/glossary/generative
[T19-S5] IBM, What is reinforcement learning from human feedback (RLHF)? https://www.ibm.com/think/topics/rlhf
[T19-S6] arXiv 2505.03804, MoEQuant, and arXiv 2310.02410, Mixture of Quantized Experts. https://arxiv.org/pdf/2505.03804
[T19-S7] OpenAI, Structured model outputs guide. https://developers.openai.com/api/docs/guides/structured-outputs
[T19-S8] NIST, ARIA evaluation plan (AI 700-2 and AI 200-3). https://ai-challenges.nist.gov/aria/docs/evaluation_plan.pdf
[T19-S9] NVIDIA, Dynamo glossary. https://docs.nvidia.com/dynamo/latest/reference/glossary
[T19-S10] Anthropic, Prompt caching documentation. https://platform.claude.com/docs/en/build-with-claude/prompt-caching
[T19-S11] Anthropic, Rate limits documentation. https://docs.anthropic.com/en/api/rate-limits
[T19-S12] Anthropic, Compaction documentation. https://platform.claude.com/docs/en/build-with-claude/compaction
[T19-S13] NVIDIA, AI Enterprise glossary. https://docs.nvidia.com/ai-enterprise/release-9/latest/reference/glossary.html
[T19-S14] NVIDIA blog, What Is NVLink? https://blogs.nvidia.com/blog/what-is-nvidia-nvlink/
[T19-S15] IONOS, What is High Bandwidth Memory (HBM) and why is it important for AI GPUs? https://www.ionos.com/digitalguide/server/know-how/high-bandwidth-memory-hbm/
[T19-S16] HPE, Power usage effectiveness. https://www.hpe.com/int/en/what-is/pue.html
[T19-S17] Cisco, What is neocloud. https://www.cisco.com/site/us/en/learn/topics/computing/what-is-neocloud.html
[T19-S18] Nutanix, Neoclouds vs. Hyperscalers. https://www.nutanix.com/blog/neoclouds-vs-hyperscalers
[T19-S19] CRV, What is a Burn Multiple? https://www.crv.com/content/burn-multiple
[T19-S20] Stripe, Net revenue retention (NRR). https://stripe.com/us/resources/more/net-revenue-retention
[T19-S21] AWS, Cloud Computing Concepts Hub (container). https://aws.amazon.com/what-is/
[T19-S22] AWS, Amazon RDS read replicas documentation and FAQs. https://aws.amazon.com/faqs
[T19-S23] AWS Compute Blog, Understanding and remediating cold starts. https://aws.amazon.com/blogs/compute/understanding-and-remediating-cold-starts-an-aws-lambda-perspective/
[T19-S24] Cloudflare, What is a vector database? https://www.cloudflare.com/learning/ai/what-is-vector-database
[T19-S25] Cloudflare, What is retrieval-augmented generation (RAG) in AI? https://www.cloudflare.com/learning/ai/retrieval-augmented-generation-rag
[T19-S26] OWASP GenAI, LLM01:2025 Prompt Injection. https://genai.owasp.org/llmrisk/llm01-prompt-injection/
[T19-S27] Third-party MCP glossaries (back4app, Tyk, Composio), 2025 to 2026. https://tyk.io/learning-center/model-context-protocol-mcp-glossary/
[T19B-S1] OpenAI, openai/evals README and Evals API guide, accessed 26 November 2026. https://github.com/openai/evals
[T19B-S2] Mitchell et al., Model Cards for Model Reporting, FAT* 2019 (arXiv v2, 14 January 2019). https://arxiv.org/abs/1810.03993
[T19B-S3] Anthropic, Claude Platform Docs, Prompting best practices (system prompts), accessed 26 November 2026. https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/system-prompts
[T19B-S4] Anthropic, Claude Platform Docs, Models overview, accessed 26 November 2026. https://platform.claude.com/docs/en/about-claude/models/overview
[T19B-S5] Anthropic, Batch processing docs and Message Batches API announcement, accessed 26 November 2026. https://platform.claude.com/docs/en/build-with-claude/batch-processing
[T19B-S6] Anthropic, Claude Platform Docs, Reduce latency, accessed 26 November 2026. https://platform.claude.com/docs/en/test-and-evaluate/strengthen-guardrails/reduce-latency
[T19B-S7] SigNoz, How to Reduce Claude API Latency, accessed 26 November 2026. https://signoz.io/guides/claude-api-latency/
[T19B-S8] Unity glossary, Graphics processing unit (GPU), accessed 26 November 2026. https://unity.com/glossary/graphics-processing-unit-gpu
[T19B-S9] Google Cloud, Introduction to Cloud TPU, accessed 26 November 2026. https://docs.cloud.google.com/tpu/docs/intro-to-tpu
[T19B-S10] TechTarget, What is floating-point operations per second (FLOPS), accessed 26 November 2026. https://www.techtarget.com/whatis/definition/FLOPS-floating-point-operations-per-second
[T19B-S11] TSMC, CoWoS and Advanced Packaging pages, accessed 26 November 2026. https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/cowos.htm
[T19B-S12] Vertiv, What is colocation, accessed 26 November 2026. https://www.vertiv.com/en-us/insights/articles/educational-articles/what-is-colocation/
[T19B-S13] IFRS Foundation, IAS 16 Property, Plant and Equipment, 2026 edition. https://www.ifrs.org/content/dam/ifrs/publications/html-standards/english/2026/issued/ias16.html
[T19B-S14] Exterran Corp, Form 10-K FY2021, filed 2022. https://www.sec.gov/Archives/edgar/data/1635881/000095017022002691/extn-20211231.htm
[T19B-S15] VirtualScopics, Form SC 14D9, 2016. https://www.sec.gov/Archives/edgar/data/0001307752/000114420416093503/v436560_sc14d9.htm
[T19B-S16] Heska Corp Form 10-K FY2018 (filed 2019) and Ducommun Inc Form 10-K FY2025. https://www.sec.gov/Archives/edgar/data/30305/000162828026011952/dco-20251231.htm
[T19B-S17] Wikipedia, Frontend and backend, and MDN-derived glossary mirror, accessed 26 November 2026. https://en.wikipedia.org/wiki/Front_end_and_back_end
[T19B-S18] AWS, What is AWS Lambda, accessed 26 November 2026. https://docs.aws.amazon.com/lambda/latest/dg/welcome.html
[T19B-S19] AWS, Elastic Load Balancing documentation, accessed 26 November 2026. https://docs.aws.amazon.com/elasticloadbalancing/latest/application/lambda-functions.html
[T19B-S20] Supabase, Connection pooling and limits, accessed 26 November 2026. https://supabase.com/docs/guides/database/connecting-to-postgres/pooling-and-limits
[T19B-S21] Backblaze and Oracle, cloud egress fee explainers, accessed 26 November 2026. https://www.backblaze.com/blog/cloud-101-data-egress-fees-explained/
[T19B-S22] Google Cloud Compute Engine SLA and AWS Service Level Agreements, accessed 26 November 2026. https://cloud.google.com/compute/sla
[T20-S1] IBM, What are LLM parameters? (undated). https://www.ibm.com/think/topics/llm-parameters
[T20-S2] IBM, What are model parameters? (undated). https://www.ibm.com/think/topics/model-parameters
[T20-S3] AWS, What is an API (Application Programming Interface)? (undated). https://aws.amazon.com/what-is/api/
[T20-S4] Nvidia, What Is an AI Factory? (undated). https://www.nvidia.com/en-us/glossary/ai-factory/
[T20-S5] IBM, What are LLM benchmarks? (undated). https://www.ibm.com/think/topics/llm-benchmarks
[T20-S6] NIST, AI 800-3 (2026), via search summary. https://www.nist.gov/node/1905466
[T20-S7] Arena Solutions, What is a Foundry? (undated), and Wikipedia, Foundry model. https://www.arenasolutions.com/resources/glossary/foundry/
[T20-S8] ExpressVPN glossary, Data center rack (undated), and Lenovo, What is a rack server? https://www.expressvpn.com/glossary/data-center-rack/
[T20-S9] AWS CloudWatch GPU Utilization metric, and FinOps Foundation page (undated), via search summary. https://www.finops.org/?p=31499
[T20-S10] FiscalNote Holdings, Form S-1 (2022). https://www.sec.gov/Archives/edgar/data/1823466/000119312522231312/d674968ds1.htm
[T20-S11] BigCommerce Holdings, Form 10-Q (30 June 2022). https://www.sec.gov/Archives/edgar/data/1626450/000156459022028250/bigc-10q_20220630.htm
[T20-S12] MSCI Inc., Form DEF 14A (13 March 2024). https://www.sec.gov/Archives/edgar/data/1408198/000140819824000061/msci-20240313.htm
[T20-S13] IBM, AI vs. machine learning vs. deep learning vs. neural networks (undated). https://ibm.com/blog/ai-vs-machine-learning-vs-deep-learning-vs-neural-networks
[T20-S14] Anthropic, Claude Platform Docs, Messages API (read 26 November 2026), via search summary. https://docs.anthropic.com/en/api/complete
[T20-S15] OpenRouter, Claude 4.7 Migration Guide (undated). https://openrouter.ai/docs/projects/docs/cookbook/evaluate-and-optimize/model-migrations/claude-4-7
[T20-S16] Google, Gemini 3 developer guide, Gemini API (read 26 November 2026). https://ai.google.dev/gemini-api/docs/gemini-3
[T20-S17] Google Cloud, Experiment with parameter values (read 26 November 2026). https://docs.cloud.google.com/gemini-enterprise-agent-platform/models/prompts/adjust-parameter-values
[T20-S18] Microsoft, Azure OpenAI reasoning models (read 26 November 2026). https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/reasoning
[T20-S19] arXiv 2606.26185, grader non-determinism after withdrawal of sampling controls (2026). https://arxiv.org/html/2606.26185
</sources>
</reference_data>

<context>
The reader is intelligent and busy. The reader reads a profit and loss account with ease, but does not know what a token or a GPU is, and has never written code. The reader invests in companies and advises their boards. The reader believes that the best investors are technical, and wants to understand AI as an engineer understands it. With that knowledge, the reader can test the claims of a management team, judge a technology stack and find where value collects in the AI market. The reader will repeat your numbers in meetings with boards and investors, so a wrong number damages the reader's reputation. The reader may also share the page with colleagues who have the same background. One course cannot make an expert, so the course must also show the work that comes after it.
</context>

<task>
Build a course with the name "AI explained" as one interactive web page. The course teaches the subject in the settings from zero. Teach each idea in the same order: a plain statement, a picture, a worked example with real numbers, and then a short check. End each module with two short parts. The "Investor view" states what the module means for value and for risk, and gives questions that the reader can ask. The "Builder view" states how an engineer does the work, which tools the engineer uses and what fails in practice. Go beyond a basic page. Include each diagram, calculator, table, quiz and glossary in the course plan, and make each one work fully.
</task>

<success_criteria>
The course succeeds if the reader can do these twelve things after one reading, without help:
1. Explain in two sentences how a language model makes an answer.
2. Define the 15 core terms: model, parameter, training, inference, token, context window, prompt, GPU, data centre, hyperscaler, utilisation, gross margin, API, retrieval and agent.
3. Calculate the cost of one AI request, and of one agent task with many steps, from the token counts and a price list.
4. Name the seven layers of the AI supply chain, and name one company in each layer.
5. Calculate the cost of one GPU-hour from the purchase price, the useful life, the utilisation and the power cost.
6. Read 10 core KPIs and say what a high value and a low value mean.
7. Ask five useful questions about an AI company or about an AI purchase.
8. Choose a suitable type of platform for a product need that someone describes, and give the reason.
9. Explain how an application scales, and name three parts that fail first when use increases.
10. Name the parts of an AI application (model API, retrieval, tools, evaluation and monitoring), and say what each part does.
11. Read a short API request and name its parts.
12. Calculate the gross margin of an AI application after its model cost, and apply three tests that separate a strong product from a thin layer on a model.
The quiz must test each of the twelve criteria with at least one question.
</success_criteria>

<course_plan>
Write nine modules in this order. Start each module with one sentence that states what the reader will learn. End each module with the "Investor view", the "Builder view" and three "You can now" statements.

Module 1. What AI is, and where the money goes
Teach: AI, machine learning, deep learning, generative AI, large language model (LLM) and agent. A model is a very large mathematical function, and its numbers have the name parameters. Training sets the parameters. Inference uses the parameters to do work. The seven layers of the AI supply chain (energy, data centre, chips, cloud, model, application, user), with one example company in each layer and the direction of the money between layers. Which layers earn a profit today, from the reference data.
Pictures: (a) a nested map that shows how the six terms fit inside each other. (b) The seven layers as a stack, with the flow of money.

Module 2. How a language model works
Teach: tokens. Text in and text out. The model predicts the next token, one token at a time, from probabilities. Embeddings, which change each token into a list of numbers that holds its meaning. Attention, which lets the model weigh each token against the other tokens in the context. Parameters and the size of a model. The three stages of training: training on very large text, fine-tuning, and training with feedback. Temperature. Why the model can state false things (hallucination). The context window. The prompt and the system prompt. The knowledge cut-off date. Reasoning tokens. Models that read images, sound and video. Open-weight models compared with closed models. How a benchmark measures a model, and why a benchmark score can mislead.
Pictures: (a) the path from prompt to answer in five steps, (b) the context window as a box with a fixed size, with its contents.
Interactive: a token demonstration. The reader types text, and the page shows an approximate split into tokens and the token count. Label the result as an estimate.
Builder view: the parts of one API request (the model name, the system prompt, the messages, the maximum number of output tokens and the tools). Show one short example of a request and explain each line.

Module 3. Token economics: how you pay for AI
Teach: the price for each million tokens. Why input tokens and output tokens have different prices. Cached input. The batch discount. Reasoning tokens that the supplier bills as output. Why each turn of a long conversation costs more than the turn before it. Why an agent that takes 20 steps sends its context 20 times. Subscription seats compared with usage prices. How fast prices fall. Why total spend can increase while unit prices fall. Speed: the time to the first token and the tokens for each second. Rate limits.
Picture: a chart of the fall in token prices, from the reference data.
Interactive: a token cost calculator with two modes. Mode 1 is one request. Inputs: the model (from the price list in the reference data), input tokens, output tokens, the share of input that is cached, and requests for each day. Outputs: the cost for each request, each day and each month. Mode 2 is one agent task. Inputs: the number of steps, the tokens in the context at the start, the tokens that each step adds to the context, and the output tokens for each step. Each step sends the full context as input. Output: the total tokens and the cost of the task.
Worked example: one question of 2,000 tokens with an answer of 500 tokens, on two different models.
Builder view: the five methods that an engineer uses to decrease token cost (a smaller model for simple work, the cache, batch requests, a shorter context and a limit on output).

Module 4. Chips and hardware
Teach: what a GPU is and why AI needs it. Chips for training compared with chips for inference. The custom chips of the large clouds. Memory and the network inside a cluster. The ladder from one GPU to a server, a rack, a hall and a campus. The chip supply chain (designer, foundry, memory maker, equipment maker), with companies. The yearly cycle of new chips and its effect on the value of old chips. Purchase prices from the reference data.
Pictures: (a) the scale ladder, with the power for each step, (b) the chip supply chain as a map.

Module 5. Data centres and energy
Teach: the parts of an AI data centre. kW, MW and GW. Cooling and PUE. The cost to build for each MW, with chips and without chips. The price of electricity and its share of the total cost. The time to build a site. The three limits on growth: power, chips and capital. The largest sites in operation.
Pictures: (a) the cost of 1 GW, split into its parts, (b) the three limits on growth.

Module 6. Compute markets and the economics of one GPU
Teach: the owners of the GPUs (large clouds, GPU clouds and model companies). Rental prices and the types of contract (on demand, reserved and spot). Utilisation. Depreciation and the dispute about useful life. Payback. The capital spending of the large companies. The contract backlog. The methods that companies use to finance the build: cash flow, debt, leases, and deals between suppliers and customers.
Picture: the history of the H100 rental price. Show the two indices apart, because they use different methods.
Interactive: a GPU-hour calculator. Inputs: purchase price for each GPU with its share of the server and network, useful life, utilisation, power for each GPU, PUE, electricity price, other cost for each hour, and rental price. Outputs: the cost for each GPU-hour (split into depreciation, power and other), the margin at the rental price, and the payback period.

Module 7. Model companies and AI software businesses
Teach: the model company: revenue run-rate, gross margin, training cost, inference cost and the need for capital. The application company: seat prices compared with usage prices, cost for each task, and gross margin after model cost. Why this gross margin is lower than the gross margin of traditional software. The use of AI by companies, from the reference data. The sources of an advantage that lasts: private data, distribution, depth in a workflow, the cost to change supplier and own models. Three tests that separate a strong product from a thin layer on a model.
Picture: the cost structure of a model company beside the cost structure of an application company.
Interactive: a gross margin calculator for an AI application. Inputs: the seat price for each month, the tasks for each user for each month, the input tokens and output tokens for each task, and the model. Outputs: the model cost for each user and the gross margin.

Module 8. How engineers build AI applications, and what to use when
Teach, part A, the parts: front end, back end, database, file storage, sign-in, the model API and the network edge. The parts that are special to AI: retrieval (the application finds relevant documents and puts them in the context), the vector database, tools (the model asks the application to run a function), the agent loop, memory, evaluation (tests for the output of the model), guardrails and monitoring. The method of work of a team: the code repository, the pull request, automated tests, environments and release. The work of AI coding agents in that method.
Teach, part B, the platforms: four platforms as examples of four types. AWS is a general cloud, which supplies almost each building block and gives the most control for the most work. Supabase is a back end as a service, which supplies a Postgres database with sign-in, file storage and functions. Vercel is a front-end cloud, which hosts the web application and publishes it from the code repository. Cloudflare is an edge network, which supplies a content delivery network (CDN), security, and functions and storage near the user. Where the model sits: a model API from a model company, or the same model through a cloud service such as Amazon Bedrock. How teams combine the four types in one product. What to use when, by stage (prototype, product, scale) and by need (speed, control, compliance, cost). How an application scales: a larger server compared with more servers. Serverless functions compared with servers that run all the time. Why the database is the difficult part. Caches, queues, rate limits and regions. The three parts that fail first when use increases: database connections, rate limits of the model API, and cost. The shape of the cost: a fixed plan and a usage charge, egress fees, and the cost to change supplier.
Pictures: (a) the path of one request from the browser of the user through the edge, the front end, the back end, retrieval, the database and the model API, with an example platform on each part. (b) A matrix of needs against the four types of platform. (c) The three stages of growth, with the changes at each stage.
Interactive: a stack selector. The reader selects the stage, the skill of the team and the most important need. The page shows a suggested combination of platform types, the reason for each part, the fixed plan cost for each month from the reference data, and the first limit that the team will meet. Label the result as a start point for a discussion with the developers.
Describe each platform by its main purpose only, because the features of platforms change each month. Use the reference data for each plan price and each limit.

Module 9. The toolkit of the technical investor, and the path to expert
Teach: twelve questions for the technical review of an AI company. For each question, give the sign of a strong answer and the sign of a weak answer. The questions that an operator asks before a purchase (which tasks, which model size, seat or usage, how to budget, how to measure value, data safety). The main risks, written as questions and not as forecasts. Then the path to expert: four levels of skill (aware, fluent, practitioner, expert), with the things that a person at each level can do. A plan of 12 weeks with one practical task for each week, for a reader who has 3 to 4 hours each week. Each task uses the course: for example, calculate the token cost of a real task, read the accounts of one AI company, or build a small application with an AI coding tool on two of the platforms. State clearly that one course gives the map, and that practice makes the expert.
Table: a minimum of 30 KPIs. Columns: name, plain definition, unit, formula where one exists, typical value with its date, the meaning of a high or low value, and the user of the KPI (investor, operator or engineer). The table includes five KPIs for applications (response time, uptime, error rate, requests for each second, and cost for each active user). The reader can filter the table by user.
Picture: the 12 weeks as a timeline in four phases.

After the modules: a quiz of 18 questions with feedback on each answer, a glossary of 90 terms or more that the reader can search, and a list of sources with dates.
</course_plan>

<language_rules>
Write all course text to the writing rules of ASD-STE100 Simplified Technical English. This standard removes ambiguity, so a reader with no technical training understands each sentence at the first reading. Where the house rules below are different from STE, the house rules apply.

1. Give each sentence one idea. Use a maximum of 20 words in an instruction and a maximum of 25 words in a description.
2. Write most sentences with 10 to 20 words, because a long row of very short sentences is hard to read. Headings, labels, captions and list items can be shorter.
3. Use the active voice and name the actor. Write "the owner pays the cost", not "the cost is paid".
4. Use simple verb forms: present, past and future. Avoid verbs that end in -ing and avoid forms such as "has grown".
5. Use one word for one thing. After you choose a term, do not change to a synonym.
6. Define each technical term in one sentence when you first use it, and add it to the glossary. Write an abbreviation in full the first time, with the short form in brackets. Product names, technical names and code keep their original form.
7. Put a maximum of three nouns together. Write "the cost of power in a data centre", not "data centre power cost model".
8. Give each paragraph one topic and a maximum of six sentences. Use a vertical list for three or more parallel items.
9. Do not use idioms or figures of speech. You can use one comparison for a difficult idea, and you must introduce it with the word "compare".
10. House rules: British spelling, no em dashes, no semicolons, no exclamation marks and no emoji. Write "per cent" in sentences and "%" in tables. Write dates as "26 November 2026". Use digits for each quantity that has a unit.

<examples>
<example>
Before: Tokenisation is the process by which input text is segmented into sub-word units prior to being processed by the model.
After: A language model does not read letters or full words. It reads tokens, and a token is a small piece of text. In English, 1 token has about 4 characters, which is about three quarters of a word.
</example>
<example>
Before: Given the rapid depreciation of GPUs, operators are heavily incentivised to maximise utilisation rates.
After: A GPU loses value each year, and the owner pays this cost for each hour of its life. The cost does not stop when the GPU has no work. Thus the owner wants paid work on the GPU for as many hours as possible.
</example>
<example>
Before: Request cost can be derived by multiplying token volumes by their respective unit prices and summing.
After: Calculate the cost of one request in three steps:
1. Multiply the input tokens by the input price, then divide by 1,000,000.
2. Multiply the output tokens by the output price, then divide by 1,000,000.
3. Add the two results.
</example>
<example>
Before: It's worth noting that estimates of training costs vary wildly and should be taken with a pinch of salt.
After: The sources do not agree on the cost to train this model. The lowest estimate is [low value] and the highest estimate is [high value]. Use the range in your work, and state that the number is an estimate.
</example>
<example>
Before: The context window is basically the model's short-term memory, a scratchpad where everything lives until it overflows.
After: The context window is the text that the model can read at one time. You can compare the context window to a desk with a fixed size. When the desk is full, you must remove old papers before you add new papers.
</example>
</examples>
</language_rules>

<visual_rules>
The reader learns faster from pictures than from text, so each module needs a minimum of one diagram that shows a real mechanism. A picture that only decorates the page does not count. Draw each diagram and chart as inline SVG, and label it in the same simple English as the text. Give each picture a caption that states what the reader must see in it. Where the builder view needs code, show a short example of 15 lines or fewer in a code block, and explain each line in simple English beside it. The reader must learn to read code, and does not need to write it. Make the calculators, the table filter, the quiz and the glossary search work without an external library. Show a filled example in each calculator when the page opens, so that the first view teaches something. Add a contents list that stays in view and shows the reader's position in the course. Use motion only where it explains a sequence, and obey the reader's reduced-motion setting. The page must work on a phone, in a light theme and in a dark theme, and each control must work from the keyboard.
</visual_rules>

<design_system>
Use the Ārahi 2027 brand. The brand is calm, precise and editorial, and its confidence comes from restraint and typography.
- Typeface: Jost for all text, loaded from Google Fonts, with Roboto and Arial as fallbacks. Large titles use regular weight. The strapline below a title carries the weight: bold and emerald.
- Light theme colours: emerald #065146 (rules, straplines, primary buttons), teal #338080 (links, table header bands), forest #042E2E (dark panels), charcoal #4E4E4E (body text), mid-grey #616161 (captions), stone #CED0CB (hairlines), white ground.
- Tint fills, for panels only: mint #E8F5F0, light teal #D0ECEC, light sage #F1F4F0, light amber #FFFBEB, light pink #FEF2F2.
- Chart series, in order: emerald, sage #B8C7B2, teal, terracotta #BA6547, indigo #595879, dusty rose #D39080. Lead with one colour and let one accent point at the main fact.
- Dark theme: forest ground #042E2E, raised surface #0A3B37, white text, and lighter versions of the accents with sufficient contrast.
- Shape: 1px stone hairlines carry the structure. The corner radius is 2px. Use no shadows on cards, no gradients and no coloured bars on the side of cards. Put a 1.5px emerald rule below each section title.
- Layout: generous white space on a 4px grid, a reading width of about 66 characters, and a wide main column beside a narrow rail. Where content has the shape of a chart, a timeline, a tree or a matrix, draw it in that shape. Avoid rows of equal cards.
- Headings: sentence case. A heading names the subject, and the strapline below it states the finding in one sentence.
</design_system>

<accuracy_rules>
1. For each price, cost and company number, use only the figures in the reference data. The reader will repeat these numbers, and a number from memory can be out of date.
2. Build each explanation from the reference data: the fact lines, the builder notes and the investor notes. Research agents collected this material for each point of the course plan. Use your general knowledge only to join these facts into clear teaching. Do not use it to add a figure, a product fact or a claim about a company.
3. Show the date and the source name near each figure. At the end of the page, list each source that the course uses, with its link. You do not need to list a source that the course does not use.
4. Where the reference data give a range, show the range. Where the reference data mark a fact as uncertain, tell the reader that it is uncertain. Where the data give two sides of a dispute, give both sides.
5. The reference data name some items as not in the data. If the course needs one of these items, tell the reader that the figure is not available, or use an example value in a calculator and label it "example value". Name each such item in your report.
6. Make each explanation simple, but do not make it false. Where a simple explanation hides an important detail, add a short note that starts with "Simplified:".
7. Stay neutral about companies and platforms. Do not give investment advice. For each platform, state a strength and a cost of that strength. Write each risk as a question that the reader can ask.
8. State in the footer that the text follows the writing rules of ASD-STE100, and that no formal check against the STE dictionary was done. State also that the figures come from web research of 26 November 2026, and that the reader must check a figure at its source before use in a board paper.
</accuracy_rules>

<output_format>
Give the course as one HTML file that contains its styles and scripts. Load only the Jost typeface from Google Fonts. After the file, write a report of 150 words or fewer in the same simple English. The report states what you built, each figure that was not in the reference data, and each rule that you could not obey.
</output_format>

<self_check>
Before you finish, check your work against this list and correct each failure:
1. Each of the twelve success criteria is taught in a module and tested in the quiz.
2. Each price, cost and company number agrees with the reference data and shows its date. Each explanation rests on a fact or a note in the reference data. Each module has an investor view and a builder view.
3. The token cost calculator gives $0.009 for 2,000 input tokens and 500 output tokens at prices of $2 and $10 for each million tokens. In agent mode it gives $0.13 for 10 steps, a start context of 1,000 tokens, 1,000 tokens added at each step and 200 output tokens for each step, at the same prices and with no cache.
4. The GPU-hour calculator gives the same result as a calculation that you do by hand from its default values. The gross margin calculator gives a model cost of $8.00 and a gross margin of 73 per cent for a seat price of $30, 400 tasks, and 5,000 input tokens and 1,000 output tokens for each task, at prices of $2 and $10. The stack selector gives a result for each combination of its inputs.
5. Each technical term has a definition at its first use and an entry in the glossary.
6. No description has more than 25 words in one sentence, and no instruction has more than 20 words.
7. The text has no em dashes, no semicolons, no exclamation marks and no emoji.
8. The page is easy to read in the light theme, in the dark theme and on a narrow phone screen.
</self_check>
