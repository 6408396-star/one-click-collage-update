# 一键拼图跨平台远程升级仓库

这个仓库用于公开存放“一键拼图”的统信、Windows 安装包和远程升级规则。

## 当前版本

- 统信 UOS：`1.0.6`
- Windows：`1.0.6`
- 最低可用版本：`1.0.6`
- 强制升级：已开启
- 本次更新：使用新的蓝色机器人程序图标，双系统窗口和启动器保持一致。

## 当前文件

- `update.json`：双平台升级规则。
- `releases/uos-one-click-collage_1.0.6_all.deb`：统信 UOS 安装包。
- `releases/one-click-collage_1.0.6_windows.exe`：Windows 程序。
- `remote_upgrade_publisher.html`：生成双平台升级规则的网页工具。

## 升级行为

1. 统信 `1.0.5` 启动后会提示升级并打开 `.deb` 下载地址。
2. Windows `1.0.5` 启动后会提示升级并打开 `.exe` 下载地址。
3. 安装或替换为 `1.0.6` 后即可使用新图标版本。

升级规则地址：

```text
https://raw.githubusercontent.com/6408396-star/one-click-collage-update/main/update.json
```

统信从 `1.0.3`、Windows 从 `1.0.4` 开始支持远程升级检查。
