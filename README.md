# CA2 Variant – In-silico PCR Primer Design

## Project Overview

This project evaluates a candidate PCR primer pair for the CA2 gene variant using computational tools.

The objective is to design primers that amplify a region containing the candidate variant for potential follow-up Sanger sequencing.

## Target Variant

| Field | Value |
|---|---|
| Gene | CA2 |
| Reference genome | hg19 |
| Chromosome | chr8 |
| Position | 86385980 |
| Reference allele | G |
| Alternate allele | A |
| Transcript | NM_000067.3 |
| Reported consequence | stop_gained |
| Protein consequence | p.Trp97* |

Variant annotation is transcript-dependent and does not establish clinical pathogenicity.

## Selected Primer Pair

| Property | Forward | Reverse |
|---|---|---|
| Sequence (5'-3') | TCCAGACAACGCATGTGAGG | AAGAAGTGGTTCACTGGGCG |
| Length | 20 bp | 20 bp |
| Tm | 60.32°C | 60.54°C |
| GC content | 55% | 55% |

Expected amplicon length: **488 bp**

## Workflow

1. Extracted the target region from the hg19 chromosome 8 reference.
2. Prepared a Primer3 input with the variant inside the target amplicon.
3. Designed candidate primer pairs using Primer3.
4. Evaluated primer melting temperatures and predicted secondary structures.
5. Screened primer sequences against the hg19 chromosome 8 reference using BLAST.
6. Evaluated the selected pair using NCBI Primer-BLAST.

## Specificity Assessment

The selected pair had one exact full-length match per primer in the local chromosome 8 BLAST database, with no additional near-full-length matches under the applied filtering criteria.

NCBI Primer-BLAST identified the intended 488 bp product on chromosome 8. It also reported potential unintended products on chromosomes 9 and 3, with lengths of 1052 bp and 2297 bp, respectively, and primer mismatches.

The Primer-BLAST search used GRCh38, whereas the local reference sequence was hg19.

## Project Structure

- `data/raw/`: target reference sequence
- `data/processed/`: Primer3 input and primer sequences
- `results/primer3/`: Primer3 output
- `results/blast/`: BLAST screening results
- `docs/`: detailed project report

## Tools

- Primer3
- BLAST+
- NCBI Primer-BLAST
- SAMtools
- Python

## Scope and Limitations

This is an in-silico primer design and evaluation project. No experimental PCR or Sanger sequencing validation was performed.


