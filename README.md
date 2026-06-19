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

### Automatic with GitHub Actions (recommended)

One quick switch is needed before the first deploy:

1. Open **Settings → Pages** and set **Source = GitHub Actions**. GitHub
   doesn't allow the Actions token to enable Pages on its own, so this single
   click has to be done by hand the first time.
2. Run the **Deploy to GitHub Pages** workflow — re-run it from the **Actions**
   tab, or push any change. It runs automatically on every push to `main` or
   `claude/affectionate-cerf-kd83ex`.
3. When the run finishes, the live URL appears in the run summary and under
   **Settings → Pages**.

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
