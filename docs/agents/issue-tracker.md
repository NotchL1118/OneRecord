# Issue tracker: GitHub

本仓库的任务和规格存放在 GitHub Issues，通过 gh CLI 操作。
仓库：NotchL1118/OneRecord。运行命令前从 git remote 确认目标仓库。

## 常用操作

- 创建：gh issue create --title "..." --body-file <file>
- 读取：gh issue view <number> --json number,title,body,labels,comments
- 列表：gh issue list --state open --json number,title,body,labels
- 评论：gh issue comment <number> --body-file <file>
- 标签：gh issue edit <number> --add-label "..." / --remove-label "..."
- 关闭：gh issue close <number> --comment "..."

多行正文先写入临时文件，再通过 --body-file 传入。

技能要求“发布到任务跟踪系统”时，创建 GitHub Issue。
技能要求“获取相关任务”时，读取对应 Issue。

## Pull requests as a triage surface

**PRs as a request surface: no.**

## Wayfinding

地图使用一个带 wayfinder:map 标签的 Issue。
子任务通过 GitHub 子 Issue 关联；不可用时，在子任务正文写
Part of #<map>，并在地图正文维护任务清单。

子任务类型标签为 wayfinder:research、wayfinder:prototype、
wayfinder:grilling 或 wayfinder:task。

阻塞关系优先使用 GitHub 原生 Issue dependencies；
不可用时，在正文顶部写 Blocked by: #<number>。
仅在所有阻塞项关闭且任务无人领取时开始任务，按地图顺序选择。
领取时将任务分配给当前开发者；完成后评论结果、关闭任务，
并在地图的 Decisions-so-far 中记录结果链接。
