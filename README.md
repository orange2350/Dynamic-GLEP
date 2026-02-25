# Dynamic-GLEP: a dynamics-informed deep learning framework for ligand efficacy prediction in representative Class A GPCRs.

✅ Published in *Briefings in Bioinformatics*, 2026 

😁 DOI: https://doi.org/10.1093/bib/bbag049

This repository is the offical implementation of Dynamic-GLEP
![图片1](https://github.com/user-attachments/assets/befaf67d-7a0d-43c8-a304-94ba4c7c7d18)

# Overview
G protein-coupled receptors (GPCRs) represent the largest membrane protein family and remain central targets in drug discovery. Ligand efficacy—defined by the ability to modulate receptor conformational states—extends beyond binding affinity and underpins functional selectivity. However, most computational approaches still emphasize affinity prediction, with limited capacity to capture the conformational dynamics driving efficacy. Here, we introduce Dynamic-GLEP, a structure- and mechanism-aware framework that integrates molecular dynamics (MD)-derived conformational ensembles with transfer learning on equivariant graph neural networks. By constructing multi-conformation receptor–ligand complexes and fine-tuning the EquiScore model, Dynamic-GLEP identifies conformation-dependent interaction features to distinguish agonists from non-agonists. Applied to the 5-HT1A receptor, the framework achieved an AUC of 0.74 in cross-validation and 0.71 on an external FDA-related dataset. Comparative analyses showed that Holo-based models are advantageous for scaffold optimization, whereas Apo-derived ensembles provided greater adaptability to chemically diverse ligands. Furthermore, extension to the adenosine A2A receptor yielded high performance (AUC > 0.85), underscoring the method’s robustness and transferability under data-scarce conditions. Collectively, these results highlight Dynamic-GLEP as a reliable and interpretable platform for ligand efficacy prediction in class A GPCRs, with broad potential to support virtual screening, candidate prioritization, and mechanism-driven drug design.

# Installation
This code requires the installation of the following packages:

1.python == 3.7.0

2.numpy

3.pandas

4.scipy

5.scikit-learn

6.pytorch

7.tqdm

8.tap (pip install typed-argument-parser)

9.rdkit

Building of EquiScore+TL models are based on EquiScore (https://github.com/CAODH/EquiScore).

All packages can be installed using conda. Neural networks can be trained with CPU or GPU.

# Process implementation

## 1.Get snapshots with molecular dynamics techniques
Gromacs(https://www.gromacs.org/)

## 2.Get complexes by Ensemble Docking
Glide (Schrodinger)

## 3.Get model with Transfer learning
EquiScore(https://github.com/CAODH/EquiScore)

