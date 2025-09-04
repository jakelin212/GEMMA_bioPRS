# GEMMA_bioPRS
GEMMA bioPRS is created to describe the workflow designed to construct and evaluate polygenic risk scores, comparing standard to biomarker (pathways and microbiome) informed based. The work is ongoing, and the workflow, created by Niina Väljä (niina.valja@tuni.fi) below captures the current iteration:
<img width="770" height="850" alt="GEMMA_PRS_Workflow" src="https://github.com/user-attachments/assets/05408c89-baba-4caa-bc24-c145041043ab" />

The pipeline assumes that WGS or imputed genotypes are processed and of high quality. 
Using plink2, We construct standard ASD PRS using Grove et al. 2019 PRS variants ( hglift is applied ) and effect estimates (https://www.pgscatalog.org/trait/EFO_0003756/). 
Biomarker informed PRS are built using 1) SFARI adjusted based genes (https://gene.sfari.org/). 
2) Pathway enrichment is performed and we identified the most relevant pathways (related to Gut brain axis and signaling based on gene membership)
PRS scores are tested with logistic regression and adjusted with population principle components
3) Microbiome exposures are identified and tested together with models from 2.

The established scripts and workflow will be made available together with the GEMMA main paper.





