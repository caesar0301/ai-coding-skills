# AI Coding Skills Repository

A collection of reusable skills for Claude Code CLI that enhance AI agent capabilities for development workflows.

## Overview

This repository contains skills that can be installed and used with Claude Code CLI. Skills are reusable, prompt-based operations that guide AI agents through complex tasks.

## Installation

Skills are installed by copying them to your project's `.claude/skills/` directory:

1. **Navigate to your project directory:**
   ```bash
   cd /path/to/your/project
   ```

2. **Create the skills directory (if it doesn't exist):**
   ```bash
   mkdir -p .claude/skills
   ```

3. **Copy the desired skill from this repository:**
   ```bash
   # For the platonic-coding-specs skill:
   cp -r /path/to/ai-coding-skills/platonic-coding-specs .claude/skills/
   ```

   Or if you're cloning this repository:
   ```bash
   git clone <repository-url>
   cp -r ai-coding-skills/platonic-coding-specs .claude/skills/
   ```

4. **Verify installation:**
   ```bash
   ls -la .claude/skills/
   ```

   You should see the skill directory (e.g., `platonic-coding-specs/`).

## Available Skills

### platonic-coding-specs

A skill for managing RFC-style specifications in development projects using AI-driven operations.

**Features:**
- Initialize new specification systems
- Generate and maintain RFC history, index, and namings files
- Validate consistency and compliance across specifications
- Check taxonomy and terminology usage

**Quick Start:**
```bash
# In Claude Code CLI, ask the AI agent to:
# "Read .claude/skills/platonic-coding-specs/prompts/init-specs.md and initialize specs for project 'MyProject'"
```

**Documentation:**
- See [platonic-coding-specs/README.md](platonic-coding-specs/README.md) for detailed usage
- See [platonic-coding-specs/SKILL.md](platonic-coding-specs/SKILL.md) for operation reference

## Using Skills in Claude Code CLI

Once installed, skills are used by directing the AI agent to read and execute the prompt files:

### Method 1: Direct Prompt Reference

Ask Claude Code CLI to read and execute a specific prompt:

```
Read .claude/skills/platonic-coding-specs/prompts/init-specs.md and apply it with:
- Project name: "MyProject"
- Specs directory: "./specs"
```

### Method 2: Skill Name Reference

If Claude Code CLI supports skill discovery, you can reference skills by name:

```
Use the platonic-coding-specs skill to initialize specs for project "MyProject"
```

### Method 3: Step-by-Step Execution

For complex operations, guide the agent step-by-step:

```
1. Read .claude/skills/platonic-coding-specs/prompts/refine-specs.md
2. Apply it to the specs/ directory
3. Show me the validation report
```

## License

See [LICENSE](LICENSE) for license information.
