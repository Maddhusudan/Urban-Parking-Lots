Dynamic Pricing for Urban Parking Lots

Project Overview
This project implements a dynamic pricing system for urban parking lots. The system adjusts parking prices in real-time based on several features like traffic conditions, occupancy, queue length, and vehicle type. Additionally, it recommends rerouting for full parking lots to nearby alternatives. The project is part of the Summer Analytics 2025 Capstone program.

Tech Stack
- Language: Python
- Libraries:
  - Pandas, NumPy (data manipulation)
  - Bokeh (time-series visualization)
  - Plotly (optional map-based visuals)
  - Matplotlib (general plotting)
- Environment: Jupyter Notebook or Google Colab

Project Architecture
Data Flow:
1. dataset.csv: Parking Data
2. Data Preprocessing
3. Model Branches:
   - Baseline Pricing Model
   - Demand-Based Model
   - Competitive Pricing Model
4. Combined Price Table
5. Rerouting Logic
6. Outputs:
   - Real-Time Simulation
   - Visualizations (Bokeh/Plotly)

Workflow
1. Data Ingestion: Load the dataset with parking data every 30 minutes over 73 days.
2. Preprocessing: Convert categorical features (traffic, vehicle type) into numerical formats. Merge date and time.
3. Baseline Pricing: Price increases linearly with occupancy.
4. Demand-Based Pricing: Price is influenced by occupancy, queue, traffic, special days, and vehicle type.
5. Competitive Pricing: Uses the Haversine formula to adjust pricing based on nearby parking lots.
6. Rerouting Suggestions: For full lots, recommend nearby available lots within 1km.
7. Visualization: Show real-time and historical price trends with Bokeh.

Dataset
- Data Format: CSV
- Fields:
  - SystemCodeNumber, Latitude, Longitude
  - Capacity, Occupancy, QueueLength
  - TrafficConditionNearby, VehicleType
  - LastUpdatedDate, LastUpdatedTime
- Size: 14 parking lots, 73 days, 30-minute interval

Repository Structure
- dataset.csv
- dynamic_pricing_notebook.ipynb
- README.md
- report.pdf (optional)

How to Run
1. Clone the repository:
   git clone https://github.com/Maddhusudan/Urban-Parking-Lots
   cd parking-pricing
2. Install dependencies:
   pip install pandas numpy bokeh
3. Open the Jupyter Notebook:
   jupyter notebook dynamic_pricing_notebook.ipynb
4. Run all cells and upload dataset.csv

Additional Notes
- All models are implemented from scratch in Python.
- Bokeh is used for browser-based, interactive plotting.
- Plotly map-based visualization is optional (disabled by default).
- Streamlit version is under development.

Future Enhancements
- Streamlit dashboard version
- Real-time API integration for live data
- Heatmap visualizations of pricing trends
- Dockerized deployment for easy setup



Repository Access
This repository is public. If required, access has been granted to reviewers. All files are documented and runnable.
