# Billu Bhaiya · Free Guides

Reels ke full detail versions — phone pe padhne ke liye, 11 pages each.

<p align="center">
  <img src="pages/page-01.jpg" alt="Startup Idea guide cover" width="260" />
  <img src="rag-to-production/pages/page-01.jpg" alt="RAG to Production guide cover" width="260" />
  <img src="ai-agent-production/pages/page-01.jpg" alt="AI Agent Demo to Production guide cover" width="260" />
  <img src="website-to-google/pages/page-01.jpg" alt="Website Live to Google SEO guide cover" width="260" />
  <img src="aeo-geo/pages/page-01.jpg" alt="AEO + GEO guide cover" width="260" />
  <img src="ai-agent-security/pages/page-01.jpg" alt="AI Agent Security guide cover" width="260" />
</p>

## 📄 Guides

| Guide | PDF | Web |
| --- | --- | --- |
| **Startup Idea se Paying Customer tak** — pehle market, phir code | [Open PDF](Billu-Bhaiya-Startup-Idea-Guide.pdf) | [Read online](https://rupakghosh4865.github.io/startup-idea-guide/) |
| **RAG Demo se Production tak** — Evals · LLMOps · Guardrails · Agents | [Open PDF](rag-to-production/Billu-Bhaiya-RAG-to-Production-Guide.pdf) | [Read online](https://rupakghosh4865.github.io/startup-idea-guide/rag-to-production/) |
| **AI Agent: Demo se Production tak** — 6 fixes + copy-paste code | [Open PDF](ai-agent-production/Billu-Bhaiya-AI-Agent-Production-Guide.pdf) | [Read online](https://rupakghosh4865.github.io/startup-idea-guide/ai-agent-production/) |
| **Website Live se Google tak** — SEO: audit, fix, speed, Search Console, Bing, ranking | [Open PDF](website-to-google/Billu-Bhaiya-Website-to-Google-SEO-Guide.pdf) | [Read online](https://rupakghosh4865.github.io/startup-idea-guide/website-to-google/) |
| **AI Answers mein tumhara Brand** — AEO + GEO: ChatGPT, Perplexity, Gemini, Copilot | [Open PDF](aeo-geo/Billu-Bhaiya-AEO-GEO-Guide.pdf) | [Read online](https://rupakghosh4865.github.io/startup-idea-guide/aeo-geo/) |
| **Login ≠ Permission: AI Agent Security** — URL · npm · lethal trifecta · blast radius | [Open PDF](ai-agent-security/Billu-Bhaiya-AI-Agent-Security-Guide.pdf) | [Read online](https://rupakghosh4865.github.io/startup-idea-guide/ai-agent-security/) |

## 1 · Startup Idea se Paying Customer tak

| # | Step | Kya milta hai |
| --- | --- | --- |
| 1 | **TrustMRR** | Kaun se chhote SaaS already paying customers se kama rahe hain |
| 2 | **Product Hunt** | Negative reviews = next opportunity |
| 3 | **IdeaBrowser** | Niche ideas (list mein hona ≠ profitable) |
| 4 | **Validation** | Claude + ChatGPT se research, phir khud verify |
| 5 | **Market Gap** | Competitors kahan fail ho rahe hain → wahi gap = tumhara product |
| 6 | **Claude Code** | Public user journey → `SPEC.md` |
| 7 | **Build** | Sirf 1 core feature wala MVP |
| ₹ | **Bonus** | Pehla paying customer + paid pilot |

<p>
  <img src="pages/page-03.jpg" alt="Step 1: TrustMRR" width="240" />
  <img src="pages/page-06.jpg" alt="Step 4: Validation" width="240" />
  <img src="pages/page-10.jpg" alt="Bonus: first paying customer" width="240" />
</p>

## 2 · RAG Demo se Production tak

| # | Step | Kya milta hai |
| --- | --- | --- |
| 1 | **Eval Set** | 30–50 real sawaal + sahi jawab (`evals/dataset.jsonl`) |
| 2 | **Measure** | Retrieval aur faithfulness alag-alag score |
| 3 | **Judge** | RAGAS + copy-paste LLM-as-judge prompt |
| 4 | **Eval Loop** | Har change ke baad run, experiment log |
| 5 | **Tracing** | Langfuse / LangSmith — production ka CCTV |
| 6 | **Guardrails** | Prompt injection, data leak, red-team set |
| 7 | **Agent ya Workflow?** | Kab agent, kab seedha workflow |
| ★ | **Portfolio** | 1 project, poora proof + README template |

<p>
  <img src="rag-to-production/pages/page-04.jpg" alt="Step 2: Retrieval vs faithfulness" width="240" />
  <img src="rag-to-production/pages/page-06.jpg" alt="Step 4: Eval loop and experiment log" width="240" />
  <img src="rag-to-production/pages/page-09.jpg" alt="Step 7: Agent ya workflow" width="240" />
</p>

## 3 · AI Agent: Demo se Production tak

"Laptop band karo" — agar agent bhi band ho gaya, toh woh demo hai. 6 fixes, har ek ke saath copy-paste code:

| # | Fix | Kya milta hai |
| --- | --- | --- |
| 1 | **Memory** | LangGraph + Postgres checkpointer (stable `thread_id`), PostgresStore, pgvector |
| 2 | **Queue** | FastAPI turant `job_id` → Redis → Celery worker (`acks_late`, idempotent tasks) |
| 3 | **Reliability** | Tenacity retries, exponential backoff + jitter, Stripe idempotency key, human-in-the-loop |
| 4 | **Cost** | Claude prompt caching, Haiku vs Sonnet routing, LiteLLM budgets |
| 5 | **Security** | Prompt injection (OWASP LLM Top 10), Pydantic, least privilege, E2B sandbox, Secrets Manager |
| 6 | **Evals + Observability** | Langfuse traces, promptfoo in GitHub Actions → merge block |
| ★ | **Deploy** | Docker + Railway (API aur worker alag scale), "laptop band" test |

<p>
  <img src="ai-agent-production/pages/page-04.jpg" alt="Fix 2: Queue" width="240" />
  <img src="ai-agent-production/pages/page-06.jpg" alt="Fix 3: Idempotency and human-in-the-loop" width="240" />
  <img src="ai-agent-production/pages/page-11.jpg" alt="Demo vs Production" width="240" />
</p>

## 4 · Website Live se Google tak

Website live hai par Google pe nahi dikhti? **Live ≠ Indexed ≠ Ranked** — teen alag stages. Guess nahi, measure:

| # | Step | Kya milta hai |
| --- | --- | --- |
| 1 | **Audit** | Claude Code SEO plugin (`/seo audit <url>`), PageSpeed Insights, Screaming Frog |
| 2 | **Technical fix** | `git commit` pehle; robots.txt, noindex, canonical, broken links, sitemap (Next.js `robots.ts`, `sitemap.ts`) |
| 3 | **Metadata + Schema** | Next.js `generateMetadata`, canonical, JSON-LD — sirf jo page pe dikhta hai |
| 4 | **Speed** | LCP ≤ 2.5s, INP ≤ 200ms, CLS ≤ 0.1 at p75 (real users) |
| 5 | **Google Search Console** | DNS TXT verify, sitemap, URL inspection, request indexing, Pages report statuses |
| 6 | **Bing + IndexNow** | Search Console se import, IndexNow ping, Copilot citations |
| 7 | **Ranking** | Performance report: CTR, position 11–20, helpful content — aur sabr |

<p>
  <img src="website-to-google/pages/page-02.jpg" alt="Live, Indexed, Ranked" width="240" />
  <img src="website-to-google/pages/page-07.jpg" alt="Google Search Console" width="240" />
  <img src="website-to-google/pages/page-09.jpg" alt="Ranking with Performance report" width="240" />
</p>

## 5 · AI Answers mein tumhara Brand (AEO + GEO)

SEO ho gaya, phir bhi ChatGPT tumhara naam nahi leta? AI answers mein sirf ranking nahi — **brand mentions aur trusted sources** bhi chalte hain:

| # | Step | Kya milta hai |
| --- | --- | --- |
| 1 | **Measure** | 30 buyer sawaal × 3 runs × ChatGPT / Perplexity / Gemini, prompt tracking sheet, mention rate |
| 2 | **AI crawlers** | robots.txt: OAI-SearchBot, PerplexityBot, GPTBot (training alag); content raw HTML mein |
| 3 | **Answer first** | Heading mein sawaal, 40–60 words mein jawab, phir stats + source |
| 4 | **Trust** | Reddit, YouTube, review sites — asli mentions, fake reviews nahi |
| 5 | **Prove** | Har hafte wahi sawaal; Bing AI Performance, Search Console, GA4 regex; 1 change, 4 hafte |
| ★ | **llms.txt** | Optional — pehle basics |

<p>
  <img src="aeo-geo/pages/page-03.jpg" alt="Measure" width="240" />
  <img src="aeo-geo/pages/page-04.jpg" alt="AI crawlers" width="240" />
  <img src="aeo-geo/pages/page-09.jpg" alt="Prove" width="240" />
</p>

## 6 · Login ≠ Permission: AI Agent Security

Client ki site pe HTTPS, MFA, rate limit — sab green. Phir bhi AI agent ne saare customers ka data bhej diya. Kyunki **login identity check hai, permission nahi**:

| Level | Kya hua | Fix |
| --- | --- | --- |
| 1 | **URL badlo** — invoice/123 → 124 (IDOR / BOLA) | Har request pe server-side ownership check + Postgres Row-Level Security |
| 2 | **npm package** — Shai-Hulud: install scripts se tokens chori | Release cooldown, approved build scripts, GitHub push protection, short-lived tokens |
| 3 | **AI agent** — lethal trifecta: private data + untrusted content + bahar bhejna | Ek leg hatao; least-privilege tools, human approval, audit logs, kill switch |
| ★ | **Blast radius** | Maan lo agent compromise hoga — read-only role, row limits, network allowlist |

<p>
  <img src="ai-agent-security/pages/page-03.jpg" alt="Level 1: ownership check" width="240" />
  <img src="ai-agent-security/pages/page-05.jpg" alt="Level 2: npm" width="240" />
  <img src="ai-agent-security/pages/page-07.jpg" alt="Level 3: lethal trifecta" width="240" />
</p>

---

Demo toh sab bana lete hain — **jo measure karta hai, wahi hire hota hai.** Chalo, build karte hain! 🚀

<sub>Tools ke features aur pricing badalte rehte hain — latest info unki official websites aur docs pe check karo.</sub>
