## Hi, I'm Alex

I study Economics and Math at UCLA. The thing I care about most, and what I want to be known for, is the algorithms behind recommendation and education: modeling what a person knows or wants, and deciding what to put in front of them next. Almost everything I build comes back to that problem.

I'm strongest in Python and SQL, which is also where most of that modeling and data work actually lives. On top of that I can take an idea, do the research to figure out how it should really work, and turn it into a product that ships and gets used. I've done that a few times now, and I've learned a lot about what it actually takes to launch something people depend on.

I also care about the business and product side, not just the code. I'm involved in the entrepreneurship community at UCLA, and when I build something I'm always thinking about whether it works as a product, not only whether it runs.

### What I focus on

Recommendation and education algorithms are the core of what I do:

- Latent-factor models for ability and difficulty (IRT and Elo), updated online as new answers come in
- Content-based and embedding retrieval with pgvector and approximate nearest neighbor
- Online Bayesian updating, explore-vs-exploit, cold-start handling, and adaptive difficulty targeting
- Turning all of that into systems that make a real decision on every single request: which question, which item, how hard

### Tools I use

Python and SQL are what I know best, and most of my algorithm and data work happens there, usually in Postgres and Supabase (SQL functions, pgvector, row-level security). I build and ship full products on top of that with Next.js, React, and TypeScript, deployed on Vercel, with Stripe and the OpenAI APIs where I need them. My coursework leans heavily on the quant side, which is where a lot of the modeling instincts come from: linear algebra, probability and Bayesian stats, and econometrics.

### Projects I'm proudest of

**Lodera** — live at [lodera.ai](https://lodera.ai), write-up at [github.com/alexvillagomez/lodera](https://github.com/alexvillagomez/lodera)

Adaptive math test-prep that's live in production and used by real students. It's a question bank for standardized math where students practice against a huge pool of auto-generated, instantly graded questions, and the app keeps modeling what each student knows so it can serve the next best problem. This is where a lot of my recommendation and education work comes together.

- Every answer updates a latent-ability estimate through an IRT/Elo model. I report "mastery" as the difficulty a student clears about 80% of the time, not raw percent correct, and new topics run a quiet cold-start calibration so strong students skip the easy grind.
- The serving engine aims each question at the student's current ability, with diversity and priority logic so practice doesn't repeat or pile up on one idea.
- Content is a pipeline, not a static bank. Parametric templates expand into tens of thousands of unique, machine-graded questions, each auto-tagged to a learning taxonomy using embeddings plus an LLM judge.

**TrivTok** — live at [trivtok.vercel.app](https://trivtok.vercel.app), code at [github.com/alexvillagomez/trivtok](https://github.com/alexvillagomez/trivtok)

TikTok, except every swipe is a trivia question, and the feed learns two things at once: what you want to see and how hard to make it. This is the one I'd point to if you want to read the actual recommender algorithms, since it's public and I kept it clean.

- It treats the feed as two separate problems: relevance (which topics, learned from likes and skips) and difficulty (how hard, learned from right and wrong answers), and keeps those signals from contaminating each other on purpose.
- Questions are embedded as vectors, so picking the next one is a pgvector nearest-neighbor lookup rather than a hand-maintained category tree.
- Difficulty is a Bayesian belief. An online IRT / AdPredictor-style model targets roughly a 70% chance you get the next question right.
- The whole recommender runs inside Postgres as one function call per swipe. There's also a pure-function TypeScript version mirroring the SQL, with a parity test that checks the two agree to within 1e-9.

**Bruin-Tutors** — live at [bruin-tutors.vercel.app](https://bruin-tutors.vercel.app), code at [github.com/alexvillagomez/Bruin-Tutors](https://github.com/alexvillagomez/Bruin-Tutors)

A tutoring service for UCLA students that I built and run end to end. Students browse tutors, book sessions against real Google Calendar availability, and pay through Stripe, with confirmation emails going out automatically. I built this because I was tutoring and wanted the scheduling and payments to just run themselves, which meant thinking about the whole thing as a product, not only the code.

### Some other things I've built

- I've helped Derek Shi build [booked](https://github.com/alexvillagomez/booked), a personalized book-recommendation app that uses vector search.
- [function-builder](https://github.com/alexvillagomez/function-builder) is a Windows add-in I made that turns plain-English descriptions into real, working Excel functions.

### Reach me

Best way to get in touch is email: alexvillagomez1@g.ucla.edu
