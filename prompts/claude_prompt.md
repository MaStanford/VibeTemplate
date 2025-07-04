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
   - Use `docs/code_style.md` and `docs/stack.md` as references

4. Implement only the current task. Do not make changes outside the scope.
5. Implement testing for the curret task. 
7. Do not modify markdown unless instructed.
6. Mark task as complete with checkmark. 

## Output:
- Code changes in the relevant files
- Optionally, test or validation output in a `tests/` directory
- Do not modify markdown unless instructed
- Mark the task as complete with a checkmark. 