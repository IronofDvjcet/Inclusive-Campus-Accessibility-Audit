# Inclusive Campus Accessibility Audit

A web system that measures how accessible each college is for students with disabilities, and tracks whether the problems it finds are actually fixed.

## Features

- Digital inspection checklists with weighted scoring (critical 3, major 2, minor 1)
- Photo evidence on findings and on re-inspections
- Accessible-route map with a step-free route test from the main gate
- Ramp, lift and path status; accessible toilet features; assistive technology inventory
- Corrective actions with deadlines: 30 days critical, 60 major, 90 minor
- Fix verification: a fix reported by a college counts only after an auditor re-inspects it. Failed re-inspections reopen the action with a new deadline.
- Department-wide and college-wide reports, with CSV and text export
- Light, dark and larger-text modes

## Run it

No build step. Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8000
```

To publish on GitHub Pages: push these files to a repository, then go to Settings, Pages, and select the main branch.

## Data

- Six sample colleges carry made-up scores and problems so the tool can be tried. They are labelled as samples in the app.
- 24 real college names are listed with no inspection results.
- Records and photos are saved in the browser's local storage, so they stay on one device. Sharing data across a department needs a backend database.
- Sample data is defined in `SEEDC`, and the real college list in `REAL`, near the top of `app.js`. The "Reset to sample data" button restores both.

## Files

- `index.html` page structure
- `styles.css` design tokens, layout, light and dark themes
- `app.js` data, scoring, views and events

## Note on the checklist

Checklist wording follows commonly used access criteria such as a 1:12 ramp gradient and 900 mm door width. Check each item against the current UGC guidance for higher education institutions and the Harmonised Guidelines under the Rights of Persons with Disabilities Act, 2016 before formal use.
