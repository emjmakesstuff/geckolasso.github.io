# GeckoLasso site

A Jekyll site for the GeckoLasso research project, built on the
[minima](https://jekyll.github.io/minima/) theme and served from
`geckolasso.github.io`.

## Deploying

1. Copy everything in this folder into the root of your `geckolasso.github.io`
   repo (don't nest it in a subfolder).
2. Commit and push to the `main` branch.
3. In the repo's **Settings → Pages**, make sure the source is set to
   deploy from the `main` branch, root folder. For a `<username>.github.io`
   repo this is usually already the default — GitHub Pages will build it
   with Jekyll automatically, no Actions workflow required.
4. Your site will be live at `https://geckolasso.github.io` within a
   minute or two of pushing.

## Previewing locally (optional but recommended)

You'll need Ruby installed. Then, from this folder:

```
bundle install
bundle exec jekyll serve
```

Visit `http://localhost:4000`.

## Where to edit things

Everything lives on a single page (`index.html`). A row of pill-style
buttons near the top links to `#publications`, `#team`, and any
featured external links (e.g. a specific paper) — edit that
`<div class="top-links">` block directly to add/remove/relabel buttons.

- **Team members** → `_data/team.yml`. Add/remove entries as needed.
- **Publications** → `_data/publications.yml`. Newest first; grouped by
  year automatically in the Publications section.
- **Featured links at the top** → the `.top-links` block in
  `index.html`. A link with no URL yet (e.g. "coming soon") should be
  a `<span class="pill-button is-disabled">` instead of an `<a>`.
- **Homepage copy** → `index.html` (hero text, the four-step "how it
  works" list).
- **Site title / description / contact email** → `_config.yml`. See
  the [minima docs](https://jekyll.github.io/minima/) for the full
  list of supported options (skins, social links, etc.).
- **Pill-button styling** → `assets/main.scss`. This is the one bit of
  custom CSS on top of minima's defaults (`@import "minima";` plus the
  `.top-links`/`.pill-button` rules below it).

## Notes

- All page copy and every team/publication entry right now is
  placeholder — swap it for your real project description, people, and
  papers whenever you're ready.
- The site otherwise uses minima's default styling and layouts.
