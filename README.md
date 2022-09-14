# RNA-Seq-matrix-integration framework
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7076416.svg)](https://doi.org/10.5281/zenodo.7076416)

Four-Step methodology to integrate raw RNA-Seq counts into a normalized and standardized expression matrix
<br><br>
Preprint can be read on:
[Named Link](http://www.google.fr/ "Named link title") and http://www.google.fr/ or <http://example.com/>
<br><br>
Cite us as: ****** (in progress)

<h3>What are the 4-steps?</h3>

* Step 1-Integration of raw-counts.<br>
* Step 2-Data normalization of raw-counts.<br>
* Step 3-Data standardization. <br>
* Step 4-Scaling requirements and outlier identification.<br><br>

<h3>Where does the data come from?</h3>

* Data are bulk RNASeq libraries downloaded from the SRA-NCBI:<br>
* ID Bioprojects: <br>
  * PRJNA148307 (SRR364389, SRR364390, SRR364391, SRR364392, SRR364400, SRR364401, SRR364398 and SRR364399) for arabidopsis infected with Colletotrichum higginsianum at 22 and 40 hpi<br>
  * PRJNA315516 (SRR3383696, SRR3383697,  SRR3383779 and SRR3383780) for arabidopsis infected with Botrytis cinerea at 12 and 18 hpi<br>
  * PRJNA593073 (SRR10586397 and SRR10586399) for arabidopsis infected with Botrytis cinerea at 24 hpi<br>
  * PRJNA418121 (SRR6283146, SRR6283147 and SRR6283148) for arabidopsis infected with Sclerotinia sclerotiorum at 30 hpi<br>
  * PRJNA315516 (SRR3383640 and SRR3383641) for arabidopsis healthy plant mock at 12hr, (SRR3383782 and SRR3383783) mock at 18 hr and (SRR3383821 and SRR3383822) mock treatment at 30hr, and PRJNA418121 (SRR6283144 and SRR6283145) mock at 30hr. <br><br>

<h3>What is the experimental design?</h3>

* The experiment was designed in 2 blocks. 
  * First block with 8 transcriptomes from healthy plants arranged in 4 groups for control (healthy12, healthy18, healthy24 and healthy30)
  * Second block with 17 transcriptomes from infected plants in interaction with three Ascomycete fungi (B=Botrytis cinerea, Ch=Colletotrichum higginsianum, and Ss=Sclerotinia sclerotiorum) arranged in 5 groups for the treatments (Bc12, Bc18, Bc24, Ch22, Ch40 and Ss30) --the digits correspond to the time of inoculation (hpi) with the fungus.<br>
* The treatments represent 68% of the total samples included (32% for C higginsianum, 24% for B cinerea and 12% for S sclerotiorum), and the 32% of the remaining samples corresponds to the controls.<br>
* The RNA was extracted from leaf among a range from 0 to 48 hpi <br>
* Only NGS Illumina libraries were considered <br>
* Minimum read lenght=100 <br>
* Minimum library size=5 millions of reads <br><br>

<h3>What is the analytical method used?</h3>

* RNASeq raw-counts were estimated and aligned to gene reference TAIR10 (GenBank accessions CP002684 – CP002688) <br>
* Quantification was done with the annotation reference ARAPORT11 with a target of 27655 Protein-Coding-Sequence (CDS) <br>
* The **expression matrices** were prepared following the **4-step methodology proposed here** <br>
* Agglomerative clustering (ML not-supervised) was performed with the WGCNA tool to evaluate the expression matrices <br>
  * Signed-networks with the *Pearson* method <br>
  * Threshold cut off close to 𝛃=0.80 <br>
  * Clustering results were merged at 0.1 distances <br>
* Gene-Modules (GM) from the networks with corr ≷ 0.75 and p-values<0.05 were identified <br>
* GM of infected plants identified & differentiated in more than 77% from the GM of healthy plants were annotated with the GO-Slim clasiffication from TAIR <br><br>

<h3>CONTENT OF THIS REPOSITORY</h3>

* notebooks:** Phython scritps to implement the 4-Step framework proposed <br>
* HTC_scripts_biotools:** linux scripts to calculate the raw-counts files <br>
* WGCNA_RScripts:** R scripts to build the gene-networks <br>
* meta-data:** files with meta-data to link to the gene-networks.<br>
* results-data:** all the results produced into this framework, including intermedian files.<br><br>

<h3>Quick search:</h3>
<h4>Where are the normalized and standardized expression matrices?</h4>

* /results-data/matrices_de_expresion/matrix_D_healthy.csv    <br>
* /results-data/matrices_de_expresion/matrix_E_infected.csv   <br>

<h4>Where are the raw expression matrices?</h4>

* /results-data/matrices_de_expresion/matrix_A_healthy.csv     <br>
* /results-data/matrices_de_expresion/matrix_A_infected.csv     <br>

<h4>Where are gene-modules identified with WGCNA?</h4>

* /results-data/wgcna_GM_logical_comp_SFT/*                     <br><br>

Any doubt, please write me to cyntsc10 at gmail dot com

Best :thumbsup: <br>
**Cynthia SC**
