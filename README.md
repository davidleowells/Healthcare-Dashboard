# Acme Health Spend Report (Excel Dashboard)

## Overview
An interactive healthcare spend and utilization dashboard built in Excel using **Power Query**, the **Data Model/Power Pivot**, and **PivotCharts**. The dashboard supports exploration of **medical and pharmacy allowed spend**, **utilization**, **risk segmentation**, and **enrollment dynamics** across **2019–2024**, with drilldowns by **plan** and **member demographics**.

> Note: This dashboard is powered by a **synthetic claims environment** created for portfolio demonstration (no real patient data).

## What This Demonstrates
- Building an end-to-end Excel analytics product using Power Query + Data Model
- Star-schema modeling concepts applied in Excel (dimensions, facts, relationship-driven filtering)
- KPI design for healthcare analytics (PMPM, utilization rates, mix metrics)
- Executive-ready visuals with consistent slicer behavior across pages

## Key Insights Surfaced
The dashboard is designed to surface practical, payer-style insights such as:
- **Cost trend and drivers:** PMPM trend over time with drilldowns to the **highest-impact medical conditions** and **top drug spend drivers**
- **Site-of-care opportunity:** Mix shifts across **Inpatient / Outpatient / ED / Professional** to flag potential steerage and avoidable utilization patterns
- **Network leakage:** In-network vs out-of-network allowed spend visibility to identify **OON concentration** by plan, provider system, and geography
- **ED expected mix (preventable vs non-preventable):** Expected preventable/non-preventable composition to support a utilization-management narrative (vs raw counts alone)
- **Pharmacy efficiency signals:** Generic utilization and fulfillment channel mix (e.g., mail/retail, 30/90-day) to highlight adherence and cost-containment levers
- **Population risk segmentation:** Low/medium/high risk mix views to contextualize spend changes and avoid misleading plan comparisons
- **Enrollment dynamics:** Covered member trends and churn directionality to separate **utilization change** from **membership change**
- **Geographic concentration:** State concentration and top-share views to identify where spend and membership are concentrated

## Pages Included
- **Overview:** Enrollment, high-risk count, total allowed spend, site-of-care mix, PMPM trend, top cost drivers, generic utilization, geographic distribution
- **Medical Claims:** In vs out-of-network allowed, top health systems by spend, ED expected preventable vs non-preventable mix, medical PMPM trend, inpatient admits per 1,000
- **Pharmacy Claims:** Rx PMPM trend and YoY deltas, top drug cost drivers, fulfillment/channel utilization and 90-day share
- **Demographics:** State concentration, risk mix by age band, covered members by age band, churn trend

## Data (Synthetic)
Data is synthetic and structured like a typical healthcare analytics model:
- Medical claims, pharmacy claims, eligibility/coverage episodes
- Dimensions for members, dates, plans, providers, drugs, diagnoses (ICD-10), procedures (CPT/HCPCS)
- ED classification weights used to show expected preventable vs non-preventable mix

## Metric Conventions (High-Level)
- **Allowed Amount:** Total allowed spend (medical + pharmacy), with separate medical and pharmacy measures
- **PMPM:** `Allowed Amount / Member Months`
- **Risk Segmentation:** Members grouped into low/medium/high buckets based on diagnosis presence patterns by year
- **Churn:** Month-over-month member presence trend, displayed as a rolling last-12-months view

## How to Use
1. Open the workbook in Excel (desktop).
2. Start on **Overview** and select the **year range**.
3. Use slicers to filter by:
   - Plan
   - State
   - Demographics (Sex, Age Band, Race, Ethnicity)
4. Navigate to the **Medical**, **Pharmacy**, and **Demographics** tabs for deeper drilldowns (slicer context remains consistent).

## Tools
- Excel **Power Query** for data ingestion and transformation
- Excel **Data Model / Power Pivot** for relationships and measures
- **PivotCharts** for interactive visuals
