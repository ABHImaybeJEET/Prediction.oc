# Prediction.oc
# ⚽ Can Machines Predict the Unpredictable?
### A Student-Led AI & Football Analytics Project | FIFA World Cup 2026

---

## What is this project?

This is a machine learning project built by students to predict FIFA World Cup 2026 match outcomes. It combines historical football data, ensemble machine learning models, and Monte Carlo tournament simulations to generate data-backed predictions — and transforms those predictions into engaging football intelligence content for social media.

---

## The core question we are trying to answer

> **Can machine learning detect hidden structure inside football chaos?**

---

## Project Structure

```
world-cup-prediction/
│
├── data/
│   ├── matches_master.csv        # Raw historical match dataset
│   └── training_features.csv    # Engineered feature matrix
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_model_training.ipynb
│   ├── 04_hyperparameter_tuning.ipynb
│   └── 05_monte_carlo_simulation.ipynb
│
├── models/
│   ├── random_forest_model.pkl
│   └── xgboost_model.pkl
│
├── outputs/
│   ├── group_stage_predictions.csv
│   ├── knockout_probabilities.csv
│   └── championship_chances.csv
│
└── README.md
```

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core programming language |
| Pandas & NumPy | Data manipulation |
| Scikit-learn | Random Forest, GridSearchCV |
| XGBoost | Gradient boosting model |
| Matplotlib | Visualizations |
| BeautifulSoup & Requests | Web scraping |
| Google Colab | Development environment |
| Canva / Figma | Social media design |

---

## How the model works

### 1. Data Layer
- 20+ years of international football match records
- FIFA ranking trajectories
- Head-to-head historical patterns
- Player market valuation indicators
- Tournament-stage pressure analysis

### 2. Feature Engineering
- Rolling 5-match offensive and defensive form scores
- Squad experience weighting
- Pressure match performance indicators
- Expected goals trend estimation
- Temporal weighting (recent matches weighted higher)

### 3. Prediction Models
- **Random Forest Classifier** — reduces overfitting by averaging multiple decision trees
- **XGBoost Classifier** — learns from errors sequentially, captures non-linear momentum shifts
- **Ensemble disagreement flag** — when both models strongly disagree, the match is flagged as genuinely unpredictable

### 4. Monte Carlo Simulation
- Runs the entire World Cup tournament 10,000 times
- Each simulation uses the model's match probabilities as input
- Outputs championship probability, knockout progression likelihood, and group standings for every team

---

## Unique model features

| Feature | Description |
|--------|-------------|
| Form Guide vs AI | Compares simple 5-match form score against model prediction |
| Upset Detector | Flags matches where underdog exceeds 30% win probability |
| Confidence Levels | Low / Medium / High tags based on predicted probability |
| Dynamic Updating | Re-runs simulations after each real match result |
| What-If Simulator | Remove a player or add a red card and see how probabilities shift |
| Separate Group vs Knockout Models | Trained independently to reflect different match dynamics |
| Temporal Weighting | Recent matches weighted exponentially higher than older ones |
| Momentum Tracker | Championship probability updated after every round like a stock price |

---

## Confidence Level Logic

```python
if probability >= 0.65:
    confidence = "High"
elif probability >= 0.45:
    confidence = "Medium"
else:
    confidence = "Low / Coin Flip"
```

---

## Team Structure

| Team | Responsibility |
|------|---------------|
| Data Infrastructure | Scraping, cleaning, matches_master.csv |
| Feature Engineering | Rolling metrics, encoding, training_features.csv |
| Modeling & Simulation | Model training, tuning, Monte Carlo simulation |
| Media & Design | Visual templates, social media content, storytelling |

---

## Deliverable Timeline

| Phase | Deliverable | Deadline |
|-------|------------|----------|
| Phase 1 | Dataset scraping and cleaning | June 02, 2026 |
| Phase 2 | Feature engineering pipeline | June 06, 2026 |
| Phase 3 | Model tuning and simulation outputs | June 09, 2026 |
| Phase 4 | Design templates and prediction assets | June 10, 2026 |
| Phase 5 | Live tournament tracking begins | June 11–19, 2026 |

---

## Marquee matches being analyzed

- Argentina vs Spain
- Brazil vs France
- England vs Germany
- Portugal vs Argentina
- Netherlands vs Japan
- Morocco vs Croatia
- France vs Senegal
- Brazil vs Uruguay
- England vs Netherlands

---

## Dark horse teams being tracked

> Japan · Morocco · Senegal · South Korea · Croatia

Special analytical segments dedicated to teams statistically capable of outperforming expectations.

---

## Final philosophy

> *The goal is not to perfectly predict football. That is impossible.*
> *The goal is to quantify uncertainty better than intuition alone.*

This project treats the FIFA World Cup 2026 as a large-scale experimental playground for applied artificial intelligence — fusing machine learning, systems thinking, sports analytics, and collaborative engineering into one unified student-led initiative.

---

## Getting started

```python
# Clone the repo and open in Google Colab
# Install dependencies
pip install pandas numpy scikit-learn xgboost matplotlib

# Start with data exploration
jupyter notebook notebooks/01_data_exploration.ipynb
```

---

*Built with curiosity, code, and a love for football.*

