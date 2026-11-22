# 可溯源加密压缩工具 · 产物仓库

本仓库只存放**打包产物**与更新清单，不包含任何源码。

- 源码仓库（私有）：https://github.com/duan-zehao/Traceable_encryption_compression_algorithm
- 本仓库（公开）：https://github.com/duan-zehao/traceable-encryption-releases

## 这里有什么

| 文件 | 用途 |
|---|---|
| `version.json` | 客户端更新清单：最新版本、最低可用版本、下载地址与 sha256 |
| `TraceableEncryptionTool-GUI.zip` | 程序内更新包（onedir 整目录） |
| `TraceableEncryptionTool-GUI.zip.sha256` | 更新包校验值 |
| `TraceableEncryptionTool-Setup.exe` | 首次安装器（Inno Setup） |

正式产物由源码仓库的 GitHub Actions（`release.yml`）在推送 `v*` tag 后构建并同步到这里。

## 请不要手动修改

- 任何文件都由 CI 生成并覆盖；手动改动会导致客户端校验失败或版本错乱。
- 如需发版，请在源码仓库按「dev → master → tag」流程操作。

## 客户端如何使用

客户端匿名拉取本仓库的 `version.json` 与 Release 资产，无需任何凭据；
下载后会校验 `sha256`，校验失败会拒绝更新。
