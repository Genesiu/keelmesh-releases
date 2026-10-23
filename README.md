# Keelark downloads

[Website](https://keelmesh.com/) · [中文官网](https://keelmesh.com/zh/) · [All releases](https://github.com/Genesiu/keelmesh-releases/releases) · [Release history](https://keelmesh.com/changelog/)

This repository distributes binaries and documentation. **Keelark product source remains private.** GitHub's automatic “Source code” archives contain this download repository's documents. The explicitly named OpenVPN MPL source-kit asset contains only the third-party engine and its adapter/build sources, not proprietary product source or user profiles.

## Keelark Access · 安全接入

### Cross-platform downloads · 0.2.2 Preview 3

[macOS Universal, Windows x64 and Linux downloads](https://github.com/Genesiu/keelmesh-releases/releases/tag/access-v0.2.2-preview.3) · [Platform requirements and guides](https://keelmesh.com/access/) · [中文安装说明](https://keelmesh.com/zh/access/)

Automatic signed resource catalogs after device approval and resource/policy changes. Upgrade the gateway and management service to enable automatic publication. Existing connections, identities and signed grants are retained. macOS Apple Silicon, Windows Server 2019 x64 and Ubuntu 22.04 x64 were tested; Linux ARM64 is cross-built, with native acceptance pending. These platform downloads and their automatic-update channels continue at Preview 3.

### Separate OpenVPN preview · 0.2.3 Preview 1

**macOS 26 or later, Apple Silicon only. This is not a Universal package.**

[OpenVPN preview downloads and release notes](https://github.com/Genesiu/keelmesh-releases/releases/tag/access-v0.2.3-preview.1) · [中文支持范围](https://keelmesh.com/updates/access/0.2.3-preview.1/RELEASE_NOTES.zh.md)

Import a self-contained certificate-based Tunnelblick `.ovpn` profile and connect from Keelark without running Tunnelblick. TUN, UDP/TCP-client and explicit IPv4 split routes are supported. Scripts, plugins, external key files, TAP, full-tunnel and interactive password/MFA authentication are not supported by this preview. OpenVPN uses classical TLS, separate from Keelark native hybrid post-quantum connections. Native signed resource catalogs do not apply to OpenVPN profiles. Existing connections, identities and authorization are retained.

Windows, Linux, Intel and older macOS OpenVPN builds have not been released. This optional download does not advance the cross-platform automatic-update channels. macOS applications are ad-hoc signed; Apple Developer ID signing and notarization are not completed. Preview use and manual opt-in are required.

| Access asset | Purpose |
|---|---|
| `*-macOS-universal.dmg` / `.zip` | Preview 3 macOS client for Apple Silicon and Intel; see the platform guide. |
| `*-macOS26-arm64.dmg` / `.zip` | Separate Preview 1 OpenVPN client for macOS 26+ Apple Silicon only. |
| `*-Windows-amd64-Setup.exe` | Windows x64 installation wizard. |
| `*-Windows-amd64.zip` | Complete Windows client; extract all files and run the included launcher. |
| `*-Linux-*-desktop.deb` | Ubuntu 22.04 x64 desktop GUI; install the matching client package. |
| `*-Linux-*-client.deb` / `*-client.tar.gz` | CLI and background-service client. |
| `*-Linux-*-server.tar.gz` | Linux gateway kit; includes installation and rollback instructions. |
| `OPENVPN-SOURCE-MPL.tar.gz` | Required third-party OpenVPN engine and adapter sources, under MPL-2.0. |
| `*.manifest.json` + `*.manifest.sig`, `SHA256SUMS` | Release-root signatures and full artifact hashes. These do not replace operating-system code signing. |

Native invitations require administrator device approval and signed network permissions. A download does not grant access. Profile removal is explicit; upgrades do not reset identities or signed grants. Earlier releases remain available for compatibility and rollback.

## Keelark Ops · Remote operations

[Ops Beta 40](https://github.com/Genesiu/keelmesh-releases/releases/tag/v0.12.41-beta.40) · [Product and platform guide](https://keelmesh.com/ops/)

The published Ops management console is the macOS 12+ Universal Beta. A Windows Ops GUI is not published. Linux, Windows and macOS Agents are remote endpoints, separate from the management console. Access and Ops have independent versions and permissions.

| Ops asset | Purpose |
|---|---|
| `*-macOS-universal.dmg` | macOS management console. |
| `*-macOS-cli.zip` | Matching `deepops` CLI and installation utility for AI tools and scripts. |
| `*-macOS-update.zip` | App/CLI kit used by the in-app updater. |
| `macos-beta.json` | Signed update-channel envelope verified against the built-in release key. |
| `manifest.json`, `SHA256SUMS`, `*.manifest.sig` | Version, signing status and package verification. |

Updates retain device pairings, Keychain identities and AI grant device scope, permissions, expiry and revocation. Installation waits for active work to finish and supports rollback. The Beta remains ad-hoc signed and not Apple-notarized. Review each release's notes and requirements before installation.

---

产品主体源码不公开。OpenVPN 预览仅适用于 macOS 26 及以上的 Apple 芯片 Mac；旧 Mac、Windows 和 Linux 请继续使用 Preview 3。公开的 MPL 源码包只包含第三方引擎及适配器。安装包下载不代表获得任何设备或网络访问权限。
