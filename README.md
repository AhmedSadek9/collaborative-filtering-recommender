🎬 Collaborative Filtering Recommendation System
📝 Overview
This project implements a Collaborative Filtering-based Recommendation System using the MovieLens 100K dataset, a classic benchmark for recommender systems. The system recommends movies to users by analyzing user preferences and leveraging both user-based and item-based collaborative filtering techniques.

The solution is modular, extensible, and supports both notebook-driven exploration and script-based execution.

🚀 Features
✅ Core Features
User-Based Collaborative Filtering: Find similar users and recommend movies they liked.

Item-Based Collaborative Filtering: Recommend items similar to those the user rated highly.

Evaluation Metrics: RMSE, Precision@K, Recall@K to assess model performance.

Top-N Recommendations: Generate personalized top-N recommendations for any user.

Data Preprocessing: Clean, merge, and encode datasets effectively.

🌟 Advanced Features
Model Comparison Dashboard: Compare evaluation metrics across different models.

Similarity Matrix Visualization: Heatmaps showing user-user and item-item similarities.

Parameter Tuning: Ability to tune similarity metrics (cosine, Pearson, etc.) and neighborhood size.

Cold-Start Handling (Optional): Simple heuristics to recommend popular items for new users.

Interactive User Input (Optional via CLI or Streamlit): Let users input their ratings and receive recommendations in real time.

Caching Mechanism (Optional): Reduce computation by caching similarity scores and predictions.

Exploratory Data Analysis (EDA): Understand rating distributions, popularity trends, user behavior, and sparsity.

📁 Project Structure
bash
Copy
Edit
collaborative-filtering-recommender/
│
├── README.md
├── requirements.txt
│
├── data/
│   ├── u.data
│   ├── u.item
│   └── u.user
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_user_based_cf.ipynb
│   ├── 03_item_based_cf.ipynb
│   └── 04_evaluation_and_visualization.ipynb
│
├── src/
│   ├── __init__.py
│   ├── data_loader.py
│   ├── recommender.py
│   ├── evaluation.py
│   ├── similarity_utils.py           # (New) Similarity metrics and helper functions
│   └── visualization.py              # (New) Custom plots and visualizations
│
├── results/
│   ├── top_n_recommendations.csv
│   └── evaluation_metrics.json
│
└── dashboard/                        # (Optional) For interactive dashboards (e.g., Streamlit)
    └── app.py
🛠️ Installation & Setup
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/yourusername/collaborative-filtering-recommender.git
cd collaborative-filtering-recommender
2. Set Up a Virtual Environment (optional)
bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
3. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
📚 Dataset
Download the dataset from Kaggle and place the files in the data/ directory.

🧪 How to Run
🔬 Jupyter Notebook Workflow
Run each notebook in order:

01_data_preprocessing.ipynb

02_user_based_cf.ipynb

03_item_based_cf.ipynb

04_evaluation_and_visualization.ipynb

⚙️ Python Script Workflow
Execute modules from the src/ folder:

bash
Copy
Edit
python src/data_loader.py
python src/recommender.py
python src/evaluation.py
📊 Evaluation
We evaluate recommendations using:

RMSE (Root Mean Square Error)

Precision@K

Recall@K

Sample output stored in:

results/evaluation_metrics.json

results/top_n_recommendations.csv

📈 Visualizations
User-User Similarity Matrix (Heatmap)

Item-Item Similarity Matrix (Heatmap)

Rating Distributions

Precision/Recall vs. K plot

RMSE over different neighborhood sizes

🧠 Concepts Used
Collaborative Filtering

Nearest Neighbors

Similarity Metrics: Cosine, Pearson

Evaluation Metrics

Matrix Factorization (optional future extension)

📦 Dependencies
Python 3.x

pandas, numpy

scikit-learn

scikit-surprise

matplotlib, seaborn

streamlit (optional for dashboard)

Install all via:

bash
Copy
Edit
pip install -r requirements.txt
