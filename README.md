# ahsentahir.github.io

Academic website for Ahsen Tahir — multi-agent LLM systems, agent-to-agent
communication, and evaluation of language-model agents.

Built on the [Academic Pages](https://github.com/academicpages/academicpages.github.io)
Jekyll template and served by GitHub Pages from the `main` branch.

## Editing

| What | Where |
|---|---|
| Homepage, research statement, news | `_pages/about.md` |
| Longer research narrative | `_pages/research.md` |
| Publications (one file each) | `_publications/` |
| Projects | `_portfolio/` |
| Teaching & outreach | `_teaching/` |
| CV page | `_pages/cv.md` (PDF at `files/Tahir_CV.pdf`) |
| Name, links, Scholar/ORCID, sidebar | `_config.yml` |
| Header nav | `_data/navigation.yml` |

Push to `main` and GitHub Pages rebuilds automatically.

## Local preview

Optional — GitHub Pages builds on push, so you can skip this entirely.

The `github-pages` gem hard-pins Liquid 4.0.3, which calls `String#tainted?`.
That method was removed in Ruby 3.2, so **local builds need Ruby 3.1.x**
(macOS system Ruby 2.6 and Homebrew Ruby 4.x both fail, for opposite reasons).

    brew install ruby@3.1
    PATH="/opt/homebrew/opt/ruby@3.1/bin:$PATH" bundle install
    PATH="/opt/homebrew/opt/ruby@3.1/bin:$PATH" bundle exec jekyll serve

Then open http://localhost:4000. Docker (`docker compose up`) also works if you
have Docker Desktop installed.
