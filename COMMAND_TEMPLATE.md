---
description: [Command Name] - [Brief, one-line description of the command's purpose]
---

# 🌀 [Command Name]

> [A brief, memorable tagline for the command. e.g., "Chart the course for new features!"]

## 1. PLAN 🎯 (規劃)

### Objective
> [Clearly state the single, primary goal of this command in one sentence. What is the desired outcome?]

### Prerequisites Check
> [A non-negotiable checklist of conditions that MUST be true before proceeding. This is the entry gate for the command.]
- ✅ **Condition 1:** [e.g., `memory-bank/projectbrief.md` exists and is filled.]
- ✅ **Condition 2:** [e.g., No uncommitted changes in the git repository.]
- ❌ **Failure Action:** If prerequisites are not met, provide clear, actionable instructions. e.g., "Please run `git status` and commit any changes before proceeding."

## 2. DO 実行 (執行)

### Core Process
> [A numbered list of the high-level steps the AI will take. This is the core workflow.]
1.  **Analyze:** [e.g., Read `projectbrief.md` to understand the core requirements.]
2.  **Synthesize:** [e.g., Generate a task breakdown based on the analysis.]
3.  **Output:** [e.g., Write the task list to `memory-bank/tasks.md`.]

### Key Inputs & Outputs
> [Specifies the exact artifacts this command interacts with.]
*   **Inputs:** 
    *   [File/document that will be read, e.g., `memory-bank/projectbrief.md`]
    *   [Environment variables or state that will be checked]
*   **Outputs:** 
    *   [File/document that will be created or modified, e.g., `memory-bank/tasks.md`]
    *   [A summary report or a log file]

## 3. CHECK ✓ (檢查)

### Verification Checklist
> [A checklist to verify that the 'Do' phase was successful and the objective was met. This ensures quality and correctness.]
- [ ] **Result 1:** [e.g., `memory-bank/tasks.md` is created and is not empty.]
- [ ] **Result 2:** [e.g., The generated tasks are aligned with the `projectbrief.md`.]
- [ ] **Quality Gate:** [e.g., The output file is correctly formatted in Markdown.]

## 4. ACT 改善 (行動)

### Finalization
> [Actions to take after successful verification. This concludes the current command's lifecycle.]
- [ ] **Cleanup:** [e.g., Remove any temporary files created during the process.]
- [ ] **State Update:** [e.g., Update `progress.md` to log the completion of this command.]

### Next Steps
> [Clear guidance on what the user or AI should do next. This connects the commands into a cohesive workflow.]
- 👉 **Primary Next Step:** Run `/[next_command]` to [achieve the next logical goal].
- 💡 **Alternative:** If [some specific condition is met], you might want to run `/[alternative_command]` instead.

---
> **[Command Name] activated. [Brief, encouraging message to signal the start of the process.]**
