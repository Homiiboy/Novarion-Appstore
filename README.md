# Novarion App Store

A curated third-party ZimaOS App Store maintained by Novarion.

The store uses the current ZimaOS App Store v2 source format and publishes generated store metadata to the `gh-pages` branch.

## Available apps

### Velaris

Velaris is a cinematic Jellyfin-compatible web client. Jellyfin remains the backend for authentication, users, libraries, playback, watch state and transcoding.

Stable image: `ghcr.io/homiiboy/velaris-web:1.0.0`

## Repository structure

```text
Novarion-Appstore/
├── Apps/
│   └── Velaris/
│       ├── docker-compose.yml
│       └── icon.svg
├── .github/workflows/
│   └── publish-store.yml
├── store-config.json
└── supported-languages.json
```

## Publishing

Every push to `main` validates and builds the v2 store with the official IceWhaleTech build action and publishes `dist/` to the `gh-pages` branch.

Public store base URL after publishing:

```text
https://cdn.jsdelivr.net/gh/Homiiboy/Novarion-Appstore@gh-pages
```

For this URL to be usable by ZimaOS without authentication, this repository must be public.

## Velaris source

Velaris Web is maintained separately in `Homiiboy/velaris-web` on the `velaris` branch. This repository only contains the ZimaOS App Store package definition and does not duplicate the Velaris application source.
