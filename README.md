<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/DolphinDepot/.github/refs/heads/main/logo-dark-mode.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/DolphinDepot/.github/refs/heads/main/logo-light-mode.svg" />
    <img alt="DolphinDepot" src="https://raw.githubusercontent.com/DolphinDepot/.github/refs/heads/main/logo-light-mode.svg" width="200" />
  </picture>
</p>

<p align="center">
  <a href="https://dolphindepot.org">Website</a> &middot;
  <a href="https://status.dolphindepot.org">Status</a> &middot;
  <a href="https://github.com/DolphinDepot/registry/pulls">Submit Your App</a>
</p>

## About

**Dolphin Depot** is a homebrew app store for Nintendo GameCube. It allows users to browse, download, and install homebrew applications directly on their console.

This repository serves as the public registry of all applications available through Dolphin Depot. Each entry contains a manifest file that describes the application, where to download it from, and how to package it for distribution. The Dolphin Depot indexer periodically scans this registry, processes new releases, and makes them available to end users.

Anyone can submit their homebrew application by opening a pull request.

## Submitting Your App

### 1. Choose a slug

Your app slug is the directory name under `registry/`. It must:

- Be lowercase alphanumeric with hyphens (e.g. `my-cool-app`)
- Match the pattern `^[a-z0-9]+(-[a-z0-9]+)*$`
- Be unique across the registry

### 2. Create your app entry

Each entry is required to provide Manifest file in `registry/<slug>/`:

**`manifest.json`** describes your application. The full JSON Schema is available at `manifest.schema.json`.

Additionallu you can provide images:
- **`banner.png`** 96x32px image displayed as app icon
- **`screenshot{0-2}.png`** up to 3 640x480px screenshots
- **`hero.png`** 640x160px background image displayed in app details

### 3. Open a pull request

Add both files and open a PR against `main`.
