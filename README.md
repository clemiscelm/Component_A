# Component A

Moving-average overlay pipeline: loads daily price data, computes a 20-day simple moving average, and plots the close price with the MA overlaid.

## Pipeline overview

1. **Load** — read `data/prices.csv`, parse the `date` column, sort chronologically.
2. **Compute** — 20-day simple moving average (`ma20`) of the `close` column.
3. **Plot** — line chart of `close` and `ma20` over time.
4. **Save** — write the chart to `outputs/plot.png`.

## Data sources

- `data/prices.csv` — CSV file with at least `date` and `close` columns.

## Outputs

- `outputs/plot.png` — daily close price with 20-day moving average overlay.

## Project structure

```
Component_A/
├── data/
│   └── prices.csv        # input data
├── outputs/
│   └── plot.png           # generated chart
├── src/
│   └── analysis.py        # pipeline script
├── requirements.txt
└── README.md
```

## How to run

From the repo root (`Component_A/`):

```bash
pip install -r requirements.txt
python src/analysis.py
```

The script reads `data/prices.csv`, computes the moving average, and saves the chart to `outputs/plot.png`.