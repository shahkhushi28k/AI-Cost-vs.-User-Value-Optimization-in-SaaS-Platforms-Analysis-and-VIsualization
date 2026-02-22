# 📅 Week 5 – Tree and Network Visualizations

## Focus: Network Relationships in AI Feature Usage

In Week 5, I extended the project into **structural and relational analysis** using tree and network visualizations. While previous weeks focused on time, geography, and categorical distribution, this stage explored *how AI features relate to one another and how they influence business outcomes*.

Network analysis allowed me to model both hierarchical influence pathways and structural similarity clusters within the AI ecosystem.

---

## Project Topic

**Network Relationships in AI Feature Usage for a SaaS Platform**

I developed two complementary network models:

1. A **Multi-Layer Influence Network** connecting:
   - AI Categories → Features → Business/System Impact

2. A **Feature Co-Usage Cluster Network** revealing:
   - Structural similarity among AI capabilities
   - Community clusters within the AI ecosystem

Together, these visualizations provide both directional and relational perspectives.

---

# 🔗 Visualization 1: Multi-Layer AI Usage Influence Network

![Multi-Layer AI Usage Influence Network](images/network_multilayer.png)

### Purpose

To model how AI capability categories translate into feature-level usage and how those features influence business and system metrics.

### Network Structure

**Layer 1:** AI Categories  
(Text Generation, Search, Recommendation, Classification, etc.)

**Layer 2:** Individual AI Features  
(Chat Completion, Semantic Search, Topic Classification, etc.)

**Layer 3:** Business & System Impact  
(Infrastructure Load, Revenue Contribution, User Engagement, Latency Sensitivity)

### Encoding

- **Node size** → Usage volume  
- **Edge thickness** → Influence strength (usage-weighted)  
- **Color** → Network layer  
- **Direction** → Flow from category → feature → impact  

### Design Rationale

I structured this as a directed, layered network to clearly represent influence pathways. The horizontal layering reduces ambiguity and visually communicates strategic flow from product capabilities to measurable outcomes.

Edge transparency was reduced to mitigate clutter caused by dense cross-layer relationships.

### Network Metrics

- Total Nodes: 18  
- Total Edges: 42  
- Network Density: 0.27  
- Average Degree: 4.67  

A density of 0.27 suggests a moderately connected system — features are neither isolated nor overly saturated with dependencies.

The average degree of 4.67 indicates meaningful interdependence among AI capabilities.

### Stakeholder Benefit

- **Product Teams** trace feature impact pathways.
- **Finance Teams** identify revenue-driving nodes.
- **Engineering Teams** detect workload concentration and stress points.

---

# 🧩 Visualization 2: AI Feature Co-Usage & Capability Clusters

![AI Feature Co-Usage & Capability Clusters](images/network_cluster.png)

### Purpose

To identify structural similarity and clustering patterns among AI features.

### Network Structure

- Undirected  
- Weighted  
- Community-based  

### Encoding

- **Node color** → Capability category  
- **Node size** → Usage volume  
- **Thick edges** → Same-category relationships  
- **Light edges** → Cross-category similarity  

### Design Rationale

This visualization reveals whether AI features operate in isolated silos or exhibit cross-capability integration. It emphasizes structural cohesion and cluster formation.

A colorblind-safe palette was used to ensure accessibility.

### Network Metrics

- Modularity Score: 0.41  

A modularity score of 0.41 indicates distinguishable capability clusters while maintaining cross-category connectivity. This reflects a modular yet interconnected AI architecture.

### Stakeholder Benefit

- **Product Managers** detect overlapping or redundant features.
- **Engineers** identify integration opportunities.
- **Leadership** evaluates structural cohesion across AI capabilities.

---

# Data Construction and Preprocessing

To construct these networks, I:

- Aggregated usage counts by feature
- Mapped features to predefined categories
- Normalized usage values for node scaling
- Generated weighted edge lists
- Modeled influence weights based on usage intensity

Two edge lists were created:

1. Category → Feature  
2. Feature → Business Impact  

Feature-to-feature similarity edges were derived from categorical membership.

---

# Constraints and Limitations

- Influence weights are usage-based, not telemetry-driven.
- Cross-category similarity edges are structurally inferred.
- Dense edges may require threshold filtering in production.
- Real infrastructure metrics would strengthen causal modeling.

To mitigate visual clutter:

- Applied horizontal layering
- Reduced edge opacity
- Normalized node scaling
- Used consistent color encoding

---

# 🤖 Part 2: AI-Assisted Design Process

## AI Tool Used

- ChatGPT (GPT-5.2 Thinking)

---

## Documented Prompts (Verbatim)

**Prompt 1:**  
> “What types of network structures best represent relationships between AI feature categories and business impact in a SaaS platform?”

**Prompt 2:**  
> “How can I visualize clustering patterns among AI features to show structural similarity?”

---

## Evaluation of AI Suggestions

AI was helpful in:

- Suggesting multi-layer network modeling
- Recommending weighted edges
- Proposing cluster-based visualization approaches

However:

- Early designs were visually cluttered
- Some suggestions exceeded assignment scope

I refined outputs by:

- Simplifying layout structure
- Applying horizontal layering
- Reducing edge opacity
- Standardizing color encoding

Final decisions were guided by clarity, stakeholder needs, and assignment constraints.

---

# Strategic Insights

The multi-layer influence network reveals that **Search and Summarization features act as structural bridges** between AI categories and business impact metrics, indicating their central role in value delivery.

The feature cluster network highlights tightly connected capability groups, suggesting modular AI functionality with meaningful cross-category integration.

Together, these visualizations provide both:

- Vertical insight (influence pathways)
- Horizontal insight (structural cohesion)

---

# Week 5 Reflection

By combining hierarchical influence modeling with relational cluster analysis, I captured both strategic impact flow and structural similarity within AI feature usage.

This dual-network approach provides a comprehensive understanding of AI capability dynamics and supports informed decision-making across Product, Finance, and Engineering teams.
