# 一键拼图跨平台远程升级仓库

这个仓库用于公开存放“一键拼图”的统信、Windows 安装包和远程升级规则。

## 当前版本

- 最新版本：`1.0.4`
- 最低可用版本：`1.0.4`
- 强制升级：已开启
- 本次新增：在导出前预览照片和模板的实际排版，可从预览窗口直接生成高清拼图。

## 文件说明

- `update.json`：软件启动时读取的远程升级规则。
- `releases/uos-one-click-collage_1.0.4_all.deb`：统信 UOS 双击安装包。
- `releases/one-click-collage_1.0.4_windows.exe`：Windows 版程序。
- `remote_upgrade_publisher.html`：生成统信和 Windows 升级规则的网页工具。
- `update_url_GitHub.txt`：软件内置的 GitHub 升级规则地址。

## 本次升级演示

发布顺序如下：

1. 先上传 `1.0.4` 安装包并确认可下载。
2. 再把 `update.json` 的 `latest_version` 和 `min_supported_version` 改成 `1.0.4`。
3. 保持 `force_update` 为 `true`。
4. 统信旧版 `1.0.3` 启动时会提示必须升级，并打开 `.deb` 下载地址。
5. 带升级检查的 Windows 旧版会打开 `.exe` 下载地址。
6. 安装 `1.0.4` 后，软件可正常打开并使用“预览拼图”。

## 以后发布新版本

例如发布 `1.0.5`：

1. 上传统信 `.deb` 和 Windows `.exe` 新安装包。
2. 把 `update.json` 中两个平台的版本号都改成 `1.0.5`。
3. 分别更新 `download_url` 和 `windows_download_url`。
4. 最后保存 `update.json`，强制升级即生效。

升级规则地址：

```text
https://raw.githubusercontent.com/6408396-star/one-click-collage-update/main/update.json
```

已经发出去但不含远程检查代码的早期版本无法被远程控制。统信从 `1.0.3`、Windows 从 `1.0.4` 开始读取本仓库规则。
