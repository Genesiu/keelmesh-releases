# Changelog

## Access 0.2.3 Preview 2 — 2026-10-24

- Add All resources → Routes: OS routing tables, tunnel names/interfaces, exact IP egress and red subnet-overlap descriptions. Unknown origins remain explicit. Local read-only diagnostics require unlock and never start a tunnel or change routes.
- Publish signed Windows x64 Setup/ZIP, macOS Universal and separate macOS 26+ arm64 OpenVPN DMG/ZIP, Ubuntu 22.04 x64 desktop and x64/ARM64 CLI packages. ARM64/Intel native and full clean-OS interaction matrices remain pending.
- Accept native Windows Server 2019 x64 upgrade and authenticated route/HTTP checks; Ubuntu 22.04 x64 matching-DEB upgrade, non-root GUI startup, hybrid tunnel/resources/revocation; existing Mac live route page. Preserve 9 Windows, 8 Linux and 14 Mac configuration/identity files and existing network service processes.
- Reuse accepted Preview 3 / sequence 9 standard network core. Gateway/server remains 0.2.2-preview.3. Only the Windows GUI signed update feed advances to sequence 23; macOS GUI and all runtime feeds remain unchanged to preserve OpenVPN flavor compatibility.
- OpenVPN remains a limited separate macOS 26+ Apple Silicon preview using classical TLS. Windows/Linux/Intel OpenVPN engines are not released. Product source remains private; MPL kit includes only required third-party engine/adapter sources. OS code-signing gates remain open.
- [Downloads](https://github.com/Genesiu/keelmesh-releases/releases/tag/access-v0.2.3-preview.2) · [中文验收和回滚说明](https://keelmesh.com/updates/access/0.2.3-preview.2/RELEASE_NOTES.zh.md).

## Access 0.2.2 Preview 3 — 2026-10-22

- Publish resource catalogs automatically after approval and resource/policy changes; reconcile at startup and retry every 15 seconds.
- macOS, Windows and Linux signed-directory support; actionable missing catalog, authorization, network and verification errors.
- Preserve identity, Owner binding, current signed scope, expiry and revocation. Catalogs cannot grant additional access. Ops AI controls unchanged.
- GUI sequence 21 / runtime sequence 9; 11 signed binary packages after native Mac, Windows Server 2019 x64 and Ubuntu 22.04 x64 acceptance. ARM64 cross-built; formal OS signing remains pending.
- [Downloads and detailed acceptance](https://github.com/Genesiu/keelmesh-releases/releases/tag/access-v0.2.2-preview.3). Application source remains private; retain previous releases for rollback.

## Access Linux client Preview 3 — 2026-10-17

- Add Ubuntu 22.04 x64 desktop and Linux x64 / ARM64 CLI and service packages, with separate DEB and tar.gz downloads.
- Keep identities local, require administrator invitation / fingerprint approval / signed network grant, and install via a fixed OS-authorized helper.
- Preserve identities and active service PIDs through shared-file upgrades and rollback; refuse package removal until installed client connections are explicitly retired.
- Validate native Ubuntu 22.04 x64 enrollment, hybrid encrypted traffic, service restart recovery, other-user rejection, tampered grants, package upgrades/rollback and GUI startup. ARM64 native acceptance and full desktop authentication matrix remain open.
- Publish release-root signatures and exact hashes. Update six-language website and guides. Source remains private; Ops Beta 20, AI permissions and existing Mac/Windows releases are unchanged.

## Access 0.1.10 Preview 2 — 2026-10-17

- Rename Keelark VPN to **Keelark Access / 安全接入** across the app, tray, installers, shortcuts, packages, website and download guides.
- Retain identity/configuration/key namespaces, service IDs, bundle ID, Windows uninstall identity and CLI compatibility. Keep previous releases available for rollback.
- Verify previous VPN release → Access upgrade and rollback on Apple Silicon/Linux x64, and Windows Server 2019 client replacement with unchanged configuration and background service PIDs.
- Continue existing release-root component sequences. Preserve required hybrid encryption, signed network policy and separate Ops AI grants.
- Add /access/ product pages in six languages; preserve /vpn/ links. Core application source remains private. Existing preview signing/native/clean-OS gates remain open.

## VPN 0.1.10 Preview 1 — 2026-10-17

- Rename software, installers and shortcuts to Keelark VPN, preserving existing identities/configuration.
- Add macOS universal DMG/ZIP and Linux x64/ARM64 server kits alongside Windows x64 Setup/ZIP.
- Add guarded Linux installation, explicit gateway provisioning and rollback, and Windows app-file transaction backups.
- Validate Apple Silicon package/app/protocol, Server 2019 client update and Linux x64 installation/gateway/update/rollback. Native Intel/ARM64, clean Windows 10/11, formal signing and full production acceptance remain open.
- Keep required hybrid encryption, invitation/approval/signed network policy, private source and separate Ops AI grants.


## VPN 0.1.9 RC1 public preview — 2026-10-16

- Publish original accepted Windows x64 RC1 Setup and ZIP without changing their bytes.
- Include installation guides, hashes and detached release-root signatures; retain legacy embedded Keelmesh naming.
- Require administrator-issued device invitations, fingerprint approval and signed network policies.
- Keep Ops releases and AI grants independent. No macOS/Linux public installer, IPsec implementation or public SDK is included.
- Authenticode, complete human UAC, clean Windows 10/11 install, reboot recovery and independent security review remain open.


Public Beta releases. Application source code remains private.

## 0.12.37-beta.20-keelark

2026-10-16 · Beta 20 · sequence 67

Keelmesh is now Keelark.

- The console, website, AI handoff instructions and product family use the Keelark name.
- New macOS installations use Keelark.app. Existing installations can upgrade through the same signed channel and retain their existing path.
- Device identities, pairing records, host snapshots and AI grants remain in place. Existing CLI commands and SSH aliases continue to work.
- Includes Beta 19 host snapshot caching. No endpoint reinstall is required.

The built-in release Root verifies the signed update target, exact artifact size and SHA-256, component/platform and monotonic release sequence. Device scope, read/write permission, one-use confirmation, the 3-hour default, expiry and revocation are unchanged.

Beta 13 and earlier need one manual DMG upgrade to gain the update checker. Finish GUI tasks, quit and replace Keelark.app; retain Application Support and Keychain. From Beta 14, use Settings → Software updates. No endpoint reinstall is needed.

macOS 12+ universal Beta; ad-hoc signed, not Apple-notarized. In-app replacement requires write access to the existing application and CLI locations. A live hung candidate is never force-killed; close it before recovery. Windows Ops GUI is not released; Ubuntu 24.04 x64 remains a separate testing preview.

The existing keelmesh.com domain, release repository, configuration paths, CLI name and protocol identifiers are retained for compatibility.


## 0.12.37-beta.19-host-snapshots

2026-10-16 · Beta 19 · sequence 66

Keep host information when the console restarts.

- Restore the last successful OS, IP addresses and CPU, memory and disk snapshot on startup. OS filters and address grouping work before connecting.
- Cards, lists and device details show when values were fetched. Online status is queried separately; cached values do not mean a device is online.
- Opening a device refreshes cached data. A failed refresh preserves the previous values and displays the failure.
- No background fleet inventory is added. Existing encryption, AI scope, permissions, three-hour expiry and revocation remain enforced when enabled.

The built-in release Root verifies the signed update target, exact artifact size and SHA-256, component/platform and monotonic release sequence. Device scope, read/write permission, one-use confirmation, the 3-hour default, expiry and revocation are unchanged.

Beta 13 and earlier need one manual DMG upgrade to gain the update checker. Finish GUI tasks, quit and replace Keelmesh.app; retain Application Support and Keychain. From Beta 14, use Settings → Software updates. No endpoint reinstall is needed.

macOS 12+ universal Beta; ad-hoc signed, not Apple-notarized. In-app replacement requires write access to the existing application and CLI locations. A live hung candidate is never force-killed; close it before recovery. Windows Ops GUI is not released; Ubuntu 24.04 x64 remains a separate testing preview.

After the first upgrade, each device needs one successful inventory fetch to populate its cache. No endpoint upgrade is required.


## 0.12.37-beta.18-audit-prefix

2026-10-16 · Beta 18 · sequence 65

Faster operations with large audit histories.

- Verified audit history is reread and hashed on every write; unchanged prefixes reuse earlier verification, while new entries are verified individually.
- Audit tampering, truncation, invalid appends and permission failures still stop operations. Rotation and concurrent writers preserve one signed chain.
- Fixes execution delays reproduced on a Mac endpoint. The same audit improvement is included in the console, CLI and future endpoint installation packages.
- Retains the Windows inventory fix and the top-bar network topology shortcut from Beta 17.

The built-in release Root verifies the signed update target, exact artifact size and SHA-256, component/platform and monotonic release sequence. Device scope, read/write permission, one-use confirmation, the 3-hour default, expiry and revocation are unchanged.

Beta 13 and earlier need one manual DMG upgrade to gain the update checker. Finish GUI tasks, quit and replace Keelmesh.app; retain Application Support and Keychain. From Beta 14, use Settings → Software updates. No endpoint reinstall is needed.

macOS 12+ universal Beta; ad-hoc signed, not Apple-notarized. In-app replacement requires write access to the existing application and CLI locations. A live hung candidate is never force-killed; close it before recovery. Windows Ops GUI is not released; Ubuntu 24.04 x64 remains a separate testing preview.


## 0.12.37-beta.17-connectivity

2026-10-16 · Beta 17 · sequence 64

Windows host information and a direct network workspace entry.

- Windows host information uses local Win32 and .NET APIs. An unresponsive WMI CPU provider no longer blocks the complete overview.
- An unavailable CPU sample remains unknown and cannot produce a healthy resource-check result.
- Host information errors are labeled separately from endpoint connection state.
- Network topology and connectivity is available beside Quick navigation in the top bar, with a current-page indicator.

The built-in release Root verifies the signed update target, exact artifact size and SHA-256, component/platform and monotonic release sequence. Device scope, read/write permission, one-use confirmation, the 3-hour default, expiry and revocation are unchanged.

Beta 13 and earlier need one manual DMG upgrade to gain the update checker. Finish GUI tasks, quit and replace Keelmesh.app; retain Application Support and Keychain. From Beta 14, use Settings → Software updates. No endpoint reinstall is needed.

macOS 12+ universal Beta; ad-hoc signed, not Apple-notarized. In-app replacement requires write access to the existing application and CLI locations. A live hung candidate is never force-killed; close it before recovery. Windows Ops GUI is not released; Ubuntu 24.04 x64 remains a separate testing preview.


## 0.12.37-beta.16-updater — 2026-10-16

Signed in-app updates, safe restart and rollback.

- Software updates in Settings checks after unlock and every 6 hours, and notifies you when a newer signed release is available.
- Download and verification run in the background. Installation waits for terminals, transfers, tasks, AI calls and pending operation confirmations; the final restart refuses new work.
- A separate native helper replaces the App and an already installed CLI together. Replacement or startup-validation failure restores the previous products. A durable journal supports interrupted-install recovery.
- Settings offers an idle-safe restore of the previous version. Device state, Keychain identities and authorization records are retained.

## Security and authorization

The built-in release Root verifies the signed update target, exact artifact size and SHA-256, component/platform and monotonic release sequence. Device scope, read/write permission, one-use confirmation, the 3-hour default, expiry and revocation are unchanged.

## Upgrade

Beta 13 and earlier need one manual DMG upgrade to gain the update checker. Finish GUI tasks, quit and replace Keelmesh.app; retain Application Support and Keychain. From Beta 14, use Settings → Software updates. No endpoint reinstall is needed.

## Known limitations

macOS 12+ universal Beta; ad-hoc signed, not Apple-notarized. In-app replacement requires write access to the existing application and CLI locations. A live hung candidate is never force-killed; close it before recovery. Windows Ops GUI is not released; Ubuntu 24.04 x64 remains a separate testing preview.

# Keelmesh Beta 16

0.12.37-beta.16-updater · 2026-10-16 · Beta

软件内检查更新，空闲安装与失败回滚。

- 设置新增“软件更新”：解锁后及每 6 小时自动检查；发现经过签名的新版本时提示。
- 下载与验证在后台进行。终端、传输、任务、AI 调用和待确认操作结束后才安装；最终重启阶段由程序阻止新操作进入。
- 独立原生辅助进程一起替换 App 与已安装的 CLI；替换或启动验证失败时恢复上一版本。保存事务记录以恢复中断的安装。
- 可在设置中等待空闲后恢复上一版本。设备配置、钥匙串身份和授权记录均保留。

## 安全与授权

内置发布公钥验证更新目标、完整安装包大小与 SHA-256、组件与平台，以及单调递增的发布序号。设备范围、读写权限、逐次确认、默认 3 小时、到期和撤销规则不变。

## 升级

Beta 13 及更早版本需手动升级一次 DMG 才能获得检查更新功能：结束 GUI 任务并退出，替换 Keelmesh.app，保留 Application Support 与钥匙串。Beta 14 起可用“设置 → 软件更新”。无需重装被控端。

## 已知限制

macOS 12+ 通用 Beta，临时签名，尚未 Apple 公证。软件内替换需要有权写入已有 App 与 CLI 位置；遇到仍在运行的卡死候选程序不会强杀，需先关闭再恢复。Windows Ops 图形管理端尚未发布；Ubuntu 24.04 x64 仍是单独测试版。

---

Beta 14 and Beta 15 were acceptance builds. Beta 15 was withdrawn after native macOS click validation found an unsupported browser confirmation dialog. Beta 16 fixes the native interaction and retains signed updates and graceful AI response draining.

## 0.12.37-beta.13-workspace-lifecycle — 2026-10-16

On-demand device connections and safe idle release.

- The fleet view reads Agent presence without opening business sessions or collecting every host’s metrics. Online, offline and unknown are separate from identity verification.
- New consoles use on-demand connections with a 5-minute idle retention, configurable from 1 to 120 minutes. Explicit existing settings are preserved.
- Closing a device tab releases idle channels; active tasks, transfers, terminals and AI calls can remain running. The carrier closes after its final operation ends.
- Online and offline devices use distinct colors. The workspace header shows real connection and data-fetching stages.
- Expired direct-TCP candidates no longer poison a healthy authenticated relay; identity, signature and protocol errors continue to fail closed.

## Security and authorization

Hybrid encryption and identity checks remain in place. Optional AI grants retain exact device scope, read-only/modification permissions, the 3-hour default, confirmation, expiry and revocation checks.

## Upgrade

Quit the app after finishing active GUI operations, back up the previous app, and replace it with Keelmesh.app. Keep Application Support and Keychain data. No endpoint reinstall is needed for these console changes. Explicit existing idle-retention settings remain unchanged; use Connection settings to reduce an older 60-minute value.

## Known limitations

macOS 12+ universal Beta, ad-hoc signed and not Apple-notarized. Direct connectivity depends on the network. Keelmesh Tunnel is a separate engineering preview.

---

# Keelmesh Beta 13

0.12.37-beta.13-workspace-lifecycle · 2026-10-16 · Beta

设备按需连接，空闲安全释放。

- 首页仅查询 Agent 在线状态，不自动建立所有设备的业务连接、获取全体指标或轮流打洞。在线、离线、未知与身份认证结果分开显示。
- 新装控制台默认按需连接，空闲保留 5 分钟，可设置为 1–120 分钟。已有明确配置继续保留。
- 关闭设备标签释放空闲连接；可保持任务、传输、终端和 AI 调用运行，最后一个操作结束后再释放。
- 在线/离线设备颜色明确区分；工作区顶部显示真实连接进度。“采集中”统一改为“获取中”。
- 修复直连 TCP 候选过期导致可用中转连接被错误阻断的问题；身份、签名和协议错误仍严格拒绝。

## 加密与授权

保留混合加密与设备身份验证。可选 AI 授权继续检查准确设备范围、只读/修改权限、默认 3 小时有效期、敏感操作确认、到期与撤销。

## 升级说明

先完成控制台中的活动操作并退出 App，备份旧版后替换 Keelmesh.app。保留 Application Support 与钥匙串，无需因本次控制台更新重装被控端。已有明确的空闲时间不被覆盖；旧版若设置为 60 分钟，可在连接设置中自行改小。

## 已知限制

macOS 12+ 通用 Beta，采用本地临时签名，尚未 Apple 公证。打洞能否成功取决于网络。Keelmesh Tunnel 是单独的工程预览产品。
