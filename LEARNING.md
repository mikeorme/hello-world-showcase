# Learning with this repo

Each page is small enough to read top to bottom. Open it in the browser, then open its source (right-click → View Source) and find the things listed below.

## Page → concept map

| Page | Concepts to find in the source |
|------|--------------------------------|
| `index.html` | **Progressive enhancement**: scroll-driven CSS animation (`animation-timeline: view()`) with an IntersectionObserver fallback. **Container queries** and `:has()`. **Lazy iframes** that load only when scrolled into view and unload after. `prefers-reduced-motion` honored. |
| `hello-original.html` | **WebGL**: a fragment shader (the `x-shader/x-fragment` script) draws the animated background on the GPU. `requestAnimationFrame` loop. **Pointer events** move the glow and fatten nearby letters via variable-font weight. `prefers-reduced-motion` honored. Graceful fallback when WebGL is missing. |
| `hello-dev-poster.html` | **DOM events**: `addEventListener` on buttons, `classList` to toggle styles, `querySelector` to find elements. A `@media` query for responsive layout. |
| `hello-farah-landing.html` | **CSS Grid** (`grid-template…`), inline **SVG**, **`localStorage`** (state that survives a page reload), `setTimeout`. |
| `hello-priya-greeting.html` | **Timers**: `setInterval` cycles greetings. SVG, `classList`, and a `@media` query. |
| `hello-sam-repl.html` | **Parsing input and printing output**, the heart of a REPL (read, evaluate, print, loop). CSS `@keyframes` animation. A cancel counter (`cancelToken`) that stops stale animations: a small taste of async bugs. |
| `hello-voice-utterance.html` | **Browser APIs**: the Web Speech API (`speechSynthesis`) says the greeting aloud. Form `<input>`. Always feature-check APIs like this. |

Suggested first exercise: change the greeting text in one page, reload, and see it change. Then break something on purpose and open DevTools (⌥⌘I) to see the error.

## Git workflow cheat sheet

The loop you'll repeat for every change:

```bash
git switch main && git pull          # start from the latest main
git switch -c my-change              # branch: a safe place to experiment
# ...edit files...
git status                           # what changed?
git diff                             # exactly what changed?
git add <file>                       # stage it
git commit -m "Say what and why"     # save a snapshot
git push -u origin my-change         # upload the branch
gh pr create --fill                  # open a pull request
# review on github.com, click Merge, then:
git switch main && git pull          # bring the merged change home
```

**Why branches and pull requests?** `main` is what the world sees. A branch lets you try things without affecting it, and a pull request is where changes get reviewed (even by yourself) before going live. Real teams work this way, and so should you.

## Words you'll meet

- **Repository (repo):** the project folder plus its full history.
- **Commit:** a saved snapshot with a message.
- **Branch:** an independent line of commits.
- **Pull request (PR):** a proposal to merge one branch into another.
- **Remote / origin:** the copy of the repo on GitHub.
- **Deploy:** making a change live. Here, merging to `main` deploys it automatically.
