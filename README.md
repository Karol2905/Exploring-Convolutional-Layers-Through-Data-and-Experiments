
---

## Exploratory Data Analysis (EDA)

A minimal exploratory analysis is performed to understand the dataset structure.
This includes:

- Dataset size and class distribution
- Image dimensions and number of channels
- Visualization of sample images per class
- Basic preprocessing requirements

The goal of the EDA is to gain structural understanding of the data rather than
to perform exhaustive statistical analysis.

---

## Baseline Model

A non-convolutional baseline model is implemented using fully connected layers.
The input image is flattened before being passed through dense layers.

This model serves as a reference point and highlights the limitations of ignoring
spatial structure when working with image data.

---

## Convolutional Architecture

A convolutional neural network is designed from scratch with the goal of
introducing spatial inductive bias while keeping the architecture simple and
intentional.

Key design decisions include:

- Three convolutional layers
- 3×3 kernels
- Stride of 1 with same padding
- ReLU activation functions
- Max pooling for spatial downsampling

The architecture is intentionally shallow and avoids unnecessary complexity.

---

## Controlled Experiment

A controlled experiment is conducted to analyze the effect of kernel size in
convolutional layers. Models using 3×3 and 5×5 kernels are compared while keeping
all other architectural and training parameters fixed.

The experiment evaluates performance, stability, and model complexity to
understand trade-offs introduced by different kernel sizes.

---

## Interpretation and Reasoning

The results show that convolutional layers outperform the non-convolutional
baseline due to their ability to exploit spatial structure and inductive bias.

Rather than achieving better performance through increased complexity, the CNN
benefits from architectural choices that align with the nature of image data.

---

## Deployment with AWS SageMaker (To Be Completed)


---

## Requirements

- Python 3.x
- TensorFlow / Keras
- NumPy
- Matplotlib

---

