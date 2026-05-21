# MASAIC Project Context

## Project Overview

MASAIC, Modular Soft Adaptive Intelligent Component, is a research project website under the CROSS-X initiative. The site presents research teams, members, publications, news, schedules, seminars, collaborators, and sponsors.

- Type: Static website
- Stack: HTML, CSS, vanilla JavaScript
- Deployment: GitHub Pages
- Site URL: `https://crest-crossx.github.io/MASAIC/`
- Repository: `https://github.com/crest-crossx/MASAIC.git`

## Architecture

```text
MASAIC/
├── index.html
├── members.html
├── publications.html
├── news.html
├── schedule.html
├── seminar.html
├── collaboration.html
├── sponsors.html
├── team-robotics.html
├── team-ai.html
├── team-neuromorphic.html
├── team-vr-ar.html
├── styles.css
├── script.js
├── i18n.js
├── images/
├── publication/
└── seminars/
```

## Development Notes

- There is no build process.
- Use a local server when testing pages that load JSON through `fetch()`.
- Keep paths case-sensitive for GitHub Pages.
- Use JPG or PNG images; avoid HEIC.
- Keep content professional and suitable for an academic research project.

## Local Testing

```bash
python -m http.server 8000
```

Open:

```text
http://localhost:8000
```

## Internationalization

The site uses English/Japanese language switching:

- `data-i18n` for short reusable strings.
- `data-lang-content="en"` and `data-lang-content="ja"` for larger blocks.
- Language state is stored in `localStorage`.

When adding visible content, update both language versions when appropriate.

## Seminar Data

Seminar data lives in:

```text
seminars/upcoming/seminars.json
seminars/past/seminars.json
```

Speaker photos and PDFs should be stored in the corresponding seminar folder.

## Publication Data

Publication data lives in:

```text
publication/paper1/info.json
publication/paper2/info.json
```

When adding new publication folders, update the folder list in `publications.html`.

## Deployment

Push changes to `main`:

```bash
git add .
git commit -m "Describe the update"
git push origin main
```

GitHub Pages deploys automatically from the repository root.
