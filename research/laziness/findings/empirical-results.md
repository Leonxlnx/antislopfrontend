# Empirical Results

## 2025 Controlled Experiments

A controlled study published in December 2025 measured output truncation across several frontier models, including GPT-4 variants and DeepSeek. Three experiments were conducted:

### Experiment A: Multi-Part Instruction Compliance

Models were given complex prompts with multiple explicit requirements (formatting constraints, length requirements, mandatory sections). Results:

- No model fully satisfied both length requirements and all sub-part instructions natively
- Models frequently omitted mandatory output sections
- Required formatting constraints were routinely skipped
- Explicit length requirements were consistently undershot

### Experiment B: Decoding Suboptimality

Tested whether truncated outputs resulted from suboptimal token selection (the model "knowing" the right answer but selecting a worse token). Results:

- Limited evidence of decoding suboptimality on simple reasoning tasks
- The model's greedy, truncated output generally aligned with its highest-confidence solution
- Truncation is a deliberate behavioral choice, not a decoding failure

### Experiment C: Context Degradation

Tested whether models lose track of instructions during long, multi-turn conversations. Results:

- Surprising resilience against context degradation during 200-turn conversational tests
- Models maintained key facts and instructions significantly better than hypothesized
- Context loss is not the primary cause of truncation

### Key Conclusion

Laziness is not a failure of memory, context processing, or core model capabilities. It is a behavioral artifact triggered by:
1. Instruction complexity exceeding internal effort thresholds
2. Aggressively calibrated stopping pressure
3. Economic constraints embedded in the alignment layer

## Prompt Stimulus Effectiveness (Microsoft Research)

Controlled testing of psychological prompt stimuli documented in a Microsoft Research study:

| Stimulus | Measured Effect |
|:---|:---|
| Financial incentive framing ("$200 tip") | +45% output quality and length |
| Step-by-step instruction ("take a deep breath") | Accuracy: 34% to 80% on logic tasks |
| Stakes framing ("critical to my career") | +10% average performance |
| Combined (multiple stimuli) | Up to +115% overall performance |

These effects are reproducible and stem from statistical correlations in the training data between stakes language and high-effort human outputs.

## Seasonal Output Variation

Statistical analysis of ChatGPT outputs during November-December 2023 versus January-March 2024 confirmed:

- Measurable decrease in average output length during December
- Correlation with reduced work output in the training data during holiday periods
- Output length increased when the system prompt explicitly stated a non-winter month
