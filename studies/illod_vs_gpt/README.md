# Abbreviation-Expansion Pair Detection Study

This directory compares ILLOD with ChatGPT-4 in detecting Abbreviation-Expansion Pairs (AEPs) in requirements documents.

## Background

AEPs play a crucial role in requirements engineering, particularly in glossary term extraction and consolidation. Their detection and understanding ensures requirement clarity and quality [1].

## Tool Description

ILLOD detects AEPs in requirement sets by analyzing:
- Initial Letters
- Term Lengths
- Order
- Distribution of characters

## Experiment Setup

### Dataset
- Source: PROMISE dataset [3] covering 15 projects
- Modification: 30 undefined abbreviations inserted
- Insertion criteria:
  - Terms appearing in ≥2 requirements
  - Maximum one abbreviation per term
  - Various abbreviation styles (not limited to acronyms)

### Experiments

#### ILLOD Results
As detailed in [2]:
- Detected 29/30 inserted abbreviations
- Correctly identified expansions for 25/29 detected abbreviations

#### ChatGPT-4 Approach
- Task 1: Find all abbreviations in modified dataset
- Task 2: Generate expansion candidates for found abbreviations
- Constraint: Only suggest expansions present in requirements

The constraint is crucial as LLMs tend to suggest plausible but technically incorrect expansions. For example, in the requirement:

"Clean and prepare audio recordings using SS and VAD to ensure clear, high-quality speech samples..."

An LLM might expand SS to "speech separation" when "source separation" is the correct technical term. By limiting expansions to terms present in requirements, we avoid such domain-specific errors.

## Directory Structure
```
data/
├── modified/       # Requirements with inserted abbreviations
└── gpt_results/    # ChatGPT-4 detection outputs
```

## References

[1] Hasso, Hussein, et al. "Abbreviation-expansion pair detection for glossary term extraction." International Working Conference on Requirements Engineering: Foundation for Software Quality. Cham: Springer International Publishing, 2022.

[2] Hasso, Hussein, et al. "ILLOD Replication Package: An Open-Source Framework for Abbreviation-Expansion Pair Detection and Term Consolidation in Requirements." 2023 IEEE 31st International Requirements Engineering Conference (RE). IEEE, 2023.

[3] Sayyad Shirabad, J., Menzies, T.: PROMISE software engineering repository. School of Information Technology and Engineering, University of Ottawa, Canada (2005), http://promise.site.uottawa.ca/SERepository/
