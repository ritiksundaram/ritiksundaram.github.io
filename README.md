# Personal site

Single-file static site. No build step, no dependencies. Just `index.html`.

## Fill these in before you publish

Search `index.html` for `FILL IN`:

Email and LinkedIn are already in. Remaining:

1. **Resume** — drop `resume.pdf` in the repo root, or delete that link in the contact section.
2. **Project links** — four cards point at your GitHub profile as a fallback. Swap in the real repo URLs once those projects are public.
3. **Boeing start year** — currently `2024 — Present`. Change if that's off.
4. **Columbia** — add your graduation year in the About spec list if you want it there.

## Deploy on GitHub Pages


```bash
# 1. On github.com, create a new PUBLIC repo named exactly:
#    ritiksundaram.github.io

# 2. Locally:
mkdir ritiksundaram.github.io && cd ritiksundaram.github.io
# copy index.html (and resume.pdf) into this folder
git init
git add .
git commit -m "personal site"
git branch -M main
git remote add origin https://github.com/ritiksundaram/ritiksundaram.github.io.git
git push -u origin main
```

Then repo → **Settings** → **Pages** → Source: `Deploy from a branch`, Branch: `main` / `root`. Save.

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

## Editing later

Everything is in one file: styles in `<style>`, the hero animation in `<script>`.
Colors are CSS variables at the top of the style block, so changing the accent is
a one-line edit to `--signal`.
