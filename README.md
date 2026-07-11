# 一键拼图跨平台远程升级仓库

这个仓库用于公开存放“一键拼图”的统信、Windows 安装包和远程升级规则。

## 当前版本

- 统信 UOS：`1.0.5`
- Windows：`1.0.5`
- 最低可用版本：`1.0.5`
- 强制升级：已开启
- 本次更新：底部按钮功能分色，蓝色用于预览、金橙色用于生成、浅色用于目录工具。

## 当前文件

- `update.json`：双平台升级规则。
- `releases/uos-one-click-collage_1.0.5_all.deb`：统信 UOS 安装包。
- `releases/one-click-collage_1.0.5_windows.exe`：Windows 程序。
- `remote_upgrade_publisher.html`：生成双平台升级规则的网页工具。

## 升级行为

1. 统信 `1.0.4` 启动后会提示升级并打开 `.deb` 下载地址。
2. Windows `1.0.4` 启动后会提示升级并打开 `.exe` 下载地址。
3. 安装或替换为 `1.0.5` 后即可正常使用新配色界面。

升级规则地址：

```text
https://raw.githubusercontent.com/6408396-star/one-click-collage-update/main/update.json
```

统信从 `1.0.3`、Windows 从 `1.0.4` 开始支持远程升级检查。
