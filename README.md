# Supply Chain Optimization with Python

<p align="center">
  <img align="center" src="https://miro.medium.com/max/700/1*rtP7otnvgY2nT-ONqtAM6A.png">
</p>


The model identifies optimal manufacturing locations, plant sizes, and production flows to minimize total cost while meeting customer demand under volatile shipping conditions.

---

## 🔍 Problem Statement
Redesign a global supply chain network to account for:
- Rising shipping costs
- Fixed and variable manufacturing costs
- Capacity constraints
- Multi-market customer demand

---

## 🧠 Methodology
- **Optimization Technique:** Linear Programming  
- **Solver:** PuLP (COIN-OR)  
- **Decision Variables:**
  - Production quantities between origin–destination markets
  - Binary plant opening decisions (Low / High capacity)

---

## 🌍 Network Scope
- **Markets:** Brazil, USA, India, Japan, Germany  
- **Plant Types:** Low-capacity, High-capacity  
- **Assumption:** 1 container = 1,000 units

---

## 📊 Inputs
- Fixed manufacturing costs
- Variable production costs
- Shipping (freight) costs
- Plant capacities
- Market demand

(All inputs managed via Excel for easy scenario testing)

---

## 📈 Scenarios Analyzed
- **Baseline network design**
- **Increased capacity in low-cost regions**
- **Severe freight cost inflation (×5 shipping costs)**

**Key Insight:**  
Rising transportation costs drive a shift from global outsourcing to localized production strategies.

---

## 🛠️ Tech Stack
- Python
- PuLP
- Pandas
- Excel-based data modeling

---

## 🚀 Key Outcomes
- Cost-optimal plant location and sizing decisions
- Quantified trade-offs between production and logistics costs
- Flexible model for strategic, long-term supply chain planning

---

## 🔮 Extensions
- Carbon emission constraints
- Inventory & storage costs
- Lead-time optimization
- Customs and currency effects

---

📌 *This project showcases applied optimization, data-driven decision-making, and supply chain strategy modeling.*
