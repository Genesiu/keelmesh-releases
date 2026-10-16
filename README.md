# Keelmesh downloads

Official Beta downloads and release notes for Keelmesh Ops.

- [Website](https://keelmesh.com/) · [中文官网](https://keelmesh.com/zh/)
- [Latest Beta downloads](https://github.com/Genesiu/keelmesh-releases/releases)
- [Release history](https://keelmesh.com/changelog/) · [中文更新日志](https://keelmesh.com/zh/changelog/)

This repository contains documentation and downloadable binaries. The application source repository is private. GitHub automatically offers “Source code” ZIP/tar archives of **this documentation repository**; they contain README and CHANGELOG, not Keelmesh application source.

## Which asset should I download?

| Asset | Purpose |
|---|---|
| `macOS-universal.dmg` | macOS Ops management console; Apple Silicon and Intel. Recommended for Mac users. |
| `macOS-cli.zip` | Matching universal `deepops` CLI, transactional installation utility and notices for AI tools/scripts. |
| `macOS-update.zip` | Source-free App/CLI kit consumed by the in-app updater; not a separate product installer. |
| `Keelmesh-*.manifest.json` + `.sig` | Offline release-Root signatures for the complete DMG and CLI kit. |
| `macos-beta.json` | Signed update-channel envelope. The app verifies it with its built-in public key. |
| `manifest.json`, `SHA256SUMS` | Version, platform, signing status, sizes and checksum metadata. |
| `README.txt`, `RELEASE_NOTES.*.md` | Installation, rollback and version notes. |

## Latest release

Beta 18 reduces delays as signed audit history grows. Every operation still rehashes historical bytes and verifies new records; tampering and authorization errors remain fail-closed. It includes Beta 17’s Windows inventory correction and top-bar network shortcut.

## Updates

Beta 16 adds Settings → Software updates: automatic checks after unlock and every 6 hours, background downloads, installation after active work finishes, and rollback. Devices, Keychain identities and AI grant scope/permissions/expiry/revocation are retained. Beta 13 and older need one manual DMG upgrade to obtain this feature. An existing CLI is updated together with the App; absence of a CLI does not silently install a system command.

## Platforms

The current public Ops management console is the macOS 12+ universal Beta. A separate Ubuntu 24.04 x64 management preview exists in development but is not published as this Beta. A Windows Ops GUI has not been released. Linux, macOS and Windows **Agents** are remote endpoints, not management consoles. Keelmesh Tunnel/VPN is a separate product preview.

This Beta is ad-hoc signed, **not Apple-notarized**, and does not claim completed independent security certification. In-app replacement requires write access to the existing product locations.

---

普通 Mac 用户下载 DMG 即可。CLI ZIP 用于 AI 与脚本；update ZIP 由软件内更新器使用。JSON、签名和校验文件用于验证发布包。

本仓库只公开下载包与说明文档，不公开产品主体源码。GitHub 自动生成的“Source code”压缩包是本说明仓库的归档。
