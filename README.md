# Skymod

Skymod is a mobile-first, Arabic-first audio PWA prototype built with React, TypeScript, Vite, Three.js and Web Audio.

## Source package

The project archive is stored as eight Base64 segments in `bootstrap/archive.part.00` through `bootstrap/archive.part.07`. The GitHub Actions workflow reconstructs the archive, installs dependencies, applies three TypeScript typing fixes, builds the app and deploys it to GitHub Pages.

To reconstruct the source locally:

```sh
cat bootstrap/archive.part.* | base64 --decode > skymod-source.tar.xz
tar -xJf skymod-source.tar.xz
```

## Enable deployment

Open **Settings → Pages → Build and deployment → Source** and select **GitHub Actions**. The workflow then runs on pushes to `main` or can be started manually from the Actions tab.

## Project status

This is an MVP prototype, not a production music service. Built-in demo soundscapes are synthesized locally. Commercial music streaming, licensed catalogues, accounts, social features and several advanced audio tools need additional services and implementation. See `FEATURE_STATUS.md` and `ARCHITECTURE.md` in the extracted source for details.
