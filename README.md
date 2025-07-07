# HeLa Proteome: Cracking the code of RNA-Dependency
## Characterization of Proteins Based on Biophysical Properties

### Authors

* Mirjam Biollaz (mirjam.biollaz@stud.uni-heidelberg.de)
* Hasset Gesesse (hasset.gesesse@stud.uni-heidelberg.de)
* Jette Klempt-Gießing (jette.klempt-giessing@stud.uni-heidelberg.de)
* Alicia Weeber (alicia.weeber@stud.uni-heidelberg.de)

### Supervisors
* Dr. Maïwen Caudron-Herger (m.caudron@dkfz.de)
* Tutor: Michela Pozzi (M.Pozzi@stud.uni-heidelberg.de)

## Abstract
<p align="justify">
Over time, RNA has been attributed an increasingly important role. The molecule no longer serves merely transcription and translation but also has a decisive influence on many other physiological and pathological processes. In this context, RNA is supported by numerous proteins, which can be collectively referred to as “RNA-dependent proteins.” A protein is considered RNA-dependent if its interactome depends on RNA, even if it does not directly bind to RNA itself.
</p> <p align="justify">
The complexes formed by RNA and proteins are called ribonucleoprotein complexes. These complexes are highly dynamic and can change significantly depending on the cellular task and extracellular stimuli. Besides transcription and translation, they also play a central role in RNA metabolism, regulation of gene expression, and transcriptional regulation of both mRNAs and non-coding RNAs. Therefore, defects in the function of these proteins can be associated with severe diseases.
</p> <p align="justify"> 
By targeted analysis and identification of proteins that are RNA-dependent, new mechanisms controlled by RNA can be elucidated, potentially leading to new therapeutic approaches.
</p> <p align="justify">
To this end, we investigated a series of proteins from HeLa cells synchronized in the interphase. For this, a HeLa cell lysate was either treated with an RNase cocktail or left untreated as a control sample. Both samples were each prepared in triplicates, loaded onto a sucrose density gradient, separated into 25 fractions according to density and size, and subsequently the protein content in each fraction was quantified by mass spectrometry.
</p> <p align="justify">
The underlying idea is that RNA-dependent proteins change their position in the density gradient in the presence or absence of RNA, showing a so-called “shift.” Therefore, the goal of our analysis is to classify proteins as non- or fully RNA-dependent based on these mass spectrometry data.
</p>

## Repository structure

#### 1. Project Setup
* The required R packages are listed at the top of the HTML report (`Data_analysis_project_group_3.3_code.html`).

#### 2. Analysis Outline
* **Data Cleaning & Normalization**
  * Handles missing values and normalizes intensity across gradients
  * Visual checks for replicate reproducibility (correlation & violin plots)
* **Exploratory Data Analysis**
  * Identifies RNA-dependent shifts across RNase-treated and control samples
  * Generates distribution plots of protein classes
* **Dimensionality Reduction**
  * **PCA & K-means clustering** to identify patterns in protein behavior
* **Modeling & Interpretation**
  * **Linear regression**: shift score predicted by isoelectric point and mass  
  * **Logistic regression**: zinc finger motifs as predictors for RNA-dependency  
  * Comparison to **[R-DeeP database](https://r-deep3.dkfz.de)**
  
Link to Full interactive report: **[Data_analysis_project_group_3.3_code.html](./Data_analysis_project_group_3.3_code.html)**  
(Download the file and open locally in your browser – includes a clickable Table of Contents for easy navigation) 

#### 3. Datasets
- **Mass Spectrometry Data:** **`ms_table`**: Mass spectrometry data (raw input) from HeLa cell gradient fractions
- **External Databases Used:**
  - [**R-DeeP v3**](https://r-deep3.dkfz.de): Reference dataset for RNA-binding and RNA-dependent protein
  - [**UniProt**](https://www.uniprot.org): Used to retrieve metadata like protein mass, isoelectric point, and functional annotations


#### 4. Additional Resources & Poster

- **Poster visuals** generated during the analysis are included in the `/postervisuals` folder.
- The final **poster PDF** summarizing the project is linked here: [Project Poster (PDF)](./Data_analysis_project_group_3.3_poster.pdf)
- All intermediate results, raw and cleaned data, and exploratory steps are stored in the `/archiv` folder.

## References

  * Sternburg et al., *Global Approaches in Studying RNA-Binding Protein Interaction Networks*, 2020, Trends in Biochemical Sciences.
  * Corley et al., *How RNA-Binding Proteins Interact with RNA Molecules and Mechanisms*, 2020, Molecular Cell.
  * Gebauer et al., *RNA-binding proteins in human genetic disease*, 2020, Nature Reviews Genetics.
  * Caudron-Herger et al., *R-DeeP Proteome-wide and Quantitative Identification of RNA-Dependent Proteins by Density Gradient Ultracentrifugation*, 2019, Molecular Cell.
  * Caudron-Herger et al., *Identification, quantification and bioinformatic analysis of RNA-dependent proteins by RNase treatment and density gradient ultracentrifugation using R-DeeP*, 2020, Nature Protocols.
  * Rajagopal et al., *Proteome-Wide Identification of RNA-Dependent Proteins in Lung Cancer Cells*, 2022, Cancers.
  * Rajagopal et al., *An atlas of RNA-dependent proteins in cell division reveals the riboregulation of mitotic protein-protein interactions*, 2025, Nat. Commun.