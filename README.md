# BMW-Global-Sales-Analysis

📌 Project Overview

This project explores BMW’s global sales dataset (2010–2024), containing 50,000 rows × 11 columns.
We perform Exploratory Data Analysis (EDA) to uncover trends in regions, models, fuel types, prices, and engine sizes.
Finally, we build a Decision Tree Classifier to predict Sales_Classification (High / Low).

📂 Dataset Description

Columns:

Model → BMW car model (e.g., 3 Series, i8, 7 Series, X1…)

Year → Year of sale/manufacture (2010–2024)

Region → Region of sale (Asia, Europe, North America, etc.)

Color → Car color (Red, Silver, White, etc.)

Fuel_Type → Petrol, Diesel, Hybrid, Electric

Transmission → Manual / Automatic

Engine_Size_L → Engine size in liters

Mileage_KM → Mileage in kilometers

Price_USD → Price in U.S. dollars

Sales_Volume → Units sold

Sales_Classification → Categorized sales (High / Low)

Data health check:

No missing values ✅

No duplicates ✅

Balanced categories (Models, Regions, Fuel Types all evenly distributed) ✅

🔍 Exploratory Data Analysis (EDA)
🌍 Sales by Region

Asia leads slightly (~42.9M units)

Europe & North America follow very closely (~42.4–42.5M)

Africa, Middle East, South America slightly lower (~41.5–42.3M)
➡️ BMW sales are evenly spread worldwide.

📈 Sales Trend (2010–2024)

Stable base of ~16.5–17.0M units annually.

2019 peak: ~17.2M units.

2020 dip: ~16.3M (likely pandemic impact).

2022 record high: ~17.9M.

2023 dip, followed by 2024 recovery to 17.5M.
➡️ Sales are resilient, showing recovery after global disruptions.

🔋 Fuel Type Trends

Hybrid sales growing steadily (highest in 2022 & 2024).

Electric sales rising gradually (strong in 2018, 2023).

Petrol & Diesel remain flat, showing no real growth.
➡️ BMW is shifting towards Hybrid and Electric models globally.

🚗 Model Performance

7 Series is the global best-seller (~23.8M units).

i8, X1, and 3 Series follow closely (~23.2–23.4M each).

Even the lowest (M3) sold >22M units.
➡️ BMW has a diverse portfolio; success is not dependent on one model.

💰 Price Insights

By Region: Very small variation (~$74.7k to $75.5k).

By Model: 7 Series and 3 Series highest (~$75.5k); lowest (X6) ~$74.4k.

By Engine Size: Weak correlation — some mid-size engines (2.1L, 3.6L, 4.2L) average higher prices than larger ones.
➡️ Price is consistent across regions and models; not strongly driven by engine size.

🤖 Machine Learning
Goal

Predict Sales_Classification (High vs Low).

Approach

Features used: Model, Year, Region, Color, Fuel_Type, Transmission, Engine_Size_L, Mileage_KM, Price_USD, Sales_Volume.

Model: Decision Tree Classifier (max_depth=8).

Evaluation: Accuracy, classification report, confusion matrix.

Results

Accuracy: 100%

Classification Report: Precision, Recall, F1 = 1.0 for both High and Low.

Confusion Matrix: Perfect separation between High and Low.

Feature Importance

Sales_Volume = 1.0 (100%)

All other features = 0.0

➡️ This shows Sales_Classification is completely determined by Sales_Volume (a simple threshold rule).
The model achieved 100% accuracy because of this direct relationship (target leakage).

📜 Key Takeaways

BMW maintains globally balanced sales — strong in all regions.

Hybrids and Electrics are growing, while Petrol and Diesel remain flat.

Pricing is remarkably consistent worldwide, not strongly affected by engine size.

ML results:

Perfect accuracy achieved, but only because the target (Sales_Classification) is derived from Sales_Volume.

If Sales_Volume is removed, a more realistic challenge would be predicting sales classification from factors like Model, Region, Price, and Fuel_Type.
