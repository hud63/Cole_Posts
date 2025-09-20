# CLAUDE.md

## Quick Reference
- **Workflow**: Clippings → Prompts → Research → Final Drafts
- **Commands**: See .claude/commands/README.md
- **Common principles**: See PRINCIPLES.md
- **File access issues**: Use find command with -exec cat
- **Research**: Use EXA MCP tools
- **Content focus**: Tax/citizenship/finance

## Slash Commands

**`/li` - LinkedIn Content Only**
- Single command triggers LinkedIn workflow
- Uses LinkedIn Post template → `final drafts/`
- 2,800 character limit, includes web research

**`/sf` - Short Form Content Only**
- 5 Twitter/X posts (280 chars each)
- Scheduled formats → `short form final drafts/`

**`/both` - Dual Content Generation**
- LinkedIn + Short Form from same source
- Archives only after BOTH complete

**`/bush` - Bush Content Generation**
- Dual sequential prompts: Hook Writer → Post Creator
- 11 hooks + 3 posts combined output → `bush_final/`
- No web research, formatting only