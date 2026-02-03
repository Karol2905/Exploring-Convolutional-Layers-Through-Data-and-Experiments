
---

# 🐱🐶 Convolutional Neural Networks: Architectural Analysis on Cats vs Dogs Dataset

## Problem Description

This project analyzes convolutional neural networks (CNNs) as architectural components rather than black-box models.
The objective is to understand how convolutional layers introduce inductive bias and how architectural design choices influence learning performance, scalability, and interpretability.

To achieve this, we study a binary image classification problem and compare a non-convolutional baseline model with a convolutional architecture designed from scratch.

---

## Dataset Description

The **Cats and Dogs** dataset is used in this project. It consists of labeled RGB images belonging to two classes: *cats* and *dogs*. Each image represents a natural scene with varying backgrounds, lighting conditions, and object poses.

The dataset is publicly available on Kaggle and is structured into class-specific folders, which facilitates reproducible loading and labeling.

---

## Why This Dataset Is Appropriate for Convolutional Neural Networks

This dataset is particularly well suited for convolutional neural networks due to the following reasons:

* **Image-based data**: Each sample is a 2D spatial structure with three color channels (RGB), matching the assumptions of 2D convolutional layers.
* **Strong local spatial patterns**: The task depends on recognizing edges, textures, and shapes such as fur patterns, facial structures, and contours.
* **Translation invariance**: Relevant features can appear at different spatial locations within the image, making weight sharing and local receptive fields highly effective.
* **Clear comparison with non-convolutional models**: Flattening the images for a fully connected baseline destroys spatial relationships, highlighting the architectural advantage introduced by convolution.
* **Simplicity without triviality**: The binary classification task is simple enough to train on limited resources, yet complex enough to demonstrate the hierarchical feature learning of CNNs.

Overall, the Cats and Dogs dataset provides a clean and interpretable setting to analyze the inductive bias of convolutional layers and to study how architectural decisions affect learning outcomes.

---

## Scope and Focus

This project intentionally avoids complex architectures or extensive hyperparameter tuning.
The emphasis is placed on **architectural reasoning**, controlled experiments on convolutional layers, and clear interpretation of results rather than maximizing predictive performance.


