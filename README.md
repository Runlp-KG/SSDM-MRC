## 2022 ACL "Learning Disentangled Semantic Representations for Zero-Shot Cross-Lingual Transfer in Multilingual Machine Reading Comprehension"

## Introduction

The multilingual MRC model is based on multilingual Pre-trained Language Models (PLMs) equipped with a Siamese Semantic Disentanglement Model (SSDM) 
to explicitly transfer only semantic knowledge to the target language.

This repository contains two directories ```src``` and ```data```, the SSDM and MRC models code in ```src```, and all the train and test datasets in ```data```.

Track the latest work, we are still optimizing and adjusting, thanks to the following code source:

[disentangle-semantics-syntax](https://github.com/mingdachen/disentangle-semantics-syntax)

[multilingual-mrc-isdg](https://github.com/lxucs/multilingual-mrc-isdg)

[HuggingFace](https://huggingface.co/)

## Environment

- GPU       Quadro RTX 6000  24G
- python    3.7.9
- torch     1.7.1
- cuda      11.0

## Usage

1、Set the configurations of SSDM in ```config.py```，mainly to set output file, choice the type of PLMs and syntax loss (POS or STL).

2、Adjust number of epochs, learning rate, etc. in ```mrc_experiments.conf```

3、Run the training code and it will print the test results in three MRC datasets (XQuAD, MLQA and TyDiQA-GoldP).

```
python main.py
```
Moreover, SSDM and MRC can be trained separately, depending on the user's choice.

## Cite

@inproceedings{DBLP:conf/acl/WuWZXCZ022,<br>
  author       = {Linjuan Wu and
                  Shaojuan Wu and
                  Xiaowang Zhang and
                  Deyi Xiong and
                  Shizhan Chen and
                  Zhiqiang Zhuang and
                  Zhiyong Feng},<br>
  title        = {Learning Disentangled Semantic Representations for Zero-Shot Cross-Lingual
                  Transfer in Multilingual Machine Reading Comprehension},<br>
  booktitle    = {Proceedings of the 60th Annual Meeting of the Association for Computational
                  Linguistics (Volume 1: Long Papers)(ACL)},<br>
  pages        = {991--1000},<br>
  publisher    = {Association for Computational Linguistics},<br>
  url          = {https://doi.org/10.18653/v1/2022.acl-long.70},<br>
  doi          = {10.18653/V1/2022.ACL-LONG.70},<br>
  biburl       = {https://dblp.org/rec/conf/acl/WuWZXCZ022.bib},<br>
  bibsource    = {dblp computer science bibliography, https://dblp.org}<br>
}
