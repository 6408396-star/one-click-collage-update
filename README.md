# 统信一键拼图远程升级仓库

这个仓库用于公开存放“统信一键拼图”的远程升级规则。

## 文件说明

- `update.json`：软件启动时读取的远程升级规则。
- `releases/uos-one-click-collage_1.0.3_all.deb`：当前 1.0.3 安装包，使用英文文件名，方便生成原始下载链接。
- `remote_upgrade_publisher.html`：以后发布强制升级规则时使用的网页工具。
- `update_url_GitHub.txt` / `update_url_Gitee.txt`：软件里要填写的升级规则地址模板。

## GitHub 使用方法

1. 登录你的 GitHub 账号。
2. 新建公开仓库：`one-click-collage-update`。
3. 把本目录里的所有文件上传到仓库根目录。
4. 打开 `update.json`，点击 `Raw`，复制浏览器地址。
5. 这个地址通常是：

```text
https://raw.githubusercontent.com/6408396-star/one-click-collage-update/main/update.json
```

6. 把这个地址写入统信电脑上的：

```text
/opt/uos-one-click-collage/update_url.txt
```

## Gitee 使用方法

1. 登录你的 Gitee 账号。
2. 新建公开仓库：`one-click-collage-update`。
3. 把本目录里的所有文件上传到仓库根目录。
4. 打开 `update.json`，点击“原始数据/Raw”，复制浏览器地址。
5. 这个地址通常是：

```text
https://gitee.com/你的Gitee用户名/one-click-collage-update/raw/main/update.json
```

6. 把这个地址写入统信电脑上的：

```text
/opt/uos-one-click-collage/update_url.txt
```

## 以后强制升级

假设以后发布 1.0.3，并要求 1.0.3 不能继续使用：

1. 上传新的安装包到 `releases/uos-one-click-collage_1.0.3_all.deb`。
2. 修改 `update.json`：

```json
{
  "enabled": true,
  "latest_version": "1.0.3",
  "min_supported_version": "1.0.3",
  "force_update": true,
  "prompt_optional_update": true,
  "download_url": "https://raw.githubusercontent.com/6408396-star/one-click-collage-update/main/releases/uos-one-click-collage_1.0.3_all.deb",
  "message": "软件已发布新版本，请先升级后再继续使用。"
}
```

3. 保存后，低于 `min_supported_version` 的软件会提示必须升级并退出。

## 重要说明

已经发出去、但没有远程升级检查代码的旧版本，无法被远程强制失效。需要先安装 1.0.3 或更新版本，后续才可以通过这里的 `update.json` 控制升级。
