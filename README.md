# ABC-XYZ Analysis for E-commerce

This repository contains tools and scripts for performing ABC-XYZ analysis in the e-commerce sector. 
The main goal of the project is to classify products based on their sales volume and demand variability, helping businesses optimize inventory management and procurement strategies.

![x](https://miro.medium.com/v2/1*UE0HHiBs-ViRM4-4-Bv3qA.png)

---

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Data Requirements](#data-requirements)
- [ABC-XYZ Analysis Methodology](#abc-xyz-analysis-methodology)
- [Results](#results)

---

## Introduction

ABC-XYZ analysis is a powerful inventory classification method that combines:
- **ABC Classification**: Categorizes products based on their revenue contribution.
- **XYZ Classification**: Categorizes products based on demand stability (coefficient of variation).

This project enables:
- Identifying high-revenue products.
- Analyzing demand consistency.
- Optimizing stock management and procurement strategies.

---

## Features

- Data loading and preprocessing.
- Computation of total and average sales.
- Calculation of demand variability.
- Classification of products into ABC and XYZ categories.
- Merging ABC and XYZ classifications for final analysis.
- Generation of insights for better inventory control.

---

## Data Requirements

The input dataset should contain the following columns:

| Column Name   | Description                             |
|--------------|-----------------------------------------|
| InvoiceDate  | Date and time of the transaction.      |
| Customer ID  | Unique customer identifier.            |
| StockCode    | Product identifier.                    |
| Quantity     | Number of purchased items.             |
| Price       | Price per item.                         |

The file should be in CSV format, without duplicates, and with correct values.

---

## ABC-XYZ Analysis Methodology

1. **Data preprocessing**:
   - Removing irrelevant columns and calculating revenue.
   - Extracting year and month for time-based analysis.
2. **XYZ Classification**:
   - Calculating average sales and standard deviation.
   - Computing the coefficient of variation (CoV).
   - Assigning categories:
     - **X**: Low variability (CoV ≤ 0.5)
     - **Y**: Medium variability (0.5 < CoV ≤ 1)
     - **Z**: High variability (CoV > 1)
3. **ABC Classification**:
   - Calculating cumulative revenue percentage.
   - Assigning categories:
     - **A**: Top 80% revenue-generating products.
     - **B**: Next 10% revenue-generating products.
     - **C**: Bottom 10% revenue-generating products.
4. **Final Analysis**:
   - Merging ABC and XYZ categories to form **ABC-XYZ** groups.
   - Generating insights for inventory management and demand forecasting.

---

## Results

- **Understanding product demand**: Identifying stable and volatile products.
- **Optimizing inventory**: Prioritizing stock for high-revenue, stable-demand items.
- **Enhancing procurement strategies**: Adjusting purchasing policies based on demand patterns.

This analysis helps businesses reduce stockouts, minimize overstocking, and improve overall supply chain efficiency.
