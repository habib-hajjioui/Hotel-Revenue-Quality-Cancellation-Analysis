# Hotel Revenue Quality & Cancellation Intelligence
### City Hotel Booking Analysis — 2015 to 2017

---

## Repository Contents

| File | Description |
|------|-------------|
| `Hotel_Revenue_Quality___Cancellation_Intelligence.ipynb` | Full technical notebook — data cleaning, Python code, 14 charts, analytical reasoning, and verified revenue calculations |
| `Hotel_CEO_Executive_Report.docx` | Non-technical business report — findings, visualizations, and recommendations written for hotel management |

---

## Project Overview

This project analyzes **77,795 city hotel bookings** spanning July 2015 to August 2017 to answer a question that standard hotel reporting cannot:

> *What share of revenue the hotel books is actually earned?*

The answer is **56.9%.**

Of €25,199,012 in total booked room revenue, only **€14,348,156 was realized** from completed stays. The remaining €10.85 million — 43.1% of all booked revenue — was lost to cancellations. This loss is not random. It is structurally concentrated in specific market segments, distribution channels, behavioral profiles, and booking time windows — all detectable from data the hotel already collects.

---

## The Business Problem

Standard hotel accounting tracks three core metrics: **ADR**, **Occupancy Rate**, and **RevPAR**. These metrics measure what was booked — not what was earned. A month with 85% occupancy looks identical on a standard report whether 95% or 55% of those bookings completed.

This project introduces a fourth metric: **Realization Rate** — the share of booked room revenue that results from a completed stay. It is the filter that reveals revenue quality, not just revenue volume.

---

## Key Findings

**1 — Revenue Gap**
€25.2M booked → €14.3M realized = **56.9% realization rate**
Minimum confirmed revenue loss (No Deposit cancellations): **€7,679,386**

**2 — Non-Completion Breakdown**
- 44,935 completed stays (57.8%)
- 31,965 true cancellations (41.1%)
- 895 No-Shows (1.2%)

Cancellations and No-Shows are operationally different events requiring different policy responses.

**3 — Segment Performance**

| Segment | Realization Rate | Revenue Lost |
|---------|-----------------|-------------|
| Groups | 31.4% | €2,141,101 |
| Offline TA/TO | 57.1% | €1,915,699 |
| Online TA | 58.5% | €6,195,993 |
| Corporate | 75.5% | €118,381 |
| Direct | 78.1% | €462,914 |

**4 — Lead Time Is the Cleanest Risk Predictor**

| Lead Time | Cancellation Rate |
|-----------|-----------------|
| 0–2 days | 10.4% |
| 3–7 days | 14.7% |
| 8–30 days | 31.2% |
| 30+ days | 50.1% |

71% of all bookings fall in the highest-risk bucket.

**5 — Behavioral Predictors (all available at time of booking)**
- 1 prior cancellation → **96.6%** recancellation rate
- 0 special requests → **55.6%** cancellation rate
- 0 booking modifications → **45.9%** cancellation rate

**6 — Channel Concentration Risk**
87.5% of bookings flow through TA/TO at 45.4% cancellation.
Direct bookings: only 8% of volume, 18.8% cancellation, €278 realized revenue per attempt vs €227 for Online TA.

---

## Dataset

- **Source:** [Hotel Booking Demand Dataset — Kaggle](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand)
- **Original size:** 119,390 rows, 32 columns
- **Scope:** City Hotel only
- **Working dataset after cleaning:** 77,795 rows, 42 columns
- **Period covered:** July 2015 – August 2017

---

## Tools and Libraries

```
Python 3
pandas
numpy
matplotlib
seaborn
Google Colab
Microsoft Word (executive report)
```

---

## Project Structure

```
├── Hotel_Revenue_Quality___Cancellation_Intelligence.ipynb
│   ├── Dataset Overview & Column Definitions
│   ├── Data Cleaning (8 steps, documented with business justification)
│   ├── Feature Engineering
│   ├── Exploratory Data Analysis (14 charts)
│   ├── Deep Business Insights
│   ├── Revenue Analysis
│   ├── Key Findings
│   ├── Recommendations
│   └── Final Conclusion
│
└── Hotel_CEO_Executive_Report.docx
    ├── Executive Summary
    ├── Business Problem
    ├── Key Findings (with chart images)
    ├── Recommendations (8 actionable items)
    └── Final Conclusion
```

---

## How to Run the Notebook

1. Download `Hotel_Revenue_Quality___Cancellation_Intelligence.ipynb`
2. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand) and save it as `hotel_booking.csv`
3. Open the notebook in **Google Colab** or **Jupyter Notebook**
4. Run cells in order from top to bottom

> **Note:** The notebook was developed in Google Colab. The first cell uses `files.upload()` to load the dataset. If running locally in Jupyter, replace that cell with `pd.read_csv('hotel_booking.csv')`.

---

## Main Business Recommendations

1. **Adopt Realization Rate as a primary KPI** alongside ADR and occupancy
2. **Prioritize Direct booking growth** — €50.66 more realized revenue per attempt than Online TA
3. **Reform Group booking policy** — require deposits for bookings made 30+ days in advance
4. **Reduce TA/TO channel dependency** — 87.5% concentration in the highest-cancellation channel is a structural risk
5. **Implement lead-time-tiered cancellation policies** — 0–7 days flexible, 30+ days non-refundable deposit
6. **Flag high-risk bookings** using the five behavioral predictors already available in PMS data
7. **Reframe Corporate** as an occupancy stabilizer, not a high-revenue growth target
8. **Track No-Shows separately** and calibrate overbooking policy using the 1.2% baseline rate

---

## Author

**Habib**
Economics & Finance — Cadi Ayyad University, Marrakech
Business Intelligence & Data Analysis Portfolio Project
Internship — City Hotel


---

*All numbers in this project are verified through Python code. Every business interpretation is grounded in data. Claims based on assumptions are labeled as such.*
