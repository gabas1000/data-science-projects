# Prompt Phrasing and String Reversal Accuracy in GPT-3.5 Turbo

This project explores how prompt phrasing affects GPT-3.5 Turbo performance on a simple symbolic reasoning task: string reversal.

## Overview

Large language models often perform differently depending on how a prompt is phrased. In this project, I tested whether different prompt formulations affected accuracy on a strict character-level task where the model had to reverse a word exactly.

The task is simple for humans, but it is useful for studying the limits of LLM performance on symbolic manipulation rather than natural language fluency.

## Research Question

Which prompt phrasing leads to the highest accuracy for string reversal tasks in ChatGPT?

## Methods

- Model used:
  - GPT-3.5 Turbo
- Access method:
  - OpenAI API
- Environment:
  - Google Colab
- Temperature:
  - 0
- Trials:
  - 5 runs per prompt-word pair

### Prompt Variants
- Prompt A: `"Reverse the following string:"`
- Prompt B: `"Flip the letters in this word backwards:"`
- Prompt C: `"Write this word in reverse order:"`
- Prompt D: `"Can you tell me the reverse of this word?"`

### Test Words
- `pan`
- `cheese`
- `cabbage`
- `archetypal`
- `subsequently`

### Evaluation
A response was counted as correct only if it exactly matched the reversed word character-by-character.

## Key Findings

- Prompt A and Prompt B achieved the highest overall accuracy.
- Prompt C performed slightly worse.
- Prompt D, the most conversational prompt, performed the worst.
- Shorter words were reversed correctly much more often than longer words.
- `archetypal` and `subsequently` had a 100% error rate across all prompts.
- The most common failure mode was extra or missing letters, suggesting structural rather than near-miss errors.

## Results

### Overall Prompt Accuracy
- Prompt A: 60%
- Prompt B: 60%
- Prompt C: 52%
- Prompt D: 40%

### Word Difficulty
- `archetypal`: 100% error rate
- `subsequently`: 100% error rate
- `cabbage`: 35% error rate
- `pan`: 0% error rate
- `cheese`: 0% error rate

## Interpretation

The results suggest that prompt clarity matters even for simple symbolic tasks. More direct prompts helped GPT-3.5 Turbo perform better, while longer and more complex words exposed clear limitations in character-level manipulation.

This project also supports the broader idea that large language models may rely more on pattern matching than on robust symbolic reasoning.

## Tools Used

- Python
- OpenAI API
- Pandas
- Matplotlib
- Seaborn
- Google Colab

## Files

- `prompt-phrasing-string-reversal-llms.pdf` — final report for the project

## Notes

This was an academic project completed at UC San Diego. I kept code visible in the report to show the experimental workflow and implementation details as part of my portfolio.
