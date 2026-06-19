# Changelog

All notable changes to the website project are documented here.
This file serves as portable long-term memory across development sessions.
Update it after every meaningful unit of work.

---

## 2026-06-19 -- Git init + GitHub Pages deploy setup

- Initialized git repo and pushed source to GitHub: `lul29/lul29.github.io` (user page, will serve at https://lul29.github.io once Pages is enabled)
- Added `.github/workflows/publish.yml`: GitHub Action renders Quarto and publishes built site to a `gh-pages` branch on every push to `main` (uses `quarto-dev/quarto-actions`)
- Site is intentionally NOT live yet -- Pages source must be set to the `gh-pages` branch in repo Settings to publish (held back for cosmetic work)
- Fixed contact email: `npb2@psu.edu` -> `lul29@psu.edu` in `_quarto.yml` navbar and `people.qmd`

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
- No hosting set up yet (GitHub Pages, Netlify, etc.)
- Tyler Lowman's project description is blank (needs input)
