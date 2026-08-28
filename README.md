# yuruzhang22.github.io

Personal academic homepage of Yuru Zhang — <https://yuruzhang22.github.io/>

Built with Jekyll on [AcademicPages](https://github.com/academicpages/academicpages.github.io),
a fork of the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme
(© 2016 Michael Rose, MIT — see `LICENSE`). The theme has been trimmed down to just
what this site uses.

## Editing content

| What | Where |
|------|-------|
| Biography, education, experience | `_pages/about.md` (the homepage, `permalink: /`) |
| Publications | `_pages/publications.md` |
| Honors and awards | `_pages/Honors and Awards.md` |
| Academic activities | `_pages/Academic Activities.md` |
| Services | `_pages/services.md` |
| Nav bar | `_data/navigation.yml` |
| Name, photo, sidebar links | `author:` block in `_config.yml` |
| Styles | `_sass/` (compiled from `assets/css/main.scss`) |

Publication lists use a kramdown block IAL so they number newest-first:

```markdown
{: reversed="reversed" start="12"}
12. First (newest) entry
11. ...
```

Kramdown renumbers ordered lists from 1 and ignores the digits you type, so
`reversed` + `start` on the `<ol>` is what actually produces the descending
numbers. Bump `start` when you add an entry.

## Publishing

Push to `master`. GitHub Pages builds the site automatically and it goes live
within a minute or two.

## Running locally

Needs `ruby-dev` for Jekyll's native extensions:

```bash
sudo apt install ruby-dev bundler
bundle install
bundle exec jekyll serve --config _config.yml,_config.dev.yml
```
