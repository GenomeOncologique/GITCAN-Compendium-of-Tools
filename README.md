[![License](https://img.shields.io/badge/License-BSD\%202--Clause-orange.svg)](https://opensource.org/licenses/BSD-2-Clause)

In the current study, we conducted a rigorous cross-cancer analysis across multiple gastrointestinal cancers (GITCANs), encompassing a range of phenotypically and genotypically distinct tumors, including esophageal, gastric, colon, and rectal cancers. We assessed metaplastic transitions, oncogenic processes, and gene expression profiles at various disease stages, providing a broad and in-depth comparison of these cancers. Our methodology introduced advanced tools via the GITCAN-compendium suite (POpCan, QuantPlasia, and PlasiaCorrelationProfiler), which enabled the examination of metaplastic epithelium and cancerous tissues across different GIT regions and stages. We applied both qualitative and quantitative analyses to capture the heterogeneity of gene-correlation profiles, transcriptional bursting, and genomic alterations, offering a robust, multi-dimensional view of the molecular drivers behind gastrointestinal cancer progression. This comprehensive cross-cancer framework not only identifies critical biomarkers and prognostic factors but also highlights shared and unique features among GITCANs, providing valuable insights into their complex biology.

# POpCan

Several genes, including pseudogenes often exhibit spatiotemporal expression specificity making them potentially valuable biomarkers. The current tool explores and quantifies the absence (indirectly exploring the presence) of such spatiotemporal expression specificity across multiple categories (up to 3) of cancer, including cancer type (CT), stage (ST) and deregulation type (DT). The analysis based on all 3 categories can include the sub-categories within and between the cancer types or it can be restricted to the sub-categories between the cancer types using the conditions 'Within' and 'Between', respectively. The possible combinations for the conditions 'Within' and 'Between' can be represented using the combination formula C(n,k) as follows:

The possible combinations for 'Within' =  C((CT * ST * DT),2)

The possible combinations for 'Between' = C((CT * ST * DT),2)-[CT * (C((ST * DT),2))]

Thus, for 4 cancer types, each having 4 stages with 2 deregulation types will have total possible combinations as 496 for 'Within' and 384 for 'Between'.

This current tool, can be extrapolated to other user-defined subcategories or disease conditions to effectively identify valuable biomarkers.

# QuantPlasia

Well-coordinated events of epithelial differentiation are essential for the homeostasis and repair of the adult gastrointestinal tract epithelium. However, persistent GI tract repair, primarily due to prolonged inflammation causing factors such as GERD, and allergens in the esophagus, Helicobacter pylori infection in the stomach, inflammatory bowel disease, Crohn’s disease, and ulcerative colitis in the intestines, leads to aberrant epithelial homeostasis.

The resultant impaired epithelial differentiation eventually leads to 'Metaplasia'; a pre-cancerous condition. In the esophagus, it results in Barrett's metaplasia (often called either gastric or intestinal metaplasia depending on the cell types observed), where esophageal cells are replaced by gastric and/or intestinal cells. In the stomach, this often results in intestinal metaplasia and pseudopyloric or pyloric metaplasia, which may progress to spasmolytic polypeptide-expressing metaplasia (SPEM). Similarly, pyloric cell metaplasia has been observed in the small intestine and colon, while Paneth cell metaplasia occurs in the colon and rectum, and squamous cell metaplasia in the rectum.

Based on gene-expression dependent enrichment profiles obtained using GSEA, *QuantPlasia* identifies the existence of such metaplastic events and utilises the metric 'Degree of Differentiation' (here, 'Extent of Differentiation') to quantify the same.

# PlasiaCorrelationProfiler

Metaplastic epithelium comprises both tissue-resident and non-resident cells. Tissue non-resident cells, when located in a different tissue, often retain phenotypic characteristics similar to those of the cells naturally found in their original tissue, but their genotypic characteristics may differ. Given the stochastic nature of cancer progression, where cells often acquire genetic alterations independent of change in phenotypic characteristics, we developed a tool to assess whether the non-resident cells of the metaplastic epithelium are genotypically more similar to the normal cells of the resident tissue or to the cancerous cells of the resident tissue. This distinction is crucial for understanding the molecular mechanisms driving metaplasia and its potential role in cancer progression.  

The genotypic similarity between two given cohorts was assessed by estimating the extent of similarity of gene-correlation profile of one cohort with another where, gene-correlations are obtained using the genes that contribute to the extent of metaplasia-associated differentiation (MAD; identified using *Quantplasia*). 

**References**  
[1] Subramanian A, Tamayo P, Mootha VK, Mukherjee S, Ebert BL, Gillette MA, et al. Gene set enrichment analysis: a knowledge-based approach for interpreting genome-wide expression profiles. Proc Natl Acad Sci.2005;102(43):15545–50  
[2] Pravallika G, Rajasekaran R. Stage II oesophageal carcinoma: peril in disguise associated with cellular reprogramming and oncogenesis regulated by pseudogenes. BMC Genomics. 2024 Feb 2;25(1):135  
[3] Chang LJ, Jolly E, Cheong JH, Rapuano KM, Greenstein N, Chen PHA, et al. Endogenous variation in ventromedial prefrontal cortex state dynamics during naturalistic viewing reflects affective experience. Sci Adv. 2021 Apr 23;7(17):eabf7129.  
[4] Eid M, Gollwitzer M, Schmitt M. Statistik und Forschungsmethoden [Statistics and research methods]. 5th ed. Weinheim, Germany: Beltz; 2017.  

COPYRIGHT

Copyright (c) 2024, Pravallika Govada All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

CONTACT INFORMATION

Please address any queries or bug reports to Pravallika Govada at pravallika.govada2018@vitstudent.ac.in or pravallika2606g@gmail.com
