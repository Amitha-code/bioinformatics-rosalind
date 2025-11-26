This project performs a Differential Gene Expression (DGE) analysis to identify genes that are significantly up-regulated or down-regulated in patients with Type 2 Diabetes Mellitus (T2DM) compared to healthy controls.
Understanding the transcriptional changes in immune cells (PBMCs) is crucial for identifying potential biomarkers and therapeutic targets for metabolic diseases.
Key Objectives:
 * Simulate realistic RNA-Seq count data for T2DM and Control groups.
 * Perform statistical modeling using the PyDESeq2 library (Python implementation of DESeq2).
 * Identify significantly differentially expressed genes (DEGs) based on Fold Change and FDR.
 * Visualize results using a Volcano Plot.
📂 Repository Structure
├── data/                   # Input data files (or simulation scripts)
├── figures/                # Generated visualizations
│   └── volcano_plot.png    # Final Volcano Plot image
├── results/                # Analysis outputs
│   └── final_deseq2_results.csv # Table of differential expression results
├── scripts/                # Source code
│   └── dge_analysis.py     # Main Python script for simulation and analysis
├── ai_usage.md             # Documentation of AI tools used
└── README.md               # Project documentation (this file)

🛠️ Methods & Workflow
1. Data Simulation
Due to the constraints of sharing large sensitive medical data, this project uses simulated data that mimics the structure of real RNA-Seq experiments:
 * Samples: 10 Total (5 Control, 5 T2DM).
 * Genes: 20,000 synthetic genes.
 * Signal: A specific subset of genes (n=50) was artificially up-regulated in the T2DM group to validate the detection pipeline.
2. Analysis Pipeline (pydeseq2)
The analysis was performed in a Python environment (Google Colab) using the following steps:
 * Normalization & Modeling: Using DeseqDataSet to model counts with a negative binomial distribution.
 * Statistical Testing: Using DeseqStats (Wald Test) to calculate p-values and Log2 Fold Changes.
 * Filtering:
   * FDR (False Discovery Rate) Threshold: < 0.05
   * Log2 Fold Change Threshold: > 1.0 or < -1.0
3. Visualization
 * Volcano Plot: Generated using matplotlib and seaborn to visualize the relationship between biological significance (Fold Change) and statistical significance (FDR).
🚀 How to Run
Prerequisites
You need Python installed along with the following libraries:
pip install pydeseq2 pandas numpy matplotlib seaborn

Execution
 * Clone this repository.
 * Open the script in Jupyter Notebook or Google Colab.
 * Run the analysis code.
 * Output files will be generated in the local directory.
📊 Results
The pipeline successfully identified the simulated bio-markers.
 * Output Table: results/final_deseq2_results.csv contains the full statistical results for all 20,000 genes.
 * Visual Output: The Volcano Plot below highlights the up-regulated genes (in Red) distinguishing the T2DM group from the Control group.
🤖 AI Use & Reproducibility
This project utilized Google Gemini for:
 * Refining the project proposal and timeline.
 * Debugging Python errors related to pydeseq2 API changes.
 * Drafting documentation structures.
👥 Team
 * Amitha Nagabelli
 * sravan kumar goud Earukala
 * Sri Navya Deepthi Challagundla
 * Venkata Nagasai Sreeram Avasarala 
