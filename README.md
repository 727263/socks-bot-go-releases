# socks-bot-go Releases

本仓库**仅发布 Linux 二进制**，用于后台「版本管理」检查更新与下载。

- 源码不公开
- 下载：Releases 中的 `socksbot-linux-amd64`
- 版本号见根目录 `VERSION`

## 下载最新版

```bash
curl -fsSL -o socksbot-linux-amd64 \
  https://github.com/727263/socks-bot-go-releases/releases/latest/download/socksbot-linux-amd64
chmod +x socksbot-linux-amd64
```

版本号：

```bash
curl -fsSL https://raw.githubusercontent.com/727263/socks-bot-go-releases/main/VERSION
```

## 发布流程（维护者）

1. 本地交叉编译：`GOOS=linux GOARCH=amd64 go build -ldflags="-s -w -X github.com/727263/socks-bot-go/internal/version.Version=x.y.z" -o socksbot-linux-amd64 ./cmd/socksbot`
2. 更新本仓库 `VERSION` 为 `x.y.z`
3. GitHub Release 打 tag `vX.Y.Z`，上传附件 `socksbot-linux-amd64`
