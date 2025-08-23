# Claude Code Configuration

## Slash Commands

### `/li` - LinkedIn Content Generator

Automated LinkedIn content creation following the established workflow:

1. **Lists available topics** from the `Clippings/` folder
2. **Handles user selection** and reads content (including files with special characters)
3. **Applies LinkedIn Post template** with all formatting rules:
   - 5 content styles (Steps, Stats, Mistakes, Lessons, Examples)
   - Hook structure (first 200 characters)
   - Skimmable headers with alternating formats
   - Sell-the-reader introductions
   - 2,800 character limit (non-negotiable)
4. **Saves final content** to `final drafts/` folder
5. **Archives source material** to `used/` folder

### `/sf` - Short Form Content Generator

Automated short-form social media content creation:

1. **Lists available topics** from the `Clippings/` folder
2. **Handles user selection** and reads content (including files with special characters)
3. **Generates 5 Twitter/X posts** using Short Form template:
   - 8:30am PT: Paragraph Style (declarative perspective)
   - 11am PT: What/How/Why (hook + bullets + insight)
   - 1pm PT: Listicle (list of tangible items)
   - 3:30pm PT: Old vs New (comparison format)
   - 7pm PT: 10 Magical Ways (tips/stats/lessons/etc.)
   - 280 characters MAX per post (non-negotiable)
4. **Saves final content** to `short form final drafts/` folder
5. **Archives source material** to `used/` folder

### `/both` - Dual Content Generator

Automated creation of both LinkedIn AND short-form content from same source:

1. **Lists available topics** from the `Clippings/` folder
2. **Handles user selection** and reads content (including files with special characters)
3. **Generates LinkedIn post** (2,800 chars) with full formatting rules
4. **Generates 5 short-form posts** (280 chars each) with time slots
5. **Saves LinkedIn content** to `final drafts/` folder
6. **Saves short-form content** to `short form final drafts/` folder
7. **Archives source material** to `used/` folder (only after BOTH are complete)

### Usage
- Type `/li` for LinkedIn content only
- Type `/sf` for short-form social content only  
- Type `/both` for dual content generation
Follow the interactive prompts to generate content.

### Files Created
- `slash_commands.json` - Command configuration
- `handlers/linkedin_content_generator.js` - Implementation handler (optional)

### Integration
The slash command integrates all functionality from:
- `README.md` workflow process
- `prompts/Linkedin Post.md` template
- `CLAUDE.md` guidelines
- File handling for special characters

This maintains the exact same output quality as the manual workflow but provides a single-command experience.