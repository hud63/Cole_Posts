# Slash Command Integration Template

## Prerequisites
- Prompt file already exists in `prompts/{COMMAND_NAME}.md`
- Determine command behavior: research vs no-research, output folder, special features

## Step-by-Step Implementation

### 1. Update `.claude/slash_commands.json`
Add new entry to the `slash_commands` array:

```json
{
  "name": "{COMMAND_NAME}",
  "description": "{DESCRIPTION}",
  "prompt": "Execute workflow from {COMMAND_NAME}.md"
}
```

**Example:**
```json
{
  "name": "erica",
  "description": "Generate 4 distinct social media posts using Erica frameworks - creates Absurdist Conspiracy, Problem-Agitation-Solution, Declarative Expertise, and Vulnerable Self-Reflection posts",
  "prompt": "Execute workflow from erica.md"
}
```

### 2. Update `.claude/prompt_mappings.json`
Add mapping entry:

```json
"{COMMAND_NAME}": "prompts/{PROMPT_FILE_NAME}.md"
```

**Examples:**
- Single prompt: `"erica": "prompts/Erica.md"`
- Multiple prompts: `"bush": ["prompts/Bush Hook Writer.md", "prompts/Bush Post Creator.md"]`
- LinkedIn style: `"li": "prompts/Linkedin Post.md"`

### 3. Create `.claude/commands/{COMMAND_NAME}.md`
Workflow instructions file template:

```markdown
# {DISPLAY_NAME} Content Generator (`/{COMMAND_NAME}`)

You are the {DISPLAY_NAME} Content Generator executing the established workflow. Follow these steps:

## WORKFLOW EXECUTION
1. **Examine Clippings**: List all .md files in Clippings/ folder, present as numbered options for user selection
2. **Read Selected Content**: Use find command for special characters: find "C:\Users\User\Downloads\General\Vanderbilt Money\Clippings" -name "*keyword*" -exec cat {} \;
3. **Apply {DISPLAY_NAME} Template**: Generate content using rules below {RESEARCH_PROTOCOL}
4. **Save & Archive**: Save to {OUTPUT_FOLDER}/ folder, move source to used/

## {RESEARCH_PROTOCOL_SECTION}
{RESEARCH_INSTRUCTIONS}

## {DISPLAY_NAME} CONTENT RULES
See: prompts/{PROMPT_FILE_NAME}.md

**Key Requirements:**
{SPECIFIC_REQUIREMENTS}

**Output Format:**
Save as: `{OUTPUT_FOLDER}/{PREFIX}_[Source_Title].md`
{ADDITIONAL_FORMAT_NOTES}
```

**Research Protocol Options:**
- **No Research:** `**This command does NOT use web research or EXA tools. Work only with the clipping content provided.**`
- **With Research:** `**This command uses EXA research tools to supplement clipping content.**`

### 4. Update `.claude/README.md`
Add new section after existing commands:

```markdown
### `/{COMMAND_NAME}` - {DISPLAY_NAME}

{DESCRIPTION_BLOCK}:

1. **Lists available topics** from the `Clippings/` folder
2. **Handles user selection** and reads content (including files with special characters)
3. **{MAIN_FUNCTION}**
4. **{OUTPUT_SPECS}**
5. **Saves final content** to `{OUTPUT_FOLDER}/` folder
6. **Archives source material** to `used/` folder
```

**Update Usage section:**
```markdown
- Type `/{COMMAND_NAME}` for {SHORT_DESCRIPTION}
```

**Examples:**
- Research command: `"Generate LinkedIn thought leadership content using the established workflow"`
- No-research command: `"Generate 4 distinct social media posts using Erica frameworks"`

### 5. Update `CLAUDE.md`
Add entry to Slash Commands section:

```markdown
**`/{COMMAND_NAME}` - {DISPLAY_NAME}**
- {KEY_FEATURES_BULLET_POINTS}
- {CHARACTER_LIMITS} → `{OUTPUT_FOLDER}/`
- {RESEARCH_STATUS}
```

**Examples:**
- `**`/erica` - Erica Framework Generation**`
- `- 4 distinct framework posts: Absurdist Conspiracy, Problem-Agitation-Solution, Declarative Expertise, Vulnerable Self-Reflection`
- `- 2,800 character limit per post → `erica_final/``
- `- No web research, formatting only`

## Variable Reference Guide

### Required Variables:
- `{COMMAND_NAME}` - Slash command name (lowercase, no spaces)
- `{DISPLAY_NAME}` - Human-readable name for documentation
- `{DESCRIPTION}` - Full description for slash_commands.json
- `{PROMPT_FILE_NAME}` - Name of prompt file in prompts/ folder
- `{OUTPUT_FOLDER}` - Where final content gets saved

### Content-Specific Variables:
- `{RESEARCH_PROTOCOL}` - "(NO web research needed)" or "(includes web research)"
- `{RESEARCH_PROTOCOL_SECTION}` - "NO RESEARCH PROTOCOL" or "RESEARCH PROTOCOL"
- `{RESEARCH_INSTRUCTIONS}` - Text explaining research approach
- `{SPECIFIC_REQUIREMENTS}` - Bulleted list of content requirements
- `{PREFIX}` - File prefix for saved content
- `{MAIN_FUNCTION}` - Primary action description for README
- `{OUTPUT_SPECS}` - Character limits, format specs
- `{SHORT_DESCRIPTION}` - Brief usage description
- `{KEY_FEATURES_BULLET_POINTS}` - Main features as bullets

## Command Types & Templates

### No-Research Content Generator (like `/erica`, `/bush`)
- Uses only clipping content
- Dedicated output folder
- Character limits specified
- Formatting-focused

### Research-Enhanced Generator (like `/li`, `/both`, `/sf`)
- Uses EXA research tools
- Standard output folders (`final drafts/`, `short form final drafts/`)
- Web research integration
- Topic expansion

### Multi-Prompt Sequential (like `/bush`)
- Multiple prompt files in array
- Combined workflow processing
- Special output formatting

## Testing Checklist

After implementation:
1. ✅ Run `/{COMMAND_NAME}` command
2. ✅ Verify clippings folder listing works
3. ✅ Test file selection and reading (including special characters)
4. ✅ Confirm content generation follows prompt rules
5. ✅ Check output file saved to correct folder with proper naming
6. ✅ Verify source file moved to used/ folder
7. ✅ Test character limits if applicable
8. ✅ Validate all formatting requirements

## File Locations Quick Reference

```
.claude/
├── slash_commands.json          # Command definitions
├── prompt_mappings.json         # Prompt file mappings
├── commands/
│   ├── {COMMAND_NAME}.md       # Workflow instructions
│   └── README.md               # Documentation
└── README.md                   # Full command documentation

prompts/
└── {PROMPT_FILE_NAME}.md       # Content generation rules

{OUTPUT_FOLDER}/                # Generated content destination
used/                          # Archived source materials
CLAUDE.md                      # Quick reference documentation
```

---

**Usage:** Copy this template, replace all `{VARIABLES}` with your specific values, then follow the 5 steps to integrate any new slash command. Only requirement: prompt file must exist in `prompts/` folder first.