# CA2 Variant – In-silico PCR Primer Design

## 1. Project objective

Design and computationally evaluate a PCR primer pair for the
CA2 candidate variant identified in a previous exome analysis.

The purpose is to prepare an amplicon suitable for potential
Sanger sequencing. No experimental PCR or sequencing was performed.

## 2. Target variant

- Gene: CA2
- Reference assembly used for initial extraction: hg19
- Genomic coordinate: chr8:86385980
- Reference allele: G
- Alternate allele: A
- Transcript: NM_000067.3
- Predicted consequence: stop_gained
- Protein consequence: p.Trp97*

## 3. Reference sequence

- Source: hg19 chromosome 8 reference FASTA
- Extracted interval: chr8:86385480-86386480
- Template length: 1001 bp
- Variant position in template: 501 (1-based)
- Repeat-masked region excluded from primer binding:
  positions 351-431

## 4. Primer3 design parameters

- Primer length: 18-25 nt
- Optimal primer length: 20 nt
- Tm range: 58-62 °C
- Optimal Tm: 60 °C
- Maximum Tm difference: 1 °C
- GC content: 40-60%
- Product size: 400-600 bp
- Maximum homopolymer length: 4
- GC clamp: 1
- Number of returned pairs: 10

## 5. Selected primer pair

| Parameter | Forward | Reverse |
|---|---|---|
| Sequence (5'-3') | TCCAGACAACGCATGTGAGG | AAGAAGTGGTTCACTGGGCG |
| Length | 20 nt | 20 nt |
| Tm | 60.321 °C | 60.535 °C |
| GC content | 55% | 55% |

Predicted amplicon length: 488 bp.

The variant is located within the predicted amplicon, approximately
294 bp from the forward primer end and 155 bp from the reverse
primer binding region.

## 6. Secondary structure evaluation

- Forward hairpin: No secondary structure could be calculated.
- Reverse hairpin: No secondary structure could be calculated.
- Heterodimer: Predicted dimer melting temperature reported by
  ntthal was approximately -7.13 °C.

These are computational predictions and do not establish
experimental PCR performance.

## 7. Specificity evaluation

### Local BLAST

Primer sequences were searched against a local hg19 chromosome 8
database using blastn-short.

Each primer had one exact full-length match on chromosome 8.
No additional full-length matches with up to two mismatches
were observed for the selected pair in this chromosome-only search.

This analysis does not represent a whole-genome specificity test.

### NCBI Primer-BLAST

The supplied Primer-BLAST result reported:

- Chromosome 8 (GRCh38.p14): 488 bp product with exact primer matches.
- Chromosome 9: potential 1052 bp product with mismatches.
- Chromosome 3: potential 2297 bp product with mismatches.

The two additional predicted products are outside the intended
400-600 bp product-size range. Their presence means that
specificity should not be described as absolute.

The initial template was extracted from hg19, whereas the
Primer-BLAST result shown uses GRCh38 coordinates. These
assemblies must be distinguished when reporting coordinates.

## 8. Conclusion

A candidate primer pair was designed computationally for the
CA2 target region. The pair has closely matched melting
temperatures, suitable GC content, and a predicted 488 bp
amplicon containing the candidate variant.

Local chromosome 8 BLAST and NCBI Primer-BLAST provided
supporting in-silico specificity evidence, with additional
potential products reported on chromosomes 3 and 9.

The primer pair remains a computational candidate. Experimental
PCR optimization and Sanger sequencing are required to establish
actual amplification performance and confirm the target sequence.

This project is educational and computational. It does not
constitute clinical variant interpretation or diagnosis.
