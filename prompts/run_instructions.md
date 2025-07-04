# Running Gemini(Or similar) and Claude(Or similar)

# Setup 

## Step 1: Use Gemini for Planning

**Prompt:**
```
You are a master code designer and architech. Read the instructions in `prompts/gemini_prompt.md` and follow them to plan for a new feature:
[USER] 
Give the new feature or task, Here is an example, "Feature: Add location-based parking search to the app."
```

## Step 2: Use Claude to Execute the Next Task

**Prompt:**
```
You are a master code developer and test engineer. Read the instructions in `prompts/claude_prompt.md` and begin by implementing the next incomplete task in `docs/planning.md`.
```

[USER]
Repeat Claude prompts for each task until the feature is complete.
Add new features with Gemini prompts.
