# ⚽ Football Tables & Data Representation

A Python toolkit for fetching, processing, and visually representing football (soccer) league standings, team stats, and match data.

For live TV schedules and broadcasts, check out [voetbal op tv vandaag](https://voetbalwedstrijdvandaag.nl/). You can also view the project documentation and source guide on [Bitbucket README](https://bitbucket.org/voetbaloptv/voetbaloptv.bitbucket.io/src/main/README.md).

## 🚀 Features

- **League Tables:** Format real-time or historical league standings.
- **Data Visualizations:** Visual charts for form guides, goal differentials, heatmaps, and shot maps.
- **Data Export:** Process structured datasets in CSV or JSON format.

## 📁 Repository Structure

- `data/` — Local storage for cached data files.
- `notebooks/` — Interactive Jupyter notebooks demonstrating data analysis and visual generation.
- `src/` — Core Python modules for API integration and plotting algorithms.

## 📊 Sample Python Code

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Sample Standings Data
data = {
    'Team': ['Arsenal', 'Manchester City', 'Liverpool', 'Aston Villa'],
    'MP': [28, 28, 28, 28],
    'GD': [46, 35, 39, 17],
    'Pts': [64, 63, 64, 55]
}

df = pd.DataFrame(data)

# Bar chart of points
plt.figure(figsize=(8, 4))
sns.barplot(data=df, x='Pts', y='Team', palette='viridis')
plt.title('Top Premier League Teams by Points')
plt.xlabel('Points')
plt.ylabel('Team')
plt.tight_layout()
plt.show()
