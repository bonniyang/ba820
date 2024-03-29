This project focusing on NLP is completed by Yu-Chun (Lila) Su, Shuo-Ming (Chris) Kuo, Pei-Hsin (Bonny) Yang, Yu-Chin (Alyssa) Chen for the BA820 project.

Dataset source

https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies

Problem Statement & Motivation

With the abundance of movies available, users often face difficulty in finding content that aligns with their tastes. However, we believe that movies favored by the same audience or movies with high box office revenue will share certain common characteristics to some extent. Leveraging this information can help platforms better select movies for release and assist production companies in creating successful films. Our primary objective is to find the patterns and develop a recommendation system that employs NLP techniques on movie overviews. Additionally, we aim to incorporate other relevant variables for clustering to enhance the accuracy and effectiveness of our recommendation system.

Data Analysis

Clustering Analysis: 
For our clustering analysis, we employed PCA along with a scree plot to determine the optimal number of components that effectively capture the most variance in the dataset. This process helped in reducing the dimensionality of the data while retaining as much information as possible. The cumulative explained variance ratio plot revealed that a minimum of 9 components is necessary to capture at least 85% of the variance, indicating the key dimensions for representing the dataset effectively (Figure 2). Furthermore, we attempted to employ t-SNE to further analyze the data. However, despite trying the number of components ranging from 3 to 9, the computation ran for 60 minutes without yielding results. Consequently, we retained the results from PCA for our analysis.
Additionally, we utilized k-means clustering to identify inherent patterns and groupings within the data. To determine the optimal number of clusters for k-means, we constructed an Elbow plot, which depicts the relationship between the number of clusters and the within-cluster sum of squares. The optimal number of clusters for our dataset would be 5.

NLP Analysis: 
For our NLP analysis, we used the "overview" column of our dataset. We utilized techniques such as n-gram analysis, TF-IDF, word2vec, and GloVe. By comparing the results obtained from these techniques, we continued to iterate and improve our NLP techniques to enhance the accuracy and relevance of our movie recommendations. Our goal is to fine-tune our algorithms and explore additional tokenization approaches to deliver even more precise suggestions to users, ensuring a satisfying and personalized movie-watching experience.
Additionally, parameter tuning was conducted in the Word2Vec model to optimize its performance. We adjusted the vector_size parameter, exploring values of 100 and 300 to refine the dimensionality of single-word embeddings and capture more semantic relationships. Further adjustments included changing the number of windows from 3 to 5, expanding the context window of word embeddings to encompass broader contextual information. Ultimately, the final parameters were selected based on computational efficiency and the resultant performance, followed by a comparative analysis with other NLP models.
