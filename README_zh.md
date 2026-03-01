# 🗂️ 项目文件管理 Skill

[English](README.md) | [日本語](README_ja.md) | [한국어](README_ko.md)

> 一个让 AI 助手在所有项目中自动执行结构化文件管理的 Skill。

## 它能做什么

安装后，你的 AI 助手会在每个项目中**主动组织文件**，再也不会在长时间工作后留下一团乱麻。

| 触发条件 | 行为 |
|---------|------|
| 启动新项目 | 自动建议并创建标准化文件夹结构 |
| 任务中创建文件 | 自动将文件放入正确的文件夹 |
| 说"整理"、"清理"、"文件结构" | 扫描并重新组织整个项目文件夹 |
| 每 3–5 次文件操作 | 执行清理检查点 |

## 核心规则

### 📁 标准项目结构

```
项目名/
├── README.md        — 项目说明、状态、约定
├── drafts/          — 工作草稿、迭代版本
├── figures/         — 图片、图表、示意图
├── scripts/         — 生成输出的代码
├── references/      — 参考材料、模板
├── output/          — 仅存放最终交付物
└── archive/         — 被替代的旧版本（移动而非删除）
```

### 📝 命名规范

| ✅ 正确 | ❌ 错误 |
|--------|--------|
| `报告_v1.docx` | `报告_最终版.docx` |
| `报告_v2.docx` | `报告_新.docx` |
| `投稿_20260226.docx` | `报告_终极最终版.docx` |

### 🏗️ 领域专用模板

内置多种项目模板：
- **学术论文** — drafts / figures / scripts / references / output / archive
- **Web 应用** — src / public / scripts / docs / dist
- **数据分析** — data / notebooks / scripts / figures / output

## 安装方法

将 `project-organizer/` 文件夹放入你的 skills 目录：

```
~/.gemini/antigravity/skills/project-organizer/
```

在所有新对话中自动生效。

## 为什么要做这个

在一个持续数周的 AI 辅助论文写作项目之后，我们发现 70 多个文件全部堆积在同一个文件夹——脚本和草稿混在一起，临时文件紧挨着最终投稿文件。这个 Skill 正是从那次痛苦经历中诞生的，它把我们希望一开始就拥有的组织原则编码成了规则。

## 许可证

MIT
