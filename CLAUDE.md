# Website Project -- Development Instructions

## Project overview

Personal academic website for Louis Leblond's Education Research Group at
Penn State University. Built with Quarto, replacing the old WordPress site
at sites.psu.edu/lleblond/.

## Building and previewing

```bash
quarto preview     # Live preview with hot reload
quarto render      # Build static site to _site/
```

## Key conventions

- **Quarto** static site generator -- `.qmd` files (markdown + YAML frontmatter)
- **No build tools** beyond Quarto itself
- Site config in `_quarto.yml`
- Custom CSS in `styles.css` (Penn State brand colors)
- Images stored locally in `images/` (not hotlinked from PSU servers)

## Site structure

```
_quarto.yml          # Site config, navbar, theme
index.qmd            # Home -- research focus, collaborative projects
people.qmd           # PI + current/former students with photos
publications.qmd     # Papers, posters, talks
iolab.qmd            # iOLab labs and course materials
styles.css           # Custom CSS (Penn State colors, card layouts)
images/
  people/            # Headshots (kebab-case filenames)
  iolab.jpg          # iOLab device photo
```

## Adding content

- **New page**: create `pagename.qmd`, add it to `navbar` in `_quarto.yml`
- **New person**: add a `person-card` block in `people.qmd`, put photo in `images/people/`
- **New publication**: add a `pub-entry` block in `publications.qmd`

## Progress tracking

Keep `CHANGELOG.md` updated after every meaningful unit of work. Record
completed tasks, failed approaches, and known limitations.
