# forge-releases-lens

Public GitHub Releases for **Forge-Lens**, the AI-powered manufacturing video work analysis app.

This repo also hosts the **reusable build/sign/release workflow** used by all 6 Forge release repos (`forge-releases-{lens,spc,fmea,8d,sop,doe}`).

- App: https://forge-tools.work/forge-lens
- Source code (private): `iyulab/forge`
- Sibling release repos: forge-releases-{spc, fmea, 8d, sop, doe}

## Workflow

`./.github/workflows/build.yml` is the canonical pipeline. Caller workflows in the 5 sibling repos delegate to it via `uses:`.

Triggered by:
- `repository_dispatch` from `iyulab/forge/.github/workflows/release.yml` on tag push or manual dispatch.
- Code signing is delegated to `iyulab/code-sign` via `sign-request` event.

## Releases

See https://github.com/iyulab/forge-releases-lens/releases

Auto-update endpoint (electron-updater): `https://github.com/iyulab/forge-releases-lens/releases/latest`
