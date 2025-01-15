# **Netflix Show Clustering**

## **Overview**
Netflix is the world's largest online streaming service provider, with over 220 million subscribers as of Q2 2022. This project aims to enhance the user experience by clustering Netflix shows into meaningful groups based on their attributes. By analyzing similarities between shows, this clustering can be used to create personalized recommendations for users, improving satisfaction and reducing churn.

---

## **Features**
- Analyze and preprocess Netflix show data.
- Cluster shows into groups based on key attributes.
- Visualize clusters for better understanding.
- Utilize clustering for personalized recommendations.

---

## **Attributes Used**
Clustering is performed using the following attributes:
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

2. **Text Embedding with Transformers**:
   - Use `SentenceTransformer` (`all-MiniLM-L6-v2`) to generate semantic embeddings for the text.

3. **Dimensionality Reduction**:
   - Apply PCA (Principal Component Analysis) to reduce dimensionality while retaining at least 80% of variance.

4. **Clustering**:
   - Perform K-Means clustering on the reduced embeddings.
   - Evaluate cluster quality using the Silhouette Score.

5. **Visualization**:
   - Visualize clusters in 2D using PCA-reduced embeddings.
   - Analyze cluster characteristics.

---

## **Technologies Used**
- **Programming Language**: Python
- **Key Libraries**:
  - `pandas`, `numpy` for data preprocessing.
  - `sentence-transformers` for generating embeddings.
  - `scikit-learn` for PCA and clustering.
  - `matplotlib`, `seaborn` for visualization.

---




