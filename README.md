# Case Study: AI-Generated Landing Page → Production Quality

![Case study page](screenshot.png)

A real, verifiable demonstration of my AI + human frontend workflow.
I asked an AI tool to generate a complete SaaS landing page, measured it
with Chrome Lighthouse, refactored it to production standards, and
measured again. Both files are in this repo — run Lighthouse yourself
to reproduce the results.

## Measured results (Chrome Lighthouse, mobile emulation)

| Category       | Before (`ai-draft.html`) | After (`refactored.html`) |
| -------------- | :----------------------: | :-----------------------: |
| Performance    | 88                       | **96**                    |
| Accessibility  | 62                       | **100**                   |
| Best Practices | 100                      | **100**                   |
| SEO            | 82                       | **100**                   |

## What the AI draft contained (before)

- Layout built desktop-first, breaking at mobile widths
- Non-semantic markup: generic `div` elements doing the job of nav,
  headings, and buttons
- Insufficient color contrast on key text (main accessibility failure)
- Missing form labels and image alt text
- Incomplete SEO metadata: no meta description, no Open Graph tags,
  no canonical URL
- Unoptimized, render-blocking asset loading
- Form UI with no working submit handling or validation

## What I changed (after)

- Rebuilt the layout mobile-first with fluid, responsive containers
- Replaced div soup with semantic HTML: `nav`, `header`, `main`,
  `section`, proper `h1`–`h3` hierarchy, real links and buttons
- Fixed color contrast to meet WCAG AA
- Added labels to every form field and descriptive alt text to images
- Added full SEO metadata: title, description, Open Graph, canonical
- Optimized loading: reduced font weights, `display=swap`, preconnect,
  `loading="lazy"` on below-fold images, explicit image dimensions to
  prevent layout shift
- Wired the form with native validation, autocomplete, and a real
  POST endpoint pattern

## Reproduce it

1. Clone the repo, open `ai-draft.html` in Chrome
2. DevTools → Lighthouse → Mobile → Analyze
3. Repeat for `refactored.html` and compare

## Files

- `index.html` — the written case study with before/after code
- `ai-draft.html` — the untouched AI output
- `refactored.html` — my production refactor

**Live:** <add Vercel URL>

By [Faaiza Saand](https://github.com/FaaizaKarim) ·
[faaizasaand7@gmail.com](mailto:faaizasaand7@gmail.com)
