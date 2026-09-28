# 🔬 Analysis Methodology

## Project: Retail Sales Performance Dashboard
**Author**: Shanmukha Sree Bendi | Business Intelligence Project | 2026

---

## 1. Dataset Overview

| Field | Detail |
|-------|--------|
| Total Records | 50 orders |
| Period | January 2026 – April 2026 |
| Regions | West, East, Central, South |
| Categories | Technology, Furniture, Office Supplies |
| Segments | Corporate, Consumer, Home Office |

### Fields Captured
- Order ID, Order Date, Ship Date
- Region, State, City
- Category, Sub-Category, Product Name
- Sales, Quantity, Discount, Profit
- Customer Name, Segment

---

## 2. Data Preparation

### Steps Applied
1. **Date formatting** — Converted Order Date to monthly periods for trend analysis
2. **Revenue calculation** — Verified Sales figures across all 50 orders
3. **Profit margin formula** — `Profit Margin % = (Profit / Sales) × 100`
4. **Discount impact analysis** — Compared margin across discount tiers (0%, 10%, 15%, 20%)
5. **Category aggregation** — Grouped by Technology, Furniture, Office Supplies
6. **Regional segmentation** — Grouped by West, East, Central, South for geographic analysis
7. **Performance classification** — Tagged products as Top / Review / Underperforming based on margin thresholds

---

## 3. DAX-Equivalent Measures

The following measures were implemented as JavaScript equivalents of Power BI DAX formulas:

### Total Revenue
```
Total Revenue = SUM(Orders[Sales])
Result: $32,847
```

### Total Profit
```
Total Profit = SUM(Orders[Profit])
Result: $6,914
```

### Profit Margin %
```
Profit Margin % = DIVIDE(SUM(Orders[Profit]), SUM(Orders[Sales]), 0) * 100
Result: 21.1%
```

### Average Order Value
```
Avg Order Value = DIVIDE(SUM(Orders[Sales]), COUNT(Orders[Order ID]), 0)
Result: $656.94
```

### Average Discount
```
Avg Discount = AVERAGE(Orders[Discount]) * 100
Result: 8.2%
```

---

## 4. Visualization Design

### Dashboard Components

| Visual | Data Used | Business Purpose |
|--------|-----------|-----------------|
| KPI Cards | Sales, Profit, Orders, Discount | At-a-glance performance summary |
| Monthly Trend (Bar+Line) | Sales + Profit by month | Track revenue growth over time |
| Category Donut | Sales by Category | Revenue contribution split |
| Region Bar Chart | Sales by Region | Geographic performance ranking |
| Segment Pie | Sales by Customer Segment | Customer type profitability |
| Margin Progress Bars | Profit/Sales by Category | Category efficiency comparison |
| Product Table | SKU-level analysis | Identify top and bottom performers |

### Interactive Features
- **Region filter** — All visuals respond to region selection dynamically
- **Hover tooltips** — Dollar values shown on all chart interactions
- **Performance badges** — ⭐ Top / ⚠️ Review / ❌ Underperform classification

### Design Principles
- Clean white background — mimics professional Power BI report theme
- Consistent color coding by region and category
- Business-friendly layout — KPIs at top, details below
- Mobile responsive — works on all screen sizes

---

## 5. Performance Classification Criteria

| Classification | Margin Threshold | Discount Level |
|---------------|-----------------|----------------|
| ⭐ Top Performer | > 20% margin | < 10% discount |
| ⚠️ Needs Review | 10–20% margin | 10–15% discount |
| ❌ Underperforming | < 12% margin | > 15% discount |

---

## 6. Key Analytical Findings

### Revenue Distribution
- Technology: $16,342 (49.8% of total)
- Furniture: $11,562 (35.2% of total)
- Office Supplies: $4,943 (15.0% of total)

### Margin Analysis
- Best margin: Office Supplies at 43.9%
- Worst margin: Furniture at 14.5%
- Margin gap: 29.4 percentage points between best and worst

### Discount Impact
- Products with 0% discount avg margin: 22%
- Products with 20% discount avg margin: 11%
- Discount correlation: Every 5% increase in discount reduces margin by ~5.5pts

---

## 7. Business Recommendations

1. **Cap furniture discounts at 10%** — Would improve furniture margin from 14.5% to ~19%
2. **Expand Technology range** — Highest revenue + good margin + low discount dependency
3. **Bundle Office Supplies with Technology** — Increase basket size while maintaining margin
4. **Focus West and Central regions** — Highest order volume and Technology demand
5. **Review South region strategy** — Fewest orders (8), highest discount rate (10.2%)

---

*Methodology Document | Shanmukha Sree Bendi | Business Intelligence Project | 2026*
