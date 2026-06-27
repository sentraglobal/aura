You are building a web-based personality audit game called AURA for Indian college students. Build this in 3 phases. Do NOT hardcode any questions — I will provide them separately. Use a questions array that is easy to fill later.

---

PHASE 1 — Foundation & UI Shell

Build the complete HTML/CSS/JS structure with:
- A dark themed UI (deep black background #0a0a0a, neon accent color #7C3AED purple or #00F5FF cyan — pick one and stay consistent)
- Smooth entrance animation on load
- Intro screen with: AURA logo/title, one-line tagline ("Find out who you actually are"), and a START button
- Name input screen: user types their name, hits continue
- Question screen layout: progress bar on top, question number, question text, 4 option buttons (A/B/C/D) — no scoring visible
- Mobile first — everything must look good on a phone screen (max-width 430px centered)
- Smooth slide/fade transition between every screen
- No backend needed — pure HTML CSS JS single file

---

PHASE 2 — Question Engine & Scoring Logic

Build the full quiz engine:
- Questions will be loaded from a JS array called `questions` — each object has: { question, options: [A, B, C, D], scores: [scoreA, scoreB, scoreC, scoreD], category: "EQ" | "Decision" | "Social" | "Ambition" | "Awareness" }
- On each answer: store the score for that question's category silently
- Progress bar fills as questions are answered
- Auto advance to next question after option is selected (300ms delay with selected state animation)
- Track 5 category scores separately
- After last question, calculate: each category score as percentage, overall AURA score as average of all 5
- Determine personality label based on top 2 scoring categories

PERSONALITY LABELS:
- High EQ + High Awareness → The Silent Observer
- High Ambition + High Decision → The Chaos Executor
- High Social + High EQ → The Magnetic Connector
- High Awareness + High Decision → The Cold Strategist
- High Ambition + High Social → The Loud Visionary
- High EQ + High Decision → The Calculated Empath
- All balanced → The Rare All-Rounder
- Low in 3+ dimensions → The Uncharted One

---

PHASE 3 — Results Screen & Share

Build the results screen:
- Dramatic reveal animation — AURA score counts up from 0 to final number
- Show personality label with a short 2-line description of that type
- Show 5 dimension bars with labels (EQ, Decision, Social, Ambition, Awareness) — animated fill
- Show 2 strengths and 1 blind spot based on highest and lowest scoring category
- A "Share Your AURA" button that generates a shareable text card like:
  "I scored 74 on AURA. I am The Chaos Executor. Take the test: [link]"
- A "Retake" button that resets everything back to intro screen
- Make the results screen feel premium — like an identity reveal, not a school result

---

GENERAL RULES:
- Single HTML file, no frameworks, no libraries except vanilla JS
- All screens in one file, shown/hidden with JS
- Mobile first, max-width 430px, centered on desktop
- Dark theme throughout, consistent design language
- Smooth animations on everything — this should feel like a premium app not a quiz website
- Add placeholder dummy questions array with 3 sample questions so the engine works and can be tested — I will replace with real 100 questions later
- Comment every major section clearly so I know where to paste real questions
