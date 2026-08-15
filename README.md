# 📚 Manga Market Analysis

An exploratory data analysis project examining **manga sales, publisher market share, demographics, and sales efficiency** using data on best-selling manga series.

## 🎯 Problem

What distinguishes the world's best-selling manga series?

This project explores several questions:

* Which manga series have the highest cumulative sales?
* Does a larger number of volumes necessarily mean higher sales?
* Which publishers dominate the best-selling manga market?
* Which demographics are most represented among high-selling titles?
* Which manga series have the highest sales efficiency per volume?

## 📊 Dataset

The dataset was compiled from publicly available records of **best-selling manga series**, including titles with approximately **50 million or more estimated sales**.

The data were collected through web scraping and subsequently cleaned and transformed for analysis.

### Main Variables

| Variable           | Description                           |
| ------------------ | ------------------------------------- |
| `Title`            | Manga series title                    |
| `Author`           | Creator / illustrator                 |
| `Publisher`        | Original Japanese publisher           |
| `Demographic`      | Primary target audience               |
| `Volumes`          | Number of compiled volumes            |
| `Sales_Millions`   | Estimated sales in millions of copies |
| `Sales_Per_Volume` | Estimated sales per published volume  |

## 🔬 Method

The analysis uses **Python-based exploratory data analysis and feature engineering**.

### 1. Data Cleaning

Raw scraped data were cleaned by:

* Removing citation markers
* Removing symbols and formatting characters
* Standardizing numeric values
* Converting sales and volume fields into numeric variables
* Handling values containing `+` and thousands separators

### 2. Feature Engineering

A **Sales Per Volume** metric was created:

**Sales Per Volume = Total Sales ÷ Number of Volumes**

This provides a simple measure of sales efficiency and helps distinguish:

* Long-running franchises with large cumulative sales
* Shorter series with unusually high sales relative to their number of volumes

### 3. Exploratory Analysis

The analysis examines:

* Top-selling manga
* Publisher distribution
* Demographic distribution
* Sales versus number of volumes
* Sales efficiency per volume

### 4. Visualization

Several visualization techniques are used:

* Bar charts
* Horizontal ranking charts
* Pie charts
* Scatter plots
* Comparative efficiency charts

## 📈 Results

### 1. Top-Selling Manga

Among the highest-selling titles in the dataset:

| Rank | Manga        | Publisher  | Demographic | Volumes | Sales (M) |
| ---: | ------------ | ---------- | ----------- | ------: | --------: |
|    1 | One Piece    | Shueisha   | Shōnen      |    108+ |       600 |
|    2 | Doraemon     | Shogakukan | Children    |      45 |       300 |
|    3 | Golgo 13     | Shogakukan | Seinen      |    200+ |       300 |
|    4 | Case Closed  | Shogakukan | Shōnen      |    105+ |       270 |
|    5 | Dragon Ball  | Shueisha   | Shōnen      |      42 |       260 |
|    6 | Naruto       | Shueisha   | Shōnen      |      72 |       250 |
|    7 | Demon Slayer | Shueisha   | Shōnen      |      23 |       220 |

The rankings illustrate that high cumulative sales can be achieved through very different publishing strategies.

### 2. Longevity vs. Sales Efficiency

The analysis reveals two broad patterns.

**Long-running franchises**

Series such as *One Piece*, *Golgo 13*, and *KochiKame* accumulate very large total sales over many volumes and years of publication.

**High-efficiency series**

Some newer or shorter series achieve unusually high sales relative to their number of volumes.

For example, **Demon Slayer** has approximately 220 million sales across 23 volumes, producing an estimated **9.56 million sales per volume**.

This demonstrates why total sales alone can provide an incomplete picture of commercial performance.

### 3. Publisher Distribution

**Shueisha** has a particularly strong presence among the highest-selling titles, supported by major franchises such as:

* One Piece
* Dragon Ball
* Naruto
* Demon Slayer
* Slam Dunk

Shogakukan and Kodansha also have substantial representation through long-running and highly successful franchises.

### 4. Demographic Distribution

The **Shōnen** demographic represents the largest share among the high-selling titles in the analyzed sample.

This suggests that Shōnen manga has a particularly strong presence among globally successful commercial franchises.

However, the analysis describes the composition of this sample rather than establishing that demographic category itself causes higher sales.

## 📊 Visualization

### Sales vs. Number of Volumes

A scatter plot compares the number of published volumes with total manga sales.

### Sales Efficiency

The `Sales_Per_Volume` metric provides another perspective by comparing cumulative sales with the number of volumes published.

This helps identify titles that achieved high sales without requiring extremely long publication histories.

## 💡 Conclusion

The analysis highlights several patterns in the commercial performance of best-selling manga.

### Key takeaways

**1. Cumulative sales and sales efficiency are different measures.**

Long-running manga can accumulate enormous total sales through hundreds of volumes, while shorter series can achieve very high sales per volume.

**2. Longevity is one path to commercial success, but not the only one.**

The dataset contains both legacy franchises with extensive publication histories and newer titles with high sales efficiency.

**3. Shueisha has a strong presence among top-selling manga.**

Major Shueisha franchises account for a substantial portion of the highest-selling titles in the analyzed sample.

**4. Shōnen dominates the high-selling sample.**

The demographic is heavily represented among titles with very large cumulative sales.

Overall, the project demonstrates how **feature engineering and exploratory data analysis can reveal different dimensions of commercial performance** that are not visible from total sales alone.

> **Note:** The analysis is descriptive. Sales estimates, publication counts, and publicly available metadata do not provide sufficient evidence to establish causal relationships between publisher, demographic, anime adaptation, or other factors and commercial success.

## 🛠️ Technologies

* **Python**
* **Pandas** — data manipulation
* **NumPy** — numerical computation
* **Matplotlib** — visualization
* **Seaborn** — statistical visualization
* **Jupyter Notebook** — analysis
* **Web Scraping** — data collection
* **Regular Expressions** — data cleaning
* **Feature Engineering** — sales efficiency metrics

## 📁 Repository Structure

```text
manga-market-analysis/
│
├── manga-market-analysis.ipynb
└── README.md
```

## 📌 Topics

`Python` `Data Analysis` `Exploratory Data Analysis` `Feature Engineering` `Web Scraping` `Data Visualization` `Manga` `Market Analysis` `Business Analytics`
