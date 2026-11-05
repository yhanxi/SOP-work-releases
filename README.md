# SOP 工作台 · 软件发布

SOP 工作台的 Windows 安装包、免安装版和签名更新文件。

- [源码与开发说明](https://github.com/yhanxi/SOP-work)
- [完整版本列表](https://github.com/yhanxi/SOP-work-releases/releases)
- [最新更新](https://github.com/yhanxi/SOP-work-releases/releases/latest)

## 首次安装

在版本列表中选择含完整安装包的版本。

| 文件 | 使用方式 |
| --- | --- |
| SOPStudio-Setup-VERSION-x64.exe | Windows 64 位安装程序，双击安装 |
| SOPStudio-VERSION-x64.zip | 免安装版，解压后运行 SOPStudio/SOPStudio.exe |
| SOPStudio-VERSION-app.asar | 软件内更新文件，由工作台下载并安装 |
| latest.json、SOP-update.json | 软件读取的签名更新清单 |
| SHA256-VERSION.json | 附件大小及 SHA256 校验值 |

完整安装包和日常小更新可能分别发布。若最新版本仅有 ASAR，请先安装带 EXE 或完整 ZIP 的版本，再通过软件内更新升级。ASAR 无法直接安装或运行。

## 软件内更新

在左下角「软件更新」或菜单「帮助 → 检查软件更新」中检查版本。可启用或关闭自动检查，发现更新后手动下载并重启安装。

日常兼容更新通常只下载几百 KB 的程序文件。更换 Electron 运行环境时，需使用完整安装程序。重启前请保存正在编辑的项目。

下载后，软件验证发布者 Ed25519 签名、SHA256、大小及版本。Windows 安装 EXE 的代码签名与此不同，目前安装包未配置 Windows 代码签名证书。

## 备用下载地址

GitHub 访问缓慢时，可在「软件更新 → 下载源设置」填写自己可访问的 HTTPS 下载目录。目录需提供同一版本的 latest.json 和 SOPStudio-VERSION-app.asar。所有下载源均通过内置公钥校验，不预置公共第三方代理。

## 模板与数据

发布包使用通用空白模板，公司名称、公司 Logo、编制、审核和批准等信息默认留空，使用者可自行填写。

项目保存在使用者选择的 .sop.json 文件中，自动恢复缓存另存在本机。软件更新功能只查询版本和下载程序，SOP 内容、现场照片和项目文件由使用者管理。分享项目文件时，文件内的公司信息与照片也会随之分享。

## 许可证

SOP 工作台项目代码采用 [MIT License](LICENSE)，源码见 [SOP-work](https://github.com/yhanxi/SOP-work)。依赖组件沿用各自的许可证，完整软件包内包含相应声明。
