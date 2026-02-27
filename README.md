# Prompt Generator

A Claude Code skill for generating, evaluating, and optimizing high-quality prompts using the Evaluator-Optimizer workflow.

## 🎯 What It Does

This skill helps you create effective prompts for LLMs (Claude, GPT, Gemini) through a three-step iterative process:

1. **Generate** - Transform your requirements into a structured, optimized prompt
2. **Evaluate** - Critically assess the prompt against best practices
3. **Optimize** - Refine based on evaluation feedback

Instead of one-shot prompt generation, this workflow produces more reliable, well-structured prompts that follow industry best practices.

## ✨ Features

- **Structured Prompt Generation**: Automatically includes key elements (Persona, Context, Task, Constraints, Format)
- **Best Practice Evaluation**: Scores prompts across 5 dimensions (Clarity, Structure, Examples, Reasoning, Constraints)
- **Iterative Optimization**: Refines prompts based on evaluation feedback
- **Variable Support**: Uses `{Variable}` syntax for reusable prompt templates
- **Chain of Thought**: Includes reasoning steps for complex tasks
- **Multi-LLM Support**: Adapts to Claude, GPT, or Gemini specifics

## 📦 Installation

### Prerequisites

- [Claude Code](https://claude.ai/code) installed
- `jq` tool for JSON processing
  ```bash
  # macOS
  brew install jq

  # Ubuntu
  sudo apt-get install jq
  ```

### Install Steps

```bash
# 1. Clone the repository
cd ~/.claude/skills/
git clone https://github.com/mht5405/prompt-generator.git

# 2. Register the skill
bash ~/.claude/add-skill.sh ~/.claude/skills/prompt-generator

# 3. Restart Claude Code
```

## 🚀 Usage

### Trigger the Skill

Use any of these phrases in your conversation with Claude Code:

- "Create a prompt for..."
- "Generate a prompt that..."
- "Optimize my prompt"
- "Improve this prompt"
- "Help me write a prompt for..."

### Example

```
You: Create a prompt for a code review assistant

Claude: [Generates initial prompt]
        [Evaluates the prompt with scores]
        [Provides optimized final version]
```

### Workflow Steps

**Step 1: Generate**
- Transforms your requirements into a structured prompt
- Includes Persona, Context, Task, Constraints, and Format

**Step 2: Evaluate**
- Scores the prompt (1-5) across multiple dimensions
- Provides specific improvement suggestions in JSON format

**Step 3: Optimize**
- Incorporates evaluation feedback
- Delivers the final, refined prompt

## 📚 What's Included

```
prompt-generator/
├── SKILL.md                          # Skill definition and workflow
├── README.md                         # This file
└── references/
    ├── generator-template.md         # Prompt generation template
    └── evaluator-template.md         # Evaluation criteria and rubric
```

## 🎓 Based On

This skill implements best practices from:
- [Anthropic's Prompt Engineering Guide](https://docs.anthropic.com/claude/docs/prompt-engineering)
- Industry-standard prompt optimization techniques
- Iterative refinement workflows

## 💡 Tips

- **Be specific**: The more details you provide about your use case, the better the generated prompt
- **Iterate**: Request further refinement if the first version doesn't meet your needs
- **Specify target LLM**: Mention if you're targeting Claude, GPT, or Gemini for tailored optimization
- **Review templates**: Check `references/` folder for detailed generation and evaluation criteria

## 🤝 Contributing

Found a bug or have a suggestion? Feel free to open an issue or submit a pull request!

## 📄 License

MIT License - feel free to use and modify as needed.

## 🔗 Links

- [Claude Code Documentation](https://docs.anthropic.com/claude/docs/claude-code)
- [Prompt Engineering Best Practices](https://docs.anthropic.com/claude/docs/prompt-engineering)

---

**Created by**: [mht5405](https://github.com/mht5405)
**Skill Type**: Prompt Engineering
**Compatible with**: Claude Code
