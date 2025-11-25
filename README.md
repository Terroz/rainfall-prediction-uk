# Rainfall Prediction Using Temperature Features

Predicts monthly rainfall in Wales from min/max temperatures (Aberporth, Cardiff, Valley).  
Models: **Linear Regression**, **Random Forest**, **SVR (RBF)** with light tuning.

## Key Findings
- **SVR best** on pooled data (R² ≈ 0.84).
- **Poor cross-station generalisation** (low/negative R²) → strong microclimate effects.
- Linear Regression weakest; Random Forest moderate.
- **Under-predicts extremes** → more features (humidity/pressure/wind) needed.

## Repository Structure
    data/        # aberporth.npy, cardiff.npy, valley.npy
    notebook/    # Rainfall.ipynb (full pipeline)
    poster/      # rainfall_poster.pdf
    README.md
    requirements.txt

## How to Run
    pip install -r requirements.txt
    jupyter notebook notebook/Rainfall.ipynb

## Requirements
    numpy
    pandas
    matplotlib
    scikit-learn

## Notes
Poster summarises methods (cross-station, within-station, pooled), metrics (R², MSE), and outcomes.
