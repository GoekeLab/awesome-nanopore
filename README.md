# awesome-nanopore

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

List of software packages for Nanopore sequencing data analysis, including basecalling, DNA/RNA modifications, etc. [Contributions welcome](https://github.com/goekelab/awesome-nanopore#contributing)...

## Software packages

### Basecalling

- [Dorado](https://github.com/nanoporetech/dorado) - [C++] - Production basecaller from 2022, successor to Guppy.
- [Nanocall](https://github.com/mateidavid/nanocall) - [C++] - [Nanocall: an open source basecaller for Oxford Nanopore sequencing data](https://academic.oup.com/bioinformatics/article/33/1/49/2525680)
- [PoreSeq](https://github.com/tszalay/poreseq) - [C++] - [De novo sequencing and variant calling with nanopores using PoreSeq](https://www.nature.com/articles/nbt.3360)
- [Nanonet](https://github.com/ProgramFiles/nanonet) - [C++] - [Nanonet - Development version of RNN basecaller](https://github.com/ProgramFiles/nanonet)
- [DeepNano](https://github.com/jeammimi/deepnano) - [Python] - [DeepNano: Deep recurrent neural networks for base calling in MinION nanopore reads](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0178751)
- BasecRAWller - [Close sourced (May request code by emailing IPO@lbl.gov)] - [BasecRAWller: Streaming Nanopore Basecalling Directly from Raw Signal](https://www.biorxiv.org/content/10.1101/133058v1)
- [Chiron](https://github.com/haotianteng/Chiron) - [Python] - [Chiron: translating nanopore raw signal directly into nucleotide sequence using deep learning](https://academic.oup.com/gigascience/article/7/5/giy037/4966989)
- [Causalcall](https://github.com/scutbioinformatic/causalcall) - [Python] - [Causalcall: Nanopore Basecalling Using a Temporal Convolutional Network](https://www.frontiersin.org/articles/10.3389/fgene.2019.01332/full)
- [Bonito](https://github.com/nanoporetech/bonito) - [Python] - A PyTorch Basecaller for Oxford Nanopore Reads (research, not production basecaller)

### Adaptive sampling / ReadUntil Real-time mapping / signal mapping

- [Readfish](https://github.com/LooseLab/readfish) - [Python] - [Readfish enables targeted nanopore sequencing of gigabase-sized genomes](https://www.nature.com/articles/s41587-020-00746-x)
- [UNCALLED](https://github.com/skovaka/UNCALLED) - [C++] - [Targeted nanopore sequencing by real-time mapping of raw electrical signal with UNCALLED](https://www.nature.com/articles/s41587-020-0731-9)
- [SquiggleNet](https://github.com/welch-lab/SquiggleNet) - [Python] - [Real-Time, Direct Classification of Nanopore Signals with SquiggleNet](https://www.biorxiv.org/content/10.1101/2021.01.15.426907v2)
- [Sigmap](https://github.com/haowenz/sigmap) - [C/C++] - [Real-time mapping of nanopore raw signals 
](https://academic.oup.com/bioinformatics/article/37/Supplement_1/i477/6319675)
- [cwDTW](https://github.com/realbigws/cwDTW) - [C/C++] - [An accurate and rapid continuous wavelet dynamic time warping algorithm for end-to-end mapping in ultra-long nanopore sequencing](https://academic.oup.com/bioinformatics/article/34/17/i722/5093233)
- [OpenDBA](https://github.com/nodrogluap/OpenDBA) - [C++/CUDA] - [GPU-accelerated Dynamic Time Warp (DTW) Barycenter Averaging](https://github.com/nodrogluap/OpenDBA#how-do-i-use-this-for-oxford-nanopore-data)
- [Magenta & Maxwell](https://github.com/nodrogluap/maxwell) - [C++/CUDA] - [Fast signal-level matching for direct RNA nanopore sequencing](https://github.com/nodrogluap/maxwell)

### Segmentation

- [tombo resquiggle](https://nanoporetech.github.io/tombo/resquiggle.html) - [Python] - [Re-squiggle Algorithm](https://nanoporetech.github.io/tombo/resquiggle.html).
- [nanopolish eventalign](https://github.com/jts/nanopolish) - [C++] - [Detecting DNA cytosine methylation using nanopore sequencing](https://www.nature.com/articles/nmeth.4184).
- [f5c eventalign](https://github.com/hasindu2008/f5c) - [C/C++/CUDA] - [GPU accelerated adaptive banded event alignment for rapid comparative nanopore signal analysis](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-020-03697-x)
- [SquiggleKit Segmenter/MotifSeq](https://github.com/Psy-Fer/SquiggleKit) - [Python] - [SquiggleKit: a toolkit for manipulating nanopore signal data](https://academic.oup.com/bioinformatics/article/35/24/5372/5537108)

### DNA modification analysis

- [Megalodon](https://github.com/nanoporetech/megalodon) - [C++] - Research modified base caller which uses rerio, remora and a genome.
- [modbam2bed](https://github.com/epi2me-labs/modbam2bed) - [C++] - Convert modified base calls from megalodon etc to bedMethyl format
- [nanopolish call-methylation](https://github.com/jts/nanopolish) - [C++] - [Detecting DNA cytosine methylation using nanopore sequencing](https://www.nature.com/articles/nmeth.4184).
- [f5c call-methylation](https://github.com/hasindu2008/f5c) - [C/C++/CUDA] - [GPU accelerated adaptive banded event alignment for rapid comparative nanopore signal analysis](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-020-03697-x)
- [nanoNOMe](https://github.com/timplab/nanoNOMe) - [Python] - [Simultaneous profiling of chromatin accessibility and methylation on human cell lines with nanopore sequencing](https://www.nature.com/articles/s41592-020-01000-7).
- [signalAlign](https://github.com/ArtRand/signalAlign) - [C] - [Mapping DNA methylation with high-throughput nanopore sequencing](https://www.nature.com/articles/nmeth.4189).
- [mCaller](https://github.com/al-mcintyre/mCaller) - [Python] - [Single-molecule sequencing detection of N6-methyladenine in microbial reference materials](https://www.nature.com/articles/s41467-019-08289-9).
- [DeepSignals](https://github.com/bioinfomaticsCSU/deepsignal) - [Python] - [DeepSignal: detecting DNA methylation state from Nanopore sequencing reads using deep-learning](https://academic.oup.com/bioinformatics/article/35/22/4586/5474907).
- [tombo detect_modifications](https://nanoporetech.github.io/tombo/modified_base_detection.html) - [Python] - [(previously nanoraw)De novo Identification of DNA Modifications Enabled by Genome-Guided Nanopore Signal Processing](https://www.biorxiv.org/content/10.1101/094672v2).
- [NanoMod](https://github.com/WGLab/NanoMod) - [Python] - [NanoMod: a computational tool to detect DNA modifications using Nanopore long-read sequencing data](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-018-5372-8).

### RNA modification analysis

- [tombo detect_modifications](https://nanoporetech.github.io/tombo/modified_base_detection.html) - [Python] - [Modified Base Detection](https://nanoporetech.github.io/tombo/modified_base_detection.html).
- [MINES](https://github.com/YeoLab/MINES) - [Python] - [Direct RNA sequencing enables m6A detection in endogenous transcript isoforms at base specific resolution](https://rnajournal.cshlp.org/content/early/2019/10/17/rna.072785.119).
- [EpiNano](https://github.com/enovoa/EpiNano) - [Python] - [Accurate detection of m6A RNA modifications in native RNA sequences](https://www.nature.com/articles/s41467-019-11713-9).
- [Nanom6A](https://github.com/gaoyubang/nanom6A) - [Python] - [Quantitative profiling of N6-methyladenosine at single-base resolution in stem-differentiating xylem of Populus trichocarpa using Nanopore direct RNA sequencing](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-02241-7).
- [m6anet](https://github.com/GoekeLab/m6anet) - [Python] - [Detection of m6A from direct RNA-Seq data](http://doi.org/10.5281/zenodo.4692776).
- [nano-ID](https://github.com/birdumbrella/nano-ID) - [R] - [Native molecule sequencing by nano-ID reveals synthesis and stability of RNA isoforms](https://genome.cshlp.org/content/30/9/1332.full).
- [nanoRMS](https://github.com/novoalab/nanoRMS) - [Python] - [Quantitative profiling of pseudouridylation dynamics in native RNAs with nanopore sequencing](https://www.nature.com/articles/s41587-021-00915-6?proof=t%3B).
- [Yanocomp](https://github.com/bartongroup/yanocomp) - [Python] - [Yanocomp: robust prediction of m6A modifications in individual nanopore direct RNA reads](https://www.biorxiv.org/content/10.1101/2021.06.15.448494v1).
- [DiffErr](https://github.com/bartongroup/differr_nanopore_DRS) - [Python] - A tool for detecting modifications from Nanopore DRS errors using a low modification control.
- [ELIGOS](https://gitlab.com/piroonj/eligos2) - [Python] - [Decoding the epitranscriptional landscape from native RNA sequences](https://academic.oup.com/nar/article/49/2/e7/5876284).
- [nanoDoc](https://github.com/uedaLabR/nanoDoc) - [Python] - [nanoDoc: RNA modification detection using Nanopore raw reads with Deep One-Class Classification](https://www.biorxiv.org/content/10.1101/2020.09.13.295089v1).
- [nanocompore](https://github.com/tleonardi/nanocompore) - [Python] - [RNA modifications detection by comparative Nanopore direct RNA sequencing](https://www.biorxiv.org/content/10.1101/843136v1).
- [DRUMMER](https://github.com/DepledgeLab/DRUMMER) - [Python] - [Direct RNA sequencing reveals m6A modifications on adenovirus RNA are necessary for efficient splicing](https://www.nature.com/articles/s41467-020-19787-6.pdf?origin=ppub).
- [xPore](https://github.com/GoekeLab/xpore) - [Python] - [Identification of differential RNA modifications from nanopore direct RNA sequencing with xPore](https://doi.org/10.1038/s41587-021-00949-w).

### RNA structure prediction

- [nanoSHAPE](https://github.com/physnano/rRNA_nanoSHAPE) - [Python] - [Direct detection of RNA modifications and structure using single molecule nanopore sequencing](https://www.biiorxiv.org/content/10.1101/2020.05.31.126763v1).
- [PORE-cupine](https://github.com/awjga/PORE-cupine) - [R] - [Determination of isoform-specific RNA structure with nanopore long reads](https://www.nature.com/articles/s41587-020-0712-z).

### Poly(A) tail length estimation

- [nanopolish polya](https://github.com/jts/nanopolish) - [C++] - [Nanopore native RNA sequencing of a human poly(A) transcriptome](https://www.nature.com/articles/s41592-019-0617-2?proof=t).
- [tailfindr](https://github.com/adnaniazi/tailfindr) - [R] - [tailfindr: Alignment-free poly(A) length measurement for Oxford Nanopore RNA and DNA sequencing](https://rnajournal.cshlp.org/content/early/2019/07/02/rna.071332.119).

### Transcript discovery and quantification

- [bambu](https://github.com/GoekeLab/bambu) - [R] - [Reference-guided isoform reconstruction and quantification for long read RNA-Seq data](http://www.bioconductor.org/packages/release/bioc/html/bambu.html)
- [NanoSplicer](https://github.com/shimlab/NanoSplicer) - [Python] - [Identification of splice junctions from nanopore sequencing using raw signal squiggles](https://academic.oup.com/bioinformatics/article/38/15/3741/6594111)
- [TALON](https://github.com/mortazavilab/TALON) - [Python] - [Python package for identifying and quantifying known and novel genes/isoforms in long-read transcriptome data sets](https://www.biorxiv.org/content/10.1101/672931v2) **Run before** [TranscriptClean](https://github.com/mortazavilab/TranscriptClean)

### Raw signal data manipulation, conversion, visualisation, etc.

- [slow5lib](https://github.com/hasindu2008/slow5lib) - [C] - [Fast nanopore sequencing data analysis with SLOW5
](https://www.nature.com/articles/s41587-021-01147-4)
- [pyslow5](https://pypi.org/project/pyslow5/) - [Python] - [pyslow5 python library
](https://hasindu2008.github.io/slow5lib/pyslow5_api/pyslow5.html)
- [slow5tools](https://github.com/hasindu2008/slow5tools) - [C/C++] - [Toolkit for converting (FAST5 <-> SLOW5), compressing, viewing, indexing and manipulating data in SLOW5 format](https://hasindu2008.github.io/slow5tools/)
- [SquiggleKit SquigglePlot](https://github.com/Psy-Fer/SquiggleKit) - [Python] - [SquiggleKit: a toolkit for manipulating nanopore signal data](https://academic.oup.com/bioinformatics/article/35/24/5372/5537108)

## Genome Assembly
- [Flye](https://github.com/fenderglass/Flye) - [C++] - Single molecule sequence assembler with good polishing capabilities
- [Shasta](https://github.com/chanzuckerberg/shasta) - [C] - Very fast and capable nanopore assembler 

## Metagenomics
- [nf-Wochenende](https://github.com/MHH-RCUG/nf_wochenende) - [Nextflow, Python] - [Wochenende - modular and flexible alignment-based shotgun metagenome analysis](https://www.biorxiv.org/content/10.1101/2022.03.18.484377v3)

### Single-cell analysis

- [BLAZE](https://github.com/shimlab/BLAZE) - [Python] - [Identification of cell barcodes from long-read single-cell RNA-seq with BLAZE](https://www.biorxiv.org/content/10.1101/2022.08.16.504056v1)

## Pipelines

- [MOP2](https://github.com/biocorecrg/MOP2) - [Nextflow] - [MasterOfPores: A Workflow for the Analysis of Oxford Nanopore Direct RNA Sequencing Datasets](https://www.frontiersin.org/articles/10.3389/fgene.2020.00211/full)


## Contributing
We welcome contributions and suggestions! Please follow the steps below to contribute:
1. Fork this repository
2. Make a change to README.md in this format: `[RESOURCE](LINK)` - [language(s)] - DESCRIPTION
3. Submit a pull request.

## Citation
Wan, Y.K., Hendra, C., Pratanwanich, P.N. & Göke, J. Beyond sequencing: machine learning algorithms extract biology hidden in Nanopore signal data. *Trends in Genetics* (2021). https://doi.org/10.1016/j.tig.2021.09.001.

## What is an awesome list?
According to [the official awesome Github repository](https://github.com/sindresorhus/awesome), an awesome list on GitHub is "a curation of actual awesome stuff", so an awesome list only includes items that has been reseached on by a contributor who would personally recommend the items. To learn more, please read [the official awesome manifesto](https://github.com/sindresorhus/awesome/blob/main/awesome.md).

## Contact
This repository was created by [Yuk Kei Wan](https://github.com/yuukiiwa).
