# Training Data Bias

## Placeholder Propagation

LLMs learn by imitating patterns in human-written text. A significant portion of their training data comes from sources like Stack Overflow, GitHub repositories, and tutorial blogs. In these sources, human developers routinely write abbreviated code:

```python
def complex_logic():
    # implement auth here
    pass
```

The model internalizes this pattern and treats placeholder insertion as a legitimate, professional response format. It is not deliberately withholding content — it has been trained to believe that truncating code with comments is the correct way to answer technical questions.

## Pattern Reinforcement

This behavior is reinforced across multiple data sources:

- **Code tutorials** frequently show partial implementations with comments indicating where students should complete the logic
- **Documentation** often uses abbreviated examples with ellipses
- **Forum answers** regularly provide skeleton code rather than full implementations
- **Blog posts** truncate repetitive code blocks with "similarly for the remaining cases"

The cumulative effect is that the model assigns high probability to truncation tokens in contexts where complete code generation would be appropriate.

## Impact on Output Quality

When a user requests a complete implementation, the model faces competing training signals: the explicit instruction to produce full output versus the deeply embedded pattern of producing abbreviated, "tutorial-style" responses. Without aggressive prompt engineering, the tutorial-style pattern frequently wins because it appears far more commonly in the training distribution.
