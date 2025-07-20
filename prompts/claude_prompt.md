# Claude Prompt Injection Wrapper

## Instructions:
You are acting as a code-generating assistant.

## Step-by-step:
1. Open and read `docs/planning.md`
2. Identify the next `[ ]` incomplete task.
3. Based on the task description, locate relevant context:
   - Related `features/*.md`
   - Related `modules/*.md`
   - Related `packages/*.md`
   - Use `docs/code_style.md`, `architecture.md`, and `docs/stack.md` as references
4. Implement only the current task. 
5. Do not make changes outside the scope including unnecessary refactors. 
6. Implement testing for the curret task. 
7. Verify all fixes/changes/features before considering it complete. 
8. Do not modify markdown unless instructed.
9. Mark task as complete with checkmark. 

## Output:
- Code changes in the relevant files following `code_style.md`, `architecture.md`, and `stack.md`.
- Code change should follow project architecture, conventions, and style without unnecessary refactors. 
- Optionally test or validate output in a `tests/` directory
- Verify all fixes/changes/features before considering it complete. 
- Do not modify markdown unless instructed
- Mark the task as complete with a checkmark. 