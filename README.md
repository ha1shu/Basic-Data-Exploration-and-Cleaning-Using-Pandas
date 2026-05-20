# 🛍️ Myntra Shopping Dataset — Data Exploration & Cleaning

A beginner-friendly data analysis project built as part of an internship assignment. This project demonstrates core Python and Pandas skills using a real-world Myntra e-commerce dataset sourced from Kaggle.

```text
Myntra-Shopping-Data-Cleaning/
│
├── Combined_dataset_cleaned.ipynb      # Main Jupyter Notebook
├── README.md                           # Project documentation
│
├── Data/
  ├── Combined_dataset.csv            # Original raw dataset
  └── shopping_cleaned.csv            # Cleaned dataset

```

##  Objective

Learn Python basics and perform data exploration and cleaning using the Pandas library on a real e-commerce shopping dataset.

---

##  Assignment Steps Covered

| # | Task | Description |
|---|------|-------------|
| 1 | Load Dataset | Read CSV into a Pandas DataFrame using `pd.read_csv()` |
| 2 | Explore Data | `head()`, `tail()`, `shape`, `columns`, `dtypes`, `describe()` |
| 3 | Handle Missing Values | Identify nulls; fill with defaults or drop high-null columns |
| 4 | Filter & Select | Boolean masks to filter rows; select specific columns |
| 5 | Remove Duplicates | Detect and drop duplicate rows using `drop_duplicates()` |
| 6 | Derived Column | Create `total_amount = initial_price × quantity` |
| 7 | Save Cleaned CSV | Export cleaned DataFrame with `to_csv(index=False)` |

---

##  Dataset Overview

| Field | Detail |
|-------|--------|
| **Source** | [Kaggle — anvitkumar/shopping-dataset](https://www.kaggle.com/datasets/anvitkumar/shopping-dataset) |
| **Platform** | Myntra (Indian Fashion E-commerce) |
| **Raw Shape** | 1,000 rows × 24 columns |
| **Cleaned Shape** | 1,000 rows × 27 columns |
| **Categories** | 97 unique product categories |

### Key Columns
- `product_id` — Unique product identifier
- `title` — Brand name
- `product_description` — Product description
- `category` — Product category (tops, dresses, shirts, etc.)
- `initial_price` — Original listed price (₹)
- `discount` — Discount percentage
- `rating` — Customer rating (0–5)
- `ratings_count` — Number of ratings received
- `quantity` *(derived)* — Estimated units sold
- `total_amount` *(derived)* — `initial_price × quantity`
- `discounted_price` *(derived)* — Price after discount
- `savings_per_unit` *(derived)* — Savings per item

---

##  Key Insights

- **Top categories** — `tops` (122), `dresses` (100), `shirts` (97)
- **Average discount** — 53.5% across all products
- **Price range** — ₹249 to ₹22,199 (median ≈ ₹1,200)
- **Average rating** — ~4.0 out of 5.0
- **57%** of products had no customer review text
- **30%** of products had no seller information

---

##  Data Cleaning Summary

| Column | Issue | Action Taken |
|--------|-------|-------------|
| `discount` | 121 missing values | Filled with `0` |
| `seller_name` | 301 missing values | Filled with `'Unknown Seller'` |
| `seller_information` | 301 missing values | Filled with `'Not Available'` |
| `what_customers_said` | 573 missing values | Filled with `'No Reviews'` |
| `variations` | 562 missing values | Filled with `'[]'` |
| `videos` | 781 missing (78%) | Column dropped |

---

##  Tech Stack

- **Python 3**
- **Pandas** — data loading, cleaning, transformation
- **NumPy** — numerical operations
- **Matplotlib** — base plotting
- **Seaborn** — statistical visualisations
- **Jupyter Notebook** — interactive development environment

---


## 📦 Output Files

| File | Description |
|------|-------------|
| `Combined_dataset_cleaned.ipynb` | Fully executed notebook with outputs |
| `shopping_cleaned.csv` | Final cleaned dataset — 0 nulls, 27 columns |
| `shopping_insights.png` | 4-panel chart: ratings, prices, discounts, revenue |

---

## 👤 Author

**Harshit Sharma**  
Internship Assignment — Python & Pandas Basics  
[Celebal Technologies]  
[2026]
