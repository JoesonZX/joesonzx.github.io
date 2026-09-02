# joesonzx.github.io — Personal Website

Personal homepage for Xuan Zhou (Joey), modeled on the classic
"hero + fixed navbar + alternating gradient sections" portfolio style.

**Live:** https://joesonzx.github.io

## Files

| File | Purpose |
|------|---------|
| `index.html` | All content — edit this to update the page |
| `styles.css` | All styling (no framework, hand-written CSS) |
| `static/img/campus.jpg` | Hero background (Geisel Library, UCSD) |
| `favicon.svg` | Browser tab icon |

The CV button links to a Google Drive file (not committed to this repo, so the
PDF can't be crawled): https://drive.google.com/file/d/1B1SUtvOEPSkLB2vcj0OwlkFqsBVCPQAA/view?usp=sharing
To change it, update the two URLs in `index.html` (navbar "CV" link and hero button).

## How to edit

1. Open `index.html`, find the section you want (`<section id="about">`, etc.).
2. Edit the text, save.
3. Commit and push:

```bash
git add .
git commit -m "Update content"
git push
```

The site updates automatically within ~1 minute of pushing.

## Replace the avatar with a real photo

1. Save your photo as `static/img/photo.jpg` (square works best).
2. In `index.html`, replace the `<div class="avatar">XZ</div>` line with:

```html
<img class="avatar-photo" src="static/img/photo.jpg" alt="Photo of Xuan Zhou">
```

## Local preview

```bash
python -m http.server 8642
# then visit http://localhost:8642
```

## Credits

- Hero background: "Geisel Library, UCSD, October 2016" by Jami (Wiki Ed),
  Wikimedia Commons, [CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Geisel_Library,_UCSD,_October_2016.jpg)
- Icons: [Bootstrap Icons](https://icons.getbootstrap.com) (MIT)
- Fonts: Mulish & Kanit (Google Fonts, OFL)

## Later upgrades

- **Custom domain** (e.g. `xuanzhou.me`): buy a domain (~$10/yr), add a `CNAME`
  file containing the domain, then set it in repo Settings → Pages. GitHub
  301-redirects `joesonzx.github.io` to the new domain automatically.
- **Blog**: either add pages by hand, or migrate to Astro/VitePress later —
  content here is plain HTML, easy to port.
