# GhostFrame Binary Distribution (`Ghost`)

Official prebuilt pure-binary release channel for **GhostFrame v4.0 LTS** (Linux Server, Headless Core CLI, Windows Desktop Client, iStoreOS `0Ghost` Side-Router, and iOS Dual Unsigned IPAs).

## Quick Install & Downloads

### Linux Server (`gft-server`)
```bash
bash <(curl -fsSL https://github.com/Spittingjiu/Ghost/releases/latest/download/install.sh)
```

### iStoreOS / OpenWrt ARM64 Side-Router (`0Ghost`)
Compatible with BusyBox `ash`:
```sh
curl -fsSL https://github.com/Spittingjiu/Ghost/releases/latest/download/install-0ghost.sh | sh
# 国内宽带镜像加速可选：
curl -fsSL https://ghfast.top/https://github.com/Spittingjiu/Ghost/releases/latest/download/install-0ghost.sh | sh -s -- --mirror https://ghfast.top
```

### Windows Desktop Client (`GhostFrame-Pro`)
Direct download (`amd64`, zero external runtime required):
```text
https://github.com/Spittingjiu/Ghost/releases/latest/download/GhostFrame-Pro-windows-amd64.exe
```

### iOS OmniSign / ESign Source URL
```text
https://github.com/Spittingjiu/Ghost/releases/latest/download/source.json
```

Verify downloads against `checksums.txt` in each [Release](https://github.com/Spittingjiu/Ghost/releases).
