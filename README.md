# Face-Classification-with-Neural-Networks


## Abstract 

This study addresses binary classification of faces into real and fake (GAN-generated). The goal is to build and evaluate neural network models capable of distinguishing authentic from synthetic faces with reliable accuracy for use in security, social media integrity, and content moderation.


## Problem Description 

Detecting fake faces, often produced by GANs, is challenging and high-stakes. Robust classification helps reduce misinformation and abuse while supporting trust and safety systems.


## Solution Strategy 

- Start with a small experimental subset of the dataset to validate pipelines and models.

- Apply fine-tuning on pretrained CNNs and train a Custom CNN for comparison.

- Use standard ML practice: preprocessing, EDA, k-fold validation, training, fine-tuning, evaluation, plus ANOVA for statistical significance across models.


## Data 

Dataset: 140K Real and Fake Faces (Kaggle)
A small sample was used for the initial implementation:

Total images: 400

Class balance: 200 real, 200 fake

Splits:

Train: 320 images (80%)

Validation: 40 images (10%)

Test: 40 images (10%)

Note: Final training, fine-tuning, and evaluation in this repo focus on the small subset due to compute constraints.


![Image 1](https://github.com/ChrisXioannou/Face-Classification-with-Neural-Networks/blob/main/Images/1.jpg)

![image 2](https://github.com/ChrisXioannou/Face-Classification-with-Neural-Networks/blob/main/Images/2.jpg)


## Models 

Five CNN approaches were evaluated:

Custom CNN

Xception

InceptionV3

DenseNet121

EfficientNetB7


## Results (Summary) 📊

Best: InceptionV3 (fine-tuned) — Accuracy: 90%, Loss: 0.3041

Xception and DenseNet121 — both at 77.5% accuracy, with DenseNet121 showing the lower loss

EfficientNetB7 improved with tuning but did not surpass the above

Custom CNN underperformed relative to pretrained models

Statistical test (ANOVA) on model accuracies:

F-statistic: 236.4000

p-value: 0.0000
Conclusion: Performance differences are statistically significant.

Final choice: InceptionV3 (fine-tuned) as the recommended model for this task.


## How to Use 

- Notebooks walk through training and evaluation on the small subset.

- Update dataset paths in the notebook to match your environment.

- Typical workflow: load data → choose model → train/fine-tune → evaluate → compare.



🤝 Contribute & Support

If this project helps you, star the repo.
PRs, issues, and feature requests are welcome.

