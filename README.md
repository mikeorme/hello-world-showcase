# hello-world-showcase

Six small, standalone "Hello, World" web pages, each taking the classic first program in a different direction. No build step, no dependencies: every page is a single HTML file.

**Live site:** https://mikeorme.github.io/hello-world-showcase/

| Page | What it is |
|------|------------|
| [index.html](index.html) | Full-screen WebGL background with a headline whose letters swell as the cursor nears |
| [hello-dev-poster.html](hello-dev-poster.html) | "No. 01" poster |
| [hello-farah-landing.html](hello-farah-landing.html) | Product-style landing page |
| [hello-priya-greeting.html](hello-priya-greeting.html) | Hello in many languages |
| [hello-sam-repl.html](hello-sam-repl.html) | A tiny REPL |
| [hello-voice-utterance.html](hello-voice-utterance.html) | Hello, spoken aloud |

This repo is also a sandbox for learning how modern software gets built and shipped. See [LEARNING.md](LEARNING.md).

## Run it locally

Open any `.html` file in a browser. Or serve the folder:

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

## How it's hosted

GitHub Pages serves the `main` branch from the repo root. Merging to `main` redeploys the site, usually within a minute.
