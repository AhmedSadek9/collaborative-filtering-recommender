# Collaborative Filtering Recommendation System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)

A complete implementation of User-Based and Item-Based Collaborative Filtering using the MovieLens 100K dataset.

---

## 📁 Project Structure

 # Movie metadata │ └── u.user # User demographics │ ├── notebooks/ # Jupyter notebooks │ ├── 01_data_preprocessing.ipynb │ ├── 02_user_based_cf.ipynb │ ├── 03_item_based_cf.ipynb │ └── 04_evaluation_and_visualization.ipynb │ ├── src/ # Source code │ ├── data_loader.py # Data loading and preprocessing │ ├── recommender.py # CF algorithms implementation │ └── evaluation.py # Metrics computation │ ├── results/ # Output files │ ├── recommendations/ # Generated recommendations │ └── metrics/ # Evaluation results │ ├── requirements.txt # Python dependencies └── README.md # Project documentation

yaml
Copy
Edit




---

## 🚀 Features

- **Two Collaborative Filtering Approaches**:
  - ✅ User-Based CF
  - ✅ Item-Based CF

- **Comprehensive Evaluation Metrics**:
  - RMSE, MAE
  - Precision@K, Recall@K
  - Coverage, Diversity

- **Data Processing**:
  - User-item matrix creation
  - Missing value handling
  - Similarity matrix computation

---

## 🛠️ Installation

1. **Clone the repository:**
```bash
git clone https://github.com/yourusername/collaborative-filtering-recommender.git
cd collaborative-filtering-recommender
pip install -r requirements.txt

mkdir -p data && cd data
wget https://files.grouplens.org/datasets/movielens/ml-100k.zip
unzip ml-100k.zip && mv ml-100k/* . && rm -r ml-100k ml-100k.zip
cd ..



📈 Usage
🔹 Running Notebooks
Execute the Jupyter notebooks in order:

01_data_preprocessing.ipynb - Data loading and cleaning

02_user_based_cf.ipynb - User-based collaborative filtering

03_item_based_cf.ipynb - Item-based collaborative filtering

04_evaluation_and_visualization.ipynb - Results and comparison



from src.data_loader import load_and_preprocess
from src.recommender import CollaborativeFiltering
from src.evaluation import RecommenderEvaluator

# Load data
ratings, movies, users = load_and_preprocess()

# Initialize recommender
cf = CollaborativeFiltering(ratings, movies)
cf.create_matrices(fillna=0)
cf.compute_similarities()

# Get recommendations for a specific user
user_recs = cf.recommend_items(user_id=1, n=5, method='user')

# Evaluate
test_ratings = ratings.sample(100)
metrics = RecommenderEvaluator.evaluate_all(
    test_ratings=test_ratings,
    recommendations={1: [r[0] for r in user_recs]},
    y_true=test_ratings['rating'],
    y_pred=[r[1] for r in user_recs],
    catalog_size=len(movies)
)



📊 Sample Evaluation Results

Metric	User-Based CF	Item-Based CF
RMSE	0.92	0.89
Precision@5	0.45	0.52
Recall@5	0.38	0.41
Coverage	62%	58%
Diversity	0.73	0.68
