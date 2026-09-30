# Bias-Variance Trade-off - Practical Assignment 1

Coursework repository for the CentraleSupelec machine-learning practical assignment on the bias-variance trade-off.

The repository contains the original assignment, a student Jupyter notebook, the supplied bibliography, and a self-contained bibliographic synthesis covering the mathematical and conceptual background required for the practical work.

## Repository contents

```text
.
├── TP_biais_variance_etudiant.ipynb
├── sujet_biais_variance.pdf
└── biblio/
    ├── Neural Networks and the BiasVariance Dilemma.pdf
    ├── The-Elements-of-Statistical-Learning-chapt7.pdf
    ├── reconciling modern machine-learning practice and the classical bias-variance-trade-off .pdf
    └── synthesisBiblio/
        ├── bias_variance_bibliographic_synthesis.tex
        └── bias_variance_bibliographic_synthesis.pdf
```

## Learning objectives

The assignment studies how prediction error depends on model flexibility, sample size, and noise. Its main topics are:

- the squared-error decomposition into squared bias, variance, and irreducible noise;
- empirical estimation of bias and variance by repeated simulation;
- polynomial regression and nearest-neighbor regression;
- cross-validation and model-selection instability;
- nonuniform input distributions and heteroscedastic noise;
- regularization and effective model complexity;
- the relation between the classical trade-off and double descent.

## Getting started

Create and activate a Python environment, then install the notebook dependencies:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install jupyter numpy matplotlib scikit-learn
```

On Windows PowerShell, activate the environment with:

```powershell
.venv\Scripts\Activate.ps1
```

Start Jupyter from the repository root:

```bash
jupyter notebook TP_biais_variance_etudiant.ipynb
```

Before running the exercises, verify the assigned values of `A`, `B`, `SIGMA`, and `SEED` in the notebook. Execute the notebook from top to bottom because the simulated results depend on the order in which the random-number generator is used.

## Bibliographic synthesis

The English synthesis in `biblio/synthesisBiblio/` is designed as a study document rather than as the one-page submission requested by the assignment. It includes:

- a complete derivation of the squared-error bias-variance identity;
- an explicit account of the relevant sources of randomness;
- Monte Carlo estimators used in the notebook;
- the distinction between regression loss and zero-one classification loss;
- regularization, cross-validation, heteroscedasticity, ensembles, and predictive uncertainty;
- double descent and the interpolation regime;
- a direct mapping from the theory to each notebook exercise.

To rebuild the PDF:

```bash
cd biblio/synthesisBiblio
latexmk -pdf -interaction=nonstopmode -halt-on-error bias_variance_bibliographic_synthesis.tex
```

Remove LaTeX auxiliary files while preserving the source and PDF with:

```bash
latexmk -c bias_variance_bibliographic_synthesis.tex
```

## Suggested workflow

1. Read the assignment and the direct-answer section of the synthesis.
2. Enter the parameters assigned to the group in the notebook.
3. Complete one exercise at a time and write the interpretation immediately after producing each figure.
4. Restart the kernel and run all cells before reporting numerical results.
5. Record figure or cell identifiers for every value cited in the final reflective note.
6. Document any use of AI assistance and independently verify generated explanations or code.

## Academic-use note

The notebook is intentionally incomplete and contains `TODO` cells. Results should be produced from the parameters assigned to the group and interpretations should be written in the students' own words. The bibliographic synthesis is a study aid, not a replacement for the required one-page source synthesis or the final reflective note.

