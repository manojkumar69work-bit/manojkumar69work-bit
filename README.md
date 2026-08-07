# Manoj Kumar Ethini

**Third-year CSE student who ships.** Full-stack products running in production on free tiers — FastAPI + PostgreSQL backends, Next.js frontends, LLM and speech pipelines. Python-first.

Currently a software development intern on my college's live ERP, used daily by students and faculty.

📍 Hyderabad, India · 📧 [manojkumar69.work@gmail.com](mailto:manojkumar69.work@gmail.com)

---

## Things I've built and shipped

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

The pipeline fails over automatically across AI providers, so a single outage or rate limit can't stall the feed. A background scraper runs every 30 minutes with fuzzy deduplication and auto-pruning to stay inside free-tier storage. Along the way: fixed a connection-pool race condition, and added per-IP rate limiting, CSP headers, and a React error boundary.

**→ [Live](https://truthvortex-sigma.vercel.app)** · [Code](https://github.com/manojkumar69work-bit/truthvortex)

---

### ☎️ Multi-lingual Voice Agent — configurable real-time AI phone agent
`Python` `FastAPI` `WebRTC` `Sarvam AI` `Twilio` `Docker`

A multi-tenant voice platform handling real-time calls in Telugu and mixed Hindi/English. Point it at a new domain — support, sales, surveys, lead capture — by swapping the prompt and extraction schema; no code changes. Shipped configured for real-estate lead capture.

Latency is the whole product, so: sentence-level TTS streaming, barge-in via Silero VAD at 0.4 s endpointing, and a Hindi language hint on ASR that transcribes code-switched speech far better than autodetect. Lead extraction runs *mid-call* — once name and contact exist the lead auto-submits, so it survives even if the caller hangs up early.

Each organisation is isolated: its own prompt, language, persona, minute quota, and login, with no cross-tenant access to calls or recordings.

[Code](https://github.com/manojkumar69work-bit/Multi-lingual-Voice-Agents)

---

## Work

**Software Development Intern** · MLR Institute of Technology · *Jul 2026 – present*

Building **Campus Hub**, the college's ERP — Next.js + Supabase, team of 6, live and used daily.

I own features end to end: requirements, schema and SQL, API layer, UI, release. Delivered the HR and attendance workflows for the faculty portal, from payroll-affecting policy rules in the data layer through to the dashboards staff actually work out of. Integrated third-party biometric data and reconciled it against existing faculty records. Led the mobile experience across both portals, consolidating duplicated flows into shared components.

---

## Stack

**Languages** · Python · Java · SQL · TypeScript / JavaScript · C

**Backend** · FastAPI · REST API design · PostgreSQL · Supabase · JWT auth · rate limiting · webhooks · cron jobs

**Frontend** · Next.js 15/16 (App Router) · React 19 · Tailwind · shadcn/ui

**AI/ML** · LLM API integration · multi-provider fallback pipelines · prompt design · speech-to-text / TTS · scikit-learn

**Infra** · Docker · Render · Vercel · Railway · Firebase · Git · Linux

---

## Also

- **Quantitative Research Job Simulation** — JPMorgan Chase & Co. (Forage), Jan 2026 · price-data analysis, commodity storage contract pricing, credit-risk modelling, FICO bucketing — in Python
- **Cloud Computing** — NPTEL/SWAYAM (IIT), Elite grade 71/100, Apr 2026

---

<sub>Graduating 2028 · open to internships and full-time roles in backend and AI engineering</sub>
