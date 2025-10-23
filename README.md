# asesmen-2025

repositori tugas mahasiswa

This repository is a Quarto "book" site. The site is built into the `docs/` folder (configured in `_quarto.yml`) and can be published to GitHub Pages.

How to publish the site (recommended):

1. Ensure the repository is pushed to GitHub and `main` is the default branch.
2. In the repository Settings -> Pages, set the Source to the `gh-pages` branch (or select `Deploy from a branch` and choose `gh-pages`). If the branch doesn't exist yet, the GitHub Actions workflow will create it on the next push to `main`.
3. The workflow `.github/workflows/deploy.yml` will deploy the content of `docs/` to the `gh-pages` branch whenever you push to `main` or trigger the workflow manually.

Local build (optional):

1. Install Quarto (https://quarto.org).
2. From the repository root, run:

```powershell
quarto render
```

This will produce the site HTML in the `docs/` folder. Commit and push the updated `docs/` files (or let CI deploy automatically if you prefer to keep `docs/` out of commits).

Notes and next steps:

- If you want GitHub Actions to build the Quarto site (instead of committing `docs/`), I can add a workflow step to install Quarto and run `quarto render` before deploying the generated `docs/`.
- To use a custom domain, add a `CNAME` file into `docs/` and configure DNS.
