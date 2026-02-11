# Deep Learning for Multiplex DNA Detection via LAMP

**Final Year Project | Imperial College London**

A deep learning framework that applies **Transformer-based architectures** to classify DNA sequences from Loop-Mediated Isothermal Amplification (LAMP) data -- enabling accurate multiplex detection from both amplification and melting curve signals.

---

## Highlights

- Designed and implemented a **custom Transformer encoder model** for time-series classification of fluorescence curves
- Benchmarked against 7 classical ML baselines (Random Forest, SVM, KNN, Logistic Regression variants, SGD, Gradient Boosting)
- Explored **two distinct signal modalities**: amplification curves (fluorescence vs. time) and melting curves (fluorescence vs. temperature)
- Built a complete ML pipeline: raw data preprocessing, feature extraction, visualization, model training, hyperparameter search, and evaluation
- Developed in Python using **PyTorch, scikit-learn, pandas, and NumPy**

---

## Background

Loop-Mediated Isothermal Amplification (LAMP) is a rapid, cost-effective technique for amplifying and detecting specific DNA sequences. While effective for single-target detection, **multiplex LAMP** -- testing multiple DNA primers in a single sample -- presents a significant classification challenge.

Building on the work of Malpartida-Cardenas et al., who proposed a machine learning approach for multiplex LAMP classification, this project investigates whether **deep learning Transformers** can improve classification accuracy over traditional ML methods. The self-attention mechanism in Transformers is particularly well-suited for capturing temporal dependencies in fluorescence signal data.

---

## Tech Stack

| Category | Tools |
|---|---|
| **Language** | Python |
| **Deep Learning** | PyTorch (Transformer Encoder, custom architectures) |
| **Machine Learning** | scikit-learn (Random Forest, SVM, KNN, Ridge, SGD, Gradient Boosting) |
| **Data Processing** | pandas, NumPy, SciPy |
| **Visualization** | Matplotlib, Seaborn |
| **Environment** | Google Colab (GPU-accelerated) |

---

## Project Structure

```
├── Data/
│   ├── LAMP_Data_Preprocess_Final.ipynb      # Data cleaning & preprocessing pipeline
│   ├── LAMP_Preprocess_Feature_Extract.ipynb  # Feature engineering & extraction
│   └── LAMP_Visualise_Preprocess.ipynb        # Exploratory data analysis & visualization
│
├── Amplification Curve/
│   ├── Amplification_Curve_Baseline.ipynb     # 7 baseline ML models + cross-validation
│   ├── Amplification_Curve_Transformer.ipynb  # Transformer model + hyperparameter search
│   └── AC_dmodel_128_nhead_4_layers_3_*.pt   # Best trained model weights
│
├── Melt_Curve/
│   ├── Melt_Curve_Baseline.ipynb              # 7 baseline ML models + cross-validation
│   ├── Melt_Curve_Transformer.ipynb           # Transformer model + hyperparameter search
│   └── MC_dmodel_128_nhead_8_layers_3_*.pt   # Best trained model weights
│
├── Final_Dissertation_Sungjun.pdf             # Full dissertation write-up
└── FYP_Presentation.pdf                       # Project presentation slides
```

---

## Methodology

### Data Pipeline
1. **Preprocessing** -- Normalization, noise filtering, and signal alignment of raw fluorescence data
2. **Feature Extraction** -- Derivation of curve-specific features (Ct values, peak characteristics, slope metrics)
3. **Group-based Splitting** -- Train/test split respecting sample groups to prevent data leakage

### Models
- **Baseline Models**: Random Forest, SVM (RBF & linear), KNN, L1/L2/Elastic Net Logistic Regression, SGD, Gradient Boosting -- evaluated with **group k-fold cross-validation**
- **Transformer Model**: Custom encoder-only Transformer with positional encoding, multi-head self-attention, and a classification head -- trained with systematic **hyperparameter grid search** over model dimension, attention heads, layer depth, learning rate, and batch size

---

## Dataset

The dataset used is a proprietary dataset from the Malpartida-Cardenas et al. research group. Access is restricted -- please contact me directly if you require it.

---

## Getting Started

The notebooks were developed in **Google Colab** with GPU acceleration. To run locally:

```bash
pip install torch scikit-learn pandas numpy scipy matplotlib seaborn
```

Adjust file paths in the notebooks from Google Drive paths to your local directory structure.

---

## Documentation

For a full discussion of methodology, experimental results, and analysis, see:
- [**Dissertation**](Final_Dissertation_Sungjun.pdf) -- Comprehensive write-up with literature review, methodology, results, and discussion
- [**Presentation**](FYP_Presentation.pdf) -- Summary slides covering key findings
