# Xu et al. — Glutamine metabolism tunes myeloid responses to drive resolution of inflammation during skin repair

[![DOI](https://img.shields.io/badge/DOI-10.1016/j.celrep.2026.117001-blue)](https://doi.org/10.1016/j.celrep.2026.117001)
[![PubMed](https://img.shields.io/badge/PubMed-41712383-green)](https://pubmed.ncbi.nlm.nih.gov/41712383/)
[![Cell Reports](https://img.shields.io/badge/Cell_Reports-45(3):117001-orange)](https://www.cell.com/cell-reports/fulltext/S2211-1247(26)00079-3)

## Overview

This repository contains analysis code for [Xu, Forni, Bhatt, Benvie et al. (2026) *Cell Reports*](https://doi.org/10.1016/j.celrep.2026.117001).

We show that glutamine metabolism in macrophages induces suppressive chromatin remodeling of neutrophil recruitment genes during resolution of skin wound inflammation, identifying a metabolic–epigenetic axis that drives tissue repair.

## Data availability

| Data type | Accession | Link |
|-----------|-----------|------|
| RNA-seq (new) | GSE289255 | [GEO](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE289255) |
| RNA-seq (new) | GSE289135 | [GEO](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE289135) |
| RNA-seq (new) | GSE289200 | [GEO](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE289200) |
| RNA-seq (new) | GSE289254 | [GEO](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE289254) |
| Metabolomics | PR002838 | [Metabolomics Workbench](https://doi.org/10.21228/M8TG2X) |
| RNA-seq (reanalyzed) | GSE223660 | [GEO](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE223660) |
| RNA-seq (reanalyzed) | GSE245703 | [GEO](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE245703) |

## Repository structure

```
├── scripts/
│   ├── 01_preprocessing/       # Read QC, alignment, and count matrix generation
│   ├── 02_differential_expression/ # DESeq2 / differential analysis
│   ├── 03_metabolomics/        # Metabolomic profiling and integration
│   ├── 04_chromatin/           # Chromatin remodeling / ATAC-seq analysis
│   └── 05_figures/             # Code to reproduce manuscript figures
├── envs/                       # Conda environment files
├── data/                       # Metadata and sample sheets (raw data on GEO)
└── README.md
```

> **Note:** Update the directory structure above to match your actual file organization.

## Reproducing the analysis

### Prerequisites

- R ≥ 4.x
- Python ≥ 3.9 (if applicable)
- Conda or mamba (recommended)

### Setup

```bash
# Clone this repository
git clone https://github.com/vhorsley/Xu-et-al-2025.git
cd Xu-et-al-2025

# Create the conda environment (if provided)
conda env create -f envs/environment.yml
conda activate xu-et-al-2025
```

### Running scripts

```bash
# Example: run differential expression analysis
Rscript scripts/02_differential_expression/run_deseq2.R
```

> **Note:** Update commands above to match your actual scripts and workflow.

## Key R/Bioconductor packages

<!-- Update versions to match your analysis -->

- [DESeq2](https://bioconductor.org/packages/DESeq2/) — Differential gene expression
- [clusterProfiler](https://bioconductor.org/packages/clusterProfiler/) — Pathway and GO enrichment
- [Seurat](https://satijalab.org/seurat/) — Single-cell analysis (if applicable)
- [ComplexHeatmap](https://bioconductor.org/packages/ComplexHeatmap/) — Heatmap visualization
- [ggplot2](https://ggplot2.tidyverse.org/) — Plotting

## Citation

If you use this code, please cite:

> Xu Y, Forni MF, Bhatt A, Benvie A, et al. Glutamine metabolism tunes myeloid responses to drive resolution of inflammation during skin repair. *Cell Reports*. 2026;45(3):117001. doi: [10.1016/j.celrep.2026.117001](https://doi.org/10.1016/j.celrep.2026.117001)

## Funding

- NIH/NIAMS AR076938
- NIH/NIAMS AR079232
- NIH/NIAMS AR084558

## License

<!-- Choose your license — MIT is common for academic code -->
This project is licensed under the [MIT License](LICENSE).

## Contact

[Horsley Laboratory](https://horsleylab.org/) — Yale University, Department of Molecular, Cellular and Developmental Biology
