# Graph Clustering & Data Mining Analysis   

## Abstract 📄  

This project explores **graph clustering and data mining** techniques with practical demonstrations. It combines a **presentation on graph clustering methods** with a **Jupyter Notebook** that implements and evaluates related approaches. Our primary focus is on community detection in networks and algorithmic comparisons for clustering.  

**Keywords**: Graph Clustering, Girvan-Newman, Louvain Algorithm, Community Detection, Data Mining  

---

## Table of Contents 📋  

* [Introduction](#introduction-💡)  
* [Graph Clustering & Community Detection](#graph-clustering--community-detection-🕸️)  
* [Girvan-Newman Algorithm](#girvan-newman-algorithm-🔍)  
* [Louvain Algorithm](#louvain-algorithm-⚡)  
* [Comparison & Applications](#comparison--applications-📊)  
* [Advantages & Disadvantages](#advantages--disadvantages-⚖️)  
* [Notebook Implementation](#notebook-implementation-💻)  
* [Conclusion & Future Work](#conclusion--future-work-🏁)  
* [References](#references-📚)  

---

## Introduction 💡  

Graph clustering, also known as **community detection**, is the process of identifying tightly connected groups of nodes within a graph. This process improves visualization and understanding of complex networks.  

### Applications  
- **Social Networks**: Detecting user communities  
- **Biological Networks**: Identifying functional gene/protein modules  
- **Marketing**: Segmenting customer groups  

---

## Graph Clustering & Community Detection 🕸️  

In networks, communities are subgroups with dense internal links and sparse external connections. Community detection is crucial for understanding hidden structures.  

---

## Girvan-Newman Algorithm 🔍  

### Working Principle  
* Remove edges with the highest **betweenness centrality**.  
* Recompute betweenness after each removal.  
* Repeat until the graph splits into communities.  

### Steps  
1. Calculate betweenness centrality of all edges.  
2. Remove edge with highest betweenness.  
3. Recalculate and repeat.  

### Example  
Applied on a sample network with nodes **A–F**, resulting in multiple community splits.  

### Advantages  
- Suitable for **small/medium graphs**  
- Detects **hierarchical structures**  

### Disadvantages  
- **High computational complexity**  
- Sensitive to **noise**  
- Not scalable for **large graphs**  

---

## Louvain Algorithm ⚡  

### Overview  
The Louvain method optimizes **modularity** to find communities efficiently, especially in large networks.  

### Steps  
1. **Local Modularity Optimization** – move nodes between communities for max modularity.  
2. **Community Aggregation** – merge nodes into super-nodes, repeat process hierarchically.  

### Formula for Modularity  
\[
Q = \frac{1}{2m} \sum_{ij} \Big[ A_{ij} - \frac{k_i k_j}{2m} \Big] \delta(c_i, c_j)
\]  

---

## Comparison & Applications 📊  

| Feature                  | Girvan-Newman                 | Louvain                     |  
|--------------------------|-------------------------------|-----------------------------|  
| **Scalability**          | Poor (small graphs only)      | Excellent (large graphs)    |  
| **Accuracy**             | Medium                        | High                        |  
| **Complexity**           | High                          | Low                         |  
| **Use Case**             | Teaching, small networks      | Real-world large networks   |  

---

## Advantages & Disadvantages ⚖️  

**Girvan-Newman**:  
- ✅ Good for small, structured graphs  
- ❌ Computationally expensive, loses important edges  

**Louvain**:  
- ✅ Scalable, modularity-based, efficient  
- ❌ May produce different results depending on initialization  

---

## Notebook Implementation 💻  

Explore implementation in the provided **Jupyter Notebook**:  

* [Girvan-Newman-and-Louvain-algorithms.ipynb](https://github.com/elahehmood/Graph-Clustering-and-Data-Mining-Analysis-/blob/main/Girvan-Newman-and-Louvain-algorithms.ipynb)  

### Run Online 🚀  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elahehmood/Graph-Clustering-and-Data-Mining-Analysis-/blob/main/Girvan-Newman-and-Louvain-algorithms.ipynb)  

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/elahehmood/Graph-Clustering-and-Data-Mining-Analysis-/HEAD?labpath=Girvan-Newman-and-Louvain-algorithms.ipynb)  

---

## Conclusion & Future Work 🏁  

### Conclusion  
Both Girvan-Newman and Louvain algorithms are effective, but Louvain is preferred for large-scale, real-world networks due to its efficiency.  

### Future Work  
- Extend analysis to **dynamic networks**  
- Apply **hybrid algorithms**  
- Test on **real-world datasets** (social media, biological networks)  

---

## References 📚  

* Girvan, M., & Newman, M. E. J. (2002). *Community structure in social and biological networks.* PNAS.  
* Blondel, V. D., Guillaume, J. L., Lambiotte, R., & Lefebvre, E. (2008). *Fast unfolding of communities in large networks.* J. of Statistical Mechanics.  
* Fortunato, S. (2010). *Community detection in graphs.* Physics Reports.  
