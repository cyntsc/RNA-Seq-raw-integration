## The scripts correspond with the next workflow:

PASO 1: Raw-count integration
Script: 1_Step1_integrating_raw_counts 

PASO 2: TPM normalization
Script: 2_Step2_TPM_normalization.ipynb
*Require to prepare a gene length file.

PASO 3: Data standardization; cut off extreme and underrepresented values.
Script: TPM_standardization.ipynb 

PASO 4: Data log transformation and atypical sample identification; reduce scale and identify noise.
Script: Log2_scale.ipynb 

Additional resources:
Script to extract gene lengths for step 2.
Gene_length_extraction_from_GTF.ipynb (extract gene lengths for normalization)

Script to extract gene modules for annotation tasks
6_modules_percentual_differentiation.ipynb

Script to make logic comparison
Venn_diagram_genes_in_ceros.ipynb 

Cynthia Soto

