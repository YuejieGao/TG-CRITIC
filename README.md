# README:TG-CRITIC: A TIMBRE-GUIDED MODEL FOR REFERENCE-INDEPENDENT SINGING EVALUATION
Created by: Yuejie Gao

Affiliation: NetEase Cloud Music, China

Last edited on: 26th May 2023

Last edited by: Yuejie Gao

Partial data of paper submitted to ICASSP2023: [TG-CRITIC: A TIMBRE-GUIDED MODEL FOR REFERENCE-INDEPENDENT SINGING EVALUATION](https://arxiv.org/abs/2305.09127)
![Image text](https://raw.github.com/YuejieGao/repositpry/master/TG-CRITIC/POSTER.jpg)

## Contents
This consists of the following (all used for the paper above):
- Subjective ground-truths of over-all score on NUS48E and PESnQ-DS (groundtruthfiles.csv)
- Results of TG-CRITIC and other reference-independent algorithms in public dataset NUS48E (Algo_Label_on_NUS48E.csv)
- Results of TG-CRITIC and other reference-independent algorithms in public dataset PESnQ-DS (Algo_Label_on_PESnQ-DS.csv)

## Label Description
- The three levels of labeling in our dataset are determined by two dimensions: 
 - Awesome(A) - Use label 0 to indicate. Works with excellent execution and impressive voice quality; 
 - Mediocre(M) - Use label 1 to indicate. Works with good intonation, but with average expressiveness;
 - Inferior(I) - Use label 2 to indicate. Works with weak intonation or poor representation.

## Audio Access
- NUS48E:[The NUS Sung and Spoken Lyrics Corpus:A Quantitative Comparison of Singing and Speech](https://smcnus.comp.nus.edu.sg/archive/pdf/2012-2013/2013_05-Pub-NUS-48E.pdf) with [data](https://drive.google.com/drive/folders/12pP9uUl0HTVANU3IPLnumTJiRjPtVUMx)
- PESnQ-DS:[PESnQ_APSIPA2017](https://github.com/chitralekha18/PESnQ_APSIPA2017)
## Experimental Results

### Abation Study on YJ-900

Accuracy & Presicion & Recall

| Model        | Accuracy        | Pr-A            | Pr-M            | Pr-I            | Re-A       | Re-M       | Re-I       |
| ------------ | --------------- | --------------- | --------------- | --------------- | ---------- | ---------- | ---------- |
| TG-Critic-1S | 0.798           | 0.835           | 0.716           | 0.840           | 0.905      | 0.792      | 0.797      |
| TG-Critic-2S | **0.823** | **0.872** | **0.736** | 0.867           | 0.899      | **0.755** | 0.818      |
| CQT-Only     | 0.782           | 0.843           | 0.698           | 0.795           | 0.889      | 0.636      | **0.824** |
| TG-Simple    | 0.790           | 0.821           | 0.684           | **0.887** | **0.929** | 0.725      | 0.716      |

AUC of Precision-Recall Curve

| Model        | Macro-AUC  | A          | M          | I          |
| ------------ | ---------- | ---------- | ---------- | ---------- |
| TG-Critic-1S | 0.866      | 0.953      | 0.732      | 0.863      |
| TG-Critic-2S | **0.876** | 0.952      | **0.769** | **0.876** |
| CQT-Only     | 0.864      | 0.946      | 0.734      | 0.864      |
| TG-Simple    | 0.858      | **0.955** | 0.724      | 0.864      |

### Comparison with Previous Work

| Model                                                           | YJ-900 | PESnQ-DS<br />Accuracy | PESnQ-DS<br />PCC | NUS48E<br />Accuracy | NUS48E<br />PCC |
| --------------------------------------------------------------- | ------ | ---------------------- | ----------------- | -------------------- | --------------- |
| [Kuaishou](https://ieeexplore.ieee.org/abstract/document/8682665/) | 0.683  | 0.850                  | 0.858             | 0.688                | 0.497           |
| [NUS20](https://ieeexplore.ieee.org/abstract/document/9306350/)    | 0.763  | 0.850                  | 0.930             | 0.688                | 0.552           |
| [NUS21](https://ieeexplore.ieee.org/abstract/document/9689271)     | 0.784  | 0.850                  | 0.925             | 0.729                | 0.548           |
| TG-Critic-1S                                                    | 0.798  | 0.800                  | 0.927             | 0.729                | **0.671**       |
| TG-Critic-2S                                                    | **0.823**  | **0.950**                  | **0.933**             | **0.771**                | 0.631           |

## Citation

If you find this work is helpful in your research, please cite our work:

```
@inproceedings{sun2023tg,
  title={Tg-Critic: A Timbre-Guided Model For Reference-Independent Singing Evaluation},
  author={Sun, Xiaoheng and Gao, Yuejie and Lin, Hanyao and Liu, Huaping},
  booktitle={ICASSP 2023-2023 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)},
  pages={1--5},
  year={2023},
  organization={IEEE}
}
```


## Contact

- Yuejie Gao: gaoyuejie[at]corp[dot]netease[dot]com
- Xiaoheng Sun: sunxiaoheng[dot]corp[dot]netease[dot]com
- Hanyao Lin: 20210180095[at]fudan[dot]edu[dot]cn
