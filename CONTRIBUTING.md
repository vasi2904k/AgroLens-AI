# Contributing Guide

Thank you for contributing to the **AgroLens-AI** computer vision project. This guide ensures that our team maintains enterprise-grade code quality and a transparent development history required for elite industry standards.

## Getting Started

1. **Clone the Shared Repository:** Work directly in our shared workspace once you have collaborator access.
2. **Branching Strategy:** Never commit directly to `main` for major changes. Create a dedicated branch for your specific Week based task:
   - `feature/data-acquisition`
   - `feature/eda-visualization`
   - `feature/preprocessing-pipeline`
3. **Daily Cadence:** Aim for a minimum of **3 to 5 meaningful commits** per active development day.

## Development Workflow

- **Synchronize:** Keep your branch up to date with `main` to avoid merge conflicts.
- **Atomic Commits:** Break down complex data transformations or model layers into logical, isolated units of work.
- **Peer Review:** Open a pull request (PR) when your task is ready. At least one teammate must review and validate the code before it is merged into the main project line.
- **Notebook Hygiene:** Before committing `.ipynb` files, clear all output cells containing massive raw data to prevent repository bloat.

## Security & Data Integrity

- **Strict Exclusion:** Raw datasets (PlantVillage images) and trained model weights (`.h5`, `.pkl`) must **never** be pushed to the repository. Verify they are listed in the `.gitignore`.
- **Credential Safety:** Never hardcode API keys or database credentials; use environment variables.

## Commit Message Standards

We use structured, semantic prefixes to maintain a highly readable repository history.

**Format:**
```text
<prefix>: <short summary>

<optional detailed description of the analytical change>
```

**Mandatory Prefixes:**
- `data-clean:` For image resizing, normalization, and noise reduction tasks.
- `eda:` For exploratory notebooks, class distribution plots, and visualizations.
- `feature-eng:` For data augmentation (rotations, flips) and image dataset splitting.
- `model-tuning:` For CNN architecture adjustments and hyperparameter optimization.

**Examples:**
- `data-clean: standardize image dimensions to 224x224`

- `eda: generate class distribution plots for tomato leaf subsets`

- `feature-eng: implement horizontal flip augmentation for training set`
