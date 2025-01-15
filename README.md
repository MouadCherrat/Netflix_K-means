Netflix Show Clustering Project
Overview
Netflix is the world's largest online streaming service provider, with over 220 million subscribers as of Q2 2022. This project aims to enhance the user experience by clustering Netflix shows into meaningful groups. By identifying similarities between shows, we can offer personalized recommendations to users, ultimately improving customer satisfaction and reducing churn.

The primary goal is to classify Netflix shows into clusters where:

Shows within a cluster share similar characteristics.
Shows in different clusters are distinct.
Project Goals
Analyze Netflix show data to identify patterns and relationships.
Cluster shows using attributes like director, cast, genre, country, and description.
Visualize clusters to interpret similarities and differences.
Provide insights to improve user recommendations on the platform.
Attributes Used for Clustering
The clustering process focuses on the following attributes:

Director: The individual(s) who directed the show.
Cast: The actors involved in the show.
Country: The country where the show was produced.
Genres: The categories or genres of the show.
Description: A brief summary of the show's storyline.
Key Steps
1. Data Preprocessing
Combine selected attributes into a single column called clustering_attributes.
Clean the text by removing non-ASCII characters, stopwords, and punctuation.
Convert all text to lowercase.
2. Embedding Generation Using Transformers
Use the SentenceTransformer model (all-MiniLM-L6-v2) to convert textual data into dense vector embeddings.
These embeddings capture semantic relationships between shows and are used as input for clustering.
3. Dimensionality Reduction
Apply Principal Component Analysis (PCA) to reduce the dimensionality of embeddings while retaining at least 80% of the variance.
Simplifies clustering and improves computational efficiency.
4. Clustering
Use K-Means Clustering to group shows into distinct clusters.
Evaluate clustering quality using the Silhouette Score.
5. Visualization
Visualize the clusters in 2D using PCA-reduced embeddings.
Analyze each cluster's characteristics to interpret its composition.
