# WorkloadEstimation
Codebase for Passive BCI Hackathon - Neuroergonomics Conference 2021 - Intra-Subject Inter-Session Transfer Learning for Workload Estimation
Competition Site - [Link](https://www.neuroergonomicsconference.um.ifi.lmu.de/pbci/)

# Data
Data & instructions available [here](https://zenodo.org/record/4917218#.YNGIVi3pODW)
15 subjects, 3 sessions (different workload levels)

First 2 sessions available with labelled dataset. 
Target - To predict workload class on 3rd session for each subject.

# Short Background
EEG signals are highly non-stationary and can drift in terms of amplitude and other features over time, even within a day for a particular user. So, there is a need for algorithms capable of inter-session transfer learning such that the calibration is minimized or eliminated for the next session.

# Methods
Ensembling of techniques using the fundamental properties of covariance matrices through Riemannian geometry and combined with unsupervised learning using an adaptive kernel for tangent space projection.

# Validation
Training on the second session gives better generalization and prediction on the first session data based on some preliminary runs, and so this was chosen as the measure of validating the performance of the algorithms.

# Results
Placed 4th
