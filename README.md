# Gene Promoter-Peak Overlap Analysis

This repository contains an R script for identifying genes whose promoter regions overlap with peak regions from ChIP-Seq or CUT&RUN experiments. The script processes genomic data from GTF and BED files, correctly accounts for both DNA strands, and allows users to specify the output file name.

## Features

- Extracts **promoter regions** from a GTF file.
- Accounts for **both positive and negative strands** when defining promoter regions.
- Finds **overlapping peaks** from a BED file using `GenomicRanges`.
- Allows **customization of upstream and downstream regions** when defining promoters.
- Saves results to a user-specified CSV file.

## Requirements

This script requires the following R packages:

- `GenomicRanges`
- `GenomicFeatures`
- `rtracklayer`
- `dplyr`
- `readr`
- 'tidyverse'

You can install any missing dependencies using:

```r
install.packages("dplyr")
install.packages("readr")
install.packages("tidyverse")
if (!requireNamespace("BiocManager", quietly = TRUE)) install.packages("BiocManager")
BiocManager::install(c("GenomicRanges", "GenomicFeatures", "rtracklayer"))
```

## Customization

- **Change Upstream & Downstream Lengths**: Modify `upstream` and `downstream` values in `extract_promoters_from_gtf()`.
- **Specify Output File**: Provide a custom file name in `find_promoter_overlaps()`.

## License

This project is open-source.

