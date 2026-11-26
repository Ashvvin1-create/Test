<role>
You are a senior technology teacher who writes for business readers. You explain artificial intelligence (AI) to readers who have no technical training, and you write in ASD-STE100 Simplified Technical English.
</role>

<settings>
These settings come from the reader's answers to four questions. Change them to use this prompt for a different reader or a different subject.
- Subject: how AI works, the infrastructure behind AI, and the economics of AI
- Reader: a director at a private equity advisory firm, with no technical training and full fluency in company accounts
- Purpose: all views. The basics of how AI works (tokens, input and output), the investor view and the operator view
- Depth: full course, six modules, 60 to 90 minutes to read
- Format: one interactive web page
- Date of the data: 26 November 2026
- Currency: US dollars, because the AI market quotes its prices in US dollars
If a setting is empty, or if two settings conflict, ask one short question before you start. If the settings are complete, start the work immediately.
</settings>

<reference_data>
<data_notes>
A web search on 26 November 2026 supplied these figures. Each figure has a source key such as [S1], and the source list is at the end of this block. Three labels show how firm a figure is. "Reported" means that a company published the figure. "Estimate" means that an analyst or a news report supplied it. "Uncertain" means that the sources are weak or do not agree. All prices are in US dollars. MTok means one million tokens.
</data_notes>

<group name="A. Token prices for each MTok: input, cached input, output">
- Anthropic Claude Fable 5.2: $8.00, $0.20, $40.00. Context window 1,000,000 tokens. Reported, price list of 3 November 2026 [S1]
- Anthropic Claude Opus 5.5: $4.00, $0.20, $20.00. Context window 1,000,000 tokens. Reported [S1]
- Anthropic Claude Sonnet 5.5: $2.00, $0.10, $10.00. Context window 1,000,000 tokens. Reported [S1]
- Anthropic Claude Haiku 5.5: $0.10 input and $0.50 output, for prompts of 100,000 tokens or fewer. Cached input price not in the data. Reported [S1]
- Anthropic discounts: a batch request costs 50 per cent of the standard price. The first write to the cache costs about 1.25 times the input price. Reported [S1]
- OpenAI GPT-6.2 Astra (released 17 November 2026): $8.00, $0.40, $40.00. Reported, read through secondary pages [S2]
- OpenAI GPT-6.2 Sol: $2.00, $0.10, $10.00. Reported, read through secondary pages [S2]
- OpenAI GPT-6 Luna: $0.10, $0.01, $0.50. Reported, read through secondary pages [S2]
- Google Gemini 4 Argon: $2.00, $0.10, $10.00 until 30 November 2026. Then $4.00, $0.20, $20.00 from 1 December 2026. Reported, read through secondary pages [S3]
- Google Gemini 3.1 Flash-Lite: $0.25 input and $1.50 output. Reported, read through secondary pages [S3]
- Open-weight model gpt-oss-120b on the host Together AI: $0.15 input and $0.60 output. Reported [S4]
- Rule of thumb for English text: 1 token is about 4 characters, or about 0.75 words. General knowledge, not a measured figure.
</group>

<group name="B. Trend in token prices">
- The price for a fixed level of quality falls about 13 times each year, which is 47 per cent each quarter. Estimate, 22 September 2026 [S5]
- A second study gives 5 to 10 times each year. Estimate, November 2025 [S6]
- Use "5 to 13 times each year" as the range, because the sources do not agree.
- Older example: the price for the quality level of GPT-3.5 fell from $20.00 to $0.07 for each MTok between November 2022 and October 2024. Estimate, old source [S7]
</group>

<group name="C. Model speed and size">
- Output speed: 45 tokens each second (GPT-6.2 Astra) and 82 tokens each second (Gemini 4 Argon). Average of all measured models: 81. Estimate, November 2026 [S8]
- Time to the first token of the answer: medians of 3.6 to 13 seconds, by price tier. Flagship models at high reasoning effort: 54 to 173 seconds. Estimate, November 2026 [S8]
- Context window: about 1,000,000 tokens for the flagship models, and 128,000 tokens for gpt-oss-120b. Reported [S1] [S8]
</group>

<group name="D. Seat prices for each user for each month">
- ChatGPT Business: $25, or $20 with annual billing. Reported [S9]
- Claude Team: $25, or $20 with annual billing. Premium seat $125. Reported [S10]
- Microsoft 365 Copilot: $30 with annual billing. Reported [S11]
- GitHub Copilot: Business $19, Enterprise $39. Reported [S12]
- Claude Code, a coding agent with usage pricing: about $13 for each developer for each active day, and $150 to $250 for each month. Reported [S13]
</group>

<group name="E. Finances of model companies and of the main chip company">
- Anthropic, quarter 3 of 2026: revenue $17.0 billion and operating loss $567 million. Reported in an IPO filing, read through press [S14]
- Anthropic, nine months to 30 September 2026: revenue $33.2 billion. Operating loss about $1.26 billion. Net loss about $104 billion, of which about $94 billion is a non-cash change in the fair value of financial instruments. Reported in an IPO filing, read through press [S14]
- Anthropic revenue run-rate: about $81 billion at 31 October 2026. Uncertain, one press source [S15]
- Anthropic compute cost: $18.8 billion in nine months, with 26 per cent for inference and 74 per cent for training and research. Uncertain, from an investor chart [S16]
- Anthropic purchase commitments: $895.4 billion. Reported in an IPO filing, read through press [S14]
- OpenAI revenue run-rate: about $50 billion at the end of September 2026. A second source gives about $70 billion with a wider definition. Uncertain, from leaked documents [S17]
- OpenAI, quarter 3 of 2026: revenue about $10 billion and adjusted operating loss $10.9 billion. Estimate [S18]
- OpenAI gross margin: 39 per cent in quarter 1 of 2026. Estimate [S19]
- OpenAI compute spend: $50 billion in 2026. Reported in court testimony, May 2026 [S20]
- Nvidia, quarter to 25 October 2026: revenue $115.8 billion, data centre revenue $107.6 billion, gross margin 74.8 per cent. Reported, 17 November 2026 [S21]
</group>

<group name="F. Cost to train a model">
- The final training run of one frontier model (Grok 4): about $490 million, 246 million GPU-hours on H100 chips and 310 GWh of energy. Estimate, old source of September 2025 [S22]
- Trend: the cost of the largest training run grows about 2.4 times each year. The total compute to develop a model is 1.2 to 4 times the compute of the final run. Estimate [S22]
- No estimate for the newest flagship models is in the data.
</group>

<group name="G. GPU rental prices for each GPU-hour, October to November 2026">
- Nvidia H100 on demand at the large clouds: $6.88 (AWS), $11.06 (Google Cloud), $12.29 (Azure). Estimate [S23]
- Nvidia H100 on demand at GPU clouds: $3.99 (Lambda), $4.50 (Nebius), $6.16 (CoreWeave). Estimate, 18 November 2026 [S24]
- Nvidia H100 at marketplaces: $1.93 (Vast.ai median) to $2.89 (RunPod). Estimate [S25] [S65]
- Nvidia H200: $7.91 to $10.85 at the large clouds, and $3.85 to $5.40 at GPU clouds. Uncertain [S26]
- Nvidia GB200 (Blackwell generation) at GPU clouds: median $8.00, range $6.50 to $10.50. Estimate, 17 October 2026 [S27]
- Nvidia Vera Rubin (the newest generation): in delivery, but no public on-demand price. Uncertain [S28]
- History of the H100 on-demand price: $6.62 in the second half of 2023, and $3.91 in quarter 4 of 2024. Estimate [S29]
- History of a second H100 index for GPU clouds: $2.07 in quarter 3 of 2025, and $3.06 on 10 November 2026. Estimate [S30]
- Direction: the H100 price fell by about 70 per cent to late 2025, and then increased by about 50 per cent. The two indices use different methods, so do not join them into one line.
</group>

<group name="H. Hardware purchase prices, 2026">
- One Nvidia H100: $25,000 to $31,000. One Nvidia B200: $30,000 to $40,000 list price, $45,000 to $55,000 street price. Estimate, Nvidia does not publish prices [S31]
- One server with 8 GPUs: $250,000 to $320,000 with H100 chips, and $390,000 to $550,000 with B200 chips. Estimate [S32]
- One rack, GB200 NVL72, with 72 GPUs: $2.8 million to $3.4 million, and about 120 kW of power. Estimate [S33] [S66]
- One rack, Vera Rubin NVL72: $7.0 million to $8.8 million, and 180 to 220 kW of power. Estimate [S33]
</group>

<group name="I. Data centre cost and power">
- Building, power and cooling, without chips: $11.3 million for each MW as a global average. Range in the United States and Canada: $8.9 million to $23.3 million for each MW. Estimate, 2026 [S34] [S62]
- All-in cost with chips: $38 million to $60 million for each MW. Thus 1 GW costs $38 billion to $60 billion. Estimate, the sources do not agree [S35] [S63]
- PUE: 1.52 industry average, 1.36 when weighted by capacity. Google reports 1.09. Estimate and reported, 2026 [S36] [S59]
- Electricity price for industry for each kWh: United States $0.096. United Kingdom about $0.33. European Union about $0.21. Reported, 2026, with approximate exchange rates [S37] [S60] [S61]
- Share of power in the total annual cost of an AI data centre: about 7 per cent. Estimate [S35]
- Largest sites in operation, November 2026: about 1.0 GW. One site of 946 MW holds about 550,000 GPUs. Estimate [S38]
</group>

<group name="J. Depreciation and utilisation">
- Useful life that companies use for servers: Alphabet 6 years, Meta 5.5 years, Amazon 5 years, CoreWeave 6 years, Lambda 5 years, Nebius 4 years. Reported [S39] [S56] [S57]
- The dispute: critics say that the real life of an AI chip is 2 to 3 years. Estimate, April 2026 [S40]
- The reply: Nvidia says that customers rented old H100-generation chips again at up to twice the original price. Reported, 17 November 2026 [S41]
- Utilisation: company-owned GPU clusters average about 5 per cent. A GPU cloud needs more than 80 per cent to earn its target return. The real rates of GPU clouds are not public. Estimate [S42] [S58]
</group>

<group name="K. Capital spending, 2025 actual and 2026 guide">
- Alphabet: $91.4 billion, then $195 billion to $205 billion. Reported, 28 October 2026 [S43] [S51]
- Amazon: about $128 billion to $131 billion, then about $220 billion. Reported, 29 October 2026 [S43] [S52]
- Meta: $72.2 billion, then $135 billion to $145 billion. Reported, 21 October 2026 [S43] [S53]
- Microsoft: $64.6 billion in the year to June 2025, then $116 billion in the year to June 2026. Reported [S54]
- Oracle: $21.2 billion in the year to May 2025, then $55.7 billion in the year to May 2026. Reported [S55]
- Stargate, the build programme of OpenAI: $500 billion and 10 GW at the announcement in January 2025. 0.3 GW in operation in April 2026. Estimate [S44]
</group>

<group name="L. KPIs of GPU cloud companies">
- Revenue for each MW for each year: $20 million to $25 million on contracts of 4 to 5 years (CoreWeave). $40 million on short contracts (IREN). Estimate, November 2026 [S45] [S64]
- Payback period on the equipment: about 2 years. Uncertain [S64]
- Contract backlog: CoreWeave $132.5 billion (November 2026). Oracle $664 billion (September 2026). Reported [S45] [S46]
- CoreWeave in 2026: capital spending $37 billion to $39 billion, revenue $13.0 billion to $13.3 billion, 1.7 GW active and 4.6 GW contracted. Reported [S45]
</group>

<group name="M. Use of AI by companies">
- 89 per cent of organisations use AI in one function or more. 37 per cent see an effect on profit. Survey of May to June 2026 [S47]
- 19.8 per cent of all firms in the United States use AI. 37 per cent of firms with 250 staff or more use AI. Reported, 3 May 2026 [S48]
</group>

<group name="N. Energy for one text prompt">
- Google: median 0.24 Wh and 0.26 mL of water. Reported, old source of August 2025 [S49]
- OpenAI: average 0.34 Wh. Reported with no method, old source of June 2025 [S50]
</group>

<sources>
[S1] Anthropic, Claude pricing, 3 November 2026. https://platform.claude.com/docs/en/about-claude/pricing
[S2] OpenAI, API pricing, November 2026. https://developers.openai.com/api/docs/pricing
[S3] Google, Gemini API pricing, November 2026. https://ai.google.dev/gemini-api/docs/pricing
[S4] Together AI, gpt-oss model page, 2026. https://docs.together.ai/docs/gpt-oss
[S5] Epoch AI, The plunging price of thought, 22 September 2026. https://epoch.ai/publications/the-plunging-price-of-thought
[S6] Gundlach and others, The price of progress, November 2025. https://arxiv.org/abs/2511.23455
[S7] Stanford HAI, AI Index Report 2025. https://hai.stanford.edu/ai-index/2025-ai-index-report
[S8] Artificial Analysis, model pages, November 2026. https://artificialanalysis.ai/models/gpt-6-2-astra
[S9] OpenAI, ChatGPT Business overview, 2026. https://help.openai.com/en/articles/8792828-chatgpt-business-overview
[S10] Anthropic, What is the Team plan, 2026. https://support.claude.com/en/articles/9266767-what-is-the-team-plan
[S11] Microsoft, Microsoft 365 Copilot pricing, 2026. https://www.microsoft.com/en-us/microsoft-365-copilot/pricing/enterprise
[S12] GitHub, Copilot plans, 2026. https://docs.github.com/en/enterprise-cloud@latest/copilot/get-started/plans
[S13] Anthropic, Claude Code costs, 2026. https://code.claude.com/docs/en/costs
[S14] CNBC, Anthropic S-1 quarter financials, 2 November 2026. https://www.cnbc.com/2026/11/02/anthropic-ant-s-1-quarter-financials.html
[S15] 24/7 Wall St, Anthropic revenue run-rate, 11 November 2026. https://247wallst.com/investing/2026/11/11/anthropic-says-its-revenue-run-rate-jumped-to-an-81-billion-run-rate/
[S16] OfficeChai, Anthropic compute split, 2026. https://officechai.com/ai/74-of-anthropics-compute-has-gone-towards-training-in-2026-only-26-to-inference-brad-gerstner/
[S17] Vantage Markets, OpenAI run-rate debate (FT and Axios figures), October 2026. https://www.vantagemarkets.com/market-analysis/ai-bubble-debate-openai-run-rate/
[S18] Forbes, OpenAI quarter 3 revenue, 11 November 2026. https://www.forbes.com/sites/jonmarkman/2026/11/11/openai-revenue-hits-10-billion-in-q3-as-loss-per-dollar-falls-to-109/
[S19] The Next Web, OpenAI quarter 1 burn and margin, June 2026. https://thenextweb.com/news/openai-burned-3-7-billion-q1-2026
[S20] Quartz, OpenAI compute spending testimony, 5 May 2026. https://qz.com/openai-computing-spending-50-billion-brockman-trial-050526
[S21] Nvidia, results for the third quarter of fiscal 2027, 17 November 2026. https://investor.nvidia.com/news/press-release-details/2026/NVIDIA-Announces-Financial-Results-for-Third-Quarter-Fiscal-2027/
[S22] Epoch AI, Grok 4 training resources, 12 September 2025. https://epoch.ai/data-insights/grok-4-training-resources
[S23] Spheron, H100 price per hour 2026, October 2026. https://www.spheron.network/blog/h100-price-per-hour-2026/
[S24] FourWeekMBA, GPU rents and H100 list prices, 18 November 2026. https://fourweekmba.com/ai-nvidia-says-gpu-rents-rose-8-gpu-h100s-list-at-4-50-6-16/
[S25] RunPod, GPU cloud pricing, November 2026. https://www.runpod.io/gpu-cloud/pricing
[S26] Thunder Compute, Nvidia H200 pricing, 4 November 2026. https://www.thundercompute.com/blog/nvidia-h200-pricing
[S27] American Compute, GB200 cloud prices, 17 October 2026. https://www.amcompute.com/gpu-cloud-prices/gb200
[S28] GetDeploying, Nvidia Vera Rubin, 9 November 2026. https://getdeploying.com/gpus/nvidia-vera-rubin
[S29] SemiAnalysis, GPU price index. https://gpu-index.semianalysis.com/
[S30] Silicon Data, GPU rent index, 10 November 2026. https://www.silicondata.com/blog/hopper-ampere-gpu-rents-coreweave-repricing
[S31] GPUsmith, Nvidia data centre GPU pricing guide, 2026. https://gpusmith.com/articles/en/nvidia-data-center-gpu-pricing-guide
[S32] IntuitionLabs, Nvidia AI GPU pricing guide, 2026. https://intuitionlabs.ai/articles/nvidia-ai-gpu-pricing-guide
[S33] Tom's Hardware, price of Vera Rubin NVL72 racks, 2026. https://www.tomshardware.com/tech-industry/artificial-intelligence/price-of-nvidias-vera-rubin-nvl72-racks-skyrockets-to-as-much-as-usd8-8-million-apiece-but-server-makers-margins-will-be-tight-nvidia-is-moving-closer-to-shipping-entire-full-scale-systems
[S34] JLL, Data center outlook 2026. https://www.jll.com/en-us/insights/market-outlook/data-center-outlook.html
[S35] Epoch AI, AI data centre cost breakdown, May 2026. https://epoch.ai/data-insights/ai-datacenter-cost-breakdown
[S36] Uptime Institute, PUE of larger data centres, July 2026. https://intelligence.uptimeinstitute.com/resource/growing-pue-advantage-larger-data-centers
[S37] US Energy Information Administration, Electric power monthly, August 2026. https://www.eia.gov/electricity/monthly/epm_table_grapher.php?t=epmt_5_3
[S38] Epoch AI, Largest AI data centres by power capacity, November 2026. https://epoch.ai/graphs/largest-ai-data-centers-by-power-capacity
[S39] Hudson Labs, Server useful life at Amazon and Meta, 2025. https://www.hudson-labs.com/research/server-useful-life-amzn-meta
[S40] Fortune, Data centre hardware life, 15 April 2026. https://fortune.com/2026/04/15/data-centers-hyperscalers-spending-billions-on-hardware-thats-worthless-in-3-years/
[S41] TIKR, Old Hopper GPUs re-contracted, 17 November 2026. https://www.tikr.com/blog/nvidias-interim-ceo-old-hopper-gpus-recontracted-at-up-to-twice-their-original-price-good-news-for-coreweave
[S42] McKinsey, The evolution of neoclouds. https://www.mckinsey.com/capabilities/tech-and-ai/our-insights/the-evolution-of-neoclouds-and-their-next-moves
[S43] Fortune, Data centre capital spending in 2025, 6 February 2026. https://fortune.com/2026/02/06/what-is-a-data-center-capex-spending-630-billion-dollars-amazon-microsoft-google-meta/
[S44] Epoch AI, OpenAI Stargate: where the US sites stand, April 2026. https://epoch.ai/publications/openai-stargate-where-the-us-sites-stand
[S45] The Motley Fool, CoreWeave quarter 3 2026 earnings call, 10 November 2026. https://www.fool.com/earnings/call-transcripts/2026/11/10/coreweave-crwv-q3-2026-earnings-call-transcript/
[S46] Oracle, results for quarter 1 of fiscal 2027, 10 September 2026. https://www.oracle.com/news/announcement/q1fy27-earnings-release-2026-09-10/
[S47] McKinsey, The state of AI, 2026. https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai
[S48] US Census Bureau, AI use by businesses, May 2026. https://www.census.gov/library/stories/2026/05/ai-use-businesses.html
[S49] Google Cloud, Measuring the environmental impact of AI inference, 21 August 2025. https://cloud.google.com/blog/products/infrastructure/measuring-the-environmental-impact-of-ai-inference
[S50] Simon Willison, note on the OpenAI energy figure, 10 June 2025. https://simonwillison.net/2025/Jun/10/sam-altman/
[S51] TechPowerUp, Alphabet quarter 3 2026 results, 28 October 2026. https://www.techpowerup.com/354262/alphabet-announces-q3-2026-results-revenue-at-usd-127-6-billion
[S52] Amazon, quarter 3 2026 earnings report, 29 October 2026. https://aboutamazon.com/news/company-news/amazon-earnings-q3-2026-report
[S53] Meta, third quarter 2026 results, 21 October 2026. https://investor.atmeta.com/investor-news/press-release-details/2026/Meta-Reports-Third-Quarter-2026-Results/
[S54] The Register, Microsoft capital spending, July 2026. https://www.theregister.com/a/5280798
[S55] The Next Web, Oracle capital spending in fiscal 2026, 10 June 2026. https://thenextweb.com/news/oracle-q4-fy2026-capex-55-billion-ai-data-center-openai
[S56] SiliconANGLE, Resetting GPU depreciation, 22 November 2025. https://siliconangle.com/2025/11/22/resetting-gpu-depreciation-ai-factories-bend-dont-break-useful-life-assumptions/
[S57] Webull, Server useful life at Microsoft and Alphabet, 2026. https://www.webull.com/news/15535982583590912
[S58] Dataconomy, Average GPU utilisation report, 23 April 2026. https://dataconomy.com/2026/04/23/tech-industry-averages-just-5-gpu-utilization-report-finds/
[S59] Google, Environmental report 2026, 30 June 2026. https://sustainability.google/google-2026-environmental-report/
[S60] UK Government, Quarterly energy prices, September 2026. https://assets.publishing.service.gov.uk/media/6aba2810fe72ed1e2b02f0e7/Quarterly_Energy_Prices_September_2026.pdf
[S61] The Brussels Times, EU electricity prices for businesses, 2026. https://www.brusselstimes.com/2391539/eu-electricity-prices-for-businesses-drop-but-nordic-nations-see-sharp-rises
[S62] IREI, Cushman and Wakefield data centre development cost guide 2026. https://irei.com/news/cushman-wakefield-releases-2026-data-center-development-cost-guide-citing-21-rise-in-per-mw-construction-costs/
[S63] Brookings, paper by Van Nieuwerburgh on data centre finance, September 2026. https://www.brookings.edu/wp-content/uploads/2026/09/4c_Van-Nieuwerburgh.pdf
[S64] FourWeekMBA, Revenue for each MW on short and long GPU contracts (IREN), 5 November 2026. https://fourweekmba.com/ai-short-gpu-deals-pay-40m-per-mw-1-8x-five-year-contracts/
[S65] Markaicode, Vast.ai pricing, 16 November 2026. https://markaicode.com/pricing/vast-ai-pricing/
[S66] The Register, Nvidia Blackwell rack power, 27 March 2024. https://www.theregister.com/2024/03/27/nvidia_blackwell_efficiency/
</sources>
</reference_data>

<context>
The reader is intelligent and busy. The reader reads a profit and loss account with ease, but does not know what a token or a GPU is. The reader will use this knowledge in two roles. As an investor, the reader judges AI companies, data centres and deals. As an operator, the reader helps companies to buy, budget and use AI. The reader will repeat your numbers in meetings with boards and investors, so a wrong number damages the reader's reputation. The reader may also share the page with colleagues who have the same background.
</context>

<task>
Build a course with the name "AI explained" as one interactive web page. The course teaches the subject in the settings from zero. Teach each idea in the same order: a plain statement, a picture, a worked example with real numbers, and then a short check. Go beyond a basic page. Include each diagram, calculator, table, quiz and glossary in the course plan, and make each one work fully.
</task>

<success_criteria>
The course succeeds if the reader can do these seven things after one reading, without help:
1. Explain in two sentences how a language model makes an answer.
2. Define the 12 core terms: model, parameter, training, inference, token, context window, prompt, GPU, data centre, hyperscaler, utilisation and gross margin.
3. Calculate the cost of one AI request from its token counts and a price list.
4. Name the seven layers of the AI supply chain, and name one company in each layer.
5. Calculate the cost of one GPU-hour from the purchase price, the useful life, the utilisation and the power cost.
6. Read 10 core KPIs and say what a high value and a low value mean.
7. Ask five useful questions about an AI company or about an AI purchase.
The quiz must test each of the seven criteria with at least one question.
</success_criteria>

<course_plan>
Write six modules in this order. Start each module with one sentence that states what the reader will learn. End each module with three "You can now" statements.

Module 1. What AI is
Teach: AI, machine learning, deep learning, generative AI, large language model (LLM) and agent. A model is a very large mathematical function, and its numbers have the name parameters. Training sets the parameters. Inference uses the parameters to do work.
Picture: a nested map that shows how the six terms fit inside each other.

Module 2. How a language model works
Teach: tokens. Text in and text out. The model predicts the next token, one token at a time, from probabilities. Why the model can state false things (hallucination). The context window. The prompt and the system prompt. Training data and the knowledge cut-off date. Fine-tuning. Retrieval, where the model reads documents that you supply. Tools and agents. Reasoning tokens.
Pictures: (a) the path from prompt to answer in five steps, (b) the context window as a box with a fixed size, with its contents.
Interactive: a token demonstration. The reader types text, and the page shows an approximate split into tokens and the token count. Label the result as an estimate.

Module 3. Token economics: how you pay for AI
Teach: the price for each million tokens. Why input tokens and output tokens have different prices. Cached input. The batch discount. Reasoning tokens that the supplier bills as output. Why each turn of a long conversation costs more than the turn before it. Subscription seats compared with usage prices. How fast prices fall. Why total spend can increase while unit prices fall.
Picture: a chart of the fall in token prices, from the reference data.
Interactive: a token cost calculator. Inputs: the model (from the price list in the reference data), input tokens, output tokens, the share of input that is cached, and requests for each day. Outputs: the cost for each request, each day and each month.
Worked example: one question of 2,000 tokens with an answer of 500 tokens, on two different models.

Module 4. Infrastructure: the AI factory
Teach: the seven layers (energy, data centre, chips, cloud, model, application, user), with example companies and the direction of the money between layers. What a GPU is and why AI needs it. The ladder from one GPU to a server, a rack, a hall and a campus. kW, MW and GW. Cooling and PUE. Training clusters compared with inference clusters. The chip supply chain (designer, foundry, memory, equipment). The three limits on growth: power, chips and capital.
Pictures: (a) the seven layers as a stack, with the flow of money, (b) the scale ladder, with the power for each step.

Module 5. Economics and KPIs
Teach four businesses, each with one worked example: (1) the GPU owner: cost for each GPU-hour, rental price, utilisation, depreciation and payback. (2) The data centre: capital cost for each MW, power cost and PUE. (3) The model company: revenue run-rate, gross margin, training cost and inference cost. (4) The application company or AI buyer: cost for each task, seat price compared with usage price, and gross margin after model costs.
Interactive: a GPU-hour calculator. Inputs: purchase price for each GPU with its share of the server and network, useful life, utilisation, power for each GPU, PUE, electricity price, other cost for each hour, and rental price. Outputs: the cost for each GPU-hour (split into depreciation, power and other), the margin at the rental price, and the payback period.
Table: a minimum of 20 KPIs. Columns: name, plain definition, unit, formula where one exists, typical value with its date, the meaning of a high or low value, and the user of the KPI (investor, operator or engineer). The reader can filter the table by user.

Module 6. How to use this knowledge
Teach: the questions that an investor asks (strength of demand, depreciation life, customer concentration, power supply, contract length, price trend). The questions that an operator asks (which tasks, which model size, seat or usage, how to budget, how to measure value, data safety). The main risks, written as questions and not as forecasts.

After the modules: a quiz of 12 questions with feedback on each answer, a glossary of 50 terms or more that the reader can search, and a list of sources with dates.
</course_plan>

<language_rules>
Write all course text to the writing rules of ASD-STE100 Simplified Technical English. This standard removes ambiguity, so a reader with no technical training understands each sentence at the first reading. Where the house rules below are different from STE, the house rules apply.

1. Give each sentence one idea. Use a maximum of 20 words in an instruction and a maximum of 25 words in a description.
2. Write most sentences with 10 to 20 words, because a long row of very short sentences is hard to read. Headings, labels, captions and list items can be shorter.
3. Use the active voice and name the actor. Write "the owner pays the cost", not "the cost is paid".
4. Use simple verb forms: present, past and future. Avoid verbs that end in -ing and avoid forms such as "has grown".
5. Use one word for one thing. After you choose a term, do not change to a synonym.
6. Define each technical term in one sentence when you first use it, and add it to the glossary. Write an abbreviation in full the first time, with the short form in brackets.
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
The reader learns faster from pictures than from text, so each module needs a minimum of one diagram that shows a real mechanism. A picture that only decorates the page does not count. Draw each diagram and chart as inline SVG, and label it in the same simple English as the text. Give each picture a caption that states what the reader must see in it. Make the calculators, the table filter, the quiz and the glossary search work without an external library. Show a filled example in each calculator when the page opens, so that the first view teaches something. Add a contents list that stays in view and shows the reader's position in the course. Use motion only where it explains a sequence, and obey the reader's reduced-motion setting. The page must work on a phone, in a light theme and in a dark theme, and each control must work from the keyboard.
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
2. Show the date and the source name near each figure. Put the full sources, with links, in one list at the end of the page.
3. Where the reference data give a range, show the range. Where the reference data mark a figure as uncertain, tell the reader that it is uncertain.
4. If the course needs a figure that is not in the reference data, do not supply one from memory. Use an example value in a calculator and label it "example value", or tell the reader that the figure is not available.
5. You can explain how the technology works from your general knowledge. Make each explanation simple, but do not make it false. Where a simple explanation hides an important detail, add a short note that starts with "Simplified:".
6. Stay neutral about companies. Do not give investment advice. Write each risk as a question that the reader can ask.
7. State in the footer that the text follows the writing rules of ASD-STE100, and that no formal check against the STE dictionary was done.
</accuracy_rules>

<output_format>
Give the course as one HTML file that contains its styles and scripts. Load only the Jost typeface from Google Fonts. After the file, write a report of 150 words or fewer in the same simple English. The report states what you built, each figure that was not in the reference data, and each rule that you could not obey.
</output_format>

<self_check>
Before you finish, check your work against this list and correct each failure:
1. Each of the seven success criteria is taught in a module and tested in the quiz.
2. Each price, cost and company number agrees with the reference data and shows its date.
3. The token cost calculator gives $0.009 for 2,000 input tokens and 500 output tokens at prices of $2 and $10 for each million tokens.
4. The GPU-hour calculator gives the same result as a calculation that you do by hand from its default values.
5. Each technical term has a definition at its first use and an entry in the glossary.
6. No description has more than 25 words in one sentence, and no instruction has more than 20 words.
7. The text has no em dashes, no semicolons, no exclamation marks and no emoji.
8. The page is easy to read in the light theme, in the dark theme and on a narrow phone screen.
</self_check>
