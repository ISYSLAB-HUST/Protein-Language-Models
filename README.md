# Protein-Language-Models

简介:...


## News

- 🌟 [2024/08] ...
- 🌟 [2024/09] ...

![Protein-Language-Models-Overview](https://github.com/shuxiang111/Protein-Language-Models/blob/c71da17722411fb364288d313198d37384f8049d/figures/overview.png)

This is the overview of our article.


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

### Non-transformer-based models

Model | Time | #Parameters | Base model | Pretraining Dataset |Open-source
---- | ---- | ---- | ---- | ---- | ---- |
[ProtVec](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0141287)|2015.11|-|Skip-gram|UniProtKB/Swiss-Prot|×
[ProtVecX](https://www.nature.com/articles/s41598-019-38746-w)|2019.03|-|ProtVec|UniProtKB/Swiss-Prot|×
[Seq2vec](https://www.sciencedirect.com/science/article/pii/S1567422320300806?via%3Dihub)|2020.09|-|CNN-LSTM|-|×
[UniRep](https://www.nature.com/articles/s41592-019-0598-1)|2019.10|-|mLSTM|-|[√](https://github.com/churchlab/UniRep)
[SeqVec](https://link.springer.com/article/10.1186/s12859-019-3220-8)|2019.12|93M|ELMo|UniRef50|×
[UDSMProt](https://academic.oup.com/bioinformatics/article/36/8/2401/5698270)|2020.01|-|AWD-LSTM|UniProtKB/Swiss-Prot|×

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
[ProtTrans](https://ieeexplore.ieee.org/abstract/document/9477085)|2021.07|-|BERT,Albert,Electra|UniRef,BFD|[√](https://github.com/agemagician/ProtTrans)
[ProteinBERT](https://academic.oup.com/bioinformatics/article/38/8/2102/6502274?login=false)|2022.03|16M|BERT|UniRef90|[√](https://github.com/nadavbra/protein_bert)
[LM-GVP](https://www.nature.com/articles/s41598-022-10775-y)|2022.04|-|Trans.enc.|Uniref50|[√](https://github.com/aws-samples/lm-gvp)
[PrompProtein](https://openreview.net/forum?id=XGagtiJ8XC)|2023.02|650M|RoBERTa|UniRef50,PDB|[√](https://github.com/HICAI-ZJU/PromptProtein)
[ProtFlash](https://www.cell.com/cell-reports-physical-science/fulltext/S2666-3864(23)00408-3)|2023.10|79M/174M|Trans.enc.|UniRef50|[√](https://github.com/ISYSLAB-HUST/ProtFlash)
[SaProt](https://www.biorxiv.org/content/10.1101/2023.10.01.560349v5.abstract)|2023.10|650M|BERT|-|[√](https://github.com/westlake-repl/SaProt)
[ProteinNPT](https://proceedings.neurips.cc/paper_files/paper/2023/hash/6a4d5d85f7a52f062d23d98d544a5578-Abstract-Conference.html)|2023.12|-|Trans.enc.|-|×
[TAPE-BERT](https://arxiv.org/abs/1906.08230)|2019.06|38M|BERT|Pfam|[√](https://github.com/songlab-cal/tape)
[DistilProtBert](https://academic.oup.com/bioinformatics/article/38/Supplement_2/ii95/6701995)|2022.09|230M|ProtBert|UniRef50|[√](https://github.com/yarongef/DistilProtBert)
[ProtBert](https://www.biorxiv.org/content/10.1101/2020.07.12.199554v3)|2020.07|420M|BERT|UniRef100|[√](https://huggingface.co/Rostlab/prot_bert)
[BioBert](https://academic.oup.com/bioinformatics/article/36/4/1234/5566506)|2019.09|110M|BERT|-|[√](https://github.com/dmis-lab/biobert)
[Bioseq-Bert](https://academic.oup.com/nar/article/49/22/e129/6377401?login=false)|2021.09|-|BERT|-|×
[AminoBert](https://www.nature.com/articles/s41587-022-01432-w)|2022.10|-|BERT|-|×
[CLEAN](https://www.science.org/doi/10.1126/science.adf2465)|2023.03|-|-|-|[√](https://github.com/tttianhao/CLEAN)
[SignalP 6.0](https://www.nature.com/articles/s41587-021-01156-3)|2022.01|-|BERT|UniRef100|[√](https://github.com/fteufel/signalp-6.0)
[BlueBert](https://arxiv.org/abs/1906.05474)|2019.06|-|BERT|-|[√](https://github.com/ncbi-nlp/bluebert)
[SS-pLM](https://www.biorxiv.org/content/10.1101/2023.08.04.551626v1.abstract)|2023.08|14.8M|Transformer|UniRef50|×

#### Decoder-only models

Model | Time | #Parameters | Base model | Pretraining Dataset |Open-source
---- | ---- | ---- | ---- | ---- | ---- |
ProGen|2020.03|1.2B|GPT|Uniparc SWISS|×
ProtGPT2|2021.01|738M|GPT|Uniref50|×
ZymCTRL|2022.01|738M|GPT|BRENDA|×
RITA|2022.05|1.2B|GPT|Uniref10|×
IgLM|2022.12|13M|GPT|-|×
LM-Design|2023.02|664M|GPT|-|×
ProGen2|2023.10|151M-6.4B|GPT|Uniref90,BFD30,PDB|×
PoET|2023.11|201M|GPT|-|×

#### Encoder-decoder models

Model | Time | #Parameters | Base model | Pretraining Dataset |Open-source
---- | ---- | ---- | ---- | ---- | ---- |
Fold2Seq|2021.01|-|Transformer|-|×
MSA-to-proteion transformer|2022.04|-|Transformer|-|×
MSA-Transformer|2021.07|110M|Transformer|Uniref50|×
ProstT5|2023.07|3B|T5|PDB|×
xTrimoPGLM|2023.07|100B|GLM|Uniref90,ColdFoldDB|×
pAbT5|2023.10|-|T5|-|×
Prot-T5|2022.06|30B|T5|Uniref50|×
AlphaFold2|2020.11|-|Transformer|Uniref30,Uniref90,PDB,BFD|×
AlphaFold3|2024.05|-|-|-|×
OntoProtein|2022.06|-|Transformer|ProteinKG25|×
Mansoor et al.|2021.09|100M|Transformer|-|×

## Datasets

### Pre-training datasets

Dataset | Time | Scale | Link
---- | ---- | ---- | ----
UniProtKB/Swiss-Prot|2023.11|570K|√
UniProtKB/TrEMBL|2023.11|251M|√
UniRef100|2023.11|251M|√
UniRef90|2023.11|314M|√
UniRef50|2023.11|632M|√
UniParc|2023.11|314M|√
UniClust30|-|-|√
Pfam|2023.09|47M|√
BFD|2021.07|2.5B|√
PDB|2023.12|214K|√
AlphafoldDB|2021.11|200M|√
BRENDA|-|-|√
MGnify|-|-|√

### Benchmarks

Dataset | Time | Scale | Link
---- | ---- | ---- | ----
TAPE|2021.09|120K|√
ProteinGym|2022.12|300K|√
CASP|2022.01|-|√
SCOP|2023.01|914K|√
CATH|2023.02|151M|√
EC|2023.11|2.6M|√
GO|2023.11|1.5M|√
CAMEO|-|-|√
Flip|2022.01|320K|√
PEER|2022.11|390K|√

## Tools

Tool | Link
---- | ----
MMseq2|[√](https://github.com/soedinglab/mmseqs2)
HHblits&HHfilter|[√](https://github.com/soedinglab/hh-suite)
Umap&t-SNE|[Umap](https://umap-learn.readthedocs.io/en/latest/)&[t-SNE](https://scikit-learn.org/0.18/preface.html)
PyMOL|[√](https://www.pymol.org/)
TM-align|[√](https://zhanggroup.org/TM-align/)
BLAST|[√](https://blast.ncbi.nlm.nih.gov/Blast.cgi)
Foldseek|[√](https://search.foldseek.com/search)









