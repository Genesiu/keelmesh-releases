# Keelark downloads

## Windows Access Preview 13 · 2026-10-30

[Windows Setup](https://keelmesh.com/updates/access/0.2.3-preview.13/Keelark-Access-0.2.3-preview.13-Windows-amd64-Setup.exe) · [Release notes and signatures](https://github.com/Genesiu/keelmesh-releases/releases/tag/access-v0.2.3-preview.13) · [All platforms](https://keelmesh.com/access/#availability)

Windows prepares the original isolated identity, system services and Wintun when submitting an invitation. Prepared applications connect after approval without a second installer; offline users resume the original application on reopening and unlocking. Legacy protected service paths remain compatible. Matching servers renew an expired delivery envelope only for the same identity and unchanged valid grant; scope and grant expiry cannot grow.

Windows Server 2019 actual packet, service restart, legacy identity continuity and overlay-upgrade acceptance passed. Existing connection files, identities and authorization remain; desktop updates preserve existing network service processes. Settings → Version and updates checks after unlock and every two hours while visible. Network component upgrades remain separate and may reconnect.

Windows x64 Preview only. Authenticode, ordinary-user human UAC, clean Windows 10/11 and actual 360 clearance remain pending. macOS/Linux client versions are unchanged. Linux servers remain controlled-trial only; product source stays private.

[Website](https://keelmesh.com/) · [中文官网](https://keelmesh.com/zh/) · [All releases](https://github.com/Genesiu/keelmesh-releases/releases) · [Release history](https://keelmesh.com/changelog/)

This repository distributes binaries and documentation. **Keelark product source remains private.** GitHub's automatic “Source code” archives contain this download repository's release documentation and automation. The explicitly named OpenVPN MPL source-kit asset contains only the third-party engine and its adapter/build sources, not proprietary product source or user profiles.

## Keelark Access · 安全接入

### 0.2.3 Preview 2 · Routes on macOS, Windows and Linux

[Downloads and release notes](https://github.com/Genesiu/keelmesh-releases/releases/tag/access-v0.2.3-preview.2) · [Platform guides](https://keelmesh.com/access/) · [中文安装说明](https://keelmesh.com/zh/access/) · [Linux guide](README.linux-client.md)

All resources → Routes shows OS routes, known tunnel origins/interfaces, overlapping subnets and actual IP egress. Diagnostics require window unlock, read local state on demand and never start a tunnel or change routes. Red means overlap; unknown route origins stay unknown. Automatic signed resource catalogs remain supported by the native connection protocol. Routes do not grant network access.

Windows x64, macOS Universal 12+ and Ubuntu 22.04 x64 desktop include the route page. Linux ARM64 CLI is cross-built, without an ARM64 desktop or native acceptance claim. Matching Linux client and desktop DEBs must be installed together. Native acceptance covers this Mac, Windows Server 2019 x64 and Ubuntu 22.04 x64; clean Windows 10/11, macOS Intel and the full Linux polkit/browser interaction matrix remain pending.

Existing connections, identities, signed grants and running per-profile services are retained. Standard packages reuse the accepted Preview 3 / sequence 9 network core. **Linux gateway/server packages remain at 0.2.2-preview.3; no gateway update is needed for route diagnostics.** Windows GUI update availability advances to sequence 23 after acceptance; installation remains explicit and waits for active work. macOS GUI automatic updates remain unchanged this batch to avoid replacing the separate OpenVPN flavor. Linux uses manual matching DEBs.

### Choose the correct Mac package

| Download | Requirements and protocols |
|---|---|
| `*-macOS-universal.dmg` / `.zip` | macOS 12+, Apple Silicon and Intel; native hybrid protocol, WireGuard compatibility and Routes. **No OpenVPN engine.** |
| `*-macOS26-arm64.dmg` / `.zip` | macOS 26+, Apple Silicon only; adds the limited OpenVPN preview and Routes. Keep this flavor when upgrading an existing OpenVPN installation. |

OpenVPN imports self-contained certificate-based Tunnelblick `.ovpn` profiles. TUN, UDP/TCP-client and explicit IPv4 split routes are supported. Scripts, plugins, external key files, TAP, full-tunnel and interactive password/MFA are not supported by this preview. OpenVPN uses classical TLS, separate from Keelark native hybrid post-quantum connections. Native signed resource catalogs do not apply to OpenVPN profiles. Windows, Linux and Intel OpenVPN engines are not released.

| Other Access asset | Purpose |
|---|---|
| `*-Windows-amd64-Setup.exe` | Windows x64 installation wizard. |
| `*-Windows-amd64.zip` | Complete Windows client; extract all files and run the included launcher. |
| `*-Linux-amd64-desktop.deb` | Ubuntu 22.04 x64 desktop GUI; install the matching client DEB. |
| `*-Linux-*-client.deb` / `*-client.tar.gz` | CLI and background-service client; x64 or cross-built ARM64. |
| [Linux server controlled trial](https://keelmesh.com/zh/access/#server-trial) | Public server downloads are paused; request a controlled trial. |
| `OPENVPN-SOURCE-MPL.tar.gz` | Required third-party OpenVPN engine and adapter sources, under MPL-2.0. |
| `*.manifest.json` + `*.manifest.sig`, `SHA256SUMS` | Release-root signatures and full hashes. These do not replace OS code signing. |

Preview packages are verified by the established Ed25519 release root. Apple Developer ID/notarization and Windows Authenticode are pending. Do not disable antivirus or certificate verification. Keep the old app for rollback; never restore expired/revoked grants. Upgrades do not reset profile identity. Downloading does not authorize access: native invitations still require administrator approval and signed network permissions.

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

产品主体源码不公开。路由页已提供 macOS、Windows x64 和 Ubuntu 22.04 x64 桌面版；Linux ARM64 仅 CLI 交叉构建。OpenVPN 独立版仅适用于 macOS 26+ Apple Silicon。服务端仅受控申请试用，配套网关已更新。公开 MPL 源码包只含第三方引擎及适配器。安装包下载不代表获得设备或网络访问权限。
