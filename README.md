# Community Detection in Collaboration Networks using Normalized Spectral Clustering  

This project applies **Normalized Spectral Clustering** to detect communities in **collaboration networks**. It evaluates the effectiveness of clustering methods in identifying meaningful research communities within large datasets.

## Overview  

**Normalized Spectral Clustering** is a graph-based clustering technique that uses the **Laplacian matrix of a graph** to partition nodes into well-defined communities. This method is particularly useful for **network-based data**, such as collaboration networks, where relationships between entities play a crucial role in forming groups.

The study applies **normalized spectral clustering with k-means** to various collaboration networks, including:  
- **ca-AstroPh** (Astrophysics collaborations)  
- **ca-CondMat** (Condensed Matter collaborations)  
- **ca-GrQc** (General Relativity collaborations)  
- **ca-HepPh** (High Energy Physics - Phenomenology)  
- **ca-HepTh** (High Energy Physics - Theory)  

## 📊 Results Summary  

The effectiveness of **Normalized Spectral Clustering** is evaluated based on competition values for different cluster sizes (`k` values).

| **Network**   | **k (Clusters)** | **Evaluation Score** |
|--------------|---------------|------------------|
| **ca-AstroPh** | 50  | 15962 |
| **ca-CondMat** | 100 | 12091 |
| **ca-GrQc**    | 2   | 5.26  |
| **ca-HepPh**   | 25  | 7791  |
| **ca-HepTh**   | 20  | 934   |

## 🛠 Installation & Dependencies  

Ensure you have **Python 3.7+** and install the required dependencies:

```bash
pip install numpy pandas networkx matplotlib scikit-learn
```

Run the training and evaluation scripts in `community_detection.ipynb`


### Evaluation

The script `evaluate.py` accepts two arguments:

1. the path of the graph file
2. the path of the clustering file

and prints the objective value (normalized min-cut) achieved by the clustering.

### How to use?

To use it, run the following in command line:

`python evaluate.py {graph_path} {clustering_path}`

If everything (format, etc) is correct, the objective value will be printed. 