---
title: "The AI-Native Office Suite - Can AI Do Work For You?"
source: "https://a16z.com/the-ai-native-office-suite-can-ai-do-work-for-you/?utm_source=www.theneurondaily.com&utm_medium=newsletter&utm_campaign=microsoft-and-openai-bury-the-hatchet&_bhlid=df6bd6c5bdaa8e67ffb1cfd0860380665d4273c0"
author:
  - "[[Daisy Zhao]]"
  - "[[Olivia Moore]]"
published: 2025-09-11
created: 2025-09-12
description: "AI-powered productivity tools are emerging as both generalist platforms and specialized applications. We benchmarked over a dozen to see how they perform across core tasks like email, spreadsheets, presentation, research and meeting notes."
tags:
  - "clippings"
---
AI isn’t just a feature anymore – it’s becoming a teammate! From drafting emails to designing slides, researching markets, or building financial models, a new layer of “agentic” tools is emerging that resemble an AI-native Office suite.

But here’s the challenge: as of now the landscape is fragmented, with new tools emerging every week. Anthropic just launched an “ creating and editing file ” feature for Claude this week! Consumers are left wondering: which tool should I actually use, and in what scenarios can I start embedding agentic tools into my daily work?

To find out how these tools perform in practice, we mapped the market and benchmarked AI-native tooling across a variety of everyday office tasks – making spreadsheets, taking meeting notes, and writing emails. Our benchmarks found impressive performance by a number of generalist tools, some standout vertical applications, and a few hints about how the marketplace is developing.  

Two Paths to Agentic Productivity: Generalists vs. Specialists

The market is splitting into two approaches to agentic productivity. On one side are the “all-in-one” horizontal tools, built to handle anything across apps and tasks. On the other are vertical specialists, designed to go deep into a single workflow like email, slides, or spreadsheets. Both are evolving quickly – and both have tradeoffs.

(

Generalists – Horizontal tools  
Generalist tools are designed for flexibility. They can move across different contexts, apps, and tasks, but often at the cost of polish and precision. Within this camp, three formats stand out:

1. General Assistants: horizontal web tools that are typically multimodal, prompt-based, and sometimes memory-enabled to execute several types of tasks.
	- Examples: Operator, Manus, Genspark.
2. Agentic Browsers: autonomous browsing and task execution across the web. Some options, like Comet, add more sophisticated features such as shortcuts that replay workflows when triggered by keywords.
	- Examples: Dia, Perplexity Comet, Browserbase.
3. Browser Extensions: lightweight helpers layered on top of existing workflows and interfaces.
	- Examples: MaxAI, Merlin, Monica.

Specialists – Vertical Tools  
Specialist tools are built for depth and reliability. Instead of trying to do everything, these tools focus on structured workflows where trust, polish, and user control are critical. Today’s vertical landscape is anchored by tools covering core professional workflows.

1. Email Assistants: assistants that draft structured replies, manage inbox triage, and handle scheduling tasks.
	- Examples: Fyxer, Serif, Jace.
2. Presentation Tools: AI-powered tools that create slides with an emphasis on visual design, speed, and editability.
	- Examples: Gamma, Chronicle, Beautiful.ai.
3. Note & Document Tools: tools for structured writing, note taking, knowledge capture, and collaborative editing.
	- Examples: Mem, Notion, Granola.
4. Spreadsheet Tools: applications that handle data extraction, formatting, and analysis. They can extend in the direction of research or workflows.
	- Examples: Paradigm, Shortcut, Meridian, Julius.

Benchmark: Do These Products Actually Work?

To see how these tools perform for real-world tasks, we tested them against benchmarks to measure where they succeed and where they fall short.

The prompts were designed to span six core dimensions: summarization, communication, file understanding, research, planning, and execution.  

Use Case 1: PowerPoint  
Prompt:Design a visual-heavy, 7-slide deck about Gen Z internet behavior trends in 2025.

(

Gamma acts as a verticalized AI-powered presentation tool with built-in templates and design features that allow a deck to be generated in under two minutes. As a full presentation editor, it offers a wide range of controls for editing after generation – users can adjust layouts, change visuals and fonts, add charts, and prompt the AI for text or design suggestions.

Genspark and Manus, operating as general assistants, tend to produce decks that are more content-heavy, often closer to research reports. Their outputs take longer to generate but tend to exhibit deeper analysis and stronger prompt alignment. ChatGPT Agent produced simpler decks resembling text-based reports, with weaker design capabilities and much longer generation time.  

Anthropic just launched file creation and editing in Claude this week. On the presentation generation task, it’s the fastest general-purpose agent we’ve tested, though the design still needs refinement.  

Overall, if you need a presentation for external use where visual quality and post-generation control are critical, Gamma is the best pick. If you’re looking for a content-heavy deck to inspire research or analysis, Genspark is the better choice.  

Use Case 2: Spreadsheet  
Prompt:Extract all the data from this PDF and calculate operating margin.

(

Spreadsheets are a sophisticated use case. Their complexity is particularly pronounced for outputs like complex financial models, where both formatting and exact accuracy are crucial. Still, AI spreadsheet tools are beginning to show signs of working for more basic and mid-level tasks, such as extracting data from PDFs and performing basic financial calculations.

In this test, we uploaded a page from an S-1 filing and asked the tools to calculate the company’s operating margin. Among the horizontal agents, Manus performed best: it extracted the data into a structured spreadsheet format and quickly returned accurate results. Claude was also the fastest in spreadsheet tasks and produced the correct answer, but its output was limited – providing minimal analysis and failing to pull the full set of data into the sheet.

Shortcut, as a vertical Excel-focused agent, offered a more comprehensive analysis in a native Excel environment, though it took longer to run and extracted only the data relevant to the calculation rather than the full dataset.  

Use Case 3: Email  
Prompt:email to schedule a dinner on next Thursday

(

Fyxer, Serif, and Jace function as vertical assistants for email. Each can generate competent drafts and maintain context across threads. Serif stands out for its level of customization: it supports playbooks, email labels, and preference settings – giving users a way to encode best practices and apply consistent workflows across similar scenarios.

Their approaches to scheduling diverge – but all were able to execute on a simple scheduling task:

Serif enables asynchronous coordination. You can copy the agent on your emails to handle back-and-forth scheduling and send calendar invites.
Fyxer generates a Calendly-style link for others to book a time.
Jace takes a lighter-touch approach, generating events but waiting for user approval before sending.

By contrast, Comet brings general-assistant capabilities into email. It can draft replies, follow prompts to schedule meetings, send invites, and search the inbox. But it lacks built-in customization features like playbooks, labels, or preferences – so drafts feel less tailored compared to dedicated email assistants.  

Use Case 4: Research  
Prompt:Summarize and compare the latest quarterly cloud revenue growth for Microsoft, Amazon, and Google in a table with sources, then analyze the drivers behind the results in a short report.

(

Thanks to AI tools, consumers can now generate deep and research-informed analyses in seconds – work that previously might have taken hours of work and years of prior experience.

All of the products we tested were able to pull the correct cloud revenue growth numbers and organize them into tables. The differences came in nuance and speed – reflecting each product’s underlying optimizations and constraints.

Comet and Dia, the two AI-native browsers, were the fastest. They returned results in under 20 seconds, but their outputs were lighter on analysis and less structured compared to Manus, which delivered more comprehensive tables and deeper explanations of the drivers behind the numbers.

Source quality also varied. Comet and ChatGPT Agent stood out for drawing directly from authoritative sources such as earnings reports and Yahoo Finance, often including inline citations that made it easier to verify accuracy.

Overall, the tradeoff is clear: if you prioritize deeper analysis and are less sensitive to process time, Manus is the strongest choice. If you value speed and want a quick, decent answer, Comet is a better fit.  

Use Case 5: Meeting Note-taking  
The notepad is on during a meeting

(

Meeting note-taking is one of the most natural AI applications, saving consumers energy by letting them focus on the conversation instead of typing. Tools in this category generally operate in a notepad format, automatically transcribing and structuring the discussion, while ChatGPT’s record mode offers a more lightweight alternative. All of the products benchmarked support retrieval through keyword search, but their strengths diverge across note quality, customization, and collaboration.

Mem produces the most exhaustive records, capturing discussions and action items in detail, while ChatGPT’s record mode offers higher-level summaries that are easier to skim but less complete. Granola differentiates with customizable templates that adapt to different meeting types, giving users more control over structure and output.

Granola, Mem, and Notion all allow users to prepare notes in advance, add guidance during the meeting, and follow along with real-time transcription. Notion stands out for collaboration: tasks can be assigned directly within notes, synced to Notion Calendar, and aligned with broader team workflows.

Overall, if you want comprehensive capture, Mem is the best fit; for structure and customization, Granola excels; and for team coordination, Notion is the strongest choice.  

Observations from Testing

From running tests across these use cases, several patterns emerged:

1. Patterns of differentiation are already clear. Vertical products stand out through design and workflow polish – focusing on the work “surface” or canvas and embedding deeply into professional workflows. This makes them especially strong for external-facing use cases where refinement and presentation matter. Horizontal products, by contrast, emphasize breadth: they compete to be the “all-in-one” entry point by layering on adjacent tasks. Manus, for instance, already spans research, presentations, and spreadsheets, positioning itself as the single place where work begins.
2. Competition is heating up for horizontal products – including from model companies. General assistants and agentic browsers are in a race to become the core UI for work. Given the importance of both speed and accuracy, companies that are closer to the model development may have a better chance at delivering. Major research labs are still entering the race: Anthropic has recently launched a browser copilot for Claude, and we expect more attempts from OpenAI and other players.
3. Convergence is coming. The sharp lines between vertical and horizontal agents are starting to blur, as vertical products look to “jump” into new categories and horizontal platforms double-down on popular use cases. If you’re building vertical, make sure to keep up with and build on the newest model primitives. If you’re building horizontal, you need workflows and iteration loops deep enough that vertical players can’t carve out your use cases.

- X
	- Linkedin
- X
	- Linkedin