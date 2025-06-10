# RL-Bed-Allocation-System
the output:
![image](https://github.com/user-attachments/assets/05e85b0d-3e17-4bb6-9907-49c05ee4e7bd)

Feature Importance: 'Age', 'Gender', 'Medical Condition', 'Admission Type', and 'Billing Amount' were identified as crucial for ICU bed allocation.
Outlier Handling: Outliers in 'Billing Amount' were addressed via IQR clipping, although no outliers were detected in the data.
Feature Engineering: A 'Severity_Score' was created, combining medical condition, admission type, and billing amount into a single weighted metric. 'Length_of_Stay' and 'Age_Group' were engineered.
Data Splitting: Stratified splitting was initially attempted but failed due to insufficient samples in some strata. Non-stratified splitting was used instead.
Model Optimization: A grid search optimized the RL model's hyperparameters (learning_rate, discount_rate, exploration_decay_rate), leading to the best configuration of 0.01, 0.99 and 0.001 respectively.
Model Evaluation: The optimized RL model (total reward: 1708.5) underperformed compared to the simple FCFS baseline (total reward: 2138.0).
Insights or Next Steps
Refine the RL Model: The current RL model's performance is unsatisfactory. Consider more sophisticated RL algorithms (e.g., Deep Q-Networks) and more comprehensive state and reward functions that accurately reflect the complexities of ICU bed allocation.
Explore Alternative Reward Functions: The simplistic reward function may not adequately capture the nuances of efficient ICU bed allocation. Design a more robust reward function that incorporates factors beyond just severity score changes, possibly including length of stay, resource utilization, and patient mortality.
