# awesome-nanopore

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

List of software packages for Nanopore sequencing data analysis, including basecalling, DNA/RNA modifications, etc. [Contributions welcome](https://github.com/goekelab/awesome-nanopore#contributing)...

## Table of contents

- [Software packages](#software-packages)
  - [Basecalling](#basecalling)
  - [QC, preprocessing](#qc-preprocessing)
  - [Alignment](#alignment)
  - [Signal analysis](#signal-analysis)
    - [Adaptive sampling / ReadUntil / signal mapping](#adaptive-sampling--readuntil-real-time-mapping--signal-mapping)
    - [Segmentation](#segmentation)
    - [Raw signal data manipulation](#raw-signal-data-manipulation-conversion-visualisation-etc)
  - [Variant, SV calling, Phasing](#variant-sv-calling-phasing)
  - [Modification analysis](#modification-analysis)
    - [DNA modification analysis](#dna-modification-analysis)
    - [RNA modification analysis](#rna-modification-analysis)
  - [Assembly](#assembly)
    - [Genome Assembly](#genome-assembly)
    - [Polishing, Error correction](#polishing-error-correction)
  - [Transcriptomics](#transcriptomics)
    - [Transcript discovery and quantification](#transcript-discovery-and-quantification)
    - [Poly(A) tail length estimation](#polya-tail-length-estimation)
    - [RNA structure prediction](#rna-structure-prediction)
    - [Single-cell analysis](#single-cell-analysis)
  - [Simulation](#simulation)
    - [Reads simulation](#reads-simulation)
    - [Coverage simulation](#coverage-simulation)
- [Pipelines](#pipelines)
  - [Metagenomics](#metagenomics)
- [Deprecated / superseded](#deprecated--superseded)
- [Contributing](#contributing)
- [Citation](#citation)
- [What is an awesome list?](#what-is-an-awesome-list)
- [Contact](#contact)

## Software packages

### Basecalling

#### ONT basecallers

- [Dorado](https://github.com/nanoporetech/dorado) - [C++] - Production basecaller from 2022, successor to Guppy.
- [Bonito](https://github.com/nanoporetech/bonito) - [Python] - A PyTorch Basecaller for Oxford Nanopore Reads (research, not production basecaller)

#### Research Basecallers (2016 - 2021)

- [Nanocall](https://github.com/mateidavid/nanocall) - [C++] - [Nanocall: an open source basecaller for Oxford Nanopore sequencing data](https://academic.oup.com/bioinformatics/article/33/1/49/2525680)
- [PoreSeq](https://github.com/tszalay/poreseq) - [C++] - [De novo sequencing and variant calling with nanopores using PoreSeq](https://www.nature.com/articles/nbt.3360)
- [Nanonet](https://github.com/ProgramFiles/nanonet) - [C++] - [Nanonet - Development version of RNN basecaller](https://github.com/ProgramFiles/nanonet)
- [DeepNano](https://github.com/jeammimi/deepnano) - [Python] - [DeepNano: Deep recurrent neural networks for base calling in MinION nanopore reads](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0178751)
- BasecRAWller - [Close sourced (May request code by emailing IPO@lbl.gov)] - [BasecRAWller: Streaming Nanopore Basecalling Directly from Raw Signal](https://www.biorxiv.org/content/10.1101/133058v1)
- [Chiron](https://github.com/haotianteng/Chiron) - [Python] - [Chiron: translating nanopore raw signal directly into nucleotide sequence using deep learning](https://academic.oup.com/gigascience/article/7/5/giy037/4966989)
- [Causalcall](https://github.com/scutbioinformatic/causalcall) - [Python] - [Causalcall: Nanopore Basecalling Using a Temporal Convolutional Network](https://www.frontiersin.org/articles/10.3389/fgene.2019.01332/full)

### QC, preprocessing

- [NanoPlot](https://github.com/wdecoster/nanoplot) - [HTML/Python] - [QC plotting tool for Nanopore reads](https://academic.oup.com/bioinformatics/article/39/5/btad311/7160911?login=false)
- [Cramino](https://github.com/wdecoster/cramino) - [Rust] - A tool for quick quality assessment of cram and bam files, intended for long read sequencing

### Alignment

- [minimap2](https://github.com/lh3/minimap2) - [C] - [Minimap2: pairwise alignment for nucleotide sequences](https://academic.oup.com/bioinformatics/article/34/18/3094/4994778)
- [Winnowmap](https://github.com/marbl/winnowmap) - [C] - [Weighted minimizer sampling improves long read mapping](https://academic.oup.com/bioinformatics/article/36/Supplement_1/i111/5870473)
- [NGMLR](https://github.com/philres/ngmlr) - [C++] - [long-read mapper designed to align PacBio or Oxford Nanopore reads to a reference genome with a focus on reads that span structural variations](https://www.nature.com/articles/s41592-018-0001-7)

### Signal analysis

#### Adaptive sampling / ReadUntil Real-time mapping / signal mapping

- [Readfish](https://github.com/LooseLab/readfish) - [Python] - [Readfish enables targeted nanopore sequencing of gigabase-sized genomes](https://www.nature.com/articles/s41587-020-00746-x)
- [UNCALLED](https://github.com/skovaka/UNCALLED) - [C++] - [Targeted nanopore sequencing by real-time mapping of raw electrical signal with UNCALLED](https://www.nature.com/articles/s41587-020-0731-9)
- [SquiggleNet](https://github.com/welch-lab/SquiggleNet) - [Python] - [Real-Time, Direct Classification of Nanopore Signals with SquiggleNet](https://www.biorxiv.org/content/10.1101/2021.01.15.426907v2)
- [Sigmap](https://github.com/haowenz/sigmap) - [C/C++] - [Real-time mapping of nanopore raw signals](https://academic.oup.com/bioinformatics/article/37/Supplement_1/i477/6319675)
- [cwDTW](https://github.com/realbigws/cwDTW) - [C/C++] - [An accurate and rapid continuous wavelet dynamic time warping algorithm for end-to-end mapping in ultra-long nanopore sequencing](https://academic.oup.com/bioinformatics/article/34/17/i722/5093233)
- [OpenDBA](https://github.com/nodrogluap/OpenDBA) - [C++/CUDA] - [GPU-accelerated Dynamic Time Warp (DTW) Barycenter Averaging](https://github.com/nodrogluap/OpenDBA#how-do-i-use-this-for-oxford-nanopore-data)
- [Magenta & Maxwell](https://github.com/nodrogluap/maxwell) - [C++/CUDA] - [Fast signal-level matching for direct RNA nanopore sequencing](https://github.com/nodrogluap/maxwell)

#### Segmentation

- [nanopolish eventalign](https://github.com/jts/nanopolish) - [C++] - [Detecting DNA cytosine methylation using nanopore sequencing](https://www.nature.com/articles/nmeth.4184).
- [f5c eventalign](https://github.com/hasindu2008/f5c) - [C/C++/CUDA] - [GPU accelerated adaptive banded event alignment for rapid comparative nanopore signal analysis](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-020-03697-x)
- [f5c resquiggle](https://github.com/hasindu2008/f5c) - [C/C++/CUDA] - [GPU accelerated adaptive banded event alignment for rapid comparative nanopore signal analysis](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-020-03697-x)
- [SquiggleKit Segmenter/MotifSeq](https://github.com/Psy-Fer/SquiggleKit) - [Python] - [SquiggleKit: a toolkit for manipulating nanopore signal data](https://academic.oup.com/bioinformatics/article/35/24/5372/5537108)
- [Dynamont](https://github.com/rnajena/dynamont) - [Python/C++] - A Dynamic Programming Approach to Segment ONT Signals
- [Uncalled4](https://github.com/skovaka/uncalled4) - [Python/C++] - [Uncalled4 improves nanopore DNA and RNA modification detection via fast and accurate signal alignment](https://doi.org/10.1101/2024.03.05.583511)

#### Raw signal data manipulation, conversion, visualisation, etc.

- [slow5lib](https://github.com/hasindu2008/slow5lib) - [C] - [Fast nanopore sequencing data analysis with SLOW5
](https://www.nature.com/articles/s41587-021-01147-4)
- [pyslow5](https://pypi.org/project/pyslow5/) - [Python] - [pyslow5 python library
](https://hasindu2008.github.io/slow5lib/pyslow5_api/pyslow5.html)
- [slow5tools](https://github.com/hasindu2008/slow5tools) - [C/C++] - [Toolkit for converting (FAST5 <-> SLOW5), compressing, viewing, indexing and manipulating data in SLOW5 format](https://hasindu2008.github.io/slow5tools/)
- [SquiggleKit SquigglePlot](https://github.com/Psy-Fer/SquiggleKit) - [Python] - [SquiggleKit: a toolkit for manipulating nanopore signal data](https://academic.oup.com/bioinformatics/article/35/24/5372/5537108)
- [Squigualiser](https://github.com/hiruna72/squigualiser) - [Python] - [Interactive visualization of nanopore sequencing signal data with Squigualiser](doi.org/10.1093/bioinformatics/btae501)

### Variant, SV calling, Phasing

- [Clair3](https://github.com/HKU-BAL/Clair3) - [Python/C++] - [Clair3-RNA: a deep learning-based small variant caller for long-read RNA sequencing data](https://www.nature.com/articles/s41467-025-67237-y)
- [Sniffles](https://github.com/fritzsedlazeck/sniffles) - [Python] - [Detection of mosaic and population-level structural variants with Sniffles2](https://www.nature.com/articles/s41587-023-02024-y)
- [whatshap](https://github.com/whatshap/whatshap) - [Python/C++] - [Read-Based Phasing and Analysis of Phased Variants with WhatsHap](https://link.springer.com/protocol/10.1007/978-1-0716-2819-5_8)
- [LongPhase](https://github.com/twolinin/longphase) - [C] - [ an ultra-fast program for simultaneously co-phasing SNPs, small indels, large SVs, and (5mC) modifications for Nanopore and PacBio platforms](https://academic.oup.com/bioinformatics/article/38/7/1816/6519151)

### Modification analysis

#### DNA modification analysis

- [modkit](https://github.com/nanoporetech/modkit) - [Rust] - Extract modified base calls from dorado BAM output to bedMethyl format, also calculate DMRs
- [nanopolish call-methylation](https://github.com/jts/nanopolish) - [C++] - [Detecting DNA cytosine methylation using nanopore sequencing](https://www.nature.com/articles/nmeth.4184).
- [f5c call-methylation](https://github.com/hasindu2008/f5c) - [C/C++/CUDA] - [GPU accelerated adaptive banded event alignment for rapid comparative nanopore signal analysis](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-020-03697-x)
- [nanoNOMe](https://github.com/timplab/nanoNOMe) - [Python] - [Simultaneous profiling of chromatin accessibility and methylation on human cell lines with nanopore sequencing](https://www.nature.com/articles/s41592-020-01000-7).
- [signalAlign](https://github.com/ArtRand/signalAlign) - [C] - [Mapping DNA methylation with high-throughput nanopore sequencing](https://www.nature.com/articles/nmeth.4189).
- [mCaller](https://github.com/al-mcintyre/mCaller) - [Python] - [Single-molecule sequencing detection of N6-methyladenine in microbial reference materials](https://www.nature.com/articles/s41467-019-08289-9).
- [DeepSignals](https://github.com/bioinfomaticsCSU/deepsignal) - [Python] - [DeepSignal: detecting DNA methylation state from Nanopore sequencing reads using deep-learning](https://academic.oup.com/bioinformatics/article/35/22/4586/5474907).
- [NanoMod](https://github.com/WGLab/NanoMod) - [Python] - [NanoMod: a computational tool to detect DNA modifications using Nanopore long-read sequencing data](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-018-5372-8).
- [MethQC](https://github.com/JMencius/methqc) - [Python] - Quality control for DNA methylation detection in long-read sequencing

#### RNA modification analysis

##### RNA004 Chemistry Compatible Tools

- [Dorado](https://github.com/nanoporetech/dorado) - [C++] - [Supports calling 8 different RNA modifications: inosine, m6A, 2′OmeA on A; pseU, 2′OmeU on U; m5C, 2′OmeC on C; and 2′OmeG on G as of May 2025](https://software-docs.nanoporetech.com/dorado/1.4.0/models/list/)
- [SingleMod](https://github.com/xieyy46/SingleMod-v1) - [Python] - [Single-molecule direct RNA sequencing reveals the shaping of epitranscriptome across multiple species](https://www.nature.com/articles/s41467-025-60447-4)
- [m6anet](https://github.com/GoekeLab/m6anet) - [Python] - [Detection of m6A from direct RNA sequencing using a multiple instance learning framework](https://www.nature.com/articles/s41592-022-01666-1).
- [MoDorado](https://github.com/KleistLab/MoDorado) - [Python] - [MoDorado: enhanced detection of tRNA modifications in nanopore sequencing by off-label use of modification callers](https://academic.oup.com/nar/article/53/15/gkaf795/8237893)

##### RNA002 Chemistry Compatible Tools

- [MINES](https://github.com/YeoLab/MINES) - [Python] - [Direct RNA sequencing enables m6A detection in endogenous transcript isoforms at base specific resolution](https://rnajournal.cshlp.org/content/early/2019/10/17/rna.072785.119).
- [EpiNano](https://github.com/novoalab/EpiNano) - [Python] - [Accurate detection of m6A RNA modifications in native RNA sequences](https://www.nature.com/articles/s41467-019-11713-9).
- [Nanom6A](https://github.com/gaoyubang/nanom6A) - [Python] - [Quantitative profiling of N6-methyladenosine at single-base resolution in stem-differentiating xylem of Populus trichocarpa using Nanopore direct RNA sequencing](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-02241-7).
- [NanoNm](https://github.com/kaifuchenlab/NanoNm) - [Python] - [A Machine Learning Method to detect the 2'-O-methylation(Nm) in Nanopore direct RNA-seq](https://doi.org/10.1016/j.molcel.2024.04.011)
- [m6anet](https://github.com/GoekeLab/m6anet) - [Python] - [Detection of m6A from direct RNA sequencing using a multiple instance learning framework](https://www.nature.com/articles/s41592-022-01666-1).
- [nanoRMS](https://github.com/novoalab/nanoRMS) - [Python] - [Quantitative profiling of pseudouridylation dynamics in native RNAs with nanopore sequencing](https://www.nature.com/articles/s41587-021-00915-6?proof=t%3B).
- [Yanocomp](https://github.com/bartongroup/yanocomp) - [Python] - [Yanocomp: robust prediction of m6A modifications in individual nanopore direct RNA reads](https://www.biorxiv.org/content/10.1101/2021.06.15.448494v1).
- [DiffErr](https://github.com/bartongroup/differr_nanopore_DRS) - [Python] - A tool for detecting modifications from Nanopore DRS errors using a low modification control.
- [ELIGOS](https://gitlab.com/piroonj/eligos2) - [Python] - [Decoding the epitranscriptional landscape from native RNA sequences](https://academic.oup.com/nar/article/49/2/e7/5876284).
- [nanoDoc](https://github.com/uedaLabR/nanoDoc) - [Python] - [nanoDoc: RNA modification detection using Nanopore raw reads with Deep One-Class Classification](https://www.biorxiv.org/content/10.1101/2020.09.13.295089v1).
- [nanocompore](https://github.com/tleonardi/nanocompore) - [Python] - [RNA modifications detection by comparative Nanopore direct RNA sequencing](https://www.nature.com/articles/s41467-021-27393-3).
- [DRUMMER](https://github.com/DepledgeLab/DRUMMER) - [Python] - [DRUMMER—rapid detection of RNA modifications through comparative nanopore sequencing](https://academic.oup.com/bioinformatics/article/38/11/3113/6569078).
- [xPore](https://github.com/GoekeLab/xpore) - [Python] - [Identification of differential RNA modifications from nanopore direct RNA sequencing with xPore](https://doi.org/10.1038/s41587-021-00949-w).
- [Magnipore](https://github.com/rnajena/magnipore) - [Python] - [Magnipore: Prediction of differential single nucleotide changes in the Oxford Nanopore Technologies sequencing signal of SARS-CoV-2 samples](https://doi.org/10.1101/2023.03.17.533105)
- [DENA](https://github.com/weir12/DENA) - [Python/R] - [DENA: training an authentic neural network model using Nanopore sequencing data of Arabidopsis transcripts for detection and quantification of N6-methyladenosine on RNA](https://doi.org/10.1186/s13059-021-02598-3)
- [Penguin](https://github.com/Janga-Lab/Penguin) - [Python] - [Penguin: A Tool for Predicting Pseudouridine Sites in Direct RNA Nanopore Sequencing Data](https://doi.org/10.1016/j.ymeth.2022.02.005)
- [TandemMod](https://github.com/yulab2021/TandemMod) - [Python] - [Transfer learning enables identification of multiple types of RNA modifications using nanopore direct RNA sequencing](https://www.nature.com/articles/s41467-024-48437-4)

### Assembly

#### Genome Assembly

- [Verkko](https://github.com/marbl/verkko) - [Python] - hybrid genome assembly pipeline developed for telomere-to-telomere assembly of accurate long reads (PacBio HiFi, Oxford Nanopore Duplex, HERRO or Hifiasm corrected Oxford Nanopore Simplex) and Oxford Nanopore ultra-long reads. [Telomere-to-telomere assembly of diploid chromosomes with Verkko](https://www.nature.com/articles/s41587-023-01662-6)
- [Flye](https://github.com/fenderglass/Flye) - [C++] - Single molecule sequence assembler with good polishing capabilities
- [Shasta](https://github.com/paoloshasta/shasta) - [C] - Very fast and capable nanopore assembler
- [Autocycler](https://github.com/rrwick/Autocycler) - [Rust] - [Autocycler: long-read consensus assembly for bacterial genomes](https://academic.oup.com/bioinformatics/article/41/9/btaf474/8242761)

#### Polishing, Error correction

- [Medaka](https://github.com/nanoporetech/medaka) - [Python] - ONT's official polisher
- [Herro](https://github.com/lbcb-sci/herro) - [Rust] - [Telomere-to-Telomere Assembly Using HERRO-Corrected Simplex Nanopore Reads](https://www.nature.com/articles/s41586-026-10563-y)

### Transcriptomics

#### Transcript discovery and quantification

- [RNAbloom2](https://github.com/bcgsc/RNA-Bloom) - [Java] - [Reference-free assembly of long-read transcriptome sequencing data with RNA-Bloom2](https://www.nature.com/articles/s41467-023-38553-y)
- [RATTLE](https://github.com/comprna/RATTLE/) - [C++] - [RATTLE: reference-free reconstruction and quantification of transcriptomes from Nanopore sequencing](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-022-02715-w)
- [bambu](https://github.com/GoekeLab/bambu) - [R] - [Context-Aware Transcript Quantification from Long Read RNA-Seq data with Bambu](https://rdcu.be/deluQ)
- [IsoQuant](https://github.com/ablab/IsoQuant) - [Python] - [Accurate isoform discovery with IsoQuant using long reads](https://www.nature.com/articles/s41587-022-01565-y)
- [NanoSplicer](https://github.com/shimlab/NanoSplicer) - [Python] - [Identification of splice junctions from nanopore sequencing using raw signal squiggles](https://academic.oup.com/bioinformatics/article/38/15/3741/6594111)
- [TALON](https://github.com/mortazavilab/TALON) - [Python] - [Python package for identifying and quantifying known and novel genes/isoforms in long-read transcriptome data sets](https://www.biorxiv.org/content/10.1101/672931v2) **Run before** [TranscriptClean](https://github.com/mortazavilab/TranscriptClean)
- [trackcluster](https://github.com/runsheng/trackcluster) -[Python] - [trackcluster is an isoform calling and quantification pipeline for long RNA/cDNA reads](https://genome.cshlp.org/content/30/2/287.short)
- [FLAIR](https://github.com/BrooksLabUCSC/FLAIR) - [Python] - [Full-Length Alternative Isoform analysis of RNA](https://www.nature.com/articles/s41467-020-15171-6)

#### Poly(A) tail length estimation

- [nanopolish polya](https://github.com/jts/nanopolish) - [C++] - [Nanopore native RNA sequencing of a human poly(A) transcriptome](https://www.nature.com/articles/s41592-019-0617-2?proof=t).
- [tailfindr](https://github.com/adnaniazi/tailfindr) - [R] - [tailfindr: Alignment-free poly(A) length measurement for Oxford Nanopore RNA and DNA sequencing](https://rnajournal.cshlp.org/content/early/2019/07/02/rna.071332.119).

#### RNA structure prediction

- [nanoSHAPE](https://github.com/physnano/rRNA_nanoSHAPE) - [Python] - [Direct detection of RNA modifications and structure using single molecule nanopore sequencing](https://www.biorxiv.org/content/10.1101/2020.05.31.126763v1).
- [PORE-cupine](https://github.com/awjga/PORE-cupine) - [R] - [Determination of isoform-specific RNA structure with nanopore long reads](https://www.nature.com/articles/s41587-020-0712-z).

#### Single-cell analysis

- [BLAZE](https://github.com/shimlab/BLAZE) - [Python] - [Identification of cell barcodes from long-read single-cell RNA-seq with BLAZE](https://www.biorxiv.org/content/10.1101/2022.08.16.504056v1)

### Simulation

#### Reads simulation

- [NanoSim](https://github.com/bcgsc/NanoSim) - [Python] - [NanoSim: nanopore sequence read simulator based on statistical characterization.](https://doi.org/10.1093/gigascience/gix010), [Trans-NanoSim characterizes and simulates nanopore RNA-sequencing data.](https://academic.oup.com/gigascience/article/9/6/giaa061/5855462?login=true), [Characterization and simulation of metagenomic nanopore sequencing data with Meta-NanoSim.](https://academic.oup.com/gigascience/article/doi/10.1093/gigascience/giad013/7080817?login=true)

#### Coverage simulation

- [esloco](https://github.com/aweich/esloco) - [Python] - [esloco: simulation-based estimation of local coverage in long-read DNA sequencing](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btag009/8418384)

## Pipelines

- [MOP2](https://github.com/biocorecrg/MOP2) - [Nextflow] - [MasterOfPores: A Workflow for the Analysis of Oxford Nanopore Direct RNA Sequencing Datasets](https://www.frontiersin.org/articles/10.3389/fgene.2020.00211/full)
- [bambu-pipe](https://github.com/GoekeLab/bambu-pipe) - [Nextflow] - [Isoform-level discovery, quantification and fusion analysis from single-cell and spatial long-read RNA-seq data with Bambu-Clump](https://www.biorxiv.org/content/10.1101/2024.12.30.630828v1.full)
- [nf-core/nanoseq](https://github.com/nf-core/nanoseq) - [Nextflow] - [A systematic benchmark of Nanopore long read RNA sequencing for transcript level analysis in human cell lines](https://www.biorxiv.org/content/10.1101/2021.04.21.440736v1) (Not yet updated for ONT's latest chemistry)

### Metagenomics
- [nf-Wochenende](https://github.com/MHH-RCUG/nf_wochenende) - [Nextflow, Python] - [Wochenende - modular and flexible alignment-based shotgun metagenome analysis](https://www.biorxiv.org/content/10.1101/2022.03.18.484377v3)


## Deprecated / superseded
- [tombo resquiggle](https://nanoporetech.github.io/tombo/resquiggle.html) - [Python] - [Re-squiggle Algorithm](https://nanoporetech.github.io/tombo/resquiggle.html). (Note - deprecated by ONT 2023, only compatible with RNA002 dRNA-seq chemistry & R9.4.1 chemistry)
- [tombo detect_modifications](https://nanoporetech.github.io/tombo/modified_base_detection.html) - [Python] - [(previously nanoraw)De novo Identification of DNA Modifications Enabled by Genome-Guided Nanopore Signal Processing](https://www.biorxiv.org/content/10.1101/094672v2).
- [Megalodon](https://github.com/nanoporetech/megalodon) - [C++] - Research modified base caller which uses rerio, remora and a genome (deprecated by ONT 2023 for Dorado).
- [modbam2bed](https://github.com/epi2me-labs/modbam2bed) - [C++] - Convert modified base calls from megalodon etc to bedMethyl format (deprecated by ONT 2023 for Modkit)
- [mAFiA](https://github.com/dieterich-lab/mAFiA) - [Python] - [Detecting m6A at single-molecular resolution via direct RNA sequencing and realistic training data](https://doi.org/10.1038/s41467-024-47661-2) (Superseded by Ψ-co-mAFiA as of Jan 2025)


## Contributing
We welcome contributions and suggestions! Please follow the steps below to contribute:
1. Fork this repository
2. Make a change to README.md in this format: `[RESOURCE](LINK)` - [language(s)] - DESCRIPTION
3. Submit a pull request.

## Citation
Wan, Y.K., Hendra, C., Pratanwanich, P.N. & Göke, J. Beyond sequencing: machine learning algorithms extract biology hidden in Nanopore signal data. *Trends in Genetics* (2021). https://doi.org/10.1016/j.tig.2021.09.001.

## What is an awesome list?
According to [the official awesome Github repository](https://github.com/sindresorhus/awesome), an awesome list on GitHub is "a curation of actual awesome stuff", so an awesome list only includes items that has been researched by a contributor who would personally recommend the items. To learn more, please read [the official awesome manifesto](https://github.com/sindresorhus/awesome/blob/main/awesome.md).

## Contact
This repository is maintained by [Clare Robinson](https://github.com/ClareRobin) and was originally created by [Yuk Kei Wan](https://github.com/yuukiiwa).
