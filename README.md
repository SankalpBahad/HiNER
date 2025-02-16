<p align="center"><img src="cfilt-dark-vec.png" alt="Computation for Indian Language Technology Logo" width="150" height="150"/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="aisurrey.svg" alt="Surrey Institute for People-Centred AI Logo" width="250"/></p>

# HiNER - Hindi Named Entity Recognition Dataset

[![GitHub issues](https://img.shields.io/github/issues/cfiltnlp/HiNER?style=flat-square)](https://github.com/cfiltnlp/HiNER/issues)
[![GitHub forks](https://img.shields.io/github/forks/cfiltnlp/HiNER?style=flat-square)](https://github.com/cfiltnlp/HiNER/network)
[![GitHub stars](https://img.shields.io/github/stars/cfiltnlp/HiNER?style=flat-square)](https://github.com/cfiltnlp/HiNER/stargazers)
[![GitHub license](https://img.shields.io/github/license/cfiltnlp/HiNER?style=flat-square)](https://github.com/cfiltnlp/HiNER/blob/main/LICENSE)
[![Twitter Follow](https://img.shields.io/twitter/follow/cfiltnlp?color=1DA1F2&logo=twitter&style=flat-square)](https://twitter.com/cfiltnlp)
[![Twitter Follow](https://img.shields.io/twitter/follow/PeopleCentredAI?color=1DA1F2&logo=twitter&style=flat-square)](https://twitter.com/PeopleCentredAI)

## About

This repository contains the Hindi Named Entity Recognition dataset (HiNER) published at the Langauge Resources and Evaluation conference (LREC) in 2022. A pre-print via arXiv is available [here](https://arxiv.org/abs/2204.13743).

### Recent Updates
* Version 0.0.5: HiNER initial release

## Usage

You should have the 'datasets' packages installed to be able to use the :rocket: HuggingFace datasets repository. Please use the following command and install via pip:

```code
    pip install datasets
```

To use the original dataset with all the tags, please use:<br/>

```python
    from datasets import load_dataset
    hiner = load_dataset('cfilt/HiNER-original')
```

To use the collapsed dataset with only PER, LOC, and ORG tags, please use:<br/>

```python
    from datasets import load_dataset
    hiner = load_dataset('cfilt/HiNER-collapsed')
```
However, the CoNLL format dataset files can also be found on this Git repository under the [data](data/) folder.

## Model(s)

Our best performing models are hosted on the HuggingFace models repository

| Models | [`HiNER - Original`](https://huggingface.co/datasets/cfilt/HiNER-original) | [`HiNER - Collapsed`](https://huggingface.co/datasets/cfilt/HiNER-collapsed) | Description |
| --- | --- | --- | --- |
| [XLM-R<sub>large</sub>](https://huggingface.co/xlm-roberta-large) | [HiNER-Original-XLM-R-Large](https://huggingface.co/cfilt/HiNER-original-xlm-roberta-large)  | [HiNER-Collapsed-XLM-R-Large](https://huggingface.co/cfilt/HiNER-collapsed-xlm-roberta-large) | Fine-tuning on the XLM-R<sub>large</sub> multilingual language model |
| [MuRIL<sub>base</sub>](https://huggingface.co/google/muril-base-cased) | [HiNER-Original-MuRIL-Base](https://huggingface.co/cfilt/HiNER-original-muril-base-cased) | [HiNER-Collapsed-MuRIL-Base](https://huggingface.co/cfilt/HiNER-collapsed-muril-base-cased) | Fine-tuning on the MuRIL<sub>base</sub> multilingual language model |


## Maintainer(s)

[Diptesh Kanojia](https://dipteshkanojia.github.io)<br/>
[Rudra Murthy V](https://murthyrudra.github.io/)<br/>

## Citation

Murthy, R., Bhattacharjee, P., Sharnagat, R., Khatri, J., Kanojia, D. and Bhattacharyya, P., 2022. HiNER: A Large Hindi Named Entity Recognition Dataset. arXiv preprint arXiv:2204.13743.

### BiBTeX Citation
```latex
@InProceedings{murthy-EtAl:2022:LREC,
  author    = {Murthy, Rudra  and  Bhattacharjee, Pallab  and  Sharnagat, Rahul  and  Khatri, Jyotsana  and  Kanojia, Diptesh  and  Bhattacharyya, Pushpak},
  title     = {HiNER: A large Hindi Named Entity Recognition Dataset},
  booktitle      = {Proceedings of the Language Resources and Evaluation Conference},
  month          = {June},
  year           = {2022},
  address        = {Marseille, France},
  publisher      = {European Language Resources Association},
  pages     = {4467--4476},
  abstract  = {Named Entity Recognition (NER) is a foundational NLP task that aims to provide class labels like Person, Location, Organisation, Time, and Number to words in free text. Named Entities can also be multi-word expressions where the additional I-O-B annotation information helps label them during the NER annotation process. While English and European languages have considerable annotated data for the NER task, Indian languages lack on that front- both in terms of quantity and following annotation standards. This paper releases a significantly sized standard-abiding Hindi NER dataset containing 109,146 sentences and 2,220,856 tokens, annotated with 11 tags. We discuss the dataset statistics in all their essential detail and provide an in-depth analysis of the NER tag-set used with our data. The statistics of tag-set in our dataset shows a healthy per-tag distribution especially for prominent classes like Person, Location and Organisation. Since the proof of resource-effectiveness is in building models with the resource and testing the model on benchmark data and against the leader-board entries in shared tasks, we do the same with the aforesaid data. We use different language models to perform the sequence labelling task for NER and show the efficacy of our data by performing a comparative evaluation with models trained on another dataset available for the Hindi NER task. Our dataset helps achieve a weighted F1 score of 88.78 with all the tags and 92.22 when we collapse the tag-set, as discussed in the paper. To the best of our knowledge, no available dataset meets the standards of volume (amount) and variability (diversity), as far as Hindi NER is concerned. We fill this gap through this work, which we hope will significantly help NLP for Hindi. We release this dataset with our code and models for further research at https://github.com/cfiltnlp/HiNER},
  url       = {https://aclanthology.org/2022.lrec-1.475}
}
```
