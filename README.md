# Airbnb Price & Scenario Analysis

## Power BI Project

An interactive Power BI dashboard for analysing Airbnb listings in Antwerp and exploring listing performance under different pricing and occupancy scenarios.

**Author:** Vinod Pulickal  
**Project Date:** 15/09/2026

---

## 1. Project Overview

The **Airbnb Price & Scenario Analysis** project uses Power BI to analyse Airbnb listing data and explore potential revenue outcomes under different occupancy and seasonal pricing assumptions.

The dashboard provides interactive analysis of:

- Listing and pricing performance
- Availability
- Reviews
- Potential revenue
- Projected revenue under different occupancy assumptions
- Seasonal pricing adjustments
- Individual listing-level details

The project uses Power BI features including slicers, What-If parameters, bookmarks, dynamic analysis, custom tooltips and drill-through.

---

## 2. Project Objective

The objective is to create an interactive Power BI dashboard for Airbnb listings in Antwerp that:

1. Provides a high-level overview of listing performance.
2. Analyses listings by location, price distribution and listing characteristics.
3. Allows users to explore revenue scenarios using occupancy and seasonal pricing assumptions.
4. Provides listing-level details through drill-through analysis.
5. Demonstrates interactive Power BI reporting and DAX-based scenario calculations.

---

## 3. Report Pages

### Overview

The Overview page provides a high-level summary using KPI cards and interactive slicers.

**KPI cards:**

- Average Price
- Availability Rate
- Total Listings
- Projected Revenue

**Slicers:**

- Date Range
- Property Type
- Room Type
- Occupancy Rate
- Seasonal Multiplier

**Bookmarks:**

- Default View
- 100% Occupancy

---

### Listing Analysis

The Listing Analysis page focuses on listing-level and market analysis.

It includes:

- Listings by Location map
- Price Distribution
- Top 10 Listings by Reviews
- Dynamic Average Price analysis
- Property Type / Room Type selection using a field parameter
- Custom tooltip interaction

---

### Scenario Insights

The Scenario Insights page allows users to evaluate different pricing and occupancy assumptions.

It includes:

- Occupancy Rate scenario selector
- Seasonal Multiplier scenario selector
- Average Price vs Scenario Price
- Potential Revenue vs Projected Revenue
- Projected Revenue Trend by Month
- Scenario Listing Details

---

### Listing Details

The Listing Details page is a drill-through page for individual listings.

It provides:

- Listing name
- Average Price
- Scenario Price
- Total Reviews
- Projected Revenue
- Average Host Age
- Room type
- Property type
- Accommodates
- Bedrooms
- Beds
- Bathrooms
- Location map

A Back button allows users to return to the originating report page.

---

### Listing Tooltip

A custom tooltip provides additional information when users hover over a listing.

The tooltip displays:

- Listing Name
- Average Price
- Total Reviews
- Projected Revenue

---

## 4. Data Sources

The project uses four primary source datasets:

- `calendar.csv`
- `hosts.csv`
- `listings.csv`
- `reviews.csv`

The Power BI data model connects listing, calendar, host and review information.

### Main Data Tables

**Listings**

Contains listing-level information including property type, room type, location, accommodation capacity and host information.

**Calendar**

Contains listing-day level information including date, availability, price and minimum/maximum nights.

**Hosts**

Contains host information including host ID, host name, host location and host registration date.

**Reviews**

Contains review information linked to individual listings.

---

## 5. Data Model

The Power BI model uses relationships between the major tables to support listing, availability, review, host and revenue analysis.

Key relationships include:

- Listings → Calendar
- Listings → Reviews
- Hosts → Listings
- Date → Calendar
- Date → Reviews

A dedicated Date table is used for time-based analysis.

A dedicated **DAX Measures** table stores the report measures.

---

## 6. Key DAX Measures

The project includes measures for listing performance, reviews, pricing, availability, revenue and scenario analysis.

Examples include:

- Total Listings
- Total Reviews
- Average Price
- Available Days
- Total Calendar Days
- Availability Rate
- Reviews per Listing
- Listings with Reviews
- Listings with Reviews %
- Potential Revenue
- Potential Revenue per Listing
- Projected Revenue
- Scenario Price
- Average Host Age
- Occupancy Rate Final

The measures respond dynamically to report filters and scenario selections.

---

## 7. What-If Scenario Analysis

Two What-If parameters are used.

### Occupancy Rate

The Occupancy Rate parameter allows users to change the assumed occupancy percentage.

The current parameter uses:

- Minimum: 0%
- Maximum: 100%
- Increment: 5%
- Default: 50%

### Seasonal Multiplier

The Seasonal Multiplier allows users to simulate changes in pricing.

The current parameter uses:

- Minimum: 50
- Maximum: 200
- Increment: 5
- Default: 100

### Scenario Logic

Projected Revenue is calculated using the potential revenue, selected occupancy rate and selected seasonal multiplier.

Scenario Price is calculated by applying the seasonal multiplier to Average Price.

These calculations allow users to compare different assumptions interactively.

---

## 8. Power BI Interactive Features

The project demonstrates the following Power BI functionality:

- Interactive slicers
- What-If parameters
- KPI cards
- Bookmarks
- Dynamic field parameters
- Map visualisation
- Price distribution analysis
- Top N filtering
- Custom tooltips
- Drill-through
- Listing-level analysis
- Monthly trend analysis

---

## 9. Testing & Validation

The report was tested for:

- Overview KPI functionality
- Default report state
- Occupancy scenario calculations
- Seasonal multiplier calculations
- Scenario price calculations
- Dynamic slicer behaviour
- Drill-through functionality
- Custom tooltip behaviour
- Bookmark functionality
- Data model relationships
- Visual and page errors
- Final model cleanup

The main calculations and interactive features were validated to ensure that scenario selections update the report correctly.

A formal Power BI Performance Analyzer benchmark was not performed. The optimization review focused on model organization, visual design, calculation structure and functional validation.

---

## 10. Repository Structure

```text
airbnb-price-scenario-analysis/
│
├── README.md
│
├── PowerBI/
│   └── Airbnb_Price_Scenario_Analysis.pbix
│
├── Data/
│   ├── calendar.csv
│   ├── hosts.csv
│   ├── listings.csv
│   └── reviews.csv
│
└── Documentation/
    └── PROJECT DOCUMENTATION.docx
```

## 11. How to Use the Dashboard

1. Open the Power BI `.pbix` file in Power BI Desktop.
2. Start with the **Overview** page.
3. Use the slicers to filter the analysis.
4. Adjust Occupancy Rate and Seasonal Multiplier to test scenarios.
5. Use the bookmarks to return to the default scenario or test 100% occupancy.
6. Explore the **Listing Analysis** page for location, pricing and top-listing analysis.
7. Use the **Scenario Insights** page to compare potential and projected revenue.
8. Select a listing and use drill-through to open **Listing Details**.
9. Hover over listings in supported visuals to view the custom tooltip.

---

## 12. Project Documentation

Detailed project documentation is provided separately and covers:

- User Guide
- Data Model & Relationships
- DAX Measures & Calculations
- What-If Parameters & Scenario Setup
- Report Pages & Interactive Features
- Testing & Validation
- Performance Optimization & Report Design
- Project Deployment & GitHub Submission

---

## 13. Project Status

The Power BI report has been completed, tested and cleaned up for project submission.

The project is intended for **GitHub submission** and does not rely on Power BI Service deployment or scheduled refresh.

---

## Author

**Vinod Pulickal**

*Airbnb Price & Scenario Analysis — Power BI Project*
