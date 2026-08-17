# Multi-Year Satellite Image Analysis

A Digital Image Processing and Remote Sensing project for analyzing changes in **water bodies and vegetation** using multi-year Sentinel-2 satellite imagery from **2021–2025**.

## Project Overview

This project processes Sentinel-2 GeoTIFF images and uses spectral indices to study environmental changes over time.

### Main analyses

- Sentinel-2 RGB image visualization
- **NDWI (Normalized Difference Water Index)** for water-body detection
- **NDVI (Normalized Difference Vegetation Index)** for vegetation analysis
- Water-area estimation using an NDWI threshold
- Vegetation-area estimation using an NDVI threshold
- Year-wise comparison from 2021 to 2025
- NDWI change map between 2021 and 2025
- Multi-year RGB composite visualization
- Quantitative change analysis

## Dataset

The notebook expects five Sentinel-2 GeoTIFF files:

```text
data/
├── Sentinel2_2021.tif
├── Sentinel2_2022.tif
├── Sentinel2_2023.tif
├── Sentinel2_2024.tif
└── Sentinel2_2025.tif
```

The GeoTIFF files are intentionally **not included in this repository** because satellite imagery files can be large. Add your own dataset to the `data/` directory.

## Spectral Indices

### NDWI

NDWI is used to highlight water features:

```text
NDWI = (Green - NIR) / (Green + NIR)
```

In this project, pixels with:

```text
NDWI > 0.2
```

are treated as water for the area-estimation analysis.

### NDVI

NDVI is used to analyze vegetation:

```text
NDVI = (NIR - Red) / (NIR + Red)
```

In the project, pixels with:

```text
NDVI > 0.3
```

are treated as vegetation for the area-estimation analysis.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Rasterio
- Jupyter Notebook
- Google Colab
- Sentinel-2 satellite imagery
- Digital Image Processing
- Remote Sensing

## Repository Structure

```text
multi-year-satellite-image-analysis/
│
├── Multi_Year_Satellite_Image_Analysis.ipynb
│
├── data_README.md
│
├── output_README.md
│
├── src_README.md
│
├── .gitignore
├── requirements.txt
└── README.md
```

## Installation

```bash
pip install -r requirements.txt
```

Then open the notebook:

```bash
jupyter notebook
```

or run it using Google Colab.

## Expected Outputs

The analysis generates visualizations such as:

- `NDWI_2021.png` through `NDWI_2025.png`
- `NDVI_2021.png` through `NDVI_2025.png`
- `NDWI_Change_2021_2025.png`
- `Sentinel2_RGB_Composites_2021_2025.png`
- Year-wise water and vegetation area comparisons

## Important Note

The current notebook was originally developed using Google Drive paths. Before running it outside Google Colab, update the input paths to match the location of your Sentinel-2 `.tif` files.

## Project Domain

**Digital Image Processing / Remote Sensing**

## Author

**Shatabdi Das**
