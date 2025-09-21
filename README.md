# Mix It Up — Release Archive

This repository is a **read‑only archive** of historical Mix It Up releases originally published at `SaviorXTanren/mixer-mixitup`. It exists to preserve past installers, source archives, and changelogs in one place for reference and reproducibility.

> Looking for active development and new releases? This is not it.

## What’s here

- Original release assets: `.zip`, `.exe`, `.msi`, and `Changelog.html` files as they were published.
- Source archives for each tag (`source-<tag>.zip`) that correspond to the historical tag contents.
- A `checksums.sha256` file per release listing SHA‑256 hashes for all assets in that release.

## What’s not here

- No working code tree; no builds are produced from this repo.
- No issue tracking or PRs. This repo is archival only.

## Authenticity and integrity

- **Code signing:** most releases from recent years are Authenticode‑signed with our EV code‑signing certificate and include a trusted timestamp. Some older releases are **unsigned**; this mirrors the original state at time of release.
- **Checksums:** every release includes `checksums.sha256`. Verify downloads before use.

## Verify checksums

**Windows (PowerShell):**
```powershell
# In the folder where you downloaded the assets
Get-FileHash * -Algorithm SHA256 | Format-Table -Auto
# Compare values with the contents of checksums.sha256
```

**macOS/Linux:**
```bash
# Verifies each file against the list
sha256sum -c checksums.sha256
# or
shasum -a 256 -c checksums.sha256
```

## Verify Windows signatures (if present)

**PowerShell:**
```powershell
Get-AuthenticodeSignature .\MixItUp-Setup.exe | Format-List *
```

**signtool (if installed):**
```powershell
signtool verify /pa /all .\MixItUp-Setup.exe
```

## Provenance

- Source: releases originally published at `SaviorXTanren/mixer-mixitup`.
- Each archived release notes the original publish date where available.
- File names and contents are preserved as originally shipped.

## Release structure

Each GitHub release in this archive mirrors a historical tag and typically contains:

- `MixItUp.zip` (or equivalent installer package)
- `Changelog.html`
- `source-<tag>.zip`
- `checksums.sha256`

## Safety notes

- Old unsigned builds may trigger SmartScreen or AV heuristics. Use checksums to confirm integrity.
- This archive is provided **as‑is** for historical reference and reproducibility.

---

*Mix It Up — Release Archive*