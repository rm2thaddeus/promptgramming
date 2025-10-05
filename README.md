# Translation Hill Project Template

A reusable, conversational AI coding project template implementing the Translation Hill methodology.

## Quick Start

1. **Clone and customize**:
   ```bash
   git clone <this-repo> my-project
   cd my-project
   ```

2. **Start Phase 0**:
   ```text
   You are my AI pair programmer. Start Phase 0 (Alignment).
   - Ask about my editor, OS, experience, and preferences.
   - Infer my prompting expertise and communication style.
   - Help me articulate the main project idea in one sentence.
   Output: update templates/phase-templates/PROFILE.yaml and templates/phase-templates/CONTEXT.md.
   ```

3. **Follow the phases**: See `templates/documentation/TEMPLATE_USAGE.md` for complete workflow.

## Repository Structure

```
├── templates/               # All template files organized
│   ├── phase-templates/     # Phase 0-3 template files
│   │   ├── PROFILE.yaml    # User profile & collaboration style
│   │   ├── CONTEXT.md      # Project background & constraints
│   │   ├── IDEA_NOTE.md    # Refined idea & goals
│   │   ├── POC_PLAN.md     # Research & architecture
│   │   ├── PRD.md          # Product requirements
│   │   └── agents.md       # AI roles & coordination
│   ├── documentation/       # Usage guides and workflows
│   │   ├── TEMPLATE_USAGE.md   # Usage guide
│   │   ├── BRANCHING_GUIDE.md  # Git workflow
│   │   └── README.md       # Template documentation
│   └── rules/              # Development guidance
│       ├── debugging.mdc   # Debugging patterns
│       ├── testing-patterns.mdc # Testing guidance
│       ├── mcp-usage.mdc   # MCP server usage
│       └── README.mdc      # Rules overview
├── reference/               # External reference materials
│   └── research/           # Symlinked to C:\Users\aitor\Documents\research
└── README.md               # This file
```

## Key Features

- **Phase-driven workflow** (0-3) with clear handoffs
- **Context preservation** via YAML frontmatter
- **MCP integration** guidance for GitHub, Supabase, Browser Tools, etc.
- **Reusable prompts** for each phase
- **Quality gates** and acceptance criteria

## Documentation

- `templates/documentation/TEMPLATE_USAGE.md` - Complete usage guide
- `templates/documentation/BRANCHING_GUIDE.md` - Git workflow and branching
- `templates/rules/` - Development and MCP guidance

## Reference Materials

External reference files are symlinked in `reference/` and ignored by git.
