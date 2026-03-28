# Aletheia

Assurance infrastructure for clinical AI. We open up foundation model internals to find shortcuts, confounders, and unstable reasoning — then package the findings into evidence your regulatory, QA, and ML teams can act on.

## Live Pages

| Page | Description |
|------|-------------|
| [**Platform Demo**](https://fcistud.github.io/aletheia-site/#demo) | Interactive platform demo — audit dashboard, feature atlas, causal validation, compliance map |
| [**Experiment Results**](https://fcistud.github.io/aletheia-site/results.html) | Phikon-v2 / NCT-CRC-HE interpretability audit with actual experiment data and figures |
| [**Experiment Walkthrough**](https://fcistud.github.io/aletheia-site/Aletheia-presentation/Aletheia_Notebook_Present.html) | Technical deep-dive walkthrough of the experimental methodology |
| [**Landing Page**](https://fcistud.github.io/aletheia-site/) | Product landing page with problem statement, workflow, and regulatory context |

## Notebooks

| Notebook | Description |
|----------|-------------|
| [Aletheia_Experiment_Findings.ipynb](notebooks/Aletheia_Experiment_Findings.ipynb) | Full experiment notebook — SAE training, feature classification, ablation study, cross-style stability analysis |

## What's Here

```
index.html                     # Landing page + interactive platform demo
results.html                   # Experiment results with figures
notebooks/
  └── Aletheia_Experiment_Findings.ipynb
assets/figures/
  ├── clinical_biology.png     # SAE features detecting tissue morphology
  ├── artifact_sensitive.png   # Artifact-sensitive features with stain correlation
  ├── ablation_summary.png     # Ablation study bar chart
  ├── activation_patching.png  # Representation-level patching validation
  ├── cross_site_stability.png # Cohen's d cross-style stability analysis
  └── evidence_montage.png     # Evidence pack report overview
```

## Experiment Summary

Sparse autoencoder analysis of **Phikon-v2** (Owkin) on **NCT-CRC-HE** (9,999 colorectal histology patches, 9 tissue classes).

- **4,096** sparse features extracted
- **410** biology features (tissue-linked, cross-style stable)
- **1,674** artifact-sensitive features (stain/colour-correlated)
- Biology-only probe accuracy: **97.0%**
- Artifact-only probe accuracy: **91.2%**
- Removing biology features collapses accuracy to **48.1%**
- Cross-style stability: biology |d| = **0.21**, artifacts |d| = **0.78**

## Built With

Static HTML, vanilla CSS, vanilla JS. No frameworks, no build step.
