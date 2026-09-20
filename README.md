# Avatar Part Assembler VPM Listing

这个仓库发布 `avatar-part-assembler` 的 VRChat Creator Companion / VPM 软件包清单。

- VPM 清单：<https://qq1299235059.github.io/hajimi_vrc_package/index.json>
- 发布页：<https://qq1299235059.github.io/hajimi_vrc_package/>
- 源码仓库：<https://github.com/qq1299235059/avatar-part-assembler>

## 工作方式

`source.json` 将公开的 `avatar-part-assembler` 仓库列为软件包来源。源仓库中的 GitHub Actions 会读取根目录 `package.json`，生成 VPM ZIP（同时生成 UnityPackage），并按版本发布 GitHub Release。

本仓库的 **Build VPM Listing** 工作流使用 VRChat 官方的 `package-list-action`：

- 每 15 分钟自动检查源仓库的新 Release；
- 也可以在 Actions 页面手动运行；
- 生成 `Website/index.json` 和发布页；
- 发布页可以直接点击 **Add to VCC**，或把上面的清单 URL 添加到 VCC。

## 版本发布

更新 `avatar-part-assembler/package.json` 的 `version` 后推送到 `main`，源仓库会自动生成对应版本的 Release。VPM 清单会在下一次工作流运行时收录该版本。

`source.json` 中的 `githubRepos`、清单 URL 和仓库信息是发布配置的唯一来源；若更换仓库名或 GitHub Pages 地址，请同步更新这些字段。
