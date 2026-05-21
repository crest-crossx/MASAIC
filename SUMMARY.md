# MASAIC Website Summary

## Current Status

The MASAIC website is a static HTML/CSS/JavaScript site deployed through GitHub Pages:

```text
https://crest-crossx.github.io/MASAIC/
```

The repository is hosted at:

```text
https://github.com/crest-crossx/MASAIC.git
```

## Completed Work

- Static site structure is in place.
- Main pages are available: home, members, publications, news, schedule, seminars, collaboration, sponsors, and team pages.
- English/Japanese language switching is implemented with `i18n.js`.
- Seminar data is loaded from JSON files.
- Publication data is loaded from JSON files.
- Main image paths have been checked for GitHub Pages compatibility.
- README has been rewritten in English.

## Important Files

- `index.html`: Homepage
- `seminar.html`: Seminar series page
- `publications.html`: Publications page
- `members.html`: Member listing
- `styles.css`: Main styles
- `script.js`: Shared page behavior
- `i18n.js`: Language switching
- `seminars/upcoming/seminars.json`: Upcoming seminars
- `seminars/past/seminars.json`: Past seminars
- `publication/*/info.json`: Publication metadata

## Local Testing

Use a local server for pages that fetch JSON:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Deployment

GitHub Pages deploys from the `main` branch root. After updates:

```bash
git add .
git commit -m "Describe the update"
git push origin main
```

The site should update automatically after GitHub Pages finishes deploying.
