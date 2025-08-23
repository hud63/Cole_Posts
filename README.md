# Content Creation Workflow

## Folder Structure
- **Clippings/**: Raw concept files and initial thoughts
- **prompts/**: High-quality prompts for content development
- **final drafts/**: Completed content pieces

## Workflow Process

### When tasked to create content:

1. **Review Clippings**: Always start by examining files in the `Clippings/` folder to understand the topic and core concepts
   - **Note**: If direct file access fails due to special characters in filenames, use: `find "Clippings/" -name "*keyword*" -exec cat {} \;`

2. **Select Prompt**: Choose appropriate prompt from the `prompts/` folder that matches the content type and requirements

3. **Gather Information**: The prompt will request specific information - extract this from the Clippings files and conduct any necessary research

4. **Research Phase**: Perform thorough research on the topic using available tools to ensure accuracy and depth

5. **Create Final Draft**: Follow the prompt instructions precisely, incorporating:
   - Information from Clippings files
   - Research findings
   - Structure and requirements specified in the prompt

6. **Output Location**: Save completed content in the `final drafts/` folder as `.md` files

7. **Archive Source Material**: After completing the final draft, move the source Clippings file(s) to the `used/` folder to maintain organization and avoid reusing content

## Key Principles
- Always read this README when starting content creation tasks
- Use Clippings as the foundation, prompts as the guide, research as the backbone
- All final content output should be saved as `.md` (Markdown) files
- Maintain consistency across all content pieces
- Follow prompt instructions exactly
- Ensure final drafts are polished and complete

This workflow ensures consistent, high-quality content creation every time.