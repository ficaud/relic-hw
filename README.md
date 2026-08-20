<div align="center">
<img src="docs/img/relic-logo.png" width="150" alt="Relic Core logo">

<br/>
<br/>
<br/>

# R.E.L.I.C
<i>Recovery and Encryption via Lagrange Interpolated Components</i>

[![Relic-core](https://img.shields.io/badge/Relic_core-v1.4.2-orange)](https://github.com/ficaud/relic-core)
[![Docs](https://img.shields.io/badge/Docs-GitHub_Pages-blue)](https://ficaud.github.io/relic-hw/)

</div>

**Relic Hardware** is a step-by-step guide that teaches **complete beginners** how to build a Relic device entirely from scratch — a physical device that safely stores your most sensitive secrets using [relic-core](https://github.com/ficaud/relic-core).

## Documentation

The full documentation is hosted on **GitHub Pages** and rendered with **MkDocs**:

- **[Read the docs](https://ficaud.github.io/relic-hw/)**

## Local development

To build and preview the documentation locally:

```bash
pip install -r requirements.txt
mkdocs serve
```

Then open <http://localhost:8000>.

### Stop the server

If the server is running in the foreground of your terminal, simply press `Ctrl+C` in that same terminal.

If it's running in the background (for example, started with `&` or from a different terminal), you'll need to find and kill the process instead. On macOS/Linux:

```bash
pkill -f "mkdocs serve"
```

Or, to target the specific port:

```bash
lsof -ti :8000 | xargs kill
```

The site is automatically rebuilt and deployed to GitHub Pages on every push to `main` (see `.github/workflows/deploy.yml`). The deployment uses the official GitHub Pages Actions (`actions/deploy-pages`), which publish the built site directly as a Pages artifact — it does **not** rely on GitHub pushing from the `gh-pages` branch.

> **One-time setup:** In **Settings → Pages → Build and deployment → Source**, select **GitHub Actions** (instead of "Deploy from a branch"). This is required for the workflow to publish the site.

## Versioning

The documentation is versioned with [`mike`](https://github.com/jimporter/mike), which publishes multiple versions of the docs and adds a version selector in the navigation bar.

### Release via git tag (recommended)

The CI workflow is configured to deploy a versioned release automatically when you push a `v*` tag. No manual `mike` command needed:

```bash
git tag v1.0.0
git push origin v1.0.0
```

This triggers the workflow, which:
- Extracts the version from the tag (`v1.0.0` → `1.0.0`)
- Deploys that version with `mike`
- Moves the `latest` alias to the new version and sets it as default
