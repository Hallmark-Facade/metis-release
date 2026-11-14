# metis-release

The release repository for **Metis** (Hallmark Facade). This is the one source of Metis release
content: the installer and the update asset live here as GitHub Release assets, and the product's
updater reads this repository - no other path serves update content.

## The assets

- **`Metis-Setup.exe`** - the Metis installer (published by plan 237).
- **`metis-release-<version>.tar`** - the update asset: the compiled release payload for version
  `<version>`, built by `npm run release` in `client/` and published by `npm run publish:github`.

The current release is `0.0.0` (a 44-file compiled payload).

## The no-content state

No Release has been published here yet. Until the first Release exists, a Check from the product
answers the plain sentence *no release published yet*; when a Release exists without the update
asset, it answers *no update published yet*. Neither is an error.

## Signing

Every asset in this repository is **unsigned** in v1: nothing here is signed, and signing is a
later round. The repository is read anonymously - no token is required.