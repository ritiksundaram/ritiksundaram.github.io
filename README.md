# ritiksundaram.github.io

Personal site for Ritik Sundaram. Single-file static site — no build step, no
dependencies. Everything lives in `index.html`.

## To-do before/after publishing

1. **Resume** — drop `resume.pdf` in the repo root, or delete that link in the
   contact section.
2. **Project links** — some cards point at the GitHub profile as a fallback.
   Swap in the real repo URLs once those projects are public.
3. **Boeing start year** — currently `2024 — Present`. Change if that's off.
4. **Columbia** — add the graduation year in the About spec list if wanted.

## Deploy on GitHub Pages

Repo → **Settings** → **Pages** → Source: `Deploy from a branch`,
Branch: `main` / `root`. Save.

Live at `https://ritiksundaram.github.io` in about a minute.

## Custom domain (optional)

Buy a domain, add a file named `CNAME` in the repo root containing just the domain
(e.g. `ritiksundaram.com`), then point these DNS records at GitHub:

```
A     @    185.199.108.153
A     @    185.199.109.153
A     @    185.199.110.153
A     @    185.199.111.153
CNAME www  ritiksundaram.github.io
```

Then Settings → Pages → Custom domain → enter it → tick "Enforce HTTPS".

## Editing

Everything is in one file: styles in `<style>`, the hero animation in `<script>`.
Colors are CSS variables at the top of the style block, so changing the accent is
a one-line edit to `--signal`.
