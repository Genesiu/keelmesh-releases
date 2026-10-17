# Keelark Access · Linux client preview

Version: 0.1.10-preview.3-linux-20261017. Proprietary binaries; source is not published.

## Supported systems

- Desktop: Ubuntu 22.04 x64, GTK 3 and WebKitGTK 4.0. A normal desktop session with a polkit authentication agent is required. Ubuntu 24.04 desktop / ARM64 desktop are not yet supported by this package.
- CLI/service: systemd Linux x64 or ARM64, Python 3.8+, iproute2, TUN and permission to create network devices. Validated on Ubuntu 22.04 x64. ARM64 is cross-built; native ARM64 acceptance remains pending.
- macOS and Windows continue to use Preview 2; this release adds Linux clients and does not replace their packages. Existing Linux server packages remain available separately.

## Install

Verify the release signatures and SHA256SUMS before installing. Download the package for your architecture from the official release. On Ubuntu / Debian:

```sh
sudo apt install ./Keelark-Access-0.1.10-preview.3-linux-20261017-Linux-amd64-client.deb
```

For the desktop also install the matching desktop package:

```sh
sudo apt install ./Keelark-Access-0.1.10-preview.3-linux-20261017-Linux-amd64-desktop.deb
keelark-access-desktop
```

The CLI tar.gz includes a fixed-path installer for systems without dpkg. Extract into a new directory, verify the signed archive, then run `sudo python3 install-client.py install`. It installs shared files only and does not start a connection. `sudo python3 install-client.py rollback` restores the previous shared files. Use .deb upgrades for a dpkg-managed installation; do not mix installation methods.

## Headless enrollment and connection

The administrator issues a separate invitation and verifies the device fingerprint. Invitations and private keys must not be pasted into AI chats or command arguments. As your normal login user, put the invitation in a local file readable only by you:

```sh
umask 077
cat > "$HOME/access-invitation.txt"
# Paste the invitation locally, then press Ctrl+D.
keelark-access join --profile work --invite-file "$HOME/access-invitation.txt"
```

Send only the public fingerprint to your administrator. While approval is pending no network profile is installed. After the administrator approves signed device network permissions:

```sh
keelark-access refresh --profile work
sudo keelark-access install work
keelark-access status work
keelark-access list
keelark-access down work
keelark-access up work
```

Local administrator authentication is required for installation/removal. Normal connection control uses the owning user's authenticated local socket. The installed service starts at boot and reconnects with the same local identity; no SSH keys are required. Signed network permissions and their expiry remain enforced.

## Desktop

Open Keelark Access from Applications. Unlock your local identity, paste the administrator's invitation locally, wait for approval, and install the approved connection using the OS authorization prompt. Closing the interface leaves installed connections running. This preview has no Linux tray icon. A desktop login screen / polkit interaction on every Linux distribution has not been certified.

## Identity, upgrades and removal

Legacy storage and service identifiers intentionally remain `KeelmeshVPN` / `keelmesh-vpn` for compatibility. Client identities stay in `~/.config/KeelmeshVPN/enrollment/PROFILE/identity` with private permissions. Do not delete or share them. A package upgrade does not recreate identities, change signed grants or restart running profile managers. Active profiles use an isolated installed binary; updating their runtime requires an explicit profile maintenance step.

```sh
sudo keelark-access remove work
sudo apt remove keelark-access-desktop keelark-access-cli
```

Removal disconnects only the selected profile, archives its protected service configuration, and preserves the user's identity. The CLI .deb refuses removal while client profiles remain installed. Preview packages have release-root signatures but no distribution repository / automatic package update channel. Reinstall the previous signed package to roll back a .deb update.

## Security scope

Transport: X25519 + ML-KEM-768; identity: Ed25519 + ML-DSA-65. Access is a separate product from Ops. Ops AI scope, read/write rules, default three-hour expiry and revocation are not changed by installing Access. Access enrollment is a signed network grant, not an Ops AI grant.

Builds strip debug symbols and local paths; the UI is minified. No dedicated code encryption, obfuscation or anti-debug protection is included. Release signatures detect package changes; they do not prevent reverse engineering.

Contact: keelmesh@genesiu.com

## 中文快速说明

桌面预览支持 Ubuntu 22.04 x64，命令行提供 x64 / ARM64 包。ARM64 尚待真机验收，Ubuntu 24.04 桌面暂不支持。先用系统包管理器安装对应 client.deb，桌面环境再装 desktop.deb。普通用户通过 `keelark-access join` 使用本地私密邀请文件，管理员核对指纹并批准后执行 `refresh`，再用 `sudo keelark-access install 连接名` 安装。普通 `up / down / status / list` 不需要管理员权限。没有默认邀请码、密码或网络权限。

身份在本地生成并保留；接入授权必须由管理员签名。软件升级不重启已安装的连接服务，移除连接需明确执行 `sudo keelark-access remove 连接名`，仅断开所选连接。安装包为预览版，尚未完成全发行版桌面验证。
