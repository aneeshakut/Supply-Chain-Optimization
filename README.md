# Global Supply Chain Optimization with Python

<p align="center">
  <img align="center" src="https://miro.medium.com/max/700/1*rtP7otnvgY2nT-ONqtAM6A.png">
</p>


This project implements a **data-driven global supply chain optimization model** to **minimize total costs** while meeting multi-country demand.  
It identifies **optimal plant locations, sizes, and production flows** under capacity, production, and shipping constraints.

---

## 📝 Problem Statement

A multinational manufacturing company aims to **redesign its supply chain** to:

- Reduce total monthly costs (fixed + production + shipping)
- Satisfy demand across multiple countries
- Adapt to rising shipping costs and capacity limitations
- Evaluate strategic scenarios for growth or disruption

---

## 🎯 Problem-Solving Methodology

### 1️⃣ Define the Problem
- Optimize **plant locations and sizes**
- Minimize total cost while satisfying all market demands

### 2️⃣ Identify Decision Variables
| Type | Variable |
|------|----------|
| Strategic | Open Low/High-capacity plant in each country (binary) |
| Operational | Production quantity from each plant to each market (continuous) |

### 3️⃣ Quantify Costs
| Cost Type | Description |
|-----------|-------------|
| Fixed | Rent, utilities, equipment, management |
| Variable | Production cost per unit in each country |
| Shipping | Shipping cost per container (converted to per unit) |

### 4️⃣ Model Supply & Demand
- All market demand must be fully satisfied
- Production can occur locally or be shipped internationally

### 5️⃣ Apply Capacity Constraints
- Production ≤ plant capacity
- Only open plants can produce

### 6️⃣ Optimization Framework
- **Mixed Integer Linear Programming (MILP)**
- Implemented using **Python + PuLP**
- Handles **binary strategic** and **continuous operational** decisions

### 7️⃣ Define Objective
> Minimize total monthly supply chain cost = Fixed Costs + Production Costs + Shipping Costs

### 8️⃣ Solve Model
- Solver finds **cost-optimal plant network** and production/shipping allocation
- Generates actionable insights for strategic decision-making

### 9️⃣ Analyze & Visualize Results
- Total cost per month
- Opened plants and capacities
- Production allocation by country
- Shipping flows

### 🔟 Simulate Strategic Scenarios
| Scenario | Description | Insights |
|----------|------------|---------|
| Base Case | Current demand and costs | Benchmark cost and plant allocation |
| Increased India Capacity | Double high-capacity India plant | Reduce global costs by outsourcing to low-cost region |
| Surging Shipping Costs | Container costs ×5 | Shifts production closer to local markets, increases total cost |

---

## 📊 Input Data

| Input | Description | Format |
|-------|------------|--------|
| Fixed Costs | Monthly cost per plant type per country | Excel |
| Variable Costs | Production cost per unit | Excel |
| Shipping Costs | Cost per container between countries | Excel |
| Plant Capacities | Low / High capacity (kUnits/month) | Excel |
| Market Demand | Units per country | Excel |

> Excel files allow **flexible scenario testing**.

---

## 🛠️ Technology Stack

- **Python 3.6+** – Modeling & data analysis  
- **PuLP** – Linear Programming solver  
- **Pandas** – Data management  
- **Excel** – Scenario input  

---

## 📈 Example Results

| Country | Low-Capacity Plant | High-Capacity Plant |
|---------|-----------------|------------------|
| USA     | 0               | 1                |
| Germany | 0               | 0                |
| Japan   | 0               | 1                |
| Brazil  | 1               | 0                |
| India   | 0               | 1                |

**Optimal Production Flows (Units/Month)**

| From → To | USA | Germany | Japan | Brazil | India |
|------------|-----|---------|------|-------|-------|
| USA        | 1,300,000 | 0 | 200,000 | 0 | 0 |
| Germany    | 0 | 0 | 0 | 0 | 0 |
| Japan      | 0 | 0 | 1,500,000 | 0 | 0 |
| Brazil     | 145,000 | 0 | 0 | 0 | 0 |
| India      | 1,500,000 | 90,000 | 0 | 0 | 160,000 |

**Total Cost:** \$92,981,000 / Month  
**Status:** Optimal

---

## 🔮 Key Insights

- **Cost-efficient outsourcing:** Low-cost countries (India, Brazil) produce for multiple markets
- **Localization under high shipping costs:** Plants produce locally when shipping surges
- **Capacity investments:** Increasing capacity in low-cost regions reduces total cost

---

## ⚡ Next Steps / Extensions

- Include **carbon emissions & sustainability constraints**
- Model **inventory and storage costs**
- Incorporate **delivery lead times & customs**
- Simulate **currency fluctuations and geopolitical risks**

## 📂 Repository Structure

