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