# Super-Resolution
Python implementation of Super-Resolution Neural Networks from papers:
* SRCNN - [Image Super-Resolution Using Deep Convolutional Networks](https://arxiv.org/abs/1501.00092)
* CARN - [Fast, Accurate, and Lightweight Super-Resolution with Cascading Residual Network](https://arxiv.org/abs/1803.08664)
* ESRT - [Transformer for Single Image Super-Resolution](https://arxiv.org/abs/2108.11084)

# Requirements

* python 3.12.3
* pytorch 2.4.1
* cuda 11.8

This is what I used, but some other versions might work too.

# Datasets
### Training:
* [T91](https://www.kaggle.com/datasets/ll01dm/t91-image-dataset) for SRCNN
* [DIV2K](https://www.kaggle.com/datasets/soumikrakshit/div2k-high-resolution-images) for CARN and ESRT

### Testing:
* [Set5 and Set14](https://www.kaggle.com/datasets/ll01dm/set-5-14-super-resolution-dataset)
* [BSD100](https://www.kaggle.com/datasets/asilva1691/bsd100)
* [Urban100](https://www.kaggle.com/datasets/harshraone/urban100)
* [Manga109](http://www.manga109.org/en/)

## Datasets folder structure

For all test datasets the structure is identical to the T91 dataset. If you don't have LR images they will be generated automatically.

```text
- Datasets
    - DIV2K
        - DIV2K_train_HR
            - 0001.png
            - 0002.png
            ...
        - DIV2K_train_LR_bicubic
            - X2
                - 0001x2.png
                - 0002x2.png
                ...
            - X3
            - X4
    - T91
        - T91_HR
            - t1.png
            - t2.png
            ...
        - T91_LR_bicubic
            - X2
                - t1x2.png
                - t2x2.png
                ...
            - X3
            - X4
    ...
```