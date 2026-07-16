# Zomato Data Analysis Using Python

Exploratory data analysis (EDA) of restaurant data scraped from Zomato, using `pandas`, `numpy`, `matplotlib`, and `seaborn` to uncover patterns in ratings, votes, order types, and pricing.

## 📌 Overview

This notebook walks through cleaning and visualizing a Zomato restaurant dataset to answer questions like:

- What types of restaurants are most common?
- Which restaurant type receives the most customer engagement (votes)?
- Do restaurants that accept online orders get rated differently than those that don't?
- What's the distribution of ratings and price points ("approx cost for two")?
- Is there a relationship between restaurant type and online ordering availability?

## 📂 Dataset

- **File expected:** `Zomato-data-.csv`
- **Path used in notebook:** `/content/Zomato-data-.csv` (this is a Google Colab path — update it to your local path, e.g. `./Zomato-data-.csv`, if running elsewhere)

**Key columns used:**

| Column | Description |
|---|---|
| `name` | Restaurant name |
| `rate` | Rating, originally in `x/5` string format |
| `votes` | Number of customer votes |
| `approx_cost(for two people)` | Approximate cost for two people |
| `listed_in(type)` | Restaurant category (e.g. Dining, Cafes, Delivery) |
| `online_order` | Whether the restaurant accepts online orders (Yes/No) |

## 🛠️ Requirements

```bash
pip install pandas numpy matplotlib seaborn
```

Tested with Python 3.x in a Jupyter/Colab environment.

## 🚀 How to Run

1. Clone/download this repository.
2. Place `Zomato-data-.csv` in the working directory (or update the file path in the second cell).
3. Open `Zomato_Data_Analysis_Using_Python.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
4. Run all cells in order.

## 🔍 Analysis Steps

1. **Import libraries** — pandas, numpy, matplotlib, seaborn
2. **Load data** — read the CSV into a DataFrame and preview it
3. **Clean the `rate` column** — convert `"4.1/5"` style strings into clean float values (e.g. `4.1`)
4. **Inspect structure** — check data types and column info (`.info()`)
5. **Check for missing values** — `.isnull().sum()`
6. **Restaurant type distribution** — count plot of `listed_in(type)`
7. **Votes by restaurant type** — line plot of total votes grouped by type
8. **Top restaurant(s) by votes** — identify the restaurant(s) with the maximum votes
9. **Online order distribution** — count plot of `online_order` (Yes/No)
10. **Ratings distribution** — histogram of the cleaned `rate` column
11. **Cost distribution** — count plot of `approx_cost(for two people)`
12. **Ratings vs. online order** — box plot comparing rating spread for online-order vs. non-online-order restaurants
13. **Type vs. online order heatmap** — pivot table + heatmap showing counts of restaurant type against online order availability

## 📊 Key Visualizations

- Count plot — restaurant types
- Line plot — votes per restaurant type
- Count plot — online order availability
- Histogram — rating distribution
- Count plot — cost for two
- Box plot — rating by online order status
- Heatmap — restaurant type vs. online order

## 💡 Sample Insights

- Most restaurants fall into a small number of dominant categories (e.g. Dining, Delivery).
- Restaurants offering online ordering tend to show a different rating spread than those that don't.
- A small number of restaurant types account for the majority of total votes, indicating where customer engagement concentrates.

*(Exact findings depend on the dataset used — run the notebook to see results for your data.)*

## 📁 Project Structure

```
.
├── Zomato_Data_Analysis_Using_Python.ipynb   # Main analysis notebook
├── Zomato-data-.csv                           # Dataset (not included — add your own)
└── README.md                                  # This file
```

## 📝 Notes

- The `handleRate` function strips the `/5` suffix from ratings and converts them to floats — re-run this cell if you reload the raw data.
- Update the CSV path if you're not running in Google Colab.

## 📄 License

This project is intended for educational and portfolio purposes.
