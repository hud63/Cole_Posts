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

**`/erica` - Erica Framework Generation**
- 4 distinct framework posts: Absurdist Conspiracy, Problem-Agitation-Solution, Declarative Expertise, Vulnerable Self-Reflection
- 2,800 character limit per post → `erica_final/`
- No web research, formatting only

**`/lian` - Lian LinkedIn Framework Generation**
- 5 LinkedIn formats: Personal Stories & Life Lessons, LinkedIn Growth Tactics, Business Strategy & Frameworks, Psychology & Human Behavior, Contrarian Reality Checks
- 2,800 character limit per post → `lian_final/`
- No web research, formatting only

**`/liz` - Liz Marketing Framework Generation**
- 4 contrarian marketing formats: Problem Reframing, Direct Advisory, Strategic Perspective, Satirical Commentary
- 150-250 words per post → `liz_final/`
- No web research, formatting only

**`/vanderbilt` - Vanderbilt International Opportunity Generation**
- 10 viral formats: Investment/Business Residency, Citizenship by Descent, Retirement Visa, Tax Optimization, Digital Nomad/Remote Work Visas, Passive Income/Non-Lucrative Visas, Offshore Banking Services, Special Opportunities & Time-Limited Programs, Business/Entrepreneur Visas, Educational/Informational posts
- 50-150 words per post → `vanderbilt_final/`
- No web research, formatting only