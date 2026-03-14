# Hilabs
Clinical-Data-Harmonizer: An AI-powered engine using SapBERT and Fuzzy Logic to map unstructured clinical strings to standardized medical codes (RxNorm, SNOMED CT, LOINC).
# 🏥 Clinical Data Harmonization Engine

## 📌 Project Overview
In clinical settings, data is often recorded in unstructured, messy formats (e.g., "Hb", "T2DM", "Paracetamol 500mg"). This project provides an automated pipeline to **standardize and harmonize** these entries into official medical coding systems like **RxNorm**, **SNOMED CT**, and **LOINC**.

This solution was developed as part of the **HiLabs Workshop** to solve the challenge of Entity Resolution in healthcare data.

## 🚀 Key Features
* **Semantic Mapping:** Uses **SapBERT** (Self-alignment pre-training for Biomedical Entity Representations) to identify synonyms (e.g., mapping "Heart Attack" to "Myocardial Infarction").
* **Hybrid Matching:** Combines Deep Learning embeddings with **Fuzzy String Matching** (RapidFuzz) to handle typos and abbreviations.
* **Medical Domain Aware:** Pre-trained on PubMed and UMLS to understand complex clinical terminology.
* **Confidence Scoring:** Provides a reliability score for every match to support human-in-the-loop validation.

## 🛠️ Technical Stack
* **Language:** Python 3.x
* **Models:** `cambridgeltl/SapBERT-from-PubMedBERT-fulltext`
* **Libraries:** `sentence-transformers`, `pandas`, `rapidfuzz`, `torch`
* **Environment:** Jupyter Notebook / Anaconda

## 📂 Project Structure
```text
├── data/
│   ├── raw_data.csv          # Unstructured clinical inputs
│   └── codebooks/            # Target RxNorm/SNOMED datasets
├── src/
│   ├── harmonizer.py         # Core logic class
│   └── utils.py              # Preprocessing scripts
├── notebooks/
│   └── solution_demo.ipynb   # Step-by-step walkthrough
└── README.md
