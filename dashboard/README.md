# 📊 Power BI Dashboard — Supply Chain Planning & Operations Intelligence

This folder contains the Power BI dashboard screenshots and data-model documentation for **Project #4 — Supply Chain Planning & Operations Intelligence**.

The dashboard integrates the Gold analytical model and Python optimization scenario outputs to support management analysis of **planned demand, capacity utilization, machine allocation, bottlenecks, and optimization trade-offs**.

## 📊 Dashboard Report Pages

### 1. Executive S&OP Overview

![Executive S&OP Overview](01_Executive_S&OP_Overview.png)

Provides a management-level overview of planned demand, modeled allocation, demand fulfillment, processing requirements, implied overtime, and planning trends.

**Business Question:** Can the modeled allocation fulfill planned demand, and what capacity and workload pressures require management attention?

### 2. Capacity & Bottlenecks

![Capacity & Bottlenecks](02_Capacity_Bottlenecks.png)

Examines aggregate and machine-level permitted capacity utilization, remaining capacity, implied overtime, and machine-period constraints.

**Business Question:** Where does capacity become constrained even when aggregate headroom remains available?

### 3. Demand & Allocation

![Demand & Allocation](03_Demand_Allocation.png)

Analyzes planned demand by product, modeled fulfillment, and workload allocation across eligible packing machines.

**Business Question:** Which products drive workload, and which resources does the optimization model depend on to fulfill demand?

### 4. Scenario Analysis

![Scenario Analysis](04_Scenario_Analysis.png)

Compares three optimization scenarios:

- **Min Processing:** Minimizes modeled processing hours.
- **Min Overtime:** Minimizes implied overtime.
- **Threshold Capacity:** Evaluates allocation within a tighter permitted-capacity framework.

**Business Question:** How do alternative optimization objectives change processing requirements, overtime exposure, and machine-level workload distribution?

---

## 🏗️ Power BI Data Model

![Power BI Data Model](05_Data_Model.png)

The Power BI analytical model integrates:

- **12 Gold Analytical Tables:** 4 dimensions, 4 facts, and 4 bridges.
- **4 Optimization Scenario Tables:** scenario assumptions, scenario summary, machine-period summary, and scenario allocations.

This architecture connects the original S&OP planning baseline with modeled optimization outputs for cross-functional analytical reporting.

### 🔗 Relationship Details

![Power BI Relationship Details](06_Relationship_Details.png)

The relationship model supports filtering and analysis across planning periods, products, machines, demand, capacity, and optimization scenarios.

---

## 🛠️ Advanced Power BI Features

- **DAX Measures & KPIs:** Demand fulfillment, processing hours, implied overtime, capacity utilization, and remaining capacity.
- **Scenario Comparison:** Interactive analysis of alternative optimization objectives.
- **Dynamic Management Narratives:** Context-sensitive explanations of selected scenario results.
- **Conditional Formatting:** Highlights high-utilization machines and constrained machine-period combinations.
- **Hierarchical Matrices:** Supports machine- and period-level capacity diagnostics.
- **Interactive Slicers & Cross-Filtering:** Enables focused analytical exploration.
- **Report-Page Tooltips:** Provides additional machine-level capacity context.
- **Product Drillthrough:** Connects product demand to modeled machine allocation.
- **Field Parameters:** Supports flexible analytical views and metric selection.

## 🔍 Key Business Insights

**1. Full Modeled Demand Fulfillment**

All three scenarios allocate the full **3,071,692 meters** of planned demand within their modeled constraints.

**2. Aggregate Headroom Masks Localized Capacity Pressure**

Under Threshold Capacity, aggregate permitted packing-capacity utilization is **62.31%**, yet **14 machine-period combinations reach 100% modeled utilization**.

**3. Machine-Level Dependency**

Machine 921 reaches **100% modeled utilization across P3–P8** under Threshold Capacity, indicating a priority area for routing and capacity analysis.

**4. Different Objectives Produce Different Allocation Strategies**

Machine 921 receives approximately **1.758M meters under Min Processing**, compared with **1.081M meters under Threshold Capacity**, demonstrating how optimization objectives influence workload distribution.

**5. Scenario Trade-offs Require Management Judgment**

Lower processing requirements do not necessarily produce lower implied overtime or less resource concentration. Management should evaluate both scenario-level KPIs and machine-level allocation before selecting a planning strategy.

---

## 💡 Management Decision Support

The dashboard supports a structured planning decision process:

**Evaluate Demand → Identify Capacity Pressure → Examine Machine Allocation → Compare Scenarios → Assess Resource Dependency → Support Planning Decisions**

**Analytical Scope:** Results represent modeled manufacturing planning scenarios, not observed factory execution or actual machine utilization.

---

[⬅️ Back to Main Project README](../README.md)
