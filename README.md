# 📦 Robust Supply Chain Optimization Using Monte Carlo Simulation
## 🌍 Global Supply Chain – Interactive Map

![Preview](images/supply_chain_map_preview.png)

🔗 [Click here to explore the interactive version](https://yourusername.github.io/your-repo-name/supply_chain_map.html)


This project implements a robust supply chain network design methodology using **Monte Carlo simulation** combined with **Linear Programming optimization**. The model accounts for **demand uncertainty** and helps in identifying the most cost-effective and reliable configuration of plants for an international business.

---

## 🧠 Objective
![image](https://github.com/user-attachments/assets/c9d1f7e4-5f3e-41d1-a31f-e7bc470e4fa9)

Design a supply chain network that minimizes:
- Fixed costs of opening manufacturing plants
- Variable costs of production and shipment  
…while handling **fluctuating demand across multiple countries** (USA, Germany, Japan, Brazil, India).

---

## 🔧 Technologies Used

- Python (Pandas, NumPy, Matplotlib)
- [PuLP](https://coin-or.github.io/pulp/) for Linear Programming
- Jupyter Notebook / Google Colab
- Excel files for input datasets

---

## 📁 Dataset Overview

| File Name              | Description                                  |
|------------------------|----------------------------------------------|
| `variable costs.xlsx`  | Manufacturing cost per unit by location      |
| `freight costs.xlsx`   | Freight cost per 1000 units                  |
| `fixed cost.xlsx`      | Fixed cost for low/high capacity plants      |
| `capacity.xlsx`        | Plant capacity (low/high)                    |
| `demand.xlsx`          | Baseline customer demand (in units/month)    |

---

## 🔄 Methodology

1. **Data Import**: Read costs, capacity, and demand data from Excel.
2. **Cost Modeling**: Calculate total variable cost = manufacturing + freight.
3. **Monte Carlo Simulation**:
   - Simulate 50 demand scenarios using a normal distribution with 20% std dev.
4. **Linear Programming**:
   - Solve a **Capacitated Plant Location Problem** for each demand scenario.
   - Constraints:
     - Each market’s demand must be fulfilled.
     - Total shipped ≤ selected plant capacity.
5. **Result Aggregation**:
   - Record total cost and chosen plant setup for each run.
   - Identify the most robust (frequent) plant configuration.

---

## 📊 Visual Output

- 📉 **Cost Distribution Histogram**: Shows how total cost varies over 50 simulations.
- 🏭 **Plant Selection Frequency**: Bar chart of how often each plant (by location and size) was chosen across simulations.

---

## ▶️ How to Run

1. Upload all Excel files in a Colab session.
2. Run the notebook from top to bottom.
3. View the final charts at the bottom for insights.

---

## 🚀 Future Improvements

- Add route-level visualization using `folium` or `plotly`.
- Integrate a dashboard using `Streamlit` or `Dash`.
- Test sensitivity to cost shocks (fuel, inflation, taxes).
- Add CO₂ or environmental cost layers.

---

## 📌 Project Highlights

- Combines **quantitative modeling** with **simulation**.
- Accounts for **real-world uncertainty** in demand.
- Offers **visual insights** into robust plant location decisions.
- Easily extendable to other industries (retail, FMCG, pharma).

---

## 📬 Contact

For academic, professional, or collaborative use, feel free to clone and extend this repository. Contributions welcome!

