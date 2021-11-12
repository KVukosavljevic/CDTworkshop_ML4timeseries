# CDT Workshop ML 4 time-series
### The Oxford EPSRC CDT in Health Data Science
HDS-M05: Module - Machine Learning for Time Series <br>
November 8 - 12, 2021 <br>

Course designed by: <br>
| Dr. Andrew Creagh      | Dr. Anshul Thakur | Dr. Davide Morelli | Prof. David Clifton
| :---: | :---: | :---: | :---: |
| <andrew.creagh@eng.ox.ac.uk>      | <anshul.thakur@eng.ox.ac.uk>   | davide.morelli@eng.ox.ac.uk  | <david.clifton@eng.ox.ac.uk> |


<img src="./img/oxford_eng_logo.png" width="500" height="150" />

The Institute of Biomedical Engineering, <br />
Department of Engineering Science,<br />
University of Oxford<br />
## Lab Overview
This repository aims to introduce the basics of applying machine learning (ML) to medical time-series data. In this module you will learn how ML for time-series is not immediately similar to traditional image-based or static modelling. You will learn the important pre-processing steps that are appropriate for time-series data, and how to frame the problem and task in time. This workshop will introduce fundamental time-series models, such as Autogresssive (AR) proceess, Markov Chains, and Hidden Markov Models (HMM), right through to Recurrent Neural Networks (RNNs) - staples of time-series data applied to healthcare problems. Later stages of this course cover advanced deep-learning based time-series models, such as Temporal Convolution Neural Networks (TCNN), an understanding of latent embeddings (such as with autoencoders, noisy autoencoders, variational autoencoders, etc.), as well as useful ML techniques, such as data augmentation and transfer leanring in medical time-series settings. <br>

## Lecture Materials
1. ML 4 time-series: Introduction to time-series analysis (lecture slides)
1. ML 4 time-series: Essential Methodology ([lecture slides](https://github.com/apcreagh/CDTworkshop_ML4timeseries/blob/MT2021/doc/CDT_HDS_ML4timeseries-methods_AC.pdf))
1. ML 4 time-series: Recurrent Neural Networks ([lecture slides](https://github.com/apcreagh/CDTworkshop_ML4timeseries/blob/MT2021/doc/CDT_HDS_ML4timeseries-RNN_AC.pdf))
1. ML 4 time-series: Advanced Recurrent Neural Networks ([lecture slides](https://github.com/apcreagh/CDTworkshop_ML4timeseries/blob/main/doc/CDT_HDS_ML4Timeseries-Advanced_RNN_AT.pdf))
3. ML 4 time-series: Transformations ([lecture slides](https://github.com/apcreagh/CDTworkshop_ML4timeseries/blob/main/doc/CDT_HDS_ML4Timeseries-Transforms_AT.pdf))
4. ML 4 time-series: Convolutional Neural Networks ([lecture slides](https://github.com/apcreagh/CDTworkshop_ML4timeseries/blob/MT2021/doc/CDT_HDS_ML4Timeseries-CNN_AC.pdf))
5. ML 4 time-series: Getting started with Gaussian processes (lecture slides)
6. ML 4 time-series: Advanced Gaussian processes (lecture slides)
7. ML 4 time-series: Introduction to Survival Analysis (lecture slides)
8. ML 4 time-series: Deep survival Analysis ([lecture slides](https://github.com/apcreagh/CDTworkshop_ML4timeseries/blob/main/doc/CDT_HDS_ML4Timeseries-Deep_survival_analysis_DM.pdf))

Further lecture materials can be found on
[canvas.ox.ac.uk](https://canvas.ox.ac.uk/courses/124779/pages/hds-m05-module-info-machine-learning-for-time-series)
## Data Access
The accompanying pre-processed data for this module can be downloaded via 
[canvas.ox.ac.uk](https://canvas.ox.ac.uk/courses/124779/pages/hds-m05-module-info-machine-learning-for-time-series)

## Setup instructions on the Virtual Machines
1. Load and initialize Anaconda. This needs to be done only once (you may not need to run this if you already see `(bash)` written in front of your prompt).

   ```bash
   module load Anaconda3
   conda init bash
   ```
   Exit and re-login so that the above takes effect.
3. Create an anaconda environment from the provided requirements YAML file: 
   ```bash
   conda env create -f ml4timeseries.yml
   ```
4. You are now ready to use the environment: 
   ```bash
   conda activate ml4timeseries
   ```
   In future logins, you only need to run this last command.

## How to run Jupyter notebooks remotely

1. In your remote machine, launch a Jupyter notebook with a specified port, e.g. 9000:
   ```bash
   jupyter-notebook --no-browser --port=9000
   ```
   This will output something like:
   ```bash
   To access the notebook, open this URL:
   http://localhost:9000/?token=
   b3ee74d492a6348430f3b74b52309060dcb754e7bf3d6ce4
   ```

1. On your local machine, perform port-forwarding, e.g. the following forwards the remote port 9000 to the local port 8888:
   ```bash
   ssh -N -f -L localhost:8888:localhost:9000 username@remote_address
   ```
   Note: You can use the same port numbers for both local and remote.

1. Finally, copy the URL from step 1. Then in your local machine, open
Chrome and paste the URL, but change the port to the local port (or do nothing else if you used the same port).
You should be able see the notebooks now.
