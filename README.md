# Information Retrieval Benchmark

## Project Overview

This project benchmarks three different Information Retrieval (IR) systems:

* **BM25 (Sparse Retrieval)**
* **Dense Vector Search (Sentence Transformers + FAISS)**
* **Hybrid Retrieval (Reciprocal Rank Fusion - RRF)**

The objective is to compare traditional keyword-based retrieval with modern semantic retrieval techniques and evaluate their performance using standard Information Retrieval metrics.

---

# Technologies Used

* Python
* NumPy
* NLTK
* Hugging Face Datasets
* rank_bm25
* Sentence Transformers
* FAISS
* pytrec_eval
* tqdm

---

# Project Structure

```
Information_Retrieval_Benchmark/

│
├── retrieval_benchmark.ipynb
├── requirements.txt
├── README.md
│
├── output/
│      ├── bm25_index.pkl
│      ├── dense.index
│      └── corpus_embeddings.npy
│
└── results/
       ├── benchmark_metrics.json
       └── failure_analysis.json
```

---

# Retrieval Systems Implemented

## 1. BM25 Retrieval

* Tokenizes the corpus
* Builds a BM25 index
* Retrieves documents using keyword matching

---

## 2. Dense Vector Search

* Uses the Sentence Transformer model:

  * `all-MiniLM-L6-v2`
* Generates embeddings for the corpus
* Stores embeddings using FAISS
* Retrieves documents using semantic similarity

---

## 3. Hybrid Retrieval

* Combines BM25 and Dense Retrieval
* Uses Reciprocal Rank Fusion (RRF)
* Produces the final ranked results

---

# Evaluation Metrics

The retrieval systems are evaluated using:

* **NDCG@10**
* **Mean Reciprocal Rank (MRR)**
* **Recall@100**

Performance benchmarking also includes:

* Index Build Time
* Embedding Time
* Index Size
* Query Latency (P50)
* Query Latency (P99)

---

# Generated Files

## output/

* `bm25_index.pkl`
* `dense.index`
* `corpus_embeddings.npy`

## results/

* `benchmark_metrics.json`
* `failure_analysis.json`

---

# How to Execute the Project

## Step 1: Clone the Repository

```bash
git clone <repository_url>
cd <repository_folder>
```

---

## Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Step 3: Launch Jupyter Notebook

```bash
jupyter notebook
```

or

```bash
jupyter lab
```

---

## Step 4: Open the Notebook

Open:

```
retrieval_benchmark.ipynb
```

---

## Step 5: Run the Notebook

Execute all cells from top to bottom using:

```
Run → Run All Cells
```

or

```
Kernel → Restart & Run All
```

---

## Step 6: Generated Outputs

After successful execution, the following files will be automatically generated:

### output/

```
bm25_index.pkl

dense.index

corpus_embeddings.npy
```

### results/

```
benchmark_metrics.json

failure_analysis.json
```

---

# Expected Folder Structure After Execution

```
Information_Retrieval_Benchmark/

│
├── retrieval_benchmark.ipynb
├── requirements.txt
├── README.md
│
├── output/
│      ├── bm25_index.pkl
│      ├── dense.index
│      └── corpus_embeddings.npy
│
└── results/
       ├── benchmark_metrics.json
       └── failure_analysis.json
```

---

# Conclusion

This project successfully implements and benchmarks:

* BM25 Retrieval
* Dense Vector Search using Sentence Transformers and FAISS
* Hybrid Retrieval using Reciprocal Rank Fusion (RRF)

It evaluates these systems using standard Information Retrieval metrics and generates quantitative benchmark results along with qualitative failure analysis.
