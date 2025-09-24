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

### `/bush` - Bush Content Generator

Sequential dual-prompt content generation:

1. **Lists available topics** from the `Clippings/` folder
2. **Handles user selection** and reads content (including files with special characters)
3. **Processes through dual prompts**: Bush Hook Writer + Bush Post Creator
4. **Generates combined output**: 11 LinkedIn hooks + 3 posts (Framework, Story, Listicle)
5. **Saves final content** to `bush_final/` folder
6. **Archives source material** to `used/` folder

### `/erica` - Erica Framework Generator

Automated generation of 4 distinct social media posts using Erica frameworks:

1. **Lists available topics** from the `Clippings/` folder
2. **Handles user selection** and reads content (including files with special characters)
3. **Generates 4 framework posts**: Absurdist Conspiracy, Problem-Agitation-Solution, Declarative Expertise, Vulnerable Self-Reflection
4. **Character limit**: 2,800 characters MAX per post (non-negotiable)
5. **Saves final content** to `erica_final/` folder
6. **Archives source material** to `used/` folder

### `/lian` - Lian Content Generator

LinkedIn thought leadership content using Lian frameworks:

1. **Lists available topics** from the `Clippings/` folder
2. **Handles user selection** and reads content (including files with special characters)
3. **Generates LinkedIn content** using one of 5 formats: Personal Stories & Life Lessons, LinkedIn Growth Tactics, Business Strategy & Frameworks, Psychology & Human Behavior, or Contrarian Reality Checks
4. **Character limit**: 2,800 characters MAX per post (non-negotiable)
5. **Saves final content** to `lian_final/` folder
6. **Archives source material** to `used/` folder

### `/liz` - Liz Content Generator

Contrarian marketing thought leadership content:

1. **Lists available topics** from the `Clippings/` folder
2. **Handles user selection** and reads content (including files with special characters)
3. **Generates contrarian content** using one of 4 formats: Problem Reframing, Direct Advisory, Strategic Perspective, or Satirical Commentary that challenges industry norms
4. **Character limit**: 150-250 words to optimize for LinkedIn engagement
5. **Saves final content** to `liz_final/` folder
6. **Archives source material** to `used/` folder

### `/vanderbilt` - Vanderbilt Content Generator

Viral international opportunity content:

1. **Lists available topics** from the `Clippings/` folder
2. **Handles user selection** and reads content (including files with special characters)
3. **Generates viral LinkedIn content** using one of 10 formats: Investment/Business Residency, Citizenship by Descent, Retirement Visa, Tax Optimization, Digital Nomad/Remote Work Visas, Passive Income/Non-Lucrative Visas, Offshore Banking Services, Special Opportunities & Time-Limited Programs, Business/Entrepreneur Visas, or Educational/Informational posts
4. **Character limit**: 50-150 words to maintain viral potential while providing substance
5. **Saves final content** to `vanderbilt_final/` folder
6. **Archives source material** to `used/` folder

### Usage
- Type `/li` for LinkedIn content only
- Type `/sf` for short-form social content only
- Type `/both` for dual content generation
- Type `/bush` for Bush dual-prompt content generation
- Type `/erica` for Erica framework content generation
- Type `/lian` for Lian LinkedIn thought leadership content
- Type `/liz` for Liz contrarian marketing content
- Type `/vanderbilt` for Vanderbilt international opportunity content
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