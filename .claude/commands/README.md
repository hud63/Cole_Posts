# Claude Code Slash Commands

## Available Commands

### `/li` - LinkedIn Content Generator
Single-platform content creation:
1. Lists Clippings → user selects
2. Applies LinkedIn Post template rules
3. Generates 2,800 character LinkedIn post
4. Saves to `final drafts/` → archives source to `used/`
- Includes web research using EXA MCP tools
- 5 content styles: Steps, Stats, Mistakes, Lessons, Examples

### `/both` - Dual Content Generator
Multi-platform content from same source:
1. Lists Clippings → user selects
2. Creates LinkedIn post (2,800 chars) + 5 short-form posts (280 chars)
3. Saves LinkedIn to `final drafts/`, short-form to `short form final drafts/`
4. Archives source to `used/` (only after BOTH complete)
- Combines /li and /sf workflows
- Scheduled posting: 8:30am, 11am, 1pm, 3:30pm, 7pm PT

### `/bush` - Bush Content Generator
Sequential prompt processor:
1. Lists Clippings → user selects
2. Runs: Hook Writer (11 hooks) → Post Creator (3 posts)
3. Saves combined output → `bush_final/`
4. Archives source → `used/`
- NO web research (unlike /li)
- Formats output only, preserves prompt results

### `/sf` - Short Form Content Generator
Social media focused:
1. Lists Clippings → user selects
2. Creates 5 Twitter/X posts (280 chars each)
3. Time-slotted formats for scheduled posting
4. Saves to `short form final drafts/` → archives source to `used/`
- 5 formats: Paragraph, What/How/Why, Listicle, Old vs New, 10 Magical Ways

## Common Features
- All commands use Clippings/ folder as source
- Special character handling with find command
- Automatic file archiving to used/ folder
- Target audience: International tax, citizenship, financial freedom