# CLAUDE.md — 课程项目主文件夹

## 项目背景

「暑期 AI 编程过渡课程」的课程项目主文件夹（当前处于阶段四）。根目录本身是一个 GitHub 仓库（`make20090408-cmyk-course`），内部包含两个独立的子项目仓库。

## 目录结构

| 目录 | 说明 |
|---|---|
| `手写数字/` | 手写数字识别项目（独立 git 仓库，GitHub 组织 IntelligenceAhead） |
| `game/` | 网页版游戏复刻 flappy-luffy（独立 git 仓库，GitHub 组织 IntelligenceAhead） |
| `daily-reports/` | AI 生成的每日汇报存档（属于主仓库） |
| `.claude/` | Claude Code 配置（commands 等，属于主仓库） |

## 约定与规则

1. **仓库隔离**：`手写数字/` 和 `game/` 是独立 git 仓库，被主仓库的 `.gitignore` 忽略。
   - 子项目的 git 操作（commit / push）用 `git -C <目录>` 在各自仓库内执行
   - 绝不在主仓库里 `git add` 子项目目录
2. **提交信息**：中文，动词开头、简洁（如「添加 2026-08-18 日报」）
3. **git 身份**：`make20090408-cmyk` + noreply 邮箱，已全局配置
4. **每日汇报**：用户输入 `/report-today` 时，按 `.claude/commands/report-today.md` 的流程执行：收集三个仓库当天工作 → 生成四部分日报 → 存入 `daily-reports/YYYY-MM-DD.md` → 提交到主仓库
5. **仓库命名规范**：`<GitHub 用户名>-<项目名>`，全小写、连字符分隔；GitHub 仓库名不能包含中文
