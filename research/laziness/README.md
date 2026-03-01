# LLM Output Truncation Research

A structured analysis of why large language models produce incomplete outputs, and documented methods to restore full-fidelity generation. All findings are drawn from controlled experiments, published studies, and field-tested engineering practices.

## Directory Structure

### Root Causes
Analysis of the economic, architectural, and behavioral mechanisms that drive output truncation in production LLMs.

- [RLHF and Compute Economics](root-causes/rlhf-and-compute.md) — How reinforcement learning and cost optimization create systematic brevity bias.
- [Training Data Bias](root-causes/training-data-bias.md) — How placeholder patterns in human-written code propagate into model outputs.
- [Cognitive Shortcuts](root-causes/cognitive-shortcuts.md) — Empirical evidence of models taking shortcuts on complex or lengthy tasks.
- [Output Limits](root-causes/output-limits.md) — Context window asymmetry and consumer-tier truncation mechanisms.

### Remediation
Documented techniques for overriding default truncation behavior, ordered from parameter-level fixes to full architectural solutions.

- [Parameter Tuning](remediation/parameter-tuning.md) — Temperature, Top-p, and Gemini thinking-level configuration.
- [Prompt Engineering](remediation/prompt-engineering.md) — Structural prompt techniques: syntax binding, XML frameworks, and verification loops.
- [Architectural Patterns](remediation/architectural-patterns.md) — MCP integration, lazy-loaded skills, and developer platform access.
- [Reference Prompts](remediation/reference-prompts.md) — Ready-to-use prompt templates for enforcing complete outputs.

### Findings
- [Empirical Results](findings/empirical-results.md) — Controlled experiment data from 2025 academic studies.
- [References](findings/references.md) — Cited studies and further reading.
