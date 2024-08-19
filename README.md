# K-Means Clustering Visualization

This repository contains a Python script for implementing and visualizing the K-Means clustering algorithm. The script demonstrates how to cluster data into groups and visualize the resulting clusters and centroids in a 2D feature space.

## Table of Contents

1. [Overview](#overview)
2. [Requirements](#requirements)
3. [Installation](#installation)
4. [Usage](#usage)
5. [How It Works](#how-it-works)
6. [Examples](#examples)
7. [Results](#results)
8. [Troubleshooting](#troubleshooting)
9. [FAQs](#faqs)
10. [License](#license)

## Overview

The project implements the K-Means clustering algorithm on synthetic 2D data and visualizes the clustering results. The script creates clusters, determines the centroids, and displays the decision boundaries that separate different clusters.

## Requirements

To run the code, you'll need the following Python libraries:

- `numpy`
- `matplotlib`
- `scikit-learn`

You can install these libraries using pip:

```bash
pip install numpy matplotlib scikit-learn
```

## Installation

1. **Clone the Repository**:

    ```bash
    git clone https://github.com/yourusername/kmeans-visualization.git
    ```

2. **Navigate to the Project Directory**:

    ```bash
    cd kmeans-visualization
    ```

3. **Install Required Libraries**:

    ```bash
    pip install numpy matplotlib scikit-learn
    ```

## Usage

1. **Run the Python Script**:

    Execute the script to perform K-Means clustering and visualize the results:

    ```bash
    python kmeans_visualization.py
    ```

2. **View the Output**:

    The script will display a plot showing:
    - The clustered data points.
    - The centroids of the clusters.
    - The decision boundaries between clusters.

## How It Works

### Data Generation

- **Synthetic Data**: The script generates synthetic 2D data with four distinct clusters using `make_blobs` from `scikit-learn`.

### Model Creation

- **K-Means Clustering**:
  - A K-Means model is instantiated with the desired number of clusters.
  - The model is trained on the synthetic data to identify clusters and compute centroids.

### Visualization

- **Scatter Plot**:
  - Data points are plotted in 2D space with colors representing different clusters.
  - Cluster centroids are marked with red 'X' symbols.

- **Cluster Boundaries**:
  - Decision boundaries are visualized using a contour plot that shows how the space is divided among the clusters.

### Plotting the Boundaries

- **Grid Creation**:
  - A grid of points is created covering the feature space to visualize cluster boundaries.
  
- **Prediction**:
  - The K-Means model predicts cluster labels for each point in the grid.

- **Contour Plot**:
  - The contour plot visualizes the regions assigned to each cluster.

## Examples

### Basic Execution

To execute the script and view the clustering results:

```bash
python kmeans_visualization.py
```

### Customization

You can modify the following parameters in the script:
- **Number of Clusters**: Change the `num_clusters` variable to adjust the number of clusters.
- **Data Generation**: Modify `make_blobs` parameters to generate different datasets.

## Results

The script generates a visual representation of K-Means clustering, including:
- **Clustered Data Points**: Colored according to their assigned cluster.
- **Centroids**: Red 'X' markers indicating the center of each cluster.
- **Cluster Boundaries**: Shaded areas representing the decision boundaries between clusters.

The visualization helps understand how K-Means partitions data into clusters and how the centroids are positioned relative to the data points.

**Output Plot:**
![K Means Clustering Visualizations](https://github.com/AartiDashore/KMeansClusteringVisualization/blob/main/Output1.png)

## Troubleshooting

### Common Issues

1. **Module Not Found Error**:
    - Ensure all required libraries are installed.
    - Verify your Python environment.

2. **Plot Not Displaying**:
    - Ensure that `matplotlib` is properly installed and configured.
    - Run the script in an environment that supports plotting, such as Jupyter Notebook or a local IDE.

## FAQs

### What is K-Means Clustering?

K-Means is a clustering algorithm that partitions data into `k` distinct clusters based on feature similarity. It iteratively refines cluster centroids to minimize within-cluster variance.

### How are Centroids Determined?

Centroids are computed as the mean of the data points in each cluster. The algorithm updates the centroids during training to improve clustering.

### What are Decision Boundaries?

Decision boundaries are the regions separating different clusters. They are visualized as contours in the feature space, showing how the model assigns data points to different clusters.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
