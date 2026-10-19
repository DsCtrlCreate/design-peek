# 源览 · PSD 快速预览

源览是一款 Chrome 扩展，可在百度网盘网页版中预览已上传 PSD 的最终合成画面，不必先把完整源文件下载到电脑。

## 下载

请在本仓库的 **Releases** 页面下载最新的 `design-peek-v0.1.0.zip`。

GitHub 自动显示的 “Source code (zip)” 不是扩展安装包，请下载 Release 中单独上传、文件名以 `design-peek-` 开头的 ZIP。

## 安装

1. 下载并解压 `design-peek-v0.1.0.zip`。
2. 把解压后的文件夹放在固定位置，不要移动或删除。
3. Chrome 打开 `chrome://extensions/`。
4. 开启右上角“开发者模式”。
5. 点击“加载已解压的扩展程序”，选择解压后的文件夹。
6. 打开源览的“扩展程序选项”。
7. 使用设置页显示的扩展 ID 和回调地址，配置自己的百度开放平台应用。
8. 填写自己的 App Key，然后连接百度网盘。

详细步骤见 [安装说明](docs/INSTALL.md) 和 [百度授权配置](docs/BAIDU-OAUTH.md)。

## 个人 App Key 模式

当前版本用于 GitHub 公开测试：

- 每位用户使用 Chrome 为本地安装生成的扩展 ID。
- 每位用户在百度开放平台创建自己的应用。
- 每位用户填写自己的 App Key。
- 绝对不要把 Secret Key 填入扩展或发送给他人。

移动扩展文件夹、换电脑或重新加载另一个目录后，扩展 ID 可能改变，需要重新登记百度 OAuth 回调地址。

## 当前支持

- 百度网盘网页版识别 `.psd` / `.PSD`
- 预览 8-bit RGB 与灰度 PSD 的最终合成图
- RAW、RLE、ZIP、ZIP Prediction 合成图
- 本地生成并缓存 WebP 预览

暂不支持 PSB、16/32-bit、CMYK/Lab PSD。未以兼容模式保存合成图的 PSD 也可能无法预览。

## 隐私

PSD 数据从百度网盘服务直接传输到用户浏览器，并在浏览器本地解析。本扩展没有作者运营的文件中转服务器。

详见 [隐私说明](PRIVACY.md) 和 [安全说明](SECURITY.md)。

## 代码说明

本仓库用于发布安装包和使用文档，不提供完整开发源代码。Chrome 扩展运行所需的编译后 JavaScript 会包含在安装包内。
