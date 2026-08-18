# ahsentahir.github.io: plain HTML version

Static HTML. No Jekyll, no Ruby, no build step, no JavaScript.

## Preview

    cd ahsen-academic-site-html
    python3 -m http.server 8000

Then open <http://localhost:8000>. Edit any `.html` file and refresh the browser.
Changes appear immediately; there is nothing to rebuild.

You can also just double-click `index.html` to open it in a browser directly. The
local server is only slightly better because it matches how GitHub Pages will
serve the site.

## Layout

| File | Page |
|---|---|
| `index.html` | Homepage: bio, research interests, selected publications, news |
| `research.html` | Research narrative |
| `publications.html` | Full publication list |
| `projects.html` | Projects |
| `teaching.html` | Teaching & outreach |
| `cv.html` | CV |
| `publication/*.html` | One page per paper |
| `assets/style.css` | All styling: every page shares this one file |

## Editing notes

**Styling** lives entirely in `assets/style.css`. Change a colour or spacing there
and every page updates. The site is **dark by default** for every visitor, whatever
their OS is set to; the palette is the `:root` block at the top of the stylesheet.
The `@media print` block at the bottom flips those same tokens back to black-on-white,
so printing the CV still produces a normal page.

**The sidebar and top nav are duplicated in every HTML file.** This is the cost of
dropping Jekyll: to change your bio, location, or add a link (Google Scholar, ORCID),
you must edit the same block in all 8 files. Find-and-replace across the folder is
the practical way to do it.

**Adding a publication** means editing three files: `index.html` (selected list),
`publications.html` (full list), and `cv.html` (CV list). They will silently drift
apart if you forget one. Check all three whenever a paper lands.

**CV PDF:** the download button on `cv.html` serves `files/Tahir_CV.pdf`, which
is compiled from the LaTeX source in `~/Desktop/coding/ahsen-cv/` (build with
`tectonic Tahir_Research_CV.tex`). When the CV changes, recompile and copy the
fresh PDF over, or the download drifts out of sync with the page. (`cv.html`
also has a print stylesheet, so Cmd-P still produces a usable PDF of the page
itself.)

## Outstanding TODOs

Search the folder for `TODO (Ahsen)`. Each one marks something only you can supply:

- **Author contribution statements** on both publication pages (highest value).
- **Google Scholar and ORCID links** in the sidebar of all 8 files.
- **GPA / scholarships** on `cv.html`.
- **TA experience** on `teaching.html`, if you have any.

## Deploying

GitHub Pages serves plain HTML as-is. When you are happy with this version, copy
these files to the root of the `AhsenTahir.github.io` repo, delete the Jekyll
scaffolding (`_config.yml`, `_pages/`, `_layouts/`, `_includes/`, `_sass/`,
`Gemfile`, etc.), and add an empty `.nojekyll` file at the root so Pages skips the
Jekyll build entirely.

Do that on a branch first and confirm it renders before touching `main`, which
is what serves the live site.
