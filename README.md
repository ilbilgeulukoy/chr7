Exon Lengths by Area in chr7

This repository contains an R Markdown report titled "Exon Lengths by Area in chr7", authored by ilbilgeulukoy. The report explores genomic features of chromosome 7 (chr7) using a .tsv file containing gene and transcript data.

🔬 Project Overview

The analysis focuses on exon positions, lengths, and strand distribution in chr7, with the following main components:

📁 Data Input
chr7.tsv file is loaded from the local system and cleaned using janitor::clean_names().
Data is processed using tidyverse tools for easier manipulation.

📊 Visualizations & Analyses
Exon Start Positions
Visualized as vertical bars along chromosome 7 to show their distribution.
Exon Length Statistics by Area
chr7 is divided into telomeric and centromeric regions.
Mean, standard deviation, and max exon lengths are calculated and summarized by region.
Exon Start and Length Mapping
Segment plot showing exon lengths with red markers at start positions.
Strand Distribution (+ / -)
Bar plots showing strand direction by transcript types.
Strand Ratio
Percent-based distribution of + / - strands by transcript types.
Violin Plot of mRNA Transcript Lengths
Focused on mRNA entries to visualize transcript length distributions.

📦 Packages Used :
tidyverse
janitor
readr
ggplot2
Data Source

-----------

Statistical Analysis of chr7, chr16, and chr19

This repository contains an R Markdown report titled "Statistical Analysis of chr7-16-19" by ilbilgeulukoy. The analysis compares mRNA transcript lengths across three human chromosomes: chr7, chr16, and chr19, using statistical and visualization methods in R.

📊 Project Description

The goal of this project is to explore and compare transcript length distributions of mRNAs located on chromosomes 7, 16, and 19.

🔍 Main Steps
Data Import and Cleaning
Reads .tsv files containing gene/transcript data for each chromosome.
Filters for transcript_type == "mRNA" entries only.
Transcript length is computed as stop - start.

Filtering and Cleaning
1-Filters mRNAs with lengths under 5000 base pairs.
2-Removes outliers using IQR (Interquartile Range) filtering per chromosome.

Visualizations
Boxplot: Shows transcript length distributions after IQR cleaning.
Histogram & Density Plot: Faceted by chromosome to compare shape and spread.

Statistical Tests
Shapiro-Wilk Test: Assesses normality (all p-values are extremely low, so data is not normally distributed).
Kruskal-Wallis Test: Non-parametric test to assess differences between chromosomes (significant result).
Dunn's Test: Post-hoc pairwise comparison with Bonferroni correction.


📦 Libraries Used :
tidyverse
janitor
rstatix
ggplot2
readr
knitr

The R Markdown file generates an HTML report that includes:

Cleaned data summaries
Boxplots and histograms
Statistical test results with interpretations
