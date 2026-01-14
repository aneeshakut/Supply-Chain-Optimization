## 1. Total Cost & Solver Status

- **Total Monthly Cost:** $92,981,000  
- **Solver Status:** Optimal solution found  

> The LP model successfully minimized total costs while satisfying all demand and capacity constraints.

---

## 2. Plant Decisions (Strategic Insight)

| Location | Low Capacity Open | High Capacity Open | Insight |
|----------|-----------------|------------------|---------|
| USA      | 0               | 1                | Open high-capacity plant to serve domestic & partial Japan demand |
| Germany  | 0               | 0                | No plant opened; demand met via imports from India |
| Japan    | 0               | 1                | High-capacity plant sufficient for local demand |
| Brazil   | 1               | 0                | Low-capacity plant sufficient for domestic demand |
| India    | 0               | 1                | High-capacity plant opened to serve domestic & USA demand |

---

## 3. Production & Shipment Plan (Operational Insight)

### Shipment Matrix (Plant → Demand Location)

| Plant \ Demand | USA      | Germany | Japan     | Brazil   | India    |
|----------------|---------|---------|-----------|----------|---------|
| USA            | 1,300,000 | 0       | 200,000   | 0        | 0       |
| India          | 1,500,000 | 90,000  | 0         | 0        | 160,000 |
| Japan          | 0        | 0       | 1,500,000 | 0        | 0       |
| Brazil         | 0        | 0       | 0         | 145,000  | 0       |
| Germany        | 0        | 0       | 0         | 0        | 0       |

> Only non-zero flows are shown; zeros indicate no shipment.  

**Key Observations:**

- India plant serves **USA and domestic demand** — cost-efficient long-distance supply.  
- USA high-capacity plant primarily serves **domestic demand** and partially **Japan**.  
- Germany has no operational plant; all demand is met via imports.  

---

## 4. Actionable Insights

### Plant Strategy
- Open high-capacity plants in **India, Japan, USA**  
- Open low-capacity plant in **Brazil**  
- Keep **Germany closed** and rely on imports  

### Shipment Strategy
- Prioritize **local production** for high-demand regions  
- Use **India plant** for strategic long-distance shipments (USA)  

### Cost Optimization
- Monitor transportation and production costs for potential adjustments  
- Germany plant opening not cost-effective currently  

### Operational Efficiency
- Brazil low-capacity plant fully utilized — consider expansion if demand increases  

---
