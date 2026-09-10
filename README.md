# 家里的故事中文版 · 纯净迁移版

本项目只是《家里的故事中文版》的**纯净网页迁移版本**，使用 Ruffle 在现代浏览器中运行原始 Flash 游戏。没有修改游戏剧情、关卡或素材，没有移除游戏内原作者标识，也没有添加广告、统计脚本或付费功能。页面不包含原托管网站的导航、推荐和广告；原始 SWF 内已有的内容和链接保持不变。

## 原游戏与作者

- [原作者 Justwo Games 官方网站](https://www.justwogames.com/)
- [《家里的故事中文版》原发布页面（7k7k）](https://www.7k7k.com/swf/182368.htm)
- [原始 SWF 资源](https://flash.7k7k.com/cms/cms10/20170706/1930289704/9.swf)

7k7k 链接是本次迁移所用中文版的来源页面，不代表本项目是官方版本。本项目与原作者及 7k7k 没有关联，游戏版权归原作者所有。本仓库没有授予游戏素材或程序的再许可。

## 在线游玩

GitHub Pages 启用后访问：<https://sunay04.github.io/home-story/>

## GitHub Pages 部署

所有运行资源已放在仓库中，无需构建，也无需外部 CDN。

1. 将文件提交到 `main` 分支。
2. 在仓库 **Settings → Pages → Build and deployment** 中选择 **Deploy from a branch**。
3. 选择 **main** 和 **/ (root)**，点击 **Save**。
4. 等待 GitHub Pages 部署完成后，打开上方地址。

仓库中的 `.nojekyll` 用于直接发布静态资源；相对资源路径兼容 `/home-story/` 子目录。

## 本地试玩

安装 Python 3 后，在仓库目录运行：

```sh
python -m http.server 8000 --bind 127.0.0.1
```

打开 <http://127.0.0.1:8000/>。不要直接双击 HTML 文件。

## 技术说明

- 原游戏文件：`game/game.swf`，保持下载原样。
- 游戏原始尺寸：800 × 550。
- 播放器：[Ruffle](https://ruffle.rs/)，固定为 `@ruffle-rs/ruffle` 0.6.0，许可文件保留在 `ruffle/` 中。
- 网页关闭游戏对 JavaScript 的访问权限。
- 已校验游戏 SHA-256、SWF 解压长度及播放器发布包完整性。尚未完成完整流程试玩，Ruffle 对部分 Flash 行为可能存在兼容性差异。

游戏 SHA-256：

```text
3a7960f9c54b7f4ab1f08d2bf02f28fd1514bcbeec71862976c6a0695b0143dd
```
