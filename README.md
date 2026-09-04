<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,2,5,30&height=200&section=header&text=Aman%20Dadsena&fontSize=54&fontColor=ffffff&animation=fadeIn&fontAlignY=34&desc=Full-Stack%20·%20Applied%20AI%20·%20Retrieval%20Systems&descAlignY=53&descSize=16" width="100%" alt="Aman Dadsena" />

<a href="https://github.com/AmanDadsena">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=21&pause=1200&color=58A6FF&center=true&vCenter=true&width=700&lines=Full-stack+developer+from+India;Next.js+%2B+TypeScript+front%2C+FastAPI+%2B+Python+back;I+build+AI+that+cites+its+sources;Retrieval+is+measured%2C+not+asserted" alt="Typing SVG" />
</a>

<br/>

<a href="https://nyay-setu-sigma.vercel.app"><img src="https://img.shields.io/badge/Live_Project-NyaySetu-58A6FF?style=for-the-badge&logo=vercel&logoColor=white" alt="Live project" /></a>
<a href="mailto:aman.dadsena07@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<img src="https://komarev.com/ghpvc/?username=AmanDadsena&label=Profile%20views&color=58a6ff&style=for-the-badge" alt="Profile views" />

</div>

---

## 👋 About me

I'm a developer from India building **full-stack AI applications that have to be right, not just fluent.**

Most of my time goes into **[NyaySetu](https://github.com/AmanDadsena/NyaySetu)** — an open-source legal assistant that answers questions about Indian law in eight languages. The interesting part isn't the chatbot; it's that every answer is grounded in a real statute passage, and the retrieval behind it is **evaluated with actual metrics** rather than vibes.

- 🔭 Building **NyaySetu** — retrieval-grounded legal help, 8 languages, works offline
- 🧠 Full-stack on purpose: **Next.js 16 + React 19 + TypeScript** front, **FastAPI + Python** back
- 📐 Interested in **hybrid retrieval, cross-lingual search, and evaluation harnesses** — the unglamorous part that decides whether an AI product actually works
- ⚡ I ship: deployed, documented, and usable by someone who isn't me
- 📫 Reach me at **aman.dadsena07@gmail.com**

> **Open to internships and collaborations** in AI/ML engineering, backend, and full-stack development.

---

## ⚖️ NyaySetu — Retrieval-Grounded Legal Assistant for India

<div align="center">

**_Resolve Smarter. Move Faster._**

**[🌐 Live app](https://nyay-setu-sigma.vercel.app)** &nbsp;·&nbsp; **[📂 Source](https://github.com/AmanDadsena/NyaySetu)**

</div>

Legal information in India is dense, expensive to interpret, and mostly written in English — for a population that largely doesn't read legal English. NyaySetu answers plain-language questions about the law, **in the language you asked in**, and shows you the exact statute passage the answer came from.

### The design decision that matters

**Retrieval produces the law. Generation only phrases it.**

The provider chain degrades gracefully — `local LLM (Ollama) → hosted model (Gemini) → extractive` — and that final fallback composes the reply directly from the retrieved passages. It *cannot* invent a section number, because it never writes one. The whole system keeps working with **no API key, no GPU, and no network.**

### Retrieval is measured, not asserted

`python -m app.rag.eval` is a gate in the repo, not a claim in a README:

| Metric | Result |
|---|---|
| Questions evaluated | **131** |
| hit@1 | **92.4%** |
| hit@3 | **100%** |
| MRR | **0.961** |
| False positives | **0 / 14** |

Cross-lingual scores are reported **separately**, because an aggregate dominated by English hides failure completely — 70 questions across seven languages: 100% answered, 93% hit@1, 100% hit@3. That split caught two regressions nothing else would have.

**Ablation** (`scripts/ablate.py`) — which part of the stack actually does the work:

| Condition | English hit@1 | Cross-lingual hit@1 |
|---|---|---|
| BM25 only | 91.5% | 0% |
| BM25 + dense | 92.3% | 50.7% |
| BM25 + lexicon | 91.5% | 88.1% |
| **All three** | **92.3%** | **92.5%** |

### What's in it

| | |
|---|---|
| 🔍 **Hybrid retrieval** | BM25 inverted index + a 2,012-entry cross-lingual legal lexicon + multilingual embeddings, fused by reciprocal rank |
| 📚 **Curated corpus** | 152 passages, each carrying its act, its section, and a verifiable source |
| 🗣️ **Eight languages** | Hindi, Tamil, Telugu, Bengali, Kannada, Gujarati, Marathi, English — with voice input and text-to-speech |
| 🧰 **Deterministic toolkit** | Court fees, stamp duty, limitation periods, maintenance, jurisdiction/forum, court holidays, case timelines — calculated, not generated |
| 📄 **Document analysis** | Upload a PDF or DOCX for clause extraction, risk flags, and a plain-language summary |
| 👨‍⚖️ **Directory & cases** | Lawyer directory, case tracking, threaded discussion |

<div align="center">

`Next.js 16` · `React 19` · `TypeScript` · `Tailwind v4` · `shadcn/ui`
`FastAPI` · `SQLAlchemy` · `PostgreSQL` · `Pydantic` · `BM25` · `Sentence-Transformers`
`Ollama` · `Gemini` · `JWT` · `Docker` · `Vercel`

</div>

---

## 📂 Other projects

<div align="center">

**[Census 2027 — Digital Enumeration Portal](https://github.com/AmanDadsena/Gen-AI-census)**
&nbsp;·&nbsp; **[🌐 Live](https://gen-ai-census.vercel.app)**

A self-serve web app for India's next census: walks a household through their own form, shows the phase schedule for every state and UT, answers common rumours from a published corpus that works with **no API key**, and does it all in **eight languages**. A Gemini key unlocks screenshot fact-checking and open-ended chat — everything else works offline by design.

`Next.js` · `TypeScript` · `FastAPI` · `Gemini`

</div>

---

## 🛠️ Tech I build with

<div align="center">

**Languages**

<img src="https://skillicons.dev/icons?i=ts,python,js,html,css" alt="Languages" />

**Frontend**

<img src="https://skillicons.dev/icons?i=nextjs,react,tailwind" alt="Frontend" />

**Backend & Data**

<img src="https://skillicons.dev/icons?i=fastapi,postgres,sqlite" alt="Backend" />

**Tools & Deployment**

<img src="https://skillicons.dev/icons?i=docker,git,github,vercel,vscode" alt="Tools" />

<br/>

<img src="https://img.shields.io/badge/Google_Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini" />
<img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama" />
<img src="https://img.shields.io/badge/shadcn/ui-000000?style=flat-square&logo=shadcnui&logoColor=white" alt="shadcn/ui" />
<img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white" alt="SQLAlchemy" />
<img src="https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white" alt="Pydantic" />
<img src="https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face" />

</div>

---

## 📊 GitHub Stats

<div align="center">

<img src="https://raw.githubusercontent.com/AmanDadsena/AmanDadsena/main/profile-summary-card-output/tokyonight/0-profile-details.svg" width="100%" alt="Profile details" />

<img width="49%" src="https://raw.githubusercontent.com/AmanDadsena/AmanDadsena/main/profile-summary-card-output/tokyonight/3-stats.svg" alt="Stats" />
<img width="49%" src="https://raw.githubusercontent.com/AmanDadsena/AmanDadsena/main/profile-summary-card-output/tokyonight/2-most-commit-language.svg" alt="Most commit language" />

<img width="49%" src="https://raw.githubusercontent.com/AmanDadsena/AmanDadsena/main/profile-summary-card-output/tokyonight/1-repos-per-language.svg" alt="Repos per language" />
<img width="49%" src="https://raw.githubusercontent.com/AmanDadsena/AmanDadsena/main/profile-summary-card-output/tokyonight/4-productive-time.svg" alt="Productive time" />

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=AmanDadsena&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=58A6FF&line=58A6FF&point=FFFFFF&area=true" width="100%" alt="Activity Graph" />

</div>

---

## 🧭 How I work

- **Measure the thing you're claiming.** If I say retrieval improved, there's an eval run that says by how much — and a cross-lingual split, because an English-dominated average hides the failure.
- **Make the fallback the honest path.** The extractive answer can't hallucinate a section number. Design so the degraded mode is the safe one.
- **Ship it, then polish it.** A deployed app with rough edges teaches more than a perfect one on localhost.
- **Write commits someone can read.** *"Stop the generator naming judges the corpus never mentions"* tells you what changed and why. `update` tells you nothing.

---

<div align="center">

### 💡 What's next

Growing the corpus — the ablation says English retrieval saturates around 74 passages while cross-lingual keeps improving to 152, which is an argument for **more coverage, not more tuning.**

<br/>

⭐ *If NyaySetu is useful to you, a star means a lot.*

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,2,5,30&height=120&section=footer" width="100%" alt="footer" />

</div>
