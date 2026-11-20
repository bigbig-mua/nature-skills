# Nature Skills 的 CC Switch 精简分支

本分支供 CC Switch 安装和更新 `nature-polishing` 及其共享依赖 `nature-shared`。手动工作流会从上游 `main` 同步两个完整的技能目录和 `LICENSE`，并清理上游已删除的旧文件。此 README 在 `cc-switch` 分支维护。

## 1. 查看上游是否有更新

- 查看 [nature-polishing 提交历史](https://github.com/Yuan1z0825/nature-skills/commits/main/skills/nature-polishing)。
- 查看 [nature-shared 提交历史](https://github.com/Yuan1z0825/nature-skills/commits/main/skills/nature-shared)。
- 如需确认许可证是否有改动，查看 [LICENSE 提交历史](https://github.com/Yuan1z0825/nature-skills/commits/main/LICENSE)。

要精确比较，在 [cc-switch 提交记录](https://github.com/bigbig-mua/nature-skills/commits/cc-switch/) 打开最近一次同步提交，找到提交说明中 `Upstream:` 后的上游提交号。用它替换下面链接里的 `<上次同步的上游提交号>`，再查看比较页的 **Files changed**。两个技能目录或许可证有改动时，运行工作流即可。

```text
https://github.com/Yuan1z0825/nature-skills/compare/<上次同步的上游提交号>...main
```

## 2. 在 GitHub 手动同步

1. 打开 [Sync Nature Skills for CC Switch](https://github.com/bigbig-mua/nature-skills/actions/workflows/sync-cc-switch.yml)。
2. 点击 **Run workflow**。在 **Use workflow from** 下拉框选 **`main`**，再点击弹窗里的 **Run workflow**。
3. 等运行记录显示绿色对勾。这里的 `main` 是工作流所在分支，同步结果写入 `cc-switch`。如果日志显示 `Already synchronized with upstream`，三个路径已与上游一致。

更新这两个技能时请使用上述工作流。仓库首页的 **Sync fork** 会按提交合并上游，可能把其他目录带进 `cc-switch`。

## 3. 在 CC Switch 更新

1. 确认仓库来源是 `bigbig-mua/nature-skills`，分支是 `cc-switch`。
2. 打开 **Skills → 已安装 → 检查更新**。
3. 对显示「可更新」的 `nature-polishing` 和 `nature-shared` 执行更新。两个技能在同一个应用中启用，润色时调用 `nature-polishing`。
