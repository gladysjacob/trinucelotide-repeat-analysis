# Comparative Analysis of Chromosome Trinucleotide Repeats

## Overview
This project performs a genome-scale comparative analysis of **trinucleotide tandem repeats** across two human chromosomes with contrasting biological properties:

- **Chromosome 1** — the largest human chromosome with moderate gene density
- **Chromosome 19** — a smaller, highly gene-dense, GC-rich chromosome

Using the GRCh38 human reference genome and Ensembl annotations, the analysis investigates how trinucleotide repeat distribution relates to **gene density, chromatin context, and genomic region**, rather than chromosome size alone.

---

## Research Question
**How do trinucleotide repeat patterns differ between chromosomes with contrasting sizes and gene densities?**

### Hypothesis
Trinucleotide repeat abundance is influenced primarily by **local genomic context** (gene density and chromatin state) rather than global chromosome size.

---

## Methods

### Data Sources
- **Genome assembly:** GRCh38 (Homo sapiens)
- **FASTA & GFF3 files:** Ensembl Release 114
- **Chromosomes analyzed:** Chr 1 and Chr 19

### Repeat Detection
- Tool: `PyTRF (STRFinder)`
- Motif length: 3 bp (trinucleotides only)
- Minimum repeat threshold: ≥3 copies (≥9 bp)

### Annotation
Each detected trinucleotide repeat was annotated for:
- **Genic vs intergenic location** (using GFF3 gene coordinates)
- **Chromosomal region**:
  - Telomere (first/last 10 kb)
  - Centromere
  - Euchromatin

### Analysis
- Repeat density per megabase
- Motif frequency and conservation
- Genic enrichment
- Regional distribution
- Comparative statistics across chromosomes

---

## Key Results

### 🔹 Trinucleotide Density
- **Chr 19 shows 1.64× higher trinucleotide density** than Chr 1
- Despite being ~4× smaller, Chr 19 contains ~39% as many repeats

**Conclusion:** Repeat abundance scales with **gene density**, not chromosome size.

---

### 🔹 Genic Association
- Chr 1: ~50% genic repeats
- Chr 19: ~59% genic repeats (+8.7%)

This enrichment mirrors Chr 19’s ~3× higher gene density, supporting a functional association between trinucleotide repeats and genes.

---

### 🔹 Motif Conservation
- Top motifs are **identical** between chromosomes (AAT, TTG, TTA, AAC, ATT)
- All dominant motifs are AT-rich (66–100% AT)

This suggests conserved biochemical or structural constraints on trinucleotide formation across the genome.

---

### 🔹 Chromosomal Regions
- ~99.9% of trinucleotide repeats localize to **euchromatin**
- Near absence in centromeres and complete absence in telomeres

This validates both the detection methodology and known chromatin biology.

---

## Technologies Used
- Python
- Pandas, NumPy
- PyTRF, pyfastx
- Matplotlib, Seaborn
- BED/GFF-based genomic annotation

---

## Reproducibility
The notebook can be run end-to-end after installing dependencies listed below.


