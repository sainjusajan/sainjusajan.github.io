# Selected projects — interview deck

A plain, 9-slide deck covering **VisualVocab**, **lendocli** and the **deployment tracker**.
One HTML file plus images, no build step.

## Viewing it

```bash
open index.html
```

`←` `→` to navigate · `F` for fullscreen · click to advance · swipe on touch.
The URL hash tracks the slide (`#4`), so you can deep-link and reload.

## Publishing to GitHub Pages

```bash
git init
git add .
git commit -m "Interview deck: selected projects"
gh repo create work --public --source=. --push
```

Then **Settings → Pages → Source: Deploy from a branch → `main` / `(root)`**.
Live at `https://sainjusajan.github.io/work/`.

Or copy the folder into your existing `sainjusajan.github.io` repo as a subdirectory.
`.nojekyll` is included so the files are served as-is.

## Slides

1. Title
2. Overview — all three projects in one table
3. VisualVocab — what it is, screenshots
4. VisualVocab — three identification modes, notable engineering
5. VisualVocab — what I built, business model
6. lendocli — the tool and my contribution
7. Deployment tracker — problem and approach
8. Stack
9. Thank you

## Before you present

**Slide 6 is deliberately scoped.** lendocli is a team tool — a colleague wrote 26 of the
30 commits. Your 4 are substantial (~1,100 lines: PR/CI annotation on deploy tags and the
rollback picker, plus per-account SSO role discovery), and the slide says exactly that.
Interviewers check, and a clean boundary reads better than ambiguity.

**The deployment tracker slide is built from its README and screenshot**, since no source
was in the folder. Worth sanity-checking the two claims you're most likely to be pressed on:
how status is derived, and that reads need no sign-in.

**Numbers, and where they came from:**

- VisualVocab: ~7.9k lines TS/Swift, 60 source files, 47 commits (app) + 17 (landing),
  3 edge functions, 5 tables, 6 RLS policies — all counted from the repos
- Performance figures (3.25 MB model, 15–24 fps, 20–40 ms) come from the project README
- IAP pricing from the in-app purchase screen
- lendocli: 5,158 lines of Go total, 30 commits, 4 yours

**Check the tracker screenshot before publishing publicly.** Names and avatars are blurred,
but repo names, Jira IDs and PR numbers are still legible, and it's an internal tool.

**Have the app on your phone.** Handing it over beats any slide about it.

## Assets

| File | Source |
| --- | --- |
| `assets/vv-home.png` | `visual-vocab-landing/public/screenshots/home.png` |
| `assets/vv-camera.png` | `visual-vocab-landing/public/screenshots/camera-detection.png` |
| `assets/vv-settings.png` | `visual-vocab-landing/public/screenshots/settings.png` |
| `assets/vv-language.png` | spare, unused |
| `assets/deployment-tracker.jpeg` | `deployment-tracker/deployment tracker.jpeg` |
