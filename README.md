# SOP 工作台 · 软件发布

本仓库仅提供通用软件安装包、免安装版和签名更新文件。源码仓库保持私有；发布内容不包含用户 SOP、现场照片、项目缓存或更新签名私钥。

[下载最新版本](https://github.com/yhanxi/SOP-work-releases/releases/latest)

Windows x64：下载 `SOPStudio-Setup-VERSION-x64.exe` 安装，或下载 ZIP 解压后运行 `SOPStudio/SOPStudio.exe`。

## 软件内更新

0.4.1 起默认从此公开仓库检查和下载更新，无需 GitHub 登录。启动后自动检查，每 6 小时复查，可关闭；左下角“软件更新”或帮助菜单可手动检查。

日常兼容更新只下载约 444 KB 的程序文件。下载后验证发布者 Ed25519 签名、SHA256 和版本；保存并退出后替换程序，保留旧版备份和本机项目恢复缓存。升级 Electron 运行环境时使用完整安装程序。

如果 GitHub 下载慢，可在“软件更新 → 下载源设置”配置自有 HTTPS 备用下载目录。目录需提供 Release 中的 `latest.json` 和相应 `SOPStudio-VERSION-app.asar`；所有来源仍验证签名。未预置第三方公共代理。

## 校验与使用

每次发布附带 `SHA256-VERSION.json`。安装包未作 Windows 代码签名，程序更新使用单独的签名校验。ASAR 和更新清单供软件自动使用，普通用户请选择 EXE 或 ZIP。

SOP 可离线编写。文件、图片、标注、页序和固定沿用内容保存于本机项目；Word 中各元素可独立编辑。更新不上传项目数据。
