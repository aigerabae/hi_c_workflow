# hi_c_workflow

This folder contains workflow on analyzing hi-C data. The input data are not raw but rather processed contacts data averaged across patients with interaction value for each cell type. The analysis presented here concerns comparing different blood cell types to each other in terms of interactions in R (PCHiC_data_processing.Rmd), visualizing the interactions in IGV browser (PCHiC_load_IGV.ipynb)  

The data are then integrated with CHiP-seq and ATAC-seq-data epigenomics data. The epigenomics data have been heavily processed, and for each ATAC-seq or ChIP-seq peak that overlaps interacting restriction fragments, the chromatin activity status (e.g. active, polycomb repressed, bivalent) has been assigned by Javierre et al. (2016) using the Chrom-HMM software, which uses a hidden Markov model-based algorithm to identify similar regions genome-wide that can then be classified based on their chromatin accessibility and chromatin marks.

