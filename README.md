# GABA-TLS
Code for reproducing analysis on the paper "GABA promotes resistance to immunotherapy of patients with TLS-positive tumours".
![alt text](https://github.com/iS4i4S/GABA-TLS/blob/main/Data/Graphical_abstract.jpg "Graphical Abstract")

## Abstract

Tertiary lymphoid structures (TLS) in the tumour microenvironment have been linked to positive clinical outcomes and responses to immune checkpoint inhibitors (ICI) in various cancers, including clear cell renal cell carcinoma (ccRCC) and soft tissue sarcoma (STS). However, a significant proportion of patients do not respond to ICI despite the presence of TLS. Our study unravels gamma-aminobutyric acid (GABA), a neurotransmission inhibitor, as a modulator of ICI resistance in TLS-positive tumours. By leveraging household and public multi-omic data, we demonstrated that GABA is upregulated in TLS-positive ccRCC and STS tumours from non-responders to ICI. In metastatic ccRCC, TLS from non-responders were distinguished from responders by a dysfunctional immune activation and a close proximity to GABA-producing proximal tubule-like tumour cells. The addition of a competitive inhibitor of GABA synthesis, 3-mercaptopropionic acid, significantly improved tumour control when compared to anti-PD1 alone when intra-tumourally injected in a mouse model of STS. Overall, our findings highlight GABA as a novel determinant of non-response to ICI in tumours harboring TLS, suggesting potential new approaches for patient stratification and personalized therapeutic strategies that could be applicable beyond metastatic ccRCC and STS.

## Citation
If you use any data or code derived from this study, please cite:

- Isaias Hernández-Verdin, Anne Calvez, et al. GABA promotes resistance to immunotherapy of patients with TLS-positive tumours.  Under revision (202X).
- DOI: Currently under revision.


## Code to reproduce main Figures
Visualize HTML files containing the code for each main figure by clicking on the coresponding links here:

 * [Figure1. High expression of GABA signatures is associated with non-response to immunotherapies in TLS-positive ccRCC tumours](http://htmlpreview.github.io/pending): To reproduce this figure you need to download the raw counts data (raw_counts_kallisto.tab) from the GEOXXXX (see Data avaliability below). Clinical data is needed to reproduce this Figure but is only available from the corresponding author upon reasonable request. 

 * [Figure2. High expression of GABA ccRCC signature is associated with decreased immune activation in TLS-positive ccRCC tumours from ICI-treated patients](http://htmlpreview.github.io/pending): To reproduce this figure you need to download the raw counts data (raw_counts_kallisto.tab) and preprocess it according to [Figure1.html](http://htmlpreview.github.io/pending). You also need the "GABA high" & "GABA low" labels for each patient available in [GABA labels](pending). 

 * [Figure3. GABA is mainly produced by proximal tubule-like tumour cells in ccRCC tumours](http://htmlpreview.github.io/pending).
   - To reproduce Panels **a-g** you need to download data from [Hu Junyi, et al. Multi-omic profiling of clear cell renal cell carcinoma identifies metabolic reprogramming associated with disease progression. Nature Genetics (2024](https://www.nature.com/articles/s41588-024-01662-5) available at [Zenodo](https://zenodo.org/record/8063124).
   - To reproduce Panels **h** and **i**, you need to download the Processed spatial transcriptomic data from the GEOXXXX (see Data avaliability below) and then obtain the [Starfysh (click here to see how to install)](https://github.com/azizilab/starfysh) immune deconvolution values by following this python code [Multiple-slide immune deconvolution by starfysh](pending). Gene signatures to use with Starfysh can be found here: [ccRcc_TLS_gene_signatures_starfysh](pending).

 * [Figure4. TLS are closer to GABA producing tumour cells and exhibit dysfunctional immune activation in tumours from non-responding patients](http://htmlpreview.github.io/pending). To reproduce any panel you need the Clinical data which is only available from the corresponding author upon reasonable request.
   - Annotating TLS-associated spots: Spatial spots belonging to TLS were defined by CD3/CD20 staining on the consecutive slide for frozen tumours or on the sample block for FFPE tumours, then we manually annotated using [Loupe Browser (10X genomics)](https://www.10xgenomics.com/support/software/loupe-browser/latest). A tutorial can be found in [Introduction to Spatial Transcriptomic Data Analysis - A Case Study of Renal carcinoma](https://www.selectscience.net/webinar/introduction-to-spatial-transcriptomic-data-analysis-a-case-study-of-renal-carcinoma). 

 * [Figure5. GABA related genes expression correlates with non response and shorter progression free survival in STS patients treated with pembrolizumab and GABA synthesis inhibitor increases response to anti-PD1 in STS tumours](http://htmlpreview.github.io/pending). This includes only the code but data regarding the Figure cannot be shared. The datasets that support the findings of the PEMBROSARC study are not publicly available due to information that could compromise research participant consent. According to French/European regulations, any reuse of the data must be approved by the ethics committee ‘CPP du Sud-Ouest et d’ Outre-Mer III’, Bordeaux, France. Individual participant data that underlie the PEMBRSOARC study results reported in this article can be shared upon request to the co-author (Antoine Italiano).


## Data avaliability
Processed spatial transcriptomic, and raw RNA-seq data from the BioniKK cohort has been deposited on gene expression omnibus (GEO) under the accession IDs [GSEXXXXXX](pending). 

## Contact
E-mail any questions to [isaias.hernandez@sorbonne-universite.fr].
