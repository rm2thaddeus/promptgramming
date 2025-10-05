# Branching Guide for Translation Hill Template

## Branch Structure

### `main` - Template Repository
- **Purpose**: Clean template with placeholders
- **Content**: All template files with `<project_name>`, `<user_or_team>` placeholders
- **Usage**: Clone this for new projects

### `template` - Template Branch
- **Purpose**: Backup of template state
- **Content**: Same as main, alternative template version
- **Usage**: Template variations or backup

### `example/sample-project` - Example Implementation
- **Purpose**: Demonstrates customization process
- **Content**: Filled-in example with real values
- **Usage**: Reference for how to customize the template

## Creating New Projects

### Method 1: Clone Template
```bash
git clone <this-repo-url> my-new-project
cd my-new-project
git remote remove origin
git remote add origin <your-new-repo-url>
```

### Method 2: Branch from Template
```bash
git checkout main
git checkout -b project/my-new-project
# Customize files
git commit -m "Customize template for my-new-project"
```

## Customization Checklist

When starting a new project:

- [ ] Replace `<project_name>` in all YAML frontmatter
- [ ] Replace `<user_or_team>` with actual owner
- [ ] Update `<YYYY-MM-DD>` with current date
- [ ] Customize `.cursor/rules/*.mdc` for project needs
- [ ] Update `README.md` with project-specific details
- [ ] Add project-specific files as needed

## Workflow Example

```bash
# 1. Start with clean template
git checkout main

# 2. Create project branch
git checkout -b project/my-awesome-app

# 3. Customize template
# Edit PROFILE.yaml, CONTEXT.md, etc.

# 4. Commit customization
git add .
git commit -m "Initialize my-awesome-app project"

# 5. Begin Phase 0
# Use prompts from TEMPLATE_USAGE.md
```

## Quality Gates

Before starting development:
- [ ] All placeholders replaced
- [ ] YAML frontmatter updated
- [ ] Project-specific rules added
- [ ] Initial commit made
- [ ] Phase 0 prompt ready to use
