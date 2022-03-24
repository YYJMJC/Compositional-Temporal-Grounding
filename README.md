# Compositional Temporal Grounding with Structured Variational Cross-Graph Correspondence Learning

This is the newly proposed splits (i.e., Charades-CG and ActivityNet-CG) for the paper "Compositional Temporal Grounding with Structured Variational Cross-Graph Correspondence Learning" (**CVPR 2022**).

## Introduction

To systematically benchmark the progress of current methods on compositional generalization, we introduce a new task, Compositional Temporal Grounding. Our compositional temporal grounding task aims to evaluate how well a model can generalize to query sentences that contain novel compositions or novel words. We construct new splits of two prevailing datasets Charades-STA and ActivityNet Captions, named Charades-CG and ActivityNet-CG, respectively. Specifically, we define two new testing splits: Novel-Composition and Novel-Word. Each sentence in the novel-composition split contains one type of novel composition. We define the composition as novel composition if its constituents are both observed during training but their combination way is novel. Each sentence in the novel-word splits contains a novel word, which aims to test whether a model can infer the potential semantics of the unseen word based on the other learned composition components appearing in the context.

## Dataset Statistics
![](https://github.com/YYJMJC/Compositional-Temporal-Grounding/blob/main/statistics.png)
![](https://github.com/YYJMJC/Compositional-Temporal-Grounding/blob/main/distributions%20of%20novel%20composition%20types.png)

## Compared Methods
We evaluate the compositional generalizability of SOTA methods on the proposed Charades-CG and ActivityNetCG datasets. Specifically, these methods can be categorized into four groups:

1) Proposal-based methods:
* [CTRL](https://github.com/jiyanggao/TALL)
* [2D-TAN](https://github.com/microsoft/2D-TAN)

2) Proposal-free methods:
* [LGI](https://github.com/JonghwanMun/LGI4temporalgrounding)
* [VLSNet](https://github.com/IsaacChanghau/VSLNet)

3) RL-based method:
* [TSP-PRL](https://github.com/WuJie1010/TSP-PRL)

4) Weakly-supervised method:
* [WSSL](https://github.com/XgDuan/WSDEC)


For all methods, we use the public ofﬁcial implementations to get their compositional temporal grounding results. We train them on the training set and evaluate them on the test-trivial, novel-composition, and novel-word splits respectively. We use uniﬁed video and language features for more fair comparisons. Concretely, we use I3D features for the video in Charades-CG and C3D features for the videos in ActivityNet-CG. We use pretrained GloVe word vectors to initialize each word in the language queries.

## Citation
If you feel this project helpful to your research, please cite our work.
```
@inproceedings{li2022compositional,
      title={Compositional Temporal Grounding with Structured Variational Cross-Graph Correspondence Learning}, 
      author={Li, Juncheng and Xie, Junlin and Qian, Long and Zhu, Linchao and Tang, Siliang and Wu, Fei and Yang, Yi and Zhuang, Yueting and Wang, Xin Eric},
      booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
      year={2022}
}
```
