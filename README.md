# CIS2004 Drug Discovery Notebook

This repository contains a Jupyter notebook for exploratory data analysis (EDA) on a virtual screening dataset used in drug discovery.

## What this repository does

- Loads and explores `drug_discovery_virtual_screening.csv`
- Inspects dataset structure (`head`, shape, column names, data types)
- Checks missing values
- Performs protein-level aggregation
- Generates protein-level pattern plots (for example: top proteins by sample count and mean binding affinity)

## Repository structure

- `CIS2004_Dataset_Explore_Dhruv_Satasiya.ipynb` — main analysis notebook
- `drug_discovery_virtual_screening.csv` — source dataset
- `README.md` — project documentation

## Dataset summary

The CSV represents compound–protein screening records. Each row corresponds to one compound tested against one protein target.

Key fields include:

- **Identifiers**: `compound_id`, `protein_id`
- **Compound descriptors**: `molecular_weight`, `logp`, `h_bond_donors`, `h_bond_acceptors`, `rotatable_bonds`, `polar_surface_area`, `compound_clogp`
- **Protein descriptors**: `protein_length`, `protein_pi`, `hydrophobicity`, `binding_site_size`
- **Engineered interaction features**: `mw_ratio`, `logp_pi_interaction`
- **Outcomes**: `binding_affinity` (continuous) and `active` (binary label)

## Requirements

- Python 3.9+
- Jupyter support (VS Code Notebook extension or Jupyter Lab)
- Python packages:
  - `pandas`
  - `matplotlib`

## How to run

### Option A: Run in VS Code (recommended)

1. Open the folder in VS Code.
2. Open `CIS2004_Dataset_Explore_Dhruv_Satasiya.ipynb`.
3. Select a Python kernel when prompted.
4. Run cells from top to bottom.

### Option B: Run with Jupyter Lab

1. Create and activate a virtual environment:

	```bash
	python3 -m venv .venv
	source .venv/bin/activate
	```

2. Install dependencies:

	```bash
	pip install pandas matplotlib notebook
	```

3. Start Jupyter:

	```bash
	jupyter notebook
	```

4. Open `CIS2004_Dataset_Explore_Dhruv_Satasiya.ipynb` and run all cells.

## Typical outputs

- Data overview tables
- Missing value summary
- Protein-level bar charts:
  - top proteins by record count
  - mean binding affinity for top proteins

## Notes

- The dataset contains some missing values in selected numeric columns.
- All file paths in the notebook are relative, so run from the repository root.