# Mind Bloom Showcase — Screenshot Placement Guide

This guide is for Claude Code working with the real Mind Bloom application repo. Do not replace placeholders with fabricated screenshots or renderings. Use real captures from the working application with test/demo data. Remove any private data, session tokens, real user contact details, or confidential admin records. Capture desktop images at a consistent width (ideally 1440px), crop away browser extensions and OS chrome, and compress WebP/PNG for web.

## Capture list and exact intended placement

| Asset file (suggested) | What it should show | Where it goes | Priority |
| --- | --- | --- | --- |
| `assets/screenshots/home.webp` | Public Mind Bloom homepage, with branding and primary call to action clearly visible | Primary/first image in Gallery for all three concepts; optionally hero product mockup in Concept 1 | Essential |
| `assets/screenshots/events.webp` | Events browsing page, preferably showing event cards and filters or calendar | Second Gallery image; beside feature description of discovering events | Essential |
| `assets/screenshots/registration.webp` | Signed-in event details or RSVP/registration form, using fictitious attendee data | Third Gallery image; beside event registration feature | Essential |
| `assets/screenshots/resources.webp` | Resource library with a few resource cards visible | Fourth Gallery image; resource library feature | Essential |
| `assets/screenshots/user-dashboard.webp` | Signed-in attendee dashboard with safe sample records | Optional fifth Gallery image or product story section | Recommended |
| `assets/screenshots/admin-dashboard.webp` | Admin overview or events management, using demo records only | Optional sixth Gallery image under Behind the Build / Admin tools | Recommended |
| `assets/screenshots/donations.webp` | Donation page showing the Zeffy link/action; avoid real donor/payment data | Optional screenshot near donation/payment feature | Optional |
| `assets/screenshots/languages.webp` | Language selector or a translated page, if working and verified | Optional supporting image for multilingual access | Optional |

## Layout-specific instructions

### 01-bloom (welcoming)
- Keep the existing four Gallery cards as the initial screenshot locations. Use `home.webp`, `events.webp`, `registration.webp`, and `resources.webp` in that order.
- If adding a hero image, use `home.webp` inside a browser-window mockup aligned with the hero copy. Never obscure prominent navigation or the product's main title.
- Give images soft rounded corners, restrained shadows, and captions describing the task a visitor can accomplish.

### 02-built-to-bloom (tech-focused)
- Use the same four starting Gallery positions, but make `events.webp` and `registration.webp` visually prominent (the product flow is the story).
- If adding interaction, support click-to-enlarge using accessible buttons and keyboard focus; never depend on hover alone.
- Put `admin-dashboard.webp` in an optional engineering/admin feature card, with a caption about management workflows only if confirmed in the codebase.

### 03-mindbloom-story (editorial)
- Use `home.webp` in the first Gallery slot and the remaining three starter images in the same order.
- You may also weave screenshots through a story sequence: *discover* (`events.webp`), *participate* (`registration.webp`), and *learn* (`resources.webp`).
- Use comfortable whitespace, unobtrusive borders, and short explanatory captions rather than a dense image grid.

## Implementation checklist for Claude Code

1. Preserve all three concept styles and the five developer profiles; the LinkedIn URL for Blayne Jarrett is confirmed despite the `elizabeth-jarrett` slug.
2. Keep a clearly labeled placeholder when an image is missing. Never replace it with an unrelated stock image.
3. Replace the `.ghost` markup inside `.shot` with an `<img>` using the paths above (relative to each `index.html`, typically `../assets/screenshots/...`), `alt` text describing the actual visible UI, `loading="lazy"`, and dimensions/aspect ratio that prevent layout shifts.
4. Keep `.shothead` browser-style captions as aesthetic framing. Retain readable crop and responsive image sizing (`max-width:100%; height:auto; object-fit:contain`).
5. Update the text to describe only features present in the actual Mind Bloom repo. Make no unsupported claims about reliability, accessibility compliance, security validation, or production deployment.
6. Run all three sites locally and ensure image URLs work both locally and when published under a GitHub Pages repository subpath.
7. Use a consistent sample dataset and do not capture sensitive information in admin or user screens.

If the project is still not ready for a safe screenshot, leave the labeled placeholder in place rather than blocking the showcase build.
