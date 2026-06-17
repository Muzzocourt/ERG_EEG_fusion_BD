# ERG_EEG_fusion_BD

This repository contains the code used to analyze EEG and ERG signals acquired during visual stimulation experiments and to identify potential biomarkers of Bipolar Disorder using machine learning and time-frequency analysis.

## Overview

The pipeline includes:

- Signal preprocessing
- Artifact rejection
- Feature extraction
- Wavelet decomposition (DWT)
- Feature selection
- Machine learning classification
- Nested cross-validation

  ## Requirements

Python 3.11

Main packages:

```bash
numpy
pandas
scipy
scikit-learn
pywavelets
matplotlib
joblib
```

## Installation

Clone the repository:

```bash
git clone https://github.com/username/project_name.git
cd project_name
```

Create a virtual environment:

```bash
conda create -n eegerg python=3.11
conda activate eegerg
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Project Structure

```text
project/
│
├── scripts/
│   ├── preprocessing.py
│   ├── feature_extraction.py
│   ├── select_features_nestedCV.py
│   └── classify_nestedCV.py
│
├── results/
│
├── figures/
│
└── README.md
```

## Data

The dataset is not publicly available due to ethical and privacy restrictions.

Data were acquired using the Retinaute® device (BioSerenity) during the BiMAR study.

## Usage

### Step 1 – Preprocessing

```bash
python preprocessing.py
```

### Step 2 – Feature extraction

```bash
python feature_extraction.py
```

### Step 3 – Feature selection

```bash
python select_features_nestedCV.py
```

### Step 4 – Classification

```bash
python classify_nestedCV.py
```

## Pipeline

1. Baseline correction
2. PCA-based outlier rejection
3. Epoch averaging
4. DWT decomposition (db4)
5. Statistical feature selection
6. Consensus feature selection across inner folds
7. Classification using:
   - Logistic Regression
   - LDA
   - k-NN
   - Random Forest
   - SVM Linear
   - SVM RBF
8. Nested cross-validation

## Citation

If you use this code, please cite:

Muzzolon J., Ren X., Le Cam S., Tursini K., Schwitzer T., Louis Dorr V.

*Towards Objective Bipolar Disorder Diagnostics: Identifying Biomarkers through EEG-ERG Fusion and Machine Learning.*

## Authors

Julie Muzzolon (Université de Lorraine, CRAN)
