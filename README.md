# QEdatasetJaEn

## Introduction

This repository contains word-level translation quality estimation labels for both source language (Japanese) and target language (English) documents.

We manually assigned word-level quality labels, OK or BAD, to 1045 Japanese sentences from 18 source documents and corresponding English MT outputs of two systems, [TexTra](https://mt-auto-minhon-mlt.ucri.jgn-x.jp/) and [Google Translate](https://translate.google.com/). Note that the manually post-edited versions of the MT outputs were referred to during the annotation process.

The source, MT and PE texts were selected from the following dataset:
- Rei Miyata (2024) MTPEdocs. https://github.com/tntc-project/MTPEdocs

## Contents

- TexTra (Ja->En; GPMT-3.9_220930_nmt; obtained 2023-01-31)
  - st_tok_gap.txt (tokenized into characters; with GAP tags)
  - st_tok_nogap.txt (tokenized into characters; without GAP tags)
  - st_label_gap.txt (with GAP tags)
  - st_label_nogap.txt (without GAP tags)
  - mt_tok_nogap.txt (tokenized into words; without GAP tags)
  - mt_label_nogap.txt (without GAP tags)
- Google (Ja->En; obtained 2023-03-05)
  - st_tok_gap.txt (tokenized into characters; with GAP tags)
  - st_tok_nogap.txt (tokenized into characters; without GAP tags)
  - st_label_gap.txt (with GAP tags)
  - st_label_nogap.txt (without GAP tags)
  - mt_tok_nogap.txt (tokenized into words; without GAP tags)
  - mt_label_nogap.txt (without GAP tags)

For tokenization of MT texts, we used [spaCy](https://pypi.org/project/spacy/) (v.3.5.4) with the default settings and manually corrected a few parts of the results.

GAP tags are annotated as [g] in the files.

## License

![Creative Commons License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)

* Use and/or redistribution of this dataset is permitted under the conditions of [Creative Commons Attribution-NonCommercial-ShareAlike License 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## Acknowledgments

Construction of the dataset was supported by JSPS KAKENHI Grant Numbers [JP19H05660](https://kaken.nii.ac.jp/en/grant/KAKENHI-PROJECT-19H05660/) and [JP23K28378](https://kaken.nii.ac.jp/en/grant/KAKENHI-PROJECT-23K28378/).

## Author and Citation

Sayuka Shimada, the first author of the following paper, developed this resource, discussing with the co-authors. Please cite if you use this resource.

```
@inproceedings{nlp-2024-shimada,
  author    = {Sayuka Shimada and Daichi Yamaguchi and Rei Miyata and Atsushi Fujita and Tomoyuki Kajiwara and Satoshi Sato},
  title     = {Designing and Building a Dataset of {Japanese-to-English} Translation Quality Estimation to Support Pre-editing for Machine Translation [機械翻訳向け原文編集の支援に向けた日英翻訳品質推定データセットの設計と構築] (in Japanese).},
  booktitle = {Proceedings of the 30th Annual Meeting of the Association for Natural Language Processing (NLP 2024)},
  year      = {2024},
  address   = {Kobe, Japan},
  pages     = {845--850},
  url       = {https://www.anlp.jp/proceedings/annual_meeting/2024/pdf_dir/P3-15.pdf}
}
```
