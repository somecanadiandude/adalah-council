# Adalah Council — website

Static single-page site for https://adalahcouncil.org. No build step; deploy the
files as-is to GitHub Pages.

## Files
- `index.html` — the entire site (HTML + CSS + structured data in one file)
- `assets/` — logo, social-share image, favicons, app icon
- `favicon.ico`, `sitemap.xml`, `robots.txt`
- `CNAME` — keeps the custom domain (adalahcouncil.org) on GitHub Pages. Don't delete.
- `.nojekyll` — serves files as-is (skips Jekyll processing)

## Deploying to GitHub Pages
1. Commit these files to the root of the branch Pages serves (e.g. `main`).
2. In the repo: Settings → Pages → confirm the branch/folder and that the custom
   domain shows `adalahcouncil.org` with HTTPS enforced.
3. Fonts load from Google Fonts; the favicon, page title, description, and the
   social-share card (`assets/adalah-og.png`) are already wired up.
4. After it's live, submit `https://adalahcouncil.org/sitemap.xml` in Google Search
   Console so the site is indexed.

## Adding real programs later (no empty pages needed)
Open `index.html`, find the four program cards under `<!-- PROGRAMS -->`. Each card
has a comment showing where to add named items, e.g. inside a card:

```html
<ul class="items">
  <li><strong>Lecture title</strong> — one line of context, date</li>
</ul>
```

Add a small block of CSS for `.items` if you want custom spacing; plain `<ul>`
works out of the box.

## Adding a bio or board members
In the "Leadership & contact" section, the President block has a comment marking
where to add a short biography and additional name/role blocks when ready.

## Zeffy donation page (must be changed inside Zeffy — not in this repo)
The site's Donate buttons already point to the live campaign. To finish the brief's
Zeffy cleanup, log into the Zeffy dashboard and:
1. Rename the campaign from "Donate to Educate our Community!" to **Support Adalah Council**.
2. Set the description to: *Help us produce principled Islamic research, public
   education, and guidance addressing the questions facing our communities and
   institutions.*
3. Remove the star emojis.
4. Replace the campaign image with **`assets/adalah-logo.png`** (tightly cropped,
   minimal empty space). It reads clearly as a cream tile on Zeffy's dark background.
5. Confirm all text is legible on the dark background.

## Editing contact details
Contact info appears in two places in `index.html`: the "Leadership & contact"
section and the footer. Update both if it changes.
