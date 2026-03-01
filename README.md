# Protein-Language-Models

Protein language models (PLMs) are rapidly reshaping computational biology. As biological sequence and structure data scale up, NLP-style modeling techniques are becoming central to protein representation learning, prediction, and design.

This repository accompanies our systematic review of PLMs and provides a **curated, model-centric knowledge base**. It summarizes historical milestones, mainstream architectures, pretraining corpora, evaluation benchmarks, and practical toolchains. In addition to cataloging resources, we discuss key open challenges in this fast-moving area.

## News

- 🌟 [2025/02] Our paper has been submitted to a [preprint server](https://arxiv.org/pdf/2502.06881).

## Quick Start

- Read the paper preprint: [arXiv:2502.06881](https://arxiv.org/pdf/2502.06881)
- Browse the curated PLM lists in **Models**, **Datasets**, and **Tools** below.
- Use this repository as a reference index when selecting models, corpora, or evaluation suites for new projects.

## Overview

The figure below summarizes the scope of the review.

![Protein-Language-Models-Overview](https://github.com/ISYSLAB-HUST/Protein-Language-Models/blob/main/figures/overview.png)

## Contents

- [News](#news)
- [Quick Start](#quick-start)
- [Overview](#overview)
- [Contents](#contents)
- [Models](#models)
  - [Non\-transformer\-based models](#non-transformer-based-models)
  - [Transformer\-based models](#transformer-based-models)
    - [Encoder\-only models](#encoder-only-models)
    - [Decoder\-only models](#decoder-only-models)
    - [Encoder\-decoder models](#encoder-decoder-models)
- [Datasets](#datasets)
  - [Pre\-training datasets](#pre-training-datasets)
    - [Sequence datasets](#sequence-datasets)
    - [Structural datasets](#structural-datasets)
  - [Benchmarks](#benchmarks)
    - [Structural benchmarks](#structural-benchmarks)
    - [Functional benchmarks](#functional-benchmarks)
    - [Other benchmarks](#other-benchmarks) 
- [Tools](#tools)
  - [Sequence tools](#sequence-tools)
  - [Structural tools](#structural-tools)
  - [Other tools](#other-tools) 

## Models

We categorize PLMs into **non-transformer-based** and **transformer-based** families. Transformer models are further split into **encoder-only**, **decoder-only**, and **encoder-decoder** paradigms.

The tables below include publication links, release dates, parameter scales, backbone types, pretraining datasets, and open-source availability. Models are listed alphabetically within each category.

### Non-transformer-based models

Model | Time | Params | Base model | Pretraining Dataset | Code
---- | ---- | ---- | ---- | ---- | ---- |
[CARP](https://www.biorxiv.org/content/10.1101/2022.05.19.492714v5)|2024.02|600K-640M|CNN|UniRef50|[√](https://github.com/microsoft/protein-sequence-models)
[MIF-ST](https://www.biorxiv.org/content/10.1101/2022.05.25.493516v3)|2023.03|3.4M|GNN|CATH|[√](https://github.com/microsoft/protein-sequence-models)
[ProSE](https://www.sciencedirect.com/science/article/pii/S2405471221002039)|2021.06|-|LSTM|UniRef90, SCOP|[√](https://github.com/tbepler/prose)
[ProtVec](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0141287)|2015.11|-|Skip-gram|UniProtKB/Swiss-Prot|×
[ProtVecX](https://www.nature.com/articles/s41598-019-38746-w)|2019.03|-|ProtVec|UniRef50, UniProtKB/Swiss-Prot|×
[SeqVec](https://link.springer.com/article/10.1186/s12859-019-3220-8)|2019.12|-|ELMo|UniRef50|[√](https://github.com/mheinzinger/SeqVec)
[Seq2vec](https://www.sciencedirect.com/science/article/pii/S1567422320300806?via%3Dihub)|2020.09|-|CNN-LSTM|-|×
[UDSMProt](https://academic.oup.com/bioinformatics/article/36/8/2401/5698270)|2020.01|-|AWD-LSTM|UniProtKB/Swiss-Prot|×
[UniRep](https://www.nature.com/articles/s41592-019-0598-1)|2019.10|-|mLSTM|UniRef50|[√](https://github.com/churchlab/UniRep)


### Transformer-based models

#### Encoder-only models

Model           | Time    | Params        | Pretraining Dataset         | Code
----------------|---------|---------------|-----------------------------|-------------------------------
[AbLang](https://academic.oup.com/bioinformaticsadvances/article/2/1/vbac046/6609807)          | 2022.06 | -             | OAS                         | [√](https://github.com/oxpig/AbLang)
[AbLang2](https://academic.oup.com/bioinformatics/article/40/11/btae618/7845256)         | 2024.02 | -             | OAS                         | [√](https://github.com/oxpig/AbLang2.git)
[AMPLIFY](https://www.biorxiv.org/content/10.1101/2024.09.23.614603v1.abstract)         | 2024.09 | 120M/350M     | UniRef50, UniRef100, OAS, SCOP | [√](https://github.com/chandar-lab/AMPLIFY)
[AminoBert](https://www.nature.com/articles/s41587-022-01432-w)       | 2022.10 | -             | UniRef90, PDB, MGnify       | ×
[AntiBERTa](https://www.cell.com/patterns/fulltext/S2666-3899(22)00105-2)       | 2022.07 | 86M           | OAS                         | [√](https://github.com/alchemab/antiberta)
[AntiBERTy](https://arxiv.org/abs/2112.07782)       | 2021.12 | 26M           | OAS                         | [√](https://pypi.org/project/antiberty/)
[BALM](https://academic.oup.com/bib/article/25/4/bbae245/7682462)            | 2024.05 | -             | OAS                         | [√](https://github.com/BEAM-Labs/BALM)
[DistilProtBert](https://academic.oup.com/bioinformatics/article/38/Supplement_2/ii95/6701995)  | 2022.09 | 230M          | UniRef50                    | [√](https://github.com/yarongef/DistilProtBert)
[ESM-1b](https://www.pnas.org/doi/abs/10.1073/pnas.2016239118)          | 2020.02 | 650M          | UniRef50                    | [√](https://github.com/facebookresearch/esm)
[ESM-1v](https://proceedings.neurips.cc/paper/2021/hash/f51338d736f95dd42427296047067694-Abstract.html)          | 2021.02 | 650M          | UniRef90                    | [√](https://github.com/facebookresearch/esm)
[ESM-2](https://www.science.org/doi/abs/10.1126/science.ade2574)           | 2023.03 | 8M-15B        | UniRef50                    | [√](https://github.com/facebookresearch/esm)
[ESM-3](https://www.biorxiv.org/content/10.1101/2024.07.01.600583v1)           | 2024.07 | 98B           | UniRef, MGnify, AlphaFoldDB, ESMAtlas | [√](https://github.com/evolutionaryscale/esm)
[ESM All-Atom](https://openreview.net/forum?id=283cGgWfM2)    | 2024.05 | 35M           | AlphaFoldDB                 | [√](https://github.com/zhengkangjie/ESM-AA)
[ESM-C](https://www.evolutionaryscale.ai/blog/esm-cambrian)           | 2024.12 | 300M, 600M, 6B | UniRef, MGnify, JGI         | ×
[ESM-GearNet](https://arxiv.org/abs/2203.06125)     | 2023.10 | -             | AlphaFoldDB                 | [√](https://github.com/DeepGraphLearning/ESM-GearNet)
[ESM-MSA-1b](https://www.biorxiv.org/content/10.1101/2021.02.12.430858v3)      | 2021.02 | 100M          | UniRef50                    | [√](https://github.com/facebookresearch/esm)
[IgBert](https://doi.org/10.1371/journal.pcbi.1012646)          | 2024.12 | 420M          | OAS                         | ×
[LM-GVP](https://www.nature.com/articles/s41598-022-10775-y)          | 2022.04 | -             | -                           | [√](https://github.com/aws-samples/lm-gvp)
[OntoProtein](https://arxiv.org/abs/2201.11147)     | 2022.06 | -             | ProteinKG25                 | [√](https://github.com/zjunlp/OntoProtein)
[PeTriBERT](https://www.biorxiv.org/content/10.1101/2022.08.10.503344v1)       | 2022.08 | 40M           | AlphaFoldDB                 | ×
[PMLM](https://arxiv.org/abs/2110.15527)            | 2021.10 | 87M-731M      | UniRef50, Pfam              | ×
[PRoBERTa](https://doi.org/10.1145/3388440.3412467)        | 2020.09 | 44M           | UniProtKB/Swiss-Prot        | [√](https://github.com/annambiar/PRoBERTa)
[PromptProtein](https://openreview.net/forum?id=XGagtiJ8XC)   | 2023.02 | 650M          | UniRef50, PDB               | [√](https://github.com/HICAI-ZJU/PromptProtein)
[ProteinBERT](https://academic.oup.com/bioinformatics/article/38/8/2102/6502274)     | 2022.03 | 16M           | UniRef90                    | [√](https://github.com/nadavbra/protein_bert)
[ProteinLM](https://arxiv.org/abs/2108.07435)       | 2021.12 | 200M/3B       | Pfam                        | [√](https://github.com/THUDM/ProteinLM)
[ProtFlash](https://www.cell.com/cell-reports-physical-science/fulltext/S2666-3864(23)00408-3)       | 2023.10 | 79M/174M      | UniRef50                    | [√](https://github.com/ISYSLAB-HUST/ProtFlash)
[ProtTrans](https://ieeexplore.ieee.org/abstract/document/9477085)       | 2021.07 | -             | UniRef, BFD                 | [√](https://github.com/agemagician/ProtTrans)
[SaProt](https://www.biorxiv.org/content/10.1101/2023.10.01.560349v5.abstract)          | 2023.10 | 650M          | AlphaFoldDB, PDB            | [√](https://github.com/westlake-repl/SaProt)
[TCR-BERT](https://www.biorxiv.org/content/10.1101/2021.11.18.469186v1)        | 2021.11 | 100M          | PIRD, VDJdb, TCRdb, murine LCMV GP33 | [√](https://github.com/wukevin/tcr-bert)


#### Decoder-only models

Model         | Time    | Params        | Pretraining Dataset          | Code
--------------|---------|---------------|------------------------------|-----------------------------------------
[DARK](https://www.biorxiv.org/content/10.1101/2022.01.27.478087v1)          | 2022.01 | 128M          | -                            | ×
[IgLM](https://www.biorxiv.org/content/10.1101/2021.12.13.472419v2.abstract)          | 2022.12 | 13M           | -                            | [√](https://github.com/Graylab/IgLM)
[PoET](https://proceedings.neurips.cc/paper_files/paper/2023/hash/f4366126eba252699b280e8f93c0ab2f-Abstract-Conference.html)          | 2023.11 | 57M-604M      | -                            | ×
[ProGen](https://arxiv.org/abs/2004.03497)        | 2020.03 | 1.2B          | UniParc, UniProtKB/Swiss-Prot | [√](https://github.com/salesforce/progen)
[ProGen2](https://www.cell.com/cell-systems/abstract/S2405-4712(23)00272-7?s=35)       | 2023.10 | 151M-6.4B     | UniRef90, BFD30, PDB         | [√](https://github.com/salesforce/progen)
[ProLLaMA](https://arxiv.org/html/2402.16445v1)      | 2024.02 | -             | UniRef50                     | [√](https://github.com/PKU-YuanGroup/ProLLaMA)
[ProtGPT2](https://www.biorxiv.org/content/10.1101/2022.03.09.483666v1.abstract)      | 2021.01 | 738M          | UniRef50                     | [√](https://huggingface.co/nferruz/ProtGPT2)
[RITA](https://arxiv.org/abs/2205.05789)          | 2022.05 | 1.2B          | UniRef100                    | ×
[ZymCTRL](https://www.mlsb.io/papers_2022/ZymCTRL_a_conditional_language_model_for_the_controllable_generation_of_artificial_enzymes.pdf)       | 2022.01 | 738M          | BRENDA                       | [√](https://huggingface.co/AI4PD/ZymCTRL)


#### Encoder-decoder models

Model         | Time    | Params       | Pretraining Dataset           | Code
--------------|---------|--------------|-------------------------------|----------------------------------------
[Ankh](https://arxiv.org/abs/2301.06568)          | 2023.01 | 450M/1.15B   | UniRef50                      | [Link](https://github.com/agemagician/Ankh)
[IgT5](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1012646)          | 2024.12 | 3B           | OAS                           | ×
[LM-Design](http://proceedings.mlr.press/v202/zheng23a.html)     | 2023.02 | 664M         | -                             | ×
[MSA-Augmenter](https://arxiv.org/abs/2306.01824?context=cs.LG) | 2023.06 | 260M         | UniRef50                      | [Link](https://github.com/lezhang7/MSA-Augmentor)
[ProSST](https://www.biorxiv.org/content/10.1101/2024.04.15.589672v2)        | 2024.05 | 110M         | AlphaFoldDB, CATH             | [Link](https://github.com/ai4protein/ProSST)
[ProstT5](https://www.biorxiv.org/content/10.1101/2023.07.23.550085v2.abstract)       | 2023.07 | 3B           | AlphaFoldDB, PDB              | [Link](https://github.com/mheinzinger/ProstT5)
[ProtT5](https://ieeexplore.ieee.org/abstract/document/9477085)        | 2022.06 | 3B/11B       | UniRef50, BFD                 | [Link](https://huggingface.co/Rostlab/prot_t5_xl_uniref50)
[pAbT5](https://arxiv.org/abs/2301.02748)         | 2023.10 | -            | OAS                           | ×
[Sapiens](https://www.tandfonline.com/doi/full/10.1080/19420862.2021.2020203)       | 2022.02 | 0.6M         | OAS                           | [Link](https://github.com/Merck/BioPhi)
[SS-pLM](https://www.biorxiv.org/content/10.1101/2023.08.04.551626v1.abstract)        | 2023.08 | 14.8M        | UniRef50                      | ×
[xTrimoPGLM](https://arxiv.org/abs/2401.06199)    | 2023.07 | 100B         | UniRef90, ColdFoldDB          | ×


## Datasets

Depending on whether annotations are available, datasets are divided into **pretraining datasets** and **benchmarks**.

- **Pretraining datasets** are typically unlabeled and used for self-supervised learning.
- **Benchmarks** are labeled and used for fine-tuning and evaluation.

The following tables summarize widely used resources in PLM research. Entries are listed alphabetically and grouped into sequence/structural pretraining data and structural/functional/other benchmarks.

### Pre-training datasets

#### Sequence datasets
Dataset | Time | Scale | Link
---- | ---- | ---- | ----
BFD[[1](https://www.nature.com/articles/s41586-021-03819-2),[2](https://www.nature.com/articles/s41592-019-0437-4),[3](https://www.nature.com/articles/s41467-018-04964-5)]|2021.07|2.5B|[√](https://bfd.mmseqs.com/)
[BRENDA](https://academic.oup.com/nar/article/30/1/47/1332638?login=false)|2002.01|-|[√](https://www.brenda-enzymes.org/)
[MGnify](https://academic.oup.com/nar/article/51/D1/D753/6880769?login=false)|2022.12|-|[√](https://www.ebi.ac.uk/metagenomics)
[Pfam](https://academic.oup.com/nar/article/34/suppl_1/D247/1133922?login=false)|2023.09|47M|[√](https://www.ebi.ac.uk/interpro/entry/pfam/)
[UniClust30](https://academic.oup.com/nar/article/45/D1/D170/2605730?login=false)|2016.11|-|[√](https://uniclust.mmseqs.com/)
[UniParc](https://academic.oup.com/nar/article/51/D1/D523/6835362?login=false)|2023.11|632M|[√](https://www.uniprot.org/uniparc?query=*)
[UniProtKB/Swiss-Prot](https://link.springer.com/protocol/10.1007/978-1-4939-3167-5_2)|2023.11|570K|[√](https://www.uniprot.org/uniprotkb?query=*)
[UniProtKB/TrEMBL](https://academic.oup.com/bioinformatics/article/15/3/219/317279?login=false)|2023.11|251M|[√](https://www.uniprot.org/uniprotkb?query=*)
UniRef50[[1](https://academic.oup.com/bioinformatics/article/23/10/1282/197795?login=false),[2](https://academic.oup.com/bioinformatics/article/31/6/926/214968?login=false)]|2023.11|53M|[√](https://www.uniprot.org/uniref?query=*)
UniRef90[[1](https://academic.oup.com/bioinformatics/article/23/10/1282/197795?login=false),[2](https://academic.oup.com/bioinformatics/article/31/6/926/214968?login=false)]|2023.11|150M|[√](https://www.uniprot.org/uniref?query=*)
UniRef100[[1](https://academic.oup.com/bioinformatics/article/23/10/1282/197795?login=false),[2](https://academic.oup.com/bioinformatics/article/31/6/926/214968?login=false)]|2023.11|314M|[√](https://www.uniprot.org/uniref?query=*)

#### Structural datasets
Dataset | Time | Scale | Link
---- | ---- | ---- | ----
AlphafoldDB[[1](https://www.nature.com/articles/s41586-021-03819-2),[2](https://academic.oup.com/nar/article/50/D1/D439/6430488?login=false)]|2021.11|200M|[√](https://alphafold.ebi.ac.uk/)
[PDB](https://academic.oup.com/nar/article/47/D1/D520/5144142?login=false)|2023.12|214K|[√](https://www.rcsb.org/)

### Benchmarks

#### Structural benchmarks
Dataset | Time | Scale | Link
---- | ---- | ---- | ----
[CAMEO](https://onlinelibrary.wiley.com/doi/full/10.1002/prot.26213)|-|-|[√](https://cameo3d.org/)
[CASP](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.26237)|-|-|[√](https://predictioncenter.org/)
[CATH](https://www.cell.com/structure/fulltext/S0969-2126(97)00260-8?cc\u003dy=)|2023.02|151M|[√](http://www.cathdb.info/)
[SCOP](https://academic.oup.com/nar/article/28/1/257/2384406?login=false)|2023.01|914K|[√](http://scop.berkeley.edu/)

#### Functional benchmarks
Dataset | Time | Scale | Link
---- | ---- | ---- | ----
[CAFA](https://www.biorxiv.org/content/10.1101/653105v1)|-|-|[√](https://biofunctionprediction.org/)
[EC](https://academic.oup.com/nar/article/37/suppl_1/D593/1000297?login=false)|2023.11|2.6M|[√](https://www.enzyme-database.org/)
[FLIP](https://www.biorxiv.org/content/10.1101/2021.11.09.467890v2.abstract)|2022.01|320K|[√](https://benchmark.protein.properties/)
[GO](https://www.nature.com/articles/ng0500_25)|2023.11|1.5M|[√](https://geneontology.org/)

#### Other benchmarks
Dataset | Time | Scale | Link
---- | ---- | ---- | ----
[PEER](https://proceedings.neurips.cc/paper_files/paper/2022/hash/e467582d42d9c13fa9603df16f31de6d-Abstract-Datasets_and_Benchmarks.html)|2022.11|390K|[√](https://github.com/DeepGraphLearning/PEER_Benchmark)
[ProteinGym](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10723403/)|2022.12|300K|[√](https://proteingym.org/)
[TAPE](https://proceedings.neurips.cc/paper_files/paper/2019/hash/37f65c068b7723cd7809ee2d31d7861c-Abstract.html)|2021.09|120K|[√](https://github.com/songlab-cal/tape)


## Tools

We also list commonly used protein research tools, grouped into sequence, structural, and other utilities. Entries are sorted alphabetically.

### Sequence tools
Tool | Link
---- | ----
BLAST|[√](https://blast.ncbi.nlm.nih.gov/Blast.cgi)
HHblits&HHfilter|[√](https://github.com/soedinglab/hh-suite)
MMseq2|[√](https://github.com/soedinglab/mmseqs2)

### Structural tools
Tool | Link
---- | ----
Foldseek|[√](https://search.foldseek.com/search)
PyMOL|[√](https://www.pymol.org/)
TM-align|[√](https://zhanggroup.org/TM-align/)

### Other tools
Tool | Link
---- | ----
t-SNE|[√](https://scikit-learn.org/0.18/preface.html)
Umap|[√](https://umap-learn.readthedocs.io/en/latest/)


