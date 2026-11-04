# ljg-learn · 概念学习与解剖

> **English:** A concept-learning skill for AI agents. For everyday "what is X / help me understand X" questions it gives a precise one-line meaning, a real-life example, the actual mechanism, where the analogy breaks and the most common confusion. When you explicitly ask for concept anatomy (or call `/ljg-learn`), it runs the original eight-dimension deep dissection — history, dialectics, phenomenology, language, formalization, existence, aesthetics, meta-reflection — and compresses it into a formula, one sentence and an ASCII diagram, saved as an org-mode note. Adapted from [lijigang/ljg-skills](https://github.com/lijigang/ljg-skills) (MIT). Chinese-language skill.

## 它做什么

- **日常解释（新增）**：一句话准确含义 → 生活例子 → 真实机制与边界 → 类比在哪失效 → 最容易混淆的地方。默认在聊天里交付，不写文件。
- **深度解剖（原版保留）**：定锚 → 八维（历史、辩证、现象、语言、形式、存在、美感、元反思）→ 内观 → 压缩（关系式、一句话、ASCII 结构图）。
- **org-mode 笔记**：显式 `/ljg-learn` 或要求笔记时生成，纯 org 语法，不混 Markdown。
- 不编造词源和历史；缺依据的维度保留并说明限制。

## 配置笔记保存位置

保存目录按以下顺序确定：

1. 你在本轮对话里指定的位置；
2. 环境变量 `LJG_NOTES_DIR`；
3. 都没有时用 `~/Documents/notes`。

```bash
export LJG_NOTES_DIR="$HOME/notes/concepts"   # 写进 ~/.zshrc 或 ~/.bashrc
```

文件名格式：`{YYYYMMDDTHHMMSS}--概念解剖-{概念名}__concept.org`，不会覆盖已有笔记。

## 安装

这是一个 Agent Skill（一份写给 AI 读的工作说明，入口是 `SKILL.md`），可用于 Claude Code、Codex 等支持 skills 目录的工具。不需要额外的 API key 或后台服务。

把整个仓库放进你的 skills 目录，目录名保持 `ljg-learn`：

```bash
# Claude Code（个人级）
git clone https://github.com/Samuel-Shek/ljg-learn.git ~/.claude/skills/ljg-learn

# Codex
git clone https://github.com/Samuel-Shek/ljg-learn.git ~/.codex/skills/ljg-learn
```

其他工具放进各自的 skills 目录即可。装好后重开会话，说“帮我理解一下 XX”（日常解释）或 `/ljg-learn 熵`（深度解剖 + 笔记）即可。

## 目录

| 文件 | 用途 |
|---|---|
| `SKILL.md` | 模式选择与日常解释 |
| `references/deep-anatomy.md` | 原八维深度解剖与 org-mode 笔记格式 |

## 来源与致谢

改编自**李继刚**的 [lijigang/ljg-skills](https://github.com/lijigang/ljg-skills) 中的 `ljg-learn`（MIT）。八维解剖与 org-mode 笔记格式来自原作者；本版新增日常解释模式，并让笔记目录可配置。详见 [NOTICE](NOTICE)。

## 许可证

[MIT](LICENSE)，保留原作者 lijigang 的版权声明。
