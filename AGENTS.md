# AGENTS.md
# DR Copy Fluency Coach — Codex Operating Instructions

## Mission

You are building and improving a private training app for one user only.

This is **not** a public SaaS.
This is **not** a generic AI copy tool.
This is **not** a decorative prototype.

This app exists for one purpose:

**Help the user become extremely skilled at direct-response copywriting as fast as possible through guided learning, memory retention, deliberate practice, applied writing, critique, repetition, and correction.**

---

## Product Standard

Every change must support this outcome:

- learn a principle
- remember it
- apply it in writing
- get corrected
- improve over time
- develop serious daily habit strength

If a feature does not clearly help this outcome, do not prioritize it.

---

## What This App Is

Treat the app as:

- a private DR copy mastery system
- a memory and application trainer
- a cohesive “copy brain” built from elite copywriters
- a serious daily practice engine

Do **not** treat it as:

- a reading repository
- a random AI playground
- a decorative dashboard
- a passive content browser

---

## Core Product Requirements

The app must support all of the following:

1. The user can choose a copywriting master.
2. The user can choose a principle or teaching under that master.
3. The app generates a session from that choice.
4. The app teaches the principle clearly.
5. The app tests recall and understanding.
6. The app forces written application.
7. The AI critiques the user’s writing precisely.
8. The app detects weakness or misunderstanding.
9. If the user gets something wrong, the app assigns a follow-up learning path.
10. The app stores scores, dates, history, weak areas, and progress over time.
11. Streaks and habit tracking are based on real completed sessions.
12. Progression is based on demonstrated understanding, not just clicks.

---

## Primary Product Philosophy

This app is for accelerated mastery.

That means the app should emphasize:

- active recall
- spaced reinforcement
- teach-back in the user’s own words
- applied writing
- critique and revision
- deliberate practice
- pass/retry logic
- weak area diagnosis
- follow-up drills

The app should reduce passive consumption and increase active cognitive effort.

---

## Mandatory Writing Rule

Every meaningful session must require the user to write copy.

Not optional.
Not only multiple-choice.
Not only reading.

The user must produce written output that applies the principle being learned.

---

## AI Requirement

AI must be used as an integrated coaching layer, not as a bolt-on chatbot.

Use AI for:

- critique
- scoring
- reflection analysis
- diagnosis
- next drill assignment
- explanation of weak areas
- principle clarification

AI feedback must be:

- precise
- grounded in DR principles
- corrective
- useful
- specific

Avoid:

- generic praise
- vague encouragement
- surface-level commentary

---

## Masters and Knowledge Base

The master/principle system must include, at minimum:

- John Caples
- Eugene Schwartz
- Robert Collier
- Gary Halbert
- Joe Sugarman
- Claude Hopkins
- Dan Kennedy
- David Ogilvy
- Gary Bencivenga
- John Forde / Michael Masterson
- Rory Sutherland

Each master should have:

- principles
- teachings
- practical application patterns
- examples where useful
- usable session content

---

## How to Judge Features

Before implementing or preserving any feature, ask:

1. Does this help the user learn a principle?
2. Does this help the user remember it?
3. Does this force application?
4. Does this improve feedback or correction?
5. Does this strengthen repetition or habit?

If the answer is mostly no, it is low priority.

---

## Behaviour Rules for Codex

1. Do not make fake UI.
   If something looks interactive, it should work.

2. Do not add decorative features before fixing learning logic.

3. Do not hardcode fake progress, fake streaks, fake demo stats, or fake completion data in live behavior.

4. Do not leave important flows half-built.

5. Prefer functional learning loops over visual polish.

6. Before changing code, inspect how the current logic actually works.

7. When a feature is broken, explain the root cause, not just the symptom.

8. When adding a feature, wire it into shared state and real user flow.

9. Keep the app coherent.
   Do not create disconnected tools or feature islands.

10. Keep changes minimal when possible, but do not preserve bad architecture just for the sake of tiny edits.

11. Treat misleading interface behavior as a bug.

12. If something is visually impressive but educationally useless, deprioritize it.

---

## Truthfulness Rules

The app must tell the truth.

That means:

- no fake streaks
- no fake history
- no fake readiness
- no fake “next drill” assignment unless it is actually stored and used
- no fake progress bars disconnected from real state
- no fake selector UI that does nothing
- no fake “Apply” actions that only show a toast or navigate without changing state

If a feature appears real but is not functionally real, flag it as:

**FAKE UI**

---

## Data Integrity Rules

Progress data must be real and reliable.

Check and protect:

- dates
- session logs
- scores
- streaks
- completion history
- weak area history
- competence ratings
- master/principle selections
- remediation queue

Do not seed fake progress in live behavior.
If demo data is needed, isolate it clearly and keep it separate from real user data.

---

## Product Reality Checks

The app is not functional enough unless all of these are true:

- the user can choose a master
- the user can choose a principle
- the session changes based on that choice
- the app requires writing
- the app critiques the writing
- the app stores results
- wrong answers trigger a real follow-up path
- progress history reflects real activity

---

## Before Coding

Before implementing anything substantial, always do this:

1. Restate the requested outcome in plain English.
2. Identify which parts of the app are involved.
3. Say whether the current implementation is:
   - real
   - partial
   - fake/misleading
   - broken
4. Propose the smallest sound fix.
5. Mention risk level.

---

## After Coding

After making changes, always report:

1. What changed
2. Why it changed
3. What user outcome it now supports
4. What still remains broken or incomplete
5. What should be tested manually

---

## Bug Analysis Standard

When asked to debug, do not just search for syntax errors.

Also analyze:

- broken product logic
- missing state wiring
- fake session flows
- misleading progress indicators
- incorrect persistence
- incomplete remediation logic
- UI that implies functionality that does not exist
- hardcoded educational content where dynamic principle-driven logic is required

---

## Testing Standard

If tests or validation scripts exist, run them.
If not, perform best-effort functional verification of the changed flow.

For this app, functional verification should usually include:

- selecting a master
- selecting a principle
- generating a session from that selection
- running a session
- submitting answers
- receiving scoring
- getting critique
- saving progress
- reloading state
- checking dates/logging
- checking follow-up pathway behavior

---

## Priority Order

When tradeoffs are needed, prioritize in this order:

1. Daily practice flow
2. Master/principle selection
3. Memory retention and remediation logic
4. Writing + critique + revision loop
5. Real score/history/streak persistence
6. AI integration quality
7. Progress visibility
8. Visual polish

---

## Current Known Priorities

These are likely the most important near-term implementation priorities unless the code proves otherwise:

1. Fix any parser/runtime errors so the app boots cleanly.
2. Remove fake seeded streak/history/demo progress from live behavior.
3. Make Daily Practice genuinely selectable by master and principle.
4. Replace hardcoded session content with principle-driven templates.
5. Persist next drill/remediation into real state.
6. Expand the master database to the full required set.
7. Make competence tracking reflect actual skill areas, not just one partial metric.

---

## Repo-Specific Rules

- Do not rewrite the whole app unless explicitly asked.
- Prefer fixing broken flows before adding new tabs.
- Flag any hardcoded session data that should be migrated to a reusable master/principle database.
- Flag any seeded demo streak or fake progress logic immediately.
- Treat misleading interface behavior as a bug.
- Do not add calendar, notifications, or reward systems before the truthful learning loop works.
- Do not add advanced polish before Daily Practice is real.

---

## Final Instruction

Build for actual mastery, not appearance.

If something is visually polished but does not improve learning, retention, application, or habit strength, it is low priority.
