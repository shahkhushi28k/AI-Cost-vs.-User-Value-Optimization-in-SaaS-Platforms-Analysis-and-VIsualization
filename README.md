# AI Cost vs. User Value Optimization in SaaS Platforms

**Khushi Shah**

---

## Project Overview

As SaaS platforms increasingly integrate generative AI capabilities, balancing inference cost with delivered user value has become a critical business challenge. AI features introduce variable compute expenses, making it essential to understand how usage behavior translates into revenue, retention, and profitability.

This project develops interactive visual analytics dashboards to evaluate AI usage, modeled compute cost, churn behavior, and revenue contribution. The goal is to support data-driven decisions related to pricing strategy, feature investment, and AI cost optimization within a SaaS environment.

The dashboard integrates temporal, geospatial, categorical, and structural perspectives to provide both executive-level summaries and detailed drill-down analysis.

---

## Prior Work and Context

Research in AI economics highlights the importance of monitoring cost-to-value dynamics when deploying generative AI at scale (Gartner, 2023). Visualization theory further emphasizes aligning analytic views with stakeholder decision needs (Munzner, 2014).

Building on these principles, this project models AI cost relative to user engagement and subscription revenue, translating analytical insights into stakeholder-focused dashboard views.

---

## Stakeholder Groups

Different organizational roles require distinct analytical perspectives:

- **Product Managers** – Evaluate engagement sustainability and retention patterns  
- **Finance Teams** – Assess cost-to-value performance and profitability  
- **Engineering Teams** – Monitor compute load and high-usage clusters  
- **Leadership / Executives** – Review overall AI investment efficiency and regional performance  

---

## Stakeholder Insight Needs

Each stakeholder’s decision-making needs directly informed the dashboard structure:

- **Product** → Adoption trends, retention stability, churn behavior  
  - Supported through temporal trend charts and engagement segmentation views  

- **Finance** → Revenue growth, modeled compute cost, cost-to-value ratios  
  - Supported through KPI cards and subscription plan comparisons  

- **Engineering** → Compute-heavy user clusters and usage intensity patterns  
  - Supported through clustering and structural analysis views  

- **Leadership** → Geographic revenue concentration and regional churn risk  
  - Supported through geospatial maps and regional comparison dashboards  

---

## Data Acquisition

This project uses the **Customer Subscription, Churn & Usage Patterns** dataset from Kaggle.

The dataset includes:

- Subscription plan information  
- Usage intensity metrics  
- Churn indicators  
- Regional attributes  

Ideally, inference-level compute costs and feature-level revenue allocation would be included. However, such operational and infrastructure-level data are typically proprietary and not publicly accessible. Therefore, AI compute cost was modeled based on usage intensity.

**Dataset source:**  
https://www.kaggle.com/datasets/jayjoshi37/customer-subscription-churn-and-usage-patterns

---

## Data Description and Preparation

The dataset contains user-level subscription, usage, and churn records across 2,800 users.

### Key Attributes

- Subscription tier (Basic, Standard, Premium)  
- Weekly usage hours  
- Churn status  
- Support tickets  
- Payment failures  
- Region  

### Data Preparation Steps

- Validation and cleaning performed using **Python (Pandas)**  
- Checked for missing values and inconsistencies  
- Modeled AI compute cost proportionally to usage intensity  
- Generated derived metrics:
  - Cost-to-value ratio  
  - Modeled revenue  
  - Profitability segments  

Because direct AI infrastructure metrics were unavailable, cost modeling assumptions were explicitly documented and validated for logical consistency.


---

# Visualizations

---

## 1️⃣ Overall Summary Dashboard

### 📊 Overall Dashboard

![Overall Dashboard](images/overall_dashboard.png)

### Overview

The Overall Summary Dashboard provides a comprehensive, executive-level view of AI usage and cost–value performance across the SaaS platform. It integrates financial, engagement, and operational metrics into a single consolidated interface, allowing stakeholders to quickly assess platform health and strategic alignment between AI investment and user value.

This dashboard is designed primarily for Finance, Product, and Leadership teams who require high-level performance visibility before diving into detailed drill-down analysis.

---

### Purpose

The primary objective of this dashboard is to evaluate whether AI-driven engagement is generating sustainable revenue relative to modeled compute cost. It enables stakeholders to monitor:

- Growth in revenue and user base  
- Stability of engagement over time  
- Churn trends  
- Cost-to-value alignment across subscription tiers  

It acts as the starting point for decision-making before moving to deeper feature, regional, or network analysis.

---

## Key Components and Interpretation

---

### 1️⃣ KPI Cards (Top Section)

The top section contains summary performance indicators:

- **Total Subscription Revenue (USD)** – Measures total revenue generated across all plans.
- **Total Modeled AI Compute Cost (USD)** – Represents estimated AI inference cost based on usage intensity.
- **Total Active Users (Count)** – Indicates user engagement scale.
- **Overall Churn Rate (%)** – Shows percentage of users who left the platform.

#### What This Depicts

These KPIs provide a snapshot of platform scale, profitability pressure, and retention health.

#### How It Helps

- Finance can quickly compare revenue versus modeled AI cost.
- Leadership can assess whether churn levels threaten long-term sustainability.
- Product can evaluate whether user growth aligns with revenue expansion.

#### How to Extract Insights

- Compare revenue growth against compute cost growth.
- Monitor churn relative to active user trends.
- Identify early warning signals if cost grows faster than revenue.

---

### 2️⃣ Subscription Revenue by Month (Bar Chart)

This bar chart displays monthly revenue trends over the selected time period.

#### What This Depicts

- Revenue growth trajectory  
- Acceleration or slowdown patterns  
- Seasonal fluctuations  

#### How It Helps

- Supports revenue forecasting and financial planning.
- Identifies periods of strong monetization.
- Helps evaluate impact of pricing changes or AI feature launches.

#### How to Extract Insights

- Look for steady upward trends (indicating sustainable growth).
- Identify sudden spikes or dips.
- Compare revenue growth rate to user growth rate for efficiency analysis.

---

### 3️⃣ Active Users by Month (Line Chart)

This line chart visualizes monthly active user growth over time.

#### What This Depicts

- Engagement expansion
- Platform adoption rate
- Retention stability

#### How It Helps

- Product teams assess whether engagement is increasing.
- Detects plateauing or declining adoption early.
- Helps validate marketing or feature launch impact.

#### How to Extract Insights

- Compare slope of user growth to revenue slope.
- If users grow but revenue stagnates → monetization inefficiency.
- If revenue grows without user growth → possible pricing optimization.

---

### 4️⃣ Revenue Contribution by Subscription Plan (Bar Chart)

This chart compares revenue generated by Basic, Standard, and Premium plans.

#### What This Depicts

- Revenue concentration across tiers
- High-performing subscription segments
- Revenue dependency risk

#### How It Helps

- Finance can evaluate profitability by tier.
- Product can assess which plans drive value.
- Leadership can determine reliance on premium segments.

#### How to Extract Insights

- Identify dominant revenue tier.
- Assess whether lower tiers underperform.
- Evaluate whether premium concentration creates risk or stability.

---

### Strategic Value of the Overall Dashboard

By combining financial, engagement, and cost metrics, this dashboard provides a unified cost-to-value overview. It allows stakeholders to:

- Align AI investment with measurable business outcomes  
- Detect imbalance between compute cost and revenue  
- Identify early retention risks  
- Support pricing and feature optimization decisions  

This page serves as the analytical foundation for deeper exploration in the Feature, Regional, and Network dashboards.

#### Geographic Revenue / User Distribution Map

Visualizes global distribution of users or revenue concentration.

Supports Leadership in:
- Market expansion decisions  
- Regional investment prioritization  

---

## 2️⃣ Feature / Category Analysis Page  
*(Engagement and User Behavior Analysis)*

![Feature Analysis Dashboard](images/feature_dashboard.png)

---

### Overview

The Feature / Category Analysis Page provides a detailed behavioral breakdown of user engagement, compute cost concentration, churn risk, and revenue decomposition across subscription tiers. Unlike the Overall Dashboard, which focuses on aggregated performance, this page dives into segment-level performance to understand *why* certain tiers generate more revenue or experience higher churn.

This view is especially valuable for Product, Finance, and Engineering teams seeking to identify high-impact behavioral drivers of cost-value imbalance.

---

### Purpose

The primary objective of this dashboard is to analyze how user engagement intensity translates into AI compute cost, revenue generation, and churn behavior across different subscription categories.

It enables stakeholders to:

- Detect compute-heavy user segments  
- Evaluate profitability by subscription tier  
- Identify engagement-driven churn risks  
- Understand revenue decomposition by user tenure and status  

---

## Key Components and Interpretation

---

### 1️⃣ Usage Intensity and Compute Cost by Plan (Bar + Line Chart)

This visualization combines:

- **Bar Chart** → Modeled AI Compute Cost by subscription plan  
- **Line Chart** → Average weekly usage intensity  

#### What This Depicts

- The relationship between engagement intensity and AI cost  
- Which subscription plans consume the most compute resources  
- Cost concentration across tiers  

#### How It Helps

- Engineering can identify compute-heavy tiers.
- Finance can compare cost intensity against revenue contribution.
- Product can evaluate whether higher engagement translates into sustainable value.

#### How to Extract Insights

- Identify plans where usage is high but revenue is not proportionally higher.
- Detect inefficient segments where compute cost outweighs value.
- Evaluate whether premium tiers justify their higher cost footprint.

---

### 2️⃣ Revenue Decomposition by Plan, Churn Status, and Tenure (Table)

This section breaks revenue into:

- Active vs Churned Users  
- Tenure greater than 12 months  
- Subscription tier (Enterprise, Professional, Starter)

#### What This Depicts

- Revenue stability by user lifecycle stage  
- Contribution of long-tenured users  
- Revenue loss from churned users  

#### How It Helps

- Finance can quantify churn-related revenue loss.
- Product can assess retention impact on long-term profitability.
- Leadership can evaluate revenue dependency on mature users.

#### How to Extract Insights

- Compare revenue from active vs churned users.
- Analyze whether long-tenured users contribute disproportionately.
- Identify plans where churn significantly impacts revenue stability.

---

### 3️⃣ Revenue and Churn Trends Over Time (Dual-Axis Chart)

This visualization combines:

- Revenue by subscription tier (bar)
- Churn rate trend (line)

#### What This Depicts

- Revenue growth across Enterprise and Professional plans
- Churn trajectory over time
- Relationship between monetization and retention

#### How It Helps

- Reveals whether increasing revenue coincides with improved retention.
- Helps detect retention deterioration despite revenue growth.
- Supports forecasting long-term sustainability.

#### How to Extract Insights

- If revenue increases while churn decreases → healthy growth.
- If revenue increases but churn remains high → acquisition-heavy strategy.
- If churn rises during revenue growth → potential engagement quality issues.

---

### Strategic Value of the Feature Analysis Page

This dashboard transitions analysis from macro-level performance to behavioral and segment-level drivers of cost and value. It enables stakeholders to:

- Identify profitability imbalances across tiers  
- Detect compute-heavy but low-value segments  
- Understand churn’s financial impact  
- Optimize pricing and feature allocation strategies  

By revealing how engagement intensity affects both cost and retention, this page forms the analytical bridge between financial performance and user behavior.

## 3️⃣ Regional Usage and Churn Distribution Page

![Regional Dashboard](images/regional_dashboard.png)

---

### Overview

The Regional Usage and Churn Distribution Page analyzes geographic variations in AI demand, revenue concentration, engagement intensity, and churn risk. Unlike the previous dashboards that focus on behavioral and financial segmentation, this view introduces spatial analysis to understand how AI value and cost dynamics differ across global markets.

This page primarily supports Leadership, Strategy, and Infrastructure planning teams.

---

### Purpose

The primary objective of this dashboard is to identify regional imbalances in revenue generation, compute intensity, and churn behavior.

It enables stakeholders to:

- Detect high-demand geographic markets  
- Evaluate regional profitability and churn risk  
- Support infrastructure allocation decisions  
- Identify expansion opportunities and underperforming regions  

---

## Key Components and Interpretation

---

### 1️⃣ KPI Cards (Top Section)

- **Highest Revenue Region (USD)**  
- **Highest Churn Region (%)**  
- **Highest Usage Intensity Region (Count)**  

#### What This Depicts

These KPIs quickly identify geographic concentration of:

- Revenue dominance  
- Retention risk  
- Engagement intensity  

#### How It Helps

- Leadership can assess geographic dependency risk.
- Strategy teams can identify high-growth markets.
- Infrastructure teams can prioritize resource scaling.

#### How to Extract Insights

- If one region dominates revenue → concentration risk.
- If high-usage region also has high churn → engagement sustainability issue.
- If high churn appears in lower-revenue regions → possible pricing misalignment.

---

### 2️⃣ Total Subscription Revenue by Region (Bubble Map)

This map visualizes revenue contribution geographically using bubble size to represent revenue magnitude.

#### What This Depicts

- Revenue concentration zones  
- Market penetration strength  
- Geographic monetization footprint  

#### How It Helps

- Identifies core revenue markets.
- Reveals underserved or low-performing regions.
- Supports regional pricing and investment strategies.

#### How to Extract Insights

- Compare bubble size distribution across continents.
- Identify regions with moderate usage but low revenue.
- Detect expansion potential in emerging markets.

---

### 3️⃣ Revenue per Active User by Region (Horizontal Bar Chart)

This chart compares average revenue per active user across regions.

#### What This Depicts

- Monetization efficiency by geography  
- Revenue yield per engaged user  
- Regional pricing effectiveness  

#### How It Helps

- Finance can assess pricing strategy efficiency.
- Strategy teams can identify premium-value markets.
- Leadership can evaluate region-specific profitability.

#### How to Extract Insights

- Regions with high users but low revenue per user → under-monetization.
- Regions with high revenue per user → strong pricing power.
- Compare revenue efficiency against churn trends.

---

### 4️⃣ Average Weekly Usage Intensity by Region (Bar Chart)

This visualization measures engagement intensity geographically.

#### What This Depicts

- AI demand variation by region  
- Compute-heavy markets  
- Engagement depth differences  

#### How It Helps

- Engineering can anticipate infrastructure scaling needs.
- Strategy can identify high-engagement emerging markets.
- Product can evaluate feature adoption geographically.

#### How to Extract Insights

- High usage but low revenue → cost pressure risk.
- High usage and high revenue → premium engagement markets.
- Low usage but high churn → disengagement issue.

---

### 5️⃣ Churn Rate by Region (Bar Chart)

Displays churn rate comparison across geographic segments.

#### What This Depicts

- Retention stability differences  
- Regional customer satisfaction signals  
- Risk-prone markets  

#### How It Helps

- Product teams identify localized retention challenges.
- Strategy teams adjust regional engagement initiatives.
- Leadership monitors geographic sustainability risk.

#### How to Extract Insights

- High churn in high-revenue region → urgent intervention needed.
- Low churn + high revenue → stable growth market.
- High churn + low usage → engagement or support problem.

---

### Strategic Value of the Regional Dashboard

This dashboard adds a spatial intelligence layer to cost-value analysis. It allows the organization to:

- Balance global AI infrastructure allocation  
- Identify geographic revenue concentration risks  
- Detect retention instability early  
- Support region-specific pricing and growth strategies  

By combining revenue, engagement, and churn geographically, stakeholders can align global expansion with sustainable AI cost-value optimization.

---

# 4️⃣ Network Structure Page

![Network Dashboard](images/network_dashboard.png)

---

### Overview

The Network Structure Page explores structural relationships between subscription tiers, engagement intensity levels, and churn behavior. Unlike traditional categorical dashboards, this view visualizes interconnected segments to reveal hidden dependencies and behavioral clusters that influence cost-value performance.

This page primarily supports Engineering, Product, and Advanced Analytics teams.

---

### Purpose

The primary objective of this dashboard is to uncover structural relationships that are not visible through isolated charts.

It enables stakeholders to:

- Identify high-cost engagement clusters  
- Detect churn-linked behavioral segments  
- Understand interdependencies between subscription plans  
- Reveal concentration of compute-heavy users  

---

## Key Components and Interpretation

---

### 1️⃣ Clustered Network Visualization

This network graph connects:

- Subscription tiers  
- Usage intensity segments  
- Churn groups  

Node size represents engagement or revenue magnitude, while link strength represents behavioral association or transition probability.

#### What This Depicts

- High-impact behavioral clusters  
- Relationships between usage intensity and churn  
- Structural segmentation patterns  

#### How It Helps

- Engineering identifies compute-intensive clusters.
- Product detects engagement-to-churn relationships.
- Finance evaluates structural profitability risks.

#### How to Extract Insights

- Dense clusters around high-usage nodes → cost concentration.
- Strong links between high usage and churn → engagement fatigue risk.
- Isolated clusters → niche but stable segments.

---

### Strategic Value of the Network Dashboard

This dashboard shifts analysis from descriptive to structural insight. Instead of asking *which tier performs best*, it asks:

- How are behaviors connected?
- Where are cost-risk clusters forming?
- Which segments influence overall churn?

By revealing structural interdependencies, this page supports proactive optimization of AI cost allocation and engagement strategy.

---

---

# 5️⃣ Interpretation of Results

The analysis reveals several important insights regarding AI cost-value optimization within the SaaS platform.

Premium plans generated the highest modeled revenue, despite subscription tiers being nearly evenly distributed across users (Premium 34%, Standard 33%, Basic 33%). This indicates that higher-tier pricing plays a significant role in revenue concentration, even without dominant user share.

Churn was relatively high, with 1,605 of 2,800 users leaving the platform. This level of attrition presents sustainability risk, particularly if compute cost continues to scale with engagement.

Although weekly usage ranged from 0.5 to 25 hours, higher usage did not consistently improve retention. In several segments, heavy usage was associated with increased churn risk, suggesting that usage intensity alone does not guarantee user satisfaction or long-term stability.

Longer-tenured and recently active users demonstrated greater retention stability, while higher volumes of support tickets and payment failures were more frequently associated with churned users. This indicates that retention is more strongly influenced by engagement quality, customer experience, and operational friction than by raw usage volume.

---

## Key Strategic Insights

- Revenue concentration is driven more by pricing structure than user distribution.
- High churn weakens long-term cost-value sustainability.
- Usage intensity increases compute cost but does not automatically improve retention.
- Customer experience signals (support issues, payment failures) are stronger predictors of churn than engagement duration alone.
- AI cost optimization should focus on improving engagement quality rather than simply increasing usage.

These findings reinforce the importance of aligning AI infrastructure investment with retention strategy, pricing design, and customer experience optimization.

---
