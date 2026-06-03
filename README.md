# Detectability limits of tree-covered coffee at Sentinel resolution: asymmetric gains from optical texture

This repository contains the computational notebooks and supporting materials associated with the manuscript:

**Detectability limits of tree-covered coffee at Sentinel resolution: asymmetric gains from optical texture**

The study evaluates the detectability limits of tree-covered coffee in the Dominican Republic using multitemporal Sentinel-1 SAR metrics, Sentinel-2 optical attributes, and Sentinel-2 optical texture features. The workflow supports the comparison of Random Forest scenarios designed to assess separability between shaded coffee and forest formations at Sentinel spatial resolution.

> **Manuscript status:** under preparation / under review.  
> The repository will be updated with the final citation and DOI after publication.

---

## Repository structure

```text
detectability-limits-tree-covered-coffee-dominican-republic/
│
├── README.md
├── LICENSE
├── requirements.txt
├── CITATION.cff
├── .gitignore
│
├── notebooks/
│   ├── 01_sentinel1_sar_extraction_and_analysis.ipynb
│   ├── 02_sentinel2_optical_texture_extraction_and_analysis.ipynb
│   └── 03_model_comparison_and_detectability_analysis.ipynb
│
└── data/
    │   ├── Database_RD_Coffee_Forest.shp
    │   └── README.md
