## Hi, I'm Alex 👋

I build full-stack products end to end. My main work is **Lodera** — a live, commercial adaptive-learning platform I designed, built, and ship to production myself.

---

## 🎓 Lodera — adaptive math test-prep, in production

A smart question bank for standardized-math prep. Students pick topics and practice against a near-unlimited pool of auto-generated, instantly graded questions, while the app continuously models what they know and serves the next best problem.

**Live courses:** AP Calculus AB · Precalculus · SAT Math · plus **Challenge**, a cross-subject Elo puzzle arena.

### Why it's more than a quiz app

🧠 **A real mastery model** — every answer updates a latent-ability (θ) estimate through an IRT/Elo model. "Mastery" is reported as the difficulty a student clears ~80% of the time, not raw percent-correct. Brand-new topics run an invisible cold-start calibration so strong students skip the easy grind.

⚙️ **Adaptive serving** — a serving engine targets each question to the student's current ability, with diversity and priority logic so practice never repeats or clusters on one idea.

🏭 **A content _pipeline_, not a static bank** — parametric templates expand into tens of thousands of unique, machine-graded questions with misconception-based distractors. Each item is auto-tagged against a learning taxonomy using embeddings plus an LLM judge, so content scales without hand-writing every question.

🏆 **Challenge arena** — a two-sided Elo system rates hand-curated puzzles across 11 subjects (statistics, linear algebra, discrete math, geometry, and more), recalibrating difficulty from real play.

### Stack

![Next.js 15](https://img.shields.io/badge/Next.js_15-000000?logo=nextdotjs&logoColor=white)
![React 19](https://img.shields.io/badge/React_19-20232A?logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?logo=supabase&logoColor=white)
![Postgres](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?logo=stripe&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)

**Next.js 15 · React 19 · TypeScript** on Vercel (push-to-`main` continuous deploy) · **Supabase / Postgres** (~25 tables, locked down with row-level security — all data access flows through typed server-side API routes) · a standalone **Python + SymPy** content pipeline for authoring, generation, tagging, and import · **Supabase Auth** + **Stripe** subscriptions with a free daily tier and a 7-day trial.

> Lodera is a commercial product, so its source stays private — this page is the technical overview.

---

## 🛠️ Selected other work

- **[function-builder](https://github.com/alexvillagomez/function-builder)** — AI-built Excel functions from plain-English descriptions.
- **[booked](https://github.com/alexvillagomez/booked)** — personalized book recommendations powered by vector search.
- **[Bruin-Tutors](https://github.com/alexvillagomez/Bruin-Tutors)** — a tutoring platform for UCLA students with custom booking and scheduling.
