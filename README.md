# F1 2026 Race Predictor 🏎️

I watch F1 regularly and wanted to see if I could actually predict race results using data. Turns out — kind of? The model gets within 3-4 positions on average which honestly feels about right given how chaotic F1 can be.

The 2026 season has been wild so far. New regulations, completely different cars, and Mercedes have built an absolute rocketship. Antonelli is already winning races at 19. So I made sure to weight the 2026 data heavier in the model since last year's patterns don't really apply anymore.

## What it does
- Pulls live F1 data using FastF1 (official F1 timing API)
- Stores everything in a SQL database
- Trains a Random Forest model weighted toward 2026 results
- Predicts finishing positions for upcoming races

## Predictions vs Reality
| Race | Predicted Winner | Actual Winner |
|------|-----------------|---------------|
| Miami GP 2026 | Kimi Antonelli | TBD — race is May 1 |

Will update this after every race to track how accurate the model actually is.

## Tech Stack
- **Python** — data pipeline and modelling
- **FastF1** — official F1 timing data
- **pandas** — data manipulation
- **scikit-learn** — Random Forest model
- **SQLAlchemy** — SQL database
- **Tableau** — dashboard (coming soon)

## Model Performance
- Algorithm: Random Forest Regressor
- Training data: 545 rows (full 2025 season + 2026 rounds 1-3)
- Mean Absolute Error: **3.40 positions**
- 2026 data weighted 3x — new regs mean last year's patterns don't tell the whole story

## How to run
```bash
git clone https://github.com/Agamps99/f1-race-predictor.git
cd f1-race-predictor
python -m venv venv
source venv/bin/activate
pip install fastf1 pandas sqlalchemy scikit-learn
jupyter notebook f1_data.ipynb
```

## Author
Agam — data science student at UTS, F1 fan, curious about whether the data can predict what happens on track.
