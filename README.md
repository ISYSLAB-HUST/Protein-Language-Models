# Protein-Language-Models

......(简介)

## News

- 🌟 [2024/09] ...
- 🌟 [2024/10] ...

## Overview

This is the overview of our article.

![Protein-Language-Models-Overview](https://github.com/shuxiang111/Protein-Language-Models/blob/c71da17722411fb364288d313198d37384f8049d/figures/overview.png)

## Contents

- [News](#news)
- [Contents](#contents)
- [Models](#models)
  - [Non\-transformer\-based models](#non-transformer-based-models)
  - [Transformer\-based models](#transformer-based-models)
    - [Encoder\-only models](#encoder-only-models)
    - [Decoder\-only models](#decoder-only-models)
    - [Encoder\-decoder models](#encoder-decoder-models)
- [Datasets](#datasets)
  - [Pre\-training datasets](#pre-training-datasets)
  - [Benchmarks](#benchmarks)
- [Tools](#tools)


## Models

We categorize protein models into two sections: Non-transformer-based models and Transformer-based models. The Transformer-based models are further divided into three parts: Encoder-only models, Decoder-only models, and Encoder-decoder models. In the following table, we provide related information on each model, including the paper link, release time, parameters, base model, pretraining dataset, and whether the model is open-source, along with the link to the open-source code for users to reference.

### Non-transformer-based models

Model | Time | #Parameters | Base model | Pretraining Dataset |Open-source
---- | ---- | ---- | ---- | ---- | ---- |
[Seq2vec](https://www.sciencedirect.com/science/article/pii/S1567422320300806?via%3Dihub)|2020.09|-|CNN-LSTM|-|×
[UDSMProt](https://academic.oup.com/bioinformatics/article/36/8/2401/5698270)|2020.01|-|AWD-LSTM|UniProtKB/Swiss-Prot|×
[SeqVec](https://link.springer.com/article/10.1186/s12859-019-3220-8)|2019.12|93M|ELMo|UniRef50|×
[UniRep](https://www.nature.com/articles/s41592-019-0598-1)|2019.10|-|mLSTM|-|[√](https://github.com/churchlab/UniRep)
[ProtVecX](https://www.nature.com/articles/s41598-019-38746-w)|2019.03|-|ProtVec|UniProtKB/Swiss-Prot|×
[ProtVec](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0141287)|2015.11|-|Skip-gram|UniProtKB/Swiss-Prot|×

### Transformer-based models

#### Encoder-only models

Model | Time | #Parameters | Base model | Pretraining Dataset |Open-source
---- | ---- | ---- | ---- | ---- | ---- |
[ESM-3](https://www.biorxiv.org/content/10.1101/2024.07.01.600583v1)|2024.07|98B|-|-|[√](https://github.com/evolutionaryscale/esm)
[ESM-Fold](https://www.biorxiv.org/content/10.1101/2022.07.20.500902v1)|2022.07|15B|ESM-2|UniRef50|[√](https://github.com/facebookresearch/esm)
[ESM-2](https://www.science.org/doi/abs/10.1126/science.ade2574)|2023.03|8M-15B|RoBERTa|UniRef50|[√](https://github.com/facebookresearch/esm)
[ESM-1b](https://www.pnas.org/doi/abs/10.1073/pnas.2016239118)|2020.02|650M|RoBERTa|UniRef50|[√](https://github.com/facebookresearch/esm)
[ESM-MSA-1b](http://proceedings.mlr.press/v139/rao21a.html?utm_source=miragenews&utm_medium=miragenews&utm_campaign=news)|2021.02|100M|ESM-1b|UniRef50|[√](https://github.com/facebookresearch/esm)
[ESM-1v](https://proceedings.neurips.cc/paper/2021/hash/f51338d736f95dd42427296047067694-Abstract.html)|2021.02|650M|ESM-1b|UniRef90|[√](https://github.com/facebookresearch/esm)
[ESM-GearNet](https://arxiv.org/abs/2303.06275)|2023.10|-|ESM-2|-|[√](https://github.com/DeepGraphLearning/ESM-GearNet)
[ProtTrans](https://ieeexplore.ieee.org/abstract/document/9477085)|2022.10|-|BERT,Albert,Electra|UniRef,BFD|[√](https://github.com/agemagician/ProtTrans)
[ProteinBERT](https://academic.oup.com/bioinformatics/article/38/8/2102/6502274?login=false)|2022.03|16M|BERT|UniRef90|[√](https://github.com/nadavbra/protein_bert)
[LM-GVP](https://www.nature.com/articles/s41598-022-10775-y)|2022.04|-|Trans.enc.|Uniref50|[√](https://github.com/aws-samples/lm-gvp)
[PrompProtein](https://openreview.net/forum?id=XGagtiJ8XC)|2023.02|650M|RoBERTa|UniRef50,PDB|[√](https://github.com/HICAI-ZJU/PromptProtein)
[ProtFlash](https://www.cell.com/cell-reports-physical-science/fulltext/S2666-3864(23)00408-3)|2023.10|79M/174M|Trans.enc.|UniRef50|[√](https://github.com/ISYSLAB-HUST/ProtFlash)
[SaProt](https://www.biorxiv.org/content/10.1101/2023.10.01.560349v5.abstract)|2023.10|650M|BERT|-|[√](https://github.com/westlake-repl/SaProt)
[ProteinNPT](https://proceedings.neurips.cc/paper_files/paper/2023/hash/6a4d5d85f7a52f062d23d98d544a5578-Abstract-Conference.html)|2023.12|-|Trans.enc.|-|×
[TAPE-BERT](https://arxiv.org/abs/1906.08230)|2019.06|38M|BERT|Pfam|[√](https://github.com/songlab-cal/tape)
[DistilProtBert](https://academic.oup.com/bioinformatics/article/38/Supplement_2/ii95/6701995)|2022.09|230M|ProtBert|UniRef50|[√](https://github.com/yarongef/DistilProtBert)
[ProtBert](https://ieeexplore.ieee.org/abstract/document/9477085)|2022.10|420M|BERT|UniRef100,BFD100|[√](https://huggingface.co/Rostlab/prot_bert)
[BioBert](https://academic.oup.com/bioinformatics/article/36/4/1234/5566506)|2019.09|110M|BERT|-|[√](https://github.com/dmis-lab/biobert)
[Bioseq-Bert](https://academic.oup.com/nar/article/49/22/e129/6377401?login=false)|2021.09|-|BERT|-|×
[AminoBert](https://www.nature.com/articles/s41587-022-01432-w)|2022.10|-|BERT|-|×
[CLEAN](https://www.science.org/doi/10.1126/science.adf2465)|2023.03|-|-|-|[√](https://github.com/tttianhao/CLEAN)
[SignalP 6.0](https://www.nature.com/articles/s41587-021-01156-3)|2022.01|-|BERT|UniRef100|[√](https://github.com/fteufel/signalp-6.0)
[BlueBert](https://arxiv.org/abs/1906.05474)|2019.06|-|BERT|-|[√](https://github.com/ncbi-nlp/bluebert)
[SS-pLM](https://www.biorxiv.org/content/10.1101/2023.08.04.551626v1.abstract)|2023.08|14.8M|Transformer|UniRef50|×
[Prot-T5](https://ieeexplore.ieee.org/abstract/document/9477085)|2022.10|3B/11B|T5|UniRef50,BFD|[√](https://huggingface.co/Rostlab)
[OntoProtein](https://arxiv.org/abs/2201.11147)|2022.06|-|BERT|ProteinKG25|[√](https://github.com/zjunlp/OntoProtein)

#### Decoder-only models

Model | Time | #Parameters | Base model | Pretraining Dataset |Open-source
---- | ---- | ---- | ---- | ---- | ---- |
[ProGen](https://arxiv.org/abs/2004.03497)|2020.03|1.2B|GPT|UniParc,UniProtKB/Swiss-Prot|[√](https://github.com/salesforce/progen)
[ProtGPT2](https://www.biorxiv.org/content/10.1101/2022.03.09.483666v1.abstract)|2021.01|738M|GPT|UniRef50|[√](https://github.com/TeletcheaLab/protGPT2)
[ZymCTRL](https://www.mlsb.io/papers_2022/ZymCTRL_a_conditional_language_model_for_the_controllable_generation_of_artificial_enzymes.pdf)|2022.01|738M|GPT|BRENDA|[√](https://huggingface.co/AI4PD/ZymCTRL)
[RITA](https://arxiv.org/abs/2205.05789)|2022.05|1.2B|GPT|UniRef10|×
[IgLM](https://www.biorxiv.org/content/10.1101/2021.12.13.472419v2.abstract)|2022.12|13M|GPT|-|[√](https://github.com/Graylab/IgLM)
[LM-Design](http://proceedings.mlr.press/v202/zheng23a.html)|2023.02|664M|GPT|-|×
[ProGen2](https://www.cell.com/cell-systems/abstract/S2405-4712(23)00272-7?s=35)|2023.10|151M-6.4B|GPT|UniRef90,BFD30,PDB|[√](https://github.com/salesforce/progen)
[PoET](https://proceedings.neurips.cc/paper_files/paper/2023/hash/f4366126eba252699b280e8f93c0ab2f-Abstract-Conference.html)|2023.11|201M|GPT|-|×

#### Encoder-decoder models

Model | Time | #Parameters | Base model | Pretraining Dataset |Open-source
---- | ---- | ---- | ---- | ---- | ---- |
[Fold2Seq](https://proceedings.mlr.press/v139/cao21a.html)|2021.01|-|Transformer|-|[√](https://github.com/IBM/fold2seq)
[MSA-to-proteion transformer](https://arxiv.org/abs/2204.01168)|2022.04|-|Transformer|-|×
[MSA-Transformer](http://proceedings.mlr.press/v139/rao21a.html?utm_source=miragenews&utm_medium=miragenews&utm_campaign=news)|2021.07|100M|Transformer|UniRef50|[√](https://github.com/rmrao/msa-transformer)
[ProstT5](https://www.biorxiv.org/content/10.1101/2023.07.23.550085v2.abstract)|2023.07|3B|T5|PDB|[√](https://github.com/mheinzinger/ProstT5)
[xTrimoPGLM](https://arxiv.org/abs/2401.06199)|2023.07|100B|GLM|UniRef90,ColdFoldDB|×
[pAbT5](https://arxiv.org/abs/2301.02748)|2023.10|-|T5|-|×
[AlphaFold2](https://www.nature.com/articles/s41586-021-03819-2)|2021.07|-|Transformer|Uniref30,Uniref90,UniProt,PDB,BFD,MGnify|[√](https://github.com/google-deepmind/alphafold)
[AlphaFold3](https://www.nature.com/articles/s41586-024-07487-w)|2024.05|-|-|-|×
[Mansoor et al.](https://www.biorxiv.org/content/10.1101/2021.09.01.458592v1.abstract)|2021.09|100M|ESM-1b|-|×

## Datasets

Protein datasets can be classified into two categories depending on whether they include annotations: pre-training datasets and benchmarks. Pre-training datasets are typically used for self-supervised pre-training as they lack labels, whereas benchmarks, which contain labeled data, are used for supervised fine-tuning or model evaluation. We provide the relevant papers and links for the pre-training datasets and benchmarks of the present popular protein language models in the following table.

### Pre-training datasets

Dataset | Time | Scale | Link
---- | ---- | ---- | ----
[UniProtKB/Swiss-Prot](https://link.springer.com/protocol/10.1007/978-1-4939-3167-5_2)|2023.11|570K|[√](https://www.uniprot.org/uniprotkb?query=*)
[UniProtKB/TrEMBL](https://academic.oup.com/bioinformatics/article/15/3/219/317279?login=false)|2023.11|251M|[√](https://www.uniprot.org/uniprotkb?query=*)
UniRef100[[1](https://academic.oup.com/bioinformatics/article/23/10/1282/197795?login=false),[2](https://academic.oup.com/bioinformatics/article/31/6/926/214968?login=false)]|2023.11|314M|[√](https://www.uniprot.org/uniref?query=*)
UniRef90[[1](https://academic.oup.com/bioinformatics/article/23/10/1282/197795?login=false),[2](https://academic.oup.com/bioinformatics/article/31/6/926/214968?login=false)]|2023.11|150M|[√](https://www.uniprot.org/uniref?query=*)
UniRef50[[1](https://academic.oup.com/bioinformatics/article/23/10/1282/197795?login=false),[2](https://academic.oup.com/bioinformatics/article/31/6/926/214968?login=false)]|2023.11|53M|[√](https://www.uniprot.org/uniref?query=*)
[UniParc](https://academic.oup.com/nar/article/51/D1/D523/6835362?login=false)|2023.11|632M|[√](https://www.uniprot.org/uniparc?query=*)
[UniClust30](https://academic.oup.com/nar/article/45/D1/D170/2605730?login=false)|2016.11|-|[√](https://uniclust.mmseqs.com/)
[Pfam](https://academic.oup.com/nar/article/34/suppl_1/D247/1133922?login=false)|2023.09|47M|[√](https://www.ebi.ac.uk/interpro/entry/pfam/)
BFD[[1](https://www.nature.com/articles/s41586-021-03819-2),[2](https://www.nature.com/articles/s41592-019-0437-4),[3](https://www.nature.com/articles/s41467-018-04964-5)]|2021.07|2.5B|[√](https://bfd.mmseqs.com/)
[PDB](https://academic.oup.com/nar/article/47/D1/D520/5144142?login=false)|2023.12|214K|[√](https://www.rcsb.org/)
AlphafoldDB[[1](https://www.nature.com/articles/s41586-021-03819-2),[2](https://academic.oup.com/nar/article/50/D1/D439/6430488?login=false)]|2021.11|200M|[√](https://alphafold.ebi.ac.uk/)
[BRENDA](https://academic.oup.com/nar/article/30/1/47/1332638?login=false)|2002.01|-|[√](https://www.brenda-enzymes.org/)
[MGnify](https://academic.oup.com/nar/article/51/D1/D753/6880769?login=false)|2022.12|-|[√](https://www.ebi.ac.uk/metagenomics)

### Benchmarks

Dataset | Time | Scale | Link
---- | ---- | ---- | ----
[TAPE](https://proceedings.neurips.cc/paper_files/paper/2019/hash/37f65c068b7723cd7809ee2d31d7861c-Abstract.html)|2021.09|120K|[√](https://github.com/songlab-cal/tape)
[ProteinGym](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10723403/)|2022.12|300K|[√](https://proteingym.org/)
[CASP](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.26237)|2022.01|-|[√](https://predictioncenter.org/)
[SCOP](https://academic.oup.com/nar/article/28/1/257/2384406?login=false)|2023.01|914K|[√](http://scop.berkeley.edu/)
[CATH](https://www.cell.com/structure/fulltext/S0969-2126(97)00260-8?cc\u003dy=)|2023.02|151M|[√](http://www.cathdb.info/)
[EC](https://academic.oup.com/nar/article/37/suppl_1/D593/1000297?login=false)|2023.11|2.6M|[√](https://www.enzyme-database.org/)
[GO](https://www.nature.com/articles/ng0500_25)|2023.11|1.5M|[√](https://geneontology.org/)
[CAMEO](https://onlinelibrary.wiley.com/doi/full/10.1002/prot.26213)|2021.08|-|[√](https://cameo3d.org/)
[Flip](https://www.biorxiv.org/content/10.1101/2021.11.09.467890v2.abstract)|2022.01|320K|[√](https://benchmark.protein.properties/)
[PEER](https://proceedings.neurips.cc/paper_files/paper/2022/hash/e467582d42d9c13fa9603df16f31de6d-Abstract-Datasets_and_Benchmarks.html)|2022.11|390K|[√](https://github.com/DeepGraphLearning/PEER_Benchmark)

## Tools

We provide links to commonly used protein tools in the following table for readers to use.

Tool | Link
---- | ----
BLAST|[√](https://blast.ncbi.nlm.nih.gov/Blast.cgi)
Foldseek|[√](https://search.foldseek.com/search)
HHblits&HHfilter|[√](https://github.com/soedinglab/hh-suite)
MMseq2|[√](https://github.com/soedinglab/mmseqs2)
PyMOL|[√](https://www.pymol.org/)
TM-align|[√](https://zhanggroup.org/TM-align/)
t-SNE|[√](https://scikit-learn.org/0.18/preface.html)
Umap|[√](https://umap-learn.readthedocs.io/en/latest/)



