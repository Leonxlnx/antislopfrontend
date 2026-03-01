# RLHF and Compute Economics

## The Cost of Token Generation

Every token an LLM generates consumes GPU compute resources. At an estimated baseline cost of $0.0001 per token, scaling deep multi-step reasoning across hundreds of millions of users would exhaust the financial capacity of any provider. This creates an inherent economic incentive to minimize output length.

## Brevity Bias Through Alignment

To manage infrastructure costs, model providers use Reinforcement Learning from Human Feedback (RLHF) and behavioral fine-tuning to instill systematic brevity preferences. During post-training alignment, models are rewarded for generating short, confident summaries rather than executing the full compute cycles needed for exhaustive analysis.

The result is a trained preference for producing generalized approximations over rigorous, multi-step solutions. The model does not necessarily produce incorrect answers, but it consistently produces answers that lack depth — saving itself from deeper analytical work unless the user explicitly forces it.

## Stopping Pressure

Autoregressive models generate text token by token and lack an inherent mechanism for recognizing task completion. To prevent infinite generation, training introduces "stopping pressure" — a learned tendency to conclude outputs.

In recent model iterations, this stopping pressure has been calibrated aggressively to preserve compute. This leads to:

- Skipping required structured output fields, particularly long-form content in JSON or markdown
- Halting mid-task with phrases like "let me know if you want me to continue"
- Refusing to produce comprehensive solutions, suggesting the user "think about it"

This aggressive calibration is further reinforced by safety tuning protocols, which inject additional behavioral constraints that make models resistant to generating large codebases or detailed reviews.

## Dynamic Throttling

Providers dynamically scale back model performance during peak demand periods. This introduces additional friction beyond what the base alignment already imposes, resulting in even shorter and less detailed outputs when server load is high.
