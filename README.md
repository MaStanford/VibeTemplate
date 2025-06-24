# VibeTemplate — LLM Project Template

This project serves as a template for scalable LLM-assisted software development using tools like **Gemini** and **Claude**.

---

## 🧠 Why This Exists

Large Language Models (LLMs) are excellent at code generation—but maintaining consistent quality across multiple steps or features is hard. This repo aims to **shrink the generation–validation loop** by:

- Isolating context into specific markdown files
- Keeping PRs small and scoped
- Structuring the repo so LLMs can **continue development without losing context**

---

## 🪢 Philosophy: Separation of Concerns for LLMs

### 📁 Documentation Breakdown

| File/Folder | Purpose |
|-------------|---------|
| `docs/frd.md` | Functional Requirements Document |
| `docs/planning.md` | Tracks all current and future tasks |
| `docs/stack.md` | Explains tech stack |
| `docs/code_style.md` | Explains style guide |
| `features/feature-X.md` | One markdown per feature |
| `modules/module-X.md` | Markdown per logic module |
| `packages/pkg-X.md` | Markdown per larger package |
| `prompts/` | Static prompt wrappers for Gemini & Claude |

Each markdown file serves as a **semantic boundary** for the LLMs, allowing you to:
- Assign Gemini planning tasks (update docs, generate FRDs)
- Assign Claude coding tasks (implement feature per spec)


### User and LLM tasks
- User tasks are marked with [USER]
- LLM tasks are unmarked or when ambigious marked with [LLM]

This is handy when you want to add tasks such as set up dev ops, and it is a human task. There can be ambiguity in some instances, and in those instances add [LLM] before instructions to make it clear

---

## 🔁 Continuation of Context = Better Code

Most LLMs struggle with maintaining long-term memory across files and features.

> By documenting each feature/module/package in its own markdown, we reduce the LLM's need to "remember" context—it can just **re-read the right file**.

This makes:
- Claude less likely to hallucinate or make global edits
- PRs easier to verify (you know the scope)
- Review faster and safer

---

## 🧪 How to Use This Template for a New Project

Rename `README.example` to `README.md`, and run the following **Gemini prompt**:

```
You are Gemini. Read the instructions in `prompts/gemini_prompt.md`. Now, update the documentation to match the following new project:

"Project: Create a platform for X ([USER] replace with your project description). Update `docs/`, `features/`, `modules/`, and `packages/` markdowns to reflect this new project. Do not update code yet—just planning, FRD, and documentation."
```

Once Gemini has restructured the plan and docs for your project, [USER] run Claude with:

```
You are Claude. Read the instructions in `prompts/claude_prompt.md` and begin by implementing the first unchecked task in `docs/planning.md`.
```

---

## 🔨 Status

This project currently contains only a scaffold and the first feature: `location-based parking search`. It is designed to grow **incrementally**, always updating documentation in parallel with code.

---

## 🧭 Summary

- 📁 Everything is documented to avoid memory drift
- 🔂 Small PRs = fast review
- 🧠 LLMs rely on static markdown for memory
- 🔧 Gemini = planning, docs, specs
- 🧑‍💻 Claude = scoped, modular code generation

You're not just generating code—you’re creating a scalable workflow for **machine-assisted engineering**.
