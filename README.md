# 🎬 Collaborative Filtering Recommendation System

A Python-based recommendation system that leverages **Collaborative Filtering** techniques to suggest movies based on user preferences and interactions. Built using the **MovieLens 100K** dataset, the system includes both user-based and item-based collaborative filtering models, model evaluation, and optional visualizations.

---

## 📝 Project Description

The project focuses on building a recommender system that:

- Learns user preferences from the MovieLens 100K dataset.
- Implements **User-Based** and **Item-Based Collaborative Filtering**.
- Evaluates model accuracy using **RMSE**, **Precision@K**, and **Recall@K**.
- Outputs top-N movie recommendations tailored to each user.

Collaborative Filtering assumes that users with similar tastes will prefer similar items. This project brings that to life through data analysis, algorithm implementation, and metric evaluation.

---

## 📂 Project Structure

```
collaborative-filtering-recommender/
├── README.md
├── requirements.txt
├── data/
│   ├── u.data
│   ├── u.item
│   └── u.user
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_user_based_cf.ipynb
│   ├── 03_item_based_cf.ipynb
│   └── 04_evaluation_and_visualization.ipynb
├── src/
│   ├── __init__.py
│   ├── data_loader.py
│   ├── recommender.py
│   └── evaluation.py
└── results/
    ├── top_n_recommendations.csv
    └── evaluation_metrics.json
```

---

## ✅ Features

- Load and preprocess the MovieLens 100K dataset
- User-Based Collaborative Filtering
- Item-Based Collaborative Filtering
- Model Evaluation with RMSE, Precision@K, and Recall@K
- Top-N movie recommendations for users
- Optional visualizations for similarities and performance

---

## 🚀 Installation

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/collaborative-filtering-recommender.git
cd collaborative-filtering-recommender
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Download the dataset**

Download the MovieLens 100K dataset from [Kaggle](https://www.kaggle.com/datasets/prajitdatta/movielens-100k-dataset) and place the files in the `data/` directory.

---

## 🧪 Usage

You can explore the functionality using the provided Jupyter notebooks:

- **Step 1:** Load and preprocess data (`notebooks/01_data_preprocessing.ipynb`)
- **Step 2:** Apply user-based filtering (`notebooks/02_user_based_cf.ipynb`)
- **Step 3:** Apply item-based filtering (`notebooks/03_item_based_cf.ipynb`)
- **Step 4:** Evaluate model performance and visualize results (`notebooks/04_evaluation_and_visualization.ipynb`)

For script-based execution, refer to the modules in the `src/` directory.

---

## 🧰 Tech Stack

- **Python 3.x**
- **Libraries:** `pandas`, `numpy`, `scikit-learn`, `surprise`, `matplotlib`, `seaborn`
- **Dataset:** [MovieLens 100K](https://www.kaggle.com/datasets/prajitdatta/movielens-100k-dataset)
- **Environment:** Jupyter Notebooks / Python scripts

---

## 📈 Evaluation Metrics

- **Root Mean Squared Error (RMSE)**
- **Precision@K**
- **Recall@K**

Results are saved in the `results/` folder.

---

## 🤝 Contributing

Contributions are welcome! Feel free to submit pull requests or open issues.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 📧 Contact

For questions or suggestions, feel free to reach out or create an issue on the repository.

---
