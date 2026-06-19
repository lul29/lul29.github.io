# Changelog

All notable changes to the website project are documented here.
This file serves as portable long-term memory across development sessions.
Update it after every meaningful unit of work.

---

## 2026-06-19 -- Git init + GitHub Pages deployment (LIVE)

- Initialized git repo and pushed source to GitHub: `lul29/lul29.github.io`
- Added `.github/workflows/publish.yml`: GitHub Action renders Quarto and publishes the built site to the `gh-pages` branch on every push to `main` (uses `quarto-dev/quarto-actions`)
- Seeded an empty `gh-pages` branch first (the action errors if the branch does not yet exist)
- **Site is LIVE at https://lul29.github.io/** -- a repo named `<user>.github.io` is a GitHub user page, and Pages CANNOT be disabled on it (GitHub returns 422). It was auto-enabled serving raw source from `main`; switched the Pages source to the `gh-pages` branch so it serves the rendered HTML. To truly hide a WIP, the only options are a custom unlinked domain, a different repo name (project page, still public), or a private repo on a paid plan.
- Fixed contact email: `npb2@psu.edu` -> `lul29@psu.edu` in `_quarto.yml` navbar and `people.qmd`
- Cosmetic polish still pending before wider sharing (see Known limitations)
- Removed the iOLab tab: deleted `iolab.qmd` and its navbar entry (homepage still uses `images/iolab.jpg` as the device photo; publication titles still mention iOLab)
- Dropped orphan image `images/people/ying-wang.jpg`

---

## 2026-03-27 -- Initial Quarto site

- Created Quarto website replacing WordPress site at sites.psu.edu/lleblond/
- Four pages: Home, People, Publications, iOLab
- Penn State navy/blue color scheme with cosmo theme
- Custom CSS: hero section, card grid, person cards with circular photos, publication entries
- All content migrated from old WordPress site
- Local images for all people photos (no more hotlinking from PSU servers)
- People: Louis Leblond (PI), Julian Mintz, Jude Sullivan, Ashlyn Leary, Heer Patel, Tyler Lowman (current); Meghan Ishler, Emma Koller, Mar Alegre (former)
- Publications: 4 papers, 3 posters, 1 talk, links to arXiv and Google Scholar
- iOLab: full lab tables for Phys 211 (Mechanics) and Phys 212 (E&M) with download links

---

## Failed approaches / dead ends

(Record things that didn't work so future sessions don't re-attempt them)

- **`subtitle` in `_quarto.yml`**: Not a valid property under `website:`. Quarto validation rejects it. Use a combined `title` string instead.

---

## Known limitations

- Lab material download links (docx, zip) still point to sites.psu.edu (will break if old site is taken down)
- Poster/talk PDF links still point to sites.psu.edu
- Hosting done: GitHub Pages at https://lul29.github.io/ (auto-deploys on push to `main`)
- Tyler Lowman's project description is blank (needs input)
- `images/people/ying-wang.jpg` exists but no matching person card in `people.qmd` (orphan image)
- Cosmetic pass still needed before sharing the URL widely
