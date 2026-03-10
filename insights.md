---
layout: default
title: Insights
---
# Insights

### [Type1/Type2 Slowly Changing Dimension(SCD) Design](/pages/insights/insight-1.html)

**The Challenge**: How do you ensure a data warehouse can accurately recreate a "point-in-time" report from three years ago without massive storage bloat?

**The Insight**: This post breaks down the transition from Silver to Gold layers, defining which business attributes require historical versioning (Type 2) versus simple overwrites (Type 1). I discuss my specific metadata framework—using effective dating, current_ind logic, and nanosecond offsets—to prevent overlapping timelines and handle the "ghosts" of source system soft-deletes.

**Key Topics**: Audit Metadata, Time-Zone Alignment, Effective Dating, Soft-Delete Handling.

[Read more...](/pages/insights/insight-1.html)

---

### [Star Schema Design for Performance and Scale](/pages/insights/insight-2.html)

**The Challenge**: Academic data models often look "beautiful" on paper but fail the "5-second dashboard load" test in production.

**The Insight**: A deep dive into why I favor a flattened Star Schema over complex Snowflaking for high-scale environments. I discuss the critical decision-making process behind defining Fact Grain, managing multi-address dimensions, and the necessity of Summary Facts for executive KPIs. I argue that a Data Architect’s job isn't done until they've collaborated with front-end developers to shift heavy calculations into the Gold layer.

**Key Topics**: Fact Grain, Surrogate vs. Business Keys, Partitioning, Summary vs. Detail Facts.

[Read more...](/pages/insights/insight-2.html)

---

### [The Engineering-Led Architect](/pages/insights/insight-3.html)

**The Challenge**: When a 200-table Medallion architecture misses its 8:00 AM SLA, the fix is rarely just a missing index or query optimization

**The Insight**: I share a case study where I reduced a daily load process from 8 hours to under 2.5 hours—not by rewriting SQL, but by decoupling the high-level orchestration flow to maximize compute utilization. I also cover micro-level optimizations in Databricks, including refactoring redundant MERGE statements, DAG caching, and Z-Ordering for high-cardinality queries.

**Key Topics**: Orchestration Design, Spark DAG Optimization, Delta Lake Merges, Z-Ordering.

[Read more...](/pages/insights/insight-3.html)

---

### [Handling Data Quality withing Databricks pipeline](/pages/Databricks/Databricks_HandleDataQuality.html)

**The Challenge**: How would someone handle Data Quality in ETL Pipelines?

**The Insight**: a structured, rule-based approach to managing Data Quality (DQ) within Databricks-based ETL pipelines.

**Key Topics**: Data Quality, ETL Pipelien transformations

[Read more...](/pages/Databricks/Databricks_HandleDataQuality.html)