# 一键拼图跨平台远程升级仓库

这个仓库用于公开存放“一键拼图”的统信、Windows 安装包和远程升级规则。

## 当前版本

- 统信 UOS：`1.0.7`
- Windows：`1.0.6`
- UOS 最低可用版本：`1.0.7`
- Windows 最低可用版本：`1.0.6`
- 强制升级：已开启
- 本次更新：修复部分统信 UOS 软件源没有 `python3-pil.imagetk` 导致安装被拦截的问题。

## 当前文件

- `update.json`：双平台升级规则。
- `releases/uos-one-click-collage_1.0.7_all.deb`：统信 UOS 修复版安装包。
- `releases/one-click-collage_1.0.6_windows.exe`：Windows 程序。
- `remote_upgrade_publisher.html`：生成双平台升级规则的网页工具。

## 升级行为

1. 统信旧版本启动后会要求升级到 `1.0.7`。
2. Windows 继续使用 `1.0.6`，不受本次 UOS 依赖修复影响。
3. UOS `1.0.7` 只依赖 `python3`、`python3-tk`、`python3-pil`。

升级规则地址：

```text
https://raw.githubusercontent.com/6408396-star/one-click-collage-update/main/update.json
```
