# CCGG Project Creator Skill

A production-ready Claude Code skill for creating structured business operation projects with automated integration, dependency tracking, and multi-phase project management.

## What This Skill Does

The **Project Creator** skill automates the creation of new projects in your business operations system, ensuring every project includes:

- **Parent System Integration**: Automatic operations logging, strategic alignment validation, and cross-project intelligence
- **Dependency Tracking**: YAML-based dependency metadata for blocking tasks, downstream impacts, and parallel work
- **Multi-Phase Support**: Optional phase tracking for projects requiring validation, testing, and refinement cycles
- **Active Projects Index**: Lightweight index entries for cross-project queries and pattern recognition
- **Coordination Hubs**: For complex projects with multiple dependencies and integration requirements

## Author

**Daron Vener**
Creator of CCGG (Claude Code for Growing Businesses)
[CCGG Skool Community](https://www.skool.com/ccgg)

## Installation

### Quick Install (One Command)

```bash
/plugin marketplace add DaronVee/ccgg-project-creator-skill
/plugin install project-creator@DaronVee/ccgg-project-creator-skill
```

### Alternative: Manual Installation

1. Clone this repository:
```bash
git clone https://github.com/DaronVee/ccgg-project-creator-skill.git
```

2. Install the skill:
```bash
/plugin add ~/ccgg-project-creator-skill/project-creator
```

## Usage

Once installed, trigger the skill by saying:

- "Create new project in my business operations"
- "Initialize new incubator project"
- "Set up project structure for [project-name]"
- "Add new sub-project"

The skill will guide you through a conversational workflow to gather:
- Project name and purpose
- Key deliverables
- Dependencies (blocking, downstream, parallel)
- Complexity level (simple vs. complex)
- Multi-phase structure (if applicable)

## What Gets Created

### Every Project Includes

1. **CLAUDE.md** - Project-specific guidance with:
   - Parent System Integration (operations logging, strategic alignment)
   - Project structure and boundaries
   - Success criteria
   - Multi-phase tracking section (if applicable)

2. **README.md** - Quick start guide with context and deliverables

3. **Active Projects Index Entry** - Lightweight index file with:
   - YAML metadata (status, dependencies, strategic alignment)
   - Current status summary
   - Quick access links

4. **PHASE_TRACKER.md** (if multi-phase) - Phase management with:
   - Phase timeline and completion criteria
   - Proactive reminder logic
   - Success definitions per phase

5. **Coordination Hub/** (if complex project) - Integration files:
   - PROJECT_DEPENDENCIES.md (upstream/downstream tracking)
   - INTEGRATION_CHECKLIST.md (pre-requisites and handoffs)
   - OUTPUT_LIBRARY.md (deliverable catalog)

### Project Types Supported

**Simple Projects** (default):
- Self-contained work
- Standalone deliverables
- Minimal coordination needs
- Examples: Research projects, single-purpose tools, content creation

**Complex Projects** (with coordination):
- Depends on outputs from other projects
- Multiple projects depend on this project
- Strategic planning affecting multiple areas
- Examples: Pricing strategy, product launches, system integrations

## Key Features

### 1. Dependency Tracking (NEW)

Every project captures dependencies in YAML format:

```yaml
dependencies:
  blocks: ["pricing-model", "clarity-catalog"]       # Must complete first
  blocked_by: ["onboarding-updates", "vsl-rewrite"]  # Waiting for this
  related_parallel: ["youtube-content"]              # Connected, not blocking
```

Benefits:
- Daily roadmaps auto-categorize READY vs BLOCKED tasks
- Completing project X surfaces what's now unblocked
- Critical path visibility (which task blocks most work?)

### 2. Multi-Phase Project Support

Skill analyzes project descriptions for phase indicators:
- Keywords: "validate", "test", "feedback", "iterate", "production"
- Complex deliverables requiring staged rollout
- Integration with existing systems

If detected, suggests 3-phase structure:
- **Phase 1**: Setup & Test / MVP / Research
- **Phase 2**: Validation & Refinement / Production Rollout
- **Phase 3**: Institutionalize / Scale / Deploy

Proactive reminders during weekly reviews ensure phases don't get forgotten.

### 3. Parent System Integration

All projects include mechanisms for:
- **Operations Logging**: Auto-log CREATE, UPDATE, COMPLETE actions to central log
- **Strategic Alignment**: Validate against business goals (OOBG, unique vehicle, avatars)
- **Cross-Project Intelligence**: Search related projects, identify reusable components
- **Index Sync**: Keep Active Projects Index current with project status

### 4. Validation & Quality Control

Built-in validation ensures:
- All required sections present in CLAUDE.md
- Template variables replaced (no `{{PLACEHOLDER}}` remaining)
- Operations log entry created
- Index file properly structured
- Coordination Hub files included (if complex)

## Templates Included

All templates are in the `templates/` folder:

- **CLAUDE_SIMPLE.md** - Standard project guidance
- **CLAUDE_COMPLEX.md** - Complex project with coordination patterns
- **README.md** - Project overview structure
- **PROJECT_INDEX.md** - Active Projects Index entry
- **PHASE_TRACKER_TEMPLATE.md** - Multi-phase tracking
- **coordination/PROJECT_DEPENDENCIES.md** - Dependency mapping
- **coordination/INTEGRATION_CHECKLIST.md** - Integration validation
- **coordination/OUTPUT_LIBRARY.md** - Deliverable catalog

## Scripts Included

- **validate_project.py** - Validates all mechanisms implemented (Python, recommended)
- **validate_project.sh** - Validates all mechanisms implemented (Bash, legacy)

## Use Cases

### Scenario 1: Simple Research Project

**Example**: "Research Dream 100 strategies"

Creates:
- Standard structure with PARENT SYSTEM INTEGRATION
- README with research deliverables checklist
- Index entry with strategic alignment
- Time: 10-15 minutes

### Scenario 2: Complex Strategic Project

**Example**: "Design pricing strategy and offer ladder"

Creates:
- Complex structure with Coordination Hub
- Dependency mapping to upstream projects (frameworks, models)
- Dependency mapping to downstream projects (onboarding, retention)
- Integration checklists for handoffs
- Time: 20-30 minutes

### Scenario 3: Multi-Phase System Build

**Example**: "Create metrics tracking system with testing and validation phases"

Creates:
- 3-phase tracker (Setup & Test → Validation → Institutionalize)
- Weekly reminder logic
- Phase completion criteria
- Automatic transition prompts
- Time: 20-30 minutes

## Requirements

- Claude Code installed
- Business operations workspace with:
  - `Active Projects/` folder structure
  - `Project Memory/Active Projects Index/` for indices
  - `operations_log.txt` for logging
  - Root `CLAUDE.md` with system mechanisms

## Documentation

See the skill's `SKILL.md` for complete workflow documentation, including:
- Step-by-step project creation workflow
- Complexity assessment criteria
- Template variable reference
- Validation checklist
- Common scenarios

## Support

- **Issues**: [GitHub Issues](https://github.com/DaronVee/ccgg-project-creator-skill/issues)
- **Community**: [CCGG Skool Community](https://www.skool.com/ccgg)
- **Email**: support@ccggskool.com

## Version History

**v1.0.0** (2025-11-17)
- Initial public release
- Simple and complex project support
- Multi-phase project tracking
- Dependency tracking integration
- Full PARENT SYSTEM INTEGRATION enforcement
- Automated validation with Python script
- Coordination Hub for complex projects

## License

MIT License - See LICENSE file for details

## Credits

Built with [Skills Factory](https://github.com/anthropics/skills) methodology to ensure production-ready quality.

---

**Created by Daron Vener** | [CCGG Community](https://www.skool.com/ccgg) | [GitHub](https://github.com/DaronVee)
