# avocat-despagubiri-victime.ro

Single-page Jekyll site for **Cabinet de Avocat VĂRZARU ION**, recreating the content of
`avocat-despagubiri-victime.ro` with a modern template (shared with `avocat-asigurari-rca.ro`
and inspired by `varzaru.ro`). Deployed on GitHub Pages at the custom domain
**avocat-despagubiri-victime.ro**.

## Structure

```
.
├── index.html              # Single page — assembles the section includes
├── _layouts/default.html   # HTML shell (head, header, footer)
├── _includes/              # Page sections
│   ├── header.html  footer.html
│   ├── hero.html  cabinet.html  servicii.html
│   ├── despagubiri.html  echipa.html  intrebari.html  testimoniale.html  contact.html
│   └── structured-data.html
├── assets/css/style.scss   # Theme (compiled to style.css by Jekyll)
├── content/                # Source content parsed from the original site (excluded from build)
├── _config.yml             # Site + contact settings
├── CNAME                   # Custom domain: avocat-despagubiri-victime.ro
└── .github/workflows/jekyll.yml   # Build + deploy to GitHub Pages
```

Editable content lives in the `_includes/*.html` section files. Contact details (phone, email, name,
address) are centralized in `_config.yml` under `contact:` and pulled in via `{{ site.contact.* }}`.

## Local preview

```bash
bundle install
bundle exec jekyll serve --livereload
# open http://localhost:4000
```

## Deploy (GitHub Pages)

1. Create a repo and push these files to the `main` branch.
2. In **Settings → Pages → Build and deployment**, set **Source = GitHub Actions**.
   (The included `.github/workflows/jekyll.yml` builds and deploys on every push to `main`.)
3. The `CNAME` file already sets the custom domain to `avocat-despagubiri-victime.ro`. In
   **Settings → Pages** confirm the custom domain and enable **Enforce HTTPS** once the
   certificate is issued.

## DNS (point the domain at GitHub Pages)

At your domain registrar / DNS host:

- **Apex `avocat-despagubiri-victime.ro`** → four `A` records:
  `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
  (optionally also the `AAAA` records: `2606:50c0:8000::153` … `8003::153`)
- **`www`** → `CNAME` to `<your-github-username>.github.io.`

DNS changes can take up to 24h to propagate; the HTTPS certificate is issued automatically afterwards.
