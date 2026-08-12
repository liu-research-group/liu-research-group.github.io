# Provenance and third-party notices

## Template ancestry

This site's code descends from two upstream projects, both MIT licensed.

| | |
|---|---|
| **Original template** | Allan Lab, Leiden University — <https://github.com/mpa139/allanlab> |
| | (`allanlab/allanlab` redirects here; `mpa139/allanlab` is canonical.) |
| **Intermediate adaptation** | Uppsala Secure Learning and Control Lab — <https://github.com/uslc-lab/uslc-lab.github.io> |
| **Snapshot seeded from** | commit `4e242bab801e`, dated 2026-06-18 |
| **Seeded on** | 2026-08-11 |

The Uppsala lab adapted the Allan Lab template and refactored its publication
handling to use Jekyll Scholar. This repository was seeded from a **file-level
snapshot** of that work, not a fork: no upstream git history, images, assets, or
bibliography were carried over.

## What was deliberately excluded

- The Uppsala lab's git history (~3,166 commits) and its ~52 MB of images
- Their bibliography (`_bibliography/uscl_publications.bib`)
- All of their people, news, projects and research-theme data
- Their Google Analytics property, which shipped in `_includes/analytics.html`
- `bin/deploy`, which deleted the working tree and force-pushed `gh-pages`
- Their CI workflows, which used the removed `::set-output` command

## Upstream copyright notices

Neither upstream repository ships a `LICENSE` file; GitHub's licence API reports
"Not Found" for both, and their MIT grants are asserted in prose. The notices are
reproduced verbatim here so they travel with the code.

**Allan Lab** — from the README of <https://github.com/mpa139/allanlab>:

> Copyright Allan Lab. Code released under the MIT License.

**Uppsala Secure Learning and Control Lab** — from their about-the-website page
at <https://uslc-lab.github.io/aboutwebsite.html>:

> It was adapted from different sources, primarily Allan's Lab, and refactored to
> use Jekyll Scholar. [...] Code released under the MIT License.

Both notices are retained under the terms of the MIT licence in [LICENSE](LICENSE),
which requires that the copyright notice and permission notice accompany copies
and substantial portions of the software.

## What was retained from upstream

The Jekyll layouts, includes, SASS, and the `_plugins` directory, all modified
for this site. `_bibliography/ieee-with-url-mod.csl` is retained as-is.

## Bundled third-party components

| Component | Licence |
|---|---|
| Bootstrap 3.3.x | MIT |
| Bootswatch | MIT |
| jQuery 1.11.3 | MIT |
| Font Awesome | SIL OFL 1.1 (fonts) / MIT (code) |
| Jekyll | MIT |
| Jekyll Scholar | GPL-3.0 (used as a build-time plugin) |

## Site content

Text, the bibliography in `_bibliography/papers.bib`, and the group's branding
assets are © 2026 Mingzhe Liu and are not covered by the upstream templates'
licences. Publication metadata was retrieved from Crossref.
