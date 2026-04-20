# Service Level Framework: SLI vs. SLO vs. SLA

This project documentation outlines the relationship between Service Level Indicators (SLI), Service Level Objectives (SLO), and Service Level Agreements (SLA) used for monitoring and maintaining system reliability.

## Overview

In a reliability-first culture, we use a tiered approach to measure and manage service health:
1.  **SLA**: What we promise (The Legal Contract).
2.  **SLO**: What we aim for (The Internal Target).
3.  **SLI**: What we measure (The Metric).

---

## The Framework

### 1. Service Level Agreement (SLA)
The contractual commitment made to external users.
*   **Consequence:** Failure to meet this usually results in financial credits or service-level penalties.
*   **Strategy:** Always set your SLA to be more "relaxed" than your SLO (e.g., SLA of 99.5% vs. SLO of 99.9%) to create a safety buffer.

### 2. Service Level Objective (SLO)
The internal target for an SLI over a rolling window (e.g., 30 days).
*   **Purpose:** Defines the "Error Budget"—the amount of failure we tolerate before halting feature work to focus on stability.
*   **Example:** 99.9% of requests must succeed.

### 3. Service Level Indicator (SLI)
The raw quantitative measure of a service's performance.
*   **Common Metrics:** Latency, Throughput, Error Rate, Availability.
*   **Example:** `(Successful HTTP Requests / Total HTTP Requests) * 100`

---

## Analogy: The Pizza Delivery Model


| Component | Definition | Real-world Example |
| :--- | :--- | :--- |
| **SLA** | Commitment | The "30 minutes or it's free" guarantee to the customer. |
| **SLO** | Internal Goal | The manager's target to deliver 98% of pizzas under 30 mins. |
| **SLI** | Measurement | The time recorded on the delivery driver's stopwatch. |

---

## Usage & Implementation
To implement this framework in your service:
1.  **Identify SLIs** that actually impact user experience.
2.  **Set SLOs** based on historical data and business needs.
3.  **Monitor Error Budgets**; if the budget is exhausted, prioritize reliability tasks over new features.
