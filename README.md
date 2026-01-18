# DataVisualization-Project
# Aesthetics vs Efficiency: Is the "Beautiful Game" a Trap? ⚽📊

![Napoli Performance Profile](napoli_pizzaplot.png)
*(Fig. 1: The Efficiency Model - Napoli's 24/25 Percentile Rank Profile)*

> **Course:** Data Visualization | MSc in Data Science, University of Milano-Bicocca
> **Academic Year:** 2025/2026
> **Author:** Lorenzo Triolo

---

## 📌 Project Description

This project presents a data-driven investigation into one of the most polarizing debates in Italian football: **"Giochisti" (Aesthetes) vs "Risultatisti" (Pragmatists)**.
Using advanced metrics from the **2024/25 Serie A Season**, the analysis challenges the conventional wisdom that ball possession and territorial dominance differ from actual success.

[cite_start]The project explores the concept of **"Sterile Dominance"**[cite: 248]: why teams with elite possession metrics often fail to achieve results, while pragmatic sides maximize efficiency. Through unsupervised learning (K-Means) and comparative visual analytics, the study identifies distinct **Tactical Identities** and quantifies the **Efficiency Gap** between creating chances (xG) and converting them.

## 🎯 Project Objectives

* [cite_start]**Deconstruct "Sterile Dominance":** Quantify the disconnect between aesthetic metrics (Ball Possession %, Field Tilt) and concrete output (Points, Goals)[cite: 14].
* [cite_start]**Map Tactical Identities:** Classify Serie A teams into 4 distinct archetypes (e.g., *Patient Strategists* vs *Elite Aggressors*) using **K-Means Clustering** on style metrics[cite: 67].
* [cite_start]**Measure Conversion Efficiency:** Reveal the "hidden" performance by analyzing the divergence between Expected Goals (xG) and Actual Goals to identify clinical overperformers versus wasteful sides[cite: 17].
* [cite_start]**Champion's Profile Analysis:** A case study on **Napoli** (visualized above), demonstrating how defensive solidity (xGA overperformance) outweighed offensive volume[cite: 27, 388].

## 🔬 Methodologies & Technical Framework

The analysis is built on a custom **ETL pipeline** and statistical framework developed in Python:

### 1. Data Pipeline (ETL)
* [cite_start]**Ingestion:** Integration of 7 distinct datasets from **FBref (StatsBomb)** covering Shooting, Passing, Possession, and Defense[cite: 32].
* [cite_start]**Parsing & Cleaning:** Custom parsers (`SerieA preprocessing.ipynb`) handles European formatting, sanitizes string keys, and merges data into a consolidated structure of **20 teams x 70 variables**[cite: 55].
* **Feature Engineering:**
    * [cite_start]**Per 90 Standardization:** All volume metrics normalized to 90-minute averages for fair comparison[cite: 63].
    * **Efficiency Ratios:** Calculation of conversion rates (e.g., *Tackle Win %*, *Passing Accuracy*).

### 2. Statistical Analysis
* [cite_start]**Z-Score Normalization:** Applied to heterogeneous metrics (e.g., *Possession %* vs *Shots on Target*) to create comparable scales for **Radar Charts**[cite: 61].
* [cite_start]**Unsupervised Learning (Clustering):** Implementation of **K-Means** to segment teams based on `Directness`, `PPDA proxies`, and `Possession`, revealing the league's tactical structure beyond simple rankings[cite: 67].
* [cite_start]**Residual Analysis:** Measuring the "Luck/Skill" factor by calculating the residuals between Expected (xG/xGA) and Actual outcomes[cite: 69].

## 🛠️ Technologies Used

* **Language:** Python 3.x
* [cite_start]**Data Manipulation:** `Pandas`, `NumPy` (Data cleaning, merging, type casting)[cite: 57].
* **Machine Learning:** `Scikit-learn` (StandardScaler, K-Means Clustering).
* [cite_start]**Visualization:** `Matplotlib`, `Seaborn` (Static, publication-quality charts)[cite: 58].
* [cite_start]**Data Source:** **FBref** (via StatsBomb) & **Understat**[cite: 31, 54].

## 📥 How to View the Code

You don't need to be a developer to view the analysis.
1.  **View the Notebooks:** Click on `SerieA preprocessing.ipynb` or the main visualization notebook directly in the file list above to see the code and charts rendered in the browser.
2.  **Download the Project:** Click the green **Code** button (top right) and select **Download ZIP** to get all data and scripts on your computer.

---
*This project is distributed under a Creative Commons CC BY-NC-SA 4.0 license.*
