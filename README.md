     1. Introduction

To understand how breast cancer progresses and how it responds to therapeutic treatments, we studied gene expression dynamics using a well-established mouse model (PYMT breast cancer model).


In biological systems, cancer development is driven by massive disruptions inside the cells, where certain genes become abnormally overactive while others are switched off or suppressed. To track these changes over time, our study focuses on two main aspects:


Disease Progression: Observing how gene expression shifts naturally between the early stage (Day 0) and a more advanced stage (Day 7) without treatment.


Drug Response: Evaluating how the introduction of a specific targeted treatment (10mMpp and higher concentrations) alters these gene patterns, aiming to see whether the drug can successfully reverse or stop the cancerous changes.


The raw data used for this entire analysis was obtained from high-throughput RNA-Seq count datasets (specifically sourced from the GSE344396 study).

     2. Methodology

To process thousands of genes and extract meaningful biological insights without getting overwhelmed by raw numbers, we built an automated data-analysis pipeline using Python and the Pandas library. The workflow was structured as follows:


Data Loading and Cleaning: We loaded the compressed RNA-Seq count datasets (.csv.gz) using Pandas to efficiently manage large expression matrices.


Comparative Calculation (Difference): For each experimental condition and time point, we calculated the exact expression change by subtracting baseline values from later stages (e.g., $\text{Difference} = \text{Day 7} - \text{Day 0}$). Across multiple replicates, we computed an Average Difference to ensure statistical reliability and accuracy. 


Sorting and Filtering: Using Pandas sorting functions (sort_values), we isolated the most critical genes—specifically identifying the ones that increased the most (top_up) and the ones that decreased the most (top_down).


Visualization: Finally, we integrated Matplotlib to plot clean, color-coded bar charts (green for upregulated/increased genes, red for downregulated/decreased genes) to clearly visualize the cellular response to the disease and the treatment.

        4. Discussion and Biological Interpretation

The results extracted from our Pandas data pipeline and visualized through our bar plots reveal a clear picture of how breast cancer cells behave over time and how they respond to treatment:



