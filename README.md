<h1 align="center">Akshat Kotecha</h1>

<p align="center">
  <strong>Data analyst · AI/ML engineer</strong><br>
  I turn messy source data into answers people can act on — and into retrieval
  systems that know when they don't have one.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white" alt="SQL Server">
  <img src="https://img.shields.io/badge/Plotly%20Dash-3F4F75?style=flat-square&logo=plotly&logoColor=white" alt="Plotly Dash">
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="pandas">
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain">
  <img src="https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white" alt="FAISS">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java">
</p>

---

Two halves of the same job, and I work on both ends of it.

**The analysis:** getting to a defensible number — schema and view design, the
statistics behind a comparison, and being explicit about what the data cannot
support. A finding without its evidence attached isn't finished.

**The engineering:** extraction pipelines, RAG, and LLM plumbing where the model
is one component rather than the whole answer. A rule that runs through most of
it — **the model routes, it doesn't invent.** Where a number can be looked up,
it gets looked up.

---

## Featured work

### 🏥 [Health Insurance Competitive Intelligence](https://github.com/akshatkotecha/insurance-competitive-analysis)

Built during an internship. End-to-end competitive analysis of eight Indian
health insurers — scraped from their own published PDFs, parsed into SQL Server,
and surfaced through a BI dashboard and two chatbots. **3,063 PDF pages in,
8,492 priced segments out.**

**What the analysis found**

- The focal insurer's price advantage **runs out at 66+** — the price index
  crosses 100 between the 56-65 and 66+ bands, after undercutting the market
  everywhere below it.
- It **doesn't compete at the entry price point.** Its cheapest cover is ₹7 L;
  all six competitors with rate data sell from ₹5 L, so a shopper starting at
  the lowest cover never sees its quote.
- One rival **undercuts it in 81% of shared segments** — more than triple the
  next closest competitor.
- **22% of that rival's rate table is corrupt**, caught by the pipeline rather
  than by eye: 195 rows sitting below a quarter of their own slab's median.

**How it's built**

- An **18-view SQL layer** carries the analytical logic — price indexing, peer
  ranking, CAGR, data-quality checks. Python reads views, never base tables, so
  the analysis is versioned SQL rather than pandas scattered across scripts.
- An **insight engine, not a chart wall.** Eight functions compute findings and
  return them as structured objects with the evidence rows attached; every claim
  on screen is one click from the data underneath it.
- **Reliability is enforced, not assumed.** Comparisons drawn against fewer than
  four competitors are greyed, labelled with their sample size, and excluded from
  every headline figure.
- **Tiered extraction:** plain HTTP → a headless-Chrome fetch that defeats WAF
  fingerprinting → Selenium, then a different parsing strategy per insurer —
  ruled tables, word-coordinate reconstruction, and Tesseract OCR for the one
  rate chart published as an image.
- **A chatbot where the LLM never writes the answer.** Regex against live
  database contents first, keyword routing second, the model only when both fail
  — returning a JSON route, never prose. A wrong model output produces a
  clarifying question, not a wrong premium. SQL runs before retrieval on purpose:
  zero rows is an unambiguous "not here", while retrieval always returns its
  nearest chunks however irrelevant, so it can never tell you it failed.

`Python` · `SQL Server` · `Dash/Plotly` · `Streamlit` · `LangChain` · `FAISS` · `Ollama` · `Tesseract`

### 📈 [NIFTY Options Pricing Model](https://github.com/akshatkotecha/nifty-options-pricing-model)

Black–Scholes pricing with strategy simulation for NIFTY derivatives — Greeks,
payoff modelling, and backtested option strategies.

`Python` · `NumPy` · `quantitative finance`

### ⌚ [Second Movement Watch Scraper](https://github.com/akshatkotecha/sm-watch-scraper)

A self-updating catalogue scraper that tracks every pre-owned watch on a
retailer's site, building price history over time rather than overwriting it.

- Three fetch strategies, cheapest first: `curl_cffi` mimicking Chrome's TLS
  fingerprint, plain `requests`, then Playwright only where JS rendering is
  genuinely required.
- Reads `schema.org` JSON-LD plus the on-page spec table, with a regex prose
  fallback for fields the table omits.
- Incremental and resumable — caches parsed products, saves every 20 pages, and
  resumes cleanly after an interrupted run.

`Python` · `Playwright` · `curl_cffi` · `openpyxl`

### 🧠 [Synapse Quest](https://github.com/akshatkotecha/synapse-quest-ai)

Developer productivity analytics from Git telemetry, with AI-driven task routing
based on inferred developer expertise. Started at a hackathon, extended
afterwards with deeper analytics and a REST API.

`JavaScript` · `Git telemetry` · `REST API`

---

## What I work with

| | |
|---|---|
| **Analytics & BI** | SQL Server schema and view design, window functions, Plotly Dash, Power BI, Streamlit, accessible chart design with CVD-validated palettes |
| **AI / ML** | RAG pipelines, FAISS, LangChain, Ollama, Groq, embedding models, prompt-as-router design |
| **Data engineering** | ETL orchestration, pandas, idempotent pipelines, data-quality instrumentation |
| **Extraction** | pdfplumber, PyMuPDF, Tesseract OCR, Selenium, Playwright, resilient tiered scraping |
| **Languages** | Python, SQL, Java, JavaScript |

Also: data structures and competitive programming in Java — see
[DSA](https://github.com/akshatkotecha/DSA) and
[CP](https://github.com/akshatkotecha/CP).

---

<p align="center">
  <a href="mailto:akshatkotecha@gmail.com">
    <img src="https://img.shields.io/badge/Email-akshatkotecha@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email">
  </a>
</p>
