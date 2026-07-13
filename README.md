# Case Study: AI-Generated Landing Page → Production Quality

## Before ##
<img width="1908" height="848" alt="image" src="https://github.com/user-attachments/assets/3369e973-e7c3-4593-9106-a7b78de72c8c" />

## After ##
<img width="1920" height="844" alt="image" src="https://github.com/user-attachments/assets/3ff93a45-217b-4ec9-a2fb-76175df9aefe" />


## case study ##
<img width="1920" height="727" alt="image" src="https://github.com/user-attachments/assets/c59e1daa-6d4f-45ab-9643-b579a12083b5" />
<img width="1704" height="572" alt="image" src="https://github.com/user-attachments/assets/975db388-a85f-4bb9-82b1-bb422839cfdb" />
<img width="1876" height="530" alt="image" src="https://github.com/user-attachments/assets/3800d2c8-4e12-4db8-90e5-84749e785635" />
<img width="1846" height="462" alt="image" src="https://github.com/user-attachments/assets/e93689aa-437c-49f5-8a1e-648ffbb276f6" />
<img width="1853" height="448" alt="image" src="https://github.com/user-attachments/assets/dccfa737-1190-4588-9c1f-8259d1852c84" />
<img width="1847" height="502" alt="image" src="https://github.com/user-attachments/assets/ca18f848-75bf-4f6e-8062-4296ce826d29" />
<img width="1890" height="717" alt="image" src="https://github.com/user-attachments/assets/eb5f56d7-7d53-45ba-9501-147f0de3a1b5" />



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

- `index.html`  the written case study with before/after code
- `ai-draft.html`  the untouched AI output
- `refactored.html`  my production refactor

**Live:** <https://ai-refactor-case-study-3bax.vercel.app/>

By [Faaiza Saand](https://github.com/FaaizaKarim) ·
[faaizasaand7@gmail.com](mailto:faaizasaand7@gmail.com)
