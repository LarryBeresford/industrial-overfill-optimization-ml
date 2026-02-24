# industrial-overfill-optimization-ml
Machine Learning system for real-time pressure calibration in high-speed food production lines. Optimized depositing accuracy by 90% using fluid rheology variables.
Business Challenge
In high-speed food manufacturing lines, overfilling represents a critical source of raw material waste and financial loss. In this specific production line, the final product exhibited an average deviation of +10g over the target weight.

The process involves a batch-type reactor where flour, water, and a variable percentage of rework material (0% to 20%) are mixed. This mixture is then transferred to a depositing station equipped with 16 pneumatic nozzles. The primary challenge was that the fluid's rheological properties (viscosity and turbidity) fluctuated constantly due to:

Rework Ratio: The manual addition of reprocessed material altered the fluid's density and flow behavior.

Thermal Variance: Changes in ambient temperature, particularly during afternoon shifts, directly affected the fluid's temperature and its viscosity.

Traditional manual calibration based on static pressure charts (measured in Pascals) proved insufficient to handle these dynamic variables, leading to inconsistent depositing weights and substantial material waste.

Technical Solution
To address this variability, a predictive Machine Learning model was implemented to serve as a real-time calibration assistant for line supervisors.

The system operates by analyzing three key input variables:

Fluid Temperature: Monitored via inline sensors to account for viscosity changes.

Turbidity/Viscosity Index: Derived from the rework percentage and sensor data to understand fluid thickness.

Rework Percentage: Recorded per batch (1-hour intervals) to adjust the predictive logic.

Methodology:

Data Collection: Comprehensive sampling across four critical stations (initial depositing, filling, and coating).

Feature Engineering: Analysis of the interaction between ambient temperature and fluid behavior, identifying the depositing stage as the most critical variance point.

Modeling: A regression model was trained to predict the optimal air pressure (Pascals) required for each specific batch condition to hit the target weight precisely.

Business Impact
Financial Impact: Achieved an annualized saving of $80M MXN through the reduction of raw material waste.

Waste Reduction: 90% decrease in overfill-related waste by stabilizing the depositing mean.

Process Stability: Eliminated weight outliers and ensured compliance with strict quality standards without sacrificing production speed.

Operational Efficiency: Shifted from reactive, manual "trial and error" calibration to a proactive, data-driven precision model.

Tech Stack
Language: Python (Pandas, Scikit-learn, NumPy).

Techniques: Linear/Non-linear Regression, Feature Scaling, Outlier Detection.

Tools: SQL for historical data extraction, sensor integration simulations, and Industrial IoT (IIoT) logic.

Project Structure
data/: Synthetic datasets mirroring the rheological behavior of the production line.

notebooks/: Exploratory Data Analysis (EDA) and model training documentation.

scripts/: Python functions for real-time pressure calculation.

requirements.txt: List of necessary libraries for replication.
