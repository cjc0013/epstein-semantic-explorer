# epstein-semantic-explorer
Semantic clusters, entity extraction, and BM25 search across recently released Congressional Epstein documents.

The full semantic dataset is hosted on Kaggle:

👉 https://www.kaggle.com/datasets/cjc0013/epstein-bge-large-hdbscan-bm25/data

# **Epstein Semantic Explorer v5 — README**

A lightweight, semantic investigation toolkit for exploring the House Oversight Epstein text dump.

This notebook **does not add any new allegations**.
It simply **organizes**, **clusters**, and **indexes** what is already public — thousands of text fragments released by Congress.

All analysis is done **locally inside Colab**, and no external services, models, or APIs are required.

---

# **📦 What This Notebook Does**

The Epstein Semantic Explorer v5 takes a messy pile of thousands of text documents and gives you:

### **1. Cluster Browser**

Explore themed groups of documents — legal strategy, PR coordination, iMessage logs, internal disputes, etc.

```
view_cluster(96)
```

---

### **2. Keyword Search (BM25-lite)**

Instantly find related documents by keyword or phrase.

```
search("Prince Andrew")
search("Ghislaine")
search("Clinton")
```

---

### **3. Cluster Summaries**

Get a quick human-readable overview of what a cluster likely contains.

```
summarize_cluster(96)
```

---

### **4. Topic Modeling**

Shows “top terms” for each cluster — a lightweight, dependency-free way to understand cluster themes.

```
show_topics()
```

---

### **5. Entity Extraction**

Find the most frequently mentioned **people**, **places**, and **organizations** inside a cluster.

```
cluster_entities(12)
```

---

### **6. Timeline Extraction**

Automatically extract dates and sort them chronologically.

```
show_timeline()
```

---

### **7. Cluster Similarity Matrix**

Shows how thematically related different clusters are.

```
cluster_similarity()
```

---

### **8. Cross-cluster Entity Search**

Instantly see which clusters mention a specific name the most.

```
entity_to_clusters("Epstein")
entity_to_clusters("Maxwell")
entity_to_clusters("Barak")
```

---

# **📁 What You Need**

Only one file:

```
epstein_semantic.jsonl
```

Your dataset should be structured like:

```jsonl
{"id": "HOUSE_OVERSIGHT_023051", "cluster": 96, "text": "…document text…"}
{"id": "HOUSE_OVERSIGHT_028614", "cluster": 122, "text": "…document text…"}
```

That’s it. No images, no PDFs needed.

---

# **🚀 How to Use the Notebook**

### **Step 1 — Upload the Notebook**

Open Google Colab → upload:

```
epstein_explorer_v5.ipynb
```

### **Step 2 — Run All Cells**

Runtime → Run all

### **Step 3 — Upload Your Data**

When prompted:

```
Upload epstein_semantic.jsonl
```

### **Step 4 — Start Exploring**

Use the tools:

```
view_cluster(96)
search("Prince Andrew")
show_topics()
cluster_entities(96)
```

Everything runs instantly on CPU; no GPU required.

---

# **🧩 FAQ**

### **Q: Does this notebook create new allegations?**

**No.**
It only organizes *existing public documents* released by the House Oversight Committee.

### **Q: Does this send data to external servers?**

**No.**
Everything runs inside your Colab session.

### **Q: Can reporters use this without technical experience?**

Yes — the notebook is designed to be **point-and-click simple**.
You can search, browse clusters, and explore without writing code.

### **Q: Is this safe for publication?**

Yes — as long as you make clear that:

* all data is public
* no new claims were added
* this is a semantic reorganization of public records

---

# **📝 Summary**

This notebook:

* converts the chaotic House Oversight Epstein text archive
  into a structured, searchable dataset
* enables investigators to quickly identify themes, contradictions, legal strategies, and PR coordination patterns
* gives reporters the ability to explore thousands of documents in minutes

This tool **makes the archive usable**, but does not alter or create any content.





