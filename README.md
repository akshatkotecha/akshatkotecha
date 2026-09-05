<h1 align="center">Akshat Kotecha</h1>

<p align="center">
  <strong>AI/ML engineer · competitive programmer</strong><br>
  I build retrieval and LLM systems that know when they don't have an answer —
  and I solve algorithm problems in Java for the same reason I like those
  systems: the constraints are the interesting part.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain">
  <img src="https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white" alt="FAISS">
  <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama">
  <img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white" alt="SQL Server">
  <img src="https://img.shields.io/badge/Codeforces-1F8ACB?style=flat-square&logo=codeforces&logoColor=white" alt="Codeforces">
</p>

---

Two threads, and they feed each other.

**Building AI systems.** RAG pipelines, LLM routing, and the extraction plumbing
underneath them. The rule I keep coming back to: **the model routes, it doesn't
invent.** Where a value can be looked up it gets looked up, and the model's job
is to decide *which* lookup — never to produce the number itself. A model that
can't hallucinate an answer is worth more than one that's usually right.

**Competitive programming.** 335 Java solutions across 224 Codeforces contests,
plus a LeetCode set. It's where the instinct for complexity bounds and edge cases
comes from — the same instinct that decides whether a retrieval fallback is safe.

---

## Featured work

### 🏥 [Health Insurance Competitive Intelligence](https://github.com/akshatkotecha/insurance-competitive-analysis)

Built during an internship. A full pipeline from eight insurers' published PDFs
to a queryable system — **3,063 PDF pages in, 8,492 structured rows out** —
fronted by two chatbots and a BI dashboard.

**The retrieval architecture is the interesting part.**

- **Three-tier routing where the LLM never writes the answer.** Regex matched
  against live database contents first, keyword routing second, and the model
  only when both fail — returning a JSON route
  (`{"intent": "metric", "company": "ABHI", "year": 2023}`), never prose. That
  route feeds the same parameterised queries as tier 1, so a wrong model output
  produces a clarifying question rather than a wrong number.
- **SQL runs before retrieval, deliberately.** SQL returning zero rows is an
  unambiguous "not in the database", so falling back to vector search is safe.
  Retrieval has no such signal — it always returns its nearest chunks however
  irrelevant, so it can never tell you it failed. The reliable source goes first.
- **Two chatbots, same core.** A SQL-only bot that cannot hallucinate by
  construction, and a SQL+RAG bot that adds FAISS retrieval over brochure text
  with a local model (Ollama) for questions that only live in policy prose.
- **Extraction that survives real websites.** Tiered downloading — plain HTTP, a
  headless-Chrome fetch that defeats WAF fingerprinting, then Selenium — and a
  different parsing strategy per insurer: ruled tables, word-coordinate
  reconstruction, and Tesseract OCR for the one rate chart published as an image.
- **The pipeline audits itself.** It flagged 195 corrupt rate rows in a
  competitor's table — 22% of it — by comparing each row against its own slab's
  median rather than an absolute threshold.

`Python` · `LangChain` · `FAISS` · `Ollama` · `Groq` · `SQL Server` · `Tesseract` · `Dash`

### ⚔️ Competitive programming — [CP](https://github.com/akshatkotecha/CP) · [DSA](https://github.com/akshatkotecha/DSA)

**335 Java solutions across 224 Codeforces contests**, each with its own
write-up, plus a LeetCode set covering dynamic programming, binary trees,
strings and greedy algorithms.

Kept as a worked archive rather than a dump — every problem folder carries the
solution and a README, so the reasoning is recoverable later, not just the
accepted code.

`Java` · `algorithms` · `data structures` · `complexity analysis`

### 🧠 [Synapse Quest](https://github.com/akshatkotecha/synapse-quest-ai)

AI-driven developer productivity platform: task routing based on expertise
inferred from Git telemetry, plus behavioural analytics and a REST API for
engineering teams. Started at a hackathon, extended afterwards.

`JavaScript` · `Git telemetry` · `REST API`

### ⌚ [Second Movement Watch Scraper](https://github.com/akshatkotecha/sm-watch-scraper)

A self-updating catalogue scraper that builds price history over time rather
than overwriting it. Three fetch strategies cheapest-first — `curl_cffi`
mimicking Chrome's TLS fingerprint, plain `requests`, then Playwright only where
JS rendering is genuinely required — with `schema.org` extraction, caching, and
resumable runs.

`Python` · `Playwright` · `curl_cffi`

### 📈 [NIFTY Options Pricing Model](https://github.com/akshatkotecha/nifty-options-pricing-model)

Black–Scholes pricing with strategy simulation for NIFTY derivatives — Greeks,
payoff modelling, and backtested option strategies.

`Python` · `NumPy` · `quantitative finance`

---

## What I work with

| | |
|---|---|
| **AI / ML** | RAG pipelines, FAISS, LangChain, Ollama, Groq, embedding models, prompt-as-router design, deterministic-first fallback chains |
| **Algorithms** | Data structures, dynamic programming, graphs, greedy, complexity analysis — in Java |
| **Data & backend** | SQL Server schema and view design, pandas, ETL orchestration, idempotent pipelines |
| **Extraction** | pdfplumber, PyMuPDF, Tesseract OCR, Selenium, Playwright, resilient tiered scraping |
| **Languages** | Python, Java, SQL, JavaScript |

---

<p align="center">
  <a href="mailto:akshatkotecha@gmail.com">
    <img src="https://img.shields.io/badge/Email-akshatkotecha@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email">
  </a>
</p>
