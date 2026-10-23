# Lysosomal Enzyme Sequence Analysis: DNASE2 (Deoxyribonuclease II)

## Protein Overview

* **Student Name:** Ortega, Jerson Lloyd T.
* **Gene Symbol:** DNASE2
* **Enzyme Name:** Deoxyribonuclease II (Lysosomal DNase)
* **NCBI Protein Accession:** [NP_001366.1](https://www.ncbi.nlm.nih.gov/protein/NP_001366.1)
* **What it breaks down:** Exogenous and endogenous deoxyribonucleic acid (DNA), including foreign nucleic acids from pathogens, host cell DNA from apoptotic bodies, and nuclei extruded from maturing erythroblasts.
* **Normal Cellular Function:** DNASE2 is an acid hydrolase active within the acidic environment of lysosomes. It hydrolyzes phosphodiester bonds in DNA to prevent toxic intracellular accumulation of nucleic acids and suppress inappropriate innate immune activation.

---

## Analysis Workflow

1. **Data Setup and Validation:** Configured target parameters (`gene <- "DNASE2"`, `accession <- "NP_001366.1"`), loaded required R packages (`rentrez`, `ggplot2`), and initialized local project directories (`data/`, `results/`, `figures/`).
2. **Data Download:** Automatically fetched the full-length protein FASTA sequence from the NCBI Protein database using `rentrez::entrez_fetch()`, validated sequence integrity, and saved the record to `data/DNASE2.fasta`.
3. **Sequence Composition Analysis:** Parsed the polypeptide sequence to calculate total protein length (360 amino acids) and determined absolute counts and percentage frequencies for all 20 standard amino acids, exporting results to `results/DNASE2_amino_acid_counts.csv`.
4. **Motif Prediction:** Scanned the sequence for potential N-linked glycosylation consensus motifs matching N-X-S/T (where X ≠ P), exporting motif positions to `results/DNASE2_motif_positions.csv`.
5. **Visualization & Reporting:** Generated and saved two analytical plots (`figures/DNASE2_amino_acid_composition.png` and `figures/DNASE2_potential_N_glycosylation.png`).

---

## Figures and Descriptions

<img width="2048" height="1152" alt="41225" src="https://github.com/user-attachments/assets/566ae9bc-6c5d-45ff-9c18-81206a774193" />

### Figure 1: Amino Acid Composition

* **Description:** A bar chart illustrating the distribution and frequency of each standard amino acid across the 360-amino-acid sequence of human DNASE2. Leucine (L) displays the highest abundance in the primary structure (43 residues, 11.94%), followed by Alanine (A) (36 residues, 10.00%) and Serine (S) (29 residues, 8.06%).


<img width="2400" height="900" alt="41298" src="https://github.com/user-attachments/assets/71fb0561-c96a-420c-8b8b-fde8678f9edd" />

### Figure 2: Potential N-Glycosylation Motifs

* **Description:** A linear sequence coordinate map depicting the locations of 5 predicted N-glycosylation motifs (N-X-S/T, where X ≠ P) along the DNASE2 polypeptide chain at positions 86, 211, 252, 275, and 328.

---

## Questions & Answers

1. **What does your enzyme normally break down inside lysosomes?**
   DNASE2 normally hydrolyzes phosphodiester bonds in deoxyribonucleic acid (DNA) inside lysosomes under acidic pH conditions. It degrades exogenous DNA brought in via endocytosis or phagocytosis (such as viral or bacterial nucleic acids) as well as endogenous self-DNA (such as nuclear chromatin from phagocytosed apoptotic cells, damaged mitochondrial DNA, and expelled nuclei from developing erythroblasts).

2. **What is the total length of your protein, and which amino acids are most common?**
   The total precursor length of human DNASE2 (RefSeq accession `NP_001366.1`) is **360 amino acids**. Based on the amino acid composition analysis (`results/DNASE2_amino_acid_counts.csv`), the most common amino acid is **Leucine (L)** with 43 residues (11.94%), followed by **Alanine (A)** with 36 residues (10.00%), **Serine (S)** with 29 residues (8.06%), and **Glycine (G)** with 28 residues (7.78%).

3. **How many potential N-glycosylation motifs did you find? Where are they located?**
   The sequence analysis identified **5 potential N-glycosylation motifs** (N-X-S/T, where X ≠ P). According to `results/DNASE2_motif_positions.csv`, they are located at the following amino acid positions:
   * Position 86: `NCS`
   * Position 211: `NFT`
   * Position 252: `NSS`
   * Position 275: `NIT`
   * Position 328: `NGT`

4. **Why can glycosylation matter for lysosomal proteins? Does finding a motif prove the protein is glycosylated?**
   Glycosylation is critical for lysosomal proteins because it facilitates proper protein folding in the endoplasmic reticulum, protects hydrolases against premature degradation by proteases, and ensures targeting and trafficking to the lysosomal compartment. However, finding an N-X-S/T sequence motif does **not** prove the protein is actively glycosylated *in vivo*. A motif only indicates a potential attachment consensus site; actual glycosylation requires structural surface exposure and post-translational enzymatic modification in the ER/Golgi apparatus.

5. **What could happen in the cell if your enzyme did not work properly?**
   If DNASE2 is deficient or dysfunctional, phagocytic cells (such as macrophages) fail to digest the DNA of engulfed apoptotic cells or expelled erythroblast nuclei. Undegraded DNA accumulates inside lysosomes, leading to lysosomal engorgement. The uncleared DNA can trigger intracellular nucleic acid sensors (such as the cGAS-STING pathway), inducing severe chronic inflammation, autoimmune conditions (resembling systemic lupus erythematosus), inflammatory polyarthritis, and severe perinatal anemia due to blocked erythropoiesis.

---

## References

* **NCBI Protein Database:** [Human Deoxyribonuclease II (DNASE2) RefSeq Record - NP_001366.1](https://www.ncbi.nlm.nih.gov/protein/NP_001366.1)
* **NCBI Gene Database:** [Human DNASE2 Gene Entry - Gene ID: 1777](https://www.ncbi.nlm.nih.gov/gene/1777)
  
