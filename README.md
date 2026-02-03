# Enterprise-Scale Causal & Probabilistic Demand Forecasting System

## Project Overview

This project implements an enterprise-scale demand forecasting system that combines causal feature engineering with probabilistic forecasting and hierarchical reconciliation. The system is designed to handle large-scale retail demand forecasting with proper uncertainty quantification for inventory optimization.

## Key Features

- **Causal Feature Engineering**: Incorporates price changes, promotions, events, and calendar-driven seasonality
- **Probabilistic Forecasting**: Uses quantile-based models to estimate demand distributions rather than point predictions
- **Hierarchical Reconciliation**: Ensures forecast consistency across SKU, store, and state levels
- **Inventory Optimization**: Converts probabilistic forecasts into inventory decisions with service-level constraints
- **Drift Detection & Monitoring**: Monitors forecast performance and detects concept drift for timely retraining

## Dataset

The project uses the M5 Forecasting competition dataset (available on Kaggle):
- Sales data with hierarchical structure (item → department → category, store → state)
- Calendar data with events and holidays
- Price data for demand elasticity modeling

## Project Structure

```
├── data/
│   ├── raw/                    # Raw datasets (calendar, sales, prices)
│   └── processed/              # Feature-engineered data and hierarchy mappings
├── notebooks/
│   ├── 01_data_understanding_and_eda.ipynb
│   ├── 02_hierarchical_structure.ipynb
│   ├── 03_causal_feature_engineering.ipynb
│   ├── 04_probabilistic_forecasting.ipynb
│   ├── 05_hierarchical_reconciliation.ipynb
│   ├── 06_inventory_optimization.ipynb
│   └── 07_drift_detection_and_monitoring.ipynb
└── outputs/
    ├── forecasts/              # Probabilistic and reconciled forecasts
    ├── inventory/              # Inventory policy recommendations
    └── monitoring/             # Drift detection results
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Ahadke/Enterprise-Scale-Causal-Probabilistic-Demand-Forecasting-System.git
cd Enterprise-Scale-Causal-Probabilistic-Demand-Forecasting-System
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

The notebooks should be executed in sequential order:

1. **01_data_understanding_and_eda.ipynb**: Initial data exploration and understanding
2. **02_hierarchical_structure.ipynb**: Construct hierarchical demand structure
3. **03_causal_feature_engineering.ipynb**: Create causal features (price, promotions, events, seasonality)
4. **04_probabilistic_forecasting.ipynb**: Train quantile-based forecasting models
5. **05_hierarchical_reconciliation.ipynb**: Reconcile forecasts across hierarchy levels
6. **06_inventory_optimization.ipynb**: Convert forecasts to inventory decisions
7. **07_drift_detection_and_monitoring.ipynb**: Monitor performance and detect drift

## Technologies & Libraries

- **Python**: Core programming language
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computations
- **matplotlib**: Data visualization
- **scikit-learn**: Machine learning models
- **scipy**: Statistical functions

## Outputs

The system generates:
- Probabilistic forecasts with uncertainty quantiles
- Reconciled forecasts ensuring hierarchy consistency
- Inventory policy recommendations (safety stock, reorder points)
- Drift monitoring reports for model maintenance

## License

This project is open source and available for educational and research purposes.


