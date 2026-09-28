# Hajimi VRC VPM Listing

这个仓库发布以下 VRChat Creator Companion / VPM 软件包的清单：

- [Avatar Part Assembler](https://github.com/qq1299235059/avatar-part-assembler)
- [VRC UV Fix Tool](https://github.com/qq1299235059/vrc_uv_fix_tool)

订阅地址：<https://qq1299235059.github.io/hajimi_vrc_package/index.json>

发布页：<https://qq1299235059.github.io/hajimi_vrc_package/>

在 VCC 中打开 **Settings > Packages > Add Repository**，粘贴订阅地址即可。

## 自动更新

`source.json` 中的 `githubRepos` 列出公开的包仓库。本仓库的 **Build VPM Listing** 工作流每 15 分钟检查这些仓库的 GitHub Release，并更新 GitHub Pages 上的 VPM 清单。也可以在 Actions 页面手动运行。

VRC UV Fix Tool 的 `package.json` 版本号更新并推送到 `main` 后，源仓库的发布工作流会创建对应的 `v<version>` tag、VPM ZIP 和 GitHub Release。订阅源在下一轮自动构建时收录新版本。

