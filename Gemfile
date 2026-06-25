source "https://rubygems.org"

# Jekyll static-site generator. We deploy via GitHub Actions
# (bundle exec jekyll build), so we use the standard Jekyll gem
# rather than the legacy `github-pages` wrapper, which pins an old
# Jekyll 3.x that does not run on modern Ruby.
gem "jekyll", "~> 4.3"

# No plugins: this is a redirect-only site. index.html and 404.html are plain
# static files copied verbatim, so we don't need sitemap / seo-tag / redirect-from
# (and don't want a sitemap advertising a noindex page).

# Windows / JRuby timezone data (harmless elsewhere)
gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]
gem "wdm", "~> 0.1.1", platforms: [:mingw, :mswin, :x64_mingw]
