Research on the misunderstanding between segmentation models and pre-modeling segmentation

## The Problem
A common mistake in banking ML: building separate models per segment (age group, region, product type) in hopes of achieving higher metrics. This inflates AUC artificially because:

- tmaller, more homogeneous samples are "easier" to model
- the model learns segment identity, not credit behavior
- OOT performance degrades because segments drift differently

## What This Repo Covers
- demonstrate AUC inflation via improper segmentation
- correct approach: segment as a feature, not a split criterion
- when segmentation IS valid: different data sources, regulatory requirement, fundamentally different populations
- pre-modeling segmentation criteria (eligibility rules, product type)
- statistical test for whether separate models are justified

## Tech Stack
Python · scikit-learn · XGBoost · pandas · matplotlib
