
# Data-independent Module-aware Pruning for Hierarchical Vision Transformers (**ICLR'24**)

[[`Paper`](https://openreview.net/pdf?id=7Ol6foUi1G)] | [[`BibTeX`](#citation)]


> **Abstract** *Hierarchical vision transformers (ViTs) have two advantages over conventional ViTs. First, hierarchical ViTs achieve linear computational complexity with respect to image size by local self-attention. Second, hierarchical ViTs create hierarchical feature maps by merging image patches in deeper layers for dense prediction. However, existing pruning methods ignore the unique properties of hierarchical ViTs and use the magnitude value as the weight importance. This approach leads to two main drawbacks. First, the "local" attention weights are compared at a "global" level, which may cause some "locally" important weights to be pruned due to their relatively small magnitude "globally". The second issue with magnitude pruning is that it fails to consider the distinct weight distributions of the network, which are essential for extracting coarse to fine-grained features at various hierarchical levels.*

> *To solve the aforementioned issues, we have developed a Data-independent Module-Aware Pruning method (DIMAP) to compress hierarchical ViTs. To ensure that "local" attention weights at different hierarchical levels are compared fairly in terms of their contribution, we treat them as a module and examine their contribution by analyzing their information distortion. Furthermore, we introduce a novel weight metric that is solely based on weights and does not require input images, thereby eliminating the dependence on the patch merging process. Our method validates its usefulness and strengths on Swin Transformers of different sizes on ImageNet-1k classification. Notably, the top-5 accuracy drop is only 0.07% when we remove 52.5% FLOPs and 52.7% parameters of Swin-B. When we reduce 33.2% FLOPs and 33.2% parameters of Swin-S, we can even achieve a 0.8% higher relative top-5 accuracy than the original model. Code is available at: https://github.com/he-y/Data-independent-Module-Aware-Pruning.*


##  Pruning Results  

| Model      | Pruning Ratio 1                                                                                    | Pruning Ratio 2                                                                    | Pruning Ratio 3                                                                    |
|------------|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| Swin-Base  | [DIMAP1](https://drive.google.com/drive/folders/10zZAO64IP5sPg5B76w_1qOpbZlbmspOX?usp=drive_link)  | [DIMAP2](https://drive.google.com/drive/folders/19uAoUqwBTLh4VaFUMPK20m61bU28h7N_) | [DIMAP3](https://drive.google.com/drive/folders/1P2rZe4zqjGN_pQB6EJ__5CyEGjo5wVjf) |
| Swin-Small | [DIMAP1](https://drive.google.com/drive/folders/18-UcXYl2aCfvX6YimfqYMgBKuk3bU1Ru)                 | [DIMAP2](https://drive.google.com/drive/folders/1KL_-9h8I-xqVXv12wI542ecWL66Tf-20) | [DIMAP3](https://drive.google.com/drive/folders/1tixTreFhtz5vS4blvRn2VSTiwvXvvlK8) |
| Swin-Tiny  | [DIMAP1](https://drive.google.com/drive/folders/1kfZB6pAdqZCXa5Zjbv60j-XPCbN7Bm3x)                 | [DIMAP2](https://drive.google.com/drive/folders/1Fvk557wEHpwXDLnsK2bg_0dqBsRlKwtR) | [DIMAP3](https://drive.google.com/drive/folders/1Bk8u9LkhIindwcqiVc8n_rEHde4CRJR4) |


 
## Citation
```
@inproceedings{he2024data,
  title={Data-independent Module-aware Pruning for Hierarchical Vision Transformers},
  author={He, Yang and Zhou, Joey Tianyi},
  booktitle={The Twelfth International Conference on Learning Representations},
  year={2024}
}
```
