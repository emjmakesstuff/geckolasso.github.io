# GeckoLasso site

A fully custom Jekyll site (no theme gem) for the GeckoLasso research
project, built to be served from `geckolasso.github.io`.

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

- **Team members** → `_data/team.yml`. Add/remove entries; each gets an
  auto-generated initials avatar (no photo needed). `color` can be
  `moss`, `ochre`, or `slate`.
- **Publications** → `_data/publications.yml`. Newest first; grouped by
  year automatically on the Publications page.
- **Homepage copy** → `index.html` (hero text, the four-step "how it
  works" strip).
- **Site title / contact email / description** → `_config.yml`.
- **Colors, type, spacing** → `assets/css/main.css`. The palette and
  fonts are declared as CSS variables at the top of the file under
  `:root` — change those and everything updates.
- **The branching-line motif** (used in the hero, footer, and as the
  basis for avatars) → `_includes/motif-branch.html`. It's a single
  reusable SVG partial.

## Notes

- All page copy and every team/publication entry right now is
  placeholder — swap it for your real project description, people, and
  papers whenever you're ready.
- No theme gem is used, so nothing here depends on minima or minimal —
  it's plain HTML/Liquid + one stylesheet, which also means GitHub Pages
  can build it without any special configuration.
