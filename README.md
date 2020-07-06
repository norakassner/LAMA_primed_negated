# Negated and Misprimed Probes for Pretrained Language Models

LAMA (LAnguage Model Analysis) is a probe for analyzing facutal knowledge caputred by pretrained language models, see the
following paper:


```bibtex
@inproceedings{petroni2019language,
  title={Language Models as Knowledge Bases?},
  author={F. Petroni, T. Rockt{\"{a}}schel, A. H. Miller, P. Lewis, A. Bakhtin, Y. Wu and S. Riedel},
  booktitle={In: Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing (EMNLP), 2019},
  year={2019}
}
@article{Kassner2019NegatedLB,
  title={Negated LAMA: Birds cannot fly},
  author={Nora Kassner and Hinrich Sch{\"u}tze},
  journal={ArXiv},
  year={2019},
  volume={abs/1911.03343}
}
```

## 1. Download Scripts

    git clone https://github.com/facebookresearch/LAMA.git

```conda create -n lama37 -y python=3.7 && conda activate lama37
pip install -r requirements.txt```


### 2. Download the models

~55 GB on disk

Install spacy model
```bash
python3 -m spacy download en
```

Download the models
```bash
chmod +x download_models.sh
./download_models.sh
```

The script will create and populate a _pre-trained_language_models_ folder.
If you are interested in a particular model please edit the script.
