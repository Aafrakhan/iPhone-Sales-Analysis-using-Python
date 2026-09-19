# 📱 iPhone Sales Analysis

Exploratory data analysis of Apple iPhone listings on Flipkart India — exploring pricing, discounts, customer ratings, and review volume across the iPhone lineup using Python, Pandas, and Seaborn/Plotly.

## 📌 Overview

This project cleans and analyzes a dataset of 62 iPhone listings to answer questions like:

- How much do iPhones cost, and how wide is the price range?
- Which iPhones are rated the highest, and by how many people?
- Do discounts differ between flagship and budget/older models?
- Does a higher price mean a higher rating — or more reviews?
- Which iPhone models drive the most sales volume?

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** & **NumPy** — data cleaning and manipulation
- **Matplotlib** & **Seaborn** — static visualizations
- **Plotly Express** — interactive charts
- **Jupyter Notebook**

## 📊 Dataset

The dataset contains 62 iPhone listings scraped from Flipkart India, with the following columns:

| Column | Description |
|---|---|
| `Product Name` | Full listing name (model, color, storage) |
| `Sale Price` | Current selling price (₹) |
| `Mrp` | Original listed price (₹) |
| `Discount Percentage` | Discount applied |
| `Number Of Ratings` | Total ratings received |
| `Number Of Reviews` | Total written reviews received |
| `Star Rating` | Average star rating (out of 5) |
| `Ram` | RAM specification |


## 🧹 Data Cleaning & Feature Engineering

- Confirmed no missing values or duplicate rows
- Split `Product Name` into separate **Model**, **Storage**, and **Color** columns
- Added a **Discount Amount** column (MRP minus Sale Price)
- Fixed a chart bug where bar labels and values were misaligned due to a `value_counts()` mismatch

## 📈 Key Insights

- Prices range from **₹29,999** (iPhone SE) to **₹140,900** (iPhone 12 Pro, 512GB) — average **₹80,074**.
- Star ratings cluster tightly between **4.5–4.7** across almost every listing — rating alone doesn't separate a "good" listing from a "great" one.
- The cheapest iPhone (SE) has **95,807 ratings and 8,154 reviews**, versus just **542 ratings and 42 reviews** for the priciest model — **budget models drive the bulk of sales volume**.
- Discounts are deepest on older/cheaper models (SE: 24% off, XR: 20% off), while flagships (11 Pro Max, 12 Pro) see little to no discount.

See [`iPhone_Sales_Analysis_Summary_Report.pdf`](./iPhone_Sales_Analysis_Summary_Report.pdf) for the full write-up.


## 🔮 Future Improvements

- Add a timestamp/date field to track how ratings and pricing change over time
- Expand the dataset to more iPhone generations and other retailers for comparison
- Build an interactive dashboard (Plotly Dash/Streamlit) for exploring price vs. popularity

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
