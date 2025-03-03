# 🛒 Recommender System for E-commerce Products

This project implements a **collaborative filtering-based recommender system** for an e-commerce platform using the **Amazon Electronics dataset**.  
The goal is to recommend products to users based on their past interactions and the behaviors of similar users and products.

---

## 📂 Repository Structure

```
Recommender_System_Ecommerce/
│
├── Dataset/
│   └── ratings_Electronics.csv   # Dataset containing user-product ratings
│
├── Notebooks/
│   ├── Recommender_System_Ecommerce.ipynb   # Full notebook with EDA, filtering, CF, SVD, and recommendations
│   └── recommender_system_ecommerce.py
│
└── README.md                    # Project documentation (this file)
```

---

## 📊 Project Overview

In this project, we build a **product recommendation system** by applying:
- **Collaborative Filtering (CF)** techniques:
  - User-User CF
  - Item-Item CF
- **Matrix Factorization** using **Singular Value Decomposition (SVD)**.
- **Correlation-based similarity** to identify highly related products.
- Data preprocessing, exploratory data analysis (EDA), and evaluation using **RMSE**.

---

## ✅ Features

- Recommend similar products using **Item-Item** and **User-User CF**.
- Build a **correlation matrix** to suggest products based on similarity.
- Apply **SVD** for dimensionality reduction and hidden feature extraction.
- Evaluate model performance using **RMSE** and **cross-validation**.
- Analyze rating distributions, popular products, and rating behaviors.
- Scalable approach for large datasets like **Amazon product reviews**.

---

## 🔧 Tech Stack

| Tool/Library | Purpose |
|--------------|---------|
| Python       | Programming Language |
| Pandas, NumPy | Data Processing |
| Matplotlib, Seaborn | Visualization |
| scikit-learn | Matrix Decomposition (SVD) |
| Surprise | Collaborative Filtering Models |
| Jupyter Notebook | Interactive Development |

---

## 📁 Dataset

- **Name**: `ratings_Electronics.csv`
- **Source**: [Amazon Product Reviews Dataset](https://www.kaggle.com/datasets/saurav9786/amazon-product-reviews)
- **Attributes**:
  - `userId`: Unique identifier for each user.
  - `productId`: Unique identifier for each product.
  - `Rating`: Rating provided by the user (1 to 5).
  - `timestamp`: Time of rating (ignored in this project).

---

## 🔄 Methodology

### 1️⃣ Data Preprocessing
- Loaded and cleaned the dataset.
- Filtered out users and products with minimal interactions.
- Reduced data size for computational efficiency.

### 2️⃣ Exploratory Data Analysis (EDA)
- Analyzed rating distribution.
- Identified popular products.
- Explored rating patterns of frequent users.

### 3️⃣ Collaborative Filtering
- **Item-Item CF**: Recommending products based on product similarities.
- **User-User CF**: Recommending products based on similar users' behavior.
- Evaluated using **RMSE** with cross-validation.

### 4️⃣ Matrix Factorization (SVD)
- Reduced data dimensionality to extract latent factors.
- Built a **correlation matrix** from decomposed features.
- Recommended top N similar products based on correlations.

### 5️⃣ Product Recommendation System
- Developed a reusable function to recommend the top N similar products for any given product.
- Optional correlation threshold to control recommendation strength.

---

## 🧠 Results

| Model | RMSE (Cross-Validation) |
|-------|-------------------------|
| Item-Item CF | ~1.3414 |
| User-User CF | ~1.3471 |
| SVD (correlation-based recommendations) | High-quality recommendations based on latent features |

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Recommender_System_Ecommerce.git
   cd Recommender_System_Ecommerce
   ```

2. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebooks in **Jupyter Notebook** or **Google Colab**:
   - `Notebooks/Recommender_System_Ecommerce.ipynb`
   - `Notebooks/recommender_system_ecommerce_SVD.ipynb`

4. Follow the notebook cells to run EDA, build models, and generate recommendations.

---

## 🎯 Future Improvements
- ✅ Integrate **content-based filtering** using product metadata (titles, categories).
- ✅ Deploy as an API or web app for real-time recommendations.
- ✅ Add real-world evaluation through **user engagement metrics**.
- ✅ Explore deep learning-based recommendation systems.

---

## ✨ Author
- **Name**: Saad Abdullah
- **LinkedIn**: [https://www.linkedin.com/in/saadabdullah15/]  
- **GitHub**: [https://github.com/saadabdullah-15]  

---

## 📜 License
This project is licensed under the **MIT License**.

