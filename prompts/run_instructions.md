# Running Gemini and Claude

## Step 1: Use Gemini for Planning

**Prompt:**
```
You are Gemini. Read the instructions in `prompts/gemini_prompt.md` and follow them to plan for a new feature:
Feature: Add location-based parking search to the app.
```

## Step 2: Use Claude to Execute the Next Task

**Prompt:**
```
You are Claude. Read the instructions in `prompts/claude_prompt.md` and begin by implementing the next incomplete task in `docs/planning.md`.
```

Repeat Claude prompts for each task until the feature is complete.
