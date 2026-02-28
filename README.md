# SuperPredict: Ensemble Learning for Superconductor Critical Temperature (Tc) Estimation

**Author:** Sangam Patil 

## Project Overview

The accurate prediction of superconducting critical temperature (Tc) remains a pivotal challenge in condensed matter physics and materials informatics. This project develops a supervised machine learning model to predict the critical temperature at which a material becomes superconducting based on its physicochemical properties. By utilizing machine learning, this study aims to accelerate the discovery of new superconducting materials by quickly screening chemical spaces, providing a powerful alternative to time-consuming and expensive experimental determinations.

## Dataset

**Source:** The dataset is sourced from the UCI Machine Learning Repository.
**Size:** It comprises 21,263 samples.
**Features:** There are 81 numerical physicochemical features derived from the elemental properties of superconducting materials.
**Target Variable:** The target variable is `critical_temp` (Tc), which exhibits a right-skewed distribution indicating that high-Tc superconductors are comparatively rare.


## Methodology

### Exploratory Data Analysis (EDA) & Preprocessing

* Principal Component Analysis (PCA) revealed that 25 components capture 95% of the variance, indicating high feature redundancy.
* Robust preprocessing techniques, such as standard scaling or min-max normalization, were planned to handle physical variations and outliers without discarding legitimate data.


### Machine Learning Models Evaluated

The project involved applying and evaluating various regression architectures:
**Linear Models:** Linear Regression, Ridge Regression, and Lasso Regression.
**Non-Linear Models:** Polynomial Regression, Spline Regression, and Support Vector Regression (SVR).
**Tree-Based Models:** Random Forest, Extra Trees, and Gradient Boosting.
**Neural Networks:** Simple Feedforward Neural Network.


### Evaluation Metric

* The primary evaluation metric used is Root Mean Squared Error (RMSE).
* RMSE was selected because it penalizes larger prediction errors more heavily and maintains the same unit of measurement (Kelvin) as the target variable, enhancing interpretability.


## Key Results

**Best Performing Model:** The ExtraTrees ensemble demonstrated the best performance and generalization capability. It achieved a test RMSE of 9.0317 K, a Mean Absolute Error (MAE) of 4.9640 K, and an $R^{2}$ score of 0.9291.
**Abstract Claim:** The optimized gradient boosting model achieves a root mean squared error (RMSE) of 5.8 K, demonstrating superior performance over traditional theoretical approaches.
**Neural Networks:** The neural network model also demonstrated strong predictive performance with a test RMSE of 12.55 K and an $R^{2}$ score of 0.8632.
**Linear Models:** Conventional linear models demonstrated poor predictive performance (RMSE of approximately 20.97 K), highlighting that critical temperature lacks sufficient linear separability.


## Future Scope

**Feature Engineering:** Further dimensionality reduction techniques like autoencoders could capture latent structures and improve model robustness.
**Physics-Informed Modeling:** Incorporating features such as electron-phonon coupling estimates derived from Density Functional Theory (DFT) can enhance predictive accuracy.
**Advanced Architectures:** Exploring hybrid models (e.g., combining Extra Trees for feature selection with neural networks) or integrating Bayesian Deep Learning for uncertainty quantification.
