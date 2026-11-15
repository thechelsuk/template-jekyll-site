# template-jekyll-site

A template for a new thechelsuk Jekyll site on GitHub Pages. It's a minimal
working site (one layout, a home page and a 404 page) with the repo set-up
already in place:

- the GitHub Pages deploy workflow (`.github/workflows/pages.yml`)
- callers of the shared [thechelsuk/workflows](https://github.com/thechelsuk/workflows):
  weekly link checker, dependency review and release
- Dependabot for GitHub Actions and Ruby gems
- community files (code of conduct, contributing, security policy, issue and
  pull request templates), an MIT licence and `.editorconfig`
- `CNAME` and `.well-known/security.txt`

## Start a site from it

1. Select **Use this template** on GitHub, then **Create a new repository**.
2. Set `CNAME` to the site's host.
3. Set `site_host` in `.github/workflows/link-checker.yml` to the same host,
   with dots escaped (`example\.thechels\.uk`).
4. Edit `_config.yml`: `title`, `description`, `url` (the same host) and
   `repository`.
5. Change the host in `.well-known/security.txt`.
6. Replace `index.md`, `404.md` and `_layouts/default.html` with the site's
   own pages and layout.
7. Point the links in `.github/CONTRIBUTING.md` and
   `.github/ISSUE_TEMPLATE/config.yml` at the new repo.
8. In **Settings → Pages**, set the source to **GitHub Actions** and add the
   custom domain.

## Run it locally

```sh
bundle install
bundle exec jekyll serve
```

## Releases

Pushing a commit to `main` whose first line starts with `release:` tags a new
minor version and writes its release notes. Use `release(patch):` or
`release(major):` for other bumps. The first release is `1.0.0`.

## Licence

[MIT](LICENSE)
