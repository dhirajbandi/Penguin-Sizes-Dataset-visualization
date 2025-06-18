# Penguin-Sizes-Dataset-visualization

This project explores the "Penguin Size" dataset. The data contains measurements for Adelie, Chinstrap and Gentoo penguins such as culmen length, culmen depth, flipper length, body mass, the island where each penguin was observed and its sex.

## Dataset

The repository includes the file `penguins_size.csv` which comes from the Kaggle [Penguin Size Dataset](https://www.kaggle.com/datasets) (also known as the Palmer Penguins dataset). The CSV has the following columns:

- `species`
- `island`
- `culmen_length_mm`
- `culmen_depth_mm`
- `flipper_length_mm`
- `body_mass_g`
- `sex`

## Requirements

The notebook was originally run on Kaggle where the required libraries are preinstalled. To execute it locally you need at minimum:

- Python 3
- pandas
- matplotlib
- scikit-learn
- missingno (optional, used for visualizing missing data)

You can install everything with:

```bash
pip install pandas matplotlib scikit-learn missingno
```

## Setup

1. Clone this repository and change into the directory.
2. Install the required packages (see above).
3. Make sure the `penguins_size.csv` file is in the same folder as the notebook. If you downloaded the data separately, adjust the CSV path in the notebook accordingly (see below).
4. Open `penguin.ipynb` in Jupyter or a compatible environment and run the cells.

## Notebook overview

`penguin.ipynb` loads the CSV, displays sample rows and visualizes distributions for features such as sex, island and flipper length using pie charts. The notebook then encodes categorical columns and trains a simple `HistGradientBoostingClassifier` to predict the penguin species.

### Changing the CSV path

The notebook expects the dataset at `/kaggle/input/penguin-size-dataset/penguins_size.csv`. When running locally, change the line

```python
df = pd.read_csv('/kaggle/input/penguin-size-dataset/penguins_size.csv')
```

to point to your local copy, for example:

```python
df = pd.read_csv('penguins_size.csv')
```

## License

This project is a simple personal exploration of the dataset and contains no specific license.
