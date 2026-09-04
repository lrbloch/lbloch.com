# lbloch.com

Personal site for Laura Bloch. Static HTML, no build step.

## Files

```
index.html                 Home — about, work, projects
cuddlecode.html            Project page
matched.html               Project page
making-with-monsters.html  Project page
ar-travel-map.html         Project page
images/                    All image assets used by the pages
unused-images/             Extra AR-project photos not on the page (mind maps,
                           QR-code tests, laser-cut fail, vinyl lotus). Delete
                           this folder before pushing, or keep it as an archive.
.nojekyll                  Tells GitHub Pages to serve files as-is
```

## Deploying to GitHub Pages

1. Create a repo named `lrbloch.github.io` (or any repo, if using a custom domain).
2. Push the contents of this folder to the `main` branch — `index.html` must sit at the repo root, not inside a subfolder.
3. Repo → **Settings** → **Pages** → Source: **Deploy from a branch**, Branch: `main`, folder: `/ (root)`.
4. Wait ~1 minute for the first deploy.

## Custom domain (lbloch.com)

1. In **Settings → Pages → Custom domain**, enter `lbloch.com` and save. This creates a `CNAME` file in the repo.
2. In Squarespace DNS (or wherever the domain is registered), set:
   - `A` records for `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www` → `lrbloch.github.io`
3. Back in Settings → Pages, tick **Enforce HTTPS** once the certificate is issued (can take up to an hour).

## Editing

Each page is self-contained — CSS lives in a `<style>` block in the `<head>`. The shared palette is defined
in `:root` at the top of every file, so a color change needs to be made in each of the four files:

```css
--ink:#181a22;        /* body text */
--paper:#faf8f5;      /* background */
--accent:#7a2e3a;     /* links, headings, accents */
--accent-soft:#c99aa2;/* card borders, underlines */
--muted:#8a8580;      /* captions, secondary text */
--line:#e3ded9;       /* rules and dividers */
```

Fonts are Fraunces (display) and Inter (body), loaded from Google Fonts.
