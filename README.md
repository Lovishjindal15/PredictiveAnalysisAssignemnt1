# Predictive Analysis Assignment 1

 Learning Probability Density Function using Maximum Likelihood Estimation (MLE)



 Introduction

This assignment focuses on estimating the Probability Density Function (PDF) of real-world environmental data using **Maximum Likelihood Estimation (MLE)**. The dataset consists of nitrogen dioxide (NO₂) concentration values collected from air quality measurements. After appropriate preprocessing, the data is transformed and modeled using a **Gaussian (Normal) distribution**.

All data preprocessing, transformation, modeling, and analysis are performed using **Google Colab**.

---

 Dataset Description

* **File name:** `data.csv`
* **Selected attribute:** `no2` (Nitrogen Dioxide concentration)

 Preprocessing Steps

The following cleaning steps are applied to make the data suitable for statistical analysis:

1. Missing values are removed
2. Non-numeric entries are discarded
3. Only positive NO₂ values are retained

After preprocessing, the cleaned NO₂ data is used for further transformation and modeling.



 Methodology

 1. Roll Number Based Parameters

To ensure uniqueness of results for each student, two parameters are derived from the roll number:

* **aᵣ = 0.05 × (roll number mod 7)**
* **bᵣ = 0.3 × (roll number mod 5 + 1)**

These parameters control the non-linear transformation applied to the dataset.

---

 2. Data Transformation

Let the original NO₂ values be represented by **x**. A non-linear transformation is applied to obtain a new variable **z**:

**z = x + aᵣ · sin(bᵣ · x)**

This transformation slightly alters the original values while preserving the overall structure of the distribution, ensuring variability across different roll numbers.



 3. Assumed Probability Model

The transformed data **z** is assumed to follow a **Gaussian (Normal) distribution**. The probability density function (PDF) is defined as:

**f(z | μ, λ) = c · exp(−λ (z − μ)²)**

Where:

* **μ** is the mean of the distribution
* **λ** controls the spread (precision) of the distribution
* **c** is the normalization constant



 4. Parameter Estimation Using MLE

Maximum Likelihood Estimation (MLE) is used to estimate the unknown parameters of the Gaussian PDF.

* **Mean (μ):**

  μ = (1/N) Σ zᵢ

* **Variance (σ²):**

  σ² = (1/N) Σ (zᵢ − μ)²

* **Lambda (λ):**

  λ = 1 / (2σ²)

* **Normalization Constant (c):**

  c = √(λ / π)

These estimated values represent the best-fit parameters for the transformed NO₂ data under the Gaussian assumption.



 Tools and Libraries Used

* Google Colab
* Python
* NumPy
* Pandas
* Matplotlib / Seaborn (for visualization)



 Conclusion

This assignment demonstrates how Maximum Likelihood Estimation can be applied to real-world environmental data for probabilistic modeling. By transforming the data using roll-number-based parameters and fitting a Gaussian distribution, unique and statistically meaningful results are obtained for each student.



 Author

**Name:** Lovish
**Course:** Predictive Analysis
**Assignment:** 1
**Rollno**102303950

