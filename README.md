# 🔥 Breathing Through the Smoke: Air Quality Analysis of the 2025 LA Wildfires

 How did one of the most destructive wildfires in California history 
 change the air that 4 million people breathed?

---

## 🌍 Why This Topic Matters

In January 2025, Los Angeles experienced some of the most devastating 
wildfires in its history. Beyond the destruction of homes and landscapes, 
wildfires leave an invisible but deadly legacy poisoned air.

This project uses real air quality sensor data to answer a question that 
affects millions of people:

> **"How did the January 2025 Los Angeles wildfires impact air quality 
> (PM2.5, CO, and O3) compared to Vancouver — a city unaffected by 
> wildfires — across the pre-fire (December 2024), during-fire 
> (January 2025), and post-fire (February 2025) periods?"**

By comparing Los Angeles to Vancouver (our control city), we can isolate 
the wildfire's true impact from normal seasonal variation.

---

## 📊 Data Source

All data was retrieved from the **OpenAQ API (v3)** — an open-source 
platform providing real-time and historical air quality measurements 
from sensors around the world.

- **Los Angeles Station:** ID 7936 — Los Angeles N. Mai
- **Vancouver Station:** ID 1528 — Vancouver Airport
- **Time Period:** December 2024 — February 2025

---

## 🧪 Parameters Analyzed

### 💨 PM2.5 — Fine Particulate Matter
The most dangerous pollutant produced by wildfires. These microscopic 
particles (smaller than 2.5 micrometers) penetrate deep into the lungs 
and enter the bloodstream, causing respiratory and cardiovascular damage.

**Unit:** µg/m³ | **Safe limit (WHO):** 15 µg/m³ (24-hour average)

**Our finding:** PM2.5 spiked to **109 µg/m³** in Los Angeles during 
the wildfire — more than 7x the WHO safe limit — while Vancouver 
remained below 16 µg/m³ throughout the entire period.

---

### 🏭 CO — Carbon Monoxide
Produced by the incomplete combustion of organic matter during fires. 
A colorless, odorless, and poisonous gas that reduces the blood's 
ability to carry oxygen.

**Unit:** ppm (parts per million)

**Our finding:** CO spiked to **1.40 ppm** on January 9th, 2025 — 
precisely coinciding with peak wildfire activity. This highlights 
that monthly averages can hide acute pollution events; daily analysis 
is essential for understanding wildfire impacts.

---

### ☀️ O3 — Ground-Level Ozone
Formed when wildfire smoke compounds react with sunlight. While ozone 
in the upper atmosphere protects us, ground-level ozone causes 
breathing problems and aggravates asthma.

**Unit:** ppm

**Our finding:** O3 showed no significant difference between the two 
cities or across the three periods, suggesting that ozone formation 
from wildfire smoke was not a major factor at this station during 
this period.

---

## 🗂️ Project Structure

## 🔬 Methodology

The analysis follows these steps:

1. **Data Retrieval** — OpenAQ API v3 queried using Python `requests`
2. **Data Processing** — Cleaning, filtering, and organizing into a 
   unified DataFrame using `pandas`
3. **Data Analysis** — Descriptive statistics (mean, min, max, std) 
   calculated per city, parameter, and period
4. **Visualization** — Bar charts and daily trend charts created 
   using `matplotlib`

---

## 📈 Key Findings

| Parameter | LA Peak | Vancouver Peak | Difference |
|-----------|---------|----------------|------------|
| PM2.5 | 109 µg/m³ | 15.5 µg/m³ | **7x higher** |
| CO | 1.40 ppm | 0.59 ppm | **2.4x higher** |
| O3 | 0.03 ppm | 0.03 ppm | No difference |

---

## ⚠️ Limitations

- Only one monitoring station per city was used
- Monthly averages underrepresent acute wildfire impacts —
  daily analysis is more appropriate for short-term events
- O3 data showed minimal variation, possibly due to station location
  or measurement frequency

---

## 🏁 Conclusion

The data tells a clear story: **the 2025 LA wildfires had a dramatic 
and measurable impact on air quality.** PM2.5 — the most health-critical 
pollutant — spiked to dangerous levels precisely when the fires were 
most active, while Vancouver remained unaffected, confirming that the 
pollution was caused by the wildfires and not by seasonal factors.

This analysis demonstrates the power of open air quality data in 
understanding environmental disasters and their public health impacts.

---

## 🛠️ How to Run

1. Open the notebook in Google Colab or Jupyter
2. Get a free API key from [openaq.org](https://openaq.org)
3. Replace `"your_api_key_here"` in Cell 3 with your key
4. Run all cells in order: **Runtime → Run all**

---

## 📚 Tools & Libraries

- Python 3
- `requests` — API calls
- `pandas` — data processing
- `matplotlib` — visualization
- OpenAQ API v3

---

*Data retrieved from OpenAQ — open-source air quality data platform*
*Analysis conducted as part of a university course project*
