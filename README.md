# noban — desktop releases

This repo hosts the public release artifacts for **[noban.gg](https://noban.gg)** — a local-first CS2 skin arbitrage desktop app for Windows. The source repository is private; only installers, checksums, and the auto-update feed live here.

## Download

Grab the latest installer from the [Releases page](https://github.com/ucsandman/noban-releases/releases/latest):

- `noban-Setup-<version>.exe` — Windows installer (NSIS)
- `SHA256SUMS.txt` — SHA-256 checksums for every asset
- `latest.yml` — auto-update feed consumed by the app (you can ignore it)

**Windows only for now.** macOS is planned; don't trust any non-Windows binary claiming to be noban.

## Unsigned during early access — verify the checksum

Early-access builds are **not code-signed yet**, so Windows SmartScreen will warn on first run ("Windows protected your PC" → More info → Run anyway). That warning is expected for unsigned software; code signing is in progress.

Because the binary is unsigned, **verify the SHA-256 before installing**:

```powershell
Get-FileHash .\noban-Setup-1.0.0.exe -Algorithm SHA256
```

Compare the output against the matching line in `SHA256SUMS.txt` from the same release. If they differ, do not run the installer.

## What noban is

- Cross-venue CS2 skin price radar (CSFloat ⇄ Steam Market + 7 read-only price feeds) with after-fee, after-hold profit math
- **Simulation by default** — real trading requires an explicit opt-in AND a paid license; a missing license can never make the app more permissive
- Local-first: your data, credentials, and database never leave your machine
- Steam Market auto-buying is unsupported by design (ToS)

Questions or issues: [noban.gg](https://noban.gg) · support@noban.gg

## Support

If my tools save you time, you can support my work here:

[![Sponsor on GitHub](https://img.shields.io/badge/GitHub%20Sponsors-%E2%9D%A4-db61a2?logo=githubsponsors&logoColor=white)](https://github.com/sponsors/ucsandman)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-%E2%98%95-ffdd00?logo=buymeacoffee&logoColor=black)](https://buymeacoffee.com/wes_sander)
