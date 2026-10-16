# Changelog

Public Beta releases. Application source code remains private.

## 0.12.37-beta.14-updater — 2026-10-16

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

# Keelmesh Beta 14

0.12.37-beta.14-updater · 2026-10-16 · Beta

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
