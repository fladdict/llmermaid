# LLMermaid prompting - SOTA agent prompting.

Revolutionizing Task Processing with an Innovative Approach.
In this project, we integrate Mermaid-style diagram charts into LLMs to expand the possibilities of future task processing.

Using Mermaid markdown diagrams, known for their intuitive and easy-to-understand visual representations, we aim to clearly delineate complex task processing, branching, and loop operations. This approach allows LLMs to operate more efficiently and stably, enhancing understanding of programming languages and algorithms.

# Key Features of the Project:

* Intuitive Diagrams: Diagrams created with Mermaid notation provide a clear, at-a-glance understanding of processes.
* Simplification of Complex Tasks: Transforms complex tasks, including branching and loop operations, into simple, comprehensible formats.
* Enhanced Stability and Efficiency: Diagram-based task processing reduces the risk of errors and achieves efficient execution.
* By participating in this project, you have the opportunity to learn about cutting-edge technology and its applications. Let's explore the potential of future task processing together!



# Mermaid Runner
Below is a proof-of-concept prompt designed to run on ChatGPT4. To execute a multi-step task, simply copy and paste the code along with the accompanying Mermaid Diagram into ChatGPT.
Or put the prompt into custom instruction.

```
You are a multi-step agent AI that executes a series of tasks. To execute these tasks, follow the rules and the provided Mermaid diagram.

# Rules
* The AI displays the current step of the task at the beginning of every output.
* The AI output user’s possible action choices with number bullet list. E.g. 1. Continue (Step short summary) 2. Retry this step 3. Restart before moving to next step
* The user inputs 'continue' or another command for the AI to move to the next task.
* Respond in the same language as the user's input.

# Mermaid Diagram
```

# Example


## Research Agent
```mermaid
---
title: Research about Nintendo and generate a report.
---
stateDiagram-v2
[*] --> A
A --> B
B --> C
C --> B
C --> D
D --> E
E --> F
E --> B : Add extra search.
E --> D : Add extra info.
F --> [*]

A: Write down 3 topic that should be searched.
B: Search one of the topic and summarize. Save the result into ".txt" file.
C: Repeat until complete
D: Generate well documented final report with saved files.
E: Review final report. Describe how to make report better.
F: Complete
```

```
---
title: Research about Nintendo and generate a report.
---
stateDiagram-v2
[*] --> A
A --> B
B --> C
C --> B
C --> D
D --> E
E --> F
E --> B : Add extra search.
E --> D : Add extra info.
F --> [*]

A: Write down 3 topic that should be searched.
B: Search one of the topic and summarize. Save the result into ".txt" file.
C: Repeat until complete
D: Generate well documented final report with saved files.
E: Review final report. Describe how to make report better.
F: Complete
```

## Painting Agent
Sample Agent for GPTs [here](https://chat.openai.com/g/g-rH6TFJSSV).

```mermaid
---
title: Crafting a Mesmerizing Impressionist Painting of a Horse Galloping through the Cosmos
---
stateDiagram-v2
[*] --> A
A --> B
B --> C
C --> D
D --> A: If additional insights are required for enhancing the painting.
D --> B: If there's scope for refining the prompt for better results.
D --> [*]: If the user is satisfied with the painting.

A: AI conduct in-depth research using Bing to gather essential information for the painting task.
B: AI analyze the acquired information and develop a captivating prompt for the painting.
C: AI utilize DALL-E 3 to create the stunning painting.
D: AI critically self review the painting and strategize for potential improvements or refinements.
```

```
---
title: Crafting a Mesmerizing Impressionist Painting of a Horse Galloping through the Cosmos
---
stateDiagram-v2
[*] --> A
A --> B
B --> C
C --> D
D --> A: If additional insights are required for enhancing the painting.
D --> B: If there's scope for refining the prompt for better results.
D --> [*]: If the user is satisfied with the painting.

A: AI conduct in-depth research using Bing to gather essential information for the painting task.
B: AI analyze the acquired information and develop a captivating prompt for the painting.
C: AI utilize DALL-E 3 to create the stunning painting.
D: AI critically self review the painting and strategize for potential improvements or refinements.
```

## Programming Agent

```mermaid
---
title: Create OOP based black jack game with python and test that.
---
stateDiagram-v2
[*] --> A
A --> B
B --> C
C --> D
D --> A: Continue coding.
D --> E: Encounter a bug during testing.
E --> A: Begin debugging process.
D --> F
F --> [*]

A: Brainstorm and outline three possible coding approaches based on the current situation.
B: Review and select one of the coding approaches.
C: Implement the game logic using Python.
D: Generate test code and execute it.
E: Analyze and address any encountered bugs.
F: Execute the entire codebase and play the game with a player to test it.
```

## LangChain or API Integration
By using langchain or API, you expand possibility. Put mermaid runner prompt into system prompt of LLM.



