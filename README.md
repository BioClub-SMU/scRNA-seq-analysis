# 🧬 scRNA-seq Analysis Tutorial

A lightweight and step-by-step **single-cell RNA-seq analysis tutorial** covering three popular analysis ecosystems:  
- **[Seurat](https://satijalab.org/seurat/)** (R)  
- **[Scanpy](https://scanpy.readthedocs.io/en/stable/)** (Python)  
- **[SingleCellExperiment (SCE)](https://bioconductor.org/packages/SingleCellExperiment/)** (R/Bioconductor)  

This repository is designed for **learners and researchers** who want to quickly get started with scRNA-seq analysis, understand the differences between ecosystems, and reproduce results with example datasets.

---


## 📊 Analysis Workflow

Each ecosystem follows a **comparable analysis pipeline** for easy cross-platform learning:

1. **Data Input & QC**
   - Load raw expression matrix (10X Genomics format, h5, h5ad, etc.)
   - Filter cells/genes based on QC metrics (mitochondrial %, nGenes, nUMIs)

2. **Normalization & Feature Selection**
   - Normalize counts (e.g., `LogNormalize` in Seurat, `pp.normalize_total` in Scanpy)
   - Identify highly variable genes (HVGs)

3. **Dimensionality Reduction**
   - PCA on HVGs
   - Optional: Harmony, FastMNN batch correction

4. **Clustering**
   - Graph-based clustering (Louvain/Leiden)

5. **Visualization**
   - UMAP / t-SNE embedding

6. **Marker Gene Identification**
   - Differential expression analysis between clusters

7. **Annotation**
   - Assign biological cell types using marker genes

---

## 🚀 Quick Start

### **1. Clone the repository**
```bash
git clone https://github.com/BioClub-SMU/scRNA-seq-analysis.git
cd scRNA-seq-analysis
```

### **2. Install dependencies**
```bash
## R
install.packages("Seurat")
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install(c("SingleCellExperiment", "scater", "scran"))
```

```bash
## Python
conda create -n scanpy_env python=3.10
conda activate scanpy_env
pip install scanpy anndata
```

## 📬 Contact

If you have questions, suggestions, or would like to contribute to this tutorial, feel free to reach out:

- **Author**: Hinna He  
- **Email**: [nanh302311@gmail.com](mailto:nanh302311@gmail.com)  
- **GitHub Issues**: [Open an issue](https://github.com/BioClub-SMU/scRNA-seq-analysis/issues)  

We welcome pull requests, bug reports, and feature suggestions!
