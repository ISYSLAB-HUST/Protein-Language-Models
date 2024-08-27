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
ProtVec|2016.05|-|skip-gram|UniProt|×
ProtVecX|-|-|-|-|×
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
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×
ProtVecX|-|-|-|-|×

#### Encoder-decoder models


## Datasets

### Pre-training datasets

Dataset | Time | Scale | Link
---- | ---- | ---- | ----
UniProtKB/Swiss-Prot|2023.11|570K|√

### Benchmarks


## Tools

Tool | Link
---- | ----
MMseq2|√









