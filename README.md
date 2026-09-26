# Ever the Cynic

One-page site for Ryan Kelly, Irish sports writer and editor, at **www.everthecynic.com**.

A static site with no build step: `index.html`, plus images and videos in `img/`.

## Preview locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Files

| Path | What it is |
|---|---|
| `index.html` | The whole page: markup, styles and scripts |
| `img/*.mp4`, `img/*.webm` | Looping chapter videos (H.264 plus a WebM fallback). Ryan is frozen in each clip so AI motion never touches his face |
| `img/*.jpg` | Video posters, shown while loading and for visitors who prefer reduced motion, plus the photo strip |
| `img/scene1-ryan.webp` | Ryan's real cut-out, layered over the fort scene |
| `img/coaster-*.webp` | The wedding coasters, front and back |
| `CNAME` | Custom domain for GitHub Pages |
| `favicon.svg` | Mustard, olive and sky mark |

## Hosting on GitHub Pages

1. **Settings → Pages → Build and deployment**: Source **Deploy from a branch**, branch **main**, folder **/ (root)**.
2. At your domain registrar, add these DNS records for `everthecynic.com`:

   | Type | Name | Value |
   |---|---|---|
   | CNAME | `www` | `mrchristian-genki.github.io` |
   | A | `@` | `185.199.108.153` |
   | A | `@` | `185.199.109.153` |
   | A | `@` | `185.199.110.153` |
   | A | `@` | `185.199.111.153` |

3. Back in **Settings → Pages**, confirm the custom domain reads `www.everthecynic.com`, wait for the DNS check, then tick **Enforce HTTPS**.

## Before launch

- [ ] Someone who knows Ryan confirms the AI-drawn faces in the Malin Head and glen scenes look like him
- [ ] Confirm his current title at GOAL ("Senior writer and SEO editor")
- [ ] Ryan is happy with the Paddy essay being featured and the wedding coasters being shown
- [ ] Remove the `<meta name="robots" content="noindex, nofollow">` line in `index.html` so search engines can list the site
