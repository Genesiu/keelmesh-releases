# Keelark downloads

## Current Access release · 0.2.2 Preview 3
+
+[Download macOS, Windows and Linux](https://github.com/Genesiu/keelmesh-releases/releases/tag/access-v0.2.2-preview.3) · [Website](https://keelmesh.com/access/)

Automatic signed resource catalogs after approval and resource/policy changes; actionable errors. Upgrade both the gateway and management service to enable automatic publication. Existing connections, identities and signed grants are preserved. macOS Apple Silicon, Windows Server 2019 x64 and Ubuntu 22.04 x64 tested; Linux ARM64 is cross-built. Preview: OS platform signing and wider compatibility testing remain pending. Source stays private. GitHub-generated source archives contain download-repository documents, not product code.

## Keelark Access · 安全接入

[Linux client Preview 3](https://github.com/Genesiu/keelmesh-releases/releases/tag/access-linux-v0.1.10-preview.3) adds **Ubuntu 22.04 x64 desktop** and **x64 / ARM64 CLI and background service** clients. Install the desktop DEB together with the matching CLI DEB. ARM64 is cross-built; native acceptance is pending. Ubuntu 24.04 desktop is not supported by this package. [Linux installation guide](README.linux-client.md).

| Linux client package | Purpose |
|---|---|
| `Keelark-Access-*-Linux-amd64-desktop.deb` | Ubuntu 22.04 x64 desktop GUI; requires the matching CLI package and normal OS administrator authorization. |
| `Keelark-Access-*-Linux-{amd64,arm64}-client.deb` | CLI / background service for systemd Linux. Invitation, fingerprint approval and signed network permission are required. |
| `Keelark-Access-*-Linux-{amd64,arm64}-client.tar.gz` | CLI kit with fixed-path install and shared-file rollback for installations not managed by dpkg. |

Client upgrades preserve local identities and running per-profile managers. Profile removal is explicit and ownership-checked. Preview 3 is a Linux client release; macOS, Windows and Linux servers remain Preview 2 below.

[Keelark Access 0.1.10 Preview 2](https://github.com/Genesiu/keelmesh-releases/releases/tag/access-v0.1.10-preview.2) is the renamed Keelark VPN product. It connects verified devices to administrator-approved private services using required hybrid post-quantum encryption and signed per-device network permissions. Existing identities, profiles, service IDs, bundle ID and CLI commands remain compatible.

| Access package | Purpose |
|---|---|
| `Keelark-Access-*-Windows-amd64-Setup.exe` | Windows x64 installation wizard; retains the existing install/uninstall identity and background services. |
| `Keelark-Access-*-Windows-amd64.zip` | Complete Windows client; extract all files and run Start-Keelark-Access.cmd. |
| `Keelark-Access-*-macOS-universal.dmg` / `.zip` | macOS 12+ client for Apple Silicon and Intel; keep the old app outside Applications for rollback. |
| `Keelark-Access-*-Linux-{amd64,arm64}-server.tar.gz` | Linux secure-access gateway kit; install-server.py verifies the kit and supports retained-image rollback. Existing CLI/install paths remain compatible. |
| `*.manifest.json` + `*.manifest.sig`, `SHA256SUMS` | Independent release-root signatures and complete artifact hashes. These do not replace OS code signing. |

[Access downloads and platform guides](https://keelmesh.com/access/) · [中文：安全接入](https://keelmesh.com/zh/access/) · [All products](https://keelmesh.com/products/)

Invitation, device fingerprint approval and signed network policy are required; downloads grant no access. This remains a preview with formal OS signing and broader clean/native-machine acceptance incomplete. Ops and Access have separate versions and permissions. Ops Beta 20 and its AI authorization rules are unchanged. Earlier VPN-named releases and links remain available for compatibility and rollback.

Official Beta downloads and release notes for Keelark Ops (formerly Keelmesh).

- [Website](https://keelmesh.com/) · [中文官网](https://keelmesh.com/zh/)
- [Latest Beta downloads](https://github.com/Genesiu/keelmesh-releases/releases)
- [Release history](https://keelmesh.com/changelog/) · [中文更新日志](https://keelmesh.com/zh/changelog/)

This repository contains documentation and downloadable binaries. The application source repository is private. GitHub automatically offers “Source code” ZIP/tar archives of **this documentation repository**; they contain public documentation, not Keelark application source.

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

Beta 20 renames the product to Keelark. The console, website and AI handoff text use the new name. New installs use Keelark.app; existing installations keep their signed update channel, identities, configuration paths, AI grants and CLI commands. It includes Beta 19 host snapshot persistence. The current website domain and release repository URL remain unchanged for compatibility.

## Updates

Beta 16 adds Settings → Software updates: automatic checks after unlock and every 6 hours, background downloads, installation after active work finishes, and rollback. Devices, Keychain identities and AI grant scope/permissions/expiry/revocation are retained. Beta 13 and older need one manual DMG upgrade to obtain this feature. An existing CLI is updated together with the App; absence of a CLI does not silently install a system command.

## Platforms

The current public Ops management console is the macOS 12+ universal Beta. A separate Ubuntu 24.04 x64 management preview exists in development but is not published as this Beta. A Windows Ops GUI has not been released. Linux, macOS and Windows **Agents** are remote endpoints, not management consoles. Keelark Access (formerly Keelark VPN) is a separate product preview.

This Beta is ad-hoc signed, **not Apple-notarized**, and does not claim completed independent security certification. In-app replacement requires write access to the existing product locations.

---

普通 Mac 用户下载 DMG 即可。CLI ZIP 用于 AI 与脚本；update ZIP 由软件内更新器使用。JSON、签名和校验文件用于验证发布包。

本仓库只公开下载包与说明文档，不公开产品主体源码。GitHub 自动生成的“Source code”压缩包是本说明仓库的归档。
