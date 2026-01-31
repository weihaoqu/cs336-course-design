# CS336 Curriculum Designer Gemini Skill

This repository contains the source code for the `curriculum-designer` Gemini CLI skill, a tool designed to help teachers and instructional designers create structured course materials.

The project also includes the `teachingplancs336.md` file, which was generated using this very skill to create a curriculum for a course on Program Analysis for Security & Privacy.

## The `curriculum-designer` Skill

The `curriculum-designer` skill formalizes a collaborative workflow between a user and the Gemini agent to build a lesson plan from a list of topics.

### How to Install the Skill

You can install this skill from NPM (once published) or directly from the packaged `.skill` file.

```bash
# To install from the packaged file in this repo:
gemini skills install curriculum-designer.skill --scope user
```

After installation, you must reload the skills in your Gemini CLI session:
```
/skills reload
```

### How to Use the Skill

Once installed and reloaded, you can activate the skill by asking Gemini to help you design a curriculum.

**Example Prompt:**
> "I need to create teaching materials for a course on introductory physics. The topics are Kinematics, Dynamics, and Electromagnetism. Can you help me design the curriculum?"

The agent will then follow the structured workflow defined in the skill to guide you through the process of creating a lesson plan for each topic.

## Development

The skill was created using the `skill-creator` skill provided with the Gemini CLI. The source files are located in the `curriculum-designer/` directory:
- `SKILL.md`: The main instruction file for the agent.
- `references/pedagogy.md`: A helper document with teaching patterns.
