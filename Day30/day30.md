# Day 30 — Supply Chain Builder

## Project

Supply Chain Builder is a beginner-friendly interactive simulation that teaches the basic decisions involved in designing a supply chain.

## Decisions

1. Supplier strategy
2. Factory location
3. Warehouse strategy
4. Transportation method
5. Inventory strategy

Before each decision, the simulator explains what the concept means, why it matters, and its business trade-offs.

## Live Metrics

- Cost
- Delivery Speed
- Risk
- Customer Satisfaction
- Sustainability

## Final Dashboard

The simulator generates:

- Overall Supply Chain Score from 0–100
- Strengths
- Weaknesses
- Biggest Risk
- Three practical improvements

## Key Learnings

### 1. Supplier Diversification

Multiple suppliers reduce dependence on a single supplier and improve resilience, although management becomes more complex.

### 2. Factory Location

A factory near customers can improve delivery speed.

A low-cost region can reduce production costs.

A central location balances cost, access, and delivery.

### 3. Warehouse Strategy

Regional warehouses can improve delivery speed and resilience but increase operating costs.

A single warehouse is simpler and cheaper but creates a larger single point of failure.

### 4. Transportation

Road is flexible and useful for shorter distances.

Rail is efficient for large land shipments.

Sea is economical for large international volumes but slower.

Air is the fastest option but is expensive and less sustainable.

### 5. Inventory

Low inventory reduces storage costs but increases stockout risk.

High inventory protects against shortages but ties up more cash.

Balanced inventory provides a practical middle ground between cost and availability.

### 6. Supply Chain Optimization

There is no perfect supply chain.

A strong supply chain balances:

- Cost
- Delivery Speed
- Risk
- Customer Satisfaction
- Sustainability

Every decision creates trade-offs, so businesses must choose the combination that best fits their customers and strategy.

## Files

- `Supply_Chain_Builder.html` — Complete single-file React application
- `screenshots/overview.png` — Welcome and company screen
- `screenshots/crisis.png` — Supply chain decision screen
- `screenshots/warroom.png` — Strategy selection screen
- `screenshots/ai.png` — Live metrics and optimization screen
- `screenshots/results.png` — Final optimization dashboard

## Git Commands

```bash
git add Day30
git commit -m "Add Day30 Supply Chain Builder"
git push origin main