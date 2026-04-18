# BookBrain

BookBrain is a single-page web app for turning books into durable study material.

## What it does

- Upload a **PDF** or **EPUB** and extract text in-browser.
- Generate a structured **Memory Brief** (thesis, non-obvious ideas, confusion risks, action trigger, and recall points).
- Build study artifacts such as flashcards, confusion pairs, and transfer prompts.
- Run memory-focused study flows (retrieval, pre-test, confusion training, multiple-choice, and application drills).
- Track progress with local spaced-repetition state and memory notes.
- Use an optional Claude API key for extraction/coaching features.

## Architecture (current repo)

- Minimal repository with one main app file: `index.html`.
- App is client-side only (HTML/CSS/JS in one file).
- State is persisted in browser `localStorage`.

## Notes

- This is currently optimized for lightweight local usage and rapid iteration.
- API key storage is local to the browser profile used to run the app.
