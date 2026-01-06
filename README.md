# spec-kit Brownfield Bootstrap Extension

> [!IMPORTANT]
> **🌱 For Brownfield (Existing) Projects**
>
> This extension is specifically designed for **existing projects** that want to adopt [spec-kit](https://github.com/github/spec-kit)'s Specification-Driven Development (SDD) workflow.
>
> If you're starting a new project from scratch, use the standard `specify init` command instead.

**Bootstrap your existing codebase into spec-kit's SDD workflow with automatic project analysis and customized template generation.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## What Is This?

When you have an **existing project (brownfield project)** and want to adopt spec-kit's structured development workflow, you face a challenge: the standard `specify init` creates generic templates that don't reflect your project's actual architecture, tech stack, and coding conventions.

**This extension solves that problem** by:

1. **Reverse-analyzing** your existing codebase to extract architectural DNA
2. **Generating customized** project constitution reflecting actual project principles
3. **Adapting templates** to your specific tech stack and coding style
4. **Validating readiness** to ensure SDD workflow can be immediately enabled

## Key Features

### 🔍 Automatic Project Discovery
- Scans project structure to identify tech stack, frameworks, and patterns
- Recognizes common architectural patterns (MVC, Hexagonal, Microservices, etc.)
- Extracts coding conventions from config files and code samples

### 📋 Multi-Module Project Support
- Full support for Maven/Gradle multi-module projects
- Node.js Monorepo with workspaces support
- Go Workspace, Rust Workspace, Python Monorepo
- Automatic module responsibility mapping and dependency analysis

### 🧪 TDD Enforcement
- Built-in Test-Driven Development discipline
- Red-Green-Refactor cycle embedded in all templates
- Coverage requirements and verification checkpoints

### 📁 Correct Directory Structure
- Ensures all files are generated in spec-kit compatible locations
- Pre-output self-check list to prevent common path mistakes
- Clear path reference standards

## Quick Start

### Prerequisites

- **spec-kit** installed ([installation guide](https://github.com/github/spec-kit))
- **AI coding agent** (Claude Code, GitHub Copilot, Cursor, Windsurf, etc.)
- **Existing project** with established codebase

### Installation

**Step 1: Copy Command File**

Copy the command file to your AI coding tool's commands directory:

| AI Tool | Target Directory |
|---------|------------------|
| **Claude Code** | `.claude/commands/` |
| **Cursor** | `.cursor/commands/` |
| **Other Tools** | Check tool documentation |

```bash
# Example for Claude Code
mkdir -p .claude/commands/
cp speckit.brownfield-bootstrap.md .claude/commands/

# For Chinese version
cp speckit.brownfield-bootstrap-cn.md .claude/commands/
```

**Step 2: Verify Installation**

In your AI coding tool, try:
```
/speckit.brownfield-bootstrap
```

### Usage

**1. Run the Bootstrap Command**

```
/speckit.brownfield-bootstrap
```

Or with specific focus:
```
/speckit.brownfield-bootstrap Focus on the user authentication module
```

**2. Review Generated Files**

The command will generate:

| File | Path | Description |
|------|------|-------------|
| Project Constitution | `.specify/memory/constitution.md` | Core principles and constraints |
| Spec Template | `.specify/templates/spec-template.md` | Feature specification template |
| Plan Template | `.specify/templates/plan-template.md` | Implementation plan template |
| Tasks Template | `.specify/templates/tasks-template.md` | Task breakdown template |

**3. Confirm Constitution**

Review the generated constitution and confirm or modify:
- Core principles derived from your code
- Tech stack locked versions
- Directory contracts
- Module responsibilities (for multi-module projects)

**4. Start Using SDD Workflow**

Once bootstrap is complete:

```bash
# Create new feature spec
/speckit.specify "Add user profile image upload"

# Generate implementation plan
/speckit.plan

# Generate task list
/speckit.tasks

# Execute implementation
/speckit.implement
```

## Generated Directory Structure

After running the bootstrap command, your project will have:

```
your-project/
├── .specify/                          # SDD configuration directory
│   ├── memory/
│   │   └── constitution.md            # Project constitution (core file)
│   └── templates/
│       ├── spec-template.md           # Feature spec template
│       ├── plan-template.md           # Implementation plan template
│       └── tasks-template.md          # Task list template
└── specs/                             # Feature specs directory
    └── [###-feature-name]/            # Organized by feature
        ├── spec.md
        ├── plan.md
        └── tasks.md
```

## Language Versions

| File | Language | Description |
|------|----------|-------------|
| `speckit.brownfield-bootstrap.md` | English | Default English version |
| `speckit.brownfield-bootstrap-cn.md` | 中文 | Chinese version |

## Compatibility

### AI Agents

This extension works with any AI agent that supports custom commands:

- ✅ **Claude Code** (fully tested)
- ✅ **Cursor** (tested)
- ✅ **GitHub Copilot** (via instructions)
- ✅ **Windsurf** (via project rules)
- ✅ **Other AI Coding Tools** (copy to commands directory)

### spec-kit Versions

- ✅ **spec-kit v0.0.18+** (uses `/speckit.` prefix)
- ✅ Fully compatible with core spec-kit workflows
- ✅ Non-breaking addition to existing spec-kit setup

### Project Types

- ✅ Single module projects
- ✅ Multi-module Maven/Gradle projects
- ✅ Node.js Monorepo (with workspaces)
- ✅ Go Workspace
- ✅ Rust Workspace
- ✅ Python Monorepo
- ✅ Any language/framework combination

## Brownfield vs Greenfield

| Aspect | Greenfield (`specify init`) | Brownfield (This Extension) |
|--------|---------------------------|----------------------------|
| **Starting Point** | Empty project | Existing codebase |
| **Tech Stack** | You choose | Auto-detected and locked |
| **Architecture** | You design | Reverse-engineered |
| **Templates** | Generic | Project-specific |
| **Constitution** | Minimal | Comprehensive from code analysis |
| **Multi-module** | Basic | Full module mapping |

## FAQ

### When should I use this vs `specify init`?

Use **brownfield-bootstrap** when:
- You have an existing codebase with established patterns
- Your project has specific tech stack constraints
- You want templates that match your existing code style
- You have a multi-module project structure

Use **`specify init`** when:
- Starting a new project from scratch
- You want to establish new conventions
- Project structure is not yet defined

### Will this modify my existing code?

**No!** This command only creates new files in `.specify/` and `specs/` directories. It does not modify any existing source code.

### Can I customize the generated templates?

Yes! After bootstrap, you can freely modify:
- `.specify/memory/constitution.md` - Update principles
- `.specify/templates/*.md` - Customize template formats

### What if my project structure is unusual?

The command will:
1. Do its best to analyze your structure
2. Mark uncertain items with `[NEEDS CLARIFICATION: ...]`
3. Ask you to confirm or provide guidance

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

MIT License - See [LICENSE](LICENSE) for details.

## Credits

- [GitHub spec-kit team](https://github.com/github/spec-kit) for the foundation
- [spec-kit-extensions](https://github.com/MartyBonacci/spec-kit-extensions) for inspiration
- Community contributors

## Support

- **Issues**: [GitHub Issues](https://github.com/wcpaxx/spec-kit-brownfield-extensions/issues)
- **Discussions**: [GitHub Discussions](https://github.com/wcpaxx/spec-kit-brownfield-extensions/discussions)
- **spec-kit**: [Original spec-kit repo](https://github.com/github/spec-kit)

---

**Ready to try it?** Copy the command file to your AI tool's commands directory and run `/speckit.brownfield-bootstrap`!
