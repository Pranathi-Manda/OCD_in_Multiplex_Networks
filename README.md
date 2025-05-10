#  Overlapping Community Detection in Multiplex Networks using VGAE + CPM

This repository contains a project that detects **overlapping communities** in real-world **multiplex networks** using a hybrid framework that combines **Variational Graph Autoencoders (VGAE)** and the **Clique Percolation Method (CPM)**. The primary use case explored is an **air transportation network**, where each node (airport) can belong to multiple overlapping communities (e.g., domestic and international hubs).

---

## 📁 Repository Contents

| File/Folder | Description |
|-------------|-------------|
| `air_transport_mutiplex_dataset.ipynb` | Main notebook for data preparation and community detection using VGAE + CPM |
| `air_transport_mutiplex_dataset2.ipynb` | Auxiliary or experimental notebook for variation/analysis |
| `OCD_in_multiplex_networks.pptx` | Presentation slides summarizing the project, methodology, and results |
| `OCD_Overlapping_Communities_Report.docx` | Full report documenting background, implementation, results, and evaluation |

---

## 📊 Dataset

The project uses a **real-world multiplex airport network dataset** provided by:

> **Alessio Cardillo et al. (2013)**  
> *"Emergence of network features from multiplexity."*  
> Scientific Reports, 3:1344.  
> [DOI: 10.1038/srep01344](https://doi.org/10.1038/srep01344)

- **Nodes**: 438 airports  
- **Edges**: 26,993 flight routes  
- **Layers**: 37 (18 major airlines, 10 low-cost, and 9 regional/cargo)  
- **Node features**: IATA code, latitude, longitude  

---

## 🧠 Methodology

### 🔷 VGAE (Variational Graph Autoencoder)
- Learns a low-dimensional latent representation for each node.
- Captures both intra-layer and inter-layer structural patterns.
- Implemented using **PyTorch Geometric**.

### 🔷 CPM (Clique Percolation Method)
- Applied to the VGAE-generated embedding graph.
- Detects **overlapping communities** based on shared k-cliques.

---

## ⚙️ Technologies

- Python 3.x
- Jupyter Notebook
- PyTorch Geometric
- NetworkX
- Scikit-learn
- Cartopy (for geographic visualizations)

---

## 🧪 Results

- **Best clique size (k)**: 5
- **Evaluation Metrics**:
  - **Modularity**: 0.3821
  - **Normalized Mutual Information (NMI)**: 0.8504
  - **Average Precision**: 0.4510

These indicate strong detection of meaningful overlapping communities and predictive accuracy.

---

## 🚀 Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/OCD-Multiplex-Networks.git
   cd OCD-Multiplex-Networks
