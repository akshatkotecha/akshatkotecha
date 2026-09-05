<h1 align="center">Akshat Kotecha</h1>

<p align="center">
  <strong>AI/ML engineer · competitive programmer</strong><br>
  I build retrieval and LLM systems that know when they don't have an answer.
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

**The rule I keep coming back to: the model routes, it doesn't invent.**

Where a value can be looked up, it gets looked up. The model's job is deciding
*which* lookup — never producing the number itself. A system that can't
hallucinate an answer is worth more than one that's usually right.

**1,200+ problems solved across competitive programming platforms.** That's
where the instinct for complexity bounds and edge cases comes from — the same
instinct that decides whether a retrieval fallback is safe to take.

---

## Featured work

### 🏥 [Health Insurance Competitive Intelligence](https://github.com/akshatkotecha/insurance-competitive-analysis)

Built during an internship. Eight insurers' published PDFs to a queryable
system — **3,063 pages in, 8,492 structured rows out** — fronted by two chatbots
and a BI dashboard.

- **Three-tier routing, and the LLM never writes the answer.** Regex against
  live database contents first, keyword routing second, the model only when both
  fail — returning a JSON route, never prose. It feeds the same parameterised
  queries as tier one, so a bad model output yields a clarifying question instead
  of a wrong number.
- **SQL runs before retrieval, on purpose.** Zero rows is an unambiguous "not in
  the database", so falling back to vector search is safe. Retrieval has no such
  signal — it always returns its nearest chunks however irrelevant, so it can
  never tell you it failed.
- **Two bots, one core.** A SQL-only assistant that cannot hallucinate by
  construction, and a SQL-then-RAG variant adding FAISS retrieval over brochure
  text with a local model for questions that only exist in policy prose.
- **Extraction that survives real websites.** Plain HTTP, then a headless-Chrome
  fetch that defeats WAF fingerprinting, then Selenium — with a different parser
  per insurer: ruled tables, word-coordinate reconstruction, and OCR for the one
  rate chart published as an image.
- **The pipeline audits itself.** It caught 195 corrupt rows in a competitor's
  rate table — 22% of it — by testing each row against its own slab's median
  rather than a fixed threshold.

`Python` · `LangChain` · `FAISS` · `Ollama` · `Groq` · `SQL Server` · `Tesseract` · `Dash`

### ⚔️ Competitive programming — [CP](https://github.com/akshatkotecha/CP) · [DSA](https://github.com/akshatkotecha/DSA)

**1,200+ problems solved across platforms**, spanning dynamic programming,
graphs, trees, strings and greedy algorithms.

These repos are the archive of that: Codeforces and LeetCode solutions in Java,
each kept with its own write-up so the reasoning survives, not just the accepted
code.

`Java` · `algorithms` · `data structures` · `complexity analysis`

### 🧠 [Synapse Quest](https://github.com/akshatkotecha/synapse-quest-ai)

AI-driven developer productivity platform — task routing from expertise inferred
out of Git telemetry, with behavioural analytics and a REST API. Started at a
hackathon, extended afterwards.

`JavaScript` · `Git telemetry` · `REST API`

### ⌚ [Second Movement Watch Scraper](https://github.com/akshatkotecha/sm-watch-scraper)

A self-updating catalogue scraper that builds price history rather than
overwriting it. Three fetch strategies cheapest-first — `curl_cffi` mimicking
Chrome's TLS fingerprint, plain `requests`, Playwright only where JS rendering
is genuinely required — with `schema.org` extraction, caching and resumable runs.

`Python` · `Playwright` · `curl_cffi`

### 📈 [NIFTY Options Pricing Model](https://github.com/akshatkotecha/nifty-options-pricing-model)

Black–Scholes pricing with strategy simulation for NIFTY derivatives — Greeks,
payoff modelling and backtested strategies.

`Python` · `NumPy` · `quantitative finance`

---

## What I work with

| | |
|---|---|
| **AI / ML** | RAG pipelines, FAISS, LangChain, Ollama, Groq, embedding models, prompt-as-router design, deterministic-first fallback chains |
| **Algorithms** | Dynamic programming, graphs, trees, greedy, complexity analysis — in Java |
| **Data & backend** | SQL Server schema and view design, pandas, ETL orchestration, idempotent pipelines |
| **Extraction** | pdfplumber, PyMuPDF, Tesseract OCR, Selenium, Playwright, resilient tiered scraping |
| **Languages** | Python, Java, SQL, JavaScript |

---

<p align="center">
  <a href="https://www.linkedin.com/in/akshat-kotecha-a3b4341ba/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="mailto:akshatkotecha@gmail.com">
    <img src="https://img.shields.io/badge/Email-akshatkotecha@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email">
  </a>
</p>
