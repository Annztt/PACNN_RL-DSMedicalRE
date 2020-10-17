## Piecewise Attentive Convolutional Neural Network with Reinforcement Learning for Distant Supervised Medical Relation Extraction

This repository contains the source code, model file and dataset for the paper: **Piecewise Attentive Convolutional Neural Network with Reinforcement Learning for Distant Supervised Medical Relation Extraction**. Tiantian Zhu 1, Yang Qin 1, Baotian Hu 1,∗, Qingcai Chen 1,2,∗, Weihua Peng 3 and Buzhou Tang 1,2


## Overview

The paper proposes a novel method for distant supervised medical relation extraction that takes denoising work into account. We first propose the Piecewise Attentive Convolutional Neural Network (PACNN) to extract relations of biomedical sentences, which applies a filter attention mechanism and relies on multichannel word embeddings. To enhance the robustness of the system, a reinforcement learning algorithm is developed to redistribute the noisy data at denoising module. The method is applied to several biomedical relation extraction tasks, namely, for the prediction of may-prevent relation, may-treat relation, drug-drug interaction and protein-protein interaction. The proposed method achieves the best performance of the first three tasks comparing to state-of-the-art systems. Besides, for the last task, we evaluated on five public datasets and reached new SOTA performance on three of them. These results show the efficiency of the proposed method, since it can significantly improve the distant supervised medical relation extraction performance.

![overview](model.jpg)


## Requirements

This repo was tested on Python 3.6.10 and Tensorflow 1.14.0 The main requirements are:

- python = 3.6.10
- tensorflow-gpu = 1.14.0
- cuda version = 10.0

## Datasets

- [Treat](https://drive.google.com/file/d/1np2jpxZL96da5pRG7w9EcHGLWb9VkLbl/view?usp=sharing)
- [Prevent](https://drive.google.com/file/d/1f06PVfjOHceLs8_O_W8b_ArPDxi4ulds/view?usp=sharing)
- [Ppi](https://drive.google.com/file/d/1i5kZPosFa125gASrW-NFfLBsLpHsO7zi/view?usp=sharing)
- [Ddi](https://drive.google.com/file/d/1tadLJL_lDLcgtPMHIR86jmsrEGag9P9z/view?usp=sharing)

## Usage

1. **Get pre-trained word embedding file**

   Download pretrained word embedding files from  **[`medicine-embedding`](https://drive.google.com/file/d/1xUAF4dbTTO7Ou6y5oQmIU1syBUqCLGs3/view?usp=sharing)**. Then decompress it under `data/medicine/`. 
   
2. **Get state-of-the-art trained models**

   Download trained mdoel files from  **[`best models`](https://drive.google.com/file/d/1VcEi3t261g74pq5ewVLtiIgZllEy1zrh/view?usp=sharing)**. Then decompress it under root dir. Finally specify the model path in train.py
   
3. **Train data**

   Download Datasets and decompress it under `data/medicine/`，Finally specify the data path in train.py
   
4. **train model**

   ```shell
   python train.py data/medicine
   ```

5. **inference** 

    ```shell
   python inference.py
   ```
