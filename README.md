# CNN Architectural Analysis – Facial Expression Recognition

## Problem Description

This project analyzes convolutional neural networks (CNNs as architectural
components rather than black-box models. The goal is to understand how specific
architectural choices influence learning behavior, performance, and
generalization when working with image-based data.

A facial expression recognition task is used as a case study to compare a
non-convolutional baseline model with a carefully designed convolutional
architecture. The emphasis is placed on architectural reasoning and controlled
experimentation, not on hyperparameter tuning.

---

## Dataset Description

The project uses the FER-2013 (Facial Expression Recognition) dataset, which
consists of grayscale images of human faces labeled with seven emotion classes:

- Angry  
- Disgust  
- Fear  
- Happy  
- Sad  
- Surprise  
- Neutral  

All images have a resolution of 48×48 pixels and contain a single face. The
dataset is organized into training and test directories, with one subdirectory
per class.

This dataset is well suited for convolutional neural networks because facial
expressions are defined by local spatial patterns such as edges, textures, and
facial components.

---

## Architecture Diagrams (Simple)

The convolutional architecture follows a simple and intentional design:

Input (48×48×1)  
→ Conv2D (3×3, 32 filters) + ReLU  
→ MaxPooling (2×2)  
→ Conv2D (3×3, 64 filters) + ReLU  
→ MaxPooling (2×2)  
→ Conv2D (3×3, 128 filters) + ReLU  
→ MaxPooling (2×2)  
→ Flatten  
→ Dense (128, ReLU)  
→ Dense (7, Softmax)

The architecture is intentionally shallow to focus on architectural principles
rather than depth or complexity.

---

## Experimental Results

Two main comparisons are performed:

1. **Baseline vs Convolutional Model**  
   The non-convolutional baseline (Flatten + Dense layers) achieves lower
   validation accuracy and shows limited generalization. In contrast, the CNN
   consistently achieves higher accuracy and more stable validation performance.

2. **Controlled Experiment on Kernel Size**  
   A controlled experiment compares 3×3 and 5×5 convolutional kernels while
   keeping all other parameters fixed. The model using 3×3 kernels achieves
   slightly better validation performance and requires fewer parameters, making
   it more efficient for this task.

Overall, convolutional models outperform the baseline with fewer parameters and
better generalization.

---

## Interpretation

Convolutional layers outperform the baseline because they preserve and exploit
the spatial structure of image data. By learning local patterns and reusing
weights across the image, CNNs build hierarchical representations that are well
aligned with the nature of facial expressions.

The inductive bias introduced by convolution assumes that nearby pixels are
related and that meaningful patterns can appear in multiple spatial locations.
This bias reduces the learning burden and improves generalization.

Convolutional architectures are not appropriate for problems without meaningful
spatial structure, such as tabular or symbolic data, where fully connected or
alternative architectures are more suitable.

---

