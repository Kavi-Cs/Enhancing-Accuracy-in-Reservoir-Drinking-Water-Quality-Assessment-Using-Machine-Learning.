Enhancing Accuracy in Reservoir Drinking Water Quality Assessment Using Machine Learning
This repository contains the research and implementation of a Machine Learning-based system designed to classify water potability. Conducted at the Electronics & Computing Laboratory, University of Colombo, this project focuses on optimizing sensor-based parameters to ensure safe drinking water monitoring.

Supervised by: Dr. Siyath Gunawardena & Dr. Luckshitha S. Liyanage

📌 Project Overview
Traditional water quality monitoring can be slow and resource-intensive. This project leverages Random Forest Classification to provide real-time, high-accuracy potability assessments based on key chemical properties.

Our core focus was Safety First: minimizing False Negatives (instances where contaminated water is wrongly classified as safe) to protect public health.

🚀 Key Features
#Statistical Validation: Rigorous T-tests performed to ensure feature significance ($p < 0.05$)
#High Precision Modeling: Achieved up to 97.07% training accuracy using optimized feature subsets.
#Deployment Ready: Includes a pipeline for saving/loading models (joblib/pickle) to evaluate unseen datasets automatically.
#Feature Engineering: Analysis of pH, Dissolved Oxygen (D.O.), and Conductivity interactions.

📊 Performance & Findings
Model Comparison
We observed a significant performance leap by moving from baseline statistical methods to optimized Random Forest subsets.

Model / Feature Subset,Accuracy
Baseline Statistical Model,77.57%
Random Forest (pH & Conductivity),95.60%
Random Forest (pH & D.O.),95.60%
"Optimized Subset (pH, D.O., & Conductivity)",97.07%

Feature Importance
Through our analysis, we identified how much each parameter contributes to the model's decision-making:

pH: 82.38% (The dominant predictor)

Dissolved Oxygen (D.O.): 17.62%

Statistical Significance
Both [pH & D.O.] and [pH & Conductivity] pairs yielded p-values < 0.05, rejecting the null hypothesis and confirming that these parameters are scientifically sound predictors for potability.

🛠️ Tech Stack
Language: Python

Libraries: Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn

Algorithms: Random Forest Classifier, T-test (SciPy)

📂 Project Structure
├── Data/               # Raw and processed datasets
├── Models/             # Saved .pkl or .joblib model files
├── Notebooks/          # Jupyter notebooks with EDA and Model Training
├── src/                # Source code for the deployment pipeline
└── README.md

⚙️ Installation & Usage
1.Clone the repository:
git-clone https://github.com/Kavi-Cs/Enhancing-Accuracy-in-Reservoir-Drinking-Water-Quality-Assessment-Using-Machine-Learning.git
2.Install dependencies:
pip install -r requirements.txt
3.Run the evaluation script:
python evaluate_new_data.py --input data/unseen_water_data.csv

🎓 Acknowledgments
Special thanks to Dr. Siyath Gunawardena and Dr. Luckshitha S. Liyanage for their guidance at the Electronics & Computing Laboratory, Faculty of Science, University of Colombo.

Contact:[induwaraBarca1899@gmail.com]
