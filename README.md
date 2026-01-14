# Global Supply Chain Optimization with Python

<p align="center">
  <img align="center" src="https://miro.medium.com/max/700/1*rtP7otnvgY2nT-ONqtAM6A.png">
</p>

This project demonstrates **data-driven supply chain network optimization** using **Linear Programming (MILP)** in Python.  
It identifies the optimal locations, sizes, and production flows of manufacturing plants to **minimize total cost** while meeting multi-country demand.

---

## 📝 Problem Statement

A multinational manufacturing company seeks to redesign its supply chain to:

- Reduce total monthly costs (production + shipping + fixed plant costs)
- Satisfy demand in multiple countries
- Adapt to rising shipping costs and capacity constraints
- Evaluate strategic scenarios for future expansion or disruption

---

## 🎯 Problem-Solving Methodology

### 1. Define the Problem
- Optimize global plant locations, sizes, and production flows
- Minimize total supply chain cost
- Meet all market demand under capacity and cost constraints

### 2. Identify Decision Variables
- **Strategic:** Open a Low/High-capacity plant in each country (binary)
- **Operational:** Production quantity from each plant to each market (continuous)

### 3. Quantify Costs
- **Fixed Costs:** Rent, utilities, equipment, and management
- **Variable Costs:** Production cost per unit
- **Shipping Costs:** Per-unit shipping cost derived from container rates

### 4. Model Supply and Demand
- Demand from each country must be fully satisfied
- Production can occur locally or be shipped internationally

### 5. Apply Capacity Constraints
- Plant production ≤ installed capacity
- Only active plants produce goods

### 6. Choose Optimization Framework
- **Mixed Integer Linear Programming (MILP)** using **PuLP**
- Captures both binary (strategic) and continuous (operational) decisions

### 7. Define Objective Function
- Minimize total cost = Fixed Plant Costs + Variable Production Costs + Shipping Costs
- Balances production location and shipping trade-offs

### 8. Solve Model
- Solver identifies cost-optimal combination of:
  - Plant locations and sizes
  - Production allocation per market
  - Cross-border shipment flows

### 9. Analyze Results
- Total monthly cost
- Plants opened and their capacities
- Production and shipping allocations
- Insights for strategic planning

### 10. Simulate Scenarios
- Test network sensitivity to:
  - Increased shipping costs
  - Growing demand in specific regions
  - Capacity expansions
  - Plant closures

---

## 📊 Inputs

| Input Type | Description |
|------------|-------------|
| Fixed Costs | Monthly operating cost per plant type per country |
| Variable Costs | Production cost per unit per country |
| Shipping Costs | Shipping cost per container between countries |
| Plant Capacities | Low / High capacity in thousands of units per month |
| Market Demand | Units required per country |

_All inputs are managed via Excel for flexible scenario testing._

---

## 🛠️ Technology Stack

- **Python** – Data processing and modeling
- **PuLP** – Linear Programming solver
- **Pandas** – Data handling and analysis
- **Excel** – Input data management

---

## 🚀 Key Outcomes

- Optimal plant location and sizing decisions
- Cost-effective production and shipping allocations
- Quantified trade-offs between local vs. global production
- Scenario-based decision support for strategic planning

---

## 🔮 Future Scope

- Include **carbon emissions / sustainability constraints**
- Model **inventory and storage costs**
- Incorporate **delivery lead times and customs**
- Simulate **currency fluctuations and geopolitical risks**
