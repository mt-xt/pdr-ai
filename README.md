# pdr-ai
GROUP 17 PROJECT PROPOSAL ECS 170

GROUP MEMBERS: Amirta Balakrishnan, Angel Jauregui, Matthew Abalos, Nathan Castellon, Quintin Tucker, Rayan Narayanaswamy, Sasha Karelina, Sia Puri, Tyler Guo

BACKGROUND: 
According to the CDC, diabetes has become one of the fastest-growing global health concerns, with a projected 38 million individuals diagnosed with some form of diabetes in the U.S. alone. A staggering 98 million individuals are classified as pre-diabetic, and these numbers continue to rise every year.

PROPOSAL:
For our ECS 170 final project, our group aims to perform a System Implementation and Optimization study where we will design, train, and optimize an AI system capable of predicting diabetes risk using supervised learning.
Our focus is to implement a complete machine-learning pipeline, covering data preprocessing, feature engineering, model training, hyperparameter tuning etc, to demonstrate how systematic optimization improves both predictive performance and model transparency.
We are interested not only in achieving high accuracy but also in understanding which factors (e.g., BMI, blood pressure, age, lifestyle habits) most strongly influence the model’s decisions.

DATASET:
We will be using the ‘Diabetes Health Indicators Dataset’ to train our model, which can be found on Kaggle.. This dataset is a synthetically curated dataset that mimics statistical distributions of real-world medical research and health patterns. 
It includes 100,000 patient profiles with a variety of health and lifestyle factors:
Physical metrics: age, ethnicity, familial diabetic disposition, etc. 
Biometrics: cholesterol, glucose levels, blood pressure, heart disease, stroke, etc.
Lifestyle factors: physical activity, smoking and alcohol use, diet, etc. 
We will clean and normalize the data, to then be split into training, validation and testing sets.

AI SYSTEM:
Through some research, we found a model called XGBoost (Extreme Gradient Boosting) as a viable option for our core learning algorithm.  XGBoost is a high-performance tree-based ensemble method that can handle both regression and classification tasks, making it suitable for diabetes risk prediction. 
We selected it because it is a pretty well known and widely used algorithm that efficiently models relationships between features, provides the ability for us to update hyperparameters for tuning and optimization, integrates a Tree SHAP which gives us insight into how a feature contributes to our model’s predictions, and overall just has a lot of open-source documentation and libraries out there. The diagram depicts the sequential flow from data preprocessing to XGBoost model training, and analysis using Tree SHAP.

SCAFFOLDING/EXTERNAL RESOURCES:
Libraries:
XGBoost as our main learning algorithm
Scikit-learn: to preprocess and split data
Pandas, NumPy, Matplotlib: common python libraries used for data manipulation and analysis

FEASIBILITY, RISKS, & MITIGATION:
This project is feasible within a 4-5 week timeline.
Week 1: Data cleaning, feature exploration, baseline models
Week 2: Hyperparameter tuning for XGBoost and Random Forest
Week 3: Model comparison and calibration
Week 4: Interpretability analysis and visualization
Week 5: Final results, report, and presentation preparation

Potential Risks & Mitigation:

Imbalanced data: There might be way more non-diabetic people than diabetic ones in our dataset. This can make the model lazy - it might just keep predicting ‘non-diabetic’ to get high accuracy.
→ Fix: We will rebalance the data by giving more weight to diabetic cases or making extra copies of them so the model pays equal attention to both groups.
Overfitting: The model might get too good at fitting the training data but then perform poorly on new data because it ‘memorized’ patterns that don’t generalize.
→ Fix: We will stop training when accuracy on unseen data stops improving and use regularization/a penalty for over-complex models to keep it from going overboard.

PRESENTATION CONSIDERATION:
We plan to visualize our pipeline and results with:
A system architecture figure showing data flow (from preprocessing to SHAP explanations)
Performance plots (ROC, confusion matrix)
SHAP summary and force plots for interpretability
A brief demo notebook or dashboard showing how feature inputs affect predicted risk. 
