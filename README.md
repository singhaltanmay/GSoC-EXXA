# GSoC-EXXA
This repo contains my submissions of all the three tasks for the project titled **"Foundation Models for Exoplanet Characterization"** by EXXA @ ML4SCI under GSoC'25. I have successfully completed all the three tasks with various approaches for all the tasks and have extensively prepared the notebooks which are well documented with proper markdown and clear code

#### Note : Since Model weights of some trained models cant be uploaded to git due to their size, I have placed a dummy file in place of them. Original model and dataset (specifically for third task) can be found through this google drive link **[here](https://drive.google.com/drive/folders/12geq5o1wHKxOkZR_NhsBvinh2wOu70WX?usp=sharing)**

---

## 1. General Task
Since this was a clustering task, the results are qualitative and well visualized in the notebook `exxa-general-task-final-submission.ipynb`. <br>
Two approaches are used in this task, Second one being more novel and physics-informed, yielding state-of-the-art results

---

## 2. Image-based Task
I performed thorough experimentation upon the protoplanetary disk dataset of ALMA that was provided to us and have discussed three major approaches which I find most suitable during my experimentations. Qualitative results are well visualized in notebook `exxa-image-based-task-final-submission.ipynb`. Quantitative results as per the metric given are as follows:

### Results Approach 1:
- **MSE : $0.00076$**
- **MS-SSIM : $0.93238$**

The trained model weights corresponding to this approach is uploaded on google drive link provided above which corresponds to dummy file `MAE_ViT_best.pth` in the models folder

### Results Approach 2:
- **MSE : $2.65 \times 10^{-6}$**
- **MS-SSIM : $0.99855$**

The trained model weights corresponding to this approach is uploaded on google drive link provided above which corresponds to dummy file `Conv_MAE_best.pth` in the models folder

### Results Approach 3:
- **MSE : $0.27384$**
- **MS-SSIM : $0.96518$**

The trained model weights are present in the models folder named `CustomAutoencoder_best.pth`

---

## 3. Sequence-based Task
Apart from the synthetic data generation, labelled real observational data was used to evaluate the the trained models. The observational data corresponds to NASA's Kepler mission Campaign 3. The labelled data used here was found on Kaggle **[here](https://www.kaggle.com/datasets/keplersmachines/kepler-labelled-time-series-data)** <br>
Synthetic data is visualized well in the notebook `exxa-sequential-task-final-submission.ipynb`. Various approaches for synthetic dataset generation are used such as:
- PyTransit
- SMOTE oversampling
- Augmenting observational data

Classifier trained was CNN-1d classifier, model weights can be found in the models folder named `CNN1d_dlassifier_best.pth`

### Results of the classifier:
- **ROC AUC Score : $0.99327$**
- **Accuracy : $98.974%$**




