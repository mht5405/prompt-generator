# MHT Skills 技能集合

[English](#english-version) | 中文

Claude Code 技能集合，用于提升生产力和工作流自动化。

## 📦 可用技能

### 1. Prompt Generator（提示词生成器）

使用评估-优化工作流生成、评估和优化高质量提示词。

**功能特性：**
- 结构化提示词生成，包含关键要素（角色、上下文、任务、约束、格式）
- 基于 5 个维度的最佳实践评估
- 基于评估反馈的迭代优化
- 支持 Claude、GPT 和 Gemini

**[查看详情 →](./prompt-generator/)**

### 2. Liuhuahui Writing Style

生成符合刘华辉真实、对话式和实用风格的内容。

**功能特性：**
- 直接对话的语气（像和朋友聊天）
- 挑战主流叙事的批判性思维
- 对读者充满同理心和关怀
- 实用的、行动导向的建议，包含"练习作业"部分
- 自然使用口语化表达和网络用语
- 适合博客文章、教程和观点文章

**[查看详情 →](./liuhuahui-writing-style/)**

## 🚀 安装方法

### 前置要求

- 已安装 [Claude Code](https://claude.ai/code)
- `jq` 工具（用于 JSON 处理）
  ```bash
  # macOS
  brew install jq

  # Ubuntu
  sudo apt-get install jq
  ```

### 安装技能

```bash
# 1. 克隆此仓库
cd ~/.claude/skills/
git clone https://github.com/mht5405/mht-skills.git

# 2. 注册你想使用的技能
# 示例：安装 prompt-generator
bash ~/.claude/add-skill.sh ~/.claude/skills/mht-skills/prompt-generator

# 3. 重启 Claude Code
```

## 📚 技能结构

此集合中的每个技能都遵循标准的 Claude Code 技能格式：

```
skill-name/
├── SKILL.md                    # 技能定义和工作流
├── README.md                   # 详细文档（可选）
└── references/                 # 额外资源（可选）
```

## 💡 使用方法

安装后，你可以通过以下方式使用技能：

1. **直接调用**：在 Claude Code 中输入 `/skill-name`
2. **自然触发**：使用与技能描述匹配的短语
3. **上下文感知**：技能会在相关时自动激活

## ⚠️ 兼容性说明

**重要**：这些技能是 **Claude Code 专用的**，不能直接在其他 AI 工具（如 opencode、codex 等）中使用。

- ✅ 可以在 Claude Code 中通过命令安装
- ❌ 不能在其他工具中自动安装
- 💡 但你可以手动复制 SKILL.md 的内容给其他 AI 工具使用

## 🛠️ 创建自己的技能

想创建自己的技能？查看 [skill-creator](https://github.com/anthropics/claude-code) 文档。

基本步骤：
1. 创建带有 YAML frontmatter 的 `SKILL.md` 文件
2. 定义技能的工作流和指令
3. 使用 `add-skill.sh` 注册

## 📖 文档

每个技能都有自己的 README，包含：
- 详细的功能描述
- 使用示例
- 配置选项
- 最佳实践

进入技能目录查看更多信息。

## 🤝 贡献

欢迎贡献！添加新技能的步骤：

1. Fork 此仓库
2. 为你的技能创建新目录
3. 添加 `SKILL.md` 和可选的 `README.md`
4. 提交 pull request

## 📄 许可证

MIT License - 可自由使用和修改。

## 🔗 链接

- [Claude Code 文档](https://docs.anthropic.com/claude/docs/claude-code)
- [提示词工程最佳实践](https://docs.anthropic.com/claude/docs/prompt-engineering)

---

**维护者**：[mht5405](https://github.com/mht5405)
**仓库地址**：https://github.com/mht5405/mht-skills

---

# English Version

A collection of Claude Code skills for enhancing productivity and workflow automation.

## 📦 Available Skills

### 1. Prompt Generator

Generate, evaluate, and optimize high-quality prompts using the Evaluator-Optimizer workflow.

**Features:**
- Structured prompt generation with key elements (Persona, Context, Task, Constraints, Format)
- Best practice evaluation across 5 dimensions
- Iterative optimization based on feedback
- Support for Claude, GPT, and Gemini

**[View Details →](./prompt-generator/)**

### 2. Liuhuahui Writing Style

Write content that matches liuhuahui's authentic, conversational, and practical voice.

**Features:**
- Direct and conversational tone (like chatting with a friend)
- Critical thinking that challenges mainstream narratives
- Empathetic and caring approach to readers
- Practical, action-oriented advice with "练习作业" sections
- Uses colloquial expressions and internet slang naturally
- Perfect for blog posts, tutorials, and opinion pieces

**[View Details →](./liuhuahui-writing-style/)**

## 🚀 Installation

### Prerequisites

- [Claude Code](https://claude.ai/code) installed
- `jq` tool for JSON processing
  ```bash
  # macOS
  brew install jq

  # Ubuntu
  sudo apt-get install jq
  ```

### Install a Skill

```bash
# 1. Clone this repository
cd ~/.claude/skills/
git clone https://github.com/mht5405/mht-skills.git

# 2. Register the skill you want to use
# Example: Install prompt-generator
bash ~/.claude/add-skill.sh ~/.claude/skills/mht-skills/prompt-generator

# 3. Restart Claude Code
```

## 📚 Skill Structure

Each skill in this collection follows the standard Claude Code skill format:

```
skill-name/
├── SKILL.md                    # Skill definition and workflow
├── README.md                   # Detailed documentation (optional)
└── references/                 # Additional resources (optional)
```

## 💡 Usage

After installation, you can use skills by:

1. **Direct invocation**: Type `/skill-name` in Claude Code
2. **Natural triggers**: Use phrases that match the skill's description
3. **Context-aware**: Skills activate automatically when relevant

## ⚠️ Compatibility Note

**Important**: These skills are **Claude Code specific** and cannot be directly installed in other AI tools (like opencode, codex, etc.).

- ✅ Can be installed via command in Claude Code
- ❌ Cannot be auto-installed in other tools
- 💡 But you can manually copy SKILL.md content for use with other AI tools

## 🛠️ Creating Your Own Skills

Want to create your own skill? Check out the [skill-creator](https://github.com/anthropics/claude-code) documentation.

Basic steps:
1. Create a `SKILL.md` file with YAML frontmatter
2. Define the skill's workflow and instructions
3. Register it using `add-skill.sh`

## 📖 Documentation

Each skill has its own README with:
- Detailed feature descriptions
- Usage examples
- Configuration options
- Best practices

Navigate to the skill's directory to read more.

## 🤝 Contributing

Contributions are welcome! To add a new skill:

1. Fork this repository
2. Create a new directory for your skill
3. Add `SKILL.md` and optional `README.md`
4. Submit a pull request

## 📄 License

MIT License - feel free to use and modify as needed.

## 🔗 Links

- [Claude Code Documentation](https://docs.anthropic.com/claude/docs/claude-code)
- [Prompt Engineering Best Practices](https://docs.anthropic.com/claude/docs/prompt-engineering)

---

**Maintained by**: [mht5405](https://github.com/mht5405)
**Repository**: https://github.com/mht5405/mht-skills
