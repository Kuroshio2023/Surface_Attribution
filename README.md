# Latent Surface Attribution

## Overview
Latent Surface Attribution (LSA) is a feature attribution method that replaces traditional 1D path–based integration with a localized 2D surface constructed in the latent space of a generative model. Inspired by surface-based action principles from string theory, LSA integrates model sensitivity over a fixed-area surface surrounding the latent representation of the input. This produces stable, baseline-free, and geometry-aware attributions.

## Method Summary
LSA builds a smooth latent surface centered at the latent code of the input and selects its principal directions using local PCA. The decoder induces a geometric structure on this surface, allowing attribution to be computed by integrating the gradient magnitude over the surface area. This approach captures the model’s local behavior in a neighborhood rather than along a single path, reducing noise and avoiding baseline selection.

## Key Advantages
- Baseline-free and locally defined  
- Captures multidimensional latent variations  
- More stable than pointwise or path-based methods  
- Grounded in geometric principles  
- Compatible with any model equipped with an encoder–decoder structure

## Evaluation
LSA was evaluated using:
- **AUC–ROC:** assesses how quickly the model prediction drops when highly attributed regions are perturbed  
- **SIC (Sufficiency-Informed Completeness):** measures how well the most salient regions preserve the model’s prediction  

LSA outperforms Manifold Integrated Gradients (MIG) on both metrics.

## Future Work
- Learning optimal surfaces for maximal attribution  
- Using attribution surfaces as training regularizers  
- Extending the framework to NLP and recommender systems  
- Studying higher-dimensional latent manifolds



---
