# Changelog

Public Beta releases. Application source code remains private.

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
