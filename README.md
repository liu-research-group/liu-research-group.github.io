# Liu Research Group — website

Source for <https://liu-research-group.github.io>, the site of the Liu Research
Group in the Department of Civil, Construction and Environmental Engineering at
The University of Alabama.

Built with [Jekyll](https://jekyllrb.com) and
[Jekyll Scholar](https://github.com/inukshuk/jekyll-scholar). Derived from the
Allan Lab template — see [NOTICE.md](NOTICE.md) for full provenance.

## Running it locally

Ruby 3.2.2 is pinned in `.ruby-version`; gem versions are pinned in `Gemfile`
and locked in `Gemfile.lock`.

```bash
bundle install
bundle exec jekyll serve --host localhost --port 4000 --livereload
```

Then open <http://localhost:4000>.

> Bind to `localhost`, not `0.0.0.0`. Jekyll writes the host you give it into
> every absolute URL, and `0.0.0.0` is not fetchable by a browser — the site
> renders with no CSS at all.

## Editing content

Most updates need no template changes.

| What | Where |
|---|---|
| News items | `_data/news.yml` |
| Group members | `_data/team_members.yml` |
| Research thrusts | `_data/research_themes.yml` |
| Featured publications | `_data/publist.yml` |
| Full publication list | `_bibliography/papers.bib` |
| Page text | `_pages/*.md` |
| Colours | `_sass/_variables.scss`, `_sass/bootstrap/_variables.scss` |

### Adding a publication

Add one BibTeX entry to `_bibliography/papers.bib`. Fetch it canonically from
the DOI rather than hand-typing it:

```bash
curl -LH "Accept: application/x-bibtex" https://doi.org/<DOI>
```

Two conventions matter:

- **Citation keys must be unique.** Crossref's default keys (`Liu_2026`) collide
  across papers, and Jekyll Scholar then silently invents misleading ones. This
  repo uses `lastnameYYYYfirstword`, e.g. `liu2026comparative`.
- **`tag={heatpumps|sciml|decarb|control}`** places a paper under a research
  thrust on the Research page. Papers without a tag still appear in the full
  list on Publications.

Crossref returns each entry on a single line — beware of edits that assume
newlines inside an entry.

### Refreshing from Google Scholar

The Scholar profile is the authoritative list of which papers are the PI's;
Crossref supplies canonical DOIs, titles, authors and dates. Neither alone is
sufficient. When resolving a title, add `filter=type:journal-article` — Crossref
otherwise often returns the SSRN preprint instead of the published version.

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds with
Bundler and publishes to GitHub Pages.

GitHub Pages' native Jekyll build **cannot** build this site: Jekyll Scholar is
not on GitHub's plugin allowlist. The Pages source must be set to
**GitHub Actions**, not "Deploy from a branch".
