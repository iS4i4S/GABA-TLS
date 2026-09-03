# GABA promotes resistance to immunotherapy of patients with TLS-positive tumors
Code for reproducing analysis on the paper "GABA promotes resistance to immunotherapy of patients with TLS-positive tumors".
![alt text](https://github.com/iS4i4S/GABA-TLS/blob/main/Data/Graphical_abstract.jpg "Graphical Abstract")

## Abstract

​​Tertiary lymphoid structures (TLS) correlate with favorable responses to immune checkpoint inhibitors (ICI) in various cancers, yet many patients with TLS-positive tumors are resistant to treatment. Multi-omic profiling of clear cell renal cell carcinoma (ccRCC) and soft tissue sarcoma tumors (STS) revealed upregulation of signatures of the neurotransmission inhibitor gamma-aminobutyric acid (GABA) in non-responders. In ccRCC, TLS from non-responders located near GABA-producing tumor cells exhibited impaired B cell maturation, reduced IgG production, higher GABA receptor expression and tricarboxylic acid cycle activation. In vitro, GABA exposure reduced HLA-DR expression, proliferation and immunoglobulin secretion by human B cells by both receptor dependent and independent mechanisms. Pharmacological inhibition of GABA synthesis increased ICI response and immune infiltration, particularly by B cells, in a TLS-positive STS mouse model. Our findings unravel GABA as a novel immunoregulatory metabolite and provide a rationale for its therapeutic targeting to overcome ICI resistance in patients with TLS-positive tumors.

## Citation
If you use any data or code derived from this study, please cite:

- Isaias Hernández-Verdin, Anne Calvez, Cheng-Ming Sun,et al. GABA promotes resistance to immunotherapy of patients with TLS-positive tumors.  Cancer Cell (2026).
- DOI: 10.1016/j.ccell.2026.06.006


## Code to reproduce main Figures
Visualize HTML files containing the code for each main figure by clicking on the coresponding links here:

 * [Figure1. High expression of GABA signatures is associated with non-response to immunotherapies in TLS-positive ccRCC tumors](http://htmlpreview.github.io/?https://github.com/iS4i4S/GABA-TLS/blob/main/Figures/Figure1.html): To reproduce this figure you need to download the raw counts data (raw_counts_kallisto.tab) from the GSE273829 (see Data avaliability below), Supplementary Table S16 from the article, and the rds file [Databases_signatures](https://github.com/iS4i4S/GABA-TLS/blob/main/Data/Databases_signatures). Clinical data is needed to reproduce this Figure but is only available from the corresponding author upon reasonable request. 

 * [Figure2. High expression of GABA ccRCC signature is associated with decreased immune activation in TLS-positive ccRCC tumors from ICI-treated patients](http://htmlpreview.github.io/?https://github.com/iS4i4S/GABA-TLS/blob/main/Figures/Figure2.html): To reproduce this figure you need to download the raw counts data (raw_counts_kallisto.tab) and preprocess it according to [Figure1](http://htmlpreview.github.io/?https://github.com/iS4i4S/GABA-TLS/blob/main/Figures/Figure1.html). You also need the "GABA high" & "GABA low" labels for each patient available in [GABA labels](https://github.com/iS4i4S/GABA-TLS/blob/main/Data/GABA_labels.tab), the Supplementary Table S16 from the article, along with the rds file [Databases_signatures](https://github.com/iS4i4S/GABA-TLS/blob/main/Data/Databases_signatures). 

 * [Figure3. GABA is mainly produced by proximal tubule-like tumour cells in ccRCC tumors](http://htmlpreview.github.io/?https://github.com/iS4i4S/GABA-TLS/blob/main/Figures/Figure3.html).
   - To reproduce Panels **A-F** you need to download data from [Hu Junyi, et al. Multi-omic profiling of clear cell renal cell carcinoma identifies metabolic reprogramming associated with disease progression. Nature Genetics (2024)](https://www.nature.com/articles/s41588-024-01662-5) available at [Zenodo](https://zenodo.org/record/8063124), the rds file [Databases_signatures](https://github.com/iS4i4S/GABA-TLS/blob/main/Data/Databases_signatures), and the Supplementary Table S16+S9 from the article.
   - To reproduce Panels **G** and **H**, you need to download the Processed spatial transcriptomic data from the GSE273952 (see Data avaliability below) and then obtain the [Starfysh (click here to see how to install)](https://github.com/azizilab/starfysh) immune deconvolution values by following this python code [Multiple-slide immune deconvolution by starfysh](http://htmlpreview.github.io/?https://github.com/iS4i4S/GABA-TLS/blob/main/Figures/Starfysh_deconvolution.html). Gene signatures to use with Starfysh can be found here: [ccRcc_TLS_gene_signatures_starfysh](https://github.com/iS4i4S/GABA-TLS/blob/main/Data/Signatures_Starfysh.csv).

 * [Figure4. TLS are closer to GABA producing tumor cells and exhibit dysfunctional immune activation in tumors from non-responding patients](http://htmlpreview.github.io/?https://github.com/iS4i4S/GABA-TLS/blob/main/Figures/Figure4.html). To reproduce any panel you need the Clinical data which is only available from the corresponding author upon reasonable request.
   - Annotating TLS-associated spots: Spatial spots belonging to TLS were defined by CD3/CD20 staining on the consecutive slide for frozen tumors or on the sample block for FFPE tumors, then we manually annotated using [Loupe Browser (10X genomics)](https://www.10xgenomics.com/support/software/loupe-browser/latest). A tutorial can be found in [Introduction to Spatial Transcriptomic Data Analysis - A Case Study of Renal carcinoma](https://www.selectscience.net/webinar/introduction-to-spatial-transcriptomic-data-analysis-a-case-study-of-renal-carcinoma). The TLS annotation of each slide can be found in the GEO under the name "TLS_annotation.csv".
   - Annotating TLS-adjacent spots: A quick function to annotate TLS-adjacent spots using a Seurat object can be found here: [TLS-adjacent annotation](https://github.com/iS4i4S/GABA-TLS/blob/main/Data/Adjacent_spot_annotation.rds).
  
 * [Figure5. TCA cycle is activated inside TLS in GABA rich areas]. Data and code is only available from the corresponding author upon reasonable request.

 * [Figure7. GABA related genes’ expression correlates with non response and shorter progression free survival in STS patients treated with pembrolizumab](http://htmlpreview.github.io/?https://github.com/iS4i4S/GABA-TLS/blob/main/Figures/Figure7.html). This includes only the code for panel **A** since it uses TCGA-SARC data. The datasets that support the findings of the PEMBROSARC study (panels **B-G**) are not publicly available due to information that could compromise research participant consent. According to French/European regulations, any reuse of the data must be approved by the ethics committee ‘CPP du Sud-Ouest et d’ Outre-Mer III’, Bordeaux, France. Individual participant data that underlie the PEMBRSOARC study results reported in this article can be shared upon request to the co-author (Antoine Italiano).



## Data avaliability
Processed spatial transcriptomic, and raw RNA-seq data from the BioniKK cohort has been deposited on gene expression omnibus (GEO) under the accession IDs [GSE273952](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE273952) and [GSE273829](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE273829), respectively. 

## Contact
E-mail any questions to [isaias.hernandez@sorbonne-universite.fr].
