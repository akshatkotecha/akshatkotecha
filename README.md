<h1 align="center">Akshat Kotecha</h1>

<p align="center">
  AI/ML engineer — retrieval systems, LLM pipelines, and the data infrastructure underneath them.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white" alt="SQL Server">
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain">
  <img src="https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white" alt="FAISS">
  <img src="https://img.shields.io/badge/Plotly%20Dash-3F4F75?style=flat-square&logo=plotly&logoColor=white" alt="Plotly Dash">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java">
</p>

---

I build systems where a model is one component, not the whole answer. Most of my
work sits at the boundary between messy source data and something a person can
actually trust — extraction pipelines, retrieval that knows when it has failed,
and analysis layers that show their evidence.

A rule that runs through most of it: **the model routes, it doesn't invent.**
Where a number can be looked up, it gets looked up.

---

## Featured work

### 🏥 [Health Insurance Competitive Intelligence](https://github.com/akshatkotecha/insurance-competitive-analysis)

Built during an internship. End-to-end competitive analysis of eight Indian
health insurers — scraped from their own published PDFs, parsed into SQL Server,
and surfaced through a BI dashboard and two chatbots.

- **3,063 PDF pages → 8,492 priced segments.** Tiered downloading (plain HTTP →
  headless-Chrome fetch that defeats WAF fingerprinting → Selenium), then a
  different parsing strategy per insurer: ruled tables, word-coordinate
  reconstruction, and Tesseract OCR for the one rate chart published as an image.
- **A three-tier chatbot where the LLM never writes the answer.** Regex against
  live database contents first, keyword routing second, and the model only when
  both fail — returning a JSON route, never prose. A wrong model output produces
  a clarifying question, not a wrong premium.
- **SQL runs before retrieval, deliberately.** SQL returning zero rows is an
  unambiguous "not here"; retrieval always returns its nearest chunks however
  irrelevant, so it can never tell you it failed.
- **An insight engine, not a chart wall.** Eight functions compute findings from
  the data and return them as structured objects with the evidence rows attached.
  The pipeline caught 195 corrupt rate rows in a competitor's table by itself.

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
| **AI / ML** | RAG pipelines, FAISS, LangChain, Ollama, Groq, embedding models, prompt-as-router design |
| **Data** | SQL Server (schema design, view layers, window functions), pandas, ETL orchestration |
| **Analytics & BI** | Plotly Dash, Streamlit, Power BI, accessible chart design (CVD-validated palettes) |
| **Extraction** | pdfplumber, PyMuPDF, Tesseract OCR, Selenium, Playwright, resilient tiered scraping |
| **Languages** | Python, Java, SQL, JavaScript |

Also: data structures and competitive programming in Java — see
[DSA](https://github.com/akshatkotecha/DSA) and
[CP](https://github.com/akshatkotecha/CP).

---

<p align="center">
  <a href="mailto:akshatkotecha@gmail.com">
    <img src="https://img.shields.io/badge/Email-akshatkotecha@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email">
  </a>
</p>
