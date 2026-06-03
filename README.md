# Detectability limits of tree-covered coffee at Sentinel resolution: asymmetric gains from optical texture

This repository contains the computational notebooks and supporting materials associated with the manuscript:

**Detectability limits of tree-covered coffee at Sentinel resolution: asymmetric gains from optical texture**

The study evaluates the detectability limits of tree-covered coffee in the Dominican Republic using multitemporal Sentinel-1 SAR metrics, Sentinel-2 optical attributes, and Sentinel-2 optical texture features. The workflow supports the comparison of Random Forest scenarios designed to assess separability between shaded coffee and forest formations at Sentinel spatial resolution.

> **Manuscript status:** under review.  
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
├── notebooks/
│   ├── Database_DR_Coffee_Forest.shp
│   └── README.md
```

---

## Notebooks

### `01_sentinel1_sar_extraction_and_analysis.ipynb`

This notebook contains the Sentinel-1 SAR workflow used to derive and analyse C-band radar metrics for tree-covered coffee and forest samples.

The workflow includes:

- Sentinel-1 image collection filtering;
- extraction of VV and VH backscatter metrics;
- derivation of SAR-based predictors;
- sample-level feature extraction;
- SAR-only model evaluation;
- interpretation of Sentinel-1 contribution to class separability.

---

### `02_sentinel2_optical_texture_extraction_and_analysis.ipynb`

This notebook contains the Sentinel-2 optical workflow used to derive multispectral, vegetation-index and optical-texture predictors.

The workflow includes:

- Sentinel-2 surface reflectance filtering;
- extraction of multispectral bands;
- calculation of vegetation indices;
- derivation of Sentinel-2 optical texture features;
- sample-level feature extraction;
- optical and texture-based analysis.

---

### `03_model_comparison_and_detectability_analysis.ipynb`

This notebook integrates the derived predictors and compares the modelling scenarios reported in the manuscript.

The workflow includes:

- SAR scenario;
- Optical scenario;
- Optical-SAR Fusion scenario;
- Fusion enhanced with Sentinel-2 optical texture;
- Random Forest model evaluation;
- stratified cross-validation;
- out-of-fold prediction analysis;
- feature-importance assessment;
- directional error analysis between coffee and forest;
- interpretation of detectability limits at Sentinel resolution.

---

## Data availability

The `data/` folder contains supporting input and/or derived datasets used to demonstrate or reproduce the computational workflow.

Users should carefully check the information provided in `data/README.md` before reusing any dataset.

If geospatial reference data are included, they should be used only for research transparency and reproducibility purposes. They should not be used to identify individual landowners, farms, private properties or sensitive production areas.

The workflow uses publicly available Earth observation datasets, including:

- Sentinel-1 Ground Range Detected imagery;
- Sentinel-2 surface reflectance imagery;
- Copernicus DEM GLO-30, when applicable.

---

## Computational environment

The analyses were developed primarily in Python and Google Colab.

The main Python packages used in the workflow include:

- `earthengine-api`
- `geemap`
- `numpy`
- `pandas`
- `geopandas`
- `scikit-learn`
- `scikit-image`
- `matplotlib`
- `seaborn`
- `rasterio`
- `shapely`

Package requirements are listed in:

```text
requirements.txt
```

To install the required packages in a local Python environment, use:

```bash
pip install -r requirements.txt
```

---

## How to use this repository

1. Clone or download this repository.

```bash
git clone https://github.com/fernandocoelh0/detectability-limits-tree-covered-coffee-dominican-republic.git
```

2. Open the notebooks in Google Colab or Jupyter Notebook.

3. Check the expected input data structure described in `data/README.md`.

4. Run the notebooks in numerical order:

```text
01_sentinel1_sar_extraction_and_analysis.ipynb
02_sentinel2_optical_texture_extraction_and_analysis.ipynb
03_model_comparison_and_detectability_analysis.ipynb
```

5. Review and adjust local paths or Google Drive paths according to your computational environment.

---

## Reproducibility notes

The notebooks were organised to document the main analytical workflow used in the manuscript. Some steps may require user-specific configuration, including:

- Google Earth Engine authentication;
- access to local or cloud-stored reference polygons;
- adjustment of input and output directories;
- verification of dataset availability and permissions.

The original modelling logic and analytical structure are preserved, while paths and sensitive configuration details were generalised for public repository use.

---

## Citation

If you use this repository, please cite the associated manuscript and this repository.

The manuscript is currently under preparation / under review. The final article citation and DOI will be added after publication.

For now, please cite the repository as:

```text
Eugenio, F. C. (2026). Detectability limits of tree-covered coffee at Sentinel resolution: asymmetric gains from optical texture. GitHub repository. https://github.com/fernandocoelh0/detectability-limits-tree-covered-coffee-dominican-republic
```

---

## Licence

This repository is distributed under the MIT Licence, unless otherwise stated.

Please note that the licence applies to the code. Data reuse conditions should be checked separately in the `data/README.md` file.

---

## AI assistance statement

Large language models were used to assist with code organisation, documentation, and manuscript-support material preparation. All scientific decisions, methodological definitions, data interpretation and final repository content were reviewed and approved by the author.
