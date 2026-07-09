# 🧠 AI Agent Skills Hub

Welcome to the **AI Agent Skills Hub**! 

这是一个旨在**跨多个 AI 编程助手（如 Antigravity, Cursor, GitHub Copilot 等）**统一管理、聚合和共享自定义指令（Skills / Rules）的中央仓库。

## 🎯 我们的愿景
实现 **“一处编写，多端复用”**。无论你在使用哪款 AI 工具，都可以从这里直接拉取最新、最优质的 Prompt 资产。未来，我们将配合 `npx ai-skill` 命令行工具，实现一键式跨端注入。

---

## 📂 仓库目录结构

为了保证仓库长期的高可维护性，我们采用了**“自有与第三方分离”**的架构设计：

```text
.
├── skills/                  # 🌟 核心资产区：存放我们自主研发、长期维护的原创 Skills。
│   └── example-skill/       # 每个 Skill 作为一个独立文件夹，内部包含 SKILL.md 及相关资源。
│
├── vendors/                 # 📦 第三方扩展区：通过 Git Submodule 引入的优秀开源 Skill 库。
│   └── mattpocock-skills/   # 例如：Matt Pocock 优秀的工程化 Prompt 集合。
│
└── README.md                # 也就是你正在阅读的这份文档。
```

---

## 🛠️ 如何参与贡献与管理

### 1. 编写你自己的原创 Skill
直接在 `skills/` 目录下新建一个文件夹，并遵循以下标准格式：
1. 文件夹名称即为 Skill 名称（如 `react-best-practices`）。
2. 在该文件夹下创建 `SKILL.md`，并在文件头部添加 YAML Frontmatter（包含 `name` 和 `description`）。

### 2. 引入优秀的开源第三方库
当你在社区发现优秀的 Prompt 集合时，**请不要直接复制代码**。请使用 `git submodule` 将其以外部模块的形式接入到 `vendors/` 目录下，以保持上游代码的同步更新：

```bash
git submodule add <repository-url> vendors/<author>-<project-name>
```

### 3. 同步与更新第三方库
如果你想获取 `vendors/` 目录下所有第三方库的最新改动，只需执行：

```bash
git submodule update --remote
```

---

## 🚀 待办事项 (Roadmap)
- [ ] 丰富 `skills/` 目录下的核心指令库。
- [ ] 编写并发布 `npx ai-skill-hub` CLI 工具，实现自动化解析与多端分发。
- [ ] 建立 `registry.json` 索引体系，支持快速检索。

---
*Generated with ❤️ by Antigravity.*
