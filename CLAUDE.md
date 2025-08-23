# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a content creation repository focused on financial services, international tax optimization, and citizenship/residency topics. The primary workflow involves researching, writing, and publishing thought leadership content for LinkedIn and newsletters.

## Folder Structure and Workflow

The repository follows a structured content creation workflow:

- **Clippings/**: Raw concept files, research materials, and initial thoughts on various topics (tax strategies, digital nomad visas, citizenship programs, etc.)
- **prompts/**: High-quality prompts for content development, including LinkedIn Post and Short Form templates
- **final drafts/**: Completed LinkedIn content pieces ready for publication
- **short form final drafts/**: Completed short-form social media posts (5 per topic, 280 chars each)
- **used/**: Archive of previously published or utilized content

## Content Creation Process

### Option 1: Slash Commands (Recommended)

**`/li` - LinkedIn Content Only**
- Single command triggers LinkedIn content workflow
- Interactive topic selection from Clippings folder  
- Automatic application of LinkedIn Post template with all formatting rules
- Saves to `final drafts/` and archives source material
- Maintains 2,800 character limit and all quality standards

**`/sf` - Short Form Content Only**
- Generates 5 Twitter/X posts (280 characters each) for scheduled posting
- Time slots: 8:30am, 11am, 1pm, 3:30pm, 7pm Pacific
- 5 formats: Paragraph Style, What/How/Why, Listicle, Old vs New, 10 Magical Ways
- Saves to `short form final drafts/` and archives source material
- Optimized for social media engagement and thought leadership

**`/both` - Dual Content Generation**
- Creates both LinkedIn post AND 5 short-form posts from same source material
- Runs both workflows sequentially using identical source content
- LinkedIn content → `final drafts/`, Short form → `short form final drafts/`
- Archives source material only after BOTH content types are generated
- Maximum efficiency for multi-platform content strategy

### Option 2: Manual Workflow
When tasked with content creation manually, follow this sequence:

1. **Start with README.md**: Review the workflow process outlined in the README
2. **Examine Clippings**: Review relevant files in the `Clippings/` folder to understand the topic and gather source material
3. **Select Appropriate Prompt**: Use prompts from the `prompts/` folder (primarily the LinkedIn Post template)
4. **Research**: Conduct additional research to supplement information from Clippings
5. **Create Content**: Follow prompt instructions precisely, incorporating research and Clippings content
6. **Save Final Output**: Place completed content in `final drafts/` folder as `.md` files

## Key Content Guidelines

- LinkedIn posts must stay under 2,800 characters (non-negotiable limit)
- Content focuses on international tax strategies, residency/citizenship programs, and financial freedom topics
- Maintain thought leadership tone with actionable, tactical information
- Use the specific LinkedIn formatting rules outlined in `prompts/Linkedin Post.md`
- All final content should be saved as Markdown files

## Integration Tools

The repository includes:
- Make.com blueprint for automated content generation (`Post Ghostwriter Agent (Gemini).blueprint.json`)
- WhisperTyping command documentation for voice-to-text workflows
- Asset management documentation for content creation tools

## Content Themes

Primary subject areas include:
- International tax optimization strategies
- Digital nomad visas and residency programs
- Citizenship by investment and descent programs
- Asset protection and offshore structures
- Financial privacy and wealth preservation
- Cryptocurrency regulation and compliance
- Fintech disruption in financial services
- Sustainable investing trends

When creating content, ensure accuracy of financial and legal information, include appropriate disclaimers, and maintain focus on educational/informational value rather than specific advice.

## File Access Troubleshooting

**Important**: Files in the `Clippings/` folder may contain special characters (apostrophes, spaces, percentage signs) that cause issues with direct file path access.

### Recommended File Access Methods:

1. **Primary Method**: Use `find` command with pattern matching:
   ```bash
   find "C:\Users\User\Downloads\General\Vanderbilt Money\Clippings" -name "*keyword*" -exec cat {} \;
   ```

2. **Alternative**: Use Bash `ls` to identify exact filenames, then try Read tool with precise paths

3. **Last Resort**: Use Task tool with general-purpose agent to locate and read problematic files

### When Direct Read Tool Fails:
- File names with special characters often cause "File does not exist" errors
- The `find -exec cat` approach bypasses path parsing issues
- Always verify file contents were actually accessed vs. generated summaries

This ensures reliable access to all Clippings content for content creation workflows.