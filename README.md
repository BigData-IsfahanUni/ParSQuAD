<span align="center">
    <a href="https://www.kaggle.com/neginabadani/parsquad"><img alt="Kaggle" src="https://img.shields.io/static/v1?label=Kaggle&message=ParSQuAD&logo=Kaggle&color=20BEFF"/></a>
</span>

# ParSQuAD: Persian Question Answering Dataset based on Machine Translation of SQuAD 2.0
Recent developments in Question Answering (QA) have improved state-of-the-art results, and various datasets have been released for this task. Since substantial English training datasets are available for this task, the majority of works published are for English Question Answering. However, due to the lack of Persian datasets, less research has been done on the latter language, making comparisons difficult. We present the first Persian Question Answering Dataset (ParSQuAD) based on the machine translation of the SQuAD 2.0 dataset. Many errors have been discovered within the process of translating the dataset; therefore, two versions of ParSQuAD have been generated depending on whether these errors have been corrected manually or automatically. As a result, the first large-scale QA training resource for Persian has been generated. In addition, we trained three baseline models, i.e., BERT, ALBERT, and Multilingual-BERT (mBERT), on both versions of ParSQuAD. mBERT achieves scores of 56.66% and 52.86% for F1 score and exact match ratio respectively on the test set with the first version and scores of 70.84% and 67.73% respectively with the second version. This model obtained the best results out of the three on each version of ParSQuAD.
# Dataset
### Download
Both versions of the dataset are available for download from the [`Dataset`](https://github.com/BigData-IsfahanUni/ParSQuAD/tree/main/Dataset) directory. The statistics of the ParSQuAD are shown below:
| Version   | Split | No. of questions | No. of titles |
|-----------|-------|------------------|---------------|
| Manual    | Train | 18906            | 136           |
| Manual    | Dev   | 5726             | 35            |
| Automatic | Train | 64961            | 442           |
| Automatic | Dev   | 5599             | 35            |

# Evalution
In order to evaluate the quality of our dataset and compare it with the SQuAD 2.0 datatset, three QA models have been trained. The pre-trained BERT (ParsBERT for the translated dataset), ALBERT, and Multilingual-BERT (mBERT) models have been fine-tuned on both versions of the ParSQuAD dataset to generate our three final Question Answering models. We evaluate each model using two widely used automatic evaluation metrics *Exact Match* and *F1*.

| Dataset                | Model     | Exact Match | F1 measure |
|------------------------|-----------|-------------|------------|
| SQuAD 2.0              | BERT      | 72.74       | 75.86      |
| SQuAD 2.0              | ALBERT    | 78.98       | 82.15      |
| SQuAD 2.0              | mBERT     | 74.92       | 78.09      |
| ParSQuAD-manual        | ParsBERT  | 46.32       | 50.06      |
| ParSQuAD-manual        | ALBERT    | 48.11       | 51.66      |
| ParSQuAD-manual        | mBERT     | 52.86       | 56.66      |
| ParSQuAD-automatic     | ParsBERT  | 62.42       | 65.26      |
| ParSQuAD-automatic     | ALBERT    | 64.71       | 67.59      |
| **ParSQuAD-automatic** | **mBERT** | **67.73**   | **70.84**  |

# Citation
### Plain
N. Abadani, J. Mozafari, A. Fatemi, M. A. Nematbakhsh, and A. Kazemi, ‘ParSQuAD: Machine Translated SQuAD dataset for Persian Question Answering’, in 2021 7th International Conference on Web Research (ICWR), 2021, pp. 163–168. doi: 10.1109/ICWR51868.2021.9443126.

N. Abadani, J. Mozafari, A. Fatemi, M. Nematbakhsh, and A. Kazemi, ‘ParSQuAD: Persian Question Answering Dataset based on Machine Translation of SQuAD 2.0’, International Journal of Web Research, vol. 4, no. 1, Art. no. 1, 2021, doi: 10.22133/IJWR.2021.293313.1101.

### Bibtex
```bibtex
@INPROCEEDINGS{Abadani2021-zl,
  title           = "{ParSQuAD}: Machine Translated {SQuAD} dataset for Persian
                     Question Answering",
  booktitle       = "2021 7th International Conference on Web Research ({ICWR})",
  author          = "Abadani, Negin and Mozafari, Jamshid and Fatemi, Afsaneh
                     and Nematbakhsh, Mohammd Ali and Kazemi, Arefeh",
  publisher       = "IEEE",
  month           =  may,
  year            =  2021,
  conference      = "2021 7th International Conference on Web Research (ICWR)",
  location        = "Tehran, Iran"
}
```
```bibtex
@ARTICLE{Abadani_undated-pf,
  title   = "{ParSQuAD}: Persian Question Answering Dataset based on Machine
             Translation of {SQuAD} 2.0",
  author  = "Abadani, N and Mozafari, J and Fatemi, A and Nematbakhsh, M and
             Kazemi, A",
  journal = "International Journal of Web Research",
  volume  =  4,
  number  =  1
}
```
