![long-read-tools.org](docs/img/banner.png)

# long-read-tools.org

[![Project Status](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)
[![Lifecycle](https://img.shields.io/badge/lifecycle-stable-brightgreen.svg)](https://www.tidyverse.org/lifecycle/#stable)

A database of software tools for the analysis of long read sequencing data. To
make it into the database software must be available for download and public use
somewhere (CRAN, Bioconductor, PyPI, Conda, GitHub, Bitbucket, a private website
etc). To view the database head to https://www.long-read-tools.org.

## Purpose

This database is designed to be an overview of the currently available long read
analysis software, it is unlikely to be 100% complete or accurate but will be
updated as new software becomes available. If you notice a problem or would like
to add something please make a pull request or open an issue.

## Citation

If you find the database useful, please consider citing our [publication](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-1935-5) in your work:

*Amarasinghe, S.L., Su, S., Dong, X. et al. Opportunities and challenges in long-read sequencing data analysis. Genome Biol 21, 30 (2020). https://doi.org/10.1186/s13059-020-1935-5*

## Structure

The main tools table has the following columns:

* **Name**
* **Platform** - Programming language or platform where it can be used
* **DOIs** - Publication DOIs separated by semi-colons
* **PubDates** - Publication dates separated with semi-colons. Preprints are
  marked with PREPRINT and will be updated when published.
* **Code** - URL for publicly available code.
* **Description**
* **License** - Software license
* **Technologies in Focus** - Long read sequencing technologies of the 
data available tools are developed for 
* ***Categories*** (Described below)

### Categories

The categories are TRUE/FALSE columns on the `lrs_tools_master.csv` indicating if the software has a
particular function. These are designed to be used as filters, for example when
looking for software to accomplish a particular task. They are also the most
likely to be inaccurate as software is frequently updated and it is hard to
judge all the functions a package has without making significant use of it. You wil see that there 
some tools hve been reported for multiple categories. The
categories are assigned based on whether the tool:
* **Alignment** -  Aligns long reads to a reference
* **BaseCalling** -  Detects of change of electrical current produced by ONT sequencers and translate it to a DNA sequence
* **LongReadOverlapping** - Finds pairs of reads that align to each other
* **DenovoAssembly** - Assembles long reads
* **GeneratingConsensusSequence** - Generate a consensus sequence from the assembled reads
* **AnalysisPipelines** - Is a pipelines that include several tools
* **ErrorCorrectionAndPolishing** - Corrects the errors to improve the genome assembly or reads before assembly. Some use a hybrid method of using short reads to achieve long reads with high accuracy
* **GeneExpressionAnalysis** - Tests of differential expression across samples
* **EvaluatingExisitingMethods** - Benchmarks and/or evaluates functionality of existing tools and/or generating synthetic long read datasets
* **GapFilling** - Improves existing assemblies based on localised alignment and assembly
* **IsoformDetection** - Identifies multiple isoforms encoded by a single gene due to alternative splicing
* **BaseModicifactionDetection** - Identifies modifications to individual bases like 5-methylcytosine, 5-hydroxymethylcytosine, and N6-methyladenine in DNA sequences
* **ProvideSummaryStatistics** - Provides statistics that could be looked at to evaluate the quality of data
* **QualityChecking** - Provides a measure of the quality of the reads
* **QualityFiltering** - Removes low quality reads based on a specified quality threshold
* **Metagenomics** - Is used for studying genetic material recovered directly from environmental samples
* **Simulators** - Simulates a sequencing process and produce <i>in-silico</i> reads
* **Demultiplexing** - Uses barcode or other information to know which sequences came from which samples in a pool of samples
* **Normalisation** - Removes unwanted variation that may affect results
* **QualityTrimming** - Removes low-quality reads
* **ReadQuantification** - Quantifies of expression from reads
* **SuitableForSingleCellExperiments** - Can be used for analysing/processing single-cell data generated by long read sequencing platforms
* **TestedOnHumanData** - Provides evidence in publications to have been successfully employed to analyse human data
* **TestedOnNonHumanData** - Provides evidence in publications to have been successfully employed to analyse non-human data
* **SNPAndVariantAnalysis** - Detects or uses variants
* **Visualisation** - Visualises some aspect of long read data or analysis

## Contributors

Thank you to everyone who has contributed to long-read-tools! Your efforts to build
and improve this resource for the community are greatly appreciated!

The following people have made significant contributions to the long-read-tools
database or website:

* [@_lazappi_](https://github.com/lazappi) - scRNA-tools source (https://github.com/Oshlack/scRNA-tools) that was re-used for this repository
* [@QGouil](https://github.com/QGouil) - Adds new tools and updates existing entries 
* [@mritchieau](https://github.com/mritchie) - Concept of the database and 
suggests new tools
* [@scottgigante](https://github.com/scottgigante) - Modified plotting code
* [@Lexisomes](https://github.com/alexiswl) - Switch to preferred
  resolver for date to character format
