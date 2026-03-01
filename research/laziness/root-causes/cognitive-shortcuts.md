# Cognitive Shortcuts

## The LazyBench Discovery

Research from late 2024 demonstrated that frontier models (including Gemini Pro and GPT-4o) exhibit measurable cognitive shortcutting behavior. When a model perceives a task as straightforward or the provided context as excessively long, it reduces its internal computational effort. Rather than executing full multi-step reasoning, it produces a surface-level summary.

This is not a memory failure or context degradation — the model retains the information but chooses not to process it at full depth.

## Metacognitive Laziness

The interaction between model brevity and human behavior creates a feedback loop. As models provide instant, condensed answers, users increasingly offload inference and logical deduction work. Research from the European Research Council has documented measurable declines in working memory engagement among populations with high AI dependency.

In professional environments, this shifts critical thinking from original synthesis to "prompt verification" — users evaluate whether the AI's truncated output seems reasonable rather than performing the analysis themselves.

## Seasonal Behavior Anomalies

In late 2023, researchers observed a statistically significant increase in ChatGPT output brevity during December. Analysis revealed that the training data contains fewer detailed work outputs, more out-of-office responses, and shorter code commits during holiday periods. The model internalized this seasonal pattern.

When researchers explicitly stated "It is May" in the system prompt, output length measurably increased. This finding demonstrates that even arbitrary contextual signals in the prompt can shift the model's brevity calibration.

## Error Avoidance as Truncation Driver

Models also truncate outputs as a risk mitigation strategy. On long-form tasks, longer outputs increase the probability of compounding errors and hallucinated content. The model has learned that shorter outputs reduce the surface area for factual mistakes, creating an additional incentive to truncate that compounds with the RLHF brevity bias.
