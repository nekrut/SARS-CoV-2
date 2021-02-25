## Files

This directory contains processed varinat calls based on the following data:

| Files | Nicknames | Origin |
|-----|------------------|--------|
| bos_by_sample.tsv.gz <br>bos_by_var.tsv.gz| **"Boston"** | Entire PRJNA622837 |
|cog_20200917_by_sample.tsv.gz <br>cog_20200917_by_var.tsv.gz| **"COG-Pre"** | Pre B.1.1.7 portion of PRJEB37886 |
| cog_20201120_by_sample.tsv.gz <br>cog_20201120_by_var.tsv.gz| **"COG-Post"** | Post B.1.1.7 portion of PRJEB37886 |

## Datasets `by_variant`

|    | Field                     | Example                                                     | Meaning |
|-----|:--------------------------|:------------------------------------------------------------|---------|
|1| `POS`                       | 25931                                                       | Position in [NC_045512.2](https://www.ncbi.nlm.nih.gov/nuccore/1798174254) |
|2| `REF`                       | C                                                        .  | Reference base |
|3| `ALT`                       | T                                                           | Alternative base |
|4| `IMPACT`                    | MODERATE                                                    | Functional impact (from SNPEff) |
|5| `FUNCLASS`                  | MISSENSE                                                    | Funclass for change (from SNPEff) |
|6| `EFFECT`                    | NON_SYNONYMOUS_CODING                                       | Effect of change (from SNPEff) |
|7| `GENE`                      | ORF3a                                                       | Gene |
|8| `CODON`                     | tCt/tTt                                                     | Codon |
|9 |`AA`                        | S180F                                                       | Amino acid |
|10|`TRID`                      | orf3a                                                       | Short name for the gene |
|11|`countunique(Sample)`       | 10                                                          | Number of distinct samples containing this change |
|12|`min(AF)`                   | 0.000787                                                    | Minimum Alternative Allele Freq across all samples containing this change |
|13|`max(AF)`                   | 0.10924400000000001                                         | Maximum Alternative Allele Freq across all samples containing this change |
|14|`SAMPLES(above-thresholds)` | ERR4860859                                                  | Number of distinct samples where this change has frequency abobe threshold (5%) |
|15|`SAMPLES(all)`              | ERR4860800,ERR4860859,ERR4859778 (7 more entries not shown) | Number of distinct samples conatining this change at any frequency (including below threshold) |
|16|`AFs(all)`                  | 0.001387,0.109244,0.001288 (7 more entries not shown)       | List of all allele frequencies across all samples |
|17|`change`                    | C>T                                                         |  Change |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

## Datasets `by_sample`

| # |  Column               | Example value     | Meaning |
|--|:----------------------|:------------------|---------|
|1| `Sample`                | ERR4859727        | SRA run ID |
|2| `POS`                   | 22388             | Position in [NC_045512.2](https://www.ncbi.nlm.nih.gov/nuccore/1798174254) |
|3| `FILTER`                | PASS              | `Filter` field from VCF |
|4| `REF`                   | C                 |  Reference base |
|5| `ALT`                   | T                 | Alternative base |
|6| `DP`                    | 13756             | Sequencing depth |
|7| `AF`                    | 0.924106          | Alternative allele frequency |
|8| `SB`                    | 0                 | Alternative allele frequency |
|9| `SB`                    | 2147483647        | Strand bias P-value from Fisher's exact test calculated by [`lofreq`](https://csb5.github.io/lofreq/) |
|10|`DP4`                   | 1,0,13700,0       | Depth for Forward Ref Counts, Reverse Ref Counts, Forward Alt Counts, Reverse Alt Counts |
|11|`IMPACT`                | LOW               | Functional impact (from SNPEff) |
|12|`FUNCLASS`              | SILENT            | Funclass for change (from SNPEff) |
|13|`EFFECT`                | SYNONYMOUS_CODING | Effect of change (from SNPEff) |
|14|`GENE`                  | S                 | Gene name |
|15|`CODON`                 | Cta/Tta           | Codon |
|16|`AA`                    | L276              | Amino acid |
|17|`TRID`                  | S                 | Short name for the gene |
|18|`min(AF)`               | 0.0009            | Minimum Alternative Allele Freq across all samples containing this change |
|19|`max(AF)`               | 0.94334           | Maximum Alternative Allele Freq across all samples containing this change |
|20|`countunique(change)`   | 3                 | Number of distinct types of changes at this site across all samples |
|21|`countunique(FUNCLASS)` | 3                 | Number of distinct FUNCLASS values at this site across all samples |
|22|`change`                | C>T               | Change at this site in this sample |