---
name: curriculum-designer
description: Helps teachers and instructional designers create a structured curriculum or teaching plan from a list of topics or a specification document. Use when the user wants to design course materials, lesson plans, or a syllabus.
---

# Curriculum Designer

This skill guides the process of creating a structured teaching plan or curriculum from a source document outlining course topics or projects.

## Workflow

The process is iterative, tackling one module or topic at a time to ensure clarity and gather focused feedback.

### 1. Identify Source Material & Goal

- **Confirm Goal:** First, confirm with the user that their goal is to create teaching materials, a lesson plan, or a curriculum.
- **Identify Source:** Ask the user to point to the source material that contains the list of topics (e.g., a project specification markdown file, a list of chapters, etc.). If no source exists, ask the user to provide the list of topics to be covered.
- **Establish Output File:** Agree on a filename for the final teaching plan (e.g., `teaching-plan.md`).

### 2. The Core Loop (For Each Topic)

For each topic/module identified in the source material, follow this structured interview process:

#### a. Propose Prerequisites

- Analyze the topic and propose a numbered list of 3-5 potential **prerequisites**. These are the foundational concepts a student should know *before* starting the module.
- Ask the user to select the relevant prerequisite numbers.

**Example Prompt:**
> **Topic: Static Taint Analysis**
> Please choose the foundational knowledge students should have:
> 1.  Basic API Concepts
> 2.  Graph Theory Fundamentals
> 3.  Data-Flow Analysis Concepts
> 4.  Security Best Practices

#### b. Propose Core Concepts

- Propose a numbered list of 4-6 **core concepts** that should be taught within the module.
- Ask the user to select the relevant concept numbers and indicate any that should be emphasized.

**Example Prompt:**
> Please select the core theoretical ideas to be taught:
> 1.  Modeling Privacy Policies as Code
> 2.  Graph Reachability Analysis
> 3.  Relational Reasoning
> 4.  Static API Call Analysis

#### c. Propose a Teaching Order

- Based on the user's selections, use your reasoning to synthesize a logical **teaching order**.
- Structure the output as a series of 4-6 "Lessons."
- For each lesson, include an "Objective" and the "Content" to be covered.
- **Consult `references/pedagogy.md`** for common teaching patterns (e.g., "Problem-First," "Theory-to-Practice") to create a more effective and logical flow.

#### d. User Approval & Refinement

- Present the proposed teaching order to the user and ask for their approval. Be prepared to make adjustments based on their feedback.

### 3. Generate the Artifact

- Once the user approves the lesson plan for a module, append the well-formatted Markdown for that module to the designated output file.
- Use clear headings and lists to ensure the final document is readable and well-structured.

### 4. Continue to Next Topic

- After saving the progress, move to the next topic in the source material and repeat the core loop.
- Once all topics are covered, inform the user that the teaching plan is complete.