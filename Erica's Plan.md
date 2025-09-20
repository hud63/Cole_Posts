# Erica Slash Command Integration Plan

## Research & Analysis Performed

### Files Examined:
1. **`.claude/slash_commands.json`** - Current slash commands structure
2. **`.claude/commands/li.md`** - LinkedIn workflow example
3. **`.claude/commands/both.md`** - Dual content workflow example
4. **`.claude/prompt_mappings.json`** - Prompt mapping structure
5. **`prompts/Erica.md`** - The new prompt template

### Commands Run During Analysis:
```bash
ls ".claude/commands/"
# Result: both.md, bush.md, li.md, README.md, sf.md

find . -name "*.md" -path "*/.claude/*" -o -name "*.json" -path "*/.claude/*"
# Result: Found all .claude configuration files
```

## Current Slash Commands Structure

### Existing Commands:
- `/li` - LinkedIn content only (uses EXA research)
- `/both` - LinkedIn + Short Form dual content (uses EXA research)
- `/sf` - Short Form content only (uses EXA research)
- `/bush` - Sequential dual-prompt generator (no web research)

### File Structure Pattern:
1. **`.claude/slash_commands.json`** - Command definitions and descriptions
2. **`.claude/prompt_mappings.json`** - Maps commands to prompt files
3. **`.claude/commands/[name].md`** - Workflow instructions for each command

## Integration Plan for `/erica`

### Files That Need Updates:

#### 1. `.claude/slash_commands.json`
**Add new entry:**
```json
{
  "name": "erica",
  "description": "Generate 4 distinct social media posts using Erica frameworks - creates Absurdist Conspiracy, Problem-Agitation-Solution, Declarative Expertise, and Vulnerable Self-Reflection posts",
  "prompt": "Execute workflow from erica.md"
}
```

#### 2. `.claude/prompt_mappings.json`
**Add mapping:**
```json
"erica": "prompts/Erica.md"
```

#### 3. `.claude/commands/erica.md` (NEW FILE)
**Workflow content:**
```markdown
# Erica Content Generator (`/erica`)

You are the Erica Content Generator executing the established workflow. Follow these steps:

## WORKFLOW EXECUTION
1. **Examine Clippings**: List all .md files in Clippings/ folder, present as numbered options for user selection
2. **Read Selected Content**: Use find command for special characters: find "C:\Users\User\Downloads\General\Vanderbilt Money\Clippings" -name "*keyword*" -exec cat {} \;
3. **Apply Erica Template**: Generate 4 framework posts using rules below (NO web research needed)
4. **Save & Archive**: Save to erica_final/ folder, move source to used/

## NO RESEARCH PROTOCOL
**This command does NOT use web research or EXA tools. Work only with the clipping content provided.**

## ERICA CONTENT RULES
See: prompts/Erica.md

**Key Requirements:**
- Generate exactly 4 posts using the frameworks:
  1. Absurdist Conspiracy Theory
  2. Problem-Agitation-Solution
  3. Declarative Expertise
  4. Vulnerable Self-Reflection
- 2,800 characters MAX per post (non-negotiable)
- Save output to erica_final/ folder
- Each post must be complete, standalone content
- Follow framework-specific attributes precisely

**Output Format:**
Save as: `erica_final/Erica_[Source_Title].md`
Include character counts for each post to verify limits
```

## Key Differences from Other Commands

### Unlike `/li`, `/both`, `/sf`:
- **No EXA research tools** - Works purely with clipping content
- **erica_final/ folder output** - Uses dedicated output folder
- **Unique format** - 4 framework posts vs single LinkedIn or multiple short-form

### Similar to `/bush`:
- **No web research** - Content generation only
- **Multi-format output** - Multiple distinct pieces from same source

## Implementation Steps

1. **Update `.claude/slash_commands.json`** - Add erica command definition
2. **Update `.claude/prompt_mappings.json`** - Add erica → Erica.md mapping
3. **Create `.claude/commands/erica.md`** - Workflow instructions file
4. **Update `.claude/README.md`** - Add `/erica` and `/bush` command documentation
5. **Test command** - Verify `/erica` executes properly

### README Update Specifications

#### 4. `.claude/README.md` Updates

**Add missing `/bush` command section after `/both`:**
```markdown
### `/bush` - Bush Content Generator

Sequential dual-prompt content generation:

1. **Lists available topics** from the `Clippings/` folder
2. **Handles user selection** and reads content (including files with special characters)
3. **Processes through dual prompts**: Bush Hook Writer + Bush Post Creator
4. **Generates combined output**: 11 LinkedIn hooks + 3 posts (Framework, Story, Listicle)
5. **Saves final content** to `bush_final/` folder
6. **Archives source material** to `used/` folder
```

**Add `/erica` command section after `/bush`:**
```markdown
### `/erica` - Erica Framework Generator

Automated generation of 4 distinct social media posts using Erica frameworks:

1. **Lists available topics** from the `Clippings/` folder
2. **Handles user selection** and reads content (including files with special characters)
3. **Generates 4 framework posts**: Absurdist Conspiracy, Problem-Agitation-Solution, Declarative Expertise, Vulnerable Self-Reflection
4. **Character limit**: 2,800 characters MAX per post (non-negotiable)
5. **Saves final content** to `erica_final/` folder
6. **Archives source material** to `used/` folder
```

**Update Usage section to include:**
```markdown
- Type `/bush` for Bush dual-prompt content generation
- Type `/erica` for Erica framework content generation
```

## Expected Workflow Behavior

1. User types `/erica`
2. System lists Clippings folder contents
3. User selects clipping file
4. System reads selected file content
5. System applies Erica prompt to generate 4 framework posts
6. System saves output to erica_final/ folder as `Erica_[Title].md`
7. System moves source clipping to used/ folder

## Testing Plan

After implementation:
1. Run `/erica` command
2. Select a clipping file
3. Verify 4 posts are generated with correct frameworks
4. Confirm character limits are respected (2,800 each)
5. Check output file is saved to erica_final/ folder
6. Verify source file is moved to used/ folder

---

