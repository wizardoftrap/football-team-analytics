# Football Team Analytics Notebook

## Overview
This Jupyter notebook, created on Kaggle, analyzes football player and team statistics for the 2024-2025 season. It provides insights into player performance, team metrics, and playing styles across major European leagues using data from the dataset `players_data-2024_2025.csv`.

## Dataset
The analysis is based on the dataset available at:
- **Kaggle Dataset**: [Football Players Stats 2024-2025](https://www.kaggle.com/datasets/6586397/players_data-2024_2025)
- Contains 2,840 entries with 267 columns, including player statistics like goals (Gls), expected goals (xG), assists (Ast), expected assists (xAG), tackles (Tkl), and more.

## Notebook Contents
The notebook performs the following analyses:
1. **Data Preprocessing**:
   - Loads the dataset and handles missing values by filling with zeros.
   - Displays dataset information and a preview of the data.

2. **Player Analysis**:
   - Extracts specific performance metrics (e.g., Gls, xG, Ast, xAG, G+A) for individual players, such as Pedri.
   - Identifies players with similar playing styles using cosine similarity on normalized features like goals, tackles, progressive passes, and carries.

3. **Team Analysis**:
   - Aggregates team statistics by summing metrics like goals, assists, and defensive actions.
   - Calculates derived metrics:
     - `Goals_per_xG`: Ratio of actual goals to expected goals.
     - `Defensive_Actions`: Sum of tackles, blocks, and clearances.
     - `Progression_Rate`: Progressive passes per touch.
     - `Turnover_Rate`: Turnovers (miscontrols + dispossessions) per touch.
   - Categorizes team performance as "Over," "Under," or "Partial" based on goals and assists compared to expected values.

4. **League Analysis**:
   - Determines dominant playing styles by league (e.g., Bundesliga: Cautious Pass and Move, Premier League: Aggressive Long Ball).

## Example Outputs
- **Player Similarity**:
  - For Lamine Yamal, the notebook identifies players like Iñaki Williams and Son Heung-min as similar based on metrics like goals, assists, and progressive carries.
- **Team Performance**:
  - Top teams by G+A (Goals + Assists): Barcelona (167), Bayern Munich (162), Paris S-G (158).
- **League Styles**:
  - Example: Premier League teams favor "Aggressive Long Ball Football."

## Notes
- The notebook assumes the dataset is in the `/kaggle/input/football-players-stats-2024-2025/` directory, as per Kaggle's default structure. Update the file path if running locally.
- Visualizations (e.g., plots) may require additional code to display results, as the provided notebook snippet focuses on data processing and analysis.
- The dataset includes goalkeeper-specific metrics (e.g., Saves, CS), which are primarily relevant for goalkeeper analysis.

## License
This notebook is intended for educational and analytical purposes. The dataset is sourced from Kaggle, and usage should comply with Kaggle's terms and the dataset's licensing.

## Acknowledgments
- **Kaggle**: For hosting the dataset and providing the environment to develop this notebook.
- **Data Source**: The `players_data-2024_2025.csv` dataset, which compiles comprehensive football statistics.
