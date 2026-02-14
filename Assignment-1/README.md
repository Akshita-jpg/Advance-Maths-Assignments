Assignment 1

Learn Probability Density Functions using Roll-Number-Parameterized Non-Linear Model

Name: Akshita

Roll Number: 102303531

📌 Objective

The objective of this assignment is to learn Probability Density Functions (PDFs) by applying a roll-number-parameterized non-linear transformation to real-world air quality data and estimating the parameters of a Gaussian distribution.

📊 Dataset
**India Air Quality Dataset**

Source: https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data

Feature used for analysis:

- **NO₂ (Nitrogen Dioxide)**

🧮 Methodology

Step 1: Nonlinear Transformation

  z=x+ar​sin(br​x)
Where:

𝑎𝑟 = 0.05(𝑟 mod 7)

  ​

𝑏r = 0.3(r mod 5+1)

Step 2: PDF Estimation

𝑝^(𝑧) = 𝑐𝑒^(-𝜆(𝑧−𝜇)^2)

Parameters estimated:

μ = Mean of transformed data

λ = 1/(2σ²)

c = 1/√(2πσ²)

​

## 🛠 Technologies Used

- Python

- NumPy

- Pandas

- Matplotlib

- SciPy

- Google Colab

📈 Results

The transformed NO2 data follows an approximately Gaussian distribution.
