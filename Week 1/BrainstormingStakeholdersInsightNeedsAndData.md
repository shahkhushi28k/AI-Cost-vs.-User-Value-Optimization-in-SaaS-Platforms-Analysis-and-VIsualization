# 📅 Week 1 – Brainstorming Stakeholders, Insight Needs, and Data

## Problem Definition

In Week 1, I defined the core problem for my visualization project: **AI Cost vs. User Value Optimization in SaaS Platforms**.

As SaaS platforms integrate generative AI features, inference and compute costs continue to rise. However, not all AI features or usage patterns generate sufficient value to justify these costs. I identified the central challenge as determining which features and user behaviors produce sustainable return on investment and which drive unsustainable cost growth.

Understanding this trade-off is critical for making informed decisions about:
- Feature investment
- Pricing tiers
- Usage limits
- Infrastructure allocation

---

## Analytical Dimensions

To fully explore the problem, I structured the analysis across multiple analytical dimensions.

### 1️⃣ Temporal Analysis

I planned to analyze AI feature usage and cost accumulation over time to identify:

- Adoption trends
- Retention and churn patterns
- Engagement decay
- Cumulative cost growth

**Planned Visualizations:**
- Time-series revenue and usage charts
- Cohort retention curves
- Cumulative cost growth charts

---

### 2️⃣ Geospatial Analysis

I identified the need to examine regional differences in AI usage and cost concentration across global markets.

**Planned Visualizations:**
- Choropleth maps
- Regional usage heatmaps
- Geographic revenue concentration maps

---

### 3️⃣ Linguistic Analysis

To evaluate perceived AI value, I planned to analyze user feedback from reviews and surveys to identify:

- Sentiment trends
- Pricing concerns
- Usability issues
- Feature satisfaction patterns

**Planned Visualizations:**
- Sentiment over time
- Topic modeling clusters
- Keyword frequency dashboards

---

### 4️⃣ Network Analysis

I proposed examining structural relationships between AI features, users, and teams to identify:

- Feature co-usage patterns
- High-cost user clusters
- Behavioral dependencies

**Planned Visualizations:**
- Node-link diagrams
- Feature dependency networks
- User cluster graphs

---

## Stakeholder Analysis

I identified two primary stakeholder groups with distinct decision-making needs.

### 👤 Stakeholder Group 1: AI Product Managers

**Decisions:**
- Expand, optimize, restrict, or remove AI features

**Insight Needs:**
- Feature-level ROI
- Engagement sustainability
- Identification of cost-heavy behaviors

**Visualization Needs:**
- Feature comparison dashboards
- Cohort retention views
- Usage decay and engagement analysis

---

### 💰 Stakeholder Group 2: Finance and Monetization Teams

**Decisions:**
- Pricing tier adjustments
- Usage caps
- Cost control strategies

**Insight Needs:**
- Cost-to-value ratios
- User profitability segmentation
- Revenue concentration metrics

**Visualization Needs:**
- Aggregated cost-value dashboards
- Pricing scenario simulations
- Profitability segmentation charts

---

### Key Differences in Stakeholder Needs

I recognized that:

- Product managers require detailed behavioral and feature-level insights.
- Finance teams require summarized, monetizable metrics focused on cost efficiency and profitability.

This distinction guided how I later structured dashboard views.

---

## Data Assessment

### Currently Available Data

I identified publicly accessible data sources including:

- Public SaaS and AI usage datasets
- Open-source LLM usage logs
- Published AI pricing data
- App store reviews and public user feedback

---

### Additional Data Needed (Modeled)

Because internal financial data was unavailable, I determined that certain variables would need to be modeled, including:

- Estimated inference cost per feature
- Revenue estimates by user segment
- Feature exposure timestamps

---

### Constraints

I acknowledged several constraints:

- No access to internal financial or infrastructure data
- Privacy restrictions on user-level revenue
- Need to estimate compute cost rather than measure directly

---

## Data Integration Strategy

I proposed combining usage logs with modeled cost estimates and linking feedback data to feature usage patterns. Users would be aggregated into cost-value segments to enable profitability analysis without exposing sensitive individual-level revenue data.

---

## Role of AI Tools

I identified that AI tools could support:

- Sentiment analysis of user feedback
- Topic modeling for feature perception
- User clustering
- Pricing scenario simulation
- Hypothesis refinement during project design

Week 1 established the conceptual foundation, stakeholder alignment, and analytical framework that guided the development of subsequent dashboards.
