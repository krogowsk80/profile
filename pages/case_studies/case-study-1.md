---
layout: default
title: Security-First Cloud Migration
---
# Case Study: Architecting a "Security-First" Cloud Migration for National Social Services
### Legacy-to-Cloud Transformation | High-Stakes Governance | 640M+ Record Volume

## The Challenge: Breaking the "On-Premise" Deadlock
A major social services department needed to modernize 20+ years of sensitive child-care data across five lines of business. However, strict security policies prohibited direct cloud-to-on-prem database access. The existing infrastructure—a fragmented mix of Oracle, Cognos, and legacy ETL—was suffering from "maintenance exhaustion," requiring 30+ disparate reporting models to serve 200+ external agencies.

## The Strategic Solution: A Pioneer Cloud Blueprint
As the Solution Architect and Technical Lead, I designed a resilient, decoupled architecture that bypassed security bottlenecks while setting the standard for the department’s transition to Azure.

### Security-First Data Ingestion
To honor the "no-access" security policy, I implemented Oracle GoldenGate for real-time Change Data Capture (CDC). This allowed for daily (and potentially real-time) synchronization to the cloud without compromising the integrity or security of the production on-prem environment.

### The Medallion Lakehouse (Databricks & Unity Catalog)
*   **Silver Layer:** Engineered high-performance Delta tables for 107 source tables, including a 313-million-record master table, utilizing Type 2 SCD to maintain a perfect audit trail of sensitive history.
*   **Gold Layer:** Consolidated 30+ legacy models into a unified set of star schemas, drastically reducing maintenance overhead.
*   **Governance:** Leveraged Unity Catalog and Dynamic Data Masking to ensure that PII was shielded from ministry staff while remaining accessible to authorized agency users.

### Custom Enterprise Orchestration
In the absence of third-party scheduling tools (e.g., Control-M), I architected a native orchestration framework using Azure Data Factory (ADF) and Databricks Workflows, incorporating automated email notifications and error handling.

## The Execution: Leading through Complexity

*   **Architectural Defense:** I co-led the technical defense of the solution to the TAG/BART (Technical & Business Architecture Review) boards, ensuring the design met every compliance, legal, and performance benchmark.
*   **Modern DevOps Foundations:** Introduced the department to modern engineering standards, including CI/CD via Databricks Bundles and Azure DevOps for agile delivery.
*   **Legacy Knowledge Transfer:** Established a comprehensive Project Wiki to serve as the "living documentation" for future departmental initiatives.

## The Impact: A Proven Template for Success

*   **Pioneer Status:** Successfully launched the first project to go to Production on the Azure Cloud for the department.
*   **Scale & Performance:** Seamlessly manages a total volume of 646M+ records (98GB compressed) with high availability for 215+ distributed users.
*   **Architecture Consolidation:** Replaced a brittle, fragmented legacy reporting environment with a scalable, governed, and automated cloud ecosystem.

<br>
*[Image Placeholder: Architectural Workflow]*