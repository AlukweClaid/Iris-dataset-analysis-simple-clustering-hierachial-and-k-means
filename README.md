# Iris Dataset Clustering Analysis

## Project Overview

This project performs comprehensive clustering analysis on the famous Iris dataset using two popular unsupervised learning techniques: **K-Means Clustering** and **Hierarchical (Agglomerative) Clustering**. The analysis includes visualization of clusters, determination of optimal cluster numbers using the elbow method, and evaluation of clustering quality using silhouette scores.

## Dataset Description

The Iris dataset is a classic dataset in machine learning and statistics, containing measurements of iris flower characteristics:

- **Number of Samples**: 150 iris flowers
- **Number of Features**: 4 numeric features
  - Sepal length (cm)
  - Sepal width (cm)
  - Petal length (cm)
  - Petal width (cm)
- **Target Classes**: 3 iris species
  - Setosa
  - Versicolor
  - Virginica

## Project Structure

```
Iris dataset/
├── irisdataset.ipynb          # Main Jupyter notebook with analysis
├── readme.md                  # This file
└── .git/                      # Git repository
```

## Key Analysis Steps

### 1. Data Loading and Exploration
- Load the Iris dataset from scikit-learn
- Display the first few samples
- Convert numeric target labels to flower species names
- Explore dataset shape, columns, statistics, and missing values

### 2. K-Means Clustering
- Apply K-Means clustering with 3 clusters (matching the 3 iris species)
- Visualize clusters using pairplots and scatter plots
- Display cluster assignments
- Create scatter plots showing sepal length vs. sepal width with cluster colors

### 3. Optimal Cluster Determination
- Use the **Elbow Method** to find the optimal number of clusters
- Test cluster numbers from 1 to 9
- Plot Sum of Squared Errors (SSE) vs. number of clusters
- Identify the "elbow" point for optimal cluster selection

### 4. Hierarchical Clustering
- Apply Agglomerative Clustering with 3 clusters
- Use Ward linkage method (minimizes within-cluster variance)
- Visualize clusters using pairplots
- Create dendrograms showing hierarchical cluster merging

### 5. Cluster Evaluation
- Calculate Silhouette Scores for both clustering methods
- Compare cluster quality metrics
- Determine which method provides better cluster separation

## Libraries Used

- **scikit-learn**: Machine learning library (KMeans, AgglomerativeClustering, silhouette_score)
- **pandas**: Data manipulation and analysis
- **matplotlib**: Basic plotting and visualization
- **seaborn**: Statistical data visualization
- **scipy**: Scientific computing (dendrogram, linkage)
- **numpy**: Numerical computing

## Installation & Requirements

### Prerequisites
- Python 3.7 or higher
- Jupyter Notebook or VS Code with Jupyter extension

### Installation

1. Clone or download the repository:
```bash
git clone <repository-url>
cd "Iris dataset"
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install scikit-learn pandas matplotlib seaborn scipy numpy
```

## Usage

### Running the Analysis

1. Open the Jupyter notebook:
```bash
jupyter notebook irisdataset.ipynb
```

2. Run all cells or execute them sequentially to see the complete analysis

3. View the generated visualizations:
   - Pairplots showing cluster distributions
   - Scatter plots of iris measurements
   - Elbow method curve for optimal K selection
   - Dendrograms for hierarchical clustering

## Key Results

### Clustering Performance

The analysis produces:
- **Cluster assignments** for each iris sample
- **Silhouette scores** comparing clustering methods
- **Visual comparisons** of K-Means vs. Hierarchical clustering results
- **Optimal cluster count** identification using the elbow method

### Visualizations Generated

1. **Pairplots**: Show relationships between all feature pairs, colored by cluster assignment
2. **Scatter Plots**: Display 2D projections (sepal length vs. width) with cluster colors
3. **Elbow Curve**: Charts showing SSE decrease as cluster count increases
4. **Dendrograms**: Hierarchical cluster dendrograms showing merge process

## Findings & Conclusions

- The analysis successfully identifies the 3 iris species through clustering
- Both K-Means and Hierarchical clustering produce similar results
- The elbow method helps visualize the optimal number of clusters
- Silhouette scores quantify the quality of cluster separation
- Iris flower measurements show clear natural groupings corresponding to species

## Notebook Sections

1. **Importing Libraries** - Load required packages
2. **Loading the Dataset** - Import and explore Iris data
3. **Data Exploration** - Statistical summary and data quality checks
4. **K-Means Clustering** - Apply and visualize K-Means results
5. **Optimal K Selection** - Elbow method analysis
6. **Hierarchical Clustering** - Apply and visualize Agglomerative Clustering
7. **Dendrogram Analysis** - Visualize clustering hierarchy
8. **Cluster Evaluation** - Compare methods using silhouette scores

## Notes

- The analysis uses random_state=42 for reproducibility
- K-Means is initialized with 3 clusters matching known iris species
- Hierarchical clustering uses Ward linkage (minimizes within-cluster variance)
- All numeric features are used for clustering (no feature scaling in basic analysis)

## Author Notes

This project demonstrates practical application of unsupervised learning techniques on real-world data. The Iris dataset serves as an excellent teaching tool for understanding clustering algorithms and their evaluation metrics.

## References

- [Iris Dataset - UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/iris)
- [scikit-learn Documentation](https://scikit-learn.org/)
- [K-Means Clustering](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)
- [Hierarchical Clustering](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html)

---

**Last Updated**: March 5, 2026
