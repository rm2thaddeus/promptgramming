# Translation Hill Template Usage

This repository serves as a reusable template for AI coding projects following the Translation Hill methodology.

## Quick Start

### 1. Clone and Branch
```bash
git clone <this-repo-url> my-project
cd my-project
git checkout -b main
```

### 2. Start Phase 0 (Alignment)
Use this prompt to begin:
```
You are my AI pair programmer. Start Phase 0 (Alignment).
- Ask about my editor, OS, experience, and preferences.
- Infer my prompting expertise and communication style.
- Help me articulate the main project idea in one sentence.
Output: update PROFILE.yaml and CONTEXT.md.
```

### 3. Progress Through Phases
- **Phase 1**: Refine idea → `IDEA_NOTE.md`
- **Phase 2**: Research & POC → `POC_PLAN.md`
- **Phase 3**: Build MVP → `PRD.md` + `agents.md`

## Template Structure

```
├── PROFILE.yaml          # User profile & collaboration style
├── CONTEXT.md            # Project background & constraints
├── IDEA_NOTE.md          # Refined idea & goals
├── POC_PLAN.md           # Research & architecture
├── PRD.md                # Product requirements
├── agents.md             # AI roles & coordination
├── .cursor/rules/        # Project-specific guidance
│   ├── debugging.mdc
│   ├── testing-patterns.mdc
│   ├── mcp-usage.mdc
│   └── README.mdc
└── TEMPLATE_USAGE.md     # This file
```

## Customization

1. **Replace placeholders** in all YAML frontmatter (`<project_name>`, `<user_or_team>`, etc.)
2. **Adapt .cursor/rules** for your project's specific needs
3. **Add project-specific files** as needed
4. **Update README.md** with your project details

## Branching Strategy

- `main` - Template version (keep clean)
- `example/[project-name]` - Example implementations
- `feature/[feature-name]` - Feature branches

## MCP Integration

The template includes guidance for using MCP servers:
- GitHub MCP for version control
- Supabase MCP for database operations
- Browser Tools for frontend development
- Context7 for documentation research

## Quality Gates

Each phase includes:
- ✅ Clear acceptance criteria
- ✅ Explicit handoffs between phases
- ✅ Context preservation via YAML frontmatter
- ✅ Reusable prompt templates
