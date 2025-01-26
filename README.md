# **Netflix Show Clustering**

## **Overview**
Netflix is the world's largest online streaming service provider, with over 220 million subscribers as of Q2 2022. This project aims to enhance the user experience by clustering Netflix shows into meaningful groups based on their attributes. By analyzing similarities between shows, this clustering can be used to create personalized recommendations for users, improving satisfaction and reducing churn. Additionally, advanced techniques such as K-Means, Support Vector Machines (SVM), Information Gain, Mutual Information (MI), and the Firefly Algorithm are integrated to optimize clustering and classification.

---

## **Features**
- Analyze and preprocess Netflix show data.
- Cluster shows into groups based on key attributes using K-Means and the Firefly Algorithm.
- Classify shows using Support Vector Machines (SVM).
- Optimize feature selection using Information Gain and Mutual Information (MI).
- Visualize clusters and classification results for better understanding.
- Utilize clustering for personalized recommendations.

---

## **Attributes Used**
Clustering and classification are performed using the following attributes:
- **Director**: The individual(s) directing the show.
- **Cast**: The actors featured in the show.
- **Country**: The country of production.
- **Genres**: The category/genre of the show.
- **Description**: A short summary of the show.

---

## **Project Workflow**
1. **Data Preprocessing**:
   - Combine selected attributes into a single column.
   - Clean data by removing non-ASCII characters, stopwords, and punctuation.
   - Convert all text to lowercase.

2. **Feature Selection with Information Gain and Mutual Information (MI)**:
   - Calculate the importance of each feature based on Information Gain.
   - Use Mutual Information to evaluate feature dependencies and select the most relevant features for clustering and classification.

3. **Text Embedding with Transformers**:
   - Use `SentenceTransformer` (`all-MiniLM-L6-v2`) to generate semantic embeddings for the text.

4. **Dimensionality Reduction**:
   - Apply PCA (Principal Component Analysis) to reduce dimensionality while retaining at least 80% of variance.

5. **Clustering**:
   - Perform K-Means clustering to partition data into groups.
   - Use the Firefly Algorithm to refine cluster centers for optimal grouping.
   - Evaluate cluster quality using the Silhouette Score.

6. **Classification with SVM**:
   - Train an SVM classifier using labeled data.
   - Use the classifier to assign labels to new shows.

7. **Visualization**:
   - Visualize clusters in 2D using PCA-reduced embeddings.
   - Analyze cluster and classification characteristics.

---

## **Technologies Used**
- **Programming Language**: Python
- **Key Libraries**:
  - `pandas`, `numpy` for data preprocessing.
  - `sentence-transformers` for generating embeddings.
  - `scikit-learn` for PCA, clustering (K-Means), classification (SVM), and feature selection.
  - `matplotlib`, `seaborn` for visualization.
  - Custom implementation of the Firefly Algorithm.

---
