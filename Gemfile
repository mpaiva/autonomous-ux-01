source "https://rubygems.org"

# Pin to the github-pages gem so local builds match what GitHub Pages
# runs in production (safe mode, whitelisted plugins only). This is the
# deliberate compatibility choice that keeps deploys from silently failing.
gem "github-pages", group: :jekyll_plugins

# Plugins are declared in _config.yml; these are bundled by github-pages.
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
end

# Windows / JRuby compatibility shims (harmless elsewhere).
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end
gem "wdm", "~> 0.1.1", platforms: [:mingw, :x64_mingw, :mswin]
