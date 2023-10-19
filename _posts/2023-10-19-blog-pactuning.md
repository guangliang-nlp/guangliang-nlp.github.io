---
title: 'PAC-tuning: Fine-tuning Pretrained Language Models with PAC-driven Perturbed Gradient Descent'
date: 2023-10-19
permalink: /posts/2023/10/blog-pactuning/
tags:
  - Pretrained Language Models
  - Fine-tuning
  - PAC-Bayes Bound
  - PAC-Bayes Training
---

This post introduces our paper **PAC-tuning: Fine-tuning Pretrained Language Models with PAC-driven Perturbed Gradient Descent** accepted by EMNLP 23. Code is available at [https://github.com/MSU-NLP-CSS/PAC-tuning](https://github.com/MSU-NLP-CSS/PAC-tuning)

Abstract: 
======
Fine-tuning pretrained language models (PLMs) for downstream tasks is a large-scale optimization problem, in which the choice of the training algorithm critically determines how well the trained model can generalize to unseen test data, especially in the context of few-shot learning. To achieve good generalization performance and avoid overfitting, techniques such as data augmentation and pruning are often applied. However, adding these regularizations necessitates heavy tuning of the hyperparameters of optimization algorithms, such as the popular Adam optimizer. In this paper, we propose a two-stage fine-tuning method, PAC-tuning, to address this optimization challenge. First, based on PAC-Bayes training, PAC-tuning directly minimizes the PAC-Bayes generalization bound to learn proper parameter distribution variances. Second, PAC-tuning modifies the gradient by injecting the noise variances learned in the first stage into the model parameters during training, a variation of perturbed gradient descent (PGD). However, in the few-shot setting, minimizing the PAC-Bayes generalization bound of an overparameterized model, such as PLMs, and injecting noise into it is a nontrivial task. Our experimental results across 5 GLUE benchmark tasks demonstrate that our PAC-tuning framework successfully handles the challenges of fine-tuning tasks and outperforms strong baseline methods by a visible margin, further confirming the potential to apply PAC training for any other settings where the Adam optimizer is currently used for training.

You can have many headings
======

Aren't headings cool?
------
