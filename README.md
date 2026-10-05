## Hi, I'm Alex

I study Economics and Math at UCLA, but most of what I actually do is build software. Specifically, I like building full-stack products that have a recommendation or ranking system doing the real work underneath. I usually end up doing the whole thing myself: the data model, the backend, the recommender math, and the frontend, and then actually shipping it so people can use it.

The common thread in what I build is taking messy real-world signals and turning them into a model that has to make a decision every single time someone opens the app. Which question to show next, which item to surface, how hard to make the next thing. That's the part I find most interesting, and it's the kind of work I want to do after I graduate.

A bit about me:

- UCLA, BA Economics with a Math minor. Most of my useful background is on the quant side: linear algebra, probability and Bayesian stats, econometrics.
- I've shipped real products, including one that's a live commercial platform with paying users.
- I'm looking for roles in machine learning and recommendation systems, and I build my own products on the side.

### What I work with

The languages I reach for most are Python, SQL, and TypeScript, plus R and SymPy when a project calls for it.

On the ML and recommendation side, I've built content-based and embedding retrieval (pgvector with approximate nearest neighbor), latent-factor models like IRT and Elo, online Bayesian updating, explore-vs-exploit logic, cold-start handling, and LLM-assisted pipelines for generating and tagging content.

For the backend I mostly live in Postgres and Supabase (row-level security, SQL functions, pgvector), designing the schema and the typed server-side APIs around it. On the frontend and infra side it's usually Next.js, React, Vercel, Stripe, and the OpenAI APIs.

My coursework covers econometrics and statistics, probability, linear algebra, and Bayesian inference, which is a lot of where the modeling instincts come from.

### Projects I'm proudest of

**Lodera** — live at [lodera.ai](https://lodera.ai)

Adaptive math test-prep that's actually in production with paying users. It's a question bank for standardized math where students practice against a huge pool of auto-generated, instantly graded questions, and the app keeps modeling what each student knows so it can serve the next best problem.

A few things that make it more than a quiz app:

- Every answer updates a latent-ability estimate through an IRT/Elo model. I report "mastery" as the difficulty a student clears about 80% of the time, not raw percent correct, and new topics run a quiet cold-start calibration so strong students skip the easy grind.
- The serving engine aims each question at the student's current ability, with diversity and priority logic so practice doesn't repeat or pile up on one idea.
- Content is a pipeline, not a static bank. Parametric templates expand into tens of thousands of unique, machine-graded questions, and each one gets auto-tagged to a learning taxonomy using embeddings plus an LLM judge.

Built with Next.js 15, React 19, and TypeScript on Vercel, backed by Supabase/Postgres (around 25 tables locked down with row-level security), a standalone Python and SymPy content pipeline, and Stripe for subscriptions. It's a commercial product so the source stays private, but the live site is the best way to see it.

**TrivTok** — live at [trivtok.vercel.app](https://trivtok.vercel.app), code at [github.com/alexvillagomez/trivtok](https://github.com/alexvillagomez/trivtok)

TikTok, except every swipe is a trivia question, and the feed learns two things at the same time: what you want to see and how hard to make it. This is the one I'd point to if you want to read actual recommender code, since it's public and I tried to keep it clean.

- It treats the feed as two separate problems: relevance (which topics to show, learned from likes and skips) and difficulty (how hard, learned from right and wrong answers). I keep those two signals from contaminating each other on purpose.
- Questions are embedded as vectors, so picking the next one is a pgvector nearest-neighbor lookup rather than a hand-maintained category tree.
- Difficulty is a Bayesian belief. An online IRT / AdPredictor-style model targets roughly a 70% chance you get the next question right, which is the range where it stays fun.
- The whole recommender runs inside Postgres as a single function call per swipe. There's also a pure-function TypeScript version that mirrors the SQL, with a parity test that checks the two agree to within 1e-9.

Built with Next.js, TypeScript, Supabase/Postgres with pgvector, and OpenAI embeddings.

**Bruin-Tutors** — live at [bruin-tutors.vercel.app](https://bruin-tutors.vercel.app), code at [github.com/alexvillagomez/Bruin-Tutors](https://github.com/alexvillagomez/Bruin-Tutors)

A tutoring service for UCLA students that I built and run. Students browse tutors, book sessions against real availability, and pay, and the whole thing runs without me having to coordinate anything by hand.

- Booking is backed by Google Calendar, so availability and scheduling stay in sync with real calendars and there are no double-bookings.
- Sign-in runs through NextAuth, payments through Stripe, and confirmation emails go out automatically with nodemailer.

Built with Next.js, TypeScript, Prisma, NextAuth, the Google Calendar API, and Stripe.

### Some other things I've built

- [CAPY](https://capy-six.vercel.app) is a capybara-themed café discovery app with pgvector semantic search and a little chatbot guide. It's a live demo.
- [function-builder](https://github.com/alexvillagomez/function-builder) is a Windows add-in that turns plain-English descriptions into real, working Excel functions.
- [booked](https://github.com/alexvillagomez/booked) does personalized book recommendations using vector search.

### Reach me

Best way to get in touch is email: alexvillagomez1@g.ucla.edu
