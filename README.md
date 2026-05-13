# High-Throughput-Virtual-Screening-of-Kappa-Opioid-Receptor-Inhibitors
End-to-end AI-driven virtual screening pipeline for Human Kappa Opioid Receptor (KOR) combining deep learning docking, cheminformatics, and structure-based drug discovery using GNINA and RDKit

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Babakmamnoon/High-Throughput-Virtual-Screening-of-Human-Kappa-Opioid-Receptor/blob/main/GNINA_Virtual_Screening_of_Human_Kappa_Opioid_Receptor_Inhibitors.ipynb)

## Overview

This project presents a complete AI-assisted Structure-Based Drug Discovery (SBDD) workflow for High-Throughput Virtual Screening (HTVS) against the Human Kappa Opioid Receptor (KOR) using GNINA deep learning docking.

The pipeline automates:

Receptor preparation (cleaning, chain isolation, and protonation).

Ligand library standardization (3D conformation generation and MMFF optimization).

Molecular docking using the GNINA engine.

Pose rescoring via Convolutional Neural Networks (CNN).

Scientific Workflow
1. Receptor Preparation
The target is the Human Kappa Opioid Receptor (PDB ID: 4DJH). The pipeline isolates Chain A, removes crystallographic additives (water, salts, etc.), and retains the co-crystallized ligand JDC to define the active site search space. OpenBabel is utilized to add hydrogens and prepare the receptor in a format compatible with GNINA.

2. Ligand Library Standardization
The ligand library is fetched directly from GitHub in CSV format. The pipeline performs the following:

Data Cleaning: Removes duplicates and handles missing SMILES.

3D Embedding: Uses RDKit's ETKDGv3 algorithm for realistic 3D conformation generation.

Energy Minimization: Refines structures using the MMFF94 force field.

3. Molecular Docking & CNN Rescoring
Docking is performed using GNINA, a fork of Smina and AutoDock Vina that utilizes deep learning.

Autoboxing: The search box is automatically centered on the reference ligand (JDC) with a 6Å buffer.

CNN Rescoring: Beyond traditional Vina affinity, poses are evaluated using a CNN model to predict binding probability and affinity based on protein-ligand spatial features.

Results & Visualization
The output includes a comprehensive CSV file (KOR_HTVS_Results.csv) containing:

Vina_Affinity: Traditional physics-based scoring.

CNN_Affinity: Deep learning-based affinity prediction.

The top-scoring hits are visualized directly within the notebook using py3Dmol.

Note: To see the interactive 3D visualizations, run the notebook using the "Open in Colab" button above.

Tools & Technologies
Python 3.x

GNINA: Deep learning molecular docking engine.

RDKit: Cheminformatics and 3D molecule manipulation.

OpenBabel: Chemical file format interconversion.

py3Dmol: Web-based 3D molecular visualization.

Author: **Babak Mamnoon**
Project Type: Computational Drug Discovery / Cheminformatics
