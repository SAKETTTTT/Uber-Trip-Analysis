# Uber Trip Analysis

Exploratory analysis of 1,156 Uber trip records from 2016, plus two small models: a linear regression that predicts trip distance and a KMeans clustering of trips.

Everything is in one notebook, `UberData-2.ipynb`, with an explanation above each step and a summary at the bottom.

## Data

`UberDataset.csv` (included) has one row per trip:

| Column | Meaning |
|---|---|
| `START_DATE`, `END_DATE` | When the trip started and ended |
| `CATEGORY` | Business or Personal |
| `START`, `STOP` | Start and end location |
| `MILES` | Distance travelled |
| `PURPOSE` | Why the trip was made (empty for about half the trips) |

## What the notebook does

1. **Clean:** fill empty purposes, parse the dates, add the hour of the day (Morning, Afternoon, Evening, Night), drop missing and duplicate rows.
2. **Explore:** trips by category, time of day, purpose, month and weekday; distribution of distances; correlations.
3. **Model:** linear regression (scikit-learn pipeline with one-hot encoding) predicting miles from trip duration and category.
4. **Cluster:** KMeans with 3 clusters on standardized miles and duration.

## Highlights

- 1,154 trips remain after cleaning, covering all 12 months; 93% are Business trips.
- Afternoon is the busiest time of day, Friday the busiest weekday and December the busiest month.
- Half of all trips are 6 miles or shorter; 96.5% are under 40 miles.
- Linear regression on duration and category: R² = 0.75.
- KMeans splits trips into three groups: short trips (about 7 miles, 18 minutes), medium trips (about 38 miles, 80 minutes) and a few very long ones (about 174 miles, 188 minutes).

## A note on the dates

The CSV mixes two date styles (`01-01-2016 21:11` and `1/13/2016 13:54`). By default, pandas guesses the format from the first row and turns every row in the other style into a missing value, which then gets dropped without any warning. The notebook parses with `format='mixed'` so all trips are kept (this needs pandas 2.0 or newer).

## Run it

```bash
git clone https://github.com/SAKETTTTT/Uber-Trip-Analysis.git
cd Uber-Trip-Analysis
pip install -r requirements.txt
jupyter notebook UberData-2.ipynb
```

## License

MIT, see [LICENSE](LICENSE).
