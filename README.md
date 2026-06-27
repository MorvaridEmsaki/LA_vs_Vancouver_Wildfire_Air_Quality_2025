# LA_vs_Vancouver_Wildfire_Air_Quality_2025
---

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
