# ansilic-resources-test
test
## 资源下载与更新

本仓库通过 gh-proxy.com 加速下载，IDE 使用固定清单地址检查 Skills 和芯片开发库的更新。

### IDE 更新源

在「工具 → 资源更新 → 设置」中填写下面的地址，点击「验证并保存」，再点击「检查更新」。

https://gh-proxy.com/https://raw.githubusercontent.com/zw611824/ansilic-resources-test/main/resources.json

### 仓库结构

- `main` 分支存放 `resources.json` 更新清单。
- `skills` 分支存放各 Skill 的 ZIP 包。
- `SDK` 分支存放各型号芯片开发库的 ZIP 包。

清单中的 ZIP 下载地址也使用 gh-proxy.com 加速。IDE 按资源独立下载，并校验 SHA-256，完成后按界面提示重启生效。

### 发布新版本

1. 将带版本号的 ZIP 上传到对应分支。
2. 更新 `main` 分支中对应资源的 `version`、`url` 和 `sha256`。
3. ZIP 内的 `VERSION` 必须与清单版本一致。

加速地址是在原始 GitHub Raw 地址前加上 `https://gh-proxy.com/`，例如：

https://gh-proxy.com/https://raw.githubusercontent.com/zw611824/ansilic-resources-test/skills/as32-build-debug-v1.0.2.zip

更新源地址保持固定。后续发布只需修改清单中的对应资源记录。下载速度和可用性取决于加速站及当前网络情况。
