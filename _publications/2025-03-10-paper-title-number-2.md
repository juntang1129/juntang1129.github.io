---
title: "[Proceeding] Graph-affiliated Unsupervised Segmentation Assisted Simple Neural Network"
collection: publications
category: conferences
permalink: /publication/2025-03-10-paper-title-number-2
excerpt: ''
date: 2025-03-10
venue: '[Proceeding] 2025 IEEE International Conference on Bioinformatics and Biomedicine (BIBM)'
paperurl: 'http://tang.qqgjyx.com/files/paper2.pdf'
citation: '<b>Juntang Wang</b>, Runkun Guo, Dongmian Zou, Shixin Xu, Xiawa Wang (2025). &quot;Graph-affiliated Unsupervised Segmentation Assisted Simple Neural Network.&quot; <i>2025 IEEE International Conference on Bioinformatics and Biomedicine (BIBM)</i>. 1(1).'
---

High-throughput 16S rRNA-seq data, complemented by detailed cultivation information, constitutes a critical resource in bacterial research with promising implications for biomedical applications such as fecal microbiota transplantation. However, the inherent high dimensionality and substantial costs associated with 16S rRNA-seq data constrain its full utility. In this paper, we introduce a novel approach—graph-affiliated unsupervised segmentation-assisted simple neural network (GASNN)—designed to analyze 16S rRNA-seq data efficiently. In a proof-of-concept application involving the prediction of cultivation media temperature, the GASNN model achieved significant performance enhancements over a traditional simple neural network (SNN). Further experiments across various tasks consistently demonstrated that GASNN improves the performance of SNN models. Nevertheless, a notable limitation of the proposed approach is that its benefits may diminish as the network architecture deepens, thereby impeding its ability to reveal the intrinsic manifold structure of the data.

![Figure 1: GASNN model architecture showing the graph-affiliated unsupervised segmentation component](../images/publications/gasnn_model_architecture.png)

![Figure 2a: Ablation study results on DSMZ temperature prediction task](../images/publications/gasnn_dsmz_temp_ablation.png)

![Figure 2b: Temperature regression performance comparison between GASNN and baseline models](../images/publications/gasnn_dsmz_temp_regression.png)

![Figure 3a: t-SNE visualization of MNIST feature embeddings](../images/publications/gasnn_mnist_tsne.png)

![Figure 3b: Confusion matrix showing classification performance on MNIST dataset](../images/publications/gasnn_mnist_confusion_matrix.png)