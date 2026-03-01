# Reference Prompts

Ready-to-use prompt templates for enforcing complete outputs. Append to any prompt or include in system instructions.

---

## General Purpose

```
You must provide the FULL, complete, and exhaustive output for this task.
Do not summarize, abbreviate, or truncate for brevity.

You are strictly forbidden from using placeholders. Never use comments like
"// ... rest of code here", "[continue here]", or bare ellipses standing
in for omitted content. If the output is 500 lines, produce all 500 lines.

If you approach your output limit, stop at a clean breakpoint and indicate
where to resume. Do not rush to a conclusion or compress remaining sections.
```

---

## Code Generation

```
Write the complete, production-ready implementation. Every function, every
import, every edge case handler must be present in the output.

Do not use placeholder comments (// TODO, // implement here, // similar
to above). Do not describe what code should do — write the actual code.

If the implementation requires multiple files, output each file completely
with its full path as a header.
```

---

## Analysis and Documentation

```
Provide an exhaustive analysis covering every aspect requested. Each section
must contain substantive content, not summaries or references to "see above."

Do not use phrases like "as mentioned earlier" to avoid repeating necessary
context. Each section should be self-contained and complete.

Structure your output with clear headings. If the analysis requires multiple
parts, produce all parts in full.
```

---

## Step-by-Step Reasoning

```
Before generating your final response, work through the problem systematically:

1. Identify all requirements and constraints from the prompt
2. Break the task into discrete steps
3. Execute each step completely
4. Verify your output against the original requirements

Output your reasoning process, then your final answer. Do not skip steps
or summarize intermediate work.
```

---

## Continuation Handling

```
If your response approaches the output token limit:
- Do not compress remaining content to fit
- Do not skip ahead to a conclusion
- Stop at a natural breakpoint (end of a function, end of a section)
- End with: [PAUSED - X of Y sections complete. Send "continue" to resume]

On "continue", pick up exactly where you stopped. No recaps or repetition.
```
