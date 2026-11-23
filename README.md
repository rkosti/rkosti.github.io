# rkosti.github.io

Personal site of Ronak Kosti, built on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) Jekyll template. Every push to `main` rebuilds and deploys it through GitHub Actions (`.github/workflows/jekyll.yml`); it's live about two minutes later.

Everything on the site lives in this repo. Edit the files below on GitHub or locally, commit, push.

## Where things are

| What | File |
|---|---|
| Sidebar (name, bio, location, links) | `_config.yml` → `author:` |
| Profile photo | `images/profile.png` (square, ~400px) |
| Home page: intro, now, highlights, news, recent GitHub repos | `_pages/about.md` |
| Portfolio projects | `_portfolio/NN-name.md` (one file each) |
| Publications | `_publications/YYYY-MM-DD-name.md` (one file each) |
| CV page | `_pages/cv.md` |
| CV PDF | `files/CV_Ronak_Kosti.pdf` (replace it to update the download) |
| Notes / blog posts | `_posts/YYYY-MM-DD-title.md` |
| Header menu | `_data/navigation.yml` |

## Adding things

**A project.** Create `_portfolio/09-short-name.md`. The number sets its position on the Portfolio page (lowest first), so renumber files to reorder.

```markdown
---
title: "Project title"
collection: portfolio
permalink: /portfolio/short-name/
excerpt: "One or two sentences shown on the Portfolio list.\n\n*Where · 2026*"
tags: [topic one, topic two]
---

*Where · 2026*

What it is, in a sentence or two.

## What I did

- A concrete result, with the number that shows it.

## Links

- [Code](https://github.com/...)
```

**A publication.** Create `_publications/2026-05-01-short-name.md`. `category` is `manuscripts` (journal) or `conferences`; the list is grouped by it and sorted by `date`.

```markdown
---
title: "Paper title"
collection: publications
category: conferences
permalink: /publication/short-name
excerpt: "One sentence on what the paper does."
date: 2026-05-01
venue: "CVPR 2026"
paperurl: "https://..."
citation: 'A. Author, R. Kosti. (2026). &quot;Paper title.&quot; <i>CVPR 2026</i>.'
---

One sentence on what the paper does.
```

**News or a "now" update.** Edit the lists in `_pages/about.md` (newest news first) and bump the "Updated" date under "What I'm working on now".

**A note or blog post.** Add `_posts/2026-12-01-title.md` with `title:` in the front matter, then add this to `_data/navigation.yml` so it shows in the menu:

```yaml
  - title: "Notes"
    url: /year-archive/
```

The "Recently on GitHub" list on the home page is fetched in the visitor's browser, so new public repos appear on their own.

## Preview locally

```bash
bundle install
bundle exec jekyll serve -l -H localhost   # http://localhost:4000
```
