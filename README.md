# 📚 Market Dynamics & Longevity Analysis of Best-Selling Manga

An end-to-end data analysis project exploring the global manga market. This project scrapes, cleans, and analyzes sales data of the world's highest-grossing manga series to uncover trends in demographics, publisher market share, and sales efficiency.

---

## 📌 Project Overview & Objectives

The primary objective of this project is to quantitatively evaluate what drives commercial success in the manga industry. By extracting publicly available records (such as Wikipedia's best-selling manga database), this analysis answers key industry questions:

* **Top-Tier Performance:** Which manga series hold the highest global sales of all time?
* **Volume Efficiency vs. Longevity:** Does a higher volume count guarantee higher sales, or do modern series achieve higher sales velocity per volume?
* **Publisher Dominance:** Which Japanese publishers (*Shueisha*, *Shogakukan*, *Kodansha*) control the largest market share?
* **Demographic Audience:** How are sales distributed across target demographics (*Shōnen*, *Seinen*, *Shōjo*, *Children*)?

---

## 📊 Dataset Description

Data was extracted using custom web scraping pipelines targeting compiled *tankōbon* sales figures worldwide (series with $\ge 50$ million estimated sales).

### Feature Dictionary

| Feature | Type | Description |
| :--- | :--- | :--- |
| `Title` | String | Official title of the manga series. |
| `Author` | String | Creator(s) / Illustrator(s) of the series. |
| `Publisher` | String | Original Japanese publishing house. |
| `Demographic` | Categorical | Primary target audience (*Shōnen*, *Seinen*, *Shōjo*, etc.). |
| `Volumes` | Integer | Total number of compiled physical volumes. |
| `Sales_Millions` | Float | Estimated global sales/circulation in millions of copies. |
| `Sales_Per_Volume` | Float | **Derived Metric:** Average sales per single published volume. |

---

## 📈 Sample Benchmark (Top 10 Rankings)

| Rank | Manga Title | Publisher | Demographic | Volumes | Total Sales (M) | Sales / Volume (M) |
| :---: | :--- | :--- | :--- | :---: | :---: | :---: |
| **1** | *One Piece* | Shueisha | Shōnen | 108+ | 600 | 5.55 |
| **2** | *Doraemon* | Shogakukan | Children | 45 | 300 | 6.67 |
| **3** | *Golgo 13* | Shogakukan | Seinen | 200+ | 300 | 1.50 |
| **4** | *Case Closed / Detective Conan* | Shogakukan | Shōnen | 105+ | 270 | 2.57 |
| **5** | *Dragon Ball* | Shueisha | Shōnen | 42 | 260 | 6.19 |
| **6** | *Naruto* | Shueisha | Shōnen | 72 | 250 | 3.47 |
| **7** | *Demon Slayer: Kimetsu no Yaiba*| Shueisha | Shōnen | 23 | 220 | **9.56** |
| **8** | *Slam Dunk* | Shueisha | Shōnen | 31 | 185 | 5.97 |
| **9** | *KochiKame* | Shueisha | Shōnen | 201 | 157 | 0.78 |
| **10**| *Jujutsu Kaisen* | Shueisha | Shōnen | 30 | 150 | 5.00 |

---

## 🔬 Analysis Methodologies Used

This project applies specific exploratory data analysis (EDA), feature engineering, and visualization techniques:

1. **Data Cleaning & Regex Extraction:** Standardizes unstructured scraping noise (removing Wikipedia citations like `[1]`, symbols `†`, `‡`, and characters like `+` or `,`) to convert raw text into clean numerical values.
2. **Feature Engineering (Sales Velocity Metric):** Introduces a derived metric to measure performance efficiency:
   $$\text{Sales Per Volume} = \frac{\text{Sales (in Millions)}}{\text{Volumes Count}}$$
   *This metric isolates high-velocity hits from long-running legacy titles.*
3. **Categorical & Frequency Aggregation:** Analyzes demographic market shares (`value_counts()`) and filters top performers (`sort_values()`).
4. **Visual Analytics:**
   * **Bar Charts:** Evaluates top absolute sales.
   * **Pie Charts:** Visualizes demographic distributions.
   * **Scatter Plots (with size encoding):** Correlates serial duration (volumes) against commercial yield (sales).
   * **Horizontal Efficiency Charts:** Identifies titles with the highest sales density per volume.

---

## 🔍 Key Insights & Analysis

### 1. Publisher Dominance (Shueisha's Monopolistic Grip)
**Shueisha** dominates the top-selling tiers, largely propelled by its flagship publication, *Weekly Shōnen Jump*. **Shogakukan** and **Kodansha** capture secondary market shares through long-running legacy franchises.

### 2. Shōnen as the Primary Economic Engine
Over **70%** of manga titles achieving $>100\text{ million}$ global sales belong to the **Shōnen** demographic. While **Seinen** holds strong secondary positions through cult-classic long-runners (*Golgo 13*, *Kingdom*), Shōnen's broad multi-generational appeal generates the highest revenue.

### 3. The Shift in Success Models: Longevity vs. High Velocity
The data reveals two distinct commercial models:
* **The Legacy Model (Longevity):** Franchises like *One Piece*, *Golgo 13*, and *KochiKame* build massive cumulative totals across decades and hundreds of volumes ($100\text{--}200+$ volumes).
* **The Modern Velocity Model (High Efficiency):** Newer titles leverage instantaneous global streaming anime adaptations to drive unprecedented backlog print sales. For example, **Demon Slayer** generated **220 million sales in just 23 volumes**, yielding an extraordinary velocity of **$\sim 9.56\text{ million}$ sales per volume**.

---

## 💡 Conclusion

* **Shift in Industry Dynamics:** Modern manga success relies less on 20-year serializations and more on high-velocity explosive growth driven by anime/streaming multimedia synergy.
* **Metric Importance:** Evaluating sales on a *per-volume* basis yields a more accurate reflection of modern popularity and market efficiency than total raw sales alone.
* **Demographic Investment:** *Shōnen* remains the most commercially scalable demographic for global market penetration and cross-media adaptations.

---
