# p4wnda Blog

Jekyll/Chirpy source for [p4wnda.github.io/blog](https://p4wnda.github.io/blog/).

This is the maintainable blog repository. Add and edit writeups here, then push to `master`; GitHub Actions builds and deploys the site.

## Project Links

The root project hub lives at [p4wnda.github.io](https://p4wnda.github.io/). The separate GitHub Pages tools are maintained in their own repositories:

- [Blog](https://p4wnda.github.io/blog/) - writeups, notes, and lab documentation.
- [Pentest Cheatsheet](https://p4wnda.github.io/pentest/) - command reference with variables, notes, tracking, and JSON run export.
- [CTF Checklists](https://p4wnda.github.io/checklists/) - standalone and Active Directory box checklists linked to cheatsheet commands.
- [Reporting Tool](https://p4wnda.github.io/reporting-tool/) - vulnerability finding editor that imports Pentest Cheatsheet run JSON.

## Add a Post

Create a Markdown file under `_posts/`, usually grouped by topic:

```text
_posts/<category>/YYYY-MM-DD-title.md
```

Example:

```text
_posts/hackthebox/2026-05-12-example-box.md
```

Use normal Jekyll front matter, for example:

```yaml
---
title: Example Box
categories: [HackTheBox]
tags: [htb, linux, writeup]
image:
  path: /assets/img/example/example.png
---
```

Put images under `assets/img/...` and reference them with absolute paths like `/assets/img/...`.

## Local Build

```bash
bundle install
bundle exec jekyll serve
```

For the deployed project path, the site is configured with:

```yaml
baseurl: "/blog"
```

## Deploy

GitHub Pages should be configured as:

- Source: GitHub Actions
- Branch: master

The workflow lives at `.github/workflows/pages-deploy.yml`.
