# WorkloadEstimation

Intra-Subject Inter-Session Transfer Learning for 3-class Workload Estimation on EEG data.

Codebase for submission to Passive BCI Hackathon - Neuroergonomics Conference 2021

Competition Site - [Link](https://www.neuroergonomicsconference.um.ifi.lmu.de/pbci/)

# Data
Data & instructions available [here](https://zenodo.org/record/4917218#.YNGIVi3pODW)

15 subjects, 3 sessions - 3 different workload levels in each session presented in a pseudorandom manner

First 2 sessions available with labelled dataset. 
Target - To predict workload class on 3rd session for each subject.

# Short Background
EEG signals are highly non-stationary and can drift in terms of amplitude and other features over time, even within a day for a particular user. So, there is a need for algorithms capable of inter-session transfer learning such that the calibration is minimized or eliminated for the next session.

# Methods
Ensembling of techniques using the fundamental properties of covariance matrices through Riemannian geometry combined with unsupervised transfer learning using an adaptive kernel for tangent space projection.

The covariance is calculated using the oracle approximating shrunk (oas) estimator from the PyRiemann package

Model 1 – PyRiemann MDM Classifier with default parameters

Model 2 – Scikit-Learn Nu-Support Vector Classifier with default parameters, PyRiemann Tangent Space Projection with adaptive kernel activated

Model 3 –  XGB Classifier with n_estimators = 1500, max_depth = 15, learning_rate= 0.3, reg_lambda =5, PyRiemann Tangent Space Projection with adaptive kernel activated


# Validation
Training on the second session gives better generalization and prediction on the first session data based on some preliminary runs, and so this was chosen as the measure of validating the performance of the algorithms.
![image](https://user-images.githubusercontent.com/47829318/132094695-3905c7d6-0922-4655-906a-13356f5743b3.png)


# Results
Placed 4th with 46.3% accuracy (Within 2% of 3rd and 2nd placed models and 8% of top model)
