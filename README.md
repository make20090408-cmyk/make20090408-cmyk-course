# 课程项目主文件夹

「暑期 AI 编程过渡课程」阶段四的标准示例仓库。展示了用 Claude Code 搭建「每日汇报与自动化记录系统」的完整结构。

## 这个仓库是什么

一个收纳所有课程项目的主文件夹。它同时是一个 GitHub 仓库，里面又装着两个独立的项目仓库：

| 目录 | 内容 | 仓库 |
|---|---|---|
| `手写数字/` | 手写数字识别项目（digit_recognition.html） | 独立仓库（如 `<用户名>-digit`） |
| `game/` | 网页版经典游戏复刻（flappy-luffy.html） | `<用户名>-game` |
| `daily-reports/` | 每日汇报存档 | 保存在本仓库 |
| `.claude/` | Claude Code 命令与技能配置 | 保存在本仓库 |

## 核心机制

- **`/report-today` 命令**：在 `.claude/commands/` 中定义，触发后 AI 汇总当天的工作，生成四部分结构的汇报存入 `daily-reports/`：
  1. 今天做了或学到了什么
  2. 遇到了或发现了什么问题
  3. 明天准备做什么
  4. AI 从旁观视角给出的评价和建议
- **仓库隔离**：主仓库通过 `.gitignore` 忽略 `手写数字/` 和 `game/`，两个子项目各自独立提交、独立推送到 GitHub，互不干扰。

## 怎么开始

1. 复制本结构，把目录名改成自己的（如 `zhang-san-course`）
2. `git init && git add . && git commit -m "初始化"`
3. 在 `手写数字/` 和 `game/` 里各自 `git init`，完成阶段二、三的任务并推送到 GitHub
4. 每天工作结束时在根目录启动 Claude Code，执行 `/report-today`

## 学习路径

本仓库服务于课程五个阶段，此阶段（阶段四）重点掌握：

- command / skill / MCP / CLAUDE.md 的区别与用途
- 用 Claude Code 建立自动化流程（每日汇报）
