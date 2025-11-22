# Network Science – Project

The project is divided in two parts, the Empirical analysis of the dataset and the poster presentation.

--- 

## Project Structure

```
├── data/                 # Dataset files  
├── src/  
│   ├── preprocessing.py  # Data loading & preprocessing  
│   ├── stats.py          # Descriptive statistics  
│   ├── metrics.py        # Network metrics  
│   ├── plots.py          # Figures, scatter plots, distributions  
│   └── communities.py    # Community detection & modularity analysis  
├── results/              # Tables, plots, exported metrics  
├── slides/               # Presentation slides  
├── requirements.txt  
└── README.md
```
---

## Part 1: Empirical Dataset Analysis

This repository contains the implementation of an empirical network analysis assignment for the Network Science course.  
It includes dataset exploration, descriptive statistics, network metrics, visualizations, and community-structure detection.

### Assignment Overview

The analysis follows five main components:

#### 1. Dataset Description
- Type of network  
- Number of nodes and edges  
- Source and properties  

#### 2. Descriptive Statistics (example)
    import networkx as nx
    G = nx.read_edgelist("data/network.edgelist")
    print(G.number_of_nodes(), G.number_of_edges())

#### 3. Network Metrics (example)
    betweenness = nx.betweenness_centrality(G)
    clustering = nx.clustering(G)

#### 4. Distributions & Scatter Plots (example)
    import matplotlib.pyplot as plt
    degrees = [d for _, d in G.degree()]
    plt.hist(degrees, bins=25)
    plt.savefig("results/plots/degree_distribution.png")

#### 5. Community Structure (example)
    import community
    partition = community.best_partition(G)

---

## How to Run

### 1. Clone the repository
    git clone git@github.com:rengav13/tu-graz-network-science.git
    cd tu-graz-network-science

### 2. Install dependencies
    pip install -r requirements.txt

### 3. Explore the analysis in Jupiter
    empirical-analysis.ipynb

---

## Data set

[Youtube social network and ground-truth communities](https://snap.stanford.edu/data/com-Youtube.html)

---

## Results & Slides
- Results are stored in: results/  
- Slides are located in: slides/  

---

## License
Educational use only. Reuse allowed with attribution.
