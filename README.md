# Now Showing — Movie Picker 🎬

A single-page movie voting board. Tap the titles you want, move them to the
**Ballot**, cast votes, and let the weighted **Surprise me** draw pick a winner.
Everything runs client-side in one `index.html` file — no build step, no
dependencies.

## Live site

Once GitHub Pages is enabled (see below), the site is served at:

```
https://ethanpullan.github.io/MoviePicker/
```

## How it works

- **Now Showing** — browse the catalogue grouped by category; tap a title to add
  it to the ballot.
- **Ballot** — adjust vote counts per movie and run the weighted random draw.
- **Edit list** — paste your own list. One movie per line, optional `(year)`,
  and lines starting with `#` begin a new category.

## Deploying to GitHub Pages

This repo ships with a workflow at
[`.github/workflows/deploy-pages.yml`](.github/workflows/deploy-pages.yml) that
builds and publishes the site automatically.

### Automatic (recommended)

1. Get this branch onto `main` (open a PR and merge, or push to `main`).
2. The **Deploy to GitHub Pages** workflow runs on every push to `main`. It
   uses `actions/configure-pages` with `enablement: true`, which turns Pages on
   for you and sets the source to **GitHub Actions**.
3. Watch it in the **Actions** tab. When it finishes, the live URL is shown in
   the run summary (and under **Settings → Pages**).

> If the workflow can't auto-enable Pages (some org policies block it), open
> **Settings → Pages**, set **Source = GitHub Actions**, then re-run the
> workflow from the **Actions** tab.

### Manual alternative (deploy from a branch)

Prefer not to use Actions? Because the site is just `index.html` at the repo
root, you can serve it directly:

1. **Settings → Pages**
2. **Source: Deploy from a branch**
3. Branch: `main`, folder: `/ (root)`, then **Save**.

## Local preview

It's a static file — open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```
