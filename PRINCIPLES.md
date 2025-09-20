# Content Creation Principles

## Character Limits
- **LinkedIn**: 2,800 characters MAX (non-negotiable)
- **Short Form/Twitter**: 280 characters per post
- **Hook sections**: ~200 characters
- **Introduction sections**: ~300-400 characters

## File Handling Best Practices

### Special Character Issues
Files in Clippings/ may contain apostrophes, spaces, percentage signs causing access issues.

**Recommended Access Methods:**
1. **Primary**: Use find command with pattern matching:
   ```bash
   find "C:\Users\User\Downloads\General\Vanderbilt Money\Clippings" -name "*keyword*" -exec cat {} \;
   ```
2. **Alternative**: Use Bash ls to identify exact filenames
3. **Last Resort**: Use Task tool with general-purpose agent

### When Direct Read Tool Fails:
- Special characters often cause "File does not exist" errors
- find -exec cat approach bypasses path parsing issues
- Always verify content was accessed vs. generated summaries

## Folder Structure
- **Source**: `Clippings/` → Raw materials, research
- **Processing**: `prompts/` → Template files
- **Output**:
  - `final drafts/` → LinkedIn content
  - `short form final drafts/` → Twitter/social content
  - `bush_final/` → Bush workflow outputs
- **Archive**: `used/` → Processed source materials

## Archive Process
**Standard Workflow:**
1. Read source from Clippings/
2. Process through appropriate prompts
3. Save output to designated folder
4. Move source file: Clippings/ → used/
5. **Critical**: Only archive after ALL content types are generated (for /both command)

## Content Focus Areas
- International tax optimization strategies
- Digital nomad visas and residency programs
- Citizenship by investment and descent programs
- Asset protection and offshore structures
- Financial privacy and wealth preservation
- Cryptocurrency regulation and compliance
- Fintech disruption in financial services

## Research Protocol
**Use EXA MCP Tools for all online research:**
- `mcp__exa__web_search_exa` - General searches
- `mcp__exa__company_research_exa` - Business research
- `mcp__exa__deep_researcher_start` - Complex analysis
- Always supplement Clippings with current data
- Document source URLs for credibility