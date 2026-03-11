# Football Match Prediction using Machine Learning

A comprehensive machine learning project for predicting football match outcomes across 10 European leagues using explainable AI techniques.

## Author
Vishal Chaudhary  

## Project Overview

This project develops and evaluates machine learning models to predict football match outcomes (Home Win, Draw, Away Win) using data from 10 European leagues spanning 6 seasons (2018-2023). The analysis includes 18,894 matches with over 150 engineered features, combining historical performance metrics, tactical formations, and player statistics.

## Key Results

- Best performing model: XGBoost with 64% accuracy and 63% F1-score
- Dataset: 18,894 matches across 10 leagues
- Features: 150+ engineered features including team performance, head-to-head records, formations, and player statistics
- Interpretability: SHAP and LIME analysis revealing key predictive factors

## Methodology

The project follows the CRISP-DM framework:

1. **Business Understanding**: Define prediction goals and success criteria
2. **Data Understanding**: Collection via API-Football and exploratory analysis
3. **Data Preparation**: Cleaning, transformation, and feature engineering
4. **Modeling**: Training and evaluation of multiple algorithms
5. **Evaluation**: Performance metrics and model comparison
6. **Deployment**: Model interpretability and insights

## Leagues Covered

- Premier League (England)
- La Liga (Spain)
- Serie A (Italy)
- Bundesliga (Germany)
- Ligue 1 (France)
- UEFA Champions League
- UEFA Europa League
- UEFA Europa Conference League
- Eredivisie (Netherlands)
- Primeira Liga (Portugal)

## Models Evaluated

1. XGBoost (Best performer)
2. LightGBM
3. Random Forest
4. Logistic Regression
5. Multi-Layer Perceptron (MLP)

## Project Structure

```
DOMAIN_APPLICATIONS_PROJECT/
├── data/
│   ├── raw/              # Raw data from API-Football
│   ├── processed/        # Cleaned and processed data
│   ├── features/         # Engineered features
│   └── predictions/      # Model predictions
├── notebooks/
│   ├── setup_notebook.ipynb
│   ├── 01_data_collection.ipynb
│   ├── 02_data_exploration_eda.ipynb
│   ├── 03_data_preprocessing.ipynb
│   ├── 04_feature_engineering.ipynb
│   ├── 05_model_training.ipynb
│   └── 06_model_explainability_interpretation.ipynb
├── models/               # Saved trained models
├── results/
│   ├── figures/         # Visualizations
│   ├── metrics/         # Performance metrics
│   ├── reports/         # Analysis reports
│   ├── model_explainability/  # SHAP and LIME outputs
│   └── tables/          # Summary tables
├── src/                 # Source code modules
└── docs/                # Documentation

```

## Features

### Historical Performance
- Rolling averages of goals scored and conceded
- Points per game over different time windows
- Form indicators (last 5, 10 matches)

### Head-to-Head Statistics
- Historical matchup records
- Goal differences in past encounters
- Win percentages between teams

### Tactical Features
- Team formations
- Starting lineups
- Substitution patterns

### League Context
- League-specific performance metrics
- Competition format (domestic vs. European)
- Home advantage indicators

## Model Interpretability

The project uses advanced explainability techniques:

- **SHAP (SHapley Additive exPlanations)**: Global and local feature importance
- **LIME (Local Interpretable Model-agnostic Explanations)**: Individual prediction explanations
- **Partial Dependence Plots**: Feature effect visualization

Key findings show that historical performance metrics and goal differences are the strongest predictors, with tactical features playing contextual roles.

## Key Insights

1. Home teams win 44.5% of matches, draws account for 24.1%, and away wins 31.4%
2. UEFA competitions show higher away win rates (nearly 50%), reflecting competitive balance
3. Home advantage decreased during 2020 COVID-19 season due to empty stadiums
4. Home teams score a median of 1.5 goals versus 1.0 for away teams
5. XGBoost outperformed other algorithms after hyperparameter tuning

## Technologies Used

- Python 3.x
- Pandas, NumPy (Data manipulation)
- Scikit-learn (Machine learning)
- XGBoost, LightGBM (Gradient boosting)
- SHAP, LIME (Model interpretability)
- Matplotlib, Seaborn (Visualization)
- API-Football (Data source)

## Data Source

Data collected from API-Football (v3.football.api-sports.io) covering seasons 2018-2023. The collection process handled rate limits of 400 requests per minute with a daily limit of 7,500 requests, ensuring compliance with API terms of service.

## Ethical Considerations

This project uses publicly available football data obtained through legitimate API access. The research respects data privacy guidelines and focuses on aggregated team-level statistics rather than individual player identification.

## Setup and Installation

1. Clone the repository
2. Install required dependencies
3. Run `setup_notebook.ipynb` to create project structure
4. Follow notebooks in sequence (01 through 06)

## Future Work

- Incorporate real-time injury and suspension data
- Expand to additional leagues and competitions
- Develop ensemble methods combining multiple models
- Create web interface for live match predictions
- Integrate betting odds as additional features

## License

This project is for educational and research purposes.

## Contact

For questions or collaboration opportunities, please contact through National College of Ireland.

---

Project completed as part of MSc Data Analytics program at National College of Ireland.
