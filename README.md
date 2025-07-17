# 3D Printer Strength Classification with Logistic Regression

This project classifies 3D printed parts as either "strong" or "weak" based on tensile strength and various printing parameters. It uses both linear and logistic regression to explore model interpretability and performance.

## Dataset
- 50 samples of 3D printed parts
- Source: [Kaggle - 3D Printer Data](https://www.kaggle.com/datasets/afumetto/3dprinter/data)
- Variables include geometry, material, thermal settings, and speed

## Objective
Predict whether a part will be strong (above mean strength) or weak (below mean strength) using:
- Linear Regression
- Logistic Regression

## Features Used
- Layer height, wall thickness, infill density
- Infill pattern (grid vs. honeycomb)
- Nozzle temperature, bed temperature
- Print speed, fan speed
- Material (ABS vs. PLA)

## Methods
- One-hot encoding for categorical data
- Min-max normalization
- Train-test split (85/15)
- Sequential feature selection for model optimization

## Results
### Linear Regression:
- Accuracy: 75%
- F1 Score: 80%

### Logistic Regression:
- Accuracy: 87.5%
- F1 Score: 89%

Logistic regression outperformed linear in every metric and is more suitable for classification tasks, especially with proper normalization.

## Insights
- PLA, height, density, and speed were repeatedly selected as important features.
- Some results were surprising (e.g., speed and density), which reflects the complexity of 3D printed part strength beyond intuition.
    - Density's effect may reflect the strength definition used.
- Both models produced interpretable outputs and informed insights for future experimentation.

## How to Run
Install dependencies:
```bash
pip install -r requirements.txt
```

Place `3DPrinter.csv` in the same directory as the notebook, and run:

Then open:
```bash
jupyter notebook
```

## Files
- `3DPrinterStrength.ipynb` - Main notebook
- `requirements.txt` - Python dependencies
- `README.md` - Project summary
- `3DPrinter.csv` - Data file
- `LICENSE`

## License
MIT License
