# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Hugo static site using the Hugo Blox Academic CV theme for a personal academic portfolio. Content is written in Markdown with YAML front matter. The theme is loaded via Hugo Modules (Go modules).

## Commands

**Local dev server:**
```bash
bash view.sh
# runs: hugo server
```

**Production build (as used by Netlify):**
```bash
hugo --gc --minify -b $URL
```

**Update theme modules:**
```bash
hugo mod get -u
```

## Architecture

- **Config**: `hugo.yaml` (root) + `config/_default/` contains `params.yaml` (theme params), `menus.yaml` (nav), `module.yaml` (Hugo modules), `languages.yaml`
- **Homepage**: Single `content/_index.md` with `type: landing` and `sections:` blocks (resume-biography-3, collection for news, collection for featured publications)
- **Content types**: Publications (`content/publications/<slug>/index.md`) and events (`content/events/<slug>.md`)
- **Static assets**: `static/img/`, `static/files/`, `static/slides/`
- **Theme**: Hugo Blox (via Go modules in `go.mod`); do not vendor theme files
- **Deployment**: Netlify, configured in `netlify.toml` (Hugo v0.139.5, Go 1.21)

## Content Conventions

- Front matter uses `---` (YAML) delimiters
- Publications use `publication_types` with string values: `paper-conference`, `article-journal`, `article`, `chapter`
- Publications use `links:` list instead of `url_pdf`/`url_code` flat fields
- Events use `event_name` (not `event`) and `{{< callout note >}}` shortcode
- The `authors/admin/_index.md` file defines the site owner profile with `profiles:` for social links
- Publications use APA citation style (configured in `params.yaml`)
