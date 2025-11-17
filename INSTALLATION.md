# Installation Guide - CCGG Project Creator Skill

## For CCGG Members (Recommended Method)

### One-Line Installation

Open Claude Code in your terminal and run:

```bash
/plugin marketplace add DaronVee/ccgg-project-creator-skill
```

Then install the skill:

```bash
/plugin install project-creator@DaronVee/ccgg-project-creator-skill
```

That's it! The skill is now available in your Claude Code environment.

### Verify Installation

To verify the skill is installed, type:

```bash
/plugin list
```

You should see `project-creator` in the list of installed skills.

### Start Using the Skill

Trigger the skill by saying any of these phrases in Claude Code:

- "Create new project"
- "Initialize new incubator project"
- "Set up project structure for [project-name]"
- "Add new sub-project"

Claude will guide you through the project creation workflow.

## Alternative Method: Direct Git Clone

If you prefer to install directly from source:

### Step 1: Clone the Repository

```bash
git clone https://github.com/DaronVee/ccgg-project-creator-skill.git
cd ccgg-project-creator-skill
```

### Step 2: Install via Claude Code

```bash
/plugin add ./project-creator
```

### Step 3: Verify Installation

```bash
/plugin list
```

## Manual Installation (Advanced)

For developers who want to customize the skill:

### Step 1: Clone to Claude Skills Directory

```bash
git clone https://github.com/DaronVee/ccgg-project-creator-skill.git ~/.claude/skills/ccgg-project-creator
```

### Step 2: Verify Files

Check that these files exist:

```bash
ls ~/.claude/skills/ccgg-project-creator/project-creator/
```

You should see:
- SKILL.md
- templates/ (folder)
- scripts/ (folder)
- references/ (folder)

### Step 3: Restart Claude Code

Exit and restart Claude Code to load the skill.

### Step 4: Test the Skill

Say "Create new project" to trigger the skill.

## Troubleshooting

### Skill Not Triggering

**Issue**: Claude doesn't respond to "Create new project"

**Solution**:
1. Verify installation: `/plugin list` should show `project-creator`
2. Try exact trigger phrase: "Create new project in my business operations"
3. Restart Claude Code
4. Check skill location: `ls ~/.claude/skills/project-creator/SKILL.md`

### Missing Templates or Scripts

**Issue**: Skill runs but says "Template not found"

**Solution**:
1. Verify complete installation:
   ```bash
   ls ~/.claude/skills/project-creator/templates/
   ls ~/.claude/skills/project-creator/scripts/
   ```
2. Re-install the skill:
   ```bash
   /plugin remove project-creator
   /plugin install project-creator@DaronVee/ccgg-project-creator-skill
   ```

### Permission Errors

**Issue**: "Permission denied" when creating project files

**Solution**:
1. Ensure you're in your business operations directory
2. Check write permissions: `ls -la Active\ Projects/_Incubator/`
3. Create directory manually if needed: `mkdir -p "Active Projects/_Incubator"`

## Requirements

### System Requirements
- Claude Code installed (latest version recommended)
- Git (for marketplace installation)
- Python 3.7+ (for validation script - optional)

### Workspace Requirements

Your business operations workspace should have:

```
/
├── Active Projects/
│   └── _Incubator/            # New projects created here
├── Project Memory/
│   └── Active Projects Index/  # Index entries created here
├── operations_log.txt          # Operations logging file
└── CLAUDE.md                   # Root system instructions
```

If you don't have this structure, the skill will guide you to create it.

## Updating the Skill

To update to the latest version:

### Method 1: Via Plugin Marketplace

```bash
/plugin update project-creator
```

### Method 2: Manual Update

```bash
cd ~/.claude/skills/project-creator
git pull origin master
```

Then restart Claude Code.

## Getting Help

- **Issues**: [GitHub Issues](https://github.com/DaronVee/ccgg-project-creator-skill/issues)
- **Community**: [CCGG Skool Community](https://www.skool.com/ccgg)
- **Email**: support@ccggskool.com

## Next Steps

After installation:

1. **Read the README**: [README.md](README.md) for feature overview
2. **Review Templates**: Explore `templates/` folder to understand project structures
3. **Create First Project**: Say "Create new project" to start
4. **Join Community**: [CCGG Skool](https://www.skool.com/ccgg) for support and updates

---

**Installation created**: 2025-11-17
**Author**: Daron Vener
**Repository**: https://github.com/DaronVee/ccgg-project-creator-skill
