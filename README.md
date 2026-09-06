<!-- ══════════════ BANNER ══════════════ -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=shark&color=0:1E1B4B,50:4F46E5,100:7C3AED&height=200&section=header&text=Akshat%20Kotecha&fontColor=FFFFFF&fontSize=52&fontAlignY=34&desc=AI/ML%20Engineer%20%C2%B7%20Competitive%20Programmer&descAlignY=54&descSize=18&animation=fadeIn" alt="Akshat Kotecha"/>

<!-- ══════════════ TYPING + LINKS ══════════════ -->
<p align="center">
  <a href="https://github.com/akshatkotecha">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3200&pause=900&color=6366F1&center=true&vCenter=true&width=620&lines=The+model+routes%2C+it+doesn't+invent.;RAG+pipelines+that+know+when+they've+failed.;750%2B+problems+solved+%E2%80%94+top+0.3%25+on+LeetCode.;B.Tech+CE+%40+DJ+Sanghvi+%7C+CGPA+9.13" alt="Typing SVG"/>
  </a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/akshat-kotecha-a3b4341ba/"><img src="https://img.shields.io/badge/LinkedIn-4F46E5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:akshatkotecha@gmail.com"><img src="https://img.shields.io/badge/Email-4F46E5?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <a href="https://leetcode.com/"><img src="https://img.shields.io/badge/LeetCode-Top%200.3%25-4F46E5?style=for-the-badge&logo=leetcode&logoColor=white" alt="LeetCode"/></a>
  <a href="https://codeforces.com/"><img src="https://img.shields.io/badge/Codeforces-Pupil-4F46E5?style=for-the-badge&logo=codeforces&logoColor=white" alt="Codeforces"/></a>
  <a href="https://www.codechef.com/"><img src="https://img.shields.io/badge/CodeChef-3%E2%98%85-4F46E5?style=for-the-badge&logo=codechef&logoColor=white" alt="CodeChef"/></a>
</p>

---

## About

I build retrieval and LLM systems that know when they don't have an answer — and
I compete in algorithm contests for the same reason I enjoy those systems: the
constraints are where the thinking happens.

The rule I keep coming back to: **the model routes, it doesn't invent.** Where a
value can be looked up, it gets looked up. The model's job is deciding *which*
lookup — never producing the number itself. A system that can't hallucinate an
answer is worth more than one that's usually right.

```bash
akshat@github:~$ whoami --verbose
  role       : AI/ML Engineer · Competitive Programmer
  education  : B.Tech Computer Engineering, DJ Sanghvi College  (2028, CGPA 9.13)
  experience : AI/ML Intern @ GenXAI Analytics
  location   : Mumbai, India
  focus      : RAG · LLM routing · extraction pipelines · DSA
  stack      : Python · Java · SQL Server · LangChain · FAISS · Ollama
  principle  : "deterministic first, model last"
```

---

## Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=py,java,c,mysql,sqlite,git&theme=dark" alt="Languages"/><br>
  <img src="https://skillicons.dev/icons?i=flask,react,tailwind,linux,github,vscode&theme=dark" alt="Tools"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white"/>
  <img src="https://img.shields.io/badge/FAISS-4F46E5?style=flat-square&logo=meta&logoColor=white"/>
  <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white"/>
  <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white"/>
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white"/>
  <img src="https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white"/>
</p>

---

## Domain Expertise

| Area | What I actually do in it |
|---|---|
| **RAG & LLM systems** | Prompt-as-router design, deterministic-first fallback chains, FAISS retrieval, local inference with Ollama, grounding every figure in a query result rather than generation |
| **Data engineering** | SQL Server schema and view design, idempotent ETL, extraction pipelines that survive real websites, data-quality instrumentation |
| **Document extraction** | pdfplumber, PyMuPDF, Tesseract OCR, tiered scraping through bot protection, per-publisher parsing strategies |
| **Algorithms** | Dynamic programming, graphs, trees, greedy, complexity analysis — in Java, under contest time pressure |

---

## Featured Projects

<details open>
<summary><b>🏥 Health Insurance Competitive Intelligence</b> — SQL + RAG query system over 8 insurers</summary>

<br>

Built during my internship at GenXAI Analytics. Eight insurers' published PDFs to
a queryable system — **3,063 pages in, 8,492 structured rows out** — fronted by
two chatbots and a BI dashboard.

- **Three-tier routing, and the LLM never writes the answer.** Regex against live
  database contents first, keyword routing second, the model only when both fail
  — returning a structured route, never prose. A bad model output yields a
  clarifying question instead of a wrong number.
- **SQL runs before retrieval, on purpose.** An empty result set unambiguously
  means the answer isn't structured, so falling back to vector search is safe.
  Retrieval has no such signal — it always returns its nearest chunks however
  irrelevant, so it can never tell you it failed.
- **Two bots, one core.** A SQL-only assistant that cannot hallucinate by
  construction, and a SQL-then-RAG variant adding FAISS retrieval over brochure
  text with a local Qwen2.5 model for questions that only live in policy prose.
- **Extraction that survives real websites.** Plain HTTP → a headless-Chrome
  fetch that defeats WAF fingerprinting → Selenium, with a different parser per
  insurer: ruled tables, word-coordinate reconstruction, and OCR for the one rate
  chart published as an image.
- **The pipeline audits itself** — it caught 195 corrupt rows in a competitor's
  rate table (22% of it) by testing each row against its own slab's median.

`Python` · `SQL Server` · `Streamlit` · `LangChain` · `FAISS` · `Ollama` · `pdfplumber` · `Selenium` · `Tesseract`

**[→ Repository](https://github.com/akshatkotecha/insurance-competitive-analysis)**

</details>

<details>
<summary><b>🛡️ Sentinel</b> — Developer productivity platform: code scoring, Git-telemetry behaviour signals, skill-based task routing</summary>

<br>

A developer command centre on a Flask backend that ingests Git commit telemetry
to profile each contributor's activity across a codebase, then routes incoming
tickets from those profiles rather than distributing them uniformly.

`React.js` · `Python (Flask)` · `TailwindCSS` · `Git integration`

**[→ Repository](https://github.com/akshatkotecha/sentinel)**

</details>

<details>
<summary><b>⌚ Second Movement Watch Scraper</b> — self-updating catalogue with price history</summary>

<br>

Tracks every pre-owned watch on a retailer's site, building price history over
time rather than overwriting it. Three fetch strategies cheapest-first —
`curl_cffi` mimicking Chrome's TLS fingerprint, plain `requests`, then Playwright
only where JS rendering is genuinely required — with `schema.org` extraction,
caching and resumable runs.

`Python` · `Playwright` · `curl_cffi` · `openpyxl`

**[→ Repository](https://github.com/akshatkotecha/sm-watch-scraper)**

</details>

<details>
<summary><b>📈 NIFTY Options Pricing Model</b> — Black–Scholes with strategy simulation</summary>

<br>

Black–Scholes pricing for NIFTY derivatives with Greeks, payoff modelling and
backtested option strategies.

`Python` · `NumPy` · `quantitative finance`

**[→ Repository](https://github.com/akshatkotecha/nifty-options-pricing-model)**

</details>

---

## Experience

**AI/ML Intern** · GenXAI Analytics — *Jun 2026 – Jul 2026*

- Built a pipeline parsing brochures, rate charts and annual reports for **8 Indian health insurers**, with Selenium and OCR fallbacks for image-only PDFs.
- Designed a **3-schema SQL Server database** covering premiums, policy features and financials (GWP, ROE, solvency), reducing manual brochure comparison to single queries.

`Python` `SQL Server` `Selenium` `OCR` `ETL`

**Marketing Team** · CodeStars — *Oct 2025 – May 2026*

- Ran sponsorship outreach and fundraising for Code Uncode across engineering colleges in Maharashtra.

---

## Competitive Programming

| Platform | Standing |
|---|---|
| **LeetCode** | **Top 0.3% globally** — 750+ algorithmic problems solved |
| **CodeChef** | **Top 5% in India** — 3★, maximum rating 1636 |
| **Codeforces** | Maximum rating **1310 (Pupil)** across consistent rated participation |
| **Code Uncode 2026** | **Rank 60** nationally |

Solutions archived with write-ups in [CP](https://github.com/akshatkotecha/CP) and
[DSA](https://github.com/akshatkotecha/DSA) — the reasoning kept alongside the
accepted code, not just the submission.

---

## GitHub Activity

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=akshatkotecha&hide_border=true&background=0D1117&stroke=6366F1&ring=7C3AED&fire=7C3AED&currStreakLabel=C9D1D9&sideLabels=C9D1D9&dates=8B949E&currStreakNum=C9D1D9&sideNums=C9D1D9" alt="streak"/>
</p>

---

## Currently

```yaml
learning:  [ agentic workflows, vector database internals, model evaluation ]
building:  [ retrieval systems where the model routes and never invents ]
grinding:  [ Codeforces rated contests, LeetCode dailies ]
open_to:   [ AI/ML engineering internships and roles ]
reach_me:  akshatkotecha@gmail.com
```

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:7C3AED,50:4F46E5,100:1E1B4B&height=120&section=footer"/>
