# Assignment 2 – GAN Based PDF Learning

## 📌 Objective

The objective of this assignment is to learn an unknown probability density function (PDF) of a transformed NO₂ variable using a Generative Adversarial Network (GAN), without assuming any parametric distribution.

---

## 📊 Dataset

India Air Quality Dataset  
Feature used: NO₂ concentration

---

## 🔄 Step 1 – Nonlinear Transformation

Each NO₂ value (x) was transformed into:

z = x + a_r sin(b_r x)

Where:

a_r = 0.5 (r mod 7)  
b_r = 0.3 ((r mod 5) + 1)

r = 102303531

This transformation introduces roll-number-based controlled nonlinearity.

---

## 🧠 Step 2 – GAN Architecture

Since no analytical PDF was provided, a Generative Adversarial Network (GAN) was used to learn the distribution of z directly from data samples.

### Generator Network
- Linear (50 → 64)
- ReLU
- Linear (64 → 64)
- ReLU
- Linear (64 → 1)

### Discriminator Network
- Linear (1 → 64)
- LeakyReLU (0.2)
- Linear (64 → 64)
- LeakyReLU (0.2)
- Linear (64 → 1)
- Sigmoid

Loss Function: Binary Cross Entropy  
Optimizer: Adam (learning rate = 0.0002)  
Epochs: 80  

---

## 📈 Step 3 – PDF Approximation

After training:

- 10,000 samples were generated from the trained generator
- Histogram density estimation was used to approximate the learned probability density
- Generated distribution was compared with real transformed data

---

## 🔍 Observations

- The GAN successfully captured the main mode of the distribution.
- Training stabilized after several epochs.
- Slight deviations observed in tail regions.
- No Gaussian or parametric assumption was used.

---

## 🛠 Technologies Used

- Python
- PyTorch
- NumPy
- Matplotlib
- Google Colab

---


