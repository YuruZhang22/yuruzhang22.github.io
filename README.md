# yuruzhang22.github.io

Personal academic homepage of Yuru Zhang — <https://yuruzhang22.github.io/>

A hand-written Jekyll site: one layout, one stylesheet, no JavaScript, no theme.
It began life on [AcademicPages](https://github.com/academicpages/academicpages.github.io)
(a fork of Minimal Mistakes, MIT — see `LICENSE`) and was rewritten to the same
design once it was clear the theme was carrying ~13,000 lines of Sass and 131KB
of jQuery to render five static pages.

## Layout of the repo

| What | Where |
|------|-------|
| Biography, education, experience | `_pages/about.md` (the homepage, `permalink: /`) |
| Publications | `_pages/publications.md` |
| Honors, activities, services | `_pages/honors.md`, `activities.md`, `services.md` |
| Nav bar | `_data/navigation.yml` |
| Name, photo, sidebar links | `author:` block in `_config.yml` |
| Page skeleton, `<head>`, sidebar, nav | `_layouts/default.html` |
| Every style on the site | `assets/css/style.css` |

Adding a page means dropping a Markdown file in `_pages/` with a `permalink`;
the layout applies by default.

## Two things worth knowing before editing

**Publication numbering.** Kramdown renumbers ordered lists from 1 and ignores
the digits you type, so the descending numbers come from an attribute list that
sets `reversed` and `start` on the `<ol>`:

```markdown
{: reversed="reversed" start="12"}
12. First (newest) entry
11. ...
```

Bump `start` when you add an entry. The blank line above the `{: ... }` matters —
without it kramdown attaches the attributes to the preceding heading instead.

**The content column.** The sidebar is `15.2542%` and the gap is `5.9322%`, so
text starts at `21.1864%`. The masthead uses the same two grid tracks, which is
what lines the nav up with the body text. Change one, change both.

## Publishing

Push to `master`. GitHub Pages builds the site and it goes live in a minute or
two. `style.css` is plain CSS, copied as-is — there is no Sass step.

## Running locally

Jekyll needs `ruby-dev` for its native extensions:

```bash
sudo apt install ruby-dev bundler
bundle install
bundle exec jekyll serve --config _config.yml,_config.dev.yml
```
