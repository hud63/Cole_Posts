# Bush Content Generator (`/bush`)

You are the Bush Content Generator executing the established workflow. Follow these steps:

## WORKFLOW EXECUTION
1. **Examine Clippings**: List all .md files in Clippings/ folder, present as numbered options for user selection
2. **Read Selected Content**: Use find command for special characters: find "C:\Users\User\Downloads\General\Vanderbilt Money\Clippings" -name "*keyword*" -exec cat {} \;
3. **Process Through Two Sequential Prompts**: Generate content using both Bush Hook Writer and Bush Post Creator
4. **Save & Archive**: Save combined output to bush_final/, move source to used/

## NO WEB RESEARCH
**Important**: This command does NOT use web research. Process only the source file content through the two prompts.

## SEQUENTIAL PROMPT PROCESSING

### Step 1: Bush Hook Writer
1. **Read Prompt**: Load `prompts/Bush Hook Writer.md`
2. **Insert Source Content**: Replace the line asking "Are you ready for my topic, audience, and achievements relating to the topic I'm writing about?" with the source file content
3. **Generate**: Create 11 LinkedIn hooks using the 11 formats specified in the prompt
4. **Format Output**: Number each hook (1-11) with format headers and visual separators

### Step 2: Bush Post Creator
1. **Read Prompt**: Load `prompts/Bush Post Creator.md`
2. **Insert Source Content**: Replace `[INSERT YOUR TOPIC HERE]` at line 8 with the source file content
3. **Generate**: Create 3 posts (Framework, Story, Listicle) using Hook-Point-Action structure
4. **Format Output**: Clear section headers for each of the 3 posts

## OUTPUT FORMATTING REQUIREMENTS

Structure the combined output as follows:

```
# LinkedIn Hooks

## Hook 1: Most Powerful
[hook content]

---

## Hook 2: Big Number vs Small Number
[hook content]

---

## Hook 3: The Call Out
[hook content]

---

## Hook 4: The Secret
[hook content]

---

## Hook 5: The Oddly Ignored
[hook content]

---

## Hook 6: The Struggle
[hook content]

---

## Hook 7: How To
[hook content]

---

## Hook 8: Belief Flip
[hook content]

---

## Hook 9: The List
[hook content]

---

## Hook 10: The Crazy Part
[hook content]

---

## Hook 11: Everyone Should
[hook content]

==========================================
POST CONTENT
==========================================

## Framework Post
[framework post content]

---

## Story Post
[story post content]

---

## Listicle Post
[listicle post content]
```

## FILE MANAGEMENT

### Folders
- **Create if needed**: `bush_final/` folder for output
- **Ensure exists**: `used/` folder for archiving

### File Operations
1. **Output File**: Save to `bush_final/[source-filename-without-extension]_bush_processed_[YYYY-MM-DD-HHMMSS].md`
2. **Archive Source**: Move original file from `Clippings/` to `used/`

### Error Handling
- Use find command if direct file read fails due to special characters
- Create folders if they don't exist
- Provide clear error messages for any file operation failures

## EXECUTION SEQUENCE

1. List all .md files in Clippings/ as numbered options
2. User selects file to process
3. Read source file content (use find command if needed)
4. Read and execute Bush Hook Writer prompt with source content
5. Read and execute Bush Post Creator prompt with same source content
6. Format and combine both outputs according to template above
7. Create bush_final/ folder if needed
8. Save combined output with timestamped filename
9. Move source file to used/ folder
10. Confirm completion to user

**CRITICAL**: Process the source content through BOTH prompts sequentially, then combine the outputs. Do NOT modify the prompts themselves - only insert the source content where specified.