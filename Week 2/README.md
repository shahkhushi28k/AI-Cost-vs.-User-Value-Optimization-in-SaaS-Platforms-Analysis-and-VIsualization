# 📅 Week 2 – Temporal Analysis & Visualization

## Focus: Temporal Analysis of AI Feature Usage

In Week 2, I focused on the **temporal dimension** of my project: analyzing how AI feature usage evolves over time and how this impacts cost accumulation and engagement sustainability.

As SaaS platforms scale AI features, understanding monthly adoption, growth patterns, and decline trends becomes critical for evaluating long-term cost-value alignment.

---

## Temporal Analysis Objective

My goal was to analyze:

- How AI feature usage changes month-over-month  
- Which features are growing, stable, or declining  
- How total AI workload evolves over time  
- Whether usage growth signals sustainable engagement  

This analysis directly supports both Product and Finance stakeholders by revealing workload trends and feature demand patterns.

---

# 📊 Visualization 1: AI Feature Usage by Month (Grouped Bar Chart)


![AI Feature Usage by Month](images/temporal_grouped_bar.png)

### Purpose

To compare usage trends of stable versus declining AI features across months.

### Design Details

- **X-axis:** Month (January–December)
- **Y-axis:** Number of AI feature calls
- **Encoding:** Grouped bars representing two feature categories (Stable vs Declining)

### Design Rationale

I selected a grouped bar chart to allow direct comparison between two feature categories within the same monthly time frame. This makes relative changes easy to detect without requiring cumulative interpretation.

### Key Insights

- Stable features show steady growth over time.
- Declining features demonstrate consistent reduction in usage.
- Divergence between feature categories becomes more pronounced in later months.

### Stakeholder Benefit

- **Product Managers** can identify which features maintain engagement.
- **Finance Teams** can anticipate compute cost concentration shifts.
- **Leadership** can evaluate feature investment decisions based on adoption trajectory.

---

# 📊 Visualization 2: AI Feature Usage Volume Over Time (Stacked Area Chart)


![AI Feature Usage Volume Over Time](images/temporal_stacked_area.png)

### Purpose

To show how total AI usage volume evolves over time and how individual features contribute to overall demand.

### Design Details

- **X-axis:** Month  
- **Y-axis:** Total number of AI calls  
- **Encoding:** Stacked areas representing individual AI features (Text Generation, Code Assistant, Image Generation)

### Design Rationale

I selected a stacked area chart to emphasize cumulative workload while preserving visibility into individual feature contribution. This design highlights system-wide demand trends rather than isolated feature performance.

### Key Insights

- Overall AI demand increases steadily through mid-year before stabilizing.
- Text generation dominates total workload.
- Code assistant shows moderate growth.
- Image generation remains smaller but consistent.

### Stakeholder Benefit

- **Finance and Leadership** can assess overall AI workload growth.
- **Engineering** can anticipate infrastructure scaling needs.
- **Product Teams** can identify dominant feature segments.

---

# 🤖 Part 2: AI-Assisted Design Process

## Use of AI Tools

In Week 2, I used ChatGPT (GPT-5.2 Thinking) as a design-support tool. I did not rely on AI for conclusions or interpretation; instead, I used it to refine stakeholder questions, validate visualization types, and support implementation.

---

## Documentation of AI Interactions

### Prompt 1 (verbatim)

> “What time-based questions would product managers and finance teams ask when evaluating AI feature usage in a SaaS platform?”

**Reasoning:**  
This clarified stakeholder-specific temporal needs before selecting visualization types.

---

### Prompt 2 (verbatim)

> “Suggest simple temporal visualization types that could clearly show AI feature usage trends over time without forecasting.”

**Reasoning:**  
This ensured the visualizations remained descriptive and aligned with assignment scope.

---

### Prompt 3 (verbatim)

> “Generate example Python code for a grouped bar chart and a stacked area chart using monthly AI usage data.”

**Reasoning:**  
This supported implementation after I finalized design decisions.

---

## Evaluation of AI Suggestions

AI was most helpful during early-stage brainstorming and visualization selection. However, some suggestions initially included overly complex visuals or additional variables beyond assignment scope.

I applied my own judgment to refine AI outputs by:

- Reducing visual clutter  
- Avoiding over-interpretation  
- Selecting familiar, stakeholder-friendly chart types  

---

## Implementation Plan

### Data Preparation

- Parsed usage timestamps into consistent datetime format  
- Aggregated AI usage events by month  
- Validated totals for accuracy  
- Explicitly retained missing months as zero values  

---

### Tools and Libraries

- **Python (Pandas, NumPy)** → Data cleaning and aggregation  
- **Matplotlib** → Static visualization creation  

These tools were chosen for transparency, reproducibility, and alignment with course examples.

---

## Handling Data Quality Issues

- Missing months were preserved as zero values to avoid misleading gaps.
- No interpolation or forecasting was applied.
- Aggregation decisions were documented clearly.

---

## Final Reflection for Week 2

This temporal analysis demonstrated that simple, well-structured visualizations can effectively communicate time-based insights about AI feature usage. By focusing on monthly trends and cumulative workload, I established a clear understanding of demand growth patterns that informed later cost-value modeling.

Week 2 strengthened the analytical foundation for evaluating AI cost sustainability over time.
