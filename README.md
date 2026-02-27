# MHT Skills Collection

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
