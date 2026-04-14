# 🛹 Predicting Street League Skateboarding Outcomes

This project focuses on predicting the top 3 finishers in the 2022 Street League Skateboarding (SLS) Last Chance Qualifier (LCQ) using statistical modeling and simulation techniques.

The project was developed as part of a course in statistical learning and data analysis, and combines both **frequentist and Bayesian approaches** to model athlete performance.

---

## 📌 Problem Overview

In the SLS competition, each athlete performs:

* 2 runs
* 4 trick attempts

Each performance is scored between 0 and 1. The final score is computed as:

* The **best run score**
* Plus the **sum of the two best trick scores**

The goal is to build models that can **predict which athletes will place in the top 3**, based on historical competition data.

---

## 📊 Dataset

The dataset contains results from multiple SLS events during the 2022 season, including:

* Run scores (`run 1`, `run 2`)
* Trick scores (`trick 1`–`trick 4`)
* Athlete identifiers
* Competition metadata (location, event type, etc.)

---

## 🧠 Methodology

The project is divided into several key components:

### 1. Exploratory Data Analysis

* Distribution of trick scores
* Estimation of landing probabilities for each athlete

### 2. Trick Modeling

* Bernoulli model for trick success:

  * ( X_s \sim \text{Bernoulli}(\rho_s) )
* Conditional Beta distribution for successful tricks:

  * ( Y_s \mid X_s = 1 \sim \text{Beta}(\alpha_s, \beta_s) )

### 3. Run Score Modeling

* Logit transformation:

  * ( g(x) = \log\left(\frac{x}{1 - x}\right) )
* Joint modeling of runs using a Gaussian framework
* Parameter estimation for each athlete

### 4. Simulation

* Monte Carlo simulation of:

  * Run scores
  * Trick scores
  * Total scores
* Ranking athletes based on simulated outcomes

### 5. Bayesian Extension

* Hierarchical model for trick performance
* Posterior sampling for athlete-specific parameters
* Posterior predictive simulations

---

## 📈 Results

* Identification of athletes with the highest probability of winning
* Comparison between frequentist and Bayesian predictions
* Visualization of simulated score distributions using boxplots

---

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib / Seaborn
* Jupyter Notebook

---
