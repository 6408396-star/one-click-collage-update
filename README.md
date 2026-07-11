# 统信一键拼图远程升级仓库

这个仓库用于公开存放“统信一键拼图”的安装包和远程升级规则。

## 当前版本

- 最新版本：`1.0.4`
- 最低可用版本：`1.0.4`
- 强制升级：已开启
- 本次新增：在导出前预览照片和模板的实际排版，可从预览窗口直接生成高清拼图。

## 文件说明

- `update.json`：软件启动时读取的远程升级规则。
- `releases/uos-one-click-collage_1.0.4_all.deb`：统信 UOS 双击安装包。
- `remote_upgrade_publisher.html`：生成升级规则的网页工具。
- `update_url_GitHub.txt`：软件内置的 GitHub 升级规则地址。

## 本次升级演示

发布顺序如下：

1. 先上传 `1.0.4` 安装包并确认可下载。
2. 再把 `update.json` 的 `latest_version` 和 `min_supported_version` 改成 `1.0.4`。
3. 保持 `force_update` 为 `true`。
4. 旧版 `1.0.3` 启动时会提示必须升级，并打开 `1.0.4` 下载地址。
5. 安装 `1.0.4` 后，软件可正常打开并使用“预览拼图”。

## 以后发布新版本

例如发布 `1.0.5`：

1. 上传新安装包到 `releases/uos-one-click-collage_1.0.5_all.deb`。
2. 把 `update.json` 中的两个版本号改成 `1.0.5`。
3. 把 `download_url` 改成新安装包地址。
4. 最后保存 `update.json`，强制升级即生效。

升级规则地址：

```text
https://raw.githubusercontent.com/6408396-star/one-click-collage-update/main/update.json
```

已经发出去但不含远程检查代码的早期版本无法被远程控制；`1.0.3` 及后续版本可以读取本仓库规则。
