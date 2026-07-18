# Graph Classification on MUTAG

A comparative study of graph classification techniques on the MUTAG dataset using traditional graph representations and Graph Neural Networks (GNNs). This project evaluates multiple approaches for predicting molecular mutagenicity and analyzes their performance on a benchmark graph dataset.

---

## Workflow

![Workflow](images/workflow.png)

---

## Overview

Graph classification is a fundamental task in graph machine learning, where an entire graph is assigned a class label. The MUTAG dataset consists of chemical compounds represented as graphs, with the objective of classifying each compound as mutagenic or non-mutagenic.

This project presents a comparative analysis of multiple graph classification methods, ranging from traditional techniques to deep learning-based Graph Neural Networks.

---

## Dataset

**Dataset:** MUTAG

**Description:** A benchmark graph dataset containing chemical compounds represented as graphs.

- **Number of Graphs:** 188
- **Classification Task:** Binary Classification
- **Classes:** Mutagenic / Non-Mutagenic
- **Node Labels:** Atom Types
- **Edge Labels:** Bond Types

---

## Methods Evaluated

The project compares different graph classification approaches, including:

- Graph Kernels
- Graph Embeddings
- Graph Convolutional Networks (GCN)
- GraphSAGE
- Other graph learning techniques implemented in the notebook

---

## Tech Stack

- Python
- Jupyter Notebook
- PyTorch
- PyTorch Geometric
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## Repository Structure

```
Graph-Classification-on-MUTAG/
│
├──MUTAG-GraphClassification.ipynb
├──images/
│   ├── workflow.png
│   ├──mutag_graph.png
│   ├──accuracy_f1_comp.png
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
└──results/
    └── model_comparison.csv
```

---

## How to Run

1. Clone the repository.
2. Install the required packages:

```bash
pip install -r requirements.txt
```

3. Open `MUTAG-GraphClassification.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the notebook sequentially.

---

## Sample Graph

![MUTAG](images/mutag_graph.png)

---

## Results

The models were evaluated using Accuracy, Precision, Recall, and F1-Score on the MUTAG dataset.

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|---------:|----------:|-------:|---------:|
| Weisfeiler-Lehman Kernel | 0.763 | 0.833 | 0.800 | 0.816 |
| Shortest Path Kernel | **0.833** | **0.909** | 0.833 | 0.870 |
| Node2Vec | 0.763 | 0.767 | 0.920 | 0.836 |
| Edge2Vec | **0.842** | 0.880 | 0.880 | **0.880** |
| DeepWalk | 0.763 | 0.750 | **0.960** | 0.842 |
| GCN | 0.778 | 0.833 | 0.833 | 0.833 |
| GraphSAGE | 0.771 | 0.793 | 0.888 | 0.838 |

### Performance Comparison

![Performance Comparison](images/accuracy_f1_comp.png)

The comparative analysis demonstrates the strengths and trade-offs of graph kernels, graph embedding methods, and Graph Neural Networks for molecular graph classification. While **Edge2Vec** achieved the highest overall Accuracy and F1-Score in this implementation, each method exhibited different strengths across the evaluation metrics.


---

## Publication

This work contributed to the book chapter **"Graph-Based Classification Methods for Detecting Mutagenicity"**, published in **_Emerging Dimensions in Biotechnology: Research, Innovation and Application (Volume 1)_** by AGROBIOS (India), 2026.

---

## Future Work

- Evaluate additional Graph Neural Network architectures
- Perform hyperparameter optimization
- Extend the study to larger benchmark graph datasets
- Investigate graph transformers for graph classification

---

## Acknowledgements

- MUTAG Benchmark Dataset
- PyTorch Geometric
- PyTorch

---

## License

This project is licensed under the MIT License.
