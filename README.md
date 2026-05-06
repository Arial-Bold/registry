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
  <a href="https://dolphindepot.org/submit/">Submit Your App</a>
</p>

## About

**Dolphin Depot** is a homebrew app store for Nintendo GameCube. It allows users to browse, download, and install homebrew applications directly on their console.

This repository serves as the public registry of all applications available through Dolphin Depot. Each entry contains a manifest file that describes the application, where to download it from, and how to package it for distribution. The Dolphin Depot indexer periodically scans this registry, processes new releases, and makes them available to end users.

Anyone can submit their homebrew application by opening a pull request. For a step-by-step walkthrough, see the [Submit Your App guide](https://dolphindepot.org/submit/).

## Submitting Your App

### 1. Choose a slug

Your app slug is the directory name under `registry/`. It must:

- Be lowercase alphanumeric with hyphens (e.g. `my-cool-app`)
- Match the pattern `^[a-z0-9]+(-[a-z0-9]+)*$`
- Be unique across the registry

### 2. Create your app entry

Each entry is required to provide a manifest file in `registry/<slug>/`:

**`manifest.json`** describes your application. You can author it by hand using the [manifest schema reference](https://dolphindepot.org/docs/manifest-schema/), or generate it interactively with the [manifest.json generator](https://dolphindepot.org/tools/manifest-json-generator/).

Make sure your release archive follows the expected layout — see the [packaging guide](https://dolphindepot.org/docs/distribute/) for the standard your app needs to follow to be compatible with the GC homebrew ecosystem.

Additionally you can provide assets:
- **`banner.png`** 96x32px image displayed as app icon
- **`screenshot{0-2}.png`** up to 3 640x480px screenshots
- **`hero.png`** 640x160px background image displayed in app details
- **`opening.bnr`** GameCube banner file shown in the launchers like Swiss — generate one with the [opening.bnr generator](https://dolphindepot.org/tools/opening-bnr-generator/)

### 3. Open a pull request

Add the manifest and any assets, then open a PR against `main`.
