# 🎬 Netflix Originals Data Analysis: Exploring Trends and Insights

Welcome to a comprehensive SQL-based analytical project focused on Netflix Originals. This study explores viewer reception, genre-based content performance, and runtime trends by leveraging IMDb ratings and genre metadata. Using structured queries and datasets, the analysis uncovers patterns that help us understand how Netflix produces and promotes its original content.

---
## 🗂️ Database Schema

The project uses a normalized schema consisting of two related tables: `netflix_originals` and `genre_details`, connected by `GenreID`.

![Database Schema](ERR_Diagram.png)

---

## 📌 Objectives

- Evaluate IMDb score distributions across genres.
- Identify high-performing genres and standout content.
- Explore relationships between runtime and content depth.
- Rank titles within genres based on audience ratings.
- Assess Netflix’s genre-wise content investment.
- Discover genres consistently delivering critically acclaimed titles.

---

## 🧠 Analytical Questions & Findings

### 1. What are the average IMDb scores for each genre?
- **Approach**: Calculated `AVG(IMDBScore)` per genre via a join and group.
- **Insight**: Provided a clear understanding of how 19 genres perform based on audience feedback.

---

### 2. Which genres have an average IMDb score higher than 7.5?
- **Approach**: Used `HAVING` clause to filter genres exceeding the average score threshold.
- **Insight**: Only **Concert Film** crossed the 7.5 mark, indicating focused excellence in that genre.

---

### 3. List Netflix Original titles in descending order of their IMDb scores.
- **Approach**: Sorted all titles by `IMDBScore DESC`.
- **Insight**: Helped spotlight the highest-rated Netflix Originals.

---

### 4. Retrieve the top 10 longest Netflix Originals by runtime.
- **Approach**: Sorted by `Runtime` and limited to the top 10.
- **Insight**: Revealed the most time-intensive productions, suggesting deeper narrative investment.

---

### 5. Retrieve the titles of Netflix Originals along with their respective genres.
- **Approach**: Simple `JOIN` on `GenreID`.
- **Insight**: Enabled genre tagging for all titles, useful for segmentation and recommendations.

---

### 6. Rank Netflix Originals based on their IMDb scores within each genre.
- **Approach**: Used `DENSE_RANK()` partitioned by genre.
- **Insight**: Identified top-rated content **within each genre** for more granular comparison.

---

### 7. Which Netflix Originals have IMDb scores higher than the average of all titles?
- **Approach**: Applied a subquery to calculate and filter using the global IMDb average.
- **Insight**: Filtered out underperformers and spotlighted quality titles.

---

### 8. How many Netflix Originals are there in each genre?
- **Approach**: Grouped by genre and counted titles.
- **Insight**: Clarified Netflix’s investment strategy across content categories.

---

### 9. Which genres have more than 5 titles with IMDb scores above 8?
- **Approach**: Applied `WHERE` and `HAVING` conditions to extract genres with high-performing titles.
- **Insight**: Only **Documentary** met the criteria, showing consistent quality and quantity.

-
