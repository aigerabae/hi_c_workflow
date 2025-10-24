# hi_c_workflow

This folder contains workflow on analyzing hi-C data. The input data are not raw but rather processed contacts data averaged across patients with interaction value for each cell type. The analysis presented here concerns comparing different blood cell types to each other in terms of interactions in R (PCHiC_data_processing.Rmd), visualizing the interactions in IGV browser (PCHiC_load_IGV.ipynb)  

The data are then integrated with CHiP-seq and ATAC-seq-data epigenomics data. The epigenomics data have been heavily processed, and for each ATAC-seq or ChIP-seq peak that overlaps interacting restriction fragments, the chromatin activity status (e.g. active, polycomb repressed, bivalent) has been assigned by Javierre et al. (2016) using the Chrom-HMM software, which uses a hidden Markov model-based algorithm to identify similar regions genome-wide that can then be classified based on their chromatin accessibility and chromatin marks.

They have further processed the data and derived single activity status calls for each promoter containing fragment or their interacting “other end” fragments. Normally, it would be your job to do this as a bioinformatician, but as it is a time-consuming process, they have done it for you and this is not part of the assignment. Nevertheless, we encourage you to think about strategies for how to do this step. In this analysis, you will perform a statistical analysis of these data using RStudio, to address the following question:  

- Are chromatin contacts enriched at gene regulatory features/chromatin marks?  
PCHiC_epigenomics_integration.Rmd file contains that analysis; it tests association between promoters and enhancers activation status
