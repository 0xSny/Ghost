# Kestrel (`Kestrel-RTC` / `ksl4://`)

**Kestrel** 是一款纯静态编译的双栈加密传输与全平台代理套件（基于自适应 **Kestrel-RTC** UDP 引擎 + Chrome 后量子 **uTLS** 双栈容灾，完全兼容 `ksl4://` 与旧版 `gft3://` / `gft2://` 节点链接）。

本仓库仅分发各平台官方预编译二进制产物、一键安装脚本、校验和及 iOS 软件源索引。

---

## 一键部署安装

### 1. Linux 服务器 (`kestrel-server` / `ksl`)

```bash
bash <(curl -fsSL https://github.com/Spittingjiu/Ghost/releases/latest/download/install.sh)
```

> 无人值守部署示例（监听 443 + UDP 端口跳跃 + 自动迁移旧版 `/etc/gft` 配置）：
> ```bash
> bash <(curl -fsSL https://github.com/Spittingjiu/Ghost/releases/latest/download/install.sh) --unattended --port 443 --hop 25000-32000
> ```

---

### 2. iStoreOS / OpenWrt 旁路由 (`KestrelBox` / `kbox`，兼容 BusyBox `ash`)

```sh
curl -fsSL https://github.com/Spittingjiu/Ghost/releases/latest/download/install-kbox.sh | sh
```

国内宽带镜像加速可选：

```sh
curl -fsSL https://ghfast.top/https://github.com/Spittingjiu/Ghost/releases/latest/download/install-kbox.sh | sh -s -- --mirror https://ghfast.top
```

- 自动从旧版 `0Ghost` (`/etc/0ghost/config.json`) 无损迁移节点配置至 `/etc/kbox/config.json`。
- 安装完成后可在路由器 LuCI 后台 **服务 -> KestrelBox** 或直接访问 `http://<路由器IP>:19080/` 管理。

---

### 3. Windows 桌面端 (`Kestrel Pro`)

直接从 [Latest Release](https://github.com/Spittingjiu/Ghost/releases/latest) 下载单文件免安装版：
- **`Kestrel-Pro-windows-amd64.exe`**（首次启动自动将旧版 `%USERPROFILE%\.gft\client.json` 无损迁移至 `%USERPROFILE%\.kestrel\client.json`）。

---

### 4. iOS 双版本软件源（全能签 / ESign / AltStore）

添加官方云端软件源 `source.json`：

```text
https://github.com/Spittingjiu/Ghost/releases/latest/download/source.json
```

包含以下两款独立未签名包：
- **Kestrel Duo** (`Kestrel-Duo-Unsigned.ipa`)：系统级全局通道 + iOS 18 控制中心快捷开关。
- **Kestrel Air** (`Kestrel-Air-Unsigned.ipa`)：轻量免扩展权限单进程后台保活版（适合普通个人证书）。
