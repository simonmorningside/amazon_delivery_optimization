# Amazon Delivery Optimization

## Overview
This capstone project builds an optimization and decision-support system for e-commerce logistics. The goal is to minimize fulfillment cost per order while maximizing delivery speed and reliability. 

The project progresses from identifying optimal tradeoffs (Phase 1) to making real-world, explainable business decisions (Phase 2), simulating how a company like Amazon balances efficiency and customer experience at scale.

---

## Business Problem
Amazon’s logistics network must balance two competing objectives:
- **Minimize shipping cost per order**
- **Maximize delivery speed and on-time performance**

Faster delivery improves customer satisfaction and competitiveness but significantly increases operational costs. Slower delivery reduces costs but risks losing customers.

This project models that tradeoff and builds a system that:
1. Identifies efficient strategies
2. Filters them based on real-world constraints
3. Selects the best option given current business conditions

---

# Part 1: Optimization Engine (Complete ✓)

## What It Does
This optimization engine analyzes 150 synthetic logistics scenarios based on delivery distance and warehouse load to identify the Pareto frontier of efficient solutions that balance:

- Shipping cost (USD)
- Delivery time (hours)

## Key Findings
- ~150 total solutions analyzed  
- ~3% of solutions are Pareto optimal  
- ~145 dominated (inefficient) solutions identified  
- Clear tradeoff between cost and speed:
  - Low-cost ground shipping performs well in many cases  
  - Same-day delivery is fastest but significantly more expensive  

## Outputs
- Pareto frontier visualization  
- Tradeoff analysis plots  
- Strategy comparisons (cost, speed, balanced)

## Running the Analysis
1. Install required packages:
2. Open `optimization_engine.ipynb`
3. Run all cells in order
4. Outputs will be saved to the `images/` folder

---

# Part 2: Constraint-Aware Decision Agent (Complete ✓)

## What It Does
The decision agent extends the optimization engine by taking the Pareto frontier and applying:

1. **Business Constraints**
- Budget limits (shipping cost caps)
- Service-level requirements (delivery time limits)
- Capacity limits (warehouse load thresholds)

2. **Scenario-Based Decision Logic**
- Adjusts decisions based on business conditions (cost pressure, urgency, competition)

3. **Explainable Recommendations**
- Outputs a single recommended strategy with clear reasoning

This transforms the system from identifying optimal solutions to **making actionable business decisions**.

---

## Key Findings
- Applied 3 real-world business constraints  
- Reduced Pareto frontier to a smaller set of feasible solutions  
- Tested across 3 scenarios:
- Budget-focused → lowest cost solution selected  
- High urgency → fastest delivery selected  
- Balanced → tradeoff solution selected  

**Final Recommendation:**  
A balanced logistics strategy that minimizes both cost and delivery time while satisfying operational constraints.

---

## Agent Features
- **Constraint-Aware**: Only considers realistic, implementable solutions  
- **Context-Sensitive**: Adapts recommendations based on business conditions  
- **Explainable**: Provides human-readable reasoning  
- **Scenario-Tested**: Validated across multiple operating environments  

---

## Example Scenarios
- **Budget Pressure** → prioritize cost efficiency  
- **Peak Demand Surge** → prioritize speed  
- **Normal Operations** → balanced optimization  

---

## Outputs
- Scenario comparison table  
- Multi-panel decision visualizations  
- Executive recommendation summary  
- Exported decision brief (`FINAL_RECOMMENDATION.txt`)

---

## Project Structure
optimization_engine.ipynb
images/
    pareto_frontier_analysis.png
    feasible_region.png
    scenario_recommendations.png
    agent_decision_process.png
    final_recommendation_summary.png
FINAL_RECOMMENDATION.txt
README.md
requirements.txt


---

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

---

## Key Insights
- Most possible solutions are inefficient and should never be chosen  
- Real-world constraints significantly reduce available options  
- Optimal decisions depend heavily on business context  
- A single “best” solution does not exist—only context-dependent tradeoffs  

---

## Limitations
- Synthetic dataset (not real Amazon data)  
- Limited variables (distance, load, transport mode)  
- Does not include real-time factors (traffic, weather, disruptions)  
- Uses rule-based logic instead of learned models  

---

## Future Improvements
- Integrate real-world logistics datasets  
- Add machine learning for adaptive decision policies  
- Incorporate real-time data (demand, traffic, inventory)  
- Expand to additional objectives (customer satisfaction, emissions)  
- Deploy as a dashboard or API  

---

## How to Run
1. Clone the repository  
2. Install dependencies: pip install -r requirements.txt
3. Run the notebook: jupyter notebook optimization_engine.ipynb


---

## Final Deliverable
This project demonstrates a complete decision pipeline: Data → Optimization → Constraints → Decision Agent → Business Recommendation

It showcases the ability to:
- Solve multi-objective optimization problems  
- Apply real-world business constraints  
- Build explainable AI systems  
- Communicate results to non-technical stakeholders  

---

## Author
Simon Zychowski

---

## License
This project is for educational and portfolio purposes.
