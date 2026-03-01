# Prompt Engineering Techniques

## Psychological Pattern Matching

LLMs do not have emotions or understand monetary incentives. However, specific linguistic patterns in the prompt activate different quality distributions in the model's latent space. Research has documented measurable effects:

| Technique | Documented Effect |
|:---|:---|
| "I will tip you $200 for a perfect solution" | Up to 45% increase in output quality and length |
| "Take a deep breath and solve step by step" | Accuracy improvement from 34% to 80% on logic tasks |
| "This task is critical to my career" | Average 10% performance increase |

These phrases work because they are statistically correlated with high-effort, rigorously reviewed content in the training data (academic papers, enterprise codebases, legal documents). The attention mechanism prioritizes the high-quality data distributions associated with these patterns.

## Explicit Syntax Binding

Conversational requests allow the model to exercise discretion about output length and detail. Structural binding removes this discretion by explicitly prohibiting truncation patterns.

Effective binding requires two components:

1. **Mandatory tool execution:** Forbid the model from generating answers solely from training weights. Require it to execute search, computation, or code before answering.
2. **Evidence blocks:** Require the model to output raw data (URLs, code execution results, data fragments) before producing its narrative response. This forces the model to read its own retrieved evidence, reducing hallucination probability to near zero.

## XML-Structured Prompts

Enterprise systems use strict XML tagging to separate prompt components, reducing the cognitive load required for the model to parse intent:

1. **System instructions** — Persona definition, quality expectations, explicit prohibitions on filler content.
2. **Context block** (`<context>`) — Passive background data: architecture details, configurations, existing code.
3. **Data block** (`<data>`, `<logs>`, `<config>`) — Active information the model must process against the context.
4. **Task block** (`<tasks>`) — Numbered list of specific actions to execute.

This compartmentalization ensures the model can distinguish between persistent rules, background context, and immediate work items. It significantly reduces the confusion that triggers premature truncation.

## Verification Loops

### Chain of Verification
1. Model generates an initial response
2. Model generates verification questions about its own claims
3. Model independently answers those verification questions
4. Model outputs a revised, evidence-backed response

This process forces iterative self-correction, consuming the model's capacity for shortcutting.

### Reverse Prompting
Instead of manually constructing a structured prompt, provide the model with a one-line objective and instruct it to generate the optimal prompt for that objective. The model produces the XML structure, constraints, and roles required for the task.

### Self-Grading Loop
The prompt requires the model to:
1. Define what excellence looks like for the given task
2. Grade its own initial output against that definition
3. Iterate until the self-defined quality bar is met
