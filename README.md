# Sandwich Batch Normalization

[![MIT licensed](https://img.shields.io/badge/license-MIT-brightgreen.svg)](LICENSE.md)

Code for [Sandwich Batch Normalization](Sandwich Batch Normalization).

## Introduction
We present Sandwich Batch Normalization (SaBN), an extremely easy improvement of Batch Normalization (BN) with only a few lines of code changes.

![method](imgs/architect.png)

We demonstrate the prevailing effectiveness of SaBN as a drop-in replacement in four tasks:
1. image generation,
2. neural architecture search,
3. adversarial training,
4. style transfer.

## Usage
Check each of them for more information:
1. [GAN](https://github.com/VITA-Group/Sandwich-Batch-Normalization/blob/main/GAN)
2. [NAS](https://github.com/VITA-Group/Sandwich-Batch-Normalization/blob/main/NAS)
3. [Adv](https://github.com/VITA-Group/Sandwich-Batch-Normalization/blob/main/Adv)
4. [NST](https://github.com/VITA-Group/Sandwich-Batch-Normalization/blob/main/NST)

## Results

### Conditional Image Generation
Using SaBN in conditional generation task enables an immediate performance boost, without any additional tricks.

Evaluation results on CIFAR-10:

|       Model      | Inception Score |      FID     |
|------------------|-----------------|--------------|
| AutoGAN          |       8.43      |        10.51 |
| BigGAN           |       8.91      |         8.57 |
| SNGAN            |       8.76      |        10.18 |
| **AutoGAN-SaBN** |   8.72 (+0.29)  |  9.11(−1.40) |
| **BigGAN-SaBN**  |   9.01(+0.10)   | 8.03 (−0.54) |
| **SNGAN-SaBN**   |   8.89 (+0.13)  |  8.97(−1.21) |

Visual results on ImageNet (128*128 resolution):

![GAN](imgs/sngan_imagenet_compare.png)

### Neural Architecture Search
Results on NAS-Bench-201:

CIFAR-100            |  ImageNet16-120
:-------------------------:|:-------------------------:
![CIFAR100](imgs/DARTS_e35_cifar100.png)  |  ![ImageNet](imgs/DARTS_e35_imagenet100.png)


### Adversarial Training

### Neural Style Transfer
Model with proposed SaAdaIN achieves lower style & content loss:

![style curves](imgs/style_curves.png)

The visual results:

![style images](imgs/style_image.png)


## Acknowledgement
1. NAS codebase from [NAS-Bench-201](https://github.com/D-X-Y/AutoDL-Projects/blob/main/docs/NAS-Bench-201.md).
2. NST codebase from [AdaIN](https://github.com/naoto0804/pytorch-AdaIN).


