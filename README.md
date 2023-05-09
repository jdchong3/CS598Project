# An Extensive Data Processing Pipeline for MIMIC-IV
This repository is an implementation of the paper [An Extensive Data Processing Pipeline for MIMIC-IV](https://proceedings.mlr.press/v193/gupta22a/gupta22a.pdf).

## Original Paper's Repository
I used the paper's repository as a skeleton to modify and replicate experiments:
https://github.com/healthylaife/MIMIC-IV-Data-Pipeline. 

## Dataset
MIMIC-IV v1.0 Dataset available at: https://physionet.org/content/mimiciv/1.0/.

You must become a credentialed user by completing the “CITI Data or Specimens Only Research” training and signing the data use agreement.

Download the dataset by downloading the files directly from the website, or using the following command:

```
wget -r -N -c -np --user [user] --ask-password https://physionet.org/files/mimiciv/1.0/
```

## Requirements
Dependencies:

```
import_ipynb==0.1.3
ipywidgets==7.5.1
Jinja2==2.11.2
matplotlib==3.2.2
numpy==1.18.5
pandas==1.0.5
scikit_learn==1.0.2
torch==1.6.0
tqdm==4.47.0
```

To install requirements:

```setup
pip install -r requirements.txt
```

## Code
The main code in [mainPipeline.ipynb](https://github.com/jdchong3/CS598Project/blob/main/mainPipeline.ipynb) is executed either in Jupyter Notebook or Google Colaboratory. Before data preprocessing begins, the notebook guides you through a series of steps to select hyperparameters used in the pipeline. Select from the choices and run each cell to preprocess the data.

## Hyperparameters
The following table provides the set of hyperparameters for each predictive task used to obtain the results in the next section.

![Hyperparameters](https://github.com/jdchong3/CS598Project/blob/main/images/Hyperparameters.png)

## Results
Using the hyperparameters mentioned above, run each of the 4 machine learning and 4 deep learning models to obtain AUROC and AUPRC values for ICU and non-ICU data on each predictive task: readmission, mortality, length of stay, and phenotype. Here is a table of results:

![Results](https://github.com/jdchong3/CS598Project/blob/main/images/Results.png)

## References
Mehak Gupta, Brennan Gallamoza, Nicolas Cutrona, Pranjal Dhakal, Raphael Poulain, and Rahmatollah Beheshti. 2022. An Extensive Data Processing Pipeline for MIMIC-IV. In Proceedings of the 2nd Machine Learning for Health symposium, volume 193 of Proceedings of Machine Learning Research, pages 311–325. PMLR.