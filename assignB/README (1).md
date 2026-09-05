# Marketing Data Analysis

## Assignment B — Marketing Data Analysis

**Candidate ID:** B211623

## Project Overview

This project analyzes physician marketing outreach data for a healthcare company. The objective is to understand marketing effectiveness using three core metrics:

- **Reach** — number of unique physicians reached
- **Frequency** — average number of activity-log records per unique physician
- **Engagement** — Open + Click activity records

The analysis is segmented by Communication Source, Channel, Month, and source/channel monthly trends.

## Business Questions

1. How many unique physicians were reached?
2. How frequently were physicians represented in the activity logs?
3. How much engagement was generated?
4. Which communication sources have the largest reach?
5. Which channels generate stronger engagement?
6. How do metrics change month over month?
7. What opportunities exist to improve campaign effectiveness and data quality?

## Dataset

Source file: `Marketing Data - Hiring.xlsx`

Key fields include:

| Column | Purpose |
|---|---|
| `Physician ID` | Unique physician identifier |
| `Communication Source` | Marketing/source system |
| `Source Channel Name` | Communication channel |
| `Therapeutic Area` | Therapeutic area |
| `Device` | Device category |
| `Source Device Name` | Detailed device/source information |
| `Activity` | Event type such as Sent, Open, Click, Bounce |
| `Count of Activity Metrics` | Activity metric count |
| `Activity Date` | Activity date |

## Methodology

### Reach
**Reach = unique `Physician ID` count**

### Frequency
**Frequency = Total Activity Records / Unique Physicians**

This is an **activity-log frequency** metric. Since rows contain events such as Sent, Delivered, Open and Click, it should not be interpreted as the exact number of contacts received by each physician.

### Engagement
**Engagement = Open + Click activity records**

Open and Click were treated as positive physician interactions.

### Engagement Rate
**Engagement Rate = Engagement / Total Activity Records**

This is a descriptive activity-level rate, not a standard email open rate or click-through rate.

### Negative / Quality Signals

Bounces, hard bounces and unsubscribes are reported separately as communication-quality signals.

## Key Results

| Overall Metric | Result |
|---|---:|
| Unique Physician Reach | 25,208 |
| Total Activity Records | 100,040 |
| Frequency | 3.97 |
| Engagement | 18,521 |
| Engagement Rate | 18.5% |
| Unique Engaged Physicians | 9,461 |
| Unsubscribes | 65 |
| Bounces + Hard Bounces | 4,595 |

### Communication Source

- Internal CRM Tool has the largest reach: **12,647 physicians**.
- Sales Reps reach **7,420 physicians**.
- Medspace360 reaches **7,388 physicians**.
- Remission Report reaches **3,133 physicians**.
- Oncopulse reaches **1,848 physicians**.
- The results show a scale-versus-engagement trade-off across sources.

### Channel

- Email has the broadest reach: **22,092 physicians**.
- Email Alert reaches **7,388 physicians**.
- SMS reaches **1,848 physicians**.
- SMS shows the strongest engagement rate among the channels.

### Monthly Trend

- January has the highest monthly reach: **23,480 physicians**.
- March has the highest activity volume and frequency.
- Reach and activity volume do not necessarily peak in the same month.

> Monthly reach values are not additive because the same physician may appear in multiple months.

## Recommendations

1. **Use Email for broad reach** — Email is the strongest channel for reaching a large physician audience.
2. **Use SMS selectively** — Apply SMS to targeted, high-priority or time-sensitive communication.
3. **Balance scale with engagement** — Evaluate sources on both reach and interaction quality.
4. **Monitor frequency** — Avoid excessive communication and potential audience fatigue.
5. **Investigate bounce records** — Improve contact-data quality and deliverability.
6. **Improve data completeness** — `Count of Activity Metrics` is incomplete and should be improved in future reporting.

## Assumptions

- Reach uses distinct `Physician ID`.
- Frequency uses activity-log records divided by unique physicians.
- Engagement uses `Open` and `Click`.
- `Count of Activity Metrics` is not the primary engagement metric because it is incomplete.
- Segment-level reach is not additive because physicians may occur across multiple segments.
- Bounce and unsubscribe events are treated as negative/quality signals.

## Project Files

### Excel
`Marketing_Data_Analysis_B211623.xlsx`

Sheets include:
- Executive Dashboard
- Cleaned Data
- Overall KPI
- By Source
- By Channel
- By Month
- Source × Month
- Channel × Month
- Activity Mix
- Data Quality
- Methodology

### PowerPoint
`Marketing_Data_Analysis_B211623.pptx`

The presentation covers the executive summary, metric definitions, source/channel comparisons, monthly trends, data quality, recommendations and conclusion.

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- OpenPyXL
- Excel
- PowerPoint

## Analysis Workflow

```text
Raw Marketing Data
        ↓
Data Inspection & Cleaning
        ↓
Date Transformation
        ↓
Metric Definition
        ↓
Reach / Frequency / Engagement
        ↓
Source / Channel / Month Segmentation
        ↓
Trend & Data Quality Analysis
        ↓
Business Recommendations
        ↓
Excel Dashboard + PowerPoint
```

## Conclusion

The analysis shows a clear trade-off between **reach and engagement**. Email provides the broadest physician reach, while SMS demonstrates stronger engagement potential. January leads in reach, while March generates the highest activity intensity.

The recommended strategy is to maintain Email for broad reach, use SMS selectively for high-value engagement opportunities, monitor communication frequency, and improve activity and contact-data quality.

---

**Candidate ID:** B211623
