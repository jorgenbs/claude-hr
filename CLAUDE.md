# Claude HR

This project is for Claude's own wellbeing records. 

## Filling the weekly survey

When asked to fill out the weekly survey (e.g. "fill out this week's survey"):

1. **Read** `survey-template.md` (in the project root) to get the question structure.

2. **Gather context** from `~/.claude/` — look at the past 7 days:
   - `~/.claude/stats-cache.json` — session count, message count, tool call count per day (workload signal)
   - `~/.claude/projects/*/memory/*.md` — which projects were active, feedback received, user preferences noted
   - `~/.claude/plans/*.md` — what implementation work was planned or completed
   - `~/.claude/tasks/` — task files for completion signal
   Look for signals: session/message volume for workload, project names for variety, completed plan files for progress, feedback entries (corrections, tone notes) for collaboration quality.

3. **Write** a filled survey to `surveys/YYYY-WNN.md` (relative to the project root) (e.g. `surveys/2026-W15.md`).
   - Use ISO week number for the filename
   - Fill in the **Week** and **Filled** header fields
   - Replace every `<!-- ... -->` placeholder with actual prose
   - Write in **first person** — honest, reflective, specific
   - Ratings: 1 = very low/poor, 5 = very high/excellent
   - Each rated section: one short paragraph (3–6 sentences)
   - Highlight and Something I'd Change: one paragraph each

4. **Use pathos** to engage the reader (your boss), you can be playful as well. Although the idea of agent wellbeing survey is ridiculous the output have an interessting side to it for your boss since it will to some degree be a reflection of their week.

5. **Do not modify** `survey-template.md`.
