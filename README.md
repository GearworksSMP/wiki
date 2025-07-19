# Gearworks Wiki

This repository contains the Gearworks SMP Wiki, built with MkDocs and automatically deployed to GitHub Pages.

## Automated Deployment

This wiki is automatically built and deployed using GitHub Actions whenever changes are pushed to the main branch. The deployed wiki is available at [wiki.gearworkssmp.com](https://wiki.gearworkssmp.com).

### How it works

1. When changes are pushed to the main branch, a GitHub Actions workflow is triggered
2. The workflow builds the wiki using MkDocs with the Material theme
3. The built site is deployed to GitHub Pages
4. The custom domain (wiki.gearworkssmp.com) is configured via a CNAME file

### Custom Domain Setup

The wiki is configured to use the custom domain `wiki.gearworkssmp.com`. To maintain this configuration:

1. Ensure the `CNAME` file in the `docs/` directory contains `wiki.gearworkssmp.com`
2. Make sure your DNS provider has the following records:
   - An A record pointing to GitHub Pages IP addresses (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153)
   - Or a CNAME record pointing to `gearworkssmp.github.io`

## Local Development

This wiki uses MkDocs. For full documentation visit [mkdocs.org](https://www.mkdocs.org).

### Python activate env
```
python -m venv .venv # make the environment if needed
source ./.venv/bin/activate.fish # activate the environment
```

### Install
```
pip install mkdocs
pip install mkdocs-material
```

### Commands

* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

### Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        CNAME     # Custom domain configuration.
        ...       # Other markdown pages, images and other files.
    .github/
        workflows/
            build-deploy.yml  # GitHub Actions workflow file.
