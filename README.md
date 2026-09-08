# PYMT Breast Cancer RNA-Seq Analysis 🧬🔬

## 📌 Project Overview
This project analyzes RNA-Seq data from a mouse breast cancer model (PYMT). The goal is to evaluate the genetic changes (transcriptomic response) after a 7-day treatment with a 50mMpp drug dose. 

## 🛠️ Tools & Methodology
* **Tech Stack:** Python, Pandas, Google Colab.
* **Process:** 
  1. Extracted and cleaned raw count RNA-Seq data from a compressed dataset.
  2. Isolated biological replicates for the 50mMpp treatment group (Day 0 vs. Day 7).
  3. Calculated the expression differences to identify the most upregulated and downregulated genes.

## 📊 Key Biological Findings
The comparison between Day 0 (pre-treatment) and Day 7 (post-treatment) revealed two major genetic shifts:

* **Downregulation (Gene ENSMUSG00000064341):** This gene showed a massive decrease in activity (-81,559 counts). Biologically, this suggests it acts as an oncogene (cancer-driving gene) that the 50mMpp treatment successfully suppressed.
* **Upregulation (Gene ENSMUSG00000045545):** This gene showed a significant spike in expression (+44,510 counts). This indicates the activation of a tumor suppressor gene or a cellular defense mechanism (like apoptosis) triggered by the drug.

## 💡 Conclusion
The data clearly demonstrates that the 50mMpp treatment effective
