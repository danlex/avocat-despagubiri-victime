# avocat-despagubiri-victime.ro

This domain is a **permanent redirect** to [varzaru.ro](https://varzaru.ro). The standalone
microsite was consolidated into varzaru.ro; this repo now serves only redirect stubs.

- `index.html` and `404.html` — plain-HTML redirect stubs (canonical + `noindex,follow` +
  meta refresh + JS `location.replace`). With no Jekyll front matter they are copied verbatim,
  so **every** URL on this domain redirects to
  `https://varzaru.ro/avocat-specializat-in-despagubiri-victime-accidente-rutiere/`.
- `CNAME` — custom domain `avocat-despagubiri-victime.ro`.
- `.github/workflows/jekyll.yml` — builds and deploys to GitHub Pages on every push to `main`.

The previous single-page Jekyll site lives in the git history prior to the consolidation commit.
