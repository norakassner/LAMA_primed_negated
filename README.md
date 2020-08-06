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
@inproceedings{kassner-schutze-2020-negated,
    title = "Negated and Misprimed Probes for Pretrained Language Models: Birds Can Talk, But Cannot Fly",
    author = {Kassner, Nora  and
      Sch{\"u}tze, Hinrich},
    booktitle = "Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics",
    month = jul,
    year = "2020",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2020.acl-main.698"}
```

## 1. Download Scripts

    git clone https://github.com/facebookresearch/LAMA.git

```conda create -n lama37 -y python=3.7 && conda activate lama37
pip install -r requirements.txt```
```

## 2. Download the models

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

## 2. Negated LAMA

Download the data via Facebook:
```bash
wget https://dl.fbaipublicfiles.com/LAMA/negated_data.tar.gz
tar -xzvf negated_data.tar.gz
rm negated_data.tar.gz
```
Set the set the flag `use_negated_probes` in `scripts/run_experiments.py`.
## 3. Data mispriming

Can be downloaded here
