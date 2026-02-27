---
name: prompt-generator
description: Generate, evaluate, and optimize high-quality prompts using the Evaluator-Optimizer workflow. Use when the user asks to "create a prompt", "generate a prompt", "optimize a prompt", "improve my prompt", or wants to transform simple requirements into structured, effective prompts for LLMs (Claude, GPT, Gemini). Based on Anthropic's best practices for iterative prompt improvement.
---

# Prompt Generator

## Overview

This skill implements the **Evaluator-Optimizer workflow** to create high-quality prompts through iterative improvement. Instead of generating a prompt in one shot, this approach:

1. **Generates** an initial optimized prompt from user requirements
2. **Evaluates** the generated prompt against best practices
3. **Optimizes** based on evaluation feedback

This three-step process produces more reliable, well-structured prompts that follow LLM best practices.

## Workflow

### Step 1: Generate Initial Prompt

Read [generator-template.md](references/generator-template.md) and use it to transform the user's requirements into an optimized prompt.

**Key principles to apply:**
- Define clear Persona (role)
- Provide Context (background)
- Specify Task (objective) with verb-driven instructions
- Set Constraints (what to do/not do)
- Define Format (output structure)
- Include Chain of Thought for complex tasks
- Variablize reusable elements with `{Variable}` syntax

**Output:** Present the generated prompt to the user.

### Step 2: Evaluate the Generated Prompt

Read [evaluator-template.md](references/evaluator-template.md) and use it to critically assess the generated prompt.

**Evaluation dimensions:**
- Clarity: Are instructions unambiguous?
- Structural Completeness: Does it include all key elements?
- Example Quality: Are there sufficient examples?
- Reasoning: Does it require step-by-step thinking for complex tasks?
- Constraints: Are instructions primarily positive (what to do)?

**Output:** Provide scores (1-5) and specific improvement suggestions in JSON format.

### Step 3: Optimize Based on Evaluation

Incorporate the evaluation feedback to refine the prompt:

1. Review the suggestions from Step 2
2. Identify the highest-impact improvements
3. Revise the prompt to address the feedback
4. Present the final optimized prompt to the user

**Output:** The final, improved prompt with explanations of key changes made.

## Usage Notes

- **When to use this skill**: Trigger when users want to create or improve prompts, not when they want to use an existing prompt
- **Iteration**: If the user requests further refinement, repeat Steps 2-3
- **Customization**: Adapt the templates based on the specific LLM target (Claude, GPT, Gemini) if the user specifies one
- **Best practices**: The templates incorporate Anthropic's prompt engineering guidelines and industry best practices

## Resources

- **references/generator-template.md**: Detailed template for generating optimized prompts
- **references/evaluator-template.md**: Comprehensive evaluation criteria and scoring rubric
