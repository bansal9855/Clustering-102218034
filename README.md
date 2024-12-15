# Clustering Analysis

This project demonstrates clustering techniques applied to the Wine Quality dataset. It uses a combination of preprocessing methods and clustering algorithms to evaluate performance metrics such as Silhouette Score, Calinski-Harabasz Index, and Davies-Bouldin Score.

## Google Colab Notebook

Access the notebook here: [Clustering Analysis](https://colab.research.google.com/drive/1pOA0m78MPqw2TUoZZARylkrTkIE8cyS_?usp=sharing)

## Features

- **Preprocessing Methods**:
  - Standard Scaling
  - Min-Max Scaling
  - Principal Component Analysis (PCA)
  - Combined Scaling + PCA
- **Clustering Algorithms**:
  - KMeans
  - Hierarchical Clustering
  - MeanShift
- **Performance Metrics**:
  - Silhouette Score
  - Calinski-Harabasz Index
  - Davies-Bouldin Score

## Input

The dataset used is the **Wine Quality Dataset** from the UCI Machine Learning Repository. It contains physicochemical properties (numerical variables) and wine quality scores.

- Dataset URL: [Wine Quality Dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/winequality-red.csv)
- Sample data:
  ```csv
  fixed acidity;volatile acidity;citric acid;residual sugar;chlorides;free sulfur dioxide;total sulfur dioxide;density;pH;sulphates;alcohol;quality
  7.4;0.7;0;1.9;0.076;11;34;0.9978;3.51;0.56;9.4;5
  7.8;0.88;0;2.6;0.098;25;67;0.9968;3.2;0.68;9.8;5
  7.8;0.76;0.04;2.3;0.092;15;54;0.997;3.26;0.65;9.8;5
  ```

## Output

The project outputs include:

1. **Performance Metrics**:
   - Silhouette Score
   - Calinski-Harabasz Index
   - Davies-Bouldin Score
2. **Visualizations**:
   - Cluster performance metrics comparison using bar plots.
   - Silhouette scores by cluster and configuration.

## Example Usage

### Sample Code for Clustering

```python
silhouette, calinski, davies = run_clustering(data, num_clusters=3, algorithm='kmeans', preprocess='scale')
print(f"Silhouette: {silhouette}, Calinski-Harabasz: {calinski}, Davies-Bouldin: {davies}")
```

### Example Results

| Algorithm  | Preprocessing | Clusters | Silhouette | Calinski-Harabasz | Davies-Bouldin |
|------------|---------------|----------|------------|--------------------|----------------|
| KMeans     | Scale         | 3        | 0.56       | 1425.87           | 0.56           |
| Hierarchical | PCA         | 4        | 0.48       | 1123.34           | 0.68           |
| MeanShift  | None          | N/A      | N/A        | N/A               | N/A            |

### Visualization Example

#### Silhouette Scores by Cluster and Configuration
![Silhouette Scores](example_silhouette_plot.png)

## Installation

1. Install required libraries:
   ```bash
   pip install -U scikit-learn pycaret matplotlib seaborn pandas numpy
   ```
2. Open the Colab link and run the notebook.

## How to Use

1. Load the dataset from the provided URL or upload your own `.csv` file.
2. Choose clustering algorithms, number of clusters, and preprocessing methods.
3. Run the notebook to compute clustering metrics and visualize results.

## Contribution

Feel free to contribute by:
- Adding more clustering techniques.
- Improving visualization.
- Enhancing the documentation.

