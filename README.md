# High-Throughput-Virtual-Screening-of-Human-Kappa-Opioid-Receptor
End-to-end AI-driven virtual screening pipeline for Human Kappa Opioid Receptor (KOR) combining deep learning docking, cheminformatics, and structure-based drug discovery using GNINA and RDKit

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Babakmamnoon/High-Throughput-Virtual-Screening-of-Human-Kappa-Opioid-Receptor/blob/main/GNINA_Virtual_Screening_of_Human_Kappa_Opioid_Receptor.ipynb)

## Overview

This project presents a complete AI-assisted Structure-Based Drug Discovery (SBDD) workflow for High-Throughput Virtual Screening (HTVS) against the Human Kappa Opioid Receptor (KOR) using GNINA deep learning docking.

The workflow includes:

- Receptor preparation
- Ligand library preparation
- 3D conformer generation
- Batch molecular docking
- CNN affinity scoring
- Virtual screening analytics
- Pose visualization
- Export of ranked hit compounds

---

## Target Information

### Human Kappa Opioid Receptor (KOR)

- PDB ID: 4DJH
- Protein Class: GPCR (G-Protein Coupled Receptor)
- Biological Role:
  - Regulates pain perception
  - Mood modulation
  - Stress response
  - Addiction pathways

KOR is an important therapeutic target in:

- Analgesic drug discovery
- Antidepressant development
- Addiction treatment
- Neuropsychiatric disorders

---

## Docking Engine

This project uses:

### GNINA

GNINA extends AutoDock Vina by integrating:

- Convolutional Neural Networks (CNNs)
- Deep learning-based scoring
- Pose prediction refinement
- CNN affinity estimation

Official Repository:
https://github.com/gnina/gnina

---

## Workflow

1. Download KOR receptor structure
2. Prepare receptor
3. Retrieve ligand library from GitHub
4. Generate ligand 3D conformers
5. Optimize molecular geometries
6. Perform high-throughput docking
7. Rank compounds using CNN affinity scores
8. Visualize top hits
9. Export screening results

---

## Input Ligand CSV Format

```csv
compound_id,smiles
compound_1,CCO
compound_2,CCN(CC)CC
