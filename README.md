# Manoj Kumar 

**Third-year CSE student who ships.** Full-stack products running in production on free tiers — FastAPI + PostgreSQL backends, Next.js frontends, LLM and speech pipelines. Python-first.

📍 Hyderabad, India · 📧 [manojkumar69.work@gmail.com](mailto:manojkumar69.work@gmail.com)

---

## 🚀 Projects

### 🎓 [BunkMax](https://bunk-max.vercel.app) — attendance tracker with automated ERP sync
`Python` `FastAPI` `PostgreSQL` `Next.js` `Razorpay` · **live**

Tells students exactly how many classes they can afford to miss. 30+ REST endpoints, scheduled push-notification cron jobs, subscription billing.

The interesting part: the college ERP has no public API, so I decoded its shipped JS bundles — base64 payloads, a nested session cookie, `Origin`/`Referer` guards — to pull subject-wise attendance in one tap. When the college replaced the portal mid-project, I migrated the integration behind an unchanged client interface, so one login now imports both attendance *and* timetable.

Stored ERP credentials are Fernet-encrypted for daily automated re-sync. Razorpay orders with signature-verified webhooks. Tuned to survive Render's free tier — single uvicorn worker, DB pool capped under the pooler budget, health keep-warm ping.

**→ [Live](https://bunk-max.vercel.app)** · [Code](https://github.com/manojkumar69work-bit/BunkMax)

---

### 📰 [TruthVortex](https://truthvortex-sigma.vercel.app) — AI Telugu news aggregator
`FastAPI` `PostgreSQL` `Next.js` `Multi-provider LLM` · **live**

Scrapes ~30 RSS sources across 5 categories and summarizes each article into 5–8 line Telugu summaries.

The pipeline fails over automatically across four AI providers, so a single outage or rate limit can't stall the feed. A background scraper runs every 30 minutes with fuzzy deduplication and auto-pruning to stay inside free-tier storage. Along the way: fixed a connection-pool race condition, and added per-IP rate limiting, CSP headers, and a React error boundary.

**→ [Live](https://truthvortex-sigma.vercel.app)** · [Code](https://github.com/manojkumar69work-bit/truthvortex)

---

### ☎️ [Multi-lingual Voice Agent](https://github.com/manojkumar69work-bit/Multi-lingual-Voice-Agents) — real-time AI phone agent
`Python` `LiveKit / WebRTC` `Groq` `Sarvam AI` `Docker`

A multi-tenant voice platform handling real-time calls in Telugu and mixed Hindi/English. Point it at a new domain — support, sales, surveys, lead capture — by swapping the prompt and extraction schema; no code changes. Shipped configured for real-estate lead capture.

Latency is the whole product, so: sentence-level TTS streaming, barge-in via Silero VAD at 0.4 s endpointing, and a Hindi language hint on ASR that transcribes code-switched speech far better than autodetect. Lead extraction runs *mid-call* — once name and contact exist the lead auto-submits, so it survives even if the caller hangs up early.

Each organisation is isolated: its own prompt, language, persona, minute quota, and login, with no cross-tenant access to calls or recordings.

[Code](https://github.com/manojkumar69work-bit/Multi-lingual-Voice-Agents)

---

## 💻 Tech Stack

**Languages**

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white)
![SQL](https://img.shields.io/badge/sql-%23025E8C.svg?style=for-the-badge&logo=amazon-dynamodb&logoColor=white)

**Backend**

![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/postgresql-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)

**Frontend**

![Next.js](https://img.shields.io/badge/Next-black?style=for-the-badge&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)

**AI / ML**

![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)

**Infra & Tools**

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Render-%2346E3B7.svg?style=for-the-badge&logo=render&logoColor=black)
![Railway](https://img.shields.io/badge/Railway-%230B0D0E.svg?style=for-the-badge&logo=railway&logoColor=white)
![Firebase](https://img.shields.io/badge/firebase-%23039BE5.svg?style=for-the-badge&logo=firebase&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

---

<sub>Graduating 2028 · open to internships and full-time roles in backend and AI engineering</sub>
