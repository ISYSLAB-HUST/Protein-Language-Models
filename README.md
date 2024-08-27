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
Seq2vec|2017.04|-|RNN|-|×
UniRep|2018.01|1.2B|LSTM|UniProt|×
SeqVec|2020.03|-|CNN|UniProt|×
UDSMProt|2022.09|-|GPT|-|×

### Transformer-based models

#### Encoder-only models

Model | Time | #Parameters | Base model | Pretraining Dataset |Open-source
---- | ---- | ---- | ---- | ---- | ---- |
ESM-3|2023.06|98B|-|Uniref90|√
ESM-Fold|2022.11|300M|ESM-2|Uniref50|×
ESM-2|2022.07|8M-15B|RoBERTa|Uniref50,PDB|×
ESM-1b|2020.02|650M|RoBERTa|Uniref50|×
ESM-MSA-1b|2021.02|100M|ESM-1b|Uniref50|×
ESM-1v|2021.02|650M|ESM-1b|Uniref90|×
ESM-GearNet|2023.10|-|ESM-1b,GearNet|-|×
ProtTrans|2021.07|87M-731M|Trans.enc.|Uniref50|×
ProteinBERT|2022.02|16M|BERT|Uniref90|×
LM-GVP|2022.04|-|Trans.enc.|Uniref50|×
PrompProtein|2023.02|650M|RoBERTa|Uniref50,PDB|×
ProtFlash|2023.10|79M/174M|Trans.enc.|Uniref50|×
SaProt|2023.10|650M|BERT|-|×
ProteinNPT|2023.12|-|Trans.enc.|-|×
TAPE-BERT|2020.12|110M|BERT|Uniref50,Pfam|×
DistilleProtBert|2022.12|50M|ProtBert|Uniref50,Pfam|×
ProtBert|2020.12|1.1M/34.5M|BERT|Uniref50|×
BioBert|2019.02|110M|BERT|-|×
Bioseq-Bert|2022.05|110M|BERT|Uniprot|×
AminoBert|2023.03|110M|BERT|UniprotKB,Pfam|×
CLEAN|2024.02|100M|-|UniprotKB,PDB,Pfam|×
SignalP 6.0|2023.10|42M|-|UniprotKB|×
BlueBert|2020.04|110M/345M|BERT|-|×
SS-pLM|2023.08|14.8M|Transformer|Uniref50|×

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









