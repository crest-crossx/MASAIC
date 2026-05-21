# MASAIC Project Website

Official website for the MASAIC project: Modular Soft Adaptive Intelligent Component, part of the CROSS-X initiative.

## Overview

MASAIC focuses on research and development of intelligent robotic systems that integrate AI, large language models, sensing, control, and adaptive modular components.

The website presents the project overview, research teams, members, publications, news, seminars, collaborations, and sponsors.

## Project Structure

```text
MASAIC/
├── index.html              # Homepage
├── members.html            # Project members
├── publications.html       # Research publications
├── news.html               # News and updates
├── schedule.html           # Project schedule and milestones
├── seminar.html            # Seminar series page
├── collaboration.html      # Academic collaborators
├── sponsors.html           # Sponsors and partners
├── team-robotics.html      # Robotics: Design and Control/Learning team
├── team-ai.html            # AI and LLM Integration team
├── team-neuromorphic.html  # Neuromorphic Sensing team
├── team-vr-ar.html         # VR/AR and Imitation Learning team
├── styles.css              # Main stylesheet
├── script.js               # Main JavaScript
├── i18n.js                 # English/Japanese language switching
├── images/                 # Image assets
├── publication/            # Publication metadata
├── seminars/               # Seminar data and assets
│   ├── upcoming/           # Upcoming seminar entries
│   └── past/               # Past seminar entries
└── README.md               # This file
```

## Technology Stack

- Static website using HTML, CSS, and vanilla JavaScript
- No build process required
- JSON-based data for seminars and publications
- English/Japanese content switching through `i18n.js`
- Designed for GitHub Pages deployment

## Editing Content

### Main Website Content

Most content is edited directly in the HTML files. Look for page sections such as:

- Project introduction
- Research teams
- Member profiles
- Publications
- News items
- Contact information
- Sponsor and collaboration sections

Some older `TODO` comments may still exist in the source files and can be used as editing hints.

### Styling

The main style file is `styles.css`.

Theme colors are defined near the top of the file:

```css
:root {
    --primary-color: #6366f1;
    --secondary-color: #8b5cf6;
    --accent-color: #ec4899;
    --tertiary-color: #06b6d4;
}
```

Update these variables to change the overall visual theme.

### Images

Images are stored under `images/`, `news/`, `collaboration/`, and `seminars/`.

Recommended image guidelines:

- Use JPG or PNG for browser compatibility.
- Do not use HEIC files, because most browsers do not support them.
- Keep image paths case-sensitive for GitHub Pages.
- Compress large images before committing them.

## Local Development

Because this is a static site, you can open most HTML files directly in a browser.

However, pages that use `fetch()` to load JSON, such as `seminar.html` and `publications.html`, should be viewed through a local server:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Seminar Management

Seminar data is stored in:

```text
seminars/upcoming/seminars.json
seminars/past/seminars.json
```

### Adding a New Upcoming Seminar

1. Create a folder under `seminars/upcoming/` for the speaker or event.
2. Add the speaker photo and any PDF flyer if available.
3. Add a new entry to `seminars/upcoming/seminars.json`.
4. Confirm that `seminar.html` displays the new entry correctly through a local server.

Example JSON structure:

```json
{
  "id": "speaker-name-2026",
  "speaker": {
    "name": "Dr. Speaker Name",
    "title": "Position",
    "affiliation": "University or Institution",
    "website": "https://example.com",
    "photo": "seminars/upcoming/Speaker_Name/photo.png",
    "bio": "Speaker biography..."
  },
  "title": "Talk Title",
  "type": "Online Lecture",
  "date": "2026-03-23",
  "time": "13:00-14:30 JST",
  "location": "JAIST / Zoom",
  "abstract": "Talk abstract...",
  "pdfPath": "seminars/upcoming/Speaker_Name/talk.pdf"
}
```

### Moving a Seminar from Upcoming to Past

1. Move the speaker folder from `seminars/upcoming/` to `seminars/past/`.
2. Move the JSON entry from `upcoming/seminars.json` to `past/seminars.json`.
3. Update the date, time, location, PDF path, and YouTube URL if available.
4. Test `seminar.html` locally.

## Publication Management

Publication metadata is stored under:

```text
publication/paper1/info.json
publication/paper2/info.json
```

To add a new publication:

1. Create a new folder such as `publication/paper3/`.
2. Add an `info.json` file.
3. Update the publication folder list in `publications.html` if needed.

## Internationalization

The website supports English and Japanese.

Two approaches are used:

- `data-i18n` for short navigation and common text.
- `data-lang-content="en"` and `data-lang-content="ja"` for larger content blocks.

When adding new visible content, update both language versions where appropriate.

Related files:

- `i18n.js`
- `LANGUAGE_GUIDE.md`
- `JAPANESE_CONTENT_TEMPLATE.md`
- `QUICK_JAPANESE_SNIPPETS.md`

## Deployment to GitHub Pages

The project is intended to be deployed through GitHub Pages.

Basic workflow:

```bash
git add .
git commit -m "Update MASAIC website"
git push origin main
```

Then check the GitHub Pages URL after the deployment finishes.

## Notes

- This is not a Node.js project and does not require `npm install`.
- Keep all pages responsive across mobile, tablet, and desktop.
- Use consistent navigation and footer structure across pages.
- Keep academic and project information accurate and professional.
- Test pages that load JSON through a local server before publishing.

## License

License information has not been added yet.

## Contributors

Contributor information has not been added yet.
